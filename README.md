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

# Soal 3

Kepala Suku North Area meminta kalian untuk membatasi DHCP dan DNS Server hanya dapat dilakukan ping oleh maksimal 3 device secara bersamaan, selebihnya akan di drop.

```
#!/bin/bash

# DHCP (Revolte) dan DNS Server (Richter)

iptables -A INPUT -m state --state ESTABLISHED,RELATED -j ACCEPT

iptables -A INPUT -p icmp -m connlimit --connlimit-above 3 --connlimit-mask 0 -j DROP
```

# Soal 4

Lakukan pembatasan sehingga koneksi SSH pada Web Server hanya dapat dilakukan oleh masyarakat yang berada pada GrobeForest.

```
#!/bin/bash

# Web Server (Stark & Sein) -> no 4
iptables -A INPUT -p tcp --dport 22 -s 10.69.8.0/22 -j ACCEPT
```

# Soal 5

Selain itu, akses menuju WebServer hanya diperbolehkan saat jam kerja yaitu Senin-Jumat pada pukul 08.00-16.00.

```
iptables -A INPUT -p tcp --dport 22 -s 10.69.8.0/22 -m time --timestart 08:00 --timestop 16:00 --weekdays Mon,Tue,Wed,Thu,Fri -j ACCEPT
```

# Soal 6

Lalu, karena ternyata terdapat beberapa waktu di mana network administrator dari WebServer tidak bisa stand by, sehingga perlu ditambahkan rule bahwa akses pada hari Senin - Kamis pada jam 12.00 - 13.00 dilarang (istirahat maksi cuy) dan akses di hari Jumat pada jam 11.00 - 13.00 juga dilarang (maklum, Jumatan rek).

```
iptables -A INPUT -p tcp --dport 22 -s 10.69.8.0/22 -m time --timestart 12:00 --timestop 13:00 --weekdays Mon,Tue,Wed,Thu -j DROP
iptables -A INPUT -p tcp --dport 22 -s 10.69.8.0/22 -m time --timestart 11:00 --timestop 13:00 --weekdays Fri -j DROP

iptables -A INPUT -p tcp --dport 22 -j
```

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

# Soal 10

Karena kepala suku ingin tau paket apa saja yang di-drop, maka di setiap node server dan router ditambahkan logging paket yang di-drop dengan standard syslog level

```
#!/bin/bash

# semua node

iptables -A INPUT -j LOG --log-level debug --log-prefix 'Dropped Packet' -m limit --limit 1/second --limit-burst 10
```
    
