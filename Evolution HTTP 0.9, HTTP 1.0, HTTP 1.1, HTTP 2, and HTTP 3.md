# EVOLUTION of HTTP



## HTTP/0.9
HTTP/0.9 adalah versi terlama dari HyperText Transfer Protocol (HTTP). HTTP/0.9 pertama kali dirilis pada tahun 1991, namun seiring berjalannya waktu versi ini telah tergantikan oleh HTTP 1.0, HTTP 1.1, HTTP 2, dan HTTP 3.
Keterbatasan utama HTTP/0.9 terletak pada ketidakdukungannya terhadap beberapa header HTTP atau tindakan otentikasi yang lebih canggih yang muncul pada revisi-revisi HTTP berikutnya. Sebaliknya, hanya permintaan GET dasar yang tersedia untuk sebagian besar operasi saat menggunakan versi protokol ini. Ini juga berarti bahwa dukungan untuk koneksi bersamaan yang banyak tidak mungkin dilakukan – browser harus menunggu hingga satu koneksi selesai sebelum melakukan permintaan HTTP lainnya.
#### FITUR HTTP/0.9
1. HTTP/0.9 hanya mendukung Single Request Method, yaitu GET, yang digunakan untuk mengambil sumber daya dari server.
2. HTTP/0.9 tidak memiliki header atau kode status, sehingga menjadi protokol yang sangat sederhana dan terbatas.
3. HTTP/0.9 tidak mendukung koneksi yang persisten, yang berarti bahwa setiap permintaan harus menjalani koneksi TCP terpisah.
4.HTTP/0.9 tidak mendukung Chunked Transfer, yang merupakan mekanisme untuk mengirimkan data dalam bagian-bagian kecil.
5. HTTP/0.9 memiliki penanganan kesalahan yang terbatas, dan tidak ada cara untuk menunjukkan kesalahan dalam respons.
6. HTTP/0.9 menggunakan format respons yang sangat sederhana, dan responsnya hanya berisi sumber daya yang diminta, tanpa header atau informasi lainnya.

## HTTP/1.0
HTTP/1.0 memungkinkan adanya server push, di mana server web mengirim informasi kepada client tanpa harus menunggu permintaan dari client. HTTP/1 menggunakan beberapa request untuk meningkatkan kecepatan. Setiap permintaan memerlukan koneksi TCP sendiri, dan setiap koneksi memerlukan waktu untuk terbuka dan tertutup. Dengan beberapa permintaan yang dikirim secara bersamaan, waktu menunggu akan berkurang dan resource yang digunakan lebih sedikit daripada jika semua permintaan dikirim secara berurutan. Selain itu, HTTP/1.0 memungkinkan Server Push yang membantu mengurangi latensi dengan mengirimkan data dari server sebelum diminta oleh client.
#### FITUR HTTP/1.0
1. Multiple request methods <br> Termasuk GET, POST, dan HEAD. Client dapat menggunakan metode yang sesuai dengan tugas yang diinginkan, seperti mengambil data (GET), mengirim data (POST), atau hanya meminta informasi kepala (HEAD).
2. Header <br> Memungkinkan komunikasi yang lebih canggih antara klien dan server. Header ini dapat berisi informasi tambahan tentang permintaan atau respons, seperti jenis konten atau bahasa yang diinginkan.
3. Status codes <br> Memungkinkan penanganan kesalahan yang lebih canggih dan pelaporan. Kode status ini memberikan informasi tentang hasil dari permintaan, misalnya, apakah permintaan berhasil (kode 200 OK) atau terjadi kesalahan (kode 404 Not Found).
4. Persistent connections <br> Dapat melakukan pengiriman dengan multiple permintaan melalui satu koneksi. Hal ini mengurangi overhead, karena koneksi tidak perlu dibuka dan ditutup untuk setiap permintaan.
5. Content negotiation <br> Memungkinkan klien untuk meminta format dan bahasa tertentu untuk kontennya. Ini membantu server memberikan respons yang paling sesuai dengan preferensi klien.
6. Improved caching <br> Dapat menyimpan resources secara lebih efisien. Ini membantu mengurangi beban server dan mempercepat pengiriman data kepada klien.

