# Socket Server dan Client

## Socket
Socket Programming adalah pemrograman yang bertujuan agar satu program bisa berinteraksi dengan program lain dalam satu jaringan. Socket digunakan untuk mengirim dan menerima data antara proses yang berjalan pada mesin yang sama maupun mesin yang berbeda. Terdapat dua jenis pengunaan protokol komunikasi untuk Socket Programming yakni :
1. TCP/IP (Transmission Control Protocol/Internet Protocol) <br> Protokol ini sering digunakan untuk koneksi yang terjamin sehingga cocok untuk aplikasi yang membutuhkan pengiriman data secara aman seperti transfer file, email, dan aplikasi web.
2. UDP/IP (User Datagram Protocol/Internet Protocol) <br> Protokol ini digunakan untuk komunikasi yang lebih cepat tetapi tidak menjamin data akan sampai di tujuan. Biasanya digunakan pada aplikasi yang perlu pengiriman data cepat tanpa memerhatikan kehilangan data. Contohnya video streaming, game online, dan streaming audio.
Untuk menjalankan Socket Programming, kita perlu minimal dua program yakni Socket Server dan Socket Client.
1. Socket Server <br> Program Socket Server berjalan pada komputer yang memliki socket terikat dengan Nomor Port komputer tersebut dan menerima requestdari Socket Client. Tujuan utama dari Socket Server adalah untuk melayani permintaan yang diterima dari client dengan cara menangani request dan memberikan respons yang sesuai.
2. Socket Client (br> Program Socket Client harus mengetahui IP Address/Hostname serta port yang digunakan komputer milik Server agar bisa mengirimkan request. Tujuan utama dari Socket CLient adalah untuk membuat request kepada Server dan kemudian menerima respons dari Server.
