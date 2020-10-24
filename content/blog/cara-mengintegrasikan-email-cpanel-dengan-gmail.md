---
title: 'Cara Mengintegrasikan Email cPanel Dengan Gmail'
date: Mon, 29 Sep 2014 02:59:06 +0000
draft: false
tags: ['Blog', 'Knowlegde Base', 'Tutorial']
---

Jika Anda telah berhasil membuat akun email berbasis domain Anda sendiri, namun Anda tidak suka dengan tampilan webmail cPanel atau Anda tidak ingin membagi kuota hosting Anda dengan keluar masuknya data email. Maka, mengintegrasikan akun email Anda tersebut dengan Gmail adalah langkah yang paling tepat. Berikut adalah cara mengintegrasikan email Anda dengan Gmail, atau klik disini jika Anda belum membuat akun email melalui cPanel Anda.

Hanya saja Anda harus mengeluarkan uang untuk mendapatkan fasilitas/servis dari Google ini yakni kurang lebih $50/tahun/akun. Walaupun begitu, biaya tersebut sebenarnya sepadan dengan fasilitas yang akan Anda dapatkan nantinya dari Google, karena fasilitas yang Anda dapatkan tidak hanya sebatas pengintegrasian email Anda dengan Gmail namun ada banyak fasilitas Google lainnya yang bisa Anda peroleh. Baca [disini](http://www.google.com/intl/id/enterprise/apps/business/) untuk mengetahui fasilitas lainnya (Google Apps).

Pryspry.com tidak bekerja sama dengan Google dalam hal ini, artikel ini murni untuk membantu Anda melakukan integrasi email cPanel dengan Gmail. Jika tertarik, silahkan baca artikel ini sampai tuntas, jika tidak, silahkan baca artikel kami lainnya mengenai tips, trik dan panduan lainnya mengenai cPanel disini.

Jika Anda tertarik, silahkan Anda masuk ke laman [Google Apps](http://www.google.com/intl/id/enterprise/apps/business/), maka akan muncul jendela seperti berikut:

Kemudian Anda klik tab Mulai Uji Coba Gratis (Google memberikan masa percobaan selama 30 hari, setelah itu Anda harus membayar servis $50/tahun) maka muncul jendela baru seperti berikut:

Isi laman tersebut dengan biodata Anda secara lengkap lalu klik tab berikutnya jika sudah selesai, lalu akan muncul jendela baru seperti berikut:

Jika Anda sudah memiliki hosting/domain sendiri, maka klik pada bulatan seperti yang ditunjukkan oleh panah merah, kemudian isi kolom yang ditunjuk oleh panah hijau dengan domain Anda, lalu klik tab Berikutnya, lalu akan muncul jendela baru seperti berikut:

Masukan nama yang akan Anda gunakan untuk akun email Anda pada kolom Pilih nama pengguna Anda, contoh: admin@domainanda.com (isi dengan kata admin saja karena domainnya sudah otomatis berada dibelakangnya), masukan kata sandi yang akan Anda gunakan pada kolom Buat sandi, masukan kembali kata sandi Anda pada kolom Masukkan kembali sandi, ketik captcha yang tersedia, centang pilihan pertama jika Anda ingin mendapatkan penawaran dari Google kepada email Anda nantinya (tidak usah dicentang jika tidak berminat), baca perjanjian Google Apps for Business lalu centang pilihan tersebut jika Anda telah membaca dan menyetujuinya, dan klik tab setuju dan daftar. Jendela baru akan muncul seperti berikut:

Terlebih dahulu Anda harus mengkonfirmasikan bahwa Anda benar-benar pemilik domain yang telah Anda daftarkan sebelumnya. Oleh karena itu, Anda harus klik

link “Konfirmasikan bahwa Anda pemilik domain”. Maka, Anda akan dibawa ke jendela baru seperti berikut:

Pilih penyedia domain yang Anda gunakan, jika penyedia domain Anda tidak tersedia pada pilihan tersebut, maka klik pilihan Lainnya lalu klik tab Mulai verifikasi setelah menu dropdown tersebut tertutup. Jendela baru muncul seperti berikut:

Anda terlebih dahulu harus menambahkan TXT Record (panah oranye) melalui kontrol panel domain manajer yang disediakan oleh penyedia jasa web hosting Anda. Namun, dikarenakan langkah tersebut pasti berbeda-beda, maka disini kami akan menyeragamkan caranya melalui penambahan rekam CNAME yang bisa Anda lakukan melalui cPanel Anda. Klik link Tambahkan rekam CNAME (panah merah). Jendela baru akan muncul seperti berikut:

Kemudian Anda buka cPanel Anda dan klik kontrol panel Simple DNS Zone Editor pada menu Domains seperti berikut:

Kemudian Anda masukan CNAME record dari Google tadi seperti berikut:

Klik add CNAME Record jika sudah, setelah itu klik tab verifikasi pada laman verifikasi Google. Setelah berhasil klik Arahkan email ke Email Google Apps pada dashboard Google seperti berikut:

Lalu klik berikutnya pada laman berikut:

Kemudian Anda harus mengedit MX Entry Anda, pilih Lainnya pada pilihan siapakah inang domain Anda (jika web hosting Anda tidak tertera pada daftar), lalu klik tab berikutnya.

Jendela baru muncul seperti berikut:

Tabel yang kami tandai dengan kotak merah harus Anda masukan pada MX Entry cPanel Anda, buka kembali cPanel Anda dan klik kontrol panel MX Entry pada menu Mail. Lalu masukan data pada tabel Google tersebut satu persatu seperti berikut:

Klik tab Add New Record untuk kelima nilai (tabel kiri) satu-persatu. Setelah semuanya Anda masukan seperti ini:

Anda harus kembali ke dashboard Google dan klik tab berikutnya. Jendela baru muncul seperti berikut:

Klik tab berikutnya, jendela baru muncul seperti berikut:

Kemudian Google akan memprosesnya paling lambat 48 jam tetapi bisa jauh lebih cepat (maka Anda harus sering mengeceknya apakah sudah selesai atau belum), silahkan Anda klik berikutnya atau keluar dari dashboard Google tersebut dan cek beberapa menit atau beberapa jam lagi.

Jika sudah berhasil, maka Anda bisa menggunakan fasilitas Gmail secara gratis selama 30 hari, setelah itu Anda harus membayar servisnya $50/tahun/akun.