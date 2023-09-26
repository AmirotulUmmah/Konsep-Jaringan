# Socket Server dan Client

## Socket
Socket Programming adalah pemrograman yang bertujuan agar satu program bisa berinteraksi dengan program lain dalam satu jaringan. Socket digunakan untuk mengirim dan menerima data antara proses yang berjalan pada mesin yang sama maupun mesin yang berbeda. Terdapat dua jenis pengunaan protokol komunikasi untuk Socket Programming yakni :
1. TCP/IP (Transmission Control Protocol/Internet Protocol) <br> Protokol ini sering digunakan untuk koneksi yang terjamin sehingga cocok untuk aplikasi yang membutuhkan pengiriman data secara aman seperti transfer file, email, dan aplikasi web.
2. UDP/IP (User Datagram Protocol/Internet Protocol) <br> Protokol ini digunakan untuk komunikasi yang lebih cepat tetapi tidak menjamin data akan sampai di tujuan. Biasanya digunakan pada aplikasi yang perlu pengiriman data cepat tanpa memerhatikan kehilangan data. Contohnya video streaming, game online, dan streaming audio.

Untuk menjalankan Socket Programming, kita perlu minimal dua program yakni Socket Server dan Socket Client.

## Socket Server

Program Socket Server berjalan pada komputer yang memliki socket terikat dengan Nomor Port komputer tersebut dan menerima requestdari Socket Client. Tujuan utama dari Socket Server adalah untuk melayani permintaan yang diterima dari client dengan cara menangani request dan memberikan respons yang sesuai.

Analisis kode: 
* Server pertama-tama membuat "socket" yang akan digunakan untuk menerima koneksi dari klien dengan perintah socket(AF_INET, SOCK_STREAM, 0).
* Fungsi init_sockaddr_in digunakan untuk menyiapkan informasi tentang alamat server, seperti jenis alamat (IPv4), alamat IP yang dapat menerima koneksi dari semua alamat (INADDR_ANY), dan nomor port yang telah ditentukan (5001 dalam contoh ini).
* Server menghubungkan socketnya ke alamat dan port yang telah ditentukan dengan perintah bind().
* Setelah itu, server siap untuk menerima koneksi masuk dari klien dengan perintah listen(). Ini mengizinkan server mendengarkan permintaan koneksi.
* Server masuk ke dalam loop utama yang akan terus menerima koneksi dari klien.
* Saat ada koneksi masuk, server menerima koneksi tersebut menggunakan accept(), yang menghasilkan "nomor telepon" (file descriptor) untuk berkomunikasi dengan klien.
* Untuk menangani setiap koneksi dari klien secara terpisah, server menggunakan fork() untuk membuat proses child yang akan mengurus komunikasi dengan klien tersebut.
* Proses child ini memiliki socket dan buffernya sendiri.
* Proses child menutup "nomor telepon" socket server asli (server_fd) karena proses ini akan digunakan oleh proses lain untuk menerima koneksi dari klien lain.
* Setiap proses child memasuki loop yang memungkinkan mereka berbicara dengan klien. Mereka membaca pesan dari klien dengan perintah read() dan mengirim respons dengan perintah send().
* Proses child juga memeriksa pesan "close" untuk menutup koneksi dengan klien.
* Jika tidak ada pesan yang diterima dalam waktu tertentu, proses child akan menutup koneksi karena time-out.
* Setelah selesai berkomunikasi dengan klien, proses child menutup koneksi dengan klien menggunakan close().
* Proses child kemudian keluar dari proses (exit()) untuk mengakhiri pekerjaannya.

## Socket Client

Program Socket Client harus mengetahui IP Address/Hostname serta port yang digunakan komputer milik Server agar bisa mengirimkan request. Tujuan utama dari Socket CLient adalah untuk membuat request kepada Server dan kemudian menerima respons dari Server.

Analisis kode :
* Kode program pertama kali membuat socket yang akan digunakan untuk berbicara dengan server menggunakan fungsi socket().
* Fungsi gethostbyname() digunakan untuk mendapatkan alamat IP server dari nama host yang telah ditentukan sebelumnya (dalam praktikum IP yang digunakan adalah "192.168.46.218").
* Kemudian, atribut dari socket diatur, seperti jenis alamat (IPv4), alamat IP tujuan, dan nomor port tujuan, dengan mengisi struktur serv_addr.
* Fungsi connect() digunakan untuk menghubungkan soket ke server yang telah diatur sebelumnya. Jika koneksi berhasil, program akan melanjutkan ke langkah berikutnya.
* Program memasuki loop tak terbatas yang memungkinkan user untuk mengirim pesan ke server dan menerima respons.
* User diminta untuk memasukkan pesan melalui perintah printf("What do you want to say? ");, dan inputnya disimpan dalam buffer buffer.
* Pesan yang dimasukkan oleh user dikirim ke server menggunakan fungsi write() dengan ukuran pesan yang dihitung menggunakan strlen(buffer).
* Respons dari server kemudian dibaca menggunakan fungsi read() dan disimpan dalam buffer yang sama.
* Jika terjadi kesalahan dalam proses write atau read, program akan menampilkan pesan kesalahan dan keluar dari loop.
* Kemudian dilakuakn pemeriksaan apakah server mengirim pesan "quit" dengan menggunakan bcmp(). Jika server mengirim pesan "quit", maka klien akan keluar dari loop dan menutup koneksi.
* Setelah selesai berkomunikasi dengan server, program menutup soket dengan menggunakan close() untuk mengakhiri koneksi.

