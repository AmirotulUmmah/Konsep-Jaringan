# Socket Server dan Client

## Socket
Socket Programming adalah pemrograman yang bertujuan agar satu program bisa berinteraksi dengan program lain dalam satu jaringan. Socket digunakan untuk mengirim dan menerima data antara proses yang berjalan pada mesin yang sama maupun mesin yang berbeda. Terdapat dua jenis pengunaan protokol komunikasi untuk Socket Programming yakni :
1. TCP/IP (Transmission Control Protocol/Internet Protocol) <br> Protokol ini sering digunakan untuk koneksi yang terjamin sehingga cocok untuk aplikasi yang membutuhkan pengiriman data secara aman seperti transfer file, email, dan aplikasi web.
2. UDP/IP (User Datagram Protocol/Internet Protocol) <br> Protokol ini digunakan untuk komunikasi yang lebih cepat tetapi tidak menjamin data akan sampai di tujuan. Biasanya digunakan pada aplikasi yang perlu pengiriman data cepat tanpa memerhatikan kehilangan data. Contohnya video streaming, game online, dan streaming audio.

Untuk menjalankan Socket Programming, kita perlu minimal dua program yakni Socket Server dan Socket Client.

## Socket Server

Program Socket Server berjalan pada komputer yang memliki socket terikat dengan Nomor Port komputer tersebut dan menerima requestdari Socket Client. Tujuan utama dari Socket Server adalah untuk melayani permintaan yang diterima dari client dengan cara menangani request dan memberikan respons yang sesuai.

## Socket Client

Program Socket Client harus mengetahui IP Address/Hostname serta port yang digunakan komputer milik Server agar bisa mengirimkan request. Tujuan utama dari Socket CLient adalah untuk membuat request kepada Server dan kemudian menerima respons dari Server.

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
