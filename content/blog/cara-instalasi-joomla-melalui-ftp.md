---
title: 'Cara Instalasi Joomla Melalui FTP'
date: Sun, 28 Sep 2014 20:49:00 +0000
draft: false
tags: ['Blog', 'Knowlegde Base', 'Tutorial']
---

1.  Ikuti langkah proses download script Joomla disini (masuk ke jangkar cara instalasi joomla pada windows point 1-2). Setelah itu, kembali ke halaman ini.
    
2.  Aktifkan FTP Anda (rekomendasi Fillezila)
    
3.  Upload semua script Joomla yang sudah Anda download dan di-extract ke folder public\_html pada server Anda seperti berikut:
    
    [![6](http://www.pryspry.com/assets/uploads/2014/09/6-300x238.jpg)](http://www.pryspry.com/wp/wp-content/uploads/2014/09/6.jpg)
    
4.  Sambil menunggu proses uploading, Anda buat database melalui cPanel. Caranya bisa Anda lihat disini (masuk ke jangkar proses pembuatan database wp). Setelah selesai kembali ke halaman ini.
    
5.  Setelah semuanya ter-_upload_ ketik domain Anda tersebut pada browser, kemudian ikuti langkah-langkah instalasi Joomla hingga selesai seperti disini. (masuk ke jangkar proses instalasi joomla di windows point 5).
    
6.  Namun, pada beberapa kasus. Host Anda tidak dapat melakukan instalasi Joomla versi terbaru (saat ini versi terbaru adalah Joomla! 3.1). Ketika Anda berhasil meng-_upload_ semua script Joomla namun ketika domain Anda ketikkan pada browser dan hasilnya gagal dengan hanya ada sebuah
    
    kalimat “_Your host needs to use PHP 5.3.1 or higher to run this version of Joomla!_”, Anda tidak usah panik, yang Anda perlukan adalah langkah-langkah seperti berikut:
    

*   Masuk ke direktori script Joomla yang telah Anda upload (bisa menggunakan FTP Filezilla) dan cari file htaccess.txt ubah (ganti nama) menjadi .htaccess
    

[![7](http://www.pryspry.com/assets/uploads/2014/09/7-300x237.jpg)](http://www.pryspry.com/wp/wp-content/uploads/2014/09/7.jpg)

Menjadi

[![8](http://www.pryspry.com/assets/uploads/2014/09/8-300x238.jpg)](http://www.pryspry.com/wp/wp-content/uploads/2014/09/8.jpg)

*   Kemudian buka file .htaccess tersebut menggunakan teks editor seperti notepad atau lainnya. Kemudian masukan kode berikut (# Use PHP 5.3 AddHandler application/x-httpd-php53 .php suPHP\_ConfigPath /opt/php53/lib) dipaling atas pada file .htaccess tersebut.
    
     [![9](http://www.pryspry.com/assets/uploads/2014/09/9-300x261.jpg)](http://www.pryspry.com/wp/wp-content/uploads/2014/09/9.jpg)
    
*   Save perubahan tersebut lalu refresh web Anda, maka Joomla installer akan muncul. Setelah itu ikuti langkah-langkah instalasinya seperti disini. (masuk ke jangkar proses instalasi joomla di windows point 5).