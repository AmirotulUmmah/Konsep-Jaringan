# FLOW GRAPH HTTP
Oleh  :
Amirotul Ummah (3122600017) - 2 D4 Teknik Informatika A <br>
Mata Kuliah  :
Konsep Jaringan

Flowgraph HTTP adalah representasi grafis yang menggambarkan alur atau langkah-langkah dari sebuah permintaan HTTP (Hypertext Transfer Protocol) dari klien ke server dan respons balik dari server ke klien. Flowgraph HTTP biasanya digunakan untuk memvisualisasikan interaksi antara klien dan server selama proses pertukaran data melalui protokol HTTP.

## Flow Graph
<br>![alt text](https://github.com/AmirotulUmmah/Konsep-Jaringan/blob/main/assets/flowgraphhttp.png?raw=true)<br>
Flowgraph HTTP membantu dalam memahami bagaimana data dan informasi mengalir antara klien dan server selama proses komunikasi menggunakan protokol HTTP. Ini berguna untuk analisis, pemecahan masalah, serta pemahaman lebih mendalam tentang interaksi yang terjadi di balik layar saat mengakses situs web atau berinteraksi dengan layanan online lainnya.

### Inisiasi Permintaan

Klien (biasanya browser web) memulai proses dengan menginisiasi permintaan HTTP. Ini bisa berupa mengklik tautan, mengisi formulir, atau melakukan permintaan lain ke server. <br> 
![alt text](https://github.com/AmirotulUmmah/Konsep-Jaringan/blob/main/assets/inisiasi.png?raw=true)<br>
1. Flag yang sering digunakan adalah flag SYN (Synchronize) dalam protokol TCP (Transmission Control Protocol). Flag SYN digunakan untuk memulai proses pembentukan koneksi TCP antara klien dan server.
2. Klien akan menggunakan alamat IP (Internet Protocol) yang mengidentifikasi perangkat klien dalam jaringan. Selain itu, klien akan menggunakan nomor port sumber yang unik untuk mengidentifikasi aplikasi atau layanan yang digunakan untuk mengirim permintaan. Port sumber biasanya dipilih secara dinamis oleh sistem operasi.
3. Klien juga harus mengetahui alamat IP server tujuan yang ingin diakses. Selain itu, klien akan menggunakan nomor port tujuan, yang merupakan nomor port di server yang menerima permintaan. Nomor port tujuan sesuai dengan layanan yang diakses (misalnya, port 80 untuk HTTP).

Pada saat inisiasi, klien mengirimkan paket SYN ke server, yang mengindikasikan bahwa klien ingin memulai proses koneksi. Paket SYN ini juga mengandung nomor urutan acak yang akan digunakan dalam koneksi. Server menerima paket SYN ini dan merespons dengan mengirimkan paket SYN/ACK. Paket SYN/ACK ini berisi nomor urutan yang direspon oleh server, serta nomor urutan acak yang diberikan oleh server.

Sebagai contoh, jika klien ingin mengakses halaman web melalui protokol HTTP (port 80), inisiasi akan melibatkan permintaan koneksi ke alamat IP server pada port 80. Klien akan mengirimkan paket SYN ke alamat IP server dan port 80, menunjukkan niat untuk memulai komunikasi. Server akan merespons dengan paket SYN/ACK, yang menegaskan bahwa server siap menerima komunikasi. Proses inisiasi ini adalah langkah pertama dalam 3-way handshake yang menjelaskan pembentukan koneksi TCP antara klien dan server dalam protokol jaringan.

## Pembentukan Request

Pembentukan permintaan (request) dalam konteks protokol HTTP terjadi setelah inisiasi koneksi antara klien dan server. Permintaan HTTP merupakan permintaan dari klien kepada server untuk mendapatkan sumber daya tertentu seperti halaman web, gambar, atau data lainnya. <br>
![alt text](https://github.com/AmirotulUmmah/Konsep-Jaringan/blob/main/assets/get.png?raw=true) <br>
Pada saat pembentukan request, ada beberapa elemen penting termasuk :
1. Metode HTTP <br> Pada gambar di atas, metode yang digunakan adalah GET yakni untuk mengambil data.
2. URL Tujuan <br> alamat yang menunjukkan resoyrse yang diinginkan oleh  klien di server. Pada gambar di atas, URL yang dituju adalah download.html

Ketika permintaan HTTP dibentuk, klien mengemasnya sesuai dengan metode, URL, header, dan data yang diperlukan. Permintaan tersebut kemudian dikirim melalui koneksi yang sudah terbentuk antara klien dan server, tanpa melibatkan flag SYN. Setelah permintaan sampai di server, server akan memproses permintaan dan merespons dengan data yang diminta atau informasi lainnya.

Setelah pembentukan Request, server akan menerima HTTP dari klien dan memproses permintaansesuai dengan informasi yang diberikan dalam permintaan.

## Penyediaan Respon <br>
![alt text](https://github.com/AmirotulUmmah/Konsep-Jaringan/blob/main/assets/httpok.png?raw=true)<br>
Penyediaan respons dalam konteks protokol HTTP terjadi setelah server menerima permintaan dari klien dan memprosesnya. Respons HTTP adalah tanggapan yang diberikan oleh server sebagai jawaban atas permintaan yang dikirimkan oleh klien. Respons ini berisi informasi yang diminta atau informasi tentang apakah permintaan tersebut berhasil dilaksanakan atau tidak.
Saat penyediaan Respons, ada beberapa elemen penting diantaranya :
1. Kode Status HTTP <br> Kode status HTTP adalah angka tiga digit yang mengindikasikan hasil dari permintaan klien. Contohnya adalah kode 200 OK (permintaan berhasil) seperti yang ada pada gambar, 404 Not Found (sumber daya tidak ditemukan), dan 500 Internal Server Error (kesalahan internal pada server).
2. Header Respons <br> Header respons HTTP berisi informasi tambahan yang dikirim bersama respons. Header ini mencakup berbagai informasi seperti "Content-Type" (jenis konten yang dikirim), "Content-Length" (panjang konten dalam byte), dan lain-lain.
3. Data Respons <br> Data respons adalah konten yang dikirim oleh server sebagai respons atas permintaan. Konten ini bisa berupa halaman web (HTML), gambar, data JSON, dan sebagainya, tergantung pada jenis permintaan yang dilakukan oleh klien.

Setelah menyediakan respons, server akan mengirimkan respons HTTP ke klien melalui protokol jaringan, pada Flow Graph http.cap (gambar terlampir), protokol jaringan yang digunakan adalah TCP. Setelah itu, klien menerima respons HTTP dari server.

## Terminasi
Terminasi HTTP merujuk pada akhir dari pertukaran data antara klien dan server melalui protokol HTTP. Ini terjadi setelah klien mengirim permintaan dan menerima respons dari server, menandakan bahwa komunikasi antara klien dan server untuk permintaan tertentu telah selesai.<br>
![alt text](https://github.com/AmirotulUmmah/Konsep-Jaringan/blob/main/assets/terminasi.png?raw=true) <br>
Saat komunikasi dihentikan, koneksi dapat ditutup menggunakan flag FIN (Finish) dalam protokol TCP. Flag FIN digunakan untuk memberi tahu lawan bicara bahwa pihak yang mengirimnya telah selesai mengirim data dan ingin menutup koneksi.
Interaksi antara flag dalam terminasi HTTP adalah sebagai berikut:
1. Klien telah mengirim semua data yang ingin dikirimkan ke server dan ingin menutup koneksi, klien akan mengirimkan flag FIN kepada server. Ini menandakan bahwa klien telah selesai mengirim data.
2. Setelah menerima flag FIN dari klien, server akan memberikan respons kepada klien jika ada data yang masih tertunda untuk dikirim. Server juga bisa mengirim flag FIN ke klien setelah selesai mengirim data.
3. Setelah menerima flag FIN dari server, klien mengerti bahwa server telah selesai mengirim data. Klien mengirimkan ACK (acknowledge) untuk flag FIN yang diterima dari server.
4. Setelah menerima ACK dari klien untuk flag FIN yang dikirim, server mengerti bahwa klien telah menerima semua data dan siap menutup koneksi. Server mengirimkan flag FIN ke klien.
5. Setelah menerima flag FIN dari server, klien mengirimkan ACK sebagai konfirmasi bahwa server telah menutup koneksi. Koneksi resmi ditutup oleh kedua belah pihak.



