---
title: 'Memasang Twitter Cards pada Web Berbasis Joomla CMS + K2 Component'
date: Sun, 08 Dec 2013 00:43:32 +0000
draft: false
tags: ['Blog', 'Featured', 'Joomla', 'K2 Component', 'Tutorial', 'Tutorial', 'Twitter Cards']
---

Pada beberapa project terdahulu, saya mulai tertib menggunakan fitur Cards yang disediakan oleh Twitter untuk mengoptimalkan display web content yang saya kelola. Prinsip kerjanya sendiri sederhana, Twitter akan mengambil metadata sebuah halaman, lalu meng-extract-nya jadi tampilan default ketika tautan konten tersebut dishare di linimassa, persis seperti kerja OpenGraph di Facebook. Bedanya, Card membutuhkan validasi yang harus diapprove terlebih dahulu oleh pihak Twitter. Twitter Card sendiri memiliki beberapa tipe card catalog, yakni Summary dan Summary Large Image (untuk format konten artikel), Product (untuk format ecommerce), Photo (untuk konten visual), Player (untuk format playback audio dan video streaming), serta App (untuk format konten aplikasi). Berikut ini sampel tag nya:```
<meta name="twitter:card" content="summary">
<meta name="twitter:site" content="@site\_username">
<meta name="twitter:title" content="Top 10 Things Ever">
<meta name="twitter:description" content="Up than 200 characters.">
<meta name="twitter:creator" content="@creator\_username">
<meta name="twitter:image:src" content="http://placekitten.com/250/250">
<meta name="twitter:domain" content="YourDomain.com">
<meta name="twitter:app:name:iphone" content="Vine">
<meta name="twitter:app:name:ipad" content="Vine">
<meta name="twitter:app:name:googleplay" content="Vine">
<meta name="twitter:app:url:iphone" content="vine://v/93582sxlkjf">
<meta name="twitter:app:url:ipad" content="vine://v/93582sxlkjf">
<meta name="twitter:app:url:googleplay" content="http://vine.co/v/93582sxlkjf">
<meta name="twitter:app:id:iphone" content="id81239204382">
<meta name="twitter:app:id:ipad" content="id432984038404">
<meta name="twitter:app:id:googleplay" content="com.foursquare.android">
```Contoh sukses penggunaan Card yang pernah saya buat antara lain di situs [Postrockstore.co](http://postrockstore.co "Postrockstore.co") berbasis Drupal dan [Efenerr](http://efenerr.com "Efenerr") berbasis Wordpress. Kebetulan dua CMS ini menyediakan modules dan plugin yang memudahkan penerapan Card cukup dengan sekali install dan beberapa jurus pengaturan di backend. Berbeda dengan Drupal dan Wordpress, kendala justru saya temui saat hendak menerapkan Card di situs berbasis Joomla. Selain karena ketersediaan pluginnya masih terbatas, saya juga terkendala ketika menggunakan K2 sebagai komponen Joomla yang kerap saya gunakan. Pasalnya, saat ini K2 baru mendukung penggunaan OpenGraph saja. Karena penasaran, saya lantas mencoba beberapa 'hacking' kecil agar si metadata Card ini bisa berfungsi di web berbasis Joomla + K2. Meski cara 'kasar' tidak saya anjurkan, tapi buat yang juga penasaran kayak saya, berikut ini langkah-langkahnya: 1. Buka /components/com\_k2/views/item/view.html.php 2. Cari baris berikut:```
// Set Facebook meta data
$document = JFactory::getDocument();
$uri = JURI::getInstance();


```Letakkan metadata berikut di bawah skrip poin 2```
// Load Twitter Cards
$document->setMetaData('twitter:card', 'summary');
$document->setMetaData('twitter:site', '@username');
$document->setMetaData('twitter:title', (K2\_JVERSION == '15') ? htmlspecialchars($document->getTitle(), ENT\_QUOTES, 'UTF-8') : $document->getTitle());
$document->setMetaData('twitter:description', strip\_tags($document->getDescription()));
$document->setMetaData('twitter:domain', 'yourdomain.com');
$document->setMetaData('twitter:image:src', 'http://yourdomain.com/gambar.jpg');


```Jangan lupa replace @username, domain, dan image source dengan data klien yang akan Anda gunakan, lalu submit tautannya di link berikut. Segera setelah diapprove oleh pihak Twitter, Cards akan secara otomatis berfungsi. --------------------------- \*) Ilustrasi dikutip dari: [Ayudawp.com](http://ayudawp.com/twitter-cards-en-wordpress/) \*) Update --> [**Membuat Dynamic Image Twitter Cards pada Web Berbasis Joomla CMS + K2 Component**](http://www.pryspry.com/2014/07/membuat-dynamic-image-twitter-cards-pada-web-berbasis-joomla-cms-k2-component/)