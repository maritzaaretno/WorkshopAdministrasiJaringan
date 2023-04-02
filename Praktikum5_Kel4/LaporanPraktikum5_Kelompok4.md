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
Untuk konfigurasi DNS Server, pertama yang dilakukan adalah melakukan instalasi beberapa paket seperti:
1. bind9
2. bind9-utils
3. dnsutils
4. resolvconf

Masuk sebagai user root:
![Masuk su](img/1.jpeg)
Kemudian lakukan instalasi beberapa paket diatas menggunakan command <b> apt-get install</b>
![apt get-isntall](img/2.jpeg)
Click Y untuk melanjutkan proses instalasi
![apt get-install](img/3.jpeg)
![apt get-install](img/4.jpeg)

### 2. Lakukan Check DNS 
Setelah melakukan instalasi, kemudian lakukan Check status DNS. menggunakan command <b>/etc/init.d/bind9 status</b>
![Check DNS Status](img/5.jpeg)

### 3. Melakukan Konfigurasi Pada DNS Server
Sebelum melakukan konfigurasi, kita harus masuk kedalam directory menggunakan comman <b>cd /etc/bind</b> setelah itu lakukan copy file menggunakan command <b>cp db.127 db.192</b> dan <b>cp db.local db.kel4</b>
![open direct dan copy](img/6.jpeg)
Lakukan perubahan pada file db.192, untuk melakukan pengeditan file dapat menggunakan perintah <b>nano</b> kemudian tambahkan nama domain yang akan digunakan
![edit db.192](img/7.jpeg)
Gambar dibawah merupakan file yang belum diedit
![edit db.192](img/8.jpeg)
Lakukan pengeditan pada localhost
![edit db.192](img/9.jpeg)
Edit localhost tersebut menjadi <b>kampus-04.takehome.com</b>
![edit db.192](img/10.jpeg)
Kemudian replace
![edit db.192](img/11.jpeg)
Edit semua localhost diganti menjadi <b>kampus-04.takehome.com</b>
![edit db.192](img/12.jpeg)
Kemudian simpan
![edit db.192](img/13.jpeg)
![edit db.192](img/14.jpeg)

Selanjutnya lakukan pengeditan pada file db.kel4
![edit db.kel4](img/15.jpeg)
Dibawah ini merupakan file yang belum diedit
![edit db.kel4](img/16.jpeg)
Search localhost untuk dilakukannya pengeditan atau replace
![edit db.kel4](img/17.jpeg)
replace <b>localhost</b> dengan <b>kampus-04.takehome.com
![edit db.kel4](img/18.jpeg)
Click Y untuk melakukan replace
![edit db.kel4](img/19.jpeg)
Maka file yang telah diedit / direplace akan menjadi tampilan dibawah.
![edit db.kel4](img/20.jpeg)

### 4. Melakukan Konfigurasi pada Default-zones

Buka file menggunakan command <b>nano named.conf.default-zones</b>

![konfig default-zones](img/21.jpeg)

pada file ini tambahkan sebuah text, kemudian simpan
![konfig default-zones](img/22.jpeg)

### 5. Menambahkan Teks pada resolv.conf
Jalankan perintah nano untuk megedit file tersebut
![resolv](img/23.jpeg)

setelah masuk pada file, lakukan pengeditan dan tambahkan <b>nameserver 192.168.4.10</b>

![konfig default-zones](img/24.jpeg)
Setelah itu simpan dan lakukan restart pada bind9
![konfig default-zones](img/25.jpeg)
![konfig default-zones](img/26.jpeg)

## 6. Lakukan Pengujian Hasil Konfigurasi DNS Server

Untuk pengujian hasil konfigurasi gunakan command nslookup

![Uji DNS](img/27.jpeg)

Lakukan test ping pada server dan client<br>
1. Client
![ping client](img/28.jpeg)
2. Server
![ping server](img/29.jpeg)