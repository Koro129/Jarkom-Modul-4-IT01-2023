# Jarkom-Modul-4-IT01-2023

## Topoogi
### GNS3
![image](https://github.com/Koro129/Jarkom-Modul-4-IT01-2023/assets/113784446/8e57f91b-9804-47bd-b998-213bae0c29b1)
## Rute
![image](https://github.com/Koro129/Jarkom-Modul-4-IT01-2023/assets/113784446/b5efca0d-4c03-4389-823b-ec30fb57fb26)
## VLSM
Berikut merupakan pohon pembagian ip dengan ip besar 10.64.0.0/19. /19 didapatkan dari jumlah ip yang dibutuhkan pada rute diatas   
![VLSM Tree](https://github.com/Koro129/Jarkom-Modul-4-IT01-2023/assets/113784446/20fc14c7-c45f-4633-8604-70df0512a74f)   
Berikut hasil pembagian Ip nya, diurutkan dari yang butuh ip terbesar (A17 /21) sampai dengan terkecil (A19 /30)
![image](https://github.com/Koro129/Jarkom-Modul-4-IT01-2023/assets/113784446/3e2e361c-148b-4449-bcbf-e997aa4d86d7)   
Kemudian konfigurasi node dengan ip address adalah rentang antara NID sampai Broadcast sesuai pada subnet nya
contoh
### Aura
```
auto eth0
iface eth0 inet dhcp

auto eth1
iface eth1 inet static
	address 10.64.24.113
	netmask 255.255.255.252

auto eth2
iface eth2 inet static
	address 10.64.24.117
	netmask 255.255.255.252

auto eth3
iface eth3 inet static
	address 10.64.24.137
	netmask 255.255.255.252
```
### Denken
```
auto eth0
iface eth0 inet static
	address 10.64.24.114
	netmask 255.255.255.252
	gateway 10.64.24.113

auto eth1
iface eth1 inet static
	address 10.64.23.1
	netmask 255.255.255.0
	gateway 10.64.24.113
```
### RoyalCapital
```
auto eth0
iface eth0 inet static
	address 10.64.23.2
	netmask 255.255.255.0
	gateway 10.64.23.1
```
### Kendala
Masih belum bisa melakukan routing pada gns3
