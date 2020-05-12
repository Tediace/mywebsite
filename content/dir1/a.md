---
title: "Blockchain"
date: 2020-05-08T16:46:46+07:00
draft: true
author: "Levi"
description: "Example article description"
categories:
  - "Development"
  -
tags:
  - "Blokchain"
  - "Hyperledger"
menu: main
thumbnail: "img/blockchain-2.jpg" # Thumbnail image
lead: "What is data center?" # Lead text
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
## Blockhain
**Blockchain/rantai blok** adalah record yang terus berkembang, disebut block, yang terhubung dan diamankan menggunakan teknik kriptografi.Setiap blok biasanya memuat hash kriptografis dari blok sebelumnya, timestamp, dan data transaksi. Secara desain, blockchain resistan terhadap modifikasi data. Blockchain merupakan sebuah buku besar terdistribusi (distributed ledger) terbuka yang dapat mencatat transaksi antara dua pihak secara efisien dan dengan cara yang dapat diverifikasi dan permanen. Untuk pemanfaatannya sebagai buku besar terdistribusi, blockchain biasanya dikelola oleh sebuah jaringan peer-to-peer secara kolektif dengan mengikuti protokol tertentu untuk komunikasi antar node dan mengkonfirmasi blok-blok baru. Setelah direkam, data dalam blok tidak dapat diubah secara retroaktif tanpa perubahan pada blok-blok berikutnya, yang membutuhkan konsensus mayoritas jaringan.

Blockchain dirancang dari awal agar aman (secure by design) dan merupakan contoh sistem komputasi terdistribusi dengan Byzantine Fault Tolerance (BFT) yang tinggi. Konsensus terdesentralisasi dapat dicapai dengan blockchain. Hal ini membuat blockchain cocok untuk merekam peristiwa, catatan medis, dan aktivitas pengelolaan record lainnya, seperti manajemen identitas, pemrosesan transaksi, dokumentasi barang bukti, ketertelusuran makanan (food traceability), dan pemungutan suara (voting).
 ## Technology Open Source Blockchain
### Hyperledger
**Hyperledger** adalah implementasi kerangka kerja blockchain yang dapat di gunakan untuk mengembangkan aplikasi atau solusi dengan arsitektur modular. yang Merupakan sebuah proyek dari blockchain open source dan related tools, dimulai pada Desember 2015 oleh Linux Foundation, dan didukung oleh industri besar seperti IBM, Intel dan SAP Ariba, untuk mendukung pengembangan kolaboratif dari buku besar yang didistribusikan berbasis blockchain.

## Kerangka Kerja Hyperledger
* Hyperledger fabric 

*Jaringan Fabric* terdiri dari "Peer Nodes", yang mengeksekusi kode rantai, mengakses data buku besar, mendukung transaksi dan antarmuka dengan aplikasi. "Node pemesan" yang memastikan konsistensi dari blockchain dan memberikan transaksi yang disetujui kepada rekan-rekan jaringan, dan layanan MSP, yang umumnya diimplementasikan sebagai Otoritas Sertifikat, mengelola sertifikat X.509 yang digunakan untuk mengotentikasi identitas dan peran anggota.

* Hyperroger Iroha

*Iroha* menciptakan algoritma konsensus BFT baru satu fase asinkron yang disebut YAC (Yet Another Consensus), untuk memastikan konsistensi keadaan data di antara node dan skala secara linear.

* Hyperledger Sawtooth

*Hyperledger Sawtooth* Awalnya dikelola oleh Intel, Sawtooth menyertakan fitur konsensus dinamis yang memungkinkan algoritme konsensus hot swapping dalam jaringan yang sedang berjalan. Di antara opsi konsensus adalah protokol yang merupakan konsensus baru yang dikenal sebagai "Proof of Elapsed Time," protokol konsensus desain lotre yang secara opsional dibangun di atas lingkungan eksekusi tepercaya yang disediakan oleh Intel Software Guard Extensions (SGX).

* Hyperledger Indy

*Hyperledger Indy* merupakan proyek Hyperledger untuk mendukung identitas independen pada buku besar yang didistribusikan.serta menyediakan alat, perpustakaan, dan komponen yang dapat digunakan kembali untuk memberikan identitas digital yang berakar pada blockchain atau buku besar lain yang didistribusikan dan disumbangkan oleh Yayasan Sovrin. 

* Hyperledger Grid

*Grid* adalah kerangka kerja untuk membangun solusi rantai pasokan. pada ekosistem teknologi, kerangka kerja, dan perpustakaan yang bekerja bersama, guna pengembang aplikasi untuk menentukan komponen mana yang paling tepat untuk industri atau model pasar mereka.

### Source code
* https://github.com/hyperledger

### Referensi
* "Blockchain in Finance: From Buzzword to Watchword in 2016". CoinDesk (News)]. Retrieved 22 December 2016.
* Open Source Blockchain Effort for the Enterprise Elects Leadership Positions and Gains New Investments - Hyperledger"