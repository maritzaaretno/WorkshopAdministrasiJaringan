<p align=center>
LAPORAN RESMI <br>
WORKSHOP ADMINISTRASI JARINGAN </br>
PRAKTIKUM 1 : MANAJEMEN PAKET

<p align=center>
Dosen Pengampu:<br>
Dr. Ferry Astika Saputra ST, M.Sc	

<p align=center>
Disusun Oleh:<br>
Maritza Retno Dwianti
<br> 3121600054
<br> 2 D4 IT B

<p align=center>
PROGRAM STUDI TEKNIK INFORMATIKA<br>
POLITEKNIK ELEKTRONIKA NEGERI SURABAYA<br>
TAHUN 2023
</p>

## 1.	EVOLUSI SISTEM OPERASI, DEBIAN DAN UBUNTU

### A.	SISTEM OPERASI
Sistem operasi merupakan perangkat lunak sistem yang mengelola sumber daya perangkat keras dan perangkat lunak komputer, dan menyediakan layanan umum untuk program komputer. Seiring dengan perkembangan teknologi Sistem Operasi atau OS tentunya terdapat evolusi atau perubahan, Berikut merupakan Evolusi dari Sistem Operasi:

**SERIAL PROCESSING (1940 - 1950)**<br>
Pada periode ini computer belum memiliki sistem operasi sehingga hanya terdapat bilangan biner yang dapat dioperasikan. Komputer berjaln dengan console yang meliputi lampu sebagai tanda indicator, toggle switch, dan input device. Terdapat kekurangan yakni pada penjadwalan proses yang masih dilakukan manual, dan proses yang dilakukan masih serial sehingga ketika terjadi kegagalan maka seluruh proses akan dilakukan dari awal lagi

**SIMPLE BATCH SYSTEM (1950 - 1960)**<br>
Adanya software bernama monitor yang berfungsi mengatur dan memantau aktifitas  proses yang dilakukan oleh pc secara otomatis, dan software ini berhasil mengatasi masalah serial. Terdapat masalah pada sistem ini seperti, Memory Protection, Privilaged Instruction yakni pengguna dapat melakukan perintah apapun terhadap komputer, terjadinya interupsi sewaktu waktu, dan waktu.

**MULTIPROGRAMMING BATCH SYSTEM**<br>
Penggunaan prosesor yang maksimal, karena pada umumnya prosesor akan berhenti bekerja ketika menunggu input user. Moment berhenti ini dimanfaatkan untuk melakukan proses lain. Jadi prosessor akan terus bekerja dan membutuhkan sedikit waktu

**TIME SHARING SYSTEM (1960 – 1970)**<br>
Digunakannya sistem multiprogramming namun adanya pembatasan waktu pengerjaan. Program akan diberikan alokasi waktu apabila jalannya program tersebut melewati         waktu maka akan dihentikan secara otomatis. Hal ini masih digunakan hingga sekarang. Terdapat kekurangan seperti pengaksesan memori, kurangnya proteksi        
terhadap system file, dan pembagian sumber daya yang dinilai kurang efektif

**PERSONAL COMPUTER (1980)**<br>
Adanya DOS (Disk Operating System) yang mulai popular yang digunakan pada computer pribadi. Merupakan sistem operasi yang berorientasi pada command prompt menggunakan perintah teks

**OS JARINGAN (1990 – 2000)**<br>
**MOBILE (2000 – SEKARANG)**<br>
Seperti adanya android dan iOS yang mendukung perangkat mobile seperti smartphone, tablet dan lain lain

### B. DEBIAN DAN UBUNTU
**UBUNTU**<br> Ubuntu merupakan OS Linux berbasis Debian dan dibangun menggunakan infrastruktur Debian yang terdiri dari server, desktop dan OS Linux
**DEBIAN**<br> Debian merupakan OS Linux Debian, juga dikenal sebagai Debian GNU/Linux, yang merupakan distribusi Linux yang terdiri dari perangkat lunak bebas dan sumber terbuka, yang dikembangkan oleh komunitas yang didukung

**FEDORA :**<br>Sebelumnya Fedora ini bernama Fedora Core, dan juga disebut dengan Fedora Linux merupakan sebuah distro Linux berbasis RPM dan yum yang dikembangkan oleH Fedora Project yang didukung oleh komunitas pemrogram serta disponsori oleh Red Hat

**CentOS (Community ENTerprise Operating System) :**<br>CentOS merupakan sebuah distribusi linux sebagai bentuk dari usaha untuk menyediakan platform komputasi berkelas enterprise yang memiliki kompatibilitas kode biner sepenuhnya dengan kode sumber yang menjadi induknya, yakni Red Hat Enterprise Linux (RHEL)
         
