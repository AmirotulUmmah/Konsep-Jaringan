# Pinging

Pinging merupakan proses untuk menguji koneksi jaringan antara dua perangkat jaringan dengan mengirimkan paket data ke perangkat tujuan dan menerima balasan dari perangkat terkait.

## Ping antar PC

![alt text](https://github.com/AmirotulUmmah/Konsep-Jaringan/blob/main/assets/ping%20pc1.jpeg?raw=true)
![alt text](https://github.com/AmirotulUmmah/Konsep-Jaringan/blob/main/assets/ping%20pc3.jpeg?raw=true)
![alt text](https://github.com/AmirotulUmmah/Konsep-Jaringan/blob/main/assets/ping%20pc2.jpeg?raw=true)

## Print IP Route

Print IP Route adalah perintah dalam sistem operasi Mikrotik RouterOS untuk menampilkan tabel routing IP yang dikonfigurasi pada perangkat Miktrotik. Di dalamnya tertera informasi terkait jaringan tujuan, gateway, dan informasi lainnya. <br>


![alt text](https://github.com/AmirotulUmmah/Konsep-Jaringan/blob/main/assets/routing%20table.jpeg?raw=true)

#### Flags
Bagian ini memberikan informasi tentang status atau sifat dari setiap entry dalam tabel routing. Berikut adalah arti dari beberapa flags yang ada pada output tersebut
X: Jalur dinonaktifkan (disabled).
A: Jalur aktif (active).
D: Jalur didapat secara dinamis (dynamic).
C: Jalur terhubung (Connect).
S: Jalur ditentukan secara statis (static).
r: Jalur diperoleh melalui protokol RIP.
b: Jalur diperoleh melalui protokol BGP.
o: Jalur diperoleh melalui protokol OSPF.
m: Jalur diperoleh melalui protokol MME.
B: Tidak mengirimkan paket yang melewati jalur ini.
U: Jalur tidak dapat dicapai (unreachable).
P: Jalur dilarang (prohibit).

#### DST ADDRESS
Ini adalah alamat jaringan tujuan (destination network) dalam bentuk CIDR (Classless Inter-Domain Routing).

#### PREF-SRC
Ini adalah alamat sumber (preferred source) yang terkait dengan jaringan tujuan. Ini adalah alamat IP yang digunakan untuk mengirim paket ke jaringan tujuan.

#### GATEWAY
Ini adalah gateway atau next hop yang akan digunakan untuk mengirim paket ke jaringan tujuan.

#### DISTANCE
Ini adalah jarak atau metric yang menunjukkan seberapa baik atau seberapa buruk jalur tersebut dalam tabel routing. Semakin rendah nilai DISTANCE, semakin baik jalur tersebut.

# Topologi Jaringan

Topologi jaringan komputer merupakan suatu teknik menghubungkan komputer untuk membentuk jaringan, menggunakan berbagai jenis media transmisi seperti kabel UTP, fiber optic, atau wireless yang memungkinkan komunikasi antar perangkat dari lokasi yang berbeda.

Topologi jaringan dibagi menjadi dua golongan yakni :
1. Physical Model
2. Logical Model

## Physical Model

Berikut merupakan physical model dari komponen jaringan yang digunakan di dalam praktikum<br>
![alt text](https://github.com/AmirotulUmmah/Konsep-Jaringan/blob/main/assets/MIKROTIK%20(3).png?raw=true)

Pada router board ini, port ETH1 terhubung ke router utama, sementara port ETH3, ETH4, dan ETH5 terhubung secara berurutan ke PC3, PC2, dan PC1. Selain itu, port eth6 terhubung ke sebuah hub. Dengan konfigurasi ini, router board ini dapat menghubungkan router utama dengan tiga komputer (PC1, PC2, dan PC3) melalui port ETH3, ETH4, dan ETH5, serta terhubung ke perangkat lain melalui hub yang terhubung ke port ETH6.

## Logical Model

Berikut adalah logical model koneksi dari router board ke pc<br>
![alt text](https://github.com/AmirotulUmmah/Konsep-Jaringan/blob/main/assets/logical%20model%20pc.png?raw=true)

Berikut adalah logical model antar router<br>
![alt text](https://github.com/AmirotulUmmah/Konsep-Jaringan/blob/main/assets/logical%20model%20router.png?raw=true)
