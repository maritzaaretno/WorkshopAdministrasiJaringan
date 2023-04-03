<p align=center>
LAPORAN RESMI <br>
WORKSHOP ADMINISTRASI JARINGAN </br>
PRAKTIKUM 3<br><br>

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

### 1. Setting IP dan Interface
Untuk setting IP dan interface menggunakan winbox. Winbox sendiri merupakan sebuah aplikasi yang digunakan untuk konfigurasi Mikrotik RouterOS menggunakan GUI. langkah pertama yang dilakukan menjalankan winbox melalui terminal menggunakan perintah <b>wine winbox64.exe</b><br>
![Buka Winbox via terminal](Kel4/0.jpeg)
<br>Setelah menjalankan perintah diatas maka akan muncul tampilan seperti gambar dibawah<br>
![Buka Winbox](Kel4/0_1.jpeg)
<br>Untuk mengatur IP Address, pada bagian menu samping pada winbox click IP lalu addresses<br>
![Setting IP Address](Kel4/1.jpeg)
<br>Kemudian akan muncul tampilan seperti gambar dibawah, Selanjutnya tambahkan ip address pada tanda plus yang diberi panah<br>
![IP Address](Kel4/1_2.jpeg)
<br>Masukkan address <b> 192.168.4.1</b> dengan Network <b>192.168.4.0</b> dan pilih inteface <b>ethernet 2</b> selanjutnya click <b>Apply</b>, maka IP yang telah dimasukkan akan tampil pada address list

![New Address2](Kel4/4.jpeg)

### 2. Seting Default Gateway 0.0.0.0/0 IP Route Gateway 10.252.108.212
<br>Untuk setting IP Routes dan Default Gateway click IP kemudian Routes<br>

![IP_ROUTES](Kel4/9.jpeg)
<br>kemudian pada tab routes tambahkan menggunakan icon yang diberi tanda panah lalu click<br>

![IP_ROUTES](Kel4/10.jpeg)
<br> Masukkan IP <br>
![IP_ROUTES](Kel4/11.jpeg)
<br>Masukkan Default gateway<br>
![IP_ROUTES](Kel4/13.jpeg)
<br>
List IP Address yang di inputkan<br>
<b>Kelompok 1: </b><br>
Gateway : 10.252.108.20<br>
Network Address : 192.168.10.1<br><br>
<b>Kelompok 2: </b><br>
Gateway : 10.252.108.12<br>
Neywork Address : 192.168.2.1<br><br>
<b>Kelompok 3: </b><br>
Gateway: 10.252.108.13<br>
Network Address : 192.168.3.1<br><br>
<b>Kelompok 4: </b><br>
Gateway : 10.252.108.14<br>
Network Address : 192.168.4.1<br><br>
<b>Kelompok 5: </b><br>
Gateway : 10.252.108.15<br>
Network Address : 192.168.5.1<br><br>
<b>Kelompok 6: </b><br>
Gateway : 10.252.108.16<br>
Network Address : 192.168.6.1<br><br>
<b>Kelompok 7: </b><br>
Gateway : 10.252.108.17<br>
Network Address : 192.168.7.1<br><br>
<b>Kelompok 8: </b><br>
Gateway : 10.252.108.18<br>
Network Address : 192.168.8.1<br><br>
<b>Kelompok 9: </b><br>
Gateway : 10.252.108.19<br>
Network Address : 192.168.9.1<br><br>

![IP_ROUTES](Kel4/12.jpeg)

### 3. Setting DHCP Server via DHCP setup [192.168.X.100 - 254]
Pada menu pilih <b>IP</b> kemudian akan muncul opsi pilih <b>DHCP Server</b><br>
![IP_DHCPSERVER](Kel4/2_0.jpeg)
<br>Selanjutnya pada bagian DHCP pilih <b>DHCP Setup</b> seperti pada gambar yang diberi tanda panah, kemudian pilih <b>ethernet2</b> pada interface, Masukkan Address, dan Gateway serta masukkan range yakni <b>192.168.4.100 - 192.168.4.254</b></br>

