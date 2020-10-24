---
title: 'Crop & Resize Thumbnail K2 Component pada Joomla CMS'
date: Sat, 04 Oct 2014 15:18:45 +0000
draft: false
tags: ['Blog', 'CSS3', 'Featured', 'Joomla', 'K2 Component', 'Tutorial', 'Tutorial']
---

K2 adalah komponen Joomla favorit yang kerap saya gunakan di berbagai project. Fiturnya yang lengkap,  _workflow_nya yang sederhana, dan dikelola secara aktif oleh developernya membuat saya selalu menjatuhkan pilihan pada K2 sebagai pengganti CCK default yang disediakan oleh sistem Joomla. Salah satu kekurangan saat ini yang cukup disayangkan adalah K2 tidak (atau setidaknya belum) memiliki konfiguasi untuk mengatur crop dan resize thumbnail yang muncul di halaman category listing dan hanya memiliki pengaturan _width_ nya saja. Sehingga bila masing-masing image yang kita gunakan memiliki _height_ berbeda, grid tampilan yang muncul tampak tidak rapih. Meski begitu, kita bisa menggunakan fungsi background-cover sebagai manipulasi CSS3. Langkahnya cukup mudah. Misal saja kita menggunakan module K2 Content untuk menampilkan listing item lengkap dengan judul, introtext dan thumbnail image. Maka yang kita ubah hanyalah satu barispada file modules/mod\_k2\_content/tmpl/YOUR\_MODULE\_THEME/default.php. Temukan baris ini:```
<img src="<?php echo $item->image; ?>" alt="<?php echo K2HelperUtilities::cleanHtml($item->title); ?>"/>
```Lalu _replace_ dengan:```
<div class="cropstyle" style="background-image: url('<?php echo $item->image; ?>');" alt="<?php echo K2HelperUtilities::cleanHtml($item->title); ?>"></div>
```Langkah selanjutnya adalah mendefinisikan class cropstyle pada file css theme Anda dengan skrip:```
.cropstyle {
width: 300px;
height: 300px;
overflow: hidden;
background-size: cover;
background-position: center center;
}
```Perhatikan bahwa contoh style di atas akan menyeragamkan thumbnail Anda menjadi full square 300 x 300px. Tentu Anda dapat mengubah nilai width dan height sendiri. Selamat mencoba!