## Proses
1. Client menentukan IP Address Server yang dituju.

![alt text](https://github.com/AmirotulUmmah/Konsep-Jaringan/blob/main/assets/client%202.jpeg?raw=true)<br>

2. Client mengirim request ke Server

![alt text](https://github.com/AmirotulUmmah/Konsep-Jaringan/blob/main/assets/client%203.jpeg?raw=true)<br>

3. Server menerima request dari Client dan merespons kembali ke Client.
![alt text](https://github.com/AmirotulUmmah/Konsep-Jaringan/blob/main/assets/Server.jpeg?raw=true)<br>


4. Client mengirim request ke Server menggunakan flag PSH untuk memastikan bahwa request segera direspon penundaan yang digunakan oleh buffering data dan flag ACK untuk mengonfirmasi bahwa data permintaan atau resapons sebelumntya telah diterima dengan benar oleh pihak yang menerima.
   
5. Server mengirim respons dengan flag PSH untuk memastikan bahwa data dari server segera tersedia untuk diproses ke aplikasi client.
   
![alt text](https://github.com/AmirotulUmmah/Konsep-Jaringan/blob/main/assets/client%201.jpeg?raw=true)<br>
![alt text](https://github.com/AmirotulUmmah/Konsep-Jaringan/blob/main/assets/client%204.jpeg?raw=true)<br>

## MSS - Maximum Segment Size

MSS (Maximum Segment Size) adalah ukuran maksimum segmen data yang dapat dikirim dalam satu paket atau frame dalam protokol TCP (Transmission Control Protocol). Dalam komunikasi jaringan, klien dan server akan saling negosiasi mengenai ukuran MSS selama proses 3 Ways Handshaking saat koneksi TCP dibuat. Nilai MSS yang lebih kecil dari kedua pihak akan digunakan sebagai ukuran maksimum segmen data yang akan dikirim selama koneksi tersebut.

Tujuan utama dari MSS adalah untuk memastikan bahwa segmen data yang dikirim dalam satu paket TCP tidak terlalu besar sehingga dapat dikirim dengan efisien melalui jaringan tanpa perlu dipecah-pecah atau menyebabkan masalah kinerja. Nilai MSS dapat bervariasi tergantung pada jenis jaringan dan konfigurasi perangkat :
1. Ethernet <br> MSS biasanya sekitar 1460 hingga 1500 byte, tergantung pada apakah jaringan tersebut menggunakan protokol seperti IPv4 atau IPv6, serta apakah ada tambahan header seperti header IP dan TCP yang perlu diperhitungkan.
2. Jaringan Mobile <br> Di jaringan mobile, seperti 4G LTE atau 5G, MSS biasanya lebih kecil daripada di jaringan kabel seperti Ethernet. Ini dapat bervariasi tergantung jenis layanan dan konfigurasi operator seluler, umumnya berkisar antara 1000 hingga 1400 byte.
3. Jaringan Wide Area <br> Di jaringan WAN (Wide Area Network) seperti Internet, MSS dapat bervariasi tergantung pada penyedia layanan Internet (ISP) dan jenis layanan yang Anda gunakan. Nilai umum adalah sekitar 1460 hingga 1500 byte.

![alt text](https://github.com/AmirotulUmmah/Konsep-Jaringan/blob/main/assets/mss.jpeg?raw=true)<br>

Jika data yang dikirim melebihi 1500 bytes, maka segmen tersebut akan dipecah menjadi beberapa segmen yang lebih kecil sebelum dikirim melalui jaringan. Fragmentasi dapat mempengaruhi kinerja jaringan dan memerlukan pemrosesan tambahan di sisi receiver. Oleh karena itu, penggunaan segmen-segmen yang lebih kecil (dalam batas MSS) dapat membantu menghindari fragmentasi yang berlebihan dan meningkatkan efisiensi komunikasi jaringan