## HTTP/1.1
HTTP/1.1 dirilis pada tahun 1997 dan mempunyai banyak perubahan yang signifikan dibandingkan dengan HTTP/0.9. HTTP/1.1 adalah protokol tingkat aplikasi yang mengatur pengiriman halaman web melalui Internet dan menjadi protokol utama yang digunakan oleh browser web dan server untuk berkomunikasi melalui internet.
#### FITUR HTTP/1.1
1. Persistent Connections <br> Mendukung koneksi persisten secara default, yang memungkinkan beberapa permintaan dan respons untuk berbagi satu koneksi TCP. Hal ini mengurangi overhead pembukaan dan penutupan koneksi, meningkatkan efisiensi, dan mengurangi waktu tunggu.
2. Pipelining <br> Fitur yang memungkinkan klien untuk mengirim beberapa permintaan sebelum menerima respons pertama. Hal ini memungkinkan permintaan dan respons untuk bergerak lebih cepat melalui koneksi danmeningkatkan kinerja secara signifikan.
3. Chunked Transfer Encoding <br> Memungkinkan transfer data dalam bentuk "chunked," di mana data dibagi menjadi bagian-bagian kecil. Ini berguna untuk mengirim data dalam waktu nyata atau ketika ukuran totalnya tidak diketahui sebelumnya.
4. Host Header: Dalam HTTP/1.1, setiap permintaan harus menyertakan header "Host," yang memungkinkan server untuk mengidentifikasi domain yang diminta. Ini mendukung hosting beberapa situs web di server yang sama.
5. Cache Control <br> Header-cache yang lebih canggih, seperti "Cache-Control," yang memberikan kontrol yang lebih baik atas caching di sisi klien dan server. Ini membantu mengoptimalkan penggunaan cache untuk meningkatkan kinerja.
6. Range Requests <br> Mendukung permintaan berdasarkan rentang (range requests), yang memungkinkan klien untuk meminta hanya bagian tertentu dari sebuah file, berguna untuk streaming media atau mengunduh bagian tertentu dari file besar.
7. Compression <br> Mengompresi data dengan header "Accept-Encoding" dan "Content-Encoding." Ini memungkinkan pengiriman data yang lebih efisien dengan mengurangi ukuran payload.
8. Transfer Encoding <br> Adanya mekanisme transfer encoding, termasuk "chunked" dan "gzip," yang mendukung pengiriman data dalam format yang lebih efisien.
9. Keep-Alive <br> HTTP/1.1 secara otomatis mendukung koneksi keep-alive, yang memungkinkan koneksi untuk tetap terbuka untuk penggunaan berulang tanpa perlu membuka kembali koneksi baru.
10. Status Codes <br> HTTP/1.1 memperluas kode status untuk memberikan informasi yang lebih spesifik tentang respons, seperti 201 Created, 206 Partial Content, dan lainnya.

