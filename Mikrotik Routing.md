# Mikrotik

## Bridge
Bridge adalah perangkat yang digunakan untuk menghubungkan dua atau lebih segmen jaringan yang berbeda, seperti dua jaringan lokal (LAN) yang beroperasi pada protokol berbeda. Bridge berfungsi untuk mengontrol lalu lintas data antara segmen jaringan tersebut. Bridge bekerja pada lapisan datalink (Lapisan 2) dalam OSI Model.
Membuat bridge baru <br>
![alt text](https://github.com/AmirotulUmmah/Konsep-Jaringan/blob/main/assets/winbox-bridge-create.png?raw=true)
![alt text](https://github.com/AmirotulUmmah/Konsep-Jaringan/blob/main/assets/winbox-bridge.png?raw=true)


## Ether
Ethernet adalah salah satu teknologi jaringan yang paling umum digunakan di seluruh dunia. Ini adalah metode komunikasi kabel yang sering digunakan untuk menghubungkan perangkat dalam jaringan lokal (LAN). Ethernet memungkinkan perangkat untuk berkomunikasi melalui kabel fisik atau wireless, dan ada berbagai standar dan kecepatan Ethernet yang berbeda.
Membuat eher baru<br>
![alt text](https://github.com/AmirotulUmmah/Konsep-Jaringan/blob/main/assets/winbox-bridge-create.png?raw=true)
![alt text](https://github.com/AmirotulUmmah/Konsep-Jaringan/blob/main/assets/winbox-bridge.png?raw=true)


## IP Addresses
Mengatur IP Address pada Bridge<br>
![alt text](https://github.com/AmirotulUmmah/Konsep-Jaringan/blob/main/assets/winbox-bridge-address.png?raw=true)

Mengatur IP Address pada Ether<br>
![alt text](https://github.com/AmirotulUmmah/Konsep-Jaringan/blob/main/assets/winbox-bridge-ether.png?raw=true)


## Routing
Menghubungkan antar Router Ether<br>
![alt text](https://github.com/AmirotulUmmah/Konsep-Jaringan/blob/main/assets/winbox-bridge-ether.png?raw=true)


## Topologi Jaringan
![alt text](https://github.com/AmirotulUmmah/Konsep-Jaringan/blob/main/assets/winbox-physical-routing.png?raw=true)

## Konfigurasi

Konfigurasi tiap komponen jaringan

1. Router 0<br>
-Static<br>
Network     : 192.168.9.0<br>
Mask        : 255.255.255.0<br>
Next Hop    : 10.252.108.19<br>
-Fe 0/0<br>
IPv4 Address: 10.252.108.9<br>
Subnet Mask : 255.0.0.0<br>

2. Router 9<br>
-Fe 0/0<br>
IPv4 Address: 10.252.108.19<br>
Subnet Mask : 255.0.0.0<br>
-Fe 1/0<br>
IPv4 Address: 192.168.9.1<br>
Subnet Mask : 255.255.255.0<br>

3. PC 0<br>
IPv4 Address    : 192.168.9.2<br>
Subnet Mask     : 255.255.255.0<br>
Default Gateway : 192.168.9.1<br>

4. PC 1<br>
IPv4 Address    : 192.168.9.3<br>
Subnet Mask     : 255.255.255.0<br>
Default Gateway : 192.168.9.1<br>

5. PC 2<br>
IPv4 Address    : 192.168.9.4<br>
Subnet Mask     : 255.255.255.0<br>
Default Gateway : 192.168.9.1<br>

