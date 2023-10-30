# Routing
Routing adalah proses mengalihkan lalu lintas data di jaringan dari satu tempat ke tempat lain dengan cara yang paling efisien, umumnya melibatkan penggunaan tabel routing dan protokol routing. Ini memungkinkan komunikasi di seluruh jaringan.

#### Macam-Macam Router
Routing terbagi menjadi dua macam :
1. Routing Statis<br> Dalam routing statis, administrator jaringan secara manual mengkonfigurasi tabel routing pada perangkat jaringan. Ini tidak berubah secara otomatis dan cocok untuk jaringan yang tidak berubah secara signifikan.
2. Routing Dinamis<br> Dalam routing dinamis, protokol routing digunakan untuk memungkinkan perangkat jaringan berkomunikasi satu sama lain dan memperbarui tabel routing secara otomatis. Ini cocok untuk jaringan yang lebih besar dan berubah-ubah.

#### Jenis-Jenis Router
Ada beberapa jenis router yang digunakan, diantaranya:

1. Core Router<br> Core router adalah router yang digunakan di pusat jaringan atau data center untuk mengarahkan lalu lintas antara berbagai jaringan. Mereka dirancang untuk menangani lalu lintas yang sangat besar dan memiliki kapabilitas tinggi dalam hal throughput dan keandalan.
2. Edge Router<br> Edge router, seperti yang telah dijelaskan sebelumnya, adalah router yang berada di "pinggiran" jaringan, menghubungkan jaringan lokal dengan jaringan eksternal seperti internet. Mereka juga sering berfungsi sebagai firewall dan melakukan fungsi NAT.
3. Access Router<br>Access router adalah router yang digunakan di ujung jaringan dan menghubungkan pengguna akhir atau jaringan lokal ke jaringan yang lebih besar atau inti jaringan.
4. Provider Edge Router (PE Router)<br> PE router digunakan oleh penyedia layanan internet (ISP) untuk menghubungkan jaringan pelanggan ke jaringan inti ISP dan jaringan global. Mereka sering memiliki fitur seperti MPLS (Multiprotocol Label Switching) untuk mengelola lalu lintas pelanggan.
5. Customer Edge Router (CE Router)<br>CE router adalah router yang digunakan oleh pelanggan untuk menghubungkan jaringan lokal mereka dengan jaringan penyedia layanan internet (ISP) melalui jalur sewa atau koneksi lainnya.

## Routing PENS
Berikut adalah routing IPv4 (Internet Protocol version 4) di dalam AS46052 (PENS) yang terhubung dengan AS4761 (INDOSAT Internet Network Provider) dan AS7713 (PT Telekomunikasi Indonesia)<br><br>
![alt text](https://github.com/AmirotulUmmah/Konsep-Jaringan/blob/main/assets/V4.png?raw=true)

## Percobaan
![alt text](https://github.com/AmirotulUmmah/Konsep-Jaringan/blob/main/assets/topology.png?raw=true)
Setiap router dalam berperan sebagai router jaringan dan juga sebagai gateway untuk host yang terhubung ke subnet mereka. Keseluruhan topologi ini membutuhkan pengaturan jaringan yang cukup kompleks dan memfasilitasi lalu lintas data antara host-host dalam subnet yang berbeda.
