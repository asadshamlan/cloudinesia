---
layout: post
status: publish
published: true
title: 'Amazon S3: Kenali dan Gunakan Menurut Kebutuhan'
author: asadshamlan
excerpt: Amazon S3 di desain oleh Amazon Web Services untuk mendistribusikan data
  secara otomatis di 3 availability zone yang berbeda. Bagaimana menggunakan menurut
  kebutuhan?
wordpress_id: 2018
wordpress_url: http://cloudinesia.com/?p=2018
date: '2018-05-19 03:25:09 +0000'
date_gmt: '2018-05-19 03:25:09 +0000'
categories:
- Tekno
- Reviews
tags:
- Amazon
- Featured
- aws
- s3 storage
- durability
comments: []
tags: [featured]
image: assets/images/s3.png
---
<p>Merujuk kembali ke durabilitas serta availability yang tinggi, S3 adalah layanan penyimpanan berbasis objek dari Amazon Web Service yang paling diminati dan paling tinggi tingkat penggunaannya dibanding kompetitor baik sebagai metode penyimpanan data aplikasi maupun sebagai tempat pemrosesan data untuk analytics.</p>
<p>Amazon S3 (Simple Storage Service) mempunyai empat jenis layanan penyimpanan yang berbeda, di klasifikasikan menurut frekuensi penggunaan serta kebutuhan redundancy.</p>
<p><em><strong>S3 Standard</strong></em>: penyimpanan yang super durable tidak memiliki batas untuk upload dan download. Di desain untuk tidak ada downtime atau kehilangan file ketika ada kegagalan infrastruktur pada oihak Amazon.</p>
<p><em><strong>S3 Infrequent Accessed</strong></em>: penyimpanan super durable untuk objek atau data - data yang termasuk dalam kategori jarang digunakan. Pada waktu data dibutuhkan, tidak ada waktu khusus yang di berikan oleh pihak Amazon. Artinya, data retrieval berlangsung dalam hitungan menit. S3 IA cenderung lebih murah di bandingkan S3 standard namun anda di kenakan biaya pengambilan data (data retrieval).</p>
<p><em><strong>S3 One Zone:</strong></em> bersifat sama dengan yang lainnya, namun One Zone ditujukan untuk penyimpanan data - data yang termasuk dalam kategori tidak penting. Hal ini karena di bandingkan yang lainnya, S3 One Zone di desain hanya untuk menyimpan data dalam satu amazon availability zone.</p>
<p>Ya, mungkin pembaca akan bertanya, "Emang yang lain berapa availability zone?". Jawabannya, S3 di desain oleh Amazon Web Services untuk mendistribusikan data secara otomatis di 3 availability zone yang berbeda. Artinya, apabila s3 bucket anda ada di singapore, kemudian s3 infrastruktur di singapore mengalami kegagalan, data anda masih dapat di akses dari availability zones lainnya.</p>
<p>Tidak hanya itu, seperti kami pernah ulas disini, pihak Amazon Web Service mengklaim S3 memiliki 99.999999999% durability (11 kali 9).</p>
<blockquote><p>S3 di desain oleh Amazon Web Services untuk mendistribusikan data secara otomatis di 3 availability zone yang berbeda.</p></blockquote>
<p>Yang terakhir yaitu <em><strong>Amazon Glacier.</strong></em> Penyimpanan ini diperuntukkan secara spesifik untuk data archiving (arsip) yang jarang di gunakan serta dalam kategori data yang tidak kritikal dalam hal pengambilan data. Amazon Glacier memberikan kisaran waktu pengambilan data standar dalam waktu kurang lebih 3 - 5 jam. Jadi, kalau ada data - data arsip yang kita jarang gunakan, dan tidak dibutuhkan waktu terburu - buru untuk mengambilnya, maka Glacier adalah pilihan tepat. Dari segi biaya, Glacier lebih murah dari layanan S3 lainnya.</p>
