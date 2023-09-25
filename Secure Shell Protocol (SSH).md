Nama  : Amirotul Ummah <br>
NRP  : 3122600017 <br>
Kelas  : 2 D4 IT A <br>
Mata Kuliah  : Praktikum Konsep Jaringan

# SECURE SHELL PROTOCOL (SSH)

SSH merupakan singkatan dari Secure Shell, yakni protokol administrasi yang memungkinkan pengguna untuk mengontrol dan memodifikasi server secara remote dan aman, mulai dari membuat folder, mengedit file, membuat file, transfer file, hingga menjalankan atau menghentikan sebuah sevices. SSH biasanya digunakan oleh administrator untuk mengelola sistem ataupun aplikasi tertentu dari jarak jauh.

## Kegunaan SSH

1. Kemanan Koneksi <br> SSH digunakan untuk mengenkripsi komunikasi antara dua komputer, sehingga informasi yang dikirimkan antara keduanya tidak dapat dengan mudah disadap oleh pihak ketiga.
2. Akses Jarak Jauh <br> SSH sering digunakan untuk mengakses dan mengelola komputer atau server dari jarak jauh. Ini memungkinkan administrator sistem untuk melakukan tugas administratif tanpa harus berada secara fisik di dekat komputer atau server tersebut.
3. Transfer File <br> SSH mendukung transfer file yang aman melalui SCP (Secure Copy) atau SFTP (SSH File Transfer Protocol).
4. Melakukan manajemen komponen dari infrastruktur jaringan secara aman
5. SSH akan memutus koneksi secara otomatis apabila ada aktivitas yang emncurigakan pada koneksi yang digunakan. Sehingga dapat terhindar dari berbagai ancaman siber seperti spoofing IP dan DNS manipulasi data, pelacakan illegal, dan sebagainya.

## RFC SSH

SSH meruapkan sebuah protokol yang diatur dan didokumentasikan dalam serangkaian RFC. RFC-4251 hingga RFC-4256, serta RFC-4250 hingga RFC-4257, mendefinisikan protokol SSH, praktik terkait, dan komponen-komponennya, seperti metode autentikasi, protokol transportasi, protokol sesi, dan lain-lain. RFC pada SSH memberikan panduan resmi tentang cara SSH bekerja, apa yang diharapkan dari implementasi SSH, dan bagaimana menggunakannya dengan benar. Berikut merupakan penjelasan terkait RFC SSH :
1. RFC-4251 (2006) <br> RFC-4251 adalah spesifikasi dasar SSH. Ini menjelaskan struktur pesan, format pesan, dan metode autentikasi yang digunakan dalam protokol SSH. Dokumen ini merupakan dasar dari implementasi SSH yang lebih lanjut.
2. RFC-4252 (2006) <br> RFC-4252 menjelaskan metode autentikasi yang digunakan dalam SSH. Ini termasuk autentikasi berbasis kata sandi dan autentikasi berbasis kunci publik. Dokumen ini mengatur cara pengguna mengidentifikasi diri kepada server SSH.
3. RFC-4253 (2006) <br> RFC-4253 mendeskripsikan protokol transportasi SSH. Ini mencakup negosiasi algoritma enkripsi, pemisahan koneksi multiplex, dan manajemen enkripsi data yang dikirimkan antara klien dan server. Dokumen ini membahas aspek keamanan komunikasi SSH.
4. RFC-4254 (2006) <br> RFC-4254 adalah tentang protokol sesi SSH. Ini mengatur bagaimana sesi komunikasi SSH diinisiasi dan dikelola, termasuk pengiriman perintah dari klien ke server SSH. Dokumen ini juga mencakup transfer file aman melalui protokol SCP (Secure Copy) dan SFTP (SSH File Transfer Protocol).
5. RFC-4250 (2006) <br> RFC-4250 adalah dokumen yang menjelaskan panjang lebar tentang format pesan dan nilai yang digunakan dalam protokol SSH. Ini mencakup definisi untuk kode kesalahan, pesan negosiasi, dan struktur data lain yang digunakan dalam komunikasi SSH.
6. RFC-4255 (2006) <br> RFC-4255 menjelaskan penggunaan kata sandi dalam autentikasi SSH, memberikan pedoman tentang keamanan kata sandi dalam konteks SSH, serta menyarankan praktik terbaik dalam manajemen kata sandi.
7. RFC-4256 (2006) <br> RFC-4256 adalah dokumen yang memberikan panduan tentang otentikasi kunci publik dalam SSH. Ini menjelaskan bagaimana kunci publik dan privat digunakan dalam proses autentikasi SSH.

Dengan adanya RFC tersebut, SSH memiliki dasar standar yang kuat yang merinci spesifikasi protokol dan praktik terkait.

