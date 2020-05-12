---
title: "MITM-Konsep"
date: 2020-05-08T16:46:46+07:00
draft: true
author: "Levi"
description: "Example article description"
categories:
  - "Hacking"
  -
tags:
  - "hacking"
  - "kali linux"
  - "Digital Forensic"
  
menu: main
thumbnail: "img/mitm.jpg" # Thumbnail image
lead: "Hacking" # Lead text
comments: false # Enable Disqus comments for specific page
authorbox: true # Enable authorbox for specific page
pager: true # Enable pager navigation (prev/next) for specific page
mathjax: true # Enable MathJax for specific page
sidebar: "right" # Enable sidebar (on the right side) per page
widgets: # Enable sidebar widgets in given order per page
  - "search"
  - "recent"
  - "taglist"
---
## Mengenal Serangan Man-in-The-Middle MITM
MiTM attack merupakan jenis serangan yang sangat berbahaya dan bisa terjadi di mana saja, baik di website, telepon seluler, maupun di peralatan komunikasi tradisional seperti surat menyurat. Oleh karena itu saya pikir perlu ada satu artikel khusus yang membahas tentang MiTM attack terlepas dari apapun dan dimanapun implementasi teknisnya.

## MITM: konsep disederhanakan
Serangan Man In the Middle (MITM) attack termasuk kategori serangan aktif, dan sangat membahayakan karena mampu menyadap komunikasi yang terenkripsi, baik menggunakan HTTPS maupun SSH. Akibatnya username & password dan berbagai informasi rahasia dapat dengan mudah di peroleh. Pada kesempatan ini, saya akan mencoba menjelaskan konsep serangan ini secara sederhana sekali. Pada kesempatan lain, akan di jelaskan teknik praktek melakukan serangan MITM. Yang normal, sebuah komputer akan terhubung ke LAN / WiFi yang tersambung ke sebuah router untuk kemudian berhubungan dengan Internet.

## Bukan Sekedar Sniffing
Mungkin banyak yang mengira tujuan dari serangan MiTM adalah untuk menyadap komunikasi data rahasia, seperti yang sniffing. Sniffing bisa disebut sebagai passive attack karena pada sniffing attacker tidak melakukan tindakan apa-apa selain memantau data yang lewat. Memang benar dengan serangan mitm, seorang attacker bisa mengetahui apa yang dibicarakan oleh dua pihak yang berkomunikasi. Namun sebenarnya kekuatan terbesar dari MiTM bukan pada kemampuan sniffingnya, namun pada kemampuan mencegat dan mengubah komunikasi sehingga MiTM attack bisa disebut sebagai jenis serangan aktif.

### Referensi
* http://tz.ucweb.com/4_m84T
* http://www.ilmuhacking.com/basic-concept/mengenal-serangan-man-in-the-middle-mitm/


