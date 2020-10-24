---
title: 'Menghilangkan ''More information about formatting options'' pada Teks Editor Drupal'
date: Wed, 03 Sep 2014 00:39:16 +0000
draft: false
tags: ['Blog', 'CKEditor', 'Drupal', 'Featured', 'Tutorial', 'Tutorial']
---

Adakalanya kita membutuhkan hint informasi tambahan (help description) tentang format teks yang dibolehkan dalam suatu teks editor. Pada Drupal, hint yang letaknya ada di bawah body teks editor ini biasanya berisi shortcode, atau berupa input html yang dibolehkan. Tapi adakalanya hint yang ditandai dengan tautan lewat kalimat 'More information about formatting options' ini juga ingin kita sembunyikan dari user. Alasannya bisa jadi karena pengguna teks editor ini adalah user awam, ataupun sekedar pertimbangan simplisitas. Di bawah ini cara menyembunyikan hint tersebut pada Drupal 7: Masukkan kode berikut di template.php pada direktori theme Anda.```
 /\*\*
\* Remove the comment filters' tips \*/
function MyThemeName\_filter\_tips($tips, $long = FALSE, $extra = '') {
return '';
}
/\*\*
\* Remove the comment filter's more information tips link \*/
function MyThemeName\_filter\_tips\_more\_info () {
return '';
}
?>

```Save Clear cache