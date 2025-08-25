# LAB-45-policy-route
tanggal 24 agustus 2025

# policy-route
PBR (Policy Based Route) merupakan fitur yang berfungsi untuk memetakan jalur. Kita bisa memetakan berdasarkan alamat IP asal, IP tujuan, bisa juga kita buat yang lebih spesifik lagi berdasarkan koneksi (port dan protokol).

![](r12.PNG)

**Konfigurasi**
Pada tahap ini, pastikan kita sudah melakukan basic config (IP Address, DNS, NAT, dll). Kemudian kita bisa coba untuk lakukan konfigurasi PBR. Pada kasus ini kita akan konfigurasi PBR1 menggunakan Route Rules.

# konfigurasi policy based route failover netwatch mikrotik
1. seting dhcp client dulu disini isp saya dari ether 1 dan wlan1
   pilih menu ip > dhcp client klik add 

![](r3.PNG)

2. lalu buat ip address untuk LAN1 dan LAN2
   di menu ip > address 

![](r5.PNG)

3. berikutnya buat dhcp server untuk ether 2 dan 3 kenpa yang ether2 saya merah karena tida terhubug/blm tercolokkan
   pilih menu ip > dhcp server

![](r4.PNG)

4.  lalu setting firewall dengan action kedua nya menggunakan masquerade
    di menu ip > firewall

![](r6.PNG)

5. jika sudah maka kita akan melakukan konfigurasi berikutnta yaitu route
   pilih menu ip > routes > rules konfigurasi seperti gambar berikut

![](r7.PNG)

6. selanjutnya kita beralih ke tab routes untuk membuat route netwach

![](r8.PNG)

7. masi di tab routes kita buat juga konfigurasi policy based routes

![](r9.PNG)

8. konfigurasi route untuk link backup

![](r10.PNG)

9. konfigurasi netwatch
   di menu tools > netwatch

   ![](r11.PNG)

   ![](r11.1.PNG)

   ![](r11.2.PNG)

# pengujian 
1. tracert di laptop kuning

![m](r1.PNG)

2. tracert di laptop biru

![m](r2.PNG)

# kesimpulan
Policy-Based Routing (PBR) adalah metode pengaturan lalu lintas jaringan yang memungkinkan administrator jaringan untuk membuat keputusan routing berdasarkan kebijakan tertentu, bukan hanya berdasarkan tabel routing standar. Dengan PBR, lalu lintas dapat diarahkan berdasarkan parameter seperti alamat IP sumber/destinasi, jenis protokol, port, atau bahkan ukuran paket.
# sumber 
https://youtu.be/lYLvUE9tRbc?si=65SQiZwTBG7DGSuz
