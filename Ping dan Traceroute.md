# Ping dan Traceroute
Oleh  :
Amirotul Ummah (3122600017) - 2 D4 Teknik Informatika A <br>
Mata Kuliah  :
Konsep Jaringan

## Definisi singkat
Konektivitas merupakan kemampuan perangkat atau host untuk terhubung dan berkomunikasi dengan perangkat lain dalam jaringan. Hal ini penting untuk memastikan bahwa aliran data dan informasi dapat berjalan dengan lancar antara berbagai perangkat, baik di dalam jaringan lokal maupun melalui internet. Konektivitas yang baik adalah dasar bagi komunikasi yang efisien dan operasi yang stabil dalam lingkungan teknologi informasi.

Ada beberapa cara untuk menguji konektivitas di dalam jaringan yakni dengan nslookup/dig, telnet, curl/wget, arp, ifconfig/ipconfig, ping6/tracert6, nmap, tcpdump, dan sebagainya. Diantaranya yang paling sederhana adalah ping dan traceroute.

## ping
Ping adalah singkatan dari Packet Internet Network Groper, perintah yang digunakan untuk mengecek status dan keberadaan host dalam sebuah jaringan internet. <br>
![alt text](https://github.com/AmirotulUmmah/Konsep-Jaringan/blob/main/assets/Sistem-Pengukuran-Kedalam-Laut-dengan-Sonar-Sistem.webp?raw=true)
Prinsip kerja ping dapat dianalogikan seperti mengukur kedalaman laut menggunakan sonar. Client akan mengirim sinyal ke dasar laut, setelah sinyal sampai di dasar laut maka akan dipantulkan kembali ke client. Pada ping, client akan mengirimkan paket berupa ICPM_ECHO ke host tujuan dan host akan membalas dengan paket berupa ICMP_ECHOREPLAY

#### Fungsi ping
1. Mengecek keadaan host dan server, apakah aktif atau tidak
2. Mengukur durasi waktu antara respon yang diberikan host dengan request client sebagai petunjuk apakah ada kendala jaringan
3. Melihat kualitas koneksi internet
4. Mengidentifikasi latensi jaringan yang dapat memengaruhi kinerja aplikasi atau layanan
5. Penggunaan ping secara berkala dapat melacak perubahan waktu respons atau masalah yang mungkin muncul

#### Cek Ping
Cara menguji konektivitas dengan ping pada sistem operasi windows yakni dengan membuka Command Prompt dan Windows Powershell lalu mengetikkan perintah ping diikuti dengan alamt domain atau alamat IP.
Setelah cek ping, maka akan didapatkan informasi mengenai :
1. Reply <br> Balasan dari host yang diikuti oleh IP Address. Balasan berupa "Request Timed Out" bisa muncul jika tidak ada balasan sesuai waktu tunggu dari ping tersebut.
2. Bytes <br> Bytes adalah jumlah data yang dikirimkan.
4. Time <br> Time adalah lamanya waktu respon dari host yang dihitung dengan satuan milisecond (ms). Jika konektivitas bagus, maka waktu respon yang dibutuhkan tidak lebih dari 100ms.
5. TTL <br> TTL atau Time To Live merupakan durasi paket data (dalam detik) bisa berada di dalam jaringan dalam waktu berapa lama. Idealnya, TTL diatur pada kisaran 64 detik.

## traceroute
Perintah "tracert" digunakan untuk melacak jalur yang ditempuh oleh paket dalam perjalanannya menuju tujuan tertentu. Proses ini dicapai dengan mengirim pesan ICMP (Internet Control Message Protocol) Echo Request ke tujuan yang diinginkan, dengan meningkatkan nilai Time to Live (TTL) pada setiap paket yang dikirim. Saat nilai TTL ditingkatkan pada setiap paket, paket tersebut melewati sejumlah hop (node atau router) dalam jaringan sebelum akhirnya mencapai tujuan akhir. Dengan menerima respons dari setiap hop, "tracert" dapat memberikan informasi rinci tentang rute yang dilalui oleh paket dalam perjalanan menuju tujuan tersebut.

#### Cek Traceroute
Sama seperti Ping, uji konektivitas pada sistem operasi windows yakni dengan membuka Command Prompt dan Windows Powershell lalu mengetikkan perintah tracert diikuti dengan alamat domain atau IP address yang ingin dilacak.
Setelah itu, akan muncul informasi sebagai berikut :
1. Hop Number <br> nomor urutan hop dalam perjalanan paket dari sumber ke tujuan.
2. Time To Live (TTL) <br> Ini menunjukkan nilai TTL pada paket saat melewati hop tertentu. Nilai TTL menurun setiap kali paket melewati hop, dan jika mencapai nol, paket akan diabaikan.
3. Response Time <br> Waktu yang diperlukan bagi paket untuk mencapai hop tertentu. Biasanya diukur dalam milisecond (ms).
4. Host Name/IP Address <br> Nama host atau alamat IP dari hop yang sedang diuji.
5. Ping Status <br>  Ini menunjukkan apakah "tracert" berhasil menghubungi hop tersebut atau tidak. Tanda "*" atau "Request Timed Out" menunjukkan bahwa hop tidak merespons.



