<p align=center>
LAPORAN RESMI <br>
WORKSHOP ADMINISTRASI JARINGAN </br>
PRAKTIKUM 5 - PRAKTIKUM DNS SERVER<br><br>

<p align=center>
Dosen Pengampu:<br>
Dr. Ferry Astika Saputra ST, M.Sc<br><br>

<p align=center>
Disusun Oleh:<br>
Hanif Nabila [ 3121600046 ]<br>
Maritza Retno Dwianti [ 3121600054 ]<br>
Muhammad Hafid Azis [ 3121600055 ]<br>
2 D4 IT B<br><br>

<p align=center>
PROGRAM STUDI TEKNIK INFORMATIKA<br>
POLITEKNIK ELEKTRONIKA NEGERI SURABAYA<br>
TAHUN 2023
</p>
<br><br><br>

# Topologi
![Topologi](img/Topologi.jpg)

### 1. Instalasi Paket DNS Server
Untuk konfigurasi DNS Server, pertama yang dilakukan adalah melakukan instalasi beberapa paket seperti:<br>
1. bind9
2. bind9-utils
3. dnsutils
4. resolvconf
<br>
Masuk sebagai user root:<br>

![Masuk su](img/1.jpeg)

<br>Kemudian lakukan instalasi beberapa paket diatas menggunakan command <b> apt-get install</b><br>

![apt get-isntall](img/2.jpeg)

<br>Click Y untuk melanjutkan proses instalasi<br>

![apt get-install](img/3.jpeg)

![apt get-install](img/4.jpeg)

### 2. Lakukan Check DNS 
Setelah melakukan instalasi, kemudian lakukan Check status DNS. menggunakan command <b>/etc/init.d/bind9 status</b><br>
![Check DNS Status](img/5.jpeg)

### 3. Melakukan Konfigurasi Pada DNS Server
Sebelum melakukan konfigurasi, kita harus masuk kedalam directory menggunakan comman <b>cd /etc/bind</b> setelah itu lakukan copy file menggunakan command <b>cp db.127 db.192</b> dan <b>cp db.local db.kel4</b><br>
![open direct dan copy](img/6.jpeg)
<br>Lakukan perubahan pada file db.192, untuk melakukan pengeditan file dapat menggunakan perintah <b>nano</b> kemudian tambahkan nama domain yang akan digunakan<br>
![edit db.192](img/7.jpeg)
<br>Gambar dibawah merupakan file yang belum diedit<br>
![edit db.192](img/8.jpeg)
<br>Lakukan pengeditan pada localhost<br>
![edit db.192](img/9.jpeg)
<br>Edit localhost tersebut menjadi <b>kampus-04.takehome.com</b><br>
![edit db.192](img/10.jpeg)
<br>Kemudian replace<br>
![edit db.192](img/11.jpeg)
<br>Edit semua localhost diganti menjadi <b>kampus-04.takehome.com</b><br>
![edit db.192](img/12.jpeg)
<br>Kemudian simpan<br>
![edit db.192](img/13.jpeg)
![edit db.192](img/14.jpeg)

<br><br>Selanjutnya lakukan pengeditan pada file db.kel4<br>
![edit db.kel4](img/15.jpeg)
<br>Dibawah ini merupakan file yang belum diedit<br>
![edit db.kel4](img/16.jpeg)
<br>Search localhost untuk dilakukannya pengeditan atau replace<br>
![edit db.kel4](img/17.jpeg)
<br>Replace <b>localhost</b> dengan <b>kampus-04.takehome.com<br>
![edit db.kel4](img/18.jpeg)
<br>Click Y untuk melakukan replace<br>
![edit db.kel4](img/19.jpeg)
<br>Maka file yang telah diedit / direplace akan menjadi tampilan dibawah.<br>
![edit db.kel4](img/20.jpeg)

### 4. Melakukan Konfigurasi pada Default-zones

Buka file menggunakan command <b>nano named.conf.default-zones</b><br>

![konfig default-zones](img/21.jpeg)

<br>Pada file tersebut tambahkan sebuah text, kemudian simpan<br>
![konfig default-zones](img/22.jpeg)

### 5. Menambahkan Teks pada resolv.conf
Jalankan perintah nano untuk megedit file tersebut<br>
![resolv](img/23.jpeg)

<br><br>setelah masuk pada file, lakukan pengeditan dan tambahkan <b>nameserver 192.168.4.10</b><br>

![konfig default-zones](img/24.jpeg)
<br>Setelah itu simpan dan lakukan restart pada bind9<br>
![konfig default-zones](img/25.jpeg)
![konfig default-zones](img/26.jpeg)

## 6. Lakukan Pengujian Hasil Konfigurasi DNS Server

Untuk pengujian hasil konfigurasi gunakan command nslookup<br>

![Uji DNS](img/27.jpeg)

<br>Lakukan test ping pada server dan client<br>
1. Client<br>
![ping client](img/28.jpeg)
2. Server<br>
![ping server](img/29.jpeg)