Pilih Interface eth2<br>
![DHCPsetup](Kel4/5.jpeg)

<br>Masukkan Address dan gateway<br>

![DHCPsetup](Kel4/6.jpeg)
![DHCPsetup](Kel4/7.jpeg) 
<br> Masukkan Range yakni 192.168.4.100 - 192.168.4.254<br>

![DHCPsetup](Kel4/22.jpeg)
<br> Masukkan DNS Server</br>

![IP_ROUTES](Kel4/23.jpeg)


### 4. Sambungkan PC/Laptop ke jaringan, Check IP Address Pastikan IP Address dari PC mendapatkan IP Address dan DHCP server
Untuk menyambungkan laptop/PC ke jaringan buka Control Panel, Network and Internet, Network Connections selanjutnya pilih Ethernet2<br>
![IP_ROUTES](Kel4/14.jpeg)
<br>Selanjutnya click properties

![IP_ROUTES](Kel4/15.jpeg)
<br> Selanjutnya pilih IPv4 <br>

![IP_ROUTES](Kel4/16.jpeg)
<br> Pada general pilih Obtain an IP address automatically dan Obtain DNS Server address automatically, dimana kita akan mendapatkan ip secara otomatis <br>

![IP_ROUTES](Kel4/17.jpeg)

<br> Kemudian cek pada Network Connection Details pada IPv4 Address, Default gateway dan DHCP server masing masing telah mendapatkan<br>

![IP_ROUTES](Kel4/18.jpeg)

### 5. Power up, Nyalakan PC VM anda pastikan konfigurasi BRIDGE, Pastikan mendapatkan IP Adddress dari DHCP Server
Pada VM Pergi ke settings kemudian pada network pastikan attached to Bridged adapter<br>
![IP_ROUTES](Kel4/19.jpeg)

### 6. Konfigurasi IP VM menjadi static, IP: 192.168.X.10
Untuk mengkonfigurasikan IP VM kita konfigurasikan melalui terminal, dengan menjalankan perintah sudo nano /etc/network/interfaces kemudian enter<br>
![IP_ROUTES](Kel4/21.jpeg)
<br> Pada sudo nano tambahkan enp0s3, iface enp0s3 inet static, masukkan address 192.168.4.10 serta netmask dan gateway selanjtnya simpan lalu ctrl exit.<br>

![IP_ROUTES](Kel4/20.jpeg)
<br> Lakukan reastart<br>

![IP_ROUTES](Kel4/24.jpeg)
![IP_ROUTES](Kel4/25.jpeg)
### 7. Konfigurasi NTP ke 0.id.pool.ntp.org, 1.id.pool.ntp.org

Merubah pengaturan sistem waktu, Set sistem timezone menggunakan command dibawah<br>
![IP_ROUTES](Kel4/26.jpeg)
<br> Aktifkan klien NTP untuk sinkronisasi waktu. Edit timesyncd.conf untuk menentukan server NTP yang Anda gunakan<br>

![IP_ROUTES](Kel4/27.jpeg)
<br>Jika jaringan ditutup, tentukan server NTP lokal seperti gambar dibawah, masukkan NTP=0.id.pool.ntp.org kemudian simpan<br>

![IP_ROUTES](Kel4/28.jpeg)
<br>Restart layanan sinkronisasi waktu. kemudian konfirmasikan layanan sinkronisasi waktu aktif. Selanjutnya Periksa pengaturan waktu dan tanggal.<br>

![IP_ROUTES](Kel4/29.jpeg)
![IP_ROUTES](Kel4/30.jpeg)

### 9. Ganti Hostname VM [/etc/hostname server10.kelompokX.takehome.com]
<br>Untuk mengganti Hostname pada VM, buka terminal pada VM selanjutnya jalankan perintah <b>sudo nano /etc/hostname<b>

![IP_ROUTES](Kel4/31.jpeg)
<br>setelah itu masukkan <b> server10.kelompok4.takehome.com<b>

![IP_ROUTES](Kel4/32.jpeg)
