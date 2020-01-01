---
layout: post
status: publish
published: true
title: Snapshot lebih simple dengan AWS Lifecycle Manager
author: asadshamlan
excerpt: Beberapa waktu lalu, pemilik akun AWS yang berada di regional Singapura mendapatkan
  satu menu baru di bawah Snapshots, yaitu Lifecycle Manager.
wordpress_id: 2100
wordpress_url: http://cloudinesia.com/?p=2100
date: '2018-10-25 08:44:01 +0000'
date_gmt: '2018-10-25 08:44:01 +0000'
categories:
- Uncategorized
- Featured
- Trending
- Tekno
tags:
- cloud computing
- cloud
- Amazon
- Featured
- aws
- snapshot
- lifecycle manager
comments: []
image: assets/images/lifecycle-2.png
---
<p>Beberapa waktu lalu, pemilik akun AWS yang berada di regional Singapura mendapatkan satu menu baru di bawah Elastic Block Store (EBS), yaitu Lifecycle Manager.</p>
<p>Mungkin setelah membaca ini, anda akan segera login untuk melihat apakah betul terdapat menu baru di konsol anda.</p>
<p>[caption id="attachment_2104" align="aligncenter" width="214"]<img class="size-full wp-image-2104" src="http://cloudinesia.com/wp-content/uploads/2018/10/lifecycle-manager-menu.png" alt="lifecycle manager menu" width="214" height="363" /> Lokasi menu Lifecycle Manager[/caption]</p>
<p>Update terbaru ini berasa kecil tapi sangat krusial dalam hal backup/cloning. Lifecycle Manager menawarkan layanan untuk pembuatan serta administrasi Snapshot secara otomatis.</p>
<p>Seperti sebelumnya (atau saat ini bagi yang belum menggunakan) anda harus membuat snapshot menggunakan script + AWS CLI atau menggunakan pre-defined template. Dengan Lifecycle Manager, anda sudah dapat mengatur  jam berapa Snapshot ingin dibuat, berapa kali snaoshot dibuat dalam sehari, serta berapa lama anda ingin menyimpan Snapshot tersebut (retention period).</p>
<p>Pengaturan dilakukan di dalam interface yang sangat simple serta mudah digunakan. Tentukan jam untuk pembuatan snapshot, berapa lama ingin disimpan, serta target instance menggunakan "Tag" (dapat berupa nama, id, atau tag yang lain). Dari sini juga dapat diketahui bahwa penggunaan resource tagging dalam konsol AWS sangat penting.</p>
<p>[caption id="attachment_2105" align="aligncenter" width="855"]<img class="size-full wp-image-2105" src="http://cloudinesia.com/wp-content/uploads/2018/10/Pengaturan-Lifecycle-Manager.png" alt="Pengaturan Lifecycle Manager" width="855" height="772" /> Pengaturan Lifecycle Manager[/caption]</p>
<p>Jadi, buat kalian yang belum mempunyai pembuatan snapshot secara otomatis di AWS environment-nya, Lifecycle manager sangat layak untuk dicoba. Untuk yang sudah, mungkin bisa jadi alternatif untuk menyederhanakan. Selamat mencoba!</p>
<p>Baca Juga: <a href="http://cloudinesia.com/amazon-s3-gunakan-menurut-kebutuhan/" target="_blank" rel="noopener">Amazon S3: Kenali dan Gunakan Menurut Kebutuhan</a></p>
