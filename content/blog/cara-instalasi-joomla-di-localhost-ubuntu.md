---
title: 'Cara Instalasi Joomla! di Localhost Ubuntu'
date: Mon, 29 Sep 2014 03:56:57 +0000
draft: false
tags: ['Blog', 'Knowlegde Base', 'Tutorial']
---

1\. Download terlebih dahulu script Joomla! terbaru untuk Ubuntu melalui situs mereka disini

[![10](http://www.pryspry.com/assets/uploads/2014/09/10-300x112.jpg)](http://www.pryspry.com/wp/wp-content/uploads/2014/09/10.jpg)

2\. Simpan dulu script di desktop Anda untuk memudahkan proses instalasi, extract disana dan ganti nama folder yang sudah ter-ekstrak dengan nama joomla untuk mempermudah (akan tetapi Anda bisa memberikan nama sesuai yang Anda inginkan).

3\. Pindahkan folder joomla tersebut ke folder htdocs lampp dengan mengetikan: cd ./Desktop \[NamaUserUbuntuAnda Desktop\]# sudo mv wordpress /opt/lampp/htdocs dan tekan Enter pada terminal. Kemudian ketik: sudo mv joomla /opt/lampp/htdocs, tekan Enter dan masukan password user Ubuntu Anda.

[![11](http://www.pryspry.com/assets/uploads/2014/09/11-300x54.jpg)](http://www.pryspry.com/wp/wp-content/uploads/2014/09/11.jpg)

4. Aktifkan lampp Anda dengan mengetikkan: sudo /opt/lampp/lampp start pada terminal

[![12](http://www.pryspry.com/assets/uploads/2014/09/12-300x101.jpg)](http://www.pryspry.com/wp/wp-content/uploads/2014/09/12.jpg)

5\. Buat database terlebih dahulu pada phpMyAdmin dengan nama 'joomla' (tanpa tanda kutip) atau silahkan buat sesuai dengan nama yang Anda inginkan. Contoh pembuatan database pada phpMyAdmin Lampp bisa dilihat disini.

6\. Setelah database dibuat, ketik http://localhost/joomla pada browser Anda, maka akan muncul laman instalasi Joomla! Langkah selanjutnya sama dengan proses instalasi Joomla! pada Xampp (instalasi Joomla! di Localhost Windows) yang dapat dilihat disini.

7\. Selamat berkreasi – Joomla! Open Source Matters.

[![13](http://www.pryspry.com/assets/uploads/2014/09/13-300x152.jpg)](http://www.pryspry.com/wp/wp-content/uploads/2014/09/13.jpg)