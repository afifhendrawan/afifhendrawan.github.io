---
layout: post
title: Android Asset Generator
categories: [Project, Tech, Java]
tags: [tech, android]
comments: true
description: Tool untuk memudahkan membuat aset pada android. Output berupa asset lpdi, mdpi, hdpi, xhdpi, xxhdpi, xxxhdpi, sesuai dengan ukuran inputan aset yang diinginkan.
date: 2016-09-08T17:23:35+07:00
---
![alt text][AndroidAssetGenerator]

Project iseng yang saya buat karena terinspirasi dari project aset generator untuk android bernama [Fred](https://github.com/leocadiotine/fred) di Github. Alasan pertama pembuatan project Android Asset Generator ini karena saya merasa kesulitan dan agak kurang fleksibel menggunakan tool yang sebenarnya lebih powerfull, yaitu aset generator buatan [Ruman Nurik](https://romannurik.github.io/AndroidAssetStudio/). Selain karena harus online, kedua kadang saya suka menyalahi pakem design Android. Alasan kedua, tool yang biasa saya pakai selain dari [Ruman Nurik](https://romannurik.github.io/AndroidAssetStudio/) yaitu [Fred](https://github.com/leocadiotine/fred) juga kurang fleksibel dengan menjadikan ukuran xxxhdpi sebagai ukuran patokan aset. Sebenarnya project ini ingin mencoba melanjutkan apa yang telah dikerjakan oleh [leocadiotine](https://github.com/leocadiotine) pada Fred dengan menambahkan opsi untuk pemilihan ukuran dasar sebagai patokan. Namun karena ditulis menggunakan *clojure* yang tidak saya tahu, maka saya putuskan untuk membuat Android Asset Generator dengan menggunakan Java.

![alt text][screen-destinies]

Perhitungan penyekalaan Android Asset Generator sudah mengikuti aturan standar design aset dari [Android](https://developer.android.com/guide/practices/screens_support.html) yaitu,

1. 0.75x ldpi
2. 1.00x mdpi --> Baseline
3. 1.50x hdpi
4. 2.00x xhdpi
5. 3.00x xxhdpi
6. 4.00x xxxhdpi

### Cara Penggunaan Android Asset Generator
1. Pasikan perangkat sudah terinstal Java.
2. Download [Android Asset Generator](https://drive.google.com/file/d/0B1gD3P_CVk2GMW4xbWV3bDh3NjQ/view?usp=sharing).
3. Jalankan Android Asset Generator.
4. Pilih lokasi aset.
5. Pilih ukuran aset yang akan digunakan sebagai patokan.
6. Pilih destinasi output aset.
7. Generate !

### Kontribusi
Untuk yang ingin melanjutkan atau sekedar ingin tahu tentang project sederhana ini bisa fork project Android Asset Generator via [Github](https://github.com/hndr91/AndroidAssetGenerator).

### 3rd Party Library
1. [Apache Common IO](https://commons.apache.org/proper/commons-io/)
2. [Thumbnailator](https://github.com/coobird/thumbnailator)

### Lisensi
**Apache License Version 2.0**

[screen-destinies]: /assets/media/screen-destinies.png "Screen Destinies"
[AndroidAssetGenerator]: /assets/media/AndroidAssetGenerator.png "Android Asset Generator"
