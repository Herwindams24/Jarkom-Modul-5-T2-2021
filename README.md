# Lapres Modul 4 Jarkom 2021 - T02
Laporan Hasil Praktikum Modul 4 Jarkom 2021
Kelompok T02
  * Herwinda Marwaa Salsabila (05311940000009)
  * Dian Arofati N. Z. (05311940000011)
  * Dava Aditya Jauhar (05311940000030)

---

## Tabel Soal

* [Konfigurasi A](#konfigurasi-a)
* [Konfigurasi B]

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
