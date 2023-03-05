# RESUME KULIAH TAMU : CLOUD SECURITY
* WORKSHOP ADMINISTRASI JARINGAN
* MARITZA RETNO DWIANTI_3121600054
* Dosen Pengampu : Dr. Ferry Astika Saputra ST, M.Sc

# TREND OF THE CLOUD SECURITY
1.	The Threats
2.	The Attacks
3.	The Security
4.	The Tools
5.	The Tests
6.	Summary

# INTRODUCTION
   Komputasi Awan merupakan model yang menawarkan layanan komputasi instan tanpa menanggung biaya. Seperti teknologi lainnya, terdapat kekurangannya. Salah satu masalah utama adalah masalah keamanan dan privasi salah satunya seperti kebocoran pada data karena infrastruktur sumber daya komputasi bersama untuk memproses informasi bisnis rahasia seperti, kekayaan intelektual, rahasia dagang, dan informasi rahasia pelanggan, yang dapat menyebabkan aktor yang tidak sah dapat mengaksesnya.

# A. THE THREATS
1. Kehilangan dan Kebocoran Data
   Fitur perlindungan data cloud untuk perusahaan sebagian ditawarkan secara terpisah sebagai layanan opsional dan tambahan, misalnya seperti penyimpanan tambahan untuk retensi snapshot dan anti ransomware karena sumber dayanya luas dan mahal. Data enkripsi dan backup merupakan basic, atleast terdapat 2-3 backup. Keduanya opsional maka dari itu  harus berlangganan untuk cloud itu
   
2. Penyalahgunaan dan Penggunaan yang salah
   Karena komputasi awan adalah ekosistem berbagai layanan, interaksi, dan saling ketergantungan, menjadi lebih umum. Eksploitasi (PaaS) untuk "Peretasan sebagai Layanan" dapat lebih menantang untuk dimitigasi karena tersembunyi di infrastruktur yang sama

3. Antarmuka dan API tidak aman
   Memanfaatkan risiko spionase (mata – mata) bisnis yang tidak aman, berpotensi mengakibatkan adanya kompromi pencurian data sensitif dan data pribadi

4. Masalah Teknologi Bersama
   Penyedia layanan cloud menggunakan infrastruktur yang dapat diskalakan untuk mendukung banyak penyewa yang berbagi infrastruktur dasar. Di lapisan paling bawah, di mana hypervisor dapat dieksploitasi dari mesin virtual yang dikompromikan di penyewa lain untuk mendapatkan akses ke semua VM di lingkungan bersama yang sama

# VIRTUALISASI
   Virtualisasi merupakan sebuah teknologi yang memungkinkan satu infrastruktur fisik berfungsi sebagai beberapa infrastruktur atau sumber daya logis, mengurangi jumlah besar yang diinvestasikan untuk membeli sumber daya tambahan adalah teknik, yang mengikuti pembagian satu contoh fisik aplikasi atau sumber daya di antara banyak organisasi atau penyewa.
   Virtualisasi perangkat keras adalah abstraksi sumber daya komputasi dari perangkat lunak yang menggunakan sumber daya tersebut. Virtualisasi perangkat keras juga disebut virtualisasi server, virtualisasi perangkat keras menginstal hypervisor atau manajer mesin virtual (VMM), yang menciptakan lapisan abstraksi antara perangkat lunak dan perangkat keras yang mendasarinya
   Lingkungan virtualisasi dikelola oleh perangkat lunak atau firmware, yang dikenal sebagai hypervisor. Hypervisor rentan terhadap semua jenis serangan untuk infrastruktur normal
   
#HYPERJACKING
   Untuk menginfeksi sistem berbasis komputasi awan dengan dos hypervisor, penyerang harus memiliki kendali atas hypervisor, penyerang menggunakan rootkit yang diinstal pada VM (Mesin Virtual) untuk menyerang untuk mendapatkan kendali atas hypervisor, upaya seperti itu oleh penyerang dunia maya adalah didefinisikan sebagai hyper-jacking. jika seorang penyerang berhasil melakukan hyper jack kekuatan hypervisor, itu bisa mendapatkan kendali atas seluruh hosting. akibatnya, penyerang dapat mengubah perilaku dan menyebabkan kerusakan pada VM
   
# B. SERANGAN
1. Serangan Tingkat Mesin Virtual
   Serangan pada platform Cloud yang sama dapat mempengaruhi penyewa lainnya. Wajib bagi penyebaran Cloud apa pun untuk mengeraskan lapisan virtualisasi untuk mencegah serangan VM ke VM.
2. Pembajakan Layanan dan Sesi
3. Man in the Cloud dan DDoS

# C. KEAMANAN
1. Lapisan Kontrol Awan
   Gunakan lapisan kontrol tambahan dalam manajemen Cloud dari 3% penyedia solusi pihak, terutama untuk penyebaran multi-cloud.
2. Tanggung Jawab Bersama
   Gunakan "perjanjian back-to-back" dengan Penyedia Cloud Anda untuk memastikan kepatuhan standar keamanan penuh.
   
# D. ALAT - ALAT
   Keamanan yang Ditetapkan Perangkat Lunak; yakinkan kembali solusi Keamanan Cloud tertinggi yang tersedia. Otentikasi Multifaktor Kemajuan AAA untuk setiap Lapisan Cloud misalnya kombinasi biometrik wajib

# E. TES
1.	Isolasi Sumber Daya Cloud; mencegah serangan pivot VM ke VM.
2.	Periksa Masalah Penguncian; cegah terjebak dalam produk yang rentan.
3.	Periksa Masalah Tata Kelola; yakinkan kembali standar praktik terbaik.
4.	Periksa Masalah Kepatuhan; hindari sanksi dan hukuman.
5.	Periksa Integritas Data, Retensi, dan Pembuangan; mencegah kebocoran dan kerugian.

# RINGKASAN
   Diskusi ini menyampaikan masalah keamanan yang terkait dengan layanan cloud. Tercatat bahwa penjahat dunia maya telah mengambil keuntungan dari kerentanan dalam ekosistem bersama dan kurangnya kontrol keamanan yang efektif, yang menyebabkan penyalahgunaan platform. Peretas dapat secara ilegal mengakses informasi rahasia penyewa lain yang berada di infrastruktur cloud yang sama. Oleh karena itu, bisnis disarankan untuk melakukan penilaian risiko berkelanjutan untuk mengurangi potensi ancaman terhadap data sensitif mereka. Selanjutnya, penyedia keamanan cloud harus meningkatkan perlindungan keamanan melalui penerapan langkah-langkah keamanan proaktif yang lebih canggih dan canggih untuk mengatasi tantangan ini.