**OpenSUSE :**<br>Sistem operasi komputer yang dibangun di atas kernel Linux yang dikembangkan secara independent. Tujuan Proyek openSUSE sendiri untuk memperkenalkan penggunaan Linux di manapun dengan menciptakan distribusi Linux yang stabil dan ramah pengguna dan dapat digunakan sebagai sistem operasi untuk desktop dan server.

## 2.	SU DAN SUDO
**SU (Switch User) :**<br>Digunakan untuk beralih ke akun root dan juga user harus memasukkan kata sandi root setelah masuk ke akun root pengguna dapat melakukan dan menjalan perintah yang tidak dapat dilakukan oleh semua user, pada perintah su memiliki akses penuh kedalam sistem dan juga dapat mengubah file pada sistem

**SUDO (superuser do) :**<br>Sudo akan melakukan perintah sebagai superuser. Pengguna sudo dan perintah-perintah yang dapat mereka pergunakan terdapat pada file konfigurasi, /etc/sudoers. Apabila seorang pengguna yang tidak berhak mencoba menjalankan perintah, sudo akan memberitahu administrator melalui e-mail. Secara default, pemberitahuan peringatan ini akan disimpan di akun root.Pengguna yang mencoba menjalankan perintah akan diminta mengisikan password. Setelah terotentifikasi, sudo akan membuat timestamp untuk pengguna.

## 3.	PACKAGE MAINTENANCE
### A. Setting Repository
Langkah - langkah : 
1. Pergi ke terminal pada Ubuntu
2. Gunakan command **sudo nano /etc/apt/sources.list** fungsinya untuk mengedit teks menggunakan perintah nano dan membuka file sources.list
3. Kemudian masukkan password
4. Pada akhir file gunakan **deb [sumber]://[nama server]/[direktori]/[versi] [distro] [main]** untuk menambah sebuah repository
5. Save dan keluar dari nano : Ctrl + x dan pilih Y untuk menyimpan perubahan
![alt text](https://github.com/maritzaaretno/WorkshopAdministrasiJaringan/blob/[branch]/sudo nano1.png?raw=true)
7. Jalankan **sudo apt-get update** yang fungsinya untuk refresh daftar repository
8. Selanjutnya gunakn **sudo apt-get install** untuk menginstall program yang telah ditambahkan sebelumnya
![repo](http://url/to/img.png)
### B. Arti dari versi di Repository
### C. Contoh instalasi package
**APT(Advanced Package Tool)**<br>
APT gunanya untuk mengatur instalasi, tidak hanya instalasi namun juga upgrade dan delete sebuah instalasi sebuah paket pada Linux, cara penggunaannya dengan melalui terminal.<br>
**Perintah APT:**<br>
1. **apt-get update**<br> Update daftar paket yang tersedia di repository Ubuntu.
2. **apt-get upgrade**<br> Install pembaruan untuk paket yang sudah terinstal.
3. **apt-get install [nama_paket]**<br> Melakukan instal paket baru.
4. **apt-get remove [nama_paket]**<br> Menghapus paket yang sudah terinstal.
5. **apt-cache search [kata_kunci]**<br> Mencari paket berdasarkan keywords tertentu.
6. **apt-cache show [nama_paket]**<br> Menampilkan informasi tentang paket tertentu.
7. **apt-get autoremove**<br> Menghapus paket yang tidak diperlukan lagi.
8. **apt-get clean**<br> Membersihkan cache paket yang sudah diunduh.
9. **apt-get purge [nama_paket]**<br> Menghapus paket dan file konfigurasinya.

## Instalasi Package pada Linux
### MC (Midnight Commander)
Merupakan sebuah apk file manager yang dikhususkan untuk Linux. Fitur utama pada sebuah aplikasi file manager seperti copy, rename, hapus file, membuat file, membuat folder.
1. Pada terminal kita akan melakukan instalasi MC.
2. Menggunakan perintah sudo apt-install mc untuk menginstall apk tersebut
3. Setelah instalasi selesai, ketikkan **mc** pada terminal untuk membuka
![alt text](http://url/to/img.png)
###	Net Tools
Merupakan kumpulan tool yang berhubungan dengan jaringan seperti ipconfig, route, hostname, rarp, dan lain lain
1. Pada terminal kita akan melakukan instalasi net-tools.
2. Menggunakan perintah sudo apt-install net-tools untuk menginstall apk tersebut
3. Setelah instalasi selesai, pengguna dapat menlakukan perintah seperti ipconfig dan lain lain
![alt text](http://url/to/img.png)
###	htop
Pada aplikasi htop ini berfungsi untuk melakukan monitoring terhadap kinerja sistem pada OS Linux
1. Pada terminal kita akan melakukan instalasi htop
2. Menggunakan perintah sudo apt-install htop untuk menginstall apk tersebut, kemudian tunggu
3. Setelah instalasi selesai, pengguna dapat menlakukan perintah htop untuk membuka ap yang telah terinstall
![alt text](http://url/to/img.png)
