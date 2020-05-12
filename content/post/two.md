---
title: "Intrusion Detection System"
date: 2020-05-12T06:20:10+07:00
draft: false 
escription: "Example article description"
categories:
  - "Data Base"

tags:
  - "Server"
  - "Security"
 # Optional, add page to a menu. Options: main, side, footer

thumbnail: "img/snort.jpg" # Thumbnail image
lead: "Snort" # Lead text
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
## Intrusion Detection System
Intrution Detection System atau IDS adalah perangkat (atau aplikasi) yang memonitor jaringan dan / atau sistem untuk kegiatan berbahaya atau pelanggaran kebijakan dan memberikan laporan ke administrator atau station manajemen jaringan. Pencegahan intrusi / pemyusupkan adalah proses melakukan deteksi intrusi dan mencoba untuk menghentikan insiden yang mungkin terdeteksi.

Intrusion Detection and Prevention System (IDPS) biasanya mencatat informasi yang berkaitan dengan peristiwa yang diamati, memberitahu administrator keamanan penting peristiwa yang diamati, dan menghasilkan laporan. Banyak IDPS juga dapat menanggapi ancaman yang terdeteksi dengan mencoba untuk mencegah berhasil. Mereka menggunakan beberapa teknik respon, yang melibatkan IDPS menghentikan serangan itu sendiri, mengubah lingkungan keamanan (misalnya, konfigurasi ulang firewall), atau mengubah konten serangan ini.

## Istilah Istilah di IDS
* **Alert/Alarm-** Sebuah kode yang menandakan bahwa sistem sedang atau telah di serang.
* **True Positive-** Serangan sebenarnya yang mentrigger IDS untuk memberikan alarm.
* **False Positive-** Sebuah kejadian yang menyebabkan IDS memberikan alarm saat tidak ada serangan yang terjadi.
* **False Negative-** Kegagalan IDS dalam mendeteksi sebuah serangan yang sesungguhnya.
* **True Negative-** Saat tidak ada serangan yang terjadi dan tidak ada alarm yang di aktifkan.
* **Noise-** Data atau interferensi yang menyebabkan terjadinya false positive.
* **Site policy-** Kebijakan dalam sebuah organisassi yang mengatur rules dan konfigurasi dari sebuah IDS.
* **Site policy** awareness- Kemampuan IDS untuk secara dinamik mengubah rules dan konfigurasinya sebagai responds terhadap aktifitas lingkungan yang berubah-ubah.
* **Confidence value-** Nilai yang diberikan pada IDS berdasarkan pada kinerja dan kemampuan analisa sebelumnya dalam menolong mengidentifikasi sebuah serangan.
* **Alarm filtering-** Proses dalam mengkategorisasi attack alert yang dibuat oleh IDS untuk membedakan antara false positive dan attack yang sesungguhnya.

## Tipe Intrusion-Detection System
Pada dasarnya ada dua tipe utama IDS, yaitu,

* network-based IDS
* host-based IDS

Pada sebuah **network-based** intrusion-detection system (NIDS), sensor biasanya diletakan pada titik pintu gerbang jaringan, seperti demilitarized zone (DMZ) atau pada perbatasan jaringan. Sensor akan menangkap semua traffic jaringan, menganalisa isi masing-masing paket akan adanya traffic yang tidak baik. NIDS, biasanya sebuah platform independent yang mengidentifitasi penyusupan dengan cara menganalisa traffic dan memonitor beberapa host sekaligus. NIDS memperoleh akses ke traffic jaringan dengan menyambungkan diri ke hub, network switch yang di konfigurasi untuk port mirroring, atau network tap. Contoh dari sebuah NIDS adalah Snort.