## Karakteristik SSH

Karakteristik utama dari SSH melibatkan aspek keamanan, otentikasi, enkripsi, dan akses jarak jauh. Berikut karakteristik dari SSH: 
1. Keamanan Koneksi <br> SSH dirancang untuk mengamankan komunikasi Anda. Ketika Anda menggunakan SSH, semua data yang dikirimkan antara komputer Anda dan komputer atau server tujuan akan dienkripsi. Ini berarti jika ada pihak ketiga yang mencoba menyadap komunikasi, mereka tidak akan dapat membaca data yang dikirimkan.
2. Otentikasi yang Kuat <br> SSH memungkinkan Anda untuk mengautentikasi (mengidentifikasi) diri Anda secara aman ke server. Ada beberapa cara untuk melakukannya, termasuk menggunakan kata sandi atau kunci publik/privat. Metode otentikasi dengan kunci publik/privat lebih aman dibandingkan kata sandi, karena sulit untuk diretas.
3. Portabilitas <br> SSH dapat digunakan di berbagai platform dan sistem operasi. Ini membuatnya sangat fleksibel dan dapat diimplementasikan di berbagai perangkat, termasuk komputer, server, router, dan perangkat lainnya.
4. Akses Jarak Jauh <br> Salah satu penggunaan utama SSH adalah untuk mengakses komputer atau server dari jarak jauh. Ini berarti Anda dapat mengendalikan komputer atau server tersebut tanpa harus berada di dekatnya secara fisik. Ini sangat berguna untuk administrator sistem yang perlu mengelola banyak perangkat.
5. Transfer File Aman <br> SSH juga mendukung transfer file aman melalui protokol seperti SCP (Secure Copy) atau SFTP (SSH File Transfer Protocol). Anda dapat mengirim atau menerima file dengan aman tanpa risiko data dicuri dalam prosesnya.
6. Tunneling Aman <br> SSH mendukung pembuatan saluran aman (tunnel) yang dapat digunakan untuk mengalirkan lalu lintas data yang tidak aman melalui koneksi SSH yang aman. Ini berguna untuk mengamankan aplikasi yang tidak memiliki tingkat keamanan yang memadai sendiri.
7. Integrasi Keamanan <br> SSH menyediakan berbagai mekanisme keamanan, termasuk enkripsi data, integritas data (untuk memastikan data tidak dimodifikasi selama transmisi), dan otentikasi kuat, semuanya dikombinasikan untuk memberikan perlindungan yang kokoh.
8. Komunitas dan Standar Terbuka <br> SSH adalah protokol yang sangat diterima dan digunakan secara luas di seluruh dunia. Ini didasarkan pada standar terbuka dan telah diuji dan diperbaiki oleh komunitas pengembang.
   
SSH menggunakan teknologi enkripsi untuk menjamin proses transfer informasi yang aman antara server dengan client. SSH sendiri menggunakan 3 teknik enkripsi yaitu :

1. Enkripsi Simetris (Symmetric Encryption):
Enkripsi simetris adalah cara di mana SSH mengamankan data dengan menggunakan sepasang kunci yang sama di server dan client. Kunci ini digunakan untuk mengenkripsi dan mendekripsi pesan. Proses ini dilakukan dengan cara rahasia sehingga data tidak dapat disadap oleh pihak ketiga selama pertukaran data berlangsung.

2. Enkripsi Asimetris (Asymmetric Encryption):
Enkripsi asimetris melibatkan dua kunci yang berbeda, yaitu public key dan private key. Public key digunakan untuk mengenkripsi pesan, sementara private key digunakan untuk mendekripsi pesan. Kunci ini terkait, tetapi private key harus dijaga kerahasiaannya. Enkripsi asimetris digunakan dalam proses pertukaran kunci sebelum koneksi SSH aman terjalin.

3. Hashing:
Hashing adalah teknik kriptografi yang menghasilkan enkripsi satu arah (one-way-hash). Ini digunakan untuk memverifikasi integritas pesan dan mencegah manipulasi data selama pertukaran. Hashing menghasilkan enkripsi yang panjang dan unik yang tidak dapat dengan mudah diuraikan. SSH menggunakan hashing untuk memastikan pesan tetap utuh dan tidak dimanipulasi selama komunikasi.

Dalam penggunaan SSH, enkripsi simetris dan hashing digunakan untuk menjaga kerahasiaan dan integritas data, sementara enkripsi asimetris digunakan dalam proses pertukaran kunci untuk mengamankan koneksi awal antara client dan server. Ini menjadikan SSH sebagai protokol yang aman untuk mengakses dan mengelola perangkat jarak jauh.








