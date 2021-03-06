# Lapres Modul 4 Jarkom 2021 - T02
Laporan Hasil Praktikum Modul 4 Jarkom 2021
Kelompok T02
  * Herwinda Marwaa Salsabila (05311940000009)
  * Dian Arofati N. Z. (05311940000011)
  * Dava Aditya Jauhar (05311940000030)

---

## Kendala

**Tidak terdapat revisi pengerjaan**

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
   
2. Kemudian menggabungkan subnet A yang paling jauh dari router dengan label subnet B. Selanjutnya melakukan labeling subnet C.
   <img src="https://user-images.githubusercontent.com/73151892/145214542-eb9bb64f-cde6-4045-aa79-de7cbc41f5a6.png">
   
3. Kemudian labeling subnet D dan subnet E
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

## Soal C

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

  <img src="https://user-images.githubusercontent.com/57980125/145408084-6b91ab64-78e5-4a3d-ada1-d0c65a7250da.png" width="400">

* Routing pada Router Guanhao sebagai berikut
  
  <img src="https://user-images.githubusercontent.com/57980125/145407879-351c6a9b-2671-4a8c-bb6d-184ccf5aa7fd.png" width="400">

## Soal D

Pada persiapan D, penulis diminta untuk `memberikan ip` pada subnet Blueno, Cipher, Fukurou, dan Elena secara `dinamis` menggunakan bantuan `DHCP server`. Sekaligus melakukan setting DHCP Relay pada router yang menghubungkannya.

