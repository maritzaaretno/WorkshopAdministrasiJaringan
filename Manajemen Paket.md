% ** LAPORAN RESMI
% WORKSHOP ADMINISTRASI JARINGAN </br>
% PRAKTIKUM 1 : MANAJEMEN PAKET **














% ** Dosen Pengampu: **
 Dr. Ferry Astika Saputra ST, M.Sc	

% ** Disusun Oleh:**
Maritza Retno Dwianti
<br> 3121600054
<br> 2 D4 IT B


PROGRAM STUDI TEKNIK INFORMATIKA
POLITEKNIK ELEKTRONIKA NEGERI SURABAYA
TAHUN 2023
# 1.	EVOLUSI SISTEM OPERASI, DEBIAN DAN UBUNTU

A.	SISTEM OPERASI
Sistem operasi merupakan perangkat lunak sistem yang mengelola sumber daya perangkat keras dan perangkat lunak komputer, dan menyediakan layanan umum untuk program komputer. Seiring dengan perkembangan teknologi Sistem Operasi atau OS tentunya terdapat evolusi atau perubahan, Berikut merupakan Evolusi dari Sistem Operasi:

SERIAL PROCESSING (1940 - 1950)
Pada periode ini computer belum memiliki sistem operasi sehingga hanya terdapat bilangan biner yang dapat dioperasikan. Komputer berjaln dengan console yang meliputi lampu sebagai tanda indicator, toggle switch, dan input device. Terdapat kekurangan yakni pada penjadwalan proses yang masih dilakukan manual, dan proses yang dilakukan masih serial sehingga ketika terjadi kegagalan maka seluruh proses akan dilakukan dari awal lagi

SIMPLE BATCH SYSTEM (1950 - 1960)
Adanya software bernama monitor yang berfungsi mengatur dan memantau aktifitas  proses yang dilakukan oleh pc secara otomatis, dan software ini berhasil mengatasi masalah serial. Terdapat masalah pada sistem ini seperti, Memory Protection, Privilaged Instruction yakni pengguna dapat melakukan perintah apapun terhadap komputer, terjadinya interupsi sewaktu waktu, dan waktu.

MULTIPROGRAMMING BATCH SYSTEM 
Penggunaan prosesor yang maksimal, karena pada umumnya prosesor akan berhenti bekerja ketika menunggu input user. Moment berhenti ini dimanfaatkan untuk melakukan proses lain. Jadi prosessor akan terus bekerja dan membutuhkan sedikit waktu

TIME SHARING SYSTEM (1960 – 1970)
Digunakannya sistem multiprogramming namun adanya pembatasan waktu pengerjaan. Program akan diberikan alokasi waktu apabila jalannya program tersebut melewati         waktu maka akan dihentikan secara otomatis. Hal ini masih digunakan hingga sekarang. Terdapat kekurangan seperti pengaksesan memori, kurangnya proteksi        
terhadap system file, dan pembagian sumber daya yang dinilai kurang efektif

PERSONAL COMPUTER (1980)
Adanya DOS (Disk Operating System) yang mulai popular yang digunakan pada computer pribadi. Merupakan sistem operasi yang berorientasi pada command prompt menggunakan perintah teks

OS JARINGAN (1990 – 2000)
MOBILE (2000 – SEKARANG)
Seperti adanya android dan iOS yang mendukung perangkat mobile seperti smartphone, tablet dan lain lain

B. DEBIAN DAN UBUNTU
UBUNTU : Ubuntu merupakan OS Linux berbasis Debian dan dibangun menggunakan infrastruktur Debian yang terdiri dari server, desktop dan OS Linux
DEBIAN : Debian merupakan OS Linux Debian, juga dikenal sebagai Debian GNU/Linux, yang merupakan distribusi Linux yang terdiri dari perangkat lunak bebas dan sumber   terbuka, yang dikembangkan oleh komunitas yang didukung

FEDORA : Sebelumnya Fedora ini bernama Fedora Core, dan juga disebut dengan Fedora Linux merupakan sebuah distro Linux berbasis RPM dan yum yang dikembangkan oleH Fedora Project yang didukung oleh komunitas pemrogram serta disponsori oleh Red Hat

CentOS (Community ENTerprise Operating System) : CentOS merupakan sebuah distribusi linux sebagai bentuk dari usaha untuk menyediakan platform komputasi berkelas enterprise yang memiliki kompatibilitas kode biner sepenuhnya dengan kode sumber yang menjadi induknya, yakni Red Hat Enterprise Linux (RHEL)
         
OpenSUSE : Sistem operasi komputer yang dibangun di atas kernel Linux yang dikembangkan secara independent. Tujuan Proyek openSUSE sendiri untuk memperkenalkan penggunaan Linux di manapun dengan menciptakan distribusi Linux yang stabil dan ramah pengguna dan dapat digunakan sebagai sistem operasi untuk desktop dan server.

# 2.	SU DAN SUDO
SU (Switch User) : Digunakan untuk beralih ke akun root dan juga user harus memasukkan kata sandi root setelah masuk ke akun root pengguna dapat melakukan dan menjalan perintah yang tidak dapat dilakukan oleh semua user, pada perintah su memiliki akses penuh kedalam sistem dan juga dapat mengubah file pada sistem

SUDO (superuser do) : Sudo akan melakukan perintah sebagai superuser. Pengguna sudo dan perintah-perintah yang dapat mereka pergunakan terdapat pada file konfigurasi, /etc/sudoers. Apabila seorang pengguna yang tidak berhak mencoba menjalankan perintah, sudo akan memberitahu administrator melalui e-mail. Secara default, pemberitahuan peringatan ini akan disimpan di akun root.Pengguna yang mencoba menjalankan perintah akan diminta mengisikan password. Setelah terotentifikasi, sudo akan membuat timestamp untuk pengguna.




3.	PACKAGE MAINTENANCE
3.1.	Setting repo
3.2.	Arti dari versi di repo
3.3.	Contoh instalasi package
3.3.1.	Mc
3.3.2.	Net tools
3.3.3.	htop
