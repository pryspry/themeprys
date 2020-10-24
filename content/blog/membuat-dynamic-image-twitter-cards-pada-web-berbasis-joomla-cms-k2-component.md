---
title: 'Membuat Dynamic Image Twitter Cards pada Web Berbasis Joomla CMS + K2 Component'
date: Thu, 03 Jul 2014 00:29:24 +0000
draft: false
tags: ['Blog', 'Featured', 'Joomla', 'K2 Component', 'Tutorial', 'Tutorial', 'Twitter Cards']
---

Pada [postingan terdahulu](http://www.pryspry.com/2013/12/memasang-twitter-cards-pada-web-berbasis-joomla-cms-k2-component/), saya sudah menjelaskan bagaimana menerapkan Twitter Cards pada komponen K2 di Joomla CMS lewat hack core sederhana lewat /components/com\_k2/views/item/view.html.php. Bagi yang sudah menerapkannya, tentu menyadari bahwa field image yang muncul pada Twitter Cards tersebut adalah image dengan menggunakan url statis, bukan field image dynamic dari item K2 itu sendiri. Simak cuplikan skrip berikut:```
// Load Twitter Cards
$document->setMetaData('twitter:card', 'summary');
$document->setMetaData('twitter:site', '@username');
$document->setMetaData('twitter:title', (K2\_JVERSION == '15') ? htmlspecialchars($document->getTitle(), ENT\_QUOTES, 'UTF-8') : $document->getTitle());
$document->setMetaData('twitter:description', strip\_tags($document->getDescription()));
$document->setMetaData('twitter:domain', 'yourdomain.com');
$document->setMetaData('twitter:image:src', 'http://yourdomain.com/gambar.jpg');

```Pada baris terakhir, field image yang saya terapkan bersumber dari http://yourdomain.com/gambar.jpg. Artinya, image ini akan mewakili semua item K2 yang muncul di Twitter Cards. Yang jadi persoalan, bagaimana jika masing-masing item K2 memiliki image yang berbeda satu sama lain, seperti halnya item blog atau postingan berita yang memiliki foto/ ilustrasinya sendiri-sendiri? Solusinya cukup sederhana: 1. Hapus baris terakhir di atas:```
$document->setMetaData('twitter:image:src', 'http://yourdomain.com/gambar.jpg');

```2\. Tambahkan baris berikut:```
$document->setMetaData('twitter:image:src', $image);

```setelah baris:```
$document->setMetaData('image', $image);

```3\. Save & Clear Cache