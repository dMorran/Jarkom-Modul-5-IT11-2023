# Jarkom-Modul-5-IT11-2023

#### Anggota Kelompok A11:

| Nama                   | NRP        |
| ---------------------- | ---------- |
| Midyanisa Yuniar       | 5027211025 |
| Dyas Amorita Radhwa N  | 5027211009 |

> Prefiks IP kelompok A11 -> 10.69

# Daftar Isi
* [Topologi](#Topologi)
* [CPT VLSM](#CPT-VLSM)
* 

# (A.) Topologi
Berikut adalah topologi dari soal yang akan kami buat berdasarkan soal
![topo](https://github.com/dMorran/Jarkom-Modul-5-IT11-2023/assets/107184933/f5fd1f30-920c-4d39-a26d-c528bfecb31e)

# (B.) VLSM Subnetting dan Pembagian IP
Untuk membuat VLSM, pertama-tama, kita perlu membuat tabel yang berisi jumlah IP pada setiap subnet

![subnet](https://github.com/dMorran/Jarkom-Modul-5-IT11-2023/assets/107184933/e08e4e83-6c8e-4059-9ac4-592cc80877aa)

## VSLM Tree
Berikut ini merupakan Tree dari VSLM

## Pembagian IP
Berdasarkan Perhitungan IP maka didapatkan pembagian IP sebagai berikut

![pembagian_ip](https://github.com/dMorran/Jarkom-Modul-5-IT11-2023/assets/107184933/ebb8b229-cf12-4c9e-a131-0b3d55b0103d)

## Konfigurasi pada VLSM

* Aura

  ```
  # config for eth0
  #auto eth0
  #iface eth0 inet dhcp
  auto eth0
  iface eth0 inet static
      address 192.168.122.2
      netmask 255.255.255.252
      gateway 192.168.122.1
      up echo nameserver 192.168.122.1 > /etc/resolv.conf
  
  # config for eth1
  auto eth1
  iface eth1 inet static
      address 10.69.14.133
      netmask 255.255.255.252
  
  # config for eth2
  auto eth2
  iface eth2 inet static
      address 10.69.14.129
      netmask 255.255.255.252

  ```
  
* Frieren

  ```
  # config for eth0
  auto eth0
  iface eth0 inet static
      address 10.69.14.134
      netmask 255.255.255.252
      gateway 10.69.14.133
      
  # config for eth1
  auto eth1
  iface eth1 inet static
      address 10.69.14.137
      netmask 255.255.255.252
  
  # config for eth2
  auto eth2
  iface eth2 inet static
      address 10.69.14.141
      netmask 255.255.255.252
  ```

  
* Fern

  ```
  # config for eth0
  auto eth0
  iface eth0 inet static
      address 10.69.14.3
      netmask 255.255.255.128
      gateway 10.69.14.1
  
  # config for eth1
  auto eth1
  iface eth1 inet static
      address 10.69.14.145
      netmask 255.255.255.252
  
  # config for eth2
  auto eth2
  iface eth2 inet static
      address 10.69.14.149
      netmask 255.255.255.252
  ```
  
* Himmel

  ```
  # config for eth0
  auto eth0
  iface eth0 inet static
      address 10.69.14.142
      netmask 255.255.255.252
      gateway 10.69.14.141
  
  # config for eth1
  auto eth1
  iface eth1 inet static
      address 10.69.12.1
      netmask 255.255.254.0
  
  # config for eth2
  auto eth2
  iface eth2 inet static
      address 10.69.14.1
      netmask 255.255.255.128
  ```
  
* Heiter

  ```
  # config for eth0
  auto eth0
  iface eth0 inet static
      address 10.69.14.130
      netmask 255.255.255.252
      gateway 10.69.14.129
  
  # config for eth1
  auto eth1
  iface eth1 inet static
      address 10.69.0.1
      netmask 255.255.248.0
  
  # config for eth2
  auto eth2
  iface eth2 inet static
      address 10.69.8.1
      netmask 255.255.252.0
  ```
  
* GrobeForest

  ```
  # config for eth0
  auto eth0
  iface eth0 inet static
      address 10.69.8.3
      netmask 255.255.252.0
      gateway 10.69.8.1
  
  auto eth0
  iface eth0 inet dhcp
      gateway 10.69.8.1
  ```
  
* Sein

  ```
  # config for eth0
  auto eth0
  iface eth0 inet static
      address 10.69.8.2
      netmask 255.255.252.0
      gateway 10.69.8.1
      up echo nameserver 192.168.122.1 > /etc/resolv.conf
  ```
 
* Ricther (DNS Server)

  ```
  # config for eth0
  auto eth0
  iface eth0 inet static
      address 10.69.14.146
      netmask 255.255.255.252
      gateway 10.69.14.145
  ```
  
* Revolte (DHCP Server)

  ```
  # config for eth0
  auto eth0
  iface eth0 inet static
      address 10.69.14.150
      netmask 255.255.255.252
      gateway 10.69.14.149
  ```

* LaubHills

  ```
  # config for eth0
  auto eth0
  iface eth0 inet static
      address 10.69.12.2
      netmask 255.255.254.0
      gateway 10.69.12.1
  
  auto eth0
  iface eth0 inet dhcp
      gateway 10.69.12.1
  ```
   
* SchwerMountains

  ```
  # config for eth0
  auto eth0
  iface eth0 inet static
      address 10.69.14.2
      netmask 255.255.255.128
      gateway 10.69.14.1
  
  auto eth0
  iface eth0 inet dhcp
      gateway 10.69.14.1
  ```

  * Stark

  ```
    # config for eth0
  auto eth0
  iface eth0 inet static
      address 10.69.14.138
      netmask 255.255.255.252
      gateway 10.69.14.137
      up echo nameserver 192.168.122.1 > /etc/resolv.conf
  ```

  * Turk-Region

  ```
  # config for eth0
  auto eth0
  iface eth0 inet static
      address 10.69.0.2
      netmask 255.255.248.0
      gateway 10.69.0.1
  
  auto eth0
  iface eth0 inet dhcp
      gateway 10.69.0.1
  ```

# (C.) Routing

#### Aura
```
# A2 Heiter eth0
route add -net 10.69.0.0 netmask 255.255.248.0 gw 10.69.14.130
# A1 Heiter eth0
route add -net 10.69.8.0 netmask 255.255.252.0 gw 10.69.14.130
# A5 Frieren eth0
route add -net 10.69.14.136 netmask 255.255.255.252 gw 10.69.14.134
# A7 Frieren eth0
route add -net 10.69.12.0 netmask 255.255.254.0 gw 10.69.14.134
# A8 Frieren eth0
route add -net 10.69.14.0 netmask 255.255.255.128 gw 10.69.14.134
# A9 Frieren eth0
route add -net 10.69.14.144 netmask 255.255.255.252 gw 10.69.14.134
# A10 Frieren eth0
route add -net 10.69.14.148 netmask 255.255.255.252 gw 10.69.14.134
```

#### Heiter
```
# Heiter Aura eth2
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.69.14.129
```

#### Frieren
```
# Frieren Aura eth1
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.69.14.133
# A7 Himmel eth0
route add -net 10.69.12.0 netmask 255.255.254.0 gw 10.69.14.142
# A8 Himmel eth0
route add -net 10.69.14.0 netmask 255.255.255.128 gw 10.69.14.142
# A9 Himmel eth0
route add -net 10.69.14.144 netmask 255.255.255.252 gw 10.69.14.142
# A10 Himmel eth0
route add -net 10.69.14.148 netmask 255.255.255.252 gw 10.69.14.142
# A2 Aura eth1
route add -net 10.69.0.0 netmask 255.255.248.0 gw 10.69.14.133
# A1 Aura eth1
route add -net 10.69.8.0 netmask 255.255.248.0 gw 10.69.14.133
```

#### Himmel
```
# Himmel Frieren eth2
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.69.14.141
# A9 Fern eth0
route add -net 10.69.14.144 netmask 255.255.255.252 gw 10.69.14.3
# A10 Fern eth0
route add -net 10.69.14.148 netmask 255.255.255.252 gw 10.69.14.3
```

#### Fern
```
# Fern Himmel eth2
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.69.14.1
```

### Konfigurasi DNS

Pada `Richter` install depedensi
```
apt update
apt install bind9 dnsutils -y
```

Masukkan kode berikut pada `/etc/bind/named.conf.options` kemudian jalankan `service bind9 restart` dan `service bind9 status`

```
options {
    listen-on-v6 { none; };
    directory "/var/cache/bind";

    # Forwarders
    forwarders {
        192.168.122.1;
    };

    # If there is no answer from the forwarders, dont attempt to resolve recursively
    forward only;

    dnssec-validation no;

    auth-nxdomain no;    # conform to RFC1035
    allow-query { any; };
};
```

# (D.) Tugas berikutnya adalah memberikan ip pada subnet SchwerMountain, LaubHills, TurkRegion, dan GrobeForest menggunakan bantuan DHCP.

### DHCP-Server
pada `Revolte`:
1. Install DHCP Server dengan command `apt-get update` dan `apt install isc-dhcp-server rsyslog -y`.
2. Edit file `/etc/default/isc-dhcp-server` dengan menambahkan kode `eth0` pada `INTERFACESv4` seperti kode berikut:
   ```
   # Defaults for isc-dhcp-server (sourced by /etc/init.d/isc-dhcp-server)
    # Path to dhcpd's config file (default: /etc/dhcp/dhcpd.conf).
    #DHCPDv4_CONF=/etc/dhcp/dhcpd.conf
    #DHCPDv6_CONF=/etc/dhcp/dhcpd6.conf
    # Path to dhcpd's PID file (default: /var/run/dhcpd.pid).
    #DHCPDv4_PID=/var/run/dhcpd.pid
    #DHCPDv6_PID=/var/run/dhcpd6.pid
    # Additional options to start dhcpd with.
    #       Don't use options -cf or -pf here; use DHCPD_CONF/ DHCPD_PID instead
    #OPTIONS=\"\"
    # On what interfaces should the DHCP server (dhcpd) serve DHCP requests?
    #       Separate multiple interfaces with spaces, e.g. \"eth0 eth1\".
    INTERFACESv4=\"eth0\"
    INTERFACESv6=\"\"
   ``` 
4. Edit file `/etc/dhcp/dhcpd.conf` dengan menambahkan kode berikut:
   ```
   # Subnet A1 Grobe Forest
    subnet 10.69.8.0 netmask 255.255.252.0 {
        range 10.69.8.3 10.69.11.254;
        option routers 10.69.8.1;
        option broadcast-address 10.69.11.255;
        option domain-name-servers 10.69.14.146;
        default-lease-time 720;
        max-lease-time 5760;
    }
    
    # Subnet A2 Turk Region
    subnet 10.69.0.0 netmask 255.255.248.0 {
        range 10.69.0.1 10.69.7.254;
        option routers 10.69.0.1;
        option broadcast-address 10.69.7.255;
        option domain-name-servers 10.69.14.146;
        default-lease-time 720;
        max-lease-time 5760;
    }
    
    # Subnet A3
    subnet 10.69.14.128 netmask 255.255.255.252 {
    }
    
    # Subnet A4
    subnet 10.69.14.132 netmask 255.255.255.252 {
    }
    
    # Subnet A5
    subnet 10.69.14.136 netmask 255.255.255.252 {
    }
    
    # Subnet A6
    subnet 10.69.14.140 netmask 255.255.255.252 {
    }
    
    # Subnet A7 Laub Hills
    subnet 10.69.12.0 netmask 255.255.254.0 {
        range 10.69.12.2 10.69.13.254;
        option routers 10.69.12.1;
        option broadcast-address 10.69.13.255;
        option domain-name-servers 10.69.14.146;
        default-lease-time 720;
        max-lease-time 5760;
    }
    
    # Subnet A8 Schwer Mountains
    subnet 10.69.14.0 netmask 255.255.255.128 {
        range 10.69.14.2 10.69.14.126;
        option routers 10.69.14.1;
        option broadcast-address 10.69.14.127;
        option domain-name-servers 10.69.14.146;
        default-lease-time 720;
        max-lease-time 5760;
    }
    
    # Subnet A9
    subnet 10.69.14.144 netmask 255.255.255.252 {
    }
    
    # Subnet A10
    subnet 10.69.14.148 netmask 255.255.255.252 {
    }
   ```
6. Jalankan atau restart DHCP server dengan perintah `service isc-dhcp-server restart` dan `service rsyslog start`

### DHCP-Relay

1. Install `apt-get install isc-dhcp-relay -y` pada Aura, Heiter, Himmel, Fern dan Frieren, `apt-get install isc-dhcp-server` pada Revolte
2. Pada Router (Aura, Heiter, Himmel, Fern dan Frieren) jalankan command berikut
    ```
    #!/bin/bash

    apt update
    apt-get install isc-dhcp-relay rsyslog -y

    echo "# Defaults for isc-dhcp-relay initscript
    # sourced by /etc/init.d/isc-dhcp-relay
    # installed at /etc/default/isc-dhcp-relay by the maintainer scripts
    # What servers should the DHCP relay forward requests to?
    SERVERS=\"10.69.14.150\"

    # On what interfaces should the DHCP relay (dhrelay) serve DHCP requests?
    INTERFACES=\"eth0 eth1 eth2\"

    # Additional options that are passed to the DHCP relay daemon?
    OPTIONS=\"\"" >/etc/default/isc-dhcp-relay

    service rsyslog start

    service isc-dhcp-relay restart
    service isc-dhcp-relay status
    ```

# Soal 1

Agar topologi yang kalian buat dapat mengakses keluar, kalian diminta untuk mengkonfigurasi Aura menggunakan iptables, tetapi tidak ingin menggunakan MASQUERADE

### Aura

  ```
  iptables -t nat -A POSTROUTING -o eth0 -j SNAT -s 10.69.14.128/30 --to-source 192.168.122.2
  iptables -t nat -A POSTROUTING -o eth0 -j SNAT -s 10.69.14.132/30 --to-source 192.168.122.2
  ```

### Heiter

  ```
  iptables -t nat -A POSTROUTING -o eth0 -j SNAT -s 10.69.0.0/21 --to-source 10.69.14.130
  iptables -t nat -A POSTROUTING -o eth0 -j SNAT -s 10.69.8.0/22 --to-source 10.69.14.130
  ```

### Frieren

  ```
  iptables -t nat -A POSTROUTING -o eth0 -j SNAT -s 10.69.14.140/30 --to-source 10.69.14.134
  iptables -t nat -A POSTROUTING -o eth0 -j SNAT -s 10.69.14.136/30 --to-source 10.69.14.134
  ```

### Himmel

  ```
  iptables -t nat -A POSTROUTING -o eth0 -j SNAT -s 10.69.14.0/25 --to-source 10.69.14.142
  iptables -t nat -A POSTROUTING -o eth0 -j SNAT -s 10.69.12.0/23 --to-source 10.69.14.142
  ```

### Fern

  ```
  iptables -t nat -A POSTROUTING -o eth0 -j SNAT -s 10.69.14.144/30 --to-source 10.69.14.3
  iptables -t nat -A POSTROUTING -o eth0 -j SNAT -s 10.69.14.148/30 --to-source 10.69.14.3
  ```

Untuk mengecek apakah sudah bisa akses keluar, dilakukan testing pada `Fern` dnegan melakukan ping pada google.com berikut ini merupakan hasil testing yang sudah dilakukan

![ping_fern](https://github.com/dMorran/Jarkom-Modul-5-IT11-2023/assets/107184933/528de99f-af5a-42b2-a4d6-595933344c61)


# Soal 2

Kalian diminta untuk melakukan drop semua TCP dan UDP kecuali port 8080 pada TCP.

```
#!/bin/bash

iptables -F
iptables -A INPUT -p icmp -j ACCEPT
iptables -A INPUT -p tcp --dport 8080 -j ACCEPT
iptables -A INPUT -p tcp -j DROP
iptables -A INPUT -p udp -j DROP
```
Untuk melakukan testing, kode tersebut dijalankan di salah satu client, contohnya Laub-hills

![image](https://github.com/dMorran/Jarkom-Modul-5-IT11-2023/assets/107184933/cec6552a-df93-4f9a-a7bf-249bfc7913d0)

Kemudian untuk mengetesnya cukup menjalankan command `nmap -p 80 10.69.12.2` pada Schwer-Mountain. Hasilnya adalah koneksi filtered untuk port 80,

![image](https://github.com/dMorran/Jarkom-Modul-5-IT11-2023/assets/107184933/5233c61c-4400-4ed1-b872-df101eb2b9ed)

sedangkan apabila menggunakan command `nmap -p 8080 10.69.12.2` hasilnya koneksi closed (terhubung namun tidak ada layanan yang aktif)

![image](https://github.com/dMorran/Jarkom-Modul-5-IT11-2023/assets/107184933/f571c29e-7b32-44c8-81d8-3d30d49195a0)


# Soal 3

Kepala Suku North Area meminta kalian untuk membatasi DHCP dan DNS Server hanya dapat dilakukan ping oleh maksimal 3 device secara bersamaan, selebihnya akan di drop.

```
#!/bin/bash

# DHCP (Revolte) dan DNS Server (Richter)

iptables -A INPUT -m state --state ESTABLISHED,RELATED -j ACCEPT

iptables -A INPUT -p icmp -m connlimit --connlimit-above 3 --connlimit-mask 0 -j DROP
```
masukkan kode tersebut pada DHCP dan DNS Server

![image](https://github.com/dMorran/Jarkom-Modul-5-IT11-2023/assets/107184933/e796ab3f-0a75-4617-bf37-b98e8c00e8ae)

Untuk melakukan testing maka dilakukan ping dari keempat client lain ke Revolte `ping 10.69.14.146`

![image](https://github.com/dMorran/Jarkom-Modul-5-IT11-2023/assets/107184933/b250c74d-30b6-4511-bc2d-f5fd031a26f3)


# Soal 4

Lakukan pembatasan sehingga koneksi SSH pada Web Server hanya dapat dilakukan oleh masyarakat yang berada pada GrobeForest.

jalankan command berikut pada sein dan stark
```
#!/bin/bash

# Web Server (Stark & Sein) -> no 4
iptables -A INPUT -p tcp --dport 22 -s 10.69.8.0/22 -j ACCEPT
```
untuk testing jalankan command

Buka koneksi port SSH dari sisi Sein terlebih dahulu dengan command

```
nc -l -p 22
```

telnet `telnet 10.69.8.2 22` pada Grobe-forest maka akan tampak bahwa grobe-forest sudah terhubung dengan Sein

![image](https://github.com/dMorran/Jarkom-Modul-5-IT11-2023/assets/107184933/d156033f-0824-4fee-bf49-702843ac76f8)

Sedangkan apabila menjalankannya pada Turk-Region, maka akan dapat pesan eror

![image](https://github.com/dMorran/Jarkom-Modul-5-IT11-2023/assets/107184933/26287beb-e8ee-4a06-b132-3b4bf1a32c5a)

testing juga bisa dilakukan dengan nmap

![image](https://github.com/dMorran/Jarkom-Modul-5-IT11-2023/assets/107184933/55646c48-f406-4919-803b-40bee9d8eb63)

# Soal 5

Selain itu, akses menuju WebServer hanya diperbolehkan saat jam kerja yaitu Senin-Jumat pada pukul 08.00-16.00.

```
iptables -A INPUT -p tcp --dport 22 -s 10.69.8.0/22 -m time --timestart 08:00 --timestop 16:00 --weekdays Mon,Tue,Wed,Thu,Fri -j ACCEPT
```
Untuk testing jalankan command ping ke web server, disini digunakan Sein jalankan `ping  10.69.8.2`. 

Testing pada Hari Rabu Pukul 10:00 

![image](https://github.com/dMorran/Jarkom-Modul-5-IT11-2023/assets/107184933/dcb4f041-c86d-43a9-bed7-abdfe2a2203f)

Kemudian untuk testing pada Hari ini pukul 18:00 dapat dilakukan dengan menjalankan sebuah command berikut terlebih dahulu ``date -s "20 DEC 2023 20:00:00"`` 

Hasilnya adalah tidak dapat melakukan ping karena diluat jam kerja

![image](https://github.com/dMorran/Jarkom-Modul-5-IT11-2023/assets/107184933/c547a2ea-fef9-42b2-a4fe-96da1a7bc42b)

Untuk testing diluar hari kerja maka set harinya menjadi hari sabtu ``date -s "23 DEC 2023 20:00:00"``. Maka sama seperti sebelumnya Web server tidak akan dapat diakses

![image](https://github.com/dMorran/Jarkom-Modul-5-IT11-2023/assets/107184933/b4f2e5ed-1f80-418b-9194-6633cc2cce49)

# Soal 6

Lalu, karena ternyata terdapat beberapa waktu di mana network administrator dari WebServer tidak bisa stand by, sehingga perlu ditambahkan rule bahwa akses pada hari Senin - Kamis pada jam 12.00 - 13.00 dilarang (istirahat maksi cuy) dan akses di hari Jumat pada jam 11.00 - 13.00 juga dilarang (maklum, Jumatan rek).

```
iptables -A INPUT -p tcp --dport 22 -s 10.69.8.0/22 -m time --timestart 12:00 --timestop 13:00 --weekdays Mon,Tue,Wed,Thu -j DROP
iptables -A INPUT -p tcp --dport 22 -s 10.69.8.0/22 -m time --timestart 11:00 --timestop 13:00 --weekdays Fri -j DROP

iptables -A INPUT -p tcp --dport 22 -j
```
Langkah testing sama seperti no 5 jalankan command ``date -s "20 DEC 2023 12:30:00"`` maka tidak akan bisa melakukan ping

![image](https://github.com/dMorran/Jarkom-Modul-5-IT11-2023/assets/107184933/6dd88128-f611-4534-bcf2-4cdfde9fc24d)

ping pada Rabu pukul 10:00 

![image](https://github.com/dMorran/Jarkom-Modul-5-IT11-2023/assets/107184933/41b0e392-1794-4b0b-847b-352232931472)

ping pada Jumat pukul 12:00, hasilnya tidak dapat melakukan ping karena diluar jam kerja

![image](https://github.com/dMorran/Jarkom-Modul-5-IT11-2023/assets/107184933/f93823e2-fbdb-4136-b8f1-093230372b6d)

ping pada Jumat pukul 09:00 dapat dilakukan karena masih jam kerja

![image](https://github.com/dMorran/Jarkom-Modul-5-IT11-2023/assets/107184933/1183266c-5542-4f5e-8f6c-ae66de015d21)


# Soal 7

Karena terdapat 2 WebServer, kalian diminta agar setiap client yang mengakses Sein dengan Port 80 akan didistribusikan secara bergantian pada Sein dan Stark secara berurutan dan request dari client yang mengakses Stark dengan port 443 akan didistribusikan secara bergantian pada Sein dan Stark secara berurutan.

```
#!/bin/bash

# heiter & frieren

iptables -A PREROUTING -t nat -p tcp --dport 80 -d 10.69.8.2 -m statistic --mode nth --every 2 --packet 0 -j DNAT --to-destination 10.69.8.2

iptables -A PREROUTING -t nat -p tcp --dport 80 -d 10.69.8.2 -j DNAT --to-destination 10.69.14.138

iptables -A PREROUTING -t nat -p tcp --dport 443 -d 10.69.14.138 -m statistic --mode nth --every 2 --packet 0 -j DNAT --to-destination 10.69.14.138

iptables -A PREROUTING -t nat -p tcp --dport 443 -d 10.69.14.138 -j DNAT --to-destination 10.69.8.2
```

hasil testing

![image](https://github.com/dMorran/Jarkom-Modul-5-IT11-2023/assets/107184933/58f0768e-7199-4212-9e23-dd5b54bafa34)


# Soal 8

Karena berbeda koalisi politik, maka subnet dengan masyarakat yang berada pada Revolte dilarang keras mengakses WebServer hingga masa pencoblosan pemilu kepala suku 2024 berakhir. Masa pemilu (hingga pemungutan dan penghitungan suara selesai) kepala suku bersamaan dengan masa pemilu Presiden dan Wakil Presiden Indonesia 2024.

```
#!/bin/bash

# revolte

revolte="10.69.14.148/30"

pemilu_start=$(date -d "2023-10-19T00:00" +"%Y-%m-%dT%H:%M")

pemilu_end=$(date -d "2024-02-15T00:00" +"%Y-%m-%dT%H:%M")

iptables -A INPUT -p tcp -s $revolte --dport 80 -m time --datestart "$pemilu_start" --datestop "$pemilu_end" -j DROP
```

Hasil config

![image](https://github.com/dMorran/Jarkom-Modul-5-IT11-2023/assets/107184933/7e915b41-5578-4b79-ab2e-fd2671eba037)


# Soal 9

Sadar akan adanya potensial saling serang antar kubu politik, maka WebServer harus dapat secara otomatis memblokir  alamat IP yang melakukan scanning port dalam jumlah banyak (maksimal 20 scan port) di dalam selang waktu 10 menit.

```
iptables -N scan_port

iptables -A INPUT -m recent --name scan_port --update --seconds 600 --hitcount 20 -j DROP

iptables -A FORWARD -m recent --name scan_port --update --seconds 600 --hitcount 20 -j DROP

iptables -A INPUT -m recent --name scan_port --set -j ACCEPT

iptables -A FORWARD -m recent --name scan_port --set -j ACCEPT
```

Check

```
for i in {1..25}; do
  echo $i
  nmap -p 80 -T2 -sS 10.69.8.2
  sleep 3
done
```

Hasil testing

![image](https://github.com/dMorran/Jarkom-Modul-5-IT11-2023/assets/107184933/a477e753-b3c3-4e91-9497-d14800bc9620)

Hanya 20 paket yang diterima, dan sisanya akan ditolak

# Soal 10

Karena kepala suku ingin tau paket apa saja yang di-drop, maka di setiap node server dan router ditambahkan logging paket yang di-drop dengan standard syslog level

```
#!/bin/bash

# semua node

iptables -A INPUT -j LOG --log-level debug --log-prefix 'Dropped Packet' -m limit --limit 1/second --limit-burst 10
```
## Problem
- Pada Nomor 10 syslog pada `/var/log/syslog` tidak mau update
