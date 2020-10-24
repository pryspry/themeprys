---
title: 'Cara Instalasi Joomla! Pada Localhost Windows'
date: Mon, 29 Sep 2014 04:33:29 +0000
draft: false
tags: ['Blog', 'Knowlegde Base', 'Tutorial']
---

1.  Download script Joomla! Pada website resmi mereka [disini](http://www.joomla.org/download.html).
    
     [![14](http://www.pryspry.com/assets/uploads/2014/09/14-300x187.jpg)](http://www.pryspry.com/wp/wp-content/uploads/2014/09/14.jpg)
    
2.  Buat folder bernamakan joomla dan extract script hasil download-an tersebut dalam folder tersebut serta pindahkan script zip-nya ke luar folder joomla. (Nama folder bisa apa saja sesuai yang Anda inginkan, tetapi disini kami membuat contoh dengan nama folder joomla untuk memudahkan proses pembelajaran).
    

[![15](http://www.pryspry.com/assets/uploads/2014/09/15-300x275.jpg)](http://www.pryspry.com/wp/wp-content/uploads/2014/09/15.jpg)

     3. Aktifkan XAMPP Anda.

[![16](http://www.pryspry.com/assets/uploads/2014/09/16-300x267.jpg)](http://www.pryspry.com/wp/wp-content/uploads/2014/09/16.jpg)

     4. Pindahkan folder joomla tersebut ke folder htdocs xampp Anda (C:xampp/htdocs)

[![17](http://www.pryspry.com/assets/uploads/2014/09/17-300x244.jpg)](http://www.pryspry.com/wp/wp-content/uploads/2014/09/17.jpg)

    5. Buka browser Anda dan ketik [http://localhost/joomla/installation/index.php](http://localhost/joomla/installation/index.php), isi menu      konfigurasi dengan data Anda dan klik next jika sudah selesai.

[![18](http://www.pryspry.com/assets/uploads/2014/09/18-300x196.jpg)](http://www.pryspry.com/wp/wp-content/uploads/2014/09/18.jpg)6\. Muncul jendela baru yakni Database Configuration, sebelum mengisi Database Configuration tersebut, terlebih dahulu Anda harus membuat database pada phpMyAdmin. Buka tab baru pada browser Anda dan ketik: [http://localhost/phpmyadmin/](http://localhost/phpmyadmin/), kemudian klik menu Databases.

[![19](http://www.pryspry.com/assets/uploads/2014/09/19-300x180.jpg)](http://www.pryspry.com/wp/wp-content/uploads/2014/09/19.jpg)

7\. Kemudian isi nama database pada kolom create new database, disini kami isi dengan nama joomla untuk memudahkan proses pembelajaran (Anda bisa membuatnya dengan nama apa pun yang Anda suka).

[![20](http://www.pryspry.com/assets/uploads/2014/09/20-300x256.jpg)](http://www.pryspry.com/wp/wp-content/uploads/2014/09/20.jpg)

8.Jika berhasil maka nama joomla akan berada pada menu phpMyAdmin disebelah kiri.

[![21](http://www.pryspry.com/wp/wp-content/uploads/2014/09/21.jpg)](http://www.pryspry.com/wp/wp-content/uploads/2014/09/21.jpg)9\. Kembali ke laman proses instalasi Joomla dan isi menu Database Configuration seperti berikut (kolom Database Name diisi dengan nama database yang Anda buat tadi pada menu phpMyAdmin dan kolom password diisi sesuai dengan password MySQL XAMPP Anda), klik next jika sudah selesai:

[![22](http://www.pryspry.com/assets/uploads/2014/09/22-300x196.jpg)](http://www.pryspry.com/wp/wp-content/uploads/2014/09/22.jpg)10\. Pada menu Finalisation, ubah pilihan Install Sample Data ke Default English (GB) Sample Data lalu klik tab Install.

[![23](http://www.pryspry.com/assets/uploads/2014/09/23-300x183.jpg)](http://www.pryspry.com/wp/wp-content/uploads/2014/09/23.jpg)11\. Tunggu proses instalasi beberapa detik

[![24](http://www.pryspry.com/assets/uploads/2014/09/24-300x149.jpg)](http://www.pryspry.com/wp/wp-content/uploads/2014/09/24.jpg)12\. Selamat Anda berhasil menginstal Joomla! Pada komputer Anda (local server). Akan tetapi proses instalasi belum sepenuhnya selesai, Anda terlebih dahulu harus meng-klik tombol Remove installation folder.

[![25](http://www.pryspry.com/assets/uploads/2014/09/25-300x202.jpg)](http://www.pryspry.com/wp/wp-content/uploads/2014/09/25.jpg)13\. Setelah berhasil di-remove, klik tab site untuk melihat tampilan Joomla! atau klik tab administrator untuk memasuki menu dashboard Joomla!

14\. Selamat, Anda telah berhasil melakukan proses instalasi Joomla! Pada komputer Anda (local server) – Open Source Matters.