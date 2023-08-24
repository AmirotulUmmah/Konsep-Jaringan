# TCP/IP LAYER

TCP/IP adalah isingkatan dari Transmission Control Protocol/Internet Protocol. TCP/IP merupakan protokol standar dalam jaringan komputer untuk menjembatani pertukaran data antar perangkat dalam jaringan tersebut. Keduanya merupakan jaringan komputer yang terpisah namun harus bekerja sama.
IP merupakan server untuk memperoleh alamat tujuan data dikirimkan sedangkan TCP berfungsi untuk mengirim data setelah alamat ditemukan oleh IP.
Model TCP/IP memecah pesan menjadi paket-paket untuk meminimalisir pengiriman ulang seluruh pesan jika terdapat kesalahan selama transmisi. Paket data harus melewati empat lapisan sebelum diterima oleh perangkat tujuan dan TCP/IP melewati lapisan dalam urutan terbalik untuk mengembalikan pesan ke format aslinya.
Adapun empat lapisan (layer) dalam TCP/IP yakni :

## Datalink
Lapisan ini mengatur aliran data antara dua perangkat di jaringan yang langsung terhubung. Ini juga mengatur deteksi kesalahan dalam transmisi data dan mengatur alamat fisik perangkat (MAC addresses). Lapisan ini juga mengatur bagaimana data dikirim, bagaimana data harus diberi sinyal oleh hardware dan perangkat transmisi lain di jaringan, serta bertanggung jawab untuk mentransmisikan data antara aplikasi atau perangkat dalam jaringan

## Internet
Layer ini bertanggung jawab untuk mengirim paket dari jaringan mengendalikan pergerakan paket di seluruh jaringan untuk memastikan apakah paket-paket tersebut sudah sampai tujuan. Lapisan ini jug amengarahkan dan mengirimkan paket data melalui jaringan, serta menangani pemecahan alamat IP dan pengiriman paket antara jaringan yang berbeda.

## Aplikasi
lapisan ini adalah lapisan tertinggi yang berhubungan langsung dengan pengguna dan aplikasi. Ini mencakup berbagai protokol untuk aplikasi seperti HTTP (web browsing), FTP (file transfer), SMTP (email), dan banyak lagi. Lapisan ini berfungsi untuk membantu mereka saling berkomunikasi.
