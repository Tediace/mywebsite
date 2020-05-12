---
title: "Server"
date: 2020-05-08T17:05:46+07:00
draft: true
author: "tedi"
language: "English"
description: "Example article description"
menu: main # Optional, add page to a menu. Options: main, side, footer

categories:
  - "Server"
tags:
  - "Linux"
  - "Server"
  - "Ubuntu"
thumbnail: "img/gns3.png" # Thumbnail image
lead: "Server" # Lead text
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

## GNS3

GNS3 adalah simulator jaringan grafis yang memungkinkan anda untuk merancang topologi jaringan yang kompleks. Anda dapat menjalankan simulasi atau mengkonfigurasi perangkat mulai dari workstation sederhana hingga router yang powerfull seperti Cisco. Hal ini didasarkan pada Dynamips, Pemu/Qemu dan Dynagen.

### Fungsi GNS3
GNS3 sering dipakai sebagai semulator router Cisco, Juniper, Mikrotik dan Virtual Machine.
Jarang terlihat GNS3 dipakai untuk simulator Switch tentunya yang managable seperti
switch Cisco. Namun bukan tidak mungkin kalau GNS3 dapat dipakai untuk mengsimulasikan switch

## Installasi 
#### Lakukan 

```html
sudo add-apt-repository ppa:gns3/ppa
sudo dpkg --add-architecture i386
sudo apt update
sudo apt -y install gns3 gns3-gui gns3-iou gns3-server virtualbox qemu wireshark libpcap-dev git ubridge
chmod 777 /usr/bin/dumpcap
exit
```
Proses instalasi di atas akan secara automatis menginstall ubridge. Ubridge dari ubuntu tampaknya tidak stabil. Tampaknya masih lebih baik compile ubridge sendiri sebagai berikut,

```html
sudo su
apt -y install libpcap-dev git
cd /usr/local/src
rm -Rf /usr/local/src/ubridge/
git clone git://github.com/GNS3/ubridge.git
cd ubridge
make
make install
cp -p ubridge /usr/bin
setcap cap_net_admin,cap_net_raw=ep /usr//bin/ubridge
```
Tiga (3) line terakhit akan menimpa ubridge hasil dari apt install.

Selanjutnya, sebagai user biasa, siapkan directory
```html
mkdir -p ~/GNS3/projects
mkdir -p ~/GNS3/images
```
```html
# optional kalau takut
cd ~
sudo chmod -Rf 777 GNS3
sudo chown -Rf nobody: GNS3
```
## Menjalankan
Sebagai **user biasa**. Jangan sebagai superuser. Tulis di shell
```html
gns3 &
```
## CATATAN:

File konfigurasi di
```html
.config/GNS3
```
Kalau ada error dll, remove dengan
```html
rm -Rf .config/GNS3
```
## Konfigurasi Pertama Kali
### Next 1
Pilih

* Run appliances on my local computer
### Klik 2
```html
Server Path  : /usr/bin/gns3server
Host binding : localhost
Port         : 3080 TCP
```
### Klik 3
Pastikan
```html
Connection to the local GNS3 server has been successful!
```
## FINISH
* Finish
### Referensi
http://www.unixmen.com/install-gns3-graphical-network-simulator-ubuntu-13-04/
https://community.gns3.com/people/rednectar/blog/2014/10/22/installing-gns3v1-on-linux
