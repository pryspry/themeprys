---
title: 'Mengatasi Plugin reCapctha yang Tidak Muncul di Joomla 2.5.x'
date: Tue, 14 Jan 2014 00:42:06 +0000
draft: false
tags: ['Blog', 'Joomla', 'reCaptcha', 'Tutorial', 'Tutorial']
---

Pagi ini saya rutin keliling ngecek beberapa website Joomla 2.5.x yang saya kelola. Baru ngeh beberapa fitur form yang menggunakan reCapctha tidak berfungsi lagi, bahkan menghilang dari halaman. Di beberapa forum developer ternyata juga cukup banyak yang mengalami hal sama. Taksiran saya Google mengubah API reCapctha nya beberapa bulan kebelakang. Jadi buat teman-teman yang mungkin mengalami hal sama, ini cara resolve nya: Buka /plugins/capctha/recaptcha/recaptcha.php Ubah line 24 sd 26 berikut:```
	const RECAPTCHA\_API\_SERVER = "http://api.recaptcha.net";
    const RECAPTCHA\_API\_SECURE\_SERVER = "https://www.google.com/recaptcha/api";
    const RECAPTCHA\_VERIFY\_SERVER = "api-verify.recaptcha.net";

```menjadi:```
	const RECAPTCHA\_API\_SERVER = "http://www.google.com/recaptcha/api";
    const RECAPTCHA\_API\_SECURE\_SERVER = "https://www.google.com/recaptcha/api";
    const RECAPTCHA\_VERIFY\_SERVER = "www.google.com";

```Ubah line 118 berikut:```
        $response = $this->\_recaptcha\_http\_post(self::RECAPTCHA\_VERIFY\_SERVER, "/verify",

```menjadi:```
	$response = $this->\_recaptcha\_http\_post(self::RECAPTCHA\_VERIFY\_SERVER, "/recaptcha/api/verify",

```Save file lalu reload halaman. reCapctha Anda akan segera muncul kembali.