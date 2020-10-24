---
title: 'Cara Menambah Akun FTP dan Menggunakannya Dengan Filezilla'
date: Sun, 28 Sep 2014 14:46:29 +0000
draft: false
tags: ['Blog', 'Knowlegde Base', 'Tutorial']
---

Jika Anda memiliki website (Anda sebagai super administrator), memiliki seorang atau lebih admin lainnya yang Anda percayakan untuk melakukan pemeliharaan terhadap website Anda. Mungkin seseorang atau lebih admin Anda tersebut membutuhkan akses melalui FTP untuk melakukan pemeliharaan website Anda terhadap direktori tertentu. Berikut kami akan menjelaskan bagaimana cara menambah akun FTP yang hanya bisa diakses untuk direktori tertentu saja dan cara menggunakan akun tersebut melalui FTP Filezilla. **Cara Menambah Akun FTP:**

1.  Login terlebih dahulu ke cPanel Anda.
2.  Klik menu FTP Accounts pada kontrol panel Files di cPanel Anda.
3.  Isi nama user yang Anda inginkan pada kolom Login (disini kami memberikan contoh dengan nama admin).
4.  Isi password untuk mengakses user tersebut pada kolom Password.
5.  Kolom Direktory diisi dengan nama direktori yang ditujukan (disini kami memberikan contoh akses ke direktori demo).
6.  Quota bisa diisi dengan pilihan unlimited atau dibatasi sekian mega/giga. Artinya direktori tersebut bisa diisi file secara unlimited (sesuai kapasitas hosting Anda) atau dibatasi sehingga apabila batasnya sudah terpenuhi maka pengguna akun FTP tersebut tidak dapat lagi menambahkan file ke direktori tersebut.
7.  Klik tombol Create FTP Account untuk menyelesaikan pembuatan akun FTP.

**Cara Menggunakan Akun FTP Tersebut Pada Filezilla:**

1.  Buka Filezilla.
2.  Pada kolom Mesin isi dengan akun server website Anda. Contoh ftp.domainanda.com jika nama domain Anda adalah www.domainanda.com.
3.  Pada kolom Nama Pengguna isi dengan user yang Anda buat tadi. Contoh admin@domainanda.com jika domain Anda adalah www.domainanda.com dan user yang dibuat namanya admin.
4.  Kolom Kata Kunci isi dengan password yang Anda buat tadi untuk akun FTP tersebut.
5.  Klik tombok Koneksi Cepat atau klik Enter pada keyboard Anda untuk menghubungkan.
6.  Maka akun tersebut hanya bisa mengakses direktori tertentu pada website Anda. Contoh yang kami buat, akun tersebut hanya bisa mengakses semua file yang berada pada direktori demo.