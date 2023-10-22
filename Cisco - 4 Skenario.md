## TOPOLOGI JARINGAN
##### Switch
![alt text](https://github.com/AmirotulUmmah/Konsep-Jaringan/blob/main/assets/topologi%20switch.jpeg?raw=true)

##### Hub
![alt text](https://github.com/AmirotulUmmah/Konsep-Jaringan/blob/main/assets/topologi%20hub.jpeg?raw=true)

## SKENARIO 1
##### PC0 ping PC1 (Switch)

![alt text](https://github.com/AmirotulUmmah/Konsep-Jaringan/blob/main/assets/sken-1.jpeg?raw=true)

1. PC0 (192.168.1.2) akan mencoba mengirimkan paket ICMP ping ke PC1 (192.168.1.3).
2. PC0 akan memeriksa alamat IP tujuan (192.168.1.3) dan menentukan bahwa alamat tersebut berada dalam jaringan lokalnya (192.168.1.0/24).
Sekarang, karena alamat IP tujuan berada dalam jaringan yang sama, PC0 akan mencoba menemukan alamat MAC (Media Access Control) dari PC1 agar dapat mengirimkan paket ICMP ping ke alamat MAC yang benar. Ini dilakukan melalui proses ARP (Address Resolution Protocol).
1. PC0 akan mengirimkan permintaan ARP broadcast ke seluruh perangkat dalam jaringan lokal (192.168.1.0/24) untuk mencari tahu alamat MAC dari PC1 (192.168.1.3). Pesan ARP ini akan berisi alamat IP pengirim (192.168.1.2) dan alamat IP tujuan (192.168.1.3).
2. Switch 0 menerima pesan ARP broadcast dan akan memeriksa tabel MAC address-nya. Jika switch 0 sudah tahu alamat MAC PC1 (misalnya karena telah mengirim paket sebelumnya), maka switch akan langsung meneruskan pesan ARP tersebut ke PC1.
3. PC1 (192.168.1.3) akan menerima permintaan ARP dan akan membalas dengan mengirimkan alamat MAC-nya ke PC0.
4. Setelah PC0 menerima alamat MAC PC1 dari balasan ARP, PC0 dapat mengemas paket ICMP ping dengan alamat MAC tujuan yang benar dan mengirimkannya ke switch 0.
5. Switch 0 menerima paket ICMP ping dari PC0 dan mengarahkannya ke PC1 berdasarkan alamat MAC yang sesuai.
6. PC1 menerima paket ICMP ping dari PC0 dan merespons dengan paket balasan ICMP ping.

Proses ini akan menyebabkan PC0 mengirim permintaan ARP broadcast awal untuk menemukan alamat MAC PC1, tetapi setelah itu, komunikasi antara PC0 dan PC1 akan berlangsung langsung dengan menggunakan alamat MAC yang benar. Setelah itu, PC0 dan PC1 dapat saling bertukar paket ICMP ping.

## SKENARIO 2
##### PC0 ping PC2(Switch)

![alt text](https://github.com/AmirotulUmmah/Konsep-Jaringan/blob/main/assets/sken-2%20(2).jpeg?raw=true)

Dalam skenario ini, jika kita mencoba melakukan ping dari PC0 ke PC21, yang berada pada jaringan yang berbeda, maka akan terjadi serangkaian proses yang lebih kompleks yang melibatkan router. Alur yang akan terjadi adalah sebagai berikut:

1. PC0 (192.168.1.2) akan mencoba mengirimkan paket ICMP ping ke PC21 (misalkan IP 192.168.10.2).
2.PC0 akan memeriksa alamat IP tujuan (192.168.10.2) dan menentukan bahwa alamat tersebut berada dalam jaringan yang berbeda dari jaringan lokalnya (192.168.1.0/24).

Sekarang, karena alamat IP tujuan berada dalam jaringan yang berbeda, PC0 akan mencoba menemukan alamat MAC dari router agar dapat mengirimkan paket ICMP ping ke router. Ini juga dilakukan melalui proses ARP.

1. PC0 akan mengirimkan permintaan ARP broadcast untuk mencari tahu alamat MAC router yang bertindak sebagai gateway ke jaringan tujuan (192.168.10.0/24). Pesan ARP ini akan berisi alamat IP pengirim (192.168.1.2) dan alamat IP tujuan (IP router, misalkan 192.168.1.1).
2. Switch 0 akan menerima pesan ARP broadcast dari PC0 dan akan meneruskannya ke semua perangkat di dalam jaringan lokal (192.168.1.0/24) untuk mencari alamat MAC router.
3. Router 1 (IP 192.168.1.1) akan merespons permintaan ARP dari PC0 dengan mengirimkan alamat MAC-nya ke PC0.
4. Setelah PC0 menerima alamat MAC router, PC0 dapat mengemas paket ICMP ping dengan alamat MAC router sebagai alamat MAC tujuan dan mengirimkannya ke switch 0.
5. Switch 0 akan meneruskan paket ICMP ping ke router 1.
6. Router 1 akan menerima paket ICMP ping dari PC0 dan akan memeriksa tabel rutingnya untuk menentukan cara terbaik untuk mengirimkan paket ke tujuan, yaitu PC21 (misalkan IP 192.168.10.2)
7. Router 1 akan mengirimkan paket ICMP ping ke switch 1 karena PC21 terhubung ke switch 1.
8. Switch 1 akan meneruskan paket ICMP ping ke PC21.
9. PC21 (IP 192.168.10.2) akan menerima paket ICMP ping dari router dan akan merespons dengan paket balasan ICMP ping.

## SKENARIO 3
##### PC0 ping PC1(Hub)

![alt text](https://github.com/AmirotulUmmah/Konsep-Jaringan/blob/main/assets/sken-3.jpeg?raw=true)

Jika Anda mengganti switch dengan hub dalam susunan yang sama, alur komunikasi antara PC0 dan PC1 akan berbeda karena hub bekerja secara berbeda daripada switch. Hub adalah perangkat jaringan yang mengirimkan data yang diterima kepada semua perangkat yang terhubung ke dalamnya, sementara switch memiliki kemampuan untuk mengirim data hanya ke perangkat yang tepat. Berikut adalah alur komunikasi antara PC0 dan PC1 dengan penggunaan hub:

1. PC0 (192.168.1.2) akan mencoba mengirimkan paket ICMP ping ke PC1 (192.168.1.3).
2. PC0 akan memeriksa alamat IP tujuan (192.168.1.3) dan menentukan bahwa alamat tersebut berada dalam jaringan lokalnya (192.168.1.0/24).
3. PC0 akan mengirimkan paket ICMP ping ke alamat MAC yang sesuai dengan alamat IP PC1.

Namun, di sini perbedaan terjadi:

1. Hub yang terhubung ke PC0 dan PC1 akan menerima paket ICMP ping dari PC0.
2. Hub akan mengirimkan paket ICMP ping tersebut ke semua perangkat yang terhubung ke dalamnya, termasuk PC1.
3. PC1 akan menerima paket ICMP ping dari hub dan merespons dengan paket balasan ICMP ping.

Dalam penggunaan hub, pesan dikirimkan ke semua perangkat dalam jaringan yang terhubung ke hub, dan bukan hanya ke perangkat yang dituju. Ini berarti semua perangkat dalam jaringan lokal (termasuk PC0 dan PC1) akan menerima paket ICMP ping yang dikirimkan oleh PC0.

## SKENARIO 4
##### PC0 ping PC1(Hub)

![alt text](https://github.com/AmirotulUmmah/Konsep-Jaringan/blob/main/assets/sken-4.jpeg?raw=true)

Di bawah ini adalah alur komunikasi antara PC0 dan PC2 dengan menggunakan hub:

1. PC0 (192.168.1.2) akan mencoba mengirimkan paket ICMP ping ke PC2 (192.168.6.2).
2. PC0 akan memeriksa alamat IP tujuan (192.168.6.2) dan menyadari bahwa alamat tersebut berada dalam jaringan yang berbeda dari jaringan lokalnya (192.168.1.0/24).
3. PC0 akan mengirimkan paket ICMP ping dengan alamat MAC tujuan yang sesuai dengan alamat IP router (misalkan 192.168.1.1).
4. Hub yang terhubung ke PC0 dan PC2 akan menerima paket ICMP ping dari PC0.
5. Hub akan mengirimkan paket ICMP ping tersebut ke semua perangkat yang terhubung ke dalamnya, termasuk PC2.
6. PC2 akan menerima paket ICMP ping dari hub dan merespons dengan paket balasan ICMP ping.

## Kesimpulan

Skenario pertama (menggunakan switch): Ketika PC0 ping PC1 dalam jaringan yang sama dengan menggunakan switch, switch akan mengarahkan lalu lintas hanya ke perangkat yang benar (PC1) berdasarkan alamat MAC. Ini efisien dan tidak membanjiri seluruh jaringan.

Skenario kedua (menggunakan switch): Ketika PC0 ping PC21 di jaringan yang berbeda dengan menggunakan switch, switch dan router akan berkolaborasi untuk mengirimkan paket melalui jalur yang benar. Ini memungkinkan komunikasi antara jaringan yang berbeda.

Skenario ketiga (menggunakan hub): Ketika PC0 ping PC1 dalam jaringan yang sama dengan menggunakan hub, hub akan mengirimkan paket ke semua perangkat dalam jaringan, termasuk PC1. Ini tidak efisien dan membanjiri lalu lintas.

Skenario keempat (menggunakan hub): Ketika PC0 ping PC2 di jaringan yang berbeda dengan menggunakan hub, hub akan mengirimkan paket ke semua perangkat dalam jaringan, termasuk PC2. Ini juga tidak efisien dan tidak ideal dalam jaringan modern.

Kesimpulannya, penggunaan switch dalam jaringan jauh lebih efisien dibandingkan dengan hub karena switch dapat mengarahkan lalu lintas ke perangkat yang benar berdasarkan alamat MAC, sedangkan hub mengirimkan lalu lintas ke semua perangkat yang terhubung. Router digunakan untuk menghubungkan jaringan yang berbeda dan mengatur lalu lintas antara mereka. Dalam jaringan modern, penggunaan switch dan router umumnya lebih disarankan daripada hub karena meningkatkan kinerja dan efisiensi.
