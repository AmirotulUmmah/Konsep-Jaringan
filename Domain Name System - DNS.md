Nama  : Amirotul Ummah <br>
NRP   : 3122600017 <br>
Kelas  : 2 D4 IT A <br>
Mata Kuliah  : Konsep Jaringan

# Domain Name System - DNS

DNS (Domain Name System) adalah sistem yang memiliki fungsi utama menyimpan semua data domain dalam jaringan dan menerjemahkan nama domain menjadi IP address agar bisa dipahami oleh komputer saat user mengakses sebuah website menggunakan nama domain untuk mengakses sumber daya di internet. Ditemukan oleh Paul Mackapetris pada tahun 1983, DNS menggantikan metode sebelumnya yang menggunakan file hosts.txt untuk memetakan nama domain ke alamat IP.
DNS bekerja seperti buku telepon atau direktori yang membantu user menemukan alamat fisik dari alamat yang user ketikkan atau nama yang user sebutkan

## Cara Kerja DNS

Berikut adalah cara umum bagaimana DNS bekerja untuk menghubungkan nama domain yang mudah diingat dengan alamat IP yang diperlukan untuk mengakses resource di internet. DNS memainkan peran kunci dalam infrastruktur internet dengan memungkinkan user untuk mengakses situs web dan layanan online dengan lebih mudah tanpa harus menghafal alamat IP setiap situs yang ingin dikunjungi.

1. Permintaan dari Peramban atau Aplikasi <br> Saat Anda memasukkan URL (misalnya, "www.contoh.com") ke dalam peramban web atau aplikasi, permintaan untuk mengakses situs web tersebut dikirimkan ke server DNS.
2. Pertanyaan ke Server DNS <br> Server DNS yang digunakan oleh perangkat Anda (biasanya disediakan oleh penyedia layanan internet atau ISP) menerima permintaan tersebut. Jika server DNS lokal tidak memiliki informasi tentang alamat IP untuk "www.contoh.com," itu akan melakukan kueri ke server DNS yang lebih tinggi dalam hierarki.
3. Hierarki DNS <br> DNS terdiri dari sejumlah server yang membentuk hierarki. Di bagian paling atas adalah root DNS server, yang mengarahkan permintaan ke server yang lebih khusus untuk domain tertentu. Ada juga server DNS tingkat atas (top-level DNS server) yang mengurus domain tingkat atas seperti ".com," ".org," ".net," dan lainnya.
4. Resolusi DNS <br> Proses resolusi DNS berlanjut hingga server DNS yang memiliki informasi tentang "www.contoh.com" menemukan alamat IP yang sesuai. Informasi ini dikirimkan kembali melalui jalur yang sama ke server DNS lokal Anda.
5. Penyimpanan Cache <br> Setelah alamat IP ditemukan, server DNS lokal Anda dapat menyimpannya dalam cache DNS. Ini memungkinkan untuk akses yang lebih cepat ke situs web yang sama di masa depan, karena tidak perlu melakukan pencarian DNS yang sama.
6. Pengembalian Informasi ke Peramban <br> Akhirnya, server DNS lokal mengembalikan alamat IP ke peramban atau aplikasi Anda. Dengan alamat IP ini, peramban dapat menghubungi server web yang sesuai untuk mengambil halaman web yang diminta.
7. Koneksi ke Situs Web <br> Peramban Anda menggunakan alamat IP untuk menghubungi server web yang meng-host "www.contoh.com." Data dari situs web tersebut kemudian diunduh dan ditampilkan pada peramban Anda.

