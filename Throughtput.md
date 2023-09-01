# Throughput
Oleh  :
Amirotul Ummah (3122600017) - 2 D4 Teknik Informatika <br>
Mata Kuliah  :
Konsep Jaringan

Throughput adalah cara untuk mengukur seberapa banyak data yang bisa bergerak melalui jaringan dalam waktu tertentu. Ini seperti mengukur berapa banyak informasi yang bisa "melewati" jaringan dalam waktu singkat. Bayangkan seperti seberapa cepat Anda bisa mengirim atau menerima pesan atau file. Throughput dihitung dalam satuan seperti Kbps, Mbps, atau Gbps. Jadi, semakin tinggi angkanya, semakin banyak data yang bisa diolah dalam waktu yang sama. Namun, ada beberapa faktor yang bisa memengaruhi hasilnya, jadi penting untuk memastikan keseimbangan antara kecepatan, latensi, dan stabilitas jaringan. <br>

![alt text](https://github.com/AmirotulUmmah/Konsep-Jaringan/blob/main/assets/throughput.png?raw=true)<br>

## Segment Length
Segment length mengacu pada ukuran sepotong data yang dikirim melalui jaringan. Ini bisa merujuk pada ukuran paket, frame, atau bagian data lainnya. Informasi ini membantu untuk memahami seberapa besar setiap "potongan" data yang dikirimkan melalui jaringan.
Data yang dikirimkan biasanya dibagi menjadi segmen-segmen dengan panjang tertentu. Setiap segmen memiliki ukuran yang ditentukan dalam bit atau byte. Panjang segmen bisa bervariasi tergantung pada konfigurasi jaringan, protokol yang digunakan, dan perangkat yang terlibat.
Panjang segmen memainkan peran penting dalam efisiensi dan pengaturan lalu lintas jaringan. Jika segmen terlalu kecil, overhead dari header protokol bisa memakan sebagian besar kapasitas, mengurangi efisiensi pengiriman data. Di sisi lain, jika segmen terlalu besar, bisa menyebabkan masalah dengan fragmentasi atau pengiriman data yang tidak optimal.

## MA Window (s)
MA window, singkatan dari Moving Average Window, merujuk pada jendela waktu yang digunakan untuk menghitung rata-rata bergerak dari throughput. Ini adalah interval waktu di mana rata-rata throughput dihitung. Penggunaan jendela waktu ini memungkinkan Anda untuk melihat bagaimana throughput berubah seiring waktu.

## Stream
Stream adalah aliran data yang bergerak melalui jaringan. Dalam beberapa analisis, data dapat dipecah menjadi beberapa aliran yang saling terpisah. Setiap aliran ini bisa berasal dari sumber atau tujuan yang berbeda. Informasi ini membantu dalam memahami bagaimana data bergerak dalam konteks spesifik.

## Goodput
Goodput mengacu pada jumlah data yang berhasil dikirimkan dari sumber ke tujuan dalam satuan waktu tertentu. Ini menghitung jumlah data yang benar-benar berguna dan berhasil tiba di tujuan, mengabaikan overhead atau data yang hilang. Goodput adalah cara untuk mengukur efisiensi sesungguhnya dalam mengirim data.

## Average Throughput
Average throughput menggambarkan jumlah rata-rata data yang berhasil diirimkan dalam satu satuan waktu tertentu. Ini mencakup semua data, baik yang berguna maupun overhead. Average throughput memberi gambaran umum tentang seberapa banyak data yang berhasil ditransfer secara keseluruhan.

## Time
Time adalah waktu yang diperlukan untuk mengirimkan data melalui jaringan. Ini bisa merujuk pada waktu yang diperlukan untuk mengirimkan satu segmen data atau keseluruhan aliran data. Informasi waktu membantu dalam memahami seberapa cepat data bisa bergerak dari sumber ke tujuan. <br><br>

Panjang segmen dapat mempengaruhi rata-rata throughput. Jika segmen lebih besar, jumlah data yang dikirimkan dalam satu waktu akan lebih besar, yang pada akhirnya dapat meningkatkan average throughput. Namun, segmen yang terlalu besar juga dapat menyebabkan fragmentasi atau overhead yang tidak efisien. 

Average throughput terkait dengan jumlah data yang dikirimkan dalam satu waktu tertentu. Time juga terkait dengan waktu yang dibutuhkan untuk mengirimkan data. Keduanya memiliki hubungan langsung: semakin besar average throughput, semakin banyak data yang dikirimkan dalam waktu yang sama, yang berarti data bisa mencapai tujuan lebih cepat.

### Membaca Throughput
![alt text](https://github.com/AmirotulUmmah/Konsep-Jaringan/blob/main/assets/contoh-paket.png?raw=true)
<br>

Berarti :

* "packet 48 (4.847 len 424 seq 1791 ack 480 win 6432)" merujuk pada informasi spesifik tentang paket nomor 48. Setiap bagian dari informasi ini memiliki arti sebagai berikut: <br>
* "4.847" adalah nomor paket.
* "len 424" menunjukkan bahwa panjang paket ini adalah 424 byte.
* "seq 1791" adalah nomor urutan (sequence number) untuk paket ini.
* "ack 480" adalah nomor pengakuan (acknowledgment number) yang diterima dalam respons sebelumnya.
* "win 6432" adalah ukuran window (window size) yang menunjukkan berapa banyak data yang dapat dikirimkan tanpa konfirmasi ulang.
* "-> 18 pkts, 18 kB <- 16 pkts, 479 bytes" adalah informasi throughput yang terkait dengan dua periode waktu yang berbeda:
* "-> 18 pkts, 18 kB" berarti bahwa dalam periode waktu tertentu (misalnya, sejak paket nomor 48), ada 18 paket yang berhasil ditransfer dengan total ukuran data 18 kilobyte (kB).
* "<- 16 pkts, 479 bytes" berarti bahwa dalam periode waktu sebelumnya, ada 16 paket yang berhasil ditransfer dengan total ukuran data sebesar 479 byte.
