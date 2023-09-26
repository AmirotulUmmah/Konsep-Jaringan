# Connection Termination

Connection termination adalah proses pengakhiran atau penutupan sebuah koneksi dalam konteks komunikasi jaringan. Ini adalah langkah penting dalam komunikasi jaringan karena memungkinkan perangkat atau aplikasi yang terlibat dalam koneksi untuk menghentikan pertukaran data dengan cara yang aman dan efisien. Terdapat beberapa metode yang digunakan untuk mengakhiri koneksi dalam protokol jaringan, terutama dalam protokol TCP (Transmission Control Protocol), yang sering digunakan dalam komunikasi internet.

Terminasi koneksi dalam konteks komunikasi jaringan dapat dibagi menjadi dua kondisi utama: full closed (tutup penuh) dan half closed (tutup setengah), yang terutama berlaku dalam protokol TCP (Transmission Control Protocol).

## Full Closed 

Di dalam full closed, kedua sisi koneksi sepakat untuk mengakhiri koneksi secara bersamaan dan menghentikan pertukaran data sepenuhnya. Ini adalah hasil akhir yang paling umum dalam terminasi koneksi TCP. Prosesnya adalah sebagai berikut:

1. Salah satu sisi koneksi (misalnya, client atau server) mengirimkan pesan FIN (Finish) ke sisi lain.
2. Sisi yang menerima pesan FIN mengirimkan ACK (Acknowledgment) sebagai konfirmasi pengakhiran.
3. Kemudian, sisi yang menerima konfirmasi ACK juga dapat mengirimkan pesan FIN-nya sendiri sebagai konfirmasi balasan.
4. Sisi lain juga mengkonfirmasi dengan ACK.
5. Setelah langkah-langkah ini selesai, koneksi dianggap ditutup penuh, dan tidak ada pertukaran data tambahan yang diizinkan antara kedua sisi.
   
## Half Closed 

Di dalam half closed, salah satu sisi koneksi menghentikan pengiriman data tetapi masih ingin menerima data dari sisi lain. Ini dapat berguna dalam skenario di mana satu sisi ingin mengakhiri pengiriman data tetapi masih ingin mendengarkan respons atau informasi tambahan dari sisi lain. Prosesnya adalah sebagai berikut:

1. Salah satu sisi koneksi mengirimkan pesan FIN ke sisi lain.
2. Sisi yang menerima pesan FIN mengirimkan ACK sebagai konfirmasi pengakhiran.
3. Sisi yang mengirimkan pesan FIN tidak mengizinkan pengiriman data tambahan ke sisi lain tetapi masih dapat menerima data dari sisi lain.
4. Setelah sisi yang menerima pesan FIN selesai mengirimkan semua data yang dibutuhkan, ia juga dapat mengirimkan pesan FIN sendiri untuk mengakhiri koneksi sepenuhnya.

## Conclusion

Perbedaan utama antara full closed dan half closed adalah dalam full closed, kedua sisi sepenuhnya menghentikan pertukaran data, sementara dalam half closed, salah satu sisi menghentikan pengiriman data tetapi masih bisa menerima data dari sisi lain. Mana yang digunakan tergantung pada kebutuhan aplikasi dan protokol yang digunakan dalam komunikasi jaringan.
