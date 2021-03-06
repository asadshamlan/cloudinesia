---
layout: post
status: publish
published: true
title: 'Android App Bundle: Aplikasi Android Jadi Lebih Slim'
author: asadshamlan
excerpt: Di hari pertama I/O, sesi developer keynote mengumumkan 3 hal penting tentang
  Android Development. Salah satunya tentang distribusi, yaitu Android App Bundle.
wordpress_id: 2006
wordpress_url: http://cloudinesia.com/?p=2006
date: '2018-05-09 04:32:59 +0000'
date_gmt: '2018-05-09 04:32:59 +0000'
categories:
- Tekno
- "#io18"
tags:
- Twitter
- google
- io18
- android
- android studio
comments: []
image: assets/images/appbundle.jpg
---
<p>Di hari pertama I/O, sesi developer keynote mengumumkan 3 hal penting tentang Android Development. Salah satunya tentang distribusi, yaitu Android App Bundle.</p>
<p>Google menyadari bahwa banyaknya jumlah library serta aset - aset digital yang di perlukan apps membuat ukuran apps membesar. Dan ini berbanding lurus dengan kesediaan pengguna untuk mendownload apps atau tidak. Artinya, semakin besar ukuran apps, presentase install akan mulai menurun.</p>
<p><img class="alignnone size-medium wp-image-2009" src="http://cloudinesia.com/wp-content/uploads/2018/05/3q3a2475-300x200.jpg" alt="" width="300" height="200" /></p>
<p><em>Photo: TechCrunch</em></p>
<p>Berdasarkan fakta di atas, Google - di I/O tahun ini - mengumumkan bahwa mereka memutuskan untuk mendesain ulang (re-architect) model pendistribusian aplikasi mereka untuk mencapai model yang mereka yakini akan mengatasi masalah pendistribusian yaitu Dynamic Delivery.</p>
<p><img class="alignnone size-medium wp-image-2010" src="http://cloudinesia.com/wp-content/uploads/2018/05/3q3a2477-300x200.jpg" alt="" width="300" height="200" /></p>
<p><em>Photo: TechCrunch.com</em></p>
<p>Dynamic Delivery Android App Bundle berbentuk distribusi modular, mampu untuk mendistribusikan 'resources' yang dibutuhkan saja. Di bandingkan dengan sekarang, pendistribusian dilakukan secara serentak. Contohnya, aplikasi berukuran 60MB akan di download secara langsung 60MB ke dalam storage.</p>
<p>Android App Bundle dibekali file metadata yang menjadi acuan sistem tentang resources yang ada di dalam App. Dan tidak perlu tambahan coding untuk menggunakan fitur ini karena per hari ini - seperti dilansir oleh Google - Android App Bundle sudah tersedia di IDE mereka. Fitur ini tersedia ketika kita berada di menu "generate APK". Sedangkan di play console, akan ada indikasi presentase ukuran yang dapat anda simpan dengan menggunakan Android App Bundle (setelah apk dan keystore di upload di play console ya guys).</p>
<p>Menariknya, Apps seperti linkedin dan twitter sudah mengadopsi Android App Bundle dan mereka berhasil mengurangi ukuran hingga 28%.</p>
<p>Karena sudah tersedia hari ini secara global, kenapa ngga coba guys?. Jangan lupa kasih tau kami ya!</p>
<p>Cheers!</p>
