# 3 WAYS HANDSHAKE
Oleh  :
Amirotul Ummah (3122600017) - 2 D4 Teknik Informatika <br>
Mata Kuliah  :
Konsep Jaringan

3 Ways Handshake adalah metode penting yang digunakan untuk menginisiasi koneksi soket TCP yang handal, memungkinkan data dikirimkan dengan aman antara perangkat. Ini sangat berguna dalam memfasilitasi komunikasi antara peramban web di perangkat klien dan server setiap kali Anda menjelajah internet.

## Alur 3 Ways Handshake
Ketika klien ingin berkomunikasi dengan server, langkah-langkah jabat tangan tiga arah dimulai. Ini terdiri dari tiga tahap yang perlu diikuti.

### 1. Membuat Koneksi antara Server dan Klien

Analoginya adalah client akan mengirimkan sebuah paket ke sever dan menyatakan "ayo mengirim paket". Client ingin memulai pengiriman paket dan mengajukan permintaan pengiriman kepada server agar saluran pengiriman dapat dibuka.

Langkah pertama melibatkan pembuatan koneksi antara server dan klien. Server harus memiliki port yang terbuka untuk menerima koneksi baru. Klien mengirimkan paket data SYN (synchronize sequence number) melalui jaringan IP ke server. Paket SYN ini berisi nomor urutan acak yang akan digunakan oleh klien untuk komunikasi (misalnya, x). Fungsi utama dari paket ini adalah untuk mengecek apakah server siap menerima koneksi baru.

### 2. Server Merespons dengan Paket SYN/ACK

Analoginya adalah server menerima permintaai client dan tau bahwa client akan mengirimkan paket. Server merespons dan mengirimkan pesan balasan, "saya siap menerima paket". Maka client dan server telah sepakat untuk memberi dan menerima paket.

Ketika server menerima paket SYN dari klien, itu merespons dengan mengirimkan paket SYN/ACK (synchronize/acknowledge). Paket ini berisi dua nomor urutan. Nomor pertama adalah ACK Number, yang diberikan oleh server kepada nomor urutan yang diterima dari klien (x+1). Nomor kedua adalah SYN yang dikirim oleh server, yang merupakan nomor urutan acak lainnya (misalnya, y). Langkah ini menunjukkan bahwa server mengakui paket klien dan merespons dengan nomor urutan yang diberikan klien.

### 3. Klien Menerima Paket SYN/ACK dan Merespons dengan ACK

Analogi untuk langkah terakhir adalah client menerima balasan server yang siap menerima paket. Kemudian saluran pengiriman paket terbuka untuk client maupun server, dan keduanya bisa berkirim paket.

Ketika klien menerima paket SYN/ACK dari server, ia merespons dengan mengirimkan paket ACK (acknowledge). Lagi pula, nomor urutan yang diterima oleh masing-masing pihak ditingkatkan satu. Klien mengakui paket server dengan menambahkan satu ke nomor urutan (y+1) dan mengirimkannya ke server. Setelah tahap ini selesai, koneksi antara klien dan server terbentuk, dan mereka siap untuk berkomunikasi.

Ketiga langkah ini sangat penting karena mereka memastikan bahwa nomor urutan yang berasal dari kedua pihak terverifikasi, menjaga stabilitas koneksi. Karena kedua belah pihak mengakui parameter koneksi satu sama lain, kesalahan pada segmen data yang hilang atau tiba di urutan yang salah dapat dengan cepat terdeteksi sebelum proses pengiriman data sebenarnya dimulai.

## Kesimpulan

Tahapan-tahapan ini memiliki signifikansi yang tinggi karena mereka bertindak sebagai mekanisme verifikasi nomor urutan yang berasal dari kedua pihak, memastikan kestabilan koneksi yang dibentuk. Karena baik klien maupun server mengakui parameter-parameter koneksi yang diajukan oleh pihak lain, ini menciptakan lapisan perlindungan yang memungkinkan kesalahan dalam segmen data, seperti yang mungkin hilang atau tiba dengan urutan yang salah, untuk diidentifikasi dengan cepat. Dengan adanya tahapan ini sebelum pengiriman data sebenarnya dimulai, potensi kesalahan dapat diatasi sebelum mereka mempengaruhi transfer data yang sesungguhnya.





