# CISCO PACKET TRACER

Cisco adalah sebuah software untuk simulasi jaringan yang dikembangkan oleh Cisco System. Software ini memungkinkan pengguna untuk merancang, membangun, dan menguji jaringan komputer secara virtual tanpa perlu memiliki perangkat jaringan fisik yang sesungguhnya. Pengguna dapat merancang dan menguji topologi jaringan secara efisien serta mengidentifikasi potensi masalah yang akan muncul di dunia nyata. Pengguna dapat membuat skenario yang berbeda untuk melihat berbagai kemungkinan bagaimana jaringan bekerja di beberapa situasi

## Komponen di dalam Cisco

Di dalam Cisco, ada berbagai jenis komponen yang digunakan dalam jaringan komputer, berikut adalah komponen dan cara kerjanya:

1. Router <br> Menghubungkan jaringan atau subnet dan mengarahkan lalu lintas data.
2. Switch <br> Menghubungkan berbagai perangkat di Local Area Network (LAN) dan memeriksa alamat Media Access Control (MAC)
3. Firewall <br> Perangkat untuk mengamankan jaringan berdasarkan kebijakan keamanan
4 Access Point <br> Perangkat untuk menghubungkan perangkat wireless ke jaringan kabel serta memungkinkan perangkat unruk terhubung ke jaringan Wi-Fi
5. Server <br> Menyediakan layanan atau resource ke perangkat lain dalam jaringan
6. Cable and Fiber <br> Menghubungkan antar perangkat dalam jaringan. Kabel tembaga biasanya digunakna di dalam jaringan LAN dan serat optik digunakan untuk jaringan yang memerlukan kecepatan serta kapasitas tinggi.

## Percobaan Jaringan

Berikut adalah contoh konfigurasi jaringan sederhana yang terdiri dari Router, Switch, dan PC.

Keterangan Konfigurasi yang dibuat :
![alt text](https://github.com/AmirotulUmmah/Konsep-Jaringan/blob/main/assets/soal_cisco.jpeg?raw=true)

Percobaan 
![alt text](https://github.com/AmirotulUmmah/Konsep-Jaringan/blob/main/assets/cisco.png?raw=true)

Router 0 dan Router 1 disambungkan menggunakan copper cross-over 
Kabel cross-over digunakan ketika menghubungakan perangkat yang sama karena perangkat tersebut biasanya memiliki pengirim dan penerima yang sama dengan pin berbeda. Kabel ini digunakan untuk memastikan bahwa pengirim pada suatu perangkat terhubung ke penerima yang sesuai pada perangkat lain.
Contoh :
Router ke Router

Kemudian Switch0 disambungkan ke Router 0 dan disambungkan ke PC0 dan PC2 menggunakan copper straight-through
Sedangkan Switch2 disambungkan ke Router 1 dan disambungkan ke PC1 dan PC3 menggunakan copper straight-through

Kabel Straight-Through digunakan ketika menghubungkan perangkat yang berbeda. Pengirim pada satu perangkat terhubung ke penerima yang sesuai pada perangkat lain.
Contoh :
Router ke Switch atau Komputer ke Switch


Router 0 memiliki fe 0/1 = 10.0.1.1 dan fe 0/0 = 192.168.1.1
Router 1 memiliki fe 0/1 = 10.0.1.2 dan fe 0/0 = 192.168.2.1

IP Address PC0 = 192.168.1.10 dan IP Address PC2 = 192.168.1.20
IP Address PC1 = 192.168.2.10 dan IP Address PC3 = 192.168.2.20

Konfigurasi jaringan berhasil dilakukan sehingga keempat PC dapat ping satu sama lain. Berikut adalah analisis dari konfigurasi yang telah dilakukan :
1. Alamat IP yang tepat 
2. Konfigurasi Router <br> Konfigurasi router pada jaringan tersebut sudah tepat, Router1 dan Router0 menggunakan kabel crossover. Koneksi ini menghubungkan dua jaringan yang berbeda dan memungkinkan lalu lintas antar subnet
3. Switch <br> Switch terhubungan ke Router0, PC0, dan PC2, sementara Switch2 terhubung ke Router1, PC1, dan PC3. Ini memungkinkan antar perangkat PC pada masing-masing Switch dapat berkomunikasi dengan router yang sesuai dengan dan perangkat subnet yang sama
4. Pengiriman paket <br> Ketika salah satu PC ingin melakukan ping ke PC yang lain, paket data akan dikirimkan melalui router yang sesuai (Router0 atau Router1) serta Switch yang tepat. Karena router telah dikonfigurasi dengan benar dan perangkat berada dalam subnet yang benar, maka mereka dapat mengirimkan paket data ke tujuan dengan benar.

Maka seluruh elemen jaringan telah dikonfigurasi dengan benar untuk memungkinkan komunikasi antar PC0, PC2, PC1, dan PC3 berhasil dilakukan.