## HTTP/2.0
HTTP/2 pertama kali distandardisasi pada tahun 2015. HTTP/2 dirancang dengan tujuan mengurangi latenSI dan overhead. HTTP/2 memiliki sejumlah fitur dan optimasi baru, termasuk pengkodean biner, multiplexing, server push, dan kompresi header, yang meningkatkan kecepatan dan efisiensi komunikasi web.
#### FITUR/2.0
1. Multiplexing <br> HTTP/2 mendukung multiplexing, yang memungkinkan beberapa permintaan dan respons dapat dikirimkan secara bersamaan melalui satu koneksi. Ini mengurangi latensi dan meningkatkan efisiensi karena permintaan tidak harus menunggu antrian.
2. Binary Protocol <br> HTTP/2 menggunakan format pesan biner daripada teks ASCII seperti yang digunakan oleh HTTP/1.1. Ini mengurangi beban proses pada server dan memungkinkan pengiriman data yang lebih efisien.
3. Header Compression <br> Terdapat kompresi header yang lebih baik, yang mengurangi ukuran header permintaan dan respons. Ini membantu menghemat bandwidth dan mempercepat waktu muat halaman.
4. Server Push <br> Fitur ini memungkinkan server untuk mengirimkan sumber daya kepada klien sebelum diminta oleh klien. Ini dapat meningkatkan kecepatan pengiriman konten dengan mengantisipasi kebutuhan klien.
5. Prioritas <br> HTTP/2 memungkinkan klien untuk menentukan prioritas permintaan mereka. Ini memungkinkan aplikasi web untuk memberikan penekanan pada permintaan yang lebih penting, meningkatkan kinerja secara keseluruhan.
6. Flow Control <br> Memiliki mekanisme kontrol aliran yang lebih baik, yang memungkinkan klien dan server mengendalikan seberapa banyak data yang mereka kirimkan atau terima sekaligus. Ini membantu mencegah kelebihan beban dan penghambatan.
7. Binary Frame Format <br> Mampu mengirimkan data dalam bentuk frame biner yang memungkinkan parsing yang lebih efisien dan pemrosesan di sisi klien dan server.
8. TLS (Transport Layer Security) <br> Sebagian besar implementasi HTTP/2 mensyaratkan penggunaan TLS untuk mengamankan koneksi. Ini meningkatkan keamanan komunikasi web secara umum.

## HTTP/3.0
HTTP/3 adalah versi ketiga dari Protokol Transfer HyperText yang digunakan untuk pertukaran informasi di World Wide Web. Ini merupakan pelengkap dari HTTP/1.1 dan HTTP/2 yang sudah banyak digunakan. Dengan kata lain, HTTP/3 adalah versi lanjutan dari protokol web yang digunakan untuk berkomunikasi di internet.
#### FITUR HTTP/3.0
1. QUIC Transport Protocol <br> enggunakan protokol transport QUIC (Quick UDP Internet Connections) yang berbasis pada UDP daripada TCP seperti HTTP/1 dan HTTP/2. Ini bertujuan mengurangi keterlambatan dan meningkatkan kecepatan pengiriman data.
2. Multiplexing <br> HTTP/3 mendukung multiplexing, yang memungkinkan pengiriman beberapa permintaan dan respons secara bersamaan melalui satu koneksi, mengurangi keterlambatan.
3. Flow Control yang Ditingkatkan: HTTP/3 memiliki kontrol aliran yang lebih canggih, yang memungkinkan pengaturan seberapa banyak data yang bisa dikirim atau diterima secara bersamaan oleh klien dan server.
4. Kompresi Header: HTTP/3 juga menggunakan kompresi header yang lebih efisien dibandingkan HTTP/1.1, mengurangi ukuran header pada permintaan dan respons.
5. Prioritas dan Pengendalian Stream: HTTP/3 memungkinkan pengaturan prioritas yang lebih baik, sehingga aplikasi web dapat mengatur urutan pemrosesan permintaan yang lebih penting.
6. Server Push: HTTP/3 tetap mendukung fitur Server Push, yang memungkinkan server mengirimkan sumber daya kepada klien sebelum diminta oleh klien, meningkatkan kecepatan pengiriman konten.
7. Encryption  <br> Meningkatkan keamanan komunikasi web secara keseluruhan dengan melindungi data yang dikirim.
8. Enhanced Performance in Unstable Networks <br> HTTP/3 dirancang untuk berkinerja lebih baik bahkan dalam kondisi jaringan yang tidak stabil, seperti saat menggunakan jaringan seluler atau koneksi Wi-Fi yang tidak optimal. Ini membantu meningkatkan pengalaman pengguna dalam situasi tersebut.





