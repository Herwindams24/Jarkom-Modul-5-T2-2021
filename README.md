# Lapres Modul 4 Jarkom 2021 - T02
Laporan Hasil Praktikum Modul 4 Jarkom 2021
Kelompok T02
  * Herwinda Marwaa Salsabila (05311940000009)
  * Dian Arofati N. Z. (05311940000011)
  * Dava Aditya Jauhar (05311940000030)

---

## Tabel Soal

* [Soal A](#soal-a)
* [Soal B](#soal-b)
* [Soal C](#soal-c)
* [Soal D](#soal-d)
* [Soal 1](#soal-1)
* [Soal 2](#soal-2)
* [Soal 3](#soal-3)
* [Soal 4](#soal-4)
* [Soal 5](#soal-5)
* [Soal 6](#soal-6)

## Soal A
Tugas pertama kalian yaitu membuat topologi jaringan sesuai dengan rancangan yang diberikan Luffy dibawah ini:

<img src="https://user-images.githubusercontent.com/73151892/145213179-2eb2f5da-6ded-4f6b-9851-43fffb2ddc4c.png">


Keterangan : 

* Doriki adalah DNS Server
* Jipangu adalah DHCP Server
* Maingate dan Jorge adalah Web Server
* Jumlah Host pada Blueno adalah 100 host
* Jumlah Host pada Cipher adalah 700 host
* Jumlah Host pada Elena adalah 300 host
* Jumlah Host pada Fukurou adalah 200 host

## Soal B
Karena kalian telah belajar subnetting dan routing, Luffy ingin meminta kalian untuk membuat topologi tersebut menggunakan teknik CIDR atau VLSM.

Setelah membuat topologi seperti pada soal A, kami melakukan subnetting dengan metode CIDR, dan Prefix IP yang digunakan yaitu 192.212.0.0

1. Menentukan pembagian subnet dan melakukan labeling di setiap subnetnya. Diperoleh subnet A1-A8 sseperti pada gambar berikut

   <img src="https://user-images.githubusercontent.com/73151892/145214037-f892559f-c3ea-407a-8691-83a5797a1305.png">
2. Kemudian menggabungkan subnet A yang paling jauh dari router dengan label subnet B
   
3. Selanjutnya melakukan labeling subnet C
   <img src="https://user-images.githubusercontent.com/73151892/145214542-eb9bb64f-cde6-4045-aa79-de7cbc41f5a6.png">
4. Melakukan labeling subnet D

5. Melakukan labeling subnet E
   <img src="https://user-images.githubusercontent.com/73151892/145214883-343064e0-5cd0-4593-98ea-9464987ac434.png">

Setelah memberi label subnet, selanjutnya melakukan pembagian IP dengan menggunakan tree
1. Sebelum membagi IP menggunakan tree, terlebih dahulu menghitung jumlah host pada subnet A untuk menentukan netmasknya, dan diperoleh hasil sebagai berikut :

   <img src="https://user-images.githubusercontent.com/73151892/145215014-5615a535-6437-4047-b47e-3986985a0791.png">
2. Selanjutnya menentukan netmask untuk subnet B, C, D, dan E
   <img src="https://user-images.githubusercontent.com/73151892/145215187-4fe09e5f-e8e1-4a64-a8ef-b582f898558e.png">
3. Kemudian melakukan pembagian IP menggunakan tree sesuai dengan netmask yang telah ditentukan sebelumnya. 
   <img src="https://user-images.githubusercontent.com/73151892/145215639-1e80d32d-0019-416e-96cf-fa69e5194d88.png">
4. Dari tree tersebut diperoleh NID tiap subnet, sehingga dapat ditentukan pula broadcast addressnya.
   <img src="https://user-images.githubusercontent.com/73151892/145215795-a272fcd9-0a35-4407-ac21-3b490249c127.png">
   
## Soal C
## Soal D
## Soal 1

## Konfigurasi Network pada GNS3

1. Pada Router
   
   * Pada Foosha

     Pertama-tama, penulis menghubungkan router Foosha melalui eth0 menuju NAT dengan DHCP.

       <img src="https://github.com/Herwindams24/Jarkom-Modul-5-T2-2021/blob/main/image/Konfigurasi%20Network/Konfigurasi%20Foosha.png" width="300" height="300">

   * Pada Water7

       <img src="https://github.com/Herwindams24/Jarkom-Modul-5-T2-2021/blob/main/image/Konfigurasi%20Network/Konfigurasi%20Water%207%201.png" width="300" height="300">
         
       <img src="https://github.com/Herwindams24/Jarkom-Modul-5-T2-2021/blob/main/image/Konfigurasi%20Network/Konfigurasi%20Water%207%202.png" width="300" height="300">

   * Pada Guanhao

       <img src="https://github.com/Herwindams24/Jarkom-Modul-5-T2-2021/blob/main/image/Konfigurasi%20Network/Konfigurasi%20Guanhao%201.png" width="300" height="300">
         
       <img src="https://github.com/Herwindams24/Jarkom-Modul-5-T2-2021/blob/main/image/Konfigurasi%20Network/Konfigurasi%20Guanhao%202.png" width="300" height="300">

2. Pada DNS Server (DORIKI)
   
    <img src="https://github.com/Herwindams24/Jarkom-Modul-5-T2-2021/blob/main/image/Konfigurasi%20Network/Konfigurasi%20Doriki.png" width="300">

3. Pada DHCP Server (JIPANGU)
   
    <img src="https://github.com/Herwindams24/Jarkom-Modul-5-T2-2021/blob/main/image/Konfigurasi%20Network/Konfigurasi%20Jipangu.png" width="300">

4. Pada Client

    * Pada Blueno
  
      <img src="https://github.com/Herwindams24/Jarkom-Modul-5-T2-2021/blob/main/image/Konfigurasi%20Network/Konfigurasi%20Blueno.png" width="300">

    * Pada Cipher

      <img src="https://github.com/Herwindams24/Jarkom-Modul-5-T2-2021/blob/main/image/Konfigurasi%20Network/Konfigurasi%20Cipher.png" width="300">

    * Pada Elena
  
      <img src="https://github.com/Herwindams24/Jarkom-Modul-5-T2-2021/blob/main/image/Konfigurasi%20Network/Konfigurasi%20Elena.png" width="300">

    * Pada Fukurou
  
      <img src="https://github.com/Herwindams24/Jarkom-Modul-5-T2-2021/blob/main/image/Konfigurasi%20Network/Konfigurasi%20Fukurou.png" width="300">

5. Pada Web Server

    * Pada Jorge
    
      <img src="https://github.com/Herwindams24/Jarkom-Modul-5-T2-2021/blob/main/image/Konfigurasi%20Network/Konfigurasi%20Jorge.png" width="300">
    
    * Pada Maingate
    
      <img src="https://github.com/Herwindams24/Jarkom-Modul-5-T2-2021/blob/main/image/Konfigurasi%20Network/Konfigurasi%20Maingate.png" width="300">
      
## Konfigurasi C

Lakukan Routing agar setiap perangkat pada jaringan tersebut terhubung.

* Routing pada Router Foosha sebagai berikut

  ```
  # =========================== Foosha ke Kiri START HERE =====================###
  # routing ke a4 WATER7
    route add -net 192.212.16.0 netmask 255.255.255.252 gw 192.212.16.2
  # routing ke a2 client BLUENO
    route add -net 192.212.8.0 netmask 255.255.255.128 gw 192.212.16.2
  # routing ke a3 client CIPHER
    route add -net 192.212.0.0 netmask 255.255.252.0 gw 192.212.16.2
  # routing ke a1 Server Doriki dan Jipangu
    route add -net 192.212.4.0 netmask 255.255.255.248 gw 192.212.16.2
  # =========================== Foosha ke Kanan START HERE =====================#$
  # routing ke a5 GUANHAO
    route add -net 192.212.36.0 netmask 255.255.255.252 gw 192.212.36.2  
  # routing ke a6 ELENA
    route add -net 192.212.34.0 netmask 255.255.254.0 gw 192.212.36.2
  # routing ke a7 FUKUROU
    route add -net 192.212.32.0 netmask 255.255.255.0 gw 192.212.36.2
  # routing ke a8 SERVER JORGE-MAINGATE
    route add -net 192.212.33.0 netmask 255.255.255.248 gw 192.212.36.2
  ```

* Routing pada Router Water7 sebagai berikut

 ```
 ```

* Routing pada Router Guanhao sebagai berikut
  
  ```
  ```
