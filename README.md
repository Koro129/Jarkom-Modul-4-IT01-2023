# Jarkom-Modul-4-IT01-2023

## Topologi
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

### CPT
![CIDR](https://github.com/Koro129/Jarkom-Modul-4-IT01-2023/assets/102176304/6b87df23-b854-408d-bef9-900f17ef5c2d)
## CIDR
Labelling netmask terhadap masing-masing subnet
![CIDR](https://github.com/Koro129/Jarkom-Modul-4-IT01-2023/assets/102176304/b1343f41-8f92-4e06-b149-03afd76cdf16)
CIDR tree
![CIDR Tree](https://github.com/Koro129/Jarkom-Modul-4-IT01-2023/assets/102176304/8bb4b5a3-54be-4140-9845-1244ae54b740)

![CIDR 1](https://github.com/Koro129/Jarkom-Modul-4-IT01-2023/assets/102176304/6c62c035-4942-4f65-aa38-97d6e3e90651)
![CIDR 2](https://github.com/Koro129/Jarkom-Modul-4-IT01-2023/assets/102176304/6c249e79-e78f-4b87-a3d4-42b4fc97d1fa)

Berikut merupakan pembagian ip dengan ip besar 10.64.0.0/13. /13 didapatkan dari jumlah ip yang dibutuhkan pada rute diatas  
![IP CIDR](https://github.com/Koro129/Jarkom-Modul-4-IT01-2023/assets/102176304/73b8ae6a-2152-4a1f-b484-28aa41bc062b)

### Kendala
Masih belum bisa melakukan routing pada gns3 dan cpt
