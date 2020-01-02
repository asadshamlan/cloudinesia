---
layout: post
status: publish
published: true
title: 'Opini: Cloud vs On Premise'
author: asadshamlan
excerpt: Beberapa dari pembaca - apalagi yang sudah berkecimpung dalam implementasi
  cloud computing - akan setuju dengan saya bahwa cloud=agile. Thats it!
wordpress_id: 1884
wordpress_url: http://localhost/wordpress/?p=1884
date: '2018-05-04 09:33:10 +0000'
date_gmt: '2018-05-04 09:33:10 +0000'
categories:
- Trending
- Tekno
- Opini
tags:
- iaas
- Featured
- opini
- cloud vs onprem
comments: []
tags: [featured]
image: assets/images/motherboard.jpg
---
<p>Seiring pesatnya perkembangan pengadopsian cloud computing, pertanyaan seputar perbandingan ini cukup banyak dilontarkan oleh para praktisi IT atau yang sebidang dengannya. Pasalnya, perkembangan yang pesat terkadang menimbulkan ketidaknyamanan bagi para fanatis on prem (baca: on premise system). Fenomena tersebut tidak hanya terjadi dalam bidang IT khususnya cloud computing, pada umumnya perubahan memang tidak pernah nyaman. Tetapi bicara tentang perubahan atau perkembangan pesat yang di alami oleh praktisi IT dalam rangka perlunya transformasi bisa dibilang cukup over. Hal ini disebabkan prinsip dari cloud computing sendiri yang notabene bersifat "Agile" (baca: lincah).</p>
<p>Beberapa dari pembaca - apalagi yang sudah berkecimpung dalam implementasi cloud computing - akan setuju dengan saya bahwa cloud=agile. Thats it!</p>
<p>Yes, memang cloud seharusnya menawarkan agility dan sebagai pengguna cloud sendiri (atau at least calon pengguna) harus mempertimbangkan agility. Ada beberapa "major player" penyedia layanan cloud services seperti <a href="https://aws.amazon.com/">Amazon Web Services</a>, <a href="https://azure.microsoft.com/en-us/">Microsoft Azure</a>, <a href="https://cloud.google.com/">Google Cloud Platform</a> (aplikasi  kebanggan kita GOJEK adalah pioneer pengadopsi GCP pertama di Indonesia loh!) , serta <a href="https://www.alibabacloud.com/">Alibabacloud</a> yang dapat kita pertimbangkan yang menurut kami lebih dari cukup untuk menawarkan agility.</p>
<p>Ada beberapa faktor penting yang kami rasa menjadi pemberat di Cloud dibandingkan On Premis. Kalau kalian termasuk penggiat IT yang terllibat transformasi on premise ke cloud, yuk, simak selengkapnya dibawah ini:</p>
<ul>
<li>Agility:
<ul>
<li>Cloud: Hampir semua pengoperasian hanya 1 API call away. Contoh: Meluncurkan server baru, menambah perangkat Load Balancer, membuat duplikat (snapshot), detailed monitoring.</li>
<li>On Premise: Butuh beberapa hari/minggu/bulan untuk penambahan resources seperti storage/RAM, Instalasi OS/Firmware. Beberapa jam dibutuhkan untuk konfigurasi Load Balancer dikarenakan firmware, firmware updates, manual implementasi, dll.</li>
</ul>
</li>
<li>Availability:
<ul>
<li>Cloud: Highly Available. Beberapa vendor (seperti AWS) bahkan memberikan SLA (Service Level Agreement) dengan presentase 99.9% (minimum downtime).</li>
<li>On Premise: Highly Available. Tetapi untuk on prem, dibutuhkan biaya yang amat tinggi untuk mendesain sistem yang mampu mengganti infrastruktur yang KO dalam hitungan menit. Penyedia cloud provider sudah memberikan solusi tersebut sepaket dengan service yang anda bayar seperti, <a href="https://aws.amazon.com/rds/">Amazon RDS</a> misalnya (Relational Database Service), sudah memiliki auto A-Z yang mana akan ada pergantian database di dalam area lain ketika database kita down.</li>
</ul>
</li>
<li>Scalability:
<ul>
<li>Cloud: Highly scalable. Dengan tingginya jumlah request ke server yang semakin meningkat untuk beberapa servis terkenal seperti GOJEK, kebutuhan server resources yang lebih tinggi adalah suatu kebutuhan yang tidak dapat dihindari. Tapi, apakah request selalu berada di Peak season? tidak. Dengan skalabilitas otomatis yang di tawarkan oleh cloud provider, hanya perlu meningkatkan jumlah resources pada saat-saat tertentu. Tentunya untuk GOJEK mungkin ketika jam berangkat kantor, makan siang, dan pulang kantor. Selebihnya "dikecilin lagi" aja.</li>
<li>On Premise: Scalable tetapi tidak se fleksibel cloud. Artinya, anda susah untuk mendapatkan hasil yang sama seperti Auto-Scale yang ditawarkan cloud services. Dan dalam hitungan detik! (yup, detik. Anda tidak salah baca.).</li>
</ul>
</li>
<li>Security:
<ul>
<li>Masih terdapat banyak pro dan kontra tentang hal ini. Dikarenakan, penggunaan cloud services sebagai operasional serta penyimpanan data juga dapat berarti "anda meletakkan data anda secara publik". Tetapi dengan data center kelas dunia yang di tawarkan oleh cloud providers (major players, contohnya), masalah keamanan seperti penetrasi hampir bisa dibilang tidak mungkin. Namun, penentuan keamanan terhadap infrastruktur yang kita gunakan juga tergantung usaha kita mengatur firewall, security groups, NACL, atau yang sejenis dengannya.</li>
</ul>
</li>
</ul>
<p>Mungkin masih banyak lagi pro dan kontra dari beberapa faktor yang mempengaruhi praktisi IT atau perusahaan secara overall untuk mengadopsi cloud services sebagai infrastruktur maupun platform. Silahkan mengisi di kolom komentar sekiranya ada yang ingin ditambahkan menurut pendapat atau pengalaman kalian selama berkecimpung di cloud computing.</p>
<p>Cheers!</p>
