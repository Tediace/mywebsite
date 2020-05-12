---
title: "What is Wireshark?"
date: 2020-05-11T06:43:10+07:00
draft: false 
escription: "Example article description"
categories:
  - "Hacking"

tags:
  - "Kali Linux"
  - "Sniffing"
menu: main # Optional, add page to a menu. Options: main, side, footer

thumbnail: "img/wireshark.png" # Thumbnail image
lead: "Wireshark (Sniffing)" # Lead text
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
# Wireshark
**Wireshark** adalah penganalisis paket bebas dan sumber terbuka. Perangkat ini digunakan untuk pemecahan masalah jaringan, analisis, perangkat lunak dan pengembangan protokol komunikasi, dan pendidikan. Awalnya bernama Ethereal, pada Mei 2006 proyek ini berganti nama menjadi Wireshark karena masalah merek dagang.

Wireshark adalah cross-platform, menggunakan GTK + widget toolkit dalam rilis saat ini, dan Qt dalam versi pengembangan, untuk mengimplementasikan antarmuka pengguna, dan menggunakan pcap untuk menangkap paket; itu berjalan pada GNU / Linux, OS X, BSD, Solaris, beberapa sistem operasi Unix-seperti lainnya, dan Microsoft Windows. Ada juga (non-GUI) versi berbasis terminal yang disebut tshark. Wireshark, dan program lain yang didistribusikan dengan itu seperti tshark, adalah perangkat lunak bebas, dirilis di bawah ketentuan GNU General Public License.

## Wireshark: Filter TCP/IP Packet
Untuk mengetahui masalah yang ada di jaringan, akan lebih mudah jika kita dapat menyadap menggunakan wireshark dan memfilter hanya packet tertentu saja yang di sadap.

LANGKAH PERTAMA: Untuk bisa menyadap dengan wireshark. Masuk ke menu Capture > Interface. Klik 'Start' untuk mulai menangkap packet.

LANGKAH KEDUA:
## Port Filter
Mem-filter packet kita perlu menset beberapa parameter. Misalnya, kita ingin menampilkan hanya traffic ke port 8080,
```html
tcp.port == 8080
```
Misalnya, kita ingin melihat hanya packet yang menuju port 8080,
```html
tcp.destport = 8080
```
Atau di balik, kita ingin melihat data dari server yang bekerja pada port 8080,
```html
tcp.srcport = 8080
```
Bisa kita buat misalnya,
```html
tcp.port == 8080
```
yang artinya sama dengan
```html
tcp.srcport == 8080 || tcp.dstport == 8080
```
## IP address Filter
Jika kita ingin menangkap hanya packet yang dikirim dari IP tertentu saja,
```html
ip.src == 80.80.80.80
```
Atau IP address tujuan tertentu saja,
```html
ip.dst == 80.80.80.80
```
atau jika kita tidak peduli arah yag dituju,
```html
ip.addr == 80.80.80.80
```
## Filter Data Tertentu
Biasanya ada banyak paket yang dikirim. Agar hanya packet yang berisi data saja yang di tampilkan, kita dapat mem-filter,
```html
tcp.len > 0
```
Atau jika kita ingin hanya menampilkan data yang berisi byte tertentu,
```html
data[0] == A0
```
Atau jika kita ingin menampilkan hanya data pada selang waktu tertentu saja,
```html
frame.time >= 'Feb 1, 2011 11:00:00' && frame.time < 'Feb 1, 2011 11:05:00'
```
## Kombinasi Filter
Kita bisa mengkombinasikan berbagai filter tersebut dengan tanda &&, misalnya,
```html
tcp.destport == 8080 &&
frame.time >= 'Feb 1, 2011 11:00:00' &&
frame.time < 'Feb 1, 2011 11:05:00' &&
ip.src == 80.80.80.80 &&
tcp.len > 0 &&
data[0] == A0
```
Kita dapat mengeksport data tersebut untuk di analisa lebih lanjut.

### Referensi 
* https://lms.onnocenter.or.id/wiki/index.php/Wireshark:_Filter_TCP/IP_Packet
* http://en.wikipedia.org/wiki/Wireshark