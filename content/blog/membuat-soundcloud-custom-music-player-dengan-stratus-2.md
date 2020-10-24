---
title: 'Membuat Soundcloud Custom Music Player dengan Stratus 2'
date: Fri, 06 Dec 2013 08:26:42 +0000
draft: false
tags: ['Blog', 'Featured', 'Javascript', 'Joomla', 'Jquery', 'Music Player', 'Rayhan Sudrajat', 'Soundcloud', 'Stratus', 'T3-Framework', 'Tutorial', 'Tutorial']
---

Pada project website personal [Rayhan Sudrajat](http://rayhansudrajat.com/), saya coba mengintegrasikan fitur soundcloud player untuk mengambil feed postingan lagu dari akun Rayhan di Soundcloud. Hal yang akan saya bahas ulang di sini adalah seputar penggunaan Soundcloud custom music player menggunakan API Soundcloud dengan bantuan plugin jQuery dari [Stratus 2](http://stratus.sc/) untuk mengambil feed lagu yang dapat diterapkan pada track, set, user maupun grup tertentu di Soundcloud. Dari informasi yang di posting di [halaman blog resmi](http://developers.soundcloud.com/blog/stratus-2-beta) developer Soundcloud, Stratus 2 sendiri dikembangkan oleh developer Soundcloud sekitar dua tahun yang lalu. Meski sudah ada beberapa situs musik/ musisi yang menggunakan Stratus antara lain [At The Drive In](http://atdimusic.com/), dan [Jenny Katz](http://www.yayforeverything.com/jennykatzmusic/), namun Stratus yang sampai hari ini masih berstatus Beta Version dan tidak di-_support_ secara _official_. Mungkin itu sebabnya mengapa Stratus [tidak stabil](http://stackoverflow.com/questions/20205955/soundcloud-stratus-component-broken-uncaught-referenceerror-soundmanager-is-no) dan cukup banyak laporan Stratus [tidak berfungsi](http://stackoverflow.com/questions/13766768/soundcloud-player-stratus-not-appearing) walaupun cara installasinya terbilang mudah. Saya sendiri sempat mengalami beberapa hari sebelum situs Rayhan Sudrajat akan dirilis dan music playernya tidak berfungsi, padahal hari-hari sebelumnya tidak ada masalah. Well, di twitter pihak Soundcloud sendiri sudah mengkonfirmasi bahwa mereka memang punya plan ke depan untuk Stratus. Dan bagi yang tetap berminat menggunakannya, kita langsung saja ya. Masukkan skrip berikut sebelum tag </body> di halaman web yang akan Anda buat:```
<script type="text/javascript" src="http://ajax.googleapis.com/ajax/libs/jquery/1.10.1/jquery.min.js"></script>
<script src="http://code.jquery.com/jquery-migrate-1.2.1.min.js"></script>
<script type="text/javascript" src="http://stratus.sc/stratus.js"></script>

```Pasang juga skrip Stratus sebelum tag </head>```
<script type="text/javascript" src="http://stratus.sc/stratus.js"></script>
```Load skrip berikut sebelum tag </body> untuk memanggil fungsi Stratus```
 <script type="text/javascript">
    $(document).ready(function(){
    $.stratus({
    links: 'https://soundcloud.com/rayhanmusic/the-horcrux'
    });
    });    
</script>
```Kustomisasikan parameter stratus dengan kebutuhan Anda. Opsi parameter lengkapnya sila cek di [tautan ini](http://stratus.sc/).