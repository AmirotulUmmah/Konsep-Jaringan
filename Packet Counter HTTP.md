# Paclet Counter
Oleh  :
Amirotul Ummah (3122600017) - 2 D4 Teknik Informatika A <br>
Mata Kuliah  :
Konsep Jaringan

![alt text](https://github.com/AmirotulUmmah/Konsep-Jaringan/blob/main/assets/packetcounter.png?raw=true)
Packet counter di dalam HTTP merupakan penghitungan jumlah paket yang dikirim dan diterima selama pertukaran data antara klien dan server melalui protokol HTTP. Paket adalah unit data yang dikirim melalui jaringan dan dapat berisi informasi seperti permintaan HTTP atau respons HTTP. Penghitungan paket dapat memberikan wawasan tentang seberapa banyak data yang dikirim atau diterima selama komunikasi, serta membantu dalam analisis kinerja dan pemecahan masalah.

## Topic/Item
#### Total HTTP Packets
Total HTTP packets mengacu pada jumlah keseluruhan paket yang dikirimkan dan diterima dalam pertukaran data antara klien dan server menggunakan protokol HTTP. Ini mencakup semua jenis paket, baik permintaan (request) maupun respons (response). Penghitungan total HTTP packets memberikan gambaran umum tentang volume data yang bergerak antara klien dan server selama pertukaran data melalui protokol HTTP. Hal ini dapat digunakan untuk menganalisis lalu lintas jaringan, pemecahan masalah, dan pemantauan kinerja secara keseluruhan.

#### HTTP Request Packets
HTTP request packets mengacu pada jumlah paket yang dikirimkan oleh klien sebagai permintaan kepada server. Setiap kali klien ingin mengakses sumber daya seperti halaman web, gambar, atau data lainnya, klien mengirimkan permintaan HTTP ke server. Permintaan ini berisi metode HTTP (seperti GET, POST, dll.), URL tujuan, header permintaan, dan mungkin data (jika menggunakan metode POST atau PUT). Jumlah HTTP request packets memberikan wawasan tentang seberapa sering klien mengirim permintaan kepada server, membantu dalam pemahaman lalu lintas yang dihasilkan oleh klien.

#### HTTP Response Packets
HTTP response packets mengacu pada jumlah paket yang dikirimkan oleh server sebagai respons terhadap permintaan yang diterima dari klien. Setelah server menerima permintaan HTTP dari klien, ia memprosesnya dan mengirimkan respons yang berisi kode status HTTP, header respons, dan data respons (seperti halaman web atau gambar). Jumlah HTTP response packets memberikan gambaran tentang seberapa banyak data yang dikirimkan oleh server sebagai respons kepada klien. Ini penting untuk memahami berapa besar data yang diunduh dari server ke klien.

##### Informational (1xx)
Kategori ini terdiri dari kode status 1xx. Kode status ini menunjukkan bahwa server telah menerima permintaan klien dan sedang memprosesnya. Respons informatif ini mungkin berisi informasi tambahan atau instruksi tentang proses yang sedang berlangsung. Contohnya adalah 100 Continue yang menandakan server siap untuk menerima data lebih lanjut dari klien.

##### Success (2xx)
Kategori ini terdiri dari kode status 2xx. Kode status ini menunjukkan bahwa permintaan klien telah berhasil diterima, dipahami, dan dijalankan oleh server. Respons sukses biasanya mengandung data yang diminta oleh klien. Contoh umum termasuk 200 OK (permintaan berhasil) dan 204 No Content (permintaan berhasil tetapi tidak ada konten yang harus dikirim).

##### Redirection (3xx)
Kategori ini terdiri dari kode status 3xx. Kode status ini menunjukkan bahwa permintaan klien perlu dialihkan ke lokasi atau URL lain. Respons redirect memberi tahu klien tentang alamat baru tempat sumber daya yang diminta berada. Contoh adalah 301 Moved Permanently (sumber daya telah dipindahkan secara permanen) dan 302 Found (sumber daya ditemukan dengan alamat baru).

##### Client Error (4xx)
Kategori ini terdiri dari kode status 4xx. Kode status ini menunjukkan bahwa ada kesalahan dalam permintaan yang dilakukan oleh klien. Respons client error menandakan bahwa server tidak dapat memproses permintaan karena masalah di pihak klien. Contoh termasuk 404 Not Found (sumber daya tidak ditemukan) dan 400 Bad Request (permintaan tidak dapat dipahami oleh server).

##### Server Error (5xx)
Kategori ini terdiri dari kode status 5xx. Kode status ini menunjukkan bahwa server menghadapi kesalahan internal saat memproses permintaan. Respons server error mengindikasikan bahwa kesalahan terjadi di pihak server. Contoh adalah 500 Internal Server Error (kesalahan internal pada server) dan 503 Service Unavailable (layanan tidak tersedia).

##### Broken
Kategori "broken" dalam konteks respons HTTP tidak umum digunakan dalam istilah resmi. Namun, dalam beberapa kasus, istilah ini mungkin merujuk pada respons yang rusak, tidak lengkap, atau tidak sesuai dengan standar HTTP. Respons yang rusak dapat terjadi karena masalah dalam komunikasi atau penanganan di pihak server atau klien.

#### Field per Topic/Item
##### Count
count merujuk pada jumlah keseluruhan dari elemen tertentu dalam suatu kategori tertentu. Misalnya, dalam analisis protokol jaringan, field count bisa merujuk pada jumlah paket dalam kategori tertentu seperti permintaan atau respons HTTP. Dalam packet counter http di atas, ditunjukkan bahwa total HTTP Packets adalah 4 dengan 2 Response Success HTTP Packets dan 2 GET HTTP Request Packets/

##### Average (Rata-rata)
Average adalah nilai yang dihasilkan dengan menjumlahkan sejumlah nilai dan kemudian membaginya dengan jumlah nilai tersebut. Dalam analisis jaringan, rata-rata dapat digunakan untuk menghitung rata-rata karakteristik seperti ukuran paket, latensi, atau throughput.

##### Min Value (Nilai Minimum)
Min value mengacu pada nilai terendah dalam suatu set data. Dalam analisis jaringan, ini bisa merujuk pada latensi minimum, ukuran paket minimum, atau nilai lainnya yang ingin diukur.

##### Max Value (Nilai Maksimum)
Max value mengacu pada nilai tertinggi dalam suatu set data. Ini digunakan untuk mengukur karakteristik seperti latensi maksimum, ukuran paket maksimum, atau nilai tertinggi lainnya.

##### Rate
Rate adalah angka yang mengindikasikan kecepatan atau frekuensi peristiwa terjadi dalam satu satuan waktu. Misalnya, data transfer rate mengacu pada seberapa cepat data ditransfer dalam waktu tertentu. Di dalam packet counter, Rate-nya adalah 10. 5 ms untuk kecepatan pengiriman HTTP Response Packets dan 5 ms untuk kecepatan pengiriman HTTP Request Packets. 

##### Percent
Percent adalah nilai yang menyatakan proporsi atau bagian dari suatu keseluruhan dalam bentuk persentase. Dalam analisis jaringan, ini bisa merujuk pada persentase penggunaan bandwidth, persentase paket yang hilang, dan lain-lain.

##### Burst Rate
Burst rate mengacu pada kecepatan di mana sejumlah besar data dikirim dalam waktu singkat (burst). Ini penting dalam mengukur bagaimana jaringan atau koneksi menangani lonjakan trafik yang tiba-tiba. Pada packet counter, burst rate masing-masing paket adalah 0.0100.

##### Burst Start
Burst start adalah waktu ketika lonjakan trafik dimulai. Ini menandakan waktu mulai terjadinya lonjakan data yang tinggi.
