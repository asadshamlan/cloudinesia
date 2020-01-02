---
layout: post
status: publish
published: true
title: Amazon IAM Sebagai Fondasi Keamanan Akun Anda
author: asadshamlan
excerpt: Jika anda pengguna Amazon Web Service, pemula maupun para 'sifu' pasti setuju
  dengan saya bahwa yang pertama kali wajib di telaah adalah Identity Access Management
  atau yang biasa di singkat IAM.
wordpress_id: 2025
wordpress_url: http://cloudinesia.com/?p=2025
date: '2018-05-26 09:00:02 +0000'
date_gmt: '2018-05-26 09:00:02 +0000'
categories:
- Uncategorized
- Featured
- Trending
- Tekno
tags:
- aws
- iam
- security
- mfa
comments: []
tags: [featured]
image: assets/images/IAM.jpg
---
<p>Jika anda pengguna Amazon Web Service, pemula maupun para 'sifu' pasti setuju dengan saya bahwa yang pertama kali wajib di telaah adalah Identity Access Management atau yang biasa di singkat IAM.</p>
<p>IAM sendiri merupakan fitur paling mendasar dalam pengelolaan cloud infrastruktur mulai dari pembagian penggunaan dibawah kategori tertentu, pengelolaan grup pengguna, serta memberikan policy atau akses kontrol terhadap pengguna, grup, bahkan ke infrastuktur itu sendiri. Contohnya virtual machine mereka atau yang dikenal dengan nama EC2. Berbeda dengan layanan produk cloud amazon lainnya yang bersifat regional, IAM ditawarkan di peringkat global hal ini dikarenakan IAM merupakan kebutuhan primer bagi setiap pemilik akun dalam usaha mengamankan 'resource' infrastruktur yang digunakan. Hal ini juga didukung oleh Amazon yang mengedepankan langkah - langkah rekomendasi pengamananan akun pada saat akun sudah berhasil di buat.</p>
<p><img class="size-large wp-image-2027 aligncenter" src="http://cloudinesia.com/wp-content/uploads/2018/05/Screen-Shot-2018-05-28-at-1.01.59-PM-1024x365.png" alt="securing iam" width="1000" height="356" /></p>
<p style="text-align: center;">Gambar: Status Pengamanan IAM</p>
<p>Seperti ditunjukkan gambar di atas, AWS Console akan menampilkan 5 aksi yang di rekomendasikan Amazon untuk mengamankan akun anda. Tentu masih ada beberapa cara lain yang dapat anda lakukan seperti di ulas di portal dokumentasi amazon <a href="https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html">ini.</a> Tapi kali ini kita akan membahas 5 langkah yang direkomendasikan oleh AWS pada saat anda membuka layanan IAM, dibawah ini:</p>
<p><strong>Delete your root access keys</strong></p>
<p>Pada saat anda mendaftar ke akun Amazon Web Service, secara otomatis anda adalah terdaftar sebagai Root atau super user. Artinya, anda memiliki peringkat akses paling tinggi dalam akun anda. Mengakses infrastruktur anda menggunakan root dapat menghapus atau menambah infrastruktur yang anda gunakan secara bebas tanpa batas. Root ataupun pengguna yang lain dapat memiliki <em>"Access keys"</em> yang berfungsi untuk <em>"Programmatic Access"</em> atau akses melalui pemrograman (script atau kode anda). Langkah pertama yang di sarankan adalah menghapus root access keys untuk menghindari penyalahgunaan akses. Dengan menghapus root access keys, anda diharuskan menambah pengguna yang di kontrol serta di dedikasikan untuk suatu tugas atau projek.</p>
<p><strong>Activate MFA on your root account</strong></p>
<p>MFA atau Multi Factor Authentication adalah fitur kemanan yang mengharuskan pengguna untuk mendapatkan token atau kode tertentu ketika berhasil masuk dengan username &amp; password. AWS IAM mendukung penggunaan MFA sebagai 'layer' keamanan ganda untuk akun anda. Anda dapat menggunakan hardware yang dapat di pesan melalui Amazon sendiri, atau menggunakan Google Authenticator sebagai perangkat MFA anda.</p>
<p><strong>Create Individual IAM users</strong></p>
<p>Setelah upaya pengamanan terhadap root berhasil, sekarang saatnya untuk membuat akun user baru. Pembuatan akun user secara individual akan sangat membantu mengatur resource yang digunakan di akun anda, serta yang dibutuhkan untuk seorang pengguna atau beberapa pengguna sekaligus yang di kemas dalam satu set bernama group. Seperti contoh, fulan bertanggung jawab sebagai penyedia server untuk tim developer. Maka anda dapat meminta detail fulan untuk di undang sebagai pengguna di konsol AWS. Setiap akun baru yang di buat melalui konsol memiliki kontrol atau permission yang dapat ditentukan masing - masing.</p>
<p><strong>Use groups to assign permission</strong></p>
<p>Menentukan akses kontrol atau permission berdasarkan group. Walaupun akses kontrol dapat diberikan ke pengguna secara langsung, AWS merekomendasikan untuk mendefinisikan akses kontrol berdasarkan grup. Hal ini disebabkan oleh mudahnya mengatur, menjaga/supervisi, serta mengaudit keamanan akun berdasarkan grup dibanding pengguna. Ketika anda mempunyai 50 pengguna yang berbeda kemudian setiap individu memiliki akses yang berbeda, akan sangat sulit bagi anda untuk 'keep track' ke setiap akses kontrol yang ada.</p>
<p><strong>Apply IAM Password Policy</strong></p>
<p>Mendefinisikan peraturan atau format password. Untuk anda yang berkecimpung di Active Directory, hal ini mungkin sangat familiar. Langkah yang terakhir ini menganjurkan anda untuk mendefiniskan sekuat serta serumit apa password yang anda ingin terapkan di organisasi/perusahaan anda. AWS mendukung penerapan password rumit seperti konten password, jumlah karakter, kombinasi angka dan huruf, serta adanya huruf kapital/non-kapital. Selain itu, AWS juga memberikan anda pilihan untuk menentukan <em>"password rotation policy"  </em>yang mana password diharuskan untuk selalu dirubah pada periode tertentu.</p>
<p>Jadi untuk pembaca yang baru saja mendaftar sebagai pengguna Amazon Web Service, pastikan anda masuk ke <a href="https://console.aws.amazon.com/iam/home">IAM Management Console</a> dan mulai melakukan langkah - langkah rekomendasi Amazon diatas sebagai upaya mengamankan akun anda.</p>
<p>Cheers!</p>
