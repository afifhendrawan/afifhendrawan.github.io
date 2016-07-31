---
layout: post
title: 4 Langkah Setup VPN di OSX
categories: [Tech]
tags: [tech, osx]
comments: true
description: Setup VPN pada OSX Menggunakan Akun Gratis dari Fastssh
date: 2016-07-28T15:38:47+07:00
---
[ss1]: /assets/media/ss1.png "SS1"
[ss2]: /assets/media/ss3.png "SS2"
[ss3]: /assets/media/ss2.png "SS3"

### Intro
Berangkat dari kebutuhan untuk menggunakan ***Virtual Private Network*** (VPN) pada OSX, saya mencoba untuk menerapkan konfigurasi VPN menggunakan tool SoftEther (yang biasa saya gunakan pada Windows) pada OSX dengan menggunakan layanan yang sama dari [fastssh](https://wwww.fastssh.com). Meskipun SoftEther mengdukung penggunaan pada OSX, berdasarkan laman fastssh, pada OSX tidak dianjurkan menggunakan SoftEther. Oleh karena itu saya mencoba untuk melakukan konfigurasi VPN secara manual. Jangan khawatif, setup akan memakan waktu sangat cepat ! ^^

### Let's Go !

#### Part 1 - Membuat Akun VPN
1. Masuk ke laman [fastssh](https://wwww.fastssh.com).
2. Pada menu pilih **SoftEther**.
3. Kemudian pilih server VPN sesuai dengan kebutuhan. Disini saya menggunakan **SoftEther SG LW 1**. Klik **Create Account**.
4. Pada bagian bawah laman **Create Account** silahkan buat akun untuk akses ke VPN.
5. Catat informasi mengenai **Host IP**, **Nomor Port**, **IPSec Pre-Shared Key**, dan jangan lupa, username dan password akun VPN tentunya.

Jika tidak ada yang terlewat, maka pembuatan akun VPN dari fastssh telah selesai ^^.

#### Part 2 - Setup VPN
1. Masuk ke **Network Preferences**
2. Klik tanda "**+**" pada bagian daftar network interface (kiri).
3. Pilih interface **VPN** dengan VPN Type **L2TP Over IPSec**, nama service bebas ^^. OK.
4. Pilih **Authentication Settings** masukkan password dan **Shared Secret** (IPSec Pre-Shared Key) yang telah dicatat sebelunnya. OK.
5. Terakhir masukkan **Host IP** dan username yang telah dibuat. Username harus memiliki prefix **fastssh.com-username**.
6. Klik Connect.

![alt text][ss1]
![alt text][ss2]
![alt text][ss3]

### Conclusion
Setup VPN secara manual pada OSX lebih mudah karena semua kebutuhan yang diberikan telah disediakan. Penggunaan layanan dari fastshh juga sangat mumpuni, meski memiliki keterbatasan waktu dan jumlah. Dalam kasus disini, saya menggunakan VPN SG LW 1 yang oleh fastssh dibatasi hanya 15 akun gratis dalam satu hari, dan akun akan expired dalam 2 x 24 jam. Fastssh juga dapat menjadi solusi yang **sangat murah** untuk sejenak keluar dari ***pagar***. Untuk penggunaan pada environment Windows, kita hanya perlu menggunakan tool SoftEther dan mengikut petunjuk yang sudah diberikan oleh fastssh.
