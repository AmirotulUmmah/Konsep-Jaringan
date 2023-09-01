# http_witp_jpegs.cap
Oleh  :
Amirotul Ummah (3122600017) - 2 D4 Teknik Informatika <br>
Mata Kuliah  :
Konsep Jaringan
 ## Menampilkan Gambar
 Di dalam file http_witp_jpegs.cap terdapat banyak baris packets, diantaranya adalah gambar berupa JPEG JFIF image.
### Mencari protokol HTTP
![alt text](https://github.com/AmirotulUmmah/Konsep-Jaringan/blob/main/assets/httpwitpjpegscap.png?raw=true)<br>
File tersebut berisi ratusan packets sehingga sulit mendeteksi packets yang dikirim melalui HTTP Protocol. Oleh karena itu, packets tersebut difilter sehingga yang ditampilkan adalah packets dengan protokol HTTP saja.
### Mencari respon server untuk permintaan gambar
![alt text](https://github.com/AmirotulUmmah/Konsep-Jaringan/blob/main/assets/200ok.png?raw=true)<br>
File tersebut merupakan bentuk response sukses dari server. Kode status "200 OK" menunjukkan bahwa server telah berhasil menemukan dan mengirimkan konten yang diminta oleh klien. Pada baris sebelumnya, klien mengirim permintaan GET untuk halaman web, respons "200 OK" menunjukkan bahwa halaman web tersebut telah ditemukan dan dikirimkan kembali kepada klien dengan sukses.
Packet tersebut berisi suatu gambar karena pada baris sebelumnya, klien meminta GET/Websidan/IMAGES/bg2.jpg HTTP/1.1 dan direspon oleh server dengan HTTP/1.1 200 OK.
### Membuka packet gambar
![alt text](https://github.com/AmirotulUmmah/Konsep-Jaringan/blob/main/assets/showpacket.png?raw=true)<br>
Klik paket dengan respons server HTTP/1.1 200 OK, kemudian klik Kanan pada bagian "JPEG File Interchange Format" dan pilih Show Packet Bytes.
### Gambar di dalam packet
![alt text](https://github.com/AmirotulUmmah/Konsep-Jaringan/blob/main/assets/packetgambar.png?raw=true)

## Gambar di http_witp_jpegs.cap
![alt text](https://github.com/AmirotulUmmah/Konsep-Jaringan/blob/main/assets/sydney.png?raw=true)
![alt text](https://github.com/AmirotulUmmah/Konsep-Jaringan/blob/main/assets/seaworld1.png?raw=true)
![alt text](https://github.com/AmirotulUmmah/Konsep-Jaringan/blob/main/assets/seaworld.png?raw=true)
![alt text](https://github.com/AmirotulUmmah/Konsep-Jaringan/blob/main/assets/dolphin.png?raw=true)


