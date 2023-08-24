# OSI LAYERS

Model OSI atau Open System Information Reference Model for Open Networking adalah model jaringan yang dikembangkan oleh ISO/International Organization for Standarization pada tahun 1997. Model ini juga disebut dengan OSI Seven Layer Mode atau Model Tujuh Lapis OSI.
OSI bisa membuat suatu perangkat bisa berkomunikasi dengan perangkat lain sesuai dengan protokol. Dengan adanya OSI, manusia bisa saling mengirimkan pesan/informasi antar perangkat dengan mudah dan efisien. OSI layer dapat memudahkan PC, jaringan komputer, serta software develpoment agar bisa tersambung tanpa perlu melakukan pengaturan khusus. OSI Layer bekerja melewati tujuh lapisan yang berurutan. Hal ini dapat memudahkan proses pencarian titik awal permasalahan sehingga pelacakan masalah jaringan dapat dilakukan dengan efisien. Berikut penjelasn 7 lapisan OSI Layer :

### Physical Layer
Lapisan ini adalah lapisan pertama pada OSI yang bertanggung jawab dalam mentransmisikan data dalam bentuk bit stream. Lapisan ini mencakup peraalatan pertukaran informasi, seperti kabel, infrared, cahaya, frekuensi radio, dan tegangan listrik.

### Datalink Layer
Lapisan ini berfungsi untuk mengakhiri koneksi antara dua node atau jaringan yang terhubung secara fisik. Lapisan ini memecah data dari network layer menjadi frame dan mengirimkannya ke tujuan. Selain itu, lapisan ini berfungsi untuk memeriksa bila terjadi kesalahan dalam menyalurkan transmisi. 

### Network Layer
Lapisan ini bertugas mendefinisikan IP Address sehingga antar komputer dapat saling terhubung dalam suatu jaringan. Lalu lapisan ini  akan melakukan proses routing dan membagi data menjadi beberapa paket lalu mengembalikannya setelah data berhasil diterima.

### Transport Layer
Lapisan ini berperan untuk memecah data lalu memasukkanyya ke dalam beberapa paket data, melakukan looping proses transmisi jika paket data hilang, dan menyalurkan bit agar data diterima dengan baik. Secara garis besar, lapisan ini berfungsi untuk mengelola pengiriman data antar perangkat serta memastikan data telah diterima dengan baik dan berurutan.

### Session Layer
Lapisan ini bertanggung jawab atas pemeliharaan sesi komunikasi antar perangkat. Lapisan ini membuka dan menutup saluran komunikasi antar perangkat, saluran akan dibuka pada saat pengiriman data dan saluran akan ditutup ketika komunikasi sudah berakhir. Lapisan ini juga mengatur checkpoint selama komunikasi. Jika lapisan ini terganggu, maka komunikasi maupun transfer data bisa dilanjurkan dari checkpoint yang terakhir.

### Presentation Layer
Lapisan ini mengelola format data dan enkripsi. Ini mengonversi data ke format yang bisa dimengerti oleh penerima dan juga menangani kompresi maupun enkripsi data. Pada lapisan ini data akan terenkripsi dan terdekripsi otomatis melalui sistem. Adapun protokol di lapisan ini seperti MIME, TLS, SSI, dan sebagainya.

### Application Layer
Lapisan ini merupakan lapisan di mana pengguna bisa berinteraksi dengan aplikasi yang menggunakan fungsionalitas jaringan. Aplikasi yang beroperasi pada lapisan ini conothnya web browser dan email. Aplikasi tersebut berhubungan protokol yang digunakan untuk komunikasi antar aplikasi. Contoh protokol yang ada di lapisan ini yakni HTTP dan SMTP


# TCP/IP LAYERS

TCP/IP adalah isingkatan dari Transmission Control Protocol/Internet Protocol. TCP/IP merupakan protokol standar dalam jaringan komputer untuk menjembatani pertukaran data antar perangkat dalam jaringan tersebut. Keduanya merupakan jaringan komputer yang terpisah namun harus bekerja sama.
IP merupakan server untuk memperoleh alamat tujuan data dikirimkan sedangkan TCP berfungsi untuk mengirim data setelah alamat ditemukan oleh IP.
Model TCP/IP memecah pesan menjadi paket-paket untuk meminimalisir pengiriman ulang seluruh pesan jika terdapat kesalahan selama transmisi. Paket data harus melewati empat lapisan sebelum diterima oleh perangkat tujuan dan TCP/IP melewati lapisan dalam urutan terbalik untuk mengembalikan pesan ke format aslinya.
Adapun empat lapisan (layer) dalam TCP/IP yakni :

### Datalink
Lapisan ini mengatur aliran data antara dua perangkat di jaringan yang langsung terhubung. Ini juga mengatur deteksi kesalahan dalam transmisi data dan mengatur alamat fisik perangkat (MAC addresses). Lapisan ini juga mengatur bagaimana data dikirim, bagaimana data harus diberi sinyal oleh hardware dan perangkat transmisi lain di jaringan, serta bertanggung jawab untuk mentransmisikan data antara aplikasi atau perangkat dalam jaringan

### Internet
Layer ini bertanggung jawab untuk mengirim paket dari jaringan mengendalikan pergerakan paket di seluruh jaringan untuk memastikan apakah paket-paket tersebut sudah sampai tujuan. Lapisan ini jug amengarahkan dan mengirimkan paket data melalui jaringan, serta menangani pemecahan alamat IP dan pengiriman paket antara jaringan yang berbeda.

### Transport
Lapisan ini bertanggung jawab untuk menyediakan koneksi data yang solid dan andal antara aplikasi dengan tujuan yang dimaksudkan. Dua protokol yang paling umum digunakan di sini adalah Transmission Control Protocol (TCP), yang menyediakan pengiriman data yang andal dan terurut, serta User Datagram Protocol (UDP), yang lebih cepat tetapi kurang andal. Lapisan ini adalah lapisan di mana data dibagi menjadi paket dan diberi nomor untuk membuat urutan kemudian lapisan ini akan menentukan berapa banyak data yang akan dikirimkan, alamat pengirimannya, dan kecepatan pengirimannya. Lapisan ini juga yang akan memastikan bahwa paket data dikirim secara berurutan dan tanpa kesalahan, serta menerima informasi jika paket data telah sampai tujuan.

### Aplikasi
lapisan ini adalah lapisan tertinggi yang berhubungan langsung dengan pengguna dan aplikasi. Ini mencakup berbagai protokol untuk aplikasi seperti HTTP (web browsing), FTP (file transfer), SMTP (email), dan banyak lagi. Lapisan ini berfungsi untuk membantu mereka saling berkomunikasi.
