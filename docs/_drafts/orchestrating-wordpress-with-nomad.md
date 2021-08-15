---
layout: post
status: publish
title: Orchestrating Wordpress with Nomad
author: asadshamlan
excerpt: ''
wordpress_id: 
wordpress_url: ''
date: 2021-08-15 11:00:00 +0800
date_gmt: 2021-08-15 11:00:00 +0800
categories:
- Containerization
- Featured
tags:
- wordpress
- orchestration
- container
- hashicorp
- nomad
comments: []
image: assets/images/nomad-img.png

---
This is long overdue to be written and documented here. I've played around with [Nomad](https://www.nomadproject.io/) for quite some time but haven't had the time to write about it. 

Nomad is a workload orchestration platform born out of HashiCorp. Workload as a choice of word is intended as Nomad is capable to also orchestrate non-containerized workloads, such as Java, raw_exec, etc. In Nomad's term, this is called 'task driver' (you can refer to the list of driver [here](https://www.nomadproject.io/docs/drivers). Nomad is a single binary installation and can be configured as a client or server. To read further, HashiCorp did a great job documenting the architecture overview [here](https://www.nomadproject.io/docs/internals/architecture).

Like many other X-as-a-code tools, Nomad is based out of _desired state_ specified within the Job. [Job Specifications](https://www.nomadproject.io/docs/job-specification) are declared in a file called Nomad job file in which group and tasks are written. Example of a job file below:

    job "consul" {
      datacenters = ["dc1"]
      group "consul" {
        count = 1
        task "consul" {
          driver = "raw_exec"
                
          config {
            command = "consul"
            args    = ["agent", "-dev", "-client=0.0.0.0"]
          }
          artifact {
            source = "https://releases.hashicorp.com/consul/1.7.2/consul_1.7.2_linux_amd64.zip"
          }
        }
      }
    }

Group is nothing more than a collection containing series of tasks expected to be placed in the same Nomad client in a cluster setup. Whereas task is the actual unit of work that will run the workload as per specification. Referring to the job file above, means you are expecting a single job that will run Consul (another HashiCorp's great product) downloaded from the listed URL in one client with the specified command. Once you submitted, Nomad has no choice other than allocating the job to one of the available clients.