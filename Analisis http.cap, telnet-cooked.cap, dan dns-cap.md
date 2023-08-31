# Konsep-Jaringan
<br><br>
## http.cap

http.cap adalah sebuah file yang berisi rekaman lalu lintas jaringan yang terkait dengan protokol http. Isi dari file tersebut tergantung dengan apa protokol http yang digunakan dalam komunikasi tersebut dan berisi serangkaian paket jaringan yang mencakup request dan response http antara client (seperti web browser) dan web server. Setiap paket biasanya mencakup informasi seperti :
1.  IP Address  : berisi alamat IP dari sumber dan tujuan paket
2.  Port        : berisi port dari sumber san tujuan yang digunakan dalam berkomunikasi
3.  Metode http  :
   1. GET
      GET digunakan untuk meminta data dari server. Permintaan ini biasanya digunakna untuk mengambil halaman web atau resource lain dari server. Data yang diminta dikirim sebagai bagain dari URL dalam permintaan. Metode ini tidak mengubah status server atau data unag diminta dan dianggap sebagai operasi yang bersifat idempoten, yakni permintaan yang berulang tidak akan menghasilkan perubahan yang berbeda.
   3. POST
      POST digunakan untuk mengirimkan data ke server untuk diproses. Permintaan POST swring digunakan untuk mengirim data yang akan diolah, seperti saat mengirimkan web form. Data dikirim sebagai bagian dari request body dan dapat digunakan untuk mengirim data yang lebih besar dan kompleks dibandingkan dengan GET. Permintaan POST tidak bersifat idempoten, yakni mengirim [ermintaan yang sama beberapa kali dapat mengahsilkan efek yang berbeda.
   5. PUT
      PUT digunakan untuk mengirim data ke server untuk membuat atau memperbarui lokasi dari resource yang ditentukan. Jika resoiurce belum ada, server akan membuatnya. Jika sudah ada, server akan memperbarui resource dengan data yang dikirim. PUT tidak akan mengubah hasil walaupun mengirim permintaan yang sama beberapa kali
   7. DELETE
      DELETE digunakan untuk menghapus resource yang ditentukan dari server. DELETE akan menghapus resource yang diidentifikasi oleh URL yang diberikan server. Metode ini juga bersifat idempoten, yakni tidak akan mengubah hasil yang dihasilkan walaupun permintaan DELETE dikirim beberapa kali.