1. Penulis perlu melakukan network configuration seperti pada tahap [Soal B](#soal-b)
2. Konfigurasi pada DHCP Server tepatnya di Jipangu sebagai berikut:
   ```
   
     echo 'nameserver 192.168.122.1' > /etc/resolv.conf
     apt-get update
     apt-get install nano
     apt-get install isc-dhcp-server
     dhcpd --version

     ## pemilihan interfaces
     echo 'INTERFACES="eth0"' > /etc/default/isc-dhcp-server
     
   ```
3. Konfigurasikan Forwarders Internet pada DNS Server agar dapat tersambung ke internet, sebagai berikut:

        ```
        echo 'nameserver 192.168.122.1' > /etc/resolv.conf
        apt-get update
        apt-get install nano
        apt-get install isc-dhcp-server
        dhcpd --version

        ## pemilihan interfaces
        echo 'INTERFACES="eth0"' > /etc/default/isc-dhcp-server
        ```

4. Lalu pembagian IP DHCP untuk Client (Blueno, Cipher, Elena, dan Fukurou) di Jipangu sebagai berikut:

    * Deklarasi subnet A1 yang mana tidak harus memiliki settingan DHCP.
  
        ```
        ## Subnet A1 DORIKI dan JIPANGU
        echo '
            subnet 192.212.4.0 netmask 255.255.255.248{}
        ```

    * Pada subnet A2 diberikan pengaturan sesuai dengan NID, netmask, range, broadcast address, dan dns server.  
  
        ```
        ## Subnet A2 BLUENO
        subnet 192.212.8.0  netmask 255.255.255.128 {
            range 192.212.8.2 192.212.8.3;
            option routers 192.212.8.1;
            option broadcast-address 192.212.8.127;
            option domain-name-servers 192.212.4.3;
            default-lease-time 600;
            max-lease-time 7200;
        }' > /etc/dhcp/dhcpd.conf
        ```

    * Pada subnet A3 diberikan pengaturan sesuai dengan NID, netmask, range, broadcast address, dan dns server. 

        ```
        ## Subnet A3 CIPHER
        echo '
            subnet 192.212.0.0  netmask 255.255.252.0 {
            range 192.212.0.2 192.212.0.3;
            option routers 192.212.0.1;
            option broadcast-address 192.212.3.255;
            option domain-name-servers 192.212.4.3;
            default-lease-time 600;
            max-lease-time 7200;
            }' >> /etc/dhcp/dhcpd.conf
        ```

    * Pada subnet A6 diberikan pengaturan sesuai dengan NID, netmask, range, broadcast address, dan dns server. 

        ```
        ## Subnet A6 ELENA
        echo '
            subnet 192.212.34.0  netmask 255.255.254.0 {
            range 192.212.34.2 192.212.34.10;
            option routers 192.212.34.1;
            option broadcast-address 192.212.35.255;
            option domain-name-servers 192.212.4.3;
            default-lease-time 600;
        ```

    * Pada subnet A7 diberikan pengaturan sesuai dengan NID, netmask, range, broadcast address, dan dns server. 

        ```
        ## Subnet A7 FUKUROU
        echo '
            subnet 192.212.32.0  netmask 255.255.255.0 {
            range 192.212.32.2 192.212.32.10;
            option routers 192.212.32.1;
            option broadcast-address 192.212.32.255;
            option domain-name-servers 192.212.4.3;
            default-lease-time 600;
            max-lease-time 7200;
        }' >> /etc/dhcp/dhcpd.conf
        ```

5. Konfigurasikan DHCP Relay pada Router Water7 dan Guanhao seperti berikut:
   
   * Water 7
  
     <img src="https://user-images.githubusercontent.com/57980125/145427903-a5f2aa8c-a44e-47b0-9f27-c651e478eb6b.png" width="500">

   * Guanhao

     <img src="https://user-images.githubusercontent.com/57980125/145428001-c5ec63e3-415a-40ca-8bb4-837339403683.png" width="500">

## Soal 1

Konfigurasi Foosha menggunakan iptables, tetapi Luffy tidak ingin menggunakan MASQUERADE.

**Jawab**

1. List iptables rules menggunakan syntax:

    ```
    iptables -t nat -v -L -n --line-number
    ```

    Di mana,
    
    * ` -t nat` : Nat table yang dipilih
    * `-v` : Verbose output
    * `-L` : Daftar semua aturan dalam chain yang dipilih atau tampilkan semua aturan di tabel nat
    * `-n` : Keluaran numerik (Alamat IP dan nomor port akan dicetak dalam format numerik, bukan nama DNS. Ini akan mempercepat aturan daftar)
    * `--line-number` : Saat membuat daftar rules, tambahkan nomor baris ke awal setiap rules, sesuai dengan posisi rules dalam chain

2. Linux IPtables menghapus aturan rules nat postrouting
3. List iptables rules kembali untuk memastikan bahwa rules tersebut berhasil terhapus
4. Ubah network configuration Foosha, sebagai berikut:
   
    ```
    echo '
    auto eth0
    iface eth0 inet dhcp 
    
    auto eth1
    iface eth1 inet static
        address 192.212.16.1
        netmask 255.255.255.252
        broadcast 192.212.16.3 
    
    auto eth2
    iface eth2 inet static
        address 192.212.36.1
        netmask 255.255.255.252
        broadcast 192.212.36.3

    ' > /etc/network/interfaces
    ```

5. Simpan address `192.168.122` ke dalam variable `ip_eth0_foosha` dengan syntax:

    ```
    ip_eth0_foosha=$(hostname -I | awk 'BEGIN{RS=" "} {print}' | grep '192.168.122')
    ```

6. Kita menggunakan -t nat NAT Table pada -A POSTROUTING POSTROUTING chain untuk -j SNAT dengan source address 192.212.0.0/18

    ```
    iptables -t nat -A POSTROUTING -s 192.212.0.0/18 -o eth0 -j SNAT --to-source $ip_eth0_foosha
    ```

7. List iptables rules kembali untuk memastikan bahwa rules tersebut berhasil tertambahkan

    ```
    iptables -t nat -v -L -n --line-number
    ```

**Dokumentasi Uji Coba**

1. Hasil running jawab.sh pada Foosha
   
   <img src="https://github.com/Herwindams24/Jarkom-Modul-5-T2-2021/blob/main/image/chrome_FCcSEXfEcg.png?raw=true" width="700">
   
   Terlihat bahwa target MASQUERADE berhasil dihapus dan penulis berhasil menambahkan target SNAT dengan source IP 192.212.0.0/18 dan destination IP 192.168.122.71
   
2. Uji coba dilakukan di setiap node client dengan melakukan ping google.com
   
   Chiper
   
   <img src="https://github.com/Herwindams24/Jarkom-Modul-5-T2-2021/blob/main/image/no1_pingGoogle/chrome_YTaItwPpyu.png" width="500">
   
   Blueno
   
   <img src="https://github.com/Herwindams24/Jarkom-Modul-5-T2-2021/blob/main/image/no1_pingGoogle/chrome_mseJwtRllf.png" width="500">
   
   Elena
   
   <img src="https://github.com/Herwindams24/Jarkom-Modul-5-T2-2021/blob/main/image/no1_pingGoogle/chrome_dunrKOQFeu.png" width="500">
   
   Fukurou
   
   <img src="https://github.com/Herwindams24/Jarkom-Modul-5-T2-2021/blob/main/image/no1_pingGoogle/chrome_utw04kuzHd.png" width="500">

## Soal 2

**Soal**

Kalian diminta untuk mendrop semua akses HTTP dari luar Topologi kalian pada server yang merupakan DHCP Server dan DNS Server demi menjaga keamanan.

**Jawab**

Gunakan syntax iptables sebagai berikut:

```
iptables -A FORWARD -d 192.212.4.0/29 -i eth0 -p tcp -m tcp --dport 80 -j DROP
```

Di mana,
* IP pertama -d merupakan IP NID untuk subnet A1 dikarenakan terdapat DHCP Server (Jipangu) dan DNS Server (Doriki)


**Dokumentasi Uji Coba**

* Dokumentasi Syntax
  
    <img src="https://user-images.githubusercontent.com/57980125/145432596-34877541-9704-4edd-a832-d0ca5c6aed14.png" width="500">

* Dokumentasi Uji Coba

Lakukan nmap -p 80 [IP Doriki/IP Jipangu] di Client Elena dan Fukurou

```
nmap -p 80 192.212.4.2
```

   <img src="https://github.com/Herwindams24/Jarkom-Modul-5-T2-2021/blob/main/image/chrome_Kpfakpq9iy.png" width="500">
   
```
nmap -p 80 192.212.4.3
```
   
   <img src="https://github.com/Herwindams24/Jarkom-Modul-5-T2-2021/blob/main/image/chrome_tTYHL6B4G5.png" width="500">


## Soal 3

**Soal**

Batasi DHCP dan DNS Server hanya boleh menerima maksimal 3 koneksi ICMP secara bersamaan menggunakan iptables, selebihnya didrop.

**Jawab**

Gunakan syntax iptables sebagai berikut pada Jipangu maupun Doriki:

```
iptables -A INPUT -p icmp -m connlimit --connlimit-above 3 --connlimit-mask 0 -sk 0 -j DROP
```

Di mana,

*  `-A INPUT` INPUT chain untuk menyaring paket 
*  Protokol ICMP`-p icmp` merupakan protokol yang membatasi paket yang masuk 
*  `-m connlimit --connlimit-above 3` berarti hanya ada maksimal 3 koneksi saja 
*  `--connlimit-mask 0` berarti dapat bebas berasal darimana saja
*  `-j DROP` selebihnya akan di DROP


**Dokumentasi Uji Coba**

* Dokumentasi Syntax
  
    <img src="https://user-images.githubusercontent.com/57980125/145432522-d1eceda3-9643-4078-8af4-123ffe38d41d.png" width="500">

* Dokumentasi Uji Coba

Lakukan ping ke IP milik Doriki/Jipangu pada 4 node yang berbeda. Di mana nantinya, hanya akan ada 3 node (node kesatu - ketiga) yang dapat melakukan ping, sisanya yaitu node ke-4 tidak akan bisa melakukan ping.

```
ping 192.212.4.2
ping 192.212.4.3
```
Ping ke Jipangu
- Ping ke-1 (Berhasil)
 
 <img src="https://github.com/Herwindams24/Jarkom-Modul-5-T2-2021/blob/main/image/chrome_gnzTZ7aqAv.png" width="500">
 
- Ping ke-2 (Berhasil)

 <img src="https://github.com/Herwindams24/Jarkom-Modul-5-T2-2021/blob/main/image/chrome_FQaqTnCKQ5.png" width="500">
 
- Ping ke-3 (Berhasil) 
 <img src="https://github.com/Herwindams24/Jarkom-Modul-5-T2-2021/blob/main/image/chrome_Ba8p5Vsx4c.png" width="500">
 
- Ping ke-4 (Gagal)

 <img src="https://github.com/Herwindams24/Jarkom-Modul-5-T2-2021/blob/main/image/chrome_TwpC1Z4II4.png" width="500">


Ping ke Doriki

- Ping ke-1 (Berhasil) 

 <img src="https://github.com/Herwindams24/Jarkom-Modul-5-T2-2021/blob/main/image/chrome_GTteCUegDc.png" width="500">
 
- Ping ke-2 (Berhasil)
 
 <img src="https://github.com/Herwindams24/Jarkom-Modul-5-T2-2021/blob/main/image/chrome_9DI6ubxpwE.png" width="500">
 
- Ping ke-3 (Berhasil)
 
 <img src="https://github.com/Herwindams24/Jarkom-Modul-5-T2-2021/blob/main/image/chrome_VWnzqcHBX5.png" width="500">
 
- Ping ke-4 (Gagal)
 
 <img src="https://github.com/Herwindams24/Jarkom-Modul-5-T2-2021/blob/main/image/chrome_i6I88hKO8e.png" width="500">
 
## Soal 4

**Soal**

Akses dari subnet Blueno dan Cipher hanya diperbolehkan pada pukul 07.00 - 15.00 pada hari Senin sampai Kamis.

**Jawab**

Pada Doriki jalankan syntax di bawah ini:

<img src="https://github.com/Herwindams24/Jarkom-Modul-5-T2-2021/blob/main/image/chrome_LfWWKqN0NM.png?raw=true" width="500">

```
### Blueno
# Blueno batas hari tidak aktif
iptables -A INPUT -s 192.212.8.0/25 -m time --weekdays Fri,Sat,Sun -j REJECT
# Blueno batas jamnya
iptables -A INPUT -s 192.212.8.0/25 -m time --timestart 00:00 --timestop 06:59 --weekdays Mon,Tue,Wed,Thu -j REJECT
iptables -A INPUT -s 192.212.8.0/25 -m time --timestart 15:01 --timestop 23:59 --weekdays Mon,Tue,Wed,Thu -j REJECT

### Cipher
# Cipher batas hari tidak aktif
iptables -A INPUT -s 192.212.0.0/22 -m time --weekdays Fri,Sat,Sun -j REJECT
# Cipher batas jamnya
iptables -A INPUT -s 192.212.0.0/22 -m time --timestart 00:00 --timestop 06:59 --weekdays Mon,Tue,Wed,Thu -j REJECT
iptables -A INPUT -s 192.212.0.0/22 -m time --timestart 15:01 --timestop 23:59 --weekdays Mon,Tue,Wed,Thu -j REJECT
```

Di mana,

* -A INPUT : Saring paket yang masuk dari -s 192.212.8.0/25 subnet BLUENO dan -s 192.212.0.0/22 subnet CHIPER 
* -m time --weekdays Fri,Sat,Sun : Pada pukul berapapun untuk hari Jumat, Sabtu dan Minggu 
* -j REJECT : Tolak permintaan akses

**Dokumentasi Uji Coba**

1. Pada Cipher lakukan ping ke IP Doriki 
   
   <img src="https://github.com/Herwindams24/Jarkom-Modul-5-T2-2021/blob/main/image/chrome_t3lvqkRvIs.png" width="500">

2. Pada Blueno lakukan ping ke IP Doriki

   <img src="https://github.com/Herwindams24/Jarkom-Modul-5-T2-2021/blob/main/image/chrome_Rcx696E3rc.png" width="500">

3. Gunakan command di bawah ini jika ingin mengatur waktu linux

   ```date --set="2021-12-04 20:00:00.00"```

## Soal 5

**Soal**

Akses dari subnet Elena dan Fukuro hanya diperbolehkan pada pukul 15.01 hingga pukul 06.59 setiap harinya. Selain itu direject.

**Jawab**

Pada Doriki jalankan syntax di bawah ini:

<img src='https://github.com/Herwindams24/Jarkom-Modul-5-T2-2021/blob/main/image/chrome_1K9dOz9sWQ.png?raw=true' width='500'>

```
###=================== Nomer 5 Batas Akses Elena dan Fukurou ================###
# Elena batas waktu
iptables -A INPUT -s 192.212.34.0/23 -m time --timestart 06:59 --timestop 15:01 -j REJECT
# Fukurou batas waktu
iptables -A INPUT -s 192.212.32.0/24 -m time --timestart 06:59 --timestop 15:01 -j REJECT
###=================== Nomer 5 Batas Akses Elena dan Fukurou ================###
```

Dikarenakan pada nomor 5 diminta untuk bisa diakses setiap, maka tidak perlu membuat batasan hari karena bisa diakses setiap hari.

**Dokumentasi Uji Coba**

1. Pada Elena lakukan ping ke IP Doriki
   
   <img src="https://github.com/Herwindams24/Jarkom-Modul-5-T2-2021/blob/main/image/chrome_bmIQEtGIRs.png" width="500">

2. Pada Fukurou

   <img src="https://github.com/Herwindams24/Jarkom-Modul-5-T2-2021/blob/main/image/chrome_auNVngI33B.png" width="500">

3. Gunakan command di bawah ini jika ingin mengatur waktu linux

   ```Date --set="2021-12-04 14:00:00.00```


## Soal 6

**Soal**

Karena kita memiliki 2 Web Server, Luffy ingin Guanhao disetting sehingga setiap request dari client yang mengakses DNS Server akan didistribusikan secara bergantian pada Jorge dan Maingate

**Jawab**

Pada nomor 6 ini, penulis menggunakan konsep load balancing. Di mana load balancing ini berfungsi untuk mendistribusikan pada webserver, sehingga beban yang dipikul oleh server tidak terlalu berat dan hasilnya lebih cepat.

1. Pada Guanhao lakukan Redirect Request dengan syntax berikut ini:

```
###====================== Nomor 6 Request diredirect ========================###

iptables -A PREROUTING -t nat -d 192.212.4.3 -p tcp --dport 80 -m statistic --mode nth --every 2 --packet 0 -j DNAT --to-destination 192.212.33.3:80
iptables -A PREROUTING -t nat -d 192.212.4.3 -p tcp --dport 80 -j DNAT --to-destination 192.212.33.2:80
iptables -t nat -A POSTROUTING -p tcp -d 192.212.33.3 --dport 80 -j SNAT --to-source 192.212.4.3:80
iptables -t nat -A POSTROUTING -p tcp -d 192.212.33.2 --dport 80 -j SNAT --to-source 192.212.4.3:80

###====================== Nomor 6 Request diredirect ========================###
```

<img src="https://github.com/Herwindams24/Jarkom-Modul-5-T2-2021/blob/main/image/chrome_HLl5tyxNHs.png?raw=true" width="500">

Di mana baris pertama dan kedua mengatur Prerouting, sedangkan ketiga dan keempat mengatur postrouting, dengan rincian:

IP Doriki : 192.212.4.3

IP Jorge : 192.212.33.2

IP MainGate : 192.212.33.3

2. Lalu dikarenakan Maingate dan Jorge merupakan webserver, maka install apache  dan netcat, lalu start apache.
   
```
echo nameserver 192.168.122.1 > /etc/resolv.conf
apt-get update
apt-get install netcat -y
apt-get install apache2 -y
service apache2 start
```

**Dokumentasi Uji Coba**

1. Jalankan script.sh di Fukurou atau Elena
2. Pada node webserver (Maingate atau Jorge) jalankan netcat dengan mode listen ke port 80 dengan syntax berikut ini:

```
nc -l -p 80
```

3. Pada Elena atau Fukurou kita kirimkan paket ke Doriki lewat port 80 dengan command di bawah ini:

```
nc 192.212.4.3 80
```

Di mana 192.212.4.2 merupakan IP dari Jipangu (DHCP Server) dan 192.212.4.3 yang merupakan IP dari Doriki (DNS Server)

4. Kemudian coba testing kirim pesan beberapa kata pada Client

<img src="https://user-images.githubusercontent.com/57520495/145680934-76f3abab-5413-4d1d-b599-c607e300d5fd.png" width="500">

<img src="https://user-images.githubusercontent.com/57980125/145664119-7e6bc234-5b6c-45ed-9eb4-836a72876b93.png" width="500">

5. Cek pada Maingate atau Jorge untuk lihat hasil load balancingnya

<img src="https://user-images.githubusercontent.com/57980125/145663924-8a076f7a-4629-4334-acb2-fd931ab3f419.png" width="500">

<img src="https://user-images.githubusercontent.com/57980125/145663913-e85eae42-79b6-415e-b4fc-929f258405ba.png" width="500">
