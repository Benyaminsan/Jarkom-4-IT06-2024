# Jarkom-4-IT06-2024

Laporan Resmi Jarkom Modul 4
Masih Pemula yg belajar Cisco Packet Tracer dan GNS3

| Nama | NRP |
| ---- | ---- |
| Callista Meyra Azizah | 5027231060 |
| Renjamin Khawarizmi Habibi | 5027231078 |

IP Prefix untuk IT06

| IT06 | 192.236 |
|----|----|

# Membuat Topologi GNS3
![WhatsApp Image 2024-11-14 at 19 09 53_1547123e](https://github.com/user-attachments/assets/bda2750b-30cf-4911-a469-a41b932cd059)

# Membuat Topologi CPT

# Catatan:
- Pembagian IP dan routing harus SE-EFISIEN MUNGKIN.
- Seluruh node yang ada pada topologi harus dapat TERKONEKSI satu sama lain dan dapat melakukan PING ke node lainnya yang ada di topologi

# Rute + Subnet
![RUTE VLSM](https://github.com/user-attachments/assets/a62f066d-d899-43c0-bf44-4c2fcddcddbf)

| Nama Subnet | Rute                                                                                             | Jumlah IP | Netmask        |
|-------------|--------------------------------------------------------------------------------------------------|-----------|----------------|
| A1          | Hololive > Holo-ID                                                                                 | 2         | /30            |
| A2          | Hololive > Holo-ID > AREA:15                                                                       | 2         | /30            |
| A3          | Hololive > Holo-ID > AREA:15 > Switch 6 > Risu---(319_HOST), Moona---(201_HOST), lofi---(140_HOST) | 661       | /22            |
| A4          | Hololive > Holo-ID > holoro                                                                       | 2         | /30            |
| A5          | Hololive > Holo-ID > holoro > Switch 7 > Ollie---(20_HOST), Anya---(3_HOST), Reine---(10_HOST)     | 34        | /26            |
| A6          | Hololive > Holo-ID > holoh3ro                                                                     | 2         | /30            |
| A7          | Hololive > Holo-ID > holoh3ro > Switch 8 > Zeta---(81_HOST), Kaela---(71_HOST), Kobo---(146_HOST)  | 299       | /23            |
| A8          | Hololive > Holo-JP                                                                                 | 2         | /30            |
| A9          | Hololive > Holo-JP > Switch1 > DEV_IS/GEN:0                                                        | 3         | /30            |
| A10         | Hololive > Holo-JP > Switch1 > DEV_IS > Re:OLO > Ririka_Raden---(3_HOST), Ao---(3_HOST), Hajime_Kanade---(7_HOST) | 14        | /29            |
| A11         | Hololive > Holo-JP > Switch1 > GEN:0 > Switch 3 > MiComet---(1501_HOST), Sora_Robo_AZKi---(542_HOST) | 2045      | /21            |
| A12         | Hololive > Holo-JP > Switch1 > GEN:0 > Switch 3 > GEN:1 > GAMERS                                    | 2         | /30            |
| A13         | Hololive > Holo-JP > Switch1 > GEN:0 > Switch 3 > GEN:1 > GAMERS > Fubuki > Korone---(51_HOST), Okayu---(32_HOST), Mio---(36_HOST) | 120       | /25            |
| A14         | Hololive > Holo-JP > Switch1 > GEN:0 > Switch 3 > GEN:1 > Member > FBK_Matsuri---(321_HOST), Aki_Hachama---(148_HOST) | 470       | /23            |
| A15         | Hololive > Holo-EN                                                                                 | 2         | /30            |
| A16         | Hololive > Holo-EN > HoloAdvent                                                                    | 2         | /30            |
| A17         | Hololive > Holo-EN > HoloAdvent > Switch > FuwaMoco---(5_HOST), Shioei_Nerissa---(12_HOST), Biboo---(10_HOST) | 28        | /27            |
| A18         | Hololive > Holo-EN > HoloAdvent > Holo-Myth                                                         | 2         | /30            |
| A19         | Hololive > Holo-EN > HoloAdvent > Holo-Myth > Switch > Kiara_Calli---(192_HOST), Gura_Ame_Ina---(309_HOST) | 503       | /23            |
| A20         | Hololive > Holo-EN > HoloAdvent > Holo-Myth > HoloPromise > Project-Hope/Holo-Council              | 3         | /30            |
| A21         | Hololive > Holo-EN > HoloAdvent > Holo-Myth > HoloPromise > Project-Hope > Irys---(2_HOST)         | 3         | /29            |
| A22         | Hololive > Holo-EN > HoloAdvent > Holo-Myth > HoloPromise > Holo-Council > Switch 4 > Kronii_Mumei---(39_HOST), Bae_Fauna---(22_HOST) | 62        | /26            |
| **Total**   |                                                                                                    | **4263**  |                |


# Tree

![WhatsApp Image 2024-11-17 at 19 55 35_9a9cf0b9](https://github.com/user-attachments/assets/795798d5-a371-40bf-bf76-d994019d9b09)

| Subnet | Network ID       | Netmask          | Broadcast       | Range IP                   |
|--------|------------------|------------------|-----------------|----------------------------|
| A11    | 192.236.6.16     | 255.255.248.0    | 192.236.7.255   | 192.236.6.17 - 192.236.7.254|
| A3     | 192.236.0.8      | 255.255.252.0    | 192.236.3.255   | 192.236.0.9 - 192.236.3.254|
| A14    | 192.236.8.128    | 255.255.254.0    | 192.236.9.255   | 192.236.8.129 - 192.236.9.254|
| A7     | 192.236.4.68     | 255.255.254.0    | 192.236.5.255   | 192.236.4.69 - 192.236.5.254|
| A19    | 192.236.10.36    | 255.255.254.0    | 192.236.11.255  | 192.236.10.37 - 192.236.11.254|
| A13    | 192.236.8.4      | 255.255.255.128  | 192.236.8.127   | 192.236.8.5 - 192.236.8.126|
| A22    | 192.236.12.12    | 255.255.255.192  | 192.236.12.63   | 192.236.12.13 - 192.236.12.62|
| A5     | 192.236.4.4      | 255.255.255.192  | 192.236.4.63    | 192.236.4.5 - 192.236.4.62 |
| A17    | 192.236.10.8     | 255.255.255.224  | 192.236.10.31   | 192.236.10.9 - 192.236.10.30|
| A10    | 192.236.6.8      | 255.255.255.248  | 192.236.6.15    | 192.236.6.9 - 192.236.6.14 |
| A21    | 192.236.12.4     | 255.255.255.248  | 192.236.12.11   | 192.236.12.5 - 192.236.12.10|
| A1     | 192.236.0.0      | 255.255.255.252  | 192.236.0.3     | 192.236.0.1 - 192.236.0.2  |
| A2     | 192.236.0.4      | 255.255.255.252  | 192.236.0.7     | 192.236.0.5 - 192.236.0.6  |
| A4     | 192.236.4.0      | 255.255.255.252  | 192.236.4.3     | 192.236.4.1 - 192.236.4.2  |
| A6     | 192.236.4.64     | 255.255.255.252  | 192.236.4.67    | 192.236.4.65 - 192.236.4.66|
| A8     | 192.236.6.0      | 255.255.255.252  | 192.236.6.3     | 192.236.6.1 - 192.236.6.2  |
| A9     | 192.236.6.4      | 255.255.255.252  | 192.236.6.7     | 192.236.6.5 - 192.236.6.6  |
| A12    | 192.236.8.0      | 255.255.255.252  | 192.236.8.3     | 192.236.8.1 - 192.236.8.2  |
| A15    | 192.236.10.0     | 255.255.255.252  | 192.236.10.3    | 192.236.10.1 - 192.236.10.2|
| A16    | 192.236.10.4     | 255.255.255.252  | 192.236.10.7    | 192.236.10.5 - 192.236.10.6|
| A18    | 192.236.10.32    | 255.255.255.252  | 192.236.10.35   | 192.236.10.33 - 192.236.10.34|
| A20    | 192.236.12.0     | 255.255.255.252  | 192.236.12.3    | 192.236.12.1 - 192.236.12.2|

# GNS (VLSM)
| Subnet | Network ID       | Netmask          | Broadcast       | Range IP                   |
|--------|------------------|------------------|-----------------|----------------------------|
| A1     | 192.236.0.0      | 255.255.255.252  | 192.236.0.3     | 192.236.0.1 - 192.236.0.2  |
| A2     | 192.236.0.4      | 255.255.255.252  | 192.236.0.7     | 192.236.0.5 - 192.236.0.6  |
| A3     | 192.236.0.8      | 255.255.252.0    | 192.236.3.255   | 192.236.0.9 - 192.236.3.254|
| A4     | 192.236.4.0      | 255.255.255.252  | 192.236.4.3     | 192.236.4.1 - 192.236.4.2  |
| A5     | 192.236.4.4      | 255.255.255.192  | 192.236.4.63    | 192.236.4.5 - 192.236.4.62 |
| A6     | 192.236.4.64     | 255.255.255.252  | 192.236.4.67    | 192.236.4.65 - 192.236.4.66|
| A7     | 192.236.4.68     | 255.255.254.0    | 192.236.5.255   | 192.236.4.69 - 192.236.5.254|
| A8     | 192.236.6.0      | 255.255.255.252  | 192.236.6.3     | 192.236.6.1 - 192.236.6.2  |
| A9     | 192.236.6.4      | 255.255.255.252  | 192.236.6.7     | 192.236.6.5 - 192.236.6.6  |
| A10    | 192.236.6.8      | 255.255.255.248  | 192.236.6.15    | 192.236.6.9 - 192.236.6.14 |
| A11    | 192.236.6.16     | 255.255.248.0    | 192.236.7.255   | 192.236.6.17 - 192.236.7.254|
| A12    | 192.236.8.0      | 255.255.255.252  | 192.236.8.3     | 192.236.8.1 - 192.236.8.2  |
| A13    | 192.236.8.4      | 255.255.255.128  | 192.236.8.127   | 192.236.8.5 - 192.236.8.126|
| A14    | 192.236.8.128    | 255.255.254.0    | 192.236.9.255   | 192.236.8.129 - 192.236.9.254|
| A15    | 192.236.10.0     | 255.255.255.252  | 192.236.10.3    | 192.236.10.1 - 192.236.10.2|
| A16    | 192.236.10.4     | 255.255.255.252  | 192.236.10.7    | 192.236.10.5 - 192.236.10.6|
| A17    | 192.236.10.8     | 255.255.255.224  | 192.236.10.31   | 192.236.10.9 - 192.236.10.30|
| A18    | 192.236.10.32    | 255.255.255.252  | 192.236.10.35   | 192.236.10.33 - 192.236.10.34|
| A19    | 192.236.10.36    | 255.255.254.0    | 192.236.11.255  | 192.236.10.37 - 192.236.11.254|
| A20    | 192.236.12.0     | 255.255.255.252  | 192.236.12.3    | 192.236.12.1 - 192.236.12.2|
| A21    | 192.236.12.4     | 255.255.255.248  | 192.236.12.11   | 192.236.12.5 - 192.236.12.10|
| A22    | 192.236.12.12    | 255.255.255.192  | 192.236.12.63   | 192.236.12.13 - 192.236.12.62|

# CPT (CIDR)

# CONFIG NODE

# A1 - Hololive
- Hololive Router
```
auto eth1
iface eth1 inet static
    address 192.236.0.1
    netmask 255.255.255.252
```
- Holo-EN Router
```
auto eth0
iface eth0 inet static
    address 192.236.0.2
    netmask 255.255.255.252
    gateway 192.236.0.1
    up echo 192.168.122.1 > /etc/resolv.conf
```

# A2 - Hololive
- Hololive Router
```
auto eth2
iface eth2 inet static
    address 192.236.0.5
    netmask 255.255.255.252
```
- Holo-ID Router
```
auto eth0
iface eth0 inet static
    address 192.236.0.6
    netmask 255.255.255.252
    gateway 192.236.0.5
    up echo 192.168.122.1 > /etc/resolv.conf
```

# A3 - AREA15
- AREA15 Router
```
auto eth1
iface eth1 inet static
    address 192.236.0.9
    netmask 255.255.252.0
```
- Risu
```
auto eth0
iface eth0 inet static
    address 192.236.0.10
    netmask 255.255.252.0
    gateway 192.236.0.9
    up echo 192.168.122.1 > /etc/resolv.conf
```
- Moona
```
auto eth0
iface eth0 inet static
    address 192.236.0.11
    netmask 255.255.252.0
    gateway 192.236.0.9
    up echo 192.168.122.1 > /etc/resolv.conf
```
- Lofi
```
auto eth0
iface eth0 inet static
    address 192.236.0.12
    netmask 255.255.252.0
    gateway 192.236.0.9
    up echo 192.168.122.1 > /etc/resolv.conf
```
# A4 - Holoro
- Holoro Router
```
auto eth0
iface eth0 inet static
    address 192.236.4.1
    netmask 255.255.255.252
```
# A5 - Holoro
- Holoro Router
```
auto eth1
iface eth1 inet static
    address 192.236.4.5
    netmask 255.255.255.192
```
- Ollie
```
auto eth0
iface eth0 inet static
    address 192.236.4.6
    netmask 255.255.255.192
    gateway 192.236.4.5
    up echo 192.168.122.1 > /etc/resolv.conf
```
- Anya
```
auto eth0
iface eth0 inet static
    address 192.236.4.7
    netmask 255.255.255.192
    gateway 192.236.4.5
    up echo 192.168.122.1 > /etc/resolv.conf
```
- Reine
```
auto eth0
iface eth0 inet static
    address 192.236.4.8
    netmask 255.255.255.192
    gateway 192.236.4.5
    up echo 192.168.122.1 > /etc/resolv.conf
```

# A6 - Holoro
- Holoro Router
```
auto eth2
iface eth2 inet static
    address 192.236.4.65
    netmask 255.255.255.252
```

# A7 - Holoh3ro
- Holoh3ro Router
```
auto eth0
iface eth0 inet static
    address 192.236.4.69
    netmask 255.255.254.0
```
- Zeta
```
auto eth0
iface eth0 inet static
    address 192.236.4.70
    netmask 255.255.254.0
    gateway 192.236.4.69
    up echo 192.168.122.1 > /etc/resolv.conf
```
- Kaela
```
auto eth0
iface eth0 inet static
    address 192.236.4.71
    netmask 255.255.254.0
    gateway 192.236.4.69
    up echo 192.168.122.1 > /etc/resolv.conf
```
- Kobo
```
auto eth0
iface eth0 inet static
    address 192.236.4.72
    netmask 255.255.254.0
    gateway 192.236.4.69
    up echo 192.168.122.1 > /etc/resolv.conf
```

# A8 - Hololive (Holo-JP Gateway)
- Hololive Router
```
auto eth0
iface eth0 inet static
    address 192.236.6.1
    netmask 255.255.255.252
```
# A9 - DEV_IS
- DEV_IS Router
```
auto eth0
iface eth0 inet static
    address 192.236.6.5
    netmask 255.255.255.252
    gateway 192.236.6.4
```

# A10 - AREA15
- AREA15 Router
```
auto eth1
iface eth1 inet static
    address 192.236.6.9
    netmask 255.255.255.248
```

- Ririka_Raden
```
auto eth0
iface eth0 inet static
    address 192.236.6.10
    netmask 255.255.255.248
    gateway 192.236.6.9
    up echo 192.168.122.1 > /etc/resolv.conf
```
- Ao
```
auto eth0
iface eth0 inet static
    address 192.236.6.11
    netmask 255.255.255.248
    gateway 192.236.6.9
    up echo 192.168.122.1 > /etc/resolv.conf
```
- Hajime_Kanade
```
auto eth0
iface eth0 inet static
    address 192.236.6.12
    netmask 255.255.255.248
    gateway 192.236.6.9
    up echo 192.168.122.1 > /etc/resolv.conf
```

# A11 - GEN:0
- GEN:0 Router
```
auto eth0
iface eth0 inet static
    address 192.236.6.16
    netmask 255.255.248.0
```
- MiComet
```
auto eth0
iface eth0 inet static
    address 192.236.6.17
    netmask 255.255.248.0
    gateway 192.236.6.16
    up echo 192.168.122.1 > /etc/resolv.conf
```
- Sora_Robo_AZKi
```
auto eth0
iface eth0 inet static
    address 192.236.6.18
    netmask 255.255.248.0
    gateway 192.236.6.16
    up echo 192.168.122.1 > /etc/resolv.conf
```

# A12 - GEN:1 (GAMERS Router)
- GEN:1 Router
```
auto eth0
iface eth0 inet static
    address 192.236.8.1
    netmask 255.255.255.252
    gateway 192.236.8.0
```

# A13 - GEN:1 (Switch - GAMERS)
- Korone
```
auto eth0
iface eth0 inet static
    address 192.236.8.5
    netmask 255.255.255.128
    gateway 192.236.8.4
    up echo 192.168.122.1 > /etc/resolv.conf
```

- Okayu
```
auto eth0
iface eth0 inet static
    address 192.236.8.6
    netmask 255.255.255.128
    gateway 192.236.8.4
    up echo 192.168.122.1 > /etc/resolv.conf
```

- Mio
```
auto eth0
iface eth0 inet static
    address 192.236.8.7
    netmask 255.255.255.128
    gateway 192.236.8.4
    up echo 192.168.122.1 > /etc/resolv.conf
```

# A14 - GEN:1 (Switch - Member)
- FBK_Matsuri
```
auto eth0
iface eth0 inet static
    address 192.236.8.129
    netmask 255.255.254.0
    gateway 192.236.8.128
    up echo 192.168.122.1 > /etc/resolv.conf
```

- Aki_Hachama
```
auto eth0
iface eth0 inet static
    address 192.236.8.130
    netmask 255.255.254.0
    gateway 192.236.8.128
    up echo 192.168.122.1 > /etc/resolv.conf
```

# A15 - Holo-EN
- Holo-EN Router
```
auto eth0
iface eth0 inet static
    address 192.236.10.1
    netmask 255.255.255.252
```

# A16 - Holo-EN (HoloAdvent Gateway)
- HoloAdvent Router
```
auto eth0
iface eth0 inet static
    address 192.236.10.5
    netmask 255.255.255.252
    gateway 192.236.10.4
```

# A17 - HoloAdvent (Switch)
- FuwaMoco
```
auto eth0
iface eth0 inet static
    address 192.236.10.9
    netmask 255.255.255.224
    gateway 192.236.10.8
    up echo 192.168.122.1 > /etc/resolv.conf
```

- Shiori_Nerissa
```
auto eth0
iface eth0 inet static
    address 192.236.10.10
    netmask 255.255.255.224
    gateway 192.236.10.8
    up echo 192.168.122.1 > /etc/resolv.conf
```

- Biboo
```
auto eth0
iface eth0 inet static
    address 192.236.10.11
    netmask 255.255.255.224
    gateway 192.236.10.8
    up echo 192.168.122.1 > /etc/resolv.conf
```

# A18 - Holo-EN (HoloMyth Gateway)
- HoloMyth Router
```
 auto eth0
iface eth0 inet static
    address 192.236.10.33
    netmask 255.255.255.252
    gateway 192.236.10.32
```

# A19 - HoloAdvent (Switch - Kiara/Gura)
- Kiara_Calli
```
auto eth0
iface eth0 inet static
    address 192.236.10.37
    netmask 255.255.254.0
    gateway 192.236.10.36
    up echo 192.168.122.1 > /etc/resolv.conf
```

- Gura_Ame_Ina
```
auto eth0
iface eth0 inet static
    address 192.236.10.38
    netmask 255.255.254.0
    gateway 192.236.10.36
    up echo 192.168.122.1 > /etc/resolv.conf
```

# 20 - HoloPromise
- HoloPromise Router

```
auto eth0
iface eth0 inet static
    address 192.236.12.1
    netmask 255.255.255.252
    gateway 192.236.12.0
```

# A21 - Project-Hope (Irys)
- Router Project-Hope
```
auto eth0
iface eth0 inet static
    address 192.236.12.4
    netmask 255.255.255.248
```
  
- Irys
```
auto eth0
iface eth0 inet static
    address 192.236.12.5
    netmask 255.255.255.248
    gateway 192.236.12.4
    up echo 192.168.122.1 > /etc/resolv.conf
```    
# A22 - Switch 4 (Kronii_Mumei & Bae_Fauna)
-Router Holo-Council
```
auto eth1
iface eth1 inet static
    address 192.236.12.12
    netmask 255.255.255.192
```
    
- Kronii_Mumei
```
auto eth0
iface eth0 inet static
    address 192.236.12.13
    netmask 255.255.255.192
    gateway 192.236.12.12
    up echo 192.168.122.1 > /etc/resolv.conf
 ```   
- Bae_Fauna
```
auto eth0
iface eth0 inet static
    address 192.236.12.14
    netmask 255.255.255.192
    gateway 192.236.12.12
    up echo 192.168.122.1 > /etc/resolv.conf
```
