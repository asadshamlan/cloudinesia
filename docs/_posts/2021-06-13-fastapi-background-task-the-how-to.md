---
layout: post
status: publish
title: 'FastAPI Background Task: The How To!'
author: asadshamlan
excerpt: 'With the increasing tractions to web framework like Flask and Django, Python
  is becoming more popular for web development projects choice beside Machine Learning
  projects. '
wordpress_id: 
wordpress_url: ''
date: 2021-06-13 12:06:00 +0800
date_gmt: 2021-06-13 12:06:00 +0800
categories:
- Programming
tags:
- Computer Vision
- Azure
- BackgroundTask
- Python
- FastAPI
comments: []
image: assets/images/fastapi.png

---
With the increasing tractions to web framework like Flask and Django, Python is becoming more popular for web development projects choice beside Machine Learning projects. Although, there are several other Python Framework options to be considered. And one of them is even released quite recent.

The new member in town dubbed as "modern, fast (high-performance), web framework for building APIs" is called [FastAPI](https://fastapi.tiangolo.com/ "FastAPI") authored by Sebastián Ramírez. FastAPI has several key metrics other than **fast** and **easy to code**. One of them is **Standards-based**. It is based on the open standards for APIs: [OpenAPI](https://github.com/OAI/OpenAPI-Specification)  and [JSON Schema](https://json-schema.org/).

I have been using this in few of my work in automating some infrastructure related projects. And I can say that learning FastAPI is even easier than Flask. Also because of [type hints](https://fastapi.tiangolo.com/python-types/), you will feel the breeze of higher accuracy in code completion while you type. Quoting an example from its docs:

    def get_full_name(first_name: str, last_name: str):
        full_name = first_name.title() + " " + last_name.title()
        return full_name
    
    print(get_full_name("john", "doe"))	

And while trying to continue using it for other project and refer to the docs for help, I found out another interesting feature which is called [Background Task](https://fastapi.tiangolo.com/tutorial/background-tasks/). Background Task is definitely what you need when you need to perform some non-time-critical operation. In a way, it adopts the asynchronous way of handling a task, in a slightly different manner. You return a response containing acknowledgement and then perform the operation in the background.Certain scenarios from the docs are as follow:

* Sending an email notification
* Processing data

However, this allows much more than that. 

In my case for instance, I've built a Blob Trigger-based function in Azure that takes images from user and generate image information/metadata using Azure Computer Vision. The information generated from Computer Vision is then parsed and processed in JSON format and committed into CosmosDB container. 

Now, the one requirement that I need is to be able to duplicate the blob to different container and set the blob tier as Archive. This is definitely not a time-critical operation. I can basically let it runs even in the next few hours. And I probably can just build one more function to handle that, but do I need to? Not anymore. Background Task came to the rescue:

    def duplicate_blob(blobName: str, blobTier=""):
    	# some operations here
    	# copy blob to different container
        # set tier to Archive
    	
    
    @app.post("/uploadfiles/")
    async def create_upload_files(request: Request, files: List[UploadFile] = File(...), background_tasks: BackgroundTasks):
        for uploaded_file in files:
            read_file = uploaded_file.file.read()
            blob_client = blob_service_client.get_blob_client(container_name, uploaded_file.filename)
            uploading = blob_client.upload_blob(read_file, blob_type="BlockBlob", overwrite=True)
            logging.info(uploading)
        background_tasks.add_task(duplicate_blob, uploaded_file.filename, blobTier="Archive")
        return templates.TemplateResponse("uploaded.html", context={"request":request, 
        									"files":[fname.filename for fname in files]})

Line #8 from the code above shows the background task usage taking function duplicate_blob to be executed with required arguments which is the blobName and blobTier.

Saved me from building one more function (read: $$$$). 