Pada sebuah **host-based** intrusion-detection system (HIDS), sensor biasanya terdiri dari software agent, yang akan memonitor semua aktifitas di host dimana dia terinstall biasanya dengan menganalisa system call, modifikasi file system (mondifikasi file binary, password, capability / acl database, log berbagai aplikasi, kernel. Contoh dari HIDS adalah OSSEC, tripwire.

Intrusion detection system dapat juga dibuat secara spesifik untuk system yang kita inginkan menggunakan custom tools dan honeypots.

## Teknik Menghindari IDS
Teknik untuk menghindari Intrusion Detection System membypass deteksi dengan menciptakan kondisi yang berbeda pada IDS dan pada komputer target. Musuh bisa mencapai ini dengan memanipulasi baik serangan itu sendiri atau lalu lintas jaringan yang berisi serangan.

## IDS berbasis Statistical Anomaly dan Signature
Sebuah Intrusion Detection Systems akan menggunakan salah satu dari dua (2) teknik deteksi, yaitu,

* berbasis statistical anomaly
* berbasis signature

Furthermore,

* **Statistical anomaly based IDS** - Sebuah IDS berbasis statistical anomaly menetapkan dasar kinerja berdasarkan evaluasi lalu lintas jaringan. Hal ini kemudian digunakan sebagai sampel untuk baseline untuk mendeteksi apakah traffic tersebut masuk atau tidak dalam parameter baseline. Jika sampel lalu lintas berada diluar parameter baseline, alarm akan dipicu.
* **Signature-based IDS** - Lalu lintas jaringan diperiksa terhadap pola serangan yang telah dikonfigurasikan dan ditentukan sebelumnya yang dikenal sebagai signatures. Banyak serangan saat ini memiliki signature yang berbeda. Dalam praktek keamanan yang baik, koleksi signature ini harus terus diperbarui untuk mengurangi ancaman yang muncul.

## Keterbatasan
Ada beberapa keterbatasan yang bisa dialami oleh IDS, yaitu,

* **Noise** - Noise akan sangat membatasi effektifitas Intrusion Detection System. Paket yang jelek yang di hasilkan oleh bug pada software, data DNS yang korup, atau paket lokal yang keluar jaringan bisa membuat tinggi-nya alarm yang salah.
* **Jumlah attack sedikit** - Adalah sangat biasa untuk melihat bahwa jumlah attack yang sebenarnya jauh di bawah dari tingkat alarm yang salah. Akibatnya attack yang sebenarnya sering kali tidak terlihat bahkan di abaikan.
* **Signature updates** - Banyak serangan yang ditujukan untuk versi tertentu dari software yang biasanya usang. Sebuah library dari signature yang dapat terus berubah dibutuhkan untuk mengurangi ancaman. Database signature usang dapat menyebabkan IDS rentan terhadap strategi baru.

## SNORT (IDS, Open Source)
Snort adalah free dan open source network intrusion prevention system (NIPS) dan network intrusion detection system (NIDS), yang di kembangkan oleh Martin Roesch tahun 1998. Snort saat ini di kembangkan oleh Sourcefire, dimana Roesch adalah founder dan CTO. Tahun 2009, Snort terpilih sebagai ‘greatest open source software of all time.’

## Uses
Snort’s open source network-based intrusion detection system (NIDS) yang mempunyai kemampuan untuk melakukan analisa traffic secara real time dan packet logging dari jaringan Internet Protocol (IP). Snort melakukan analisa protocol, pencarian content, pencocokan content. Snort juga dapat digunakan untuk mendeteksi serangan, termasuk, tapi tidak terbatas pada, operating system fingerprinting attempts, common gateway interface, buffer overflows, server message block probes, dan stealth port scans.

Snort dapat dikonfigurasi menggunakan tiga mode utama: sniffer, packet logger, dan network intrusion detection.

* **Mode sniffer** - snort akan membaca paket yang lewat dan menampilkan ke layar.
* **Mode logger** - snort akan mencatat paket yang lewat ke disk.
* **MOde Intrusion Detection** - snort akan memonitor semua traffic yang lewat, membandingkan dengan rule yang di definisikan oleh user.
Ada beberapa tool yang bisa di kawinkan dengan snort untuk administrasi, reporting, dan analisa log, seperti,

Ada beberapa tool yang bisa di kawinkan dengan snort untuk administrasi, reporting, dan analisa log, seperti,

* Snorby 
* BASE 
* RazorBack 

### Source code
* https://github.com/snort3/snort3

### Referensi yang bagus
* https://www.slideshare.net/CiscoDevNet/introduction-to-snort-rule-writing
* http://paginas.fe.up.pt/~mgi98020/pgr/writing_snort_rules.htm#rule_options