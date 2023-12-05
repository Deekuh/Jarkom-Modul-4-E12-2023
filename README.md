# Jarkom-Modul-4-E12-2023

## Anggota Kelompok
- Andhika Lingga Mariano (5025211161)
- Beauty Valen Fajri (5025211227)

## Daftar Isi
- [Topologi](#topologi)
    - [GNS3](#gns3)
    - [CPT](#cpt)
    - [Subnet](#subnet)
- [VLSM pada GNS3](#vlsm-pada-gns3)
    - [Tree VLSM](#tree-vlsm)
    - [Pembagian IP VLSM](#pembagian-ip-vlsm)
    - [Config GNS3](#config-gns3)
    - [Routing GNS3](#routing-gns3)
- [CIDR pada CPT](#cidr-pada-cpt)
    - [Penggabungan Subnet](#penggabungan-subnet)
    - [Tree CIDR](#tree-cidr)
    - [Pembagian IP CIDR](#pembagian-ip-cidr)
    - [Config dan Routing CPT](#config-dan-routing-cpt)

## Topologi
### GNS3

![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/90295688/844bb1c8-73d0-4cb0-90fa-bb86d4cff717)

### CPT

![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/90295688/7600d795-2845-4b93-8ce9-cd0baa9187be)

### Subnet

![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/90295688/56e11699-7c95-45b5-a4b8-66c621d47cd4)

## VLSM pada GNS3


### Tree VLSM

![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/90295688/a660e25a-1a6c-455d-957b-11a6b18db8fc)

### Pembagian IP VLSM

![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/90295688/012733f8-9b3d-4e77-8415-e9d4dcc501ae)

### Config GNS3

- Aura
```
auto eth0
iface eth0 inet dhcp

auto eth1
iface eth1 inet static
    address 192.212.0.13
    netmask 255.255.255.252

auto eth2
iface eth2 inet static
    address 192.212.0.21
    netmask 255.255.255.252

auto eth3
iface eth3 inet static
    address 192.212.0.9
    netmask 255.255.255.252
```

- Frieren
```
auto eth0
iface eth0 inet static
	address 192.212.0.10
	netmask 255.255.255.252

auto eth1
iface eth1 inet static
	address 192.212.0.65
	netmask 255.255.255.224

auto eth2
iface eth2 inet static
	address 192.212.4.1
	netmask 255.255.255.252
```

- Flamme
```
auto eth0
iface eth0 inet static
	address 192.212.4.2
	netmask 255.255.255.252

auto eth1
iface eth1 inet static
	address 192.212.0.1
	netmask 255.255.255.252

auto eth2
iface eth2 inet static
	address 192.212.8.1
	netmask 255.255.252.0

auto eth3
iface eth3 inet static
	address 192.212.0.17
	netmask 255.255.255.252
```

- Fern
```
auto eth0
iface eth0 inet static
	address 192.212.0.2
	netmask 255.255.255.252

auto eth1
iface eth1 inet static
	address 192.212.24.1
	netmask 255.255.248.0
```


- Himmel
```
auto eth0
iface eth0 inet static
	address 192.212.0.18
	netmask 255.255.255.252

auto eth1
iface eth1 inet static
	address 192.212.0.41
	netmask 255.255.255.248
```


- LakeKorridor (24 Host)
```
auto eth0
iface eth0 inet static
	address 192.212.0.66
	netmask 255.255.255.224
	gateway 192.212.0.65
```


- LaubHills (397 Host)
```
auto eth0
iface eth0 inet static
	address 192.212.24.2
	netmask 255.255.248.0
	gateway 192.212.24.1
```


- AppetitRegion (625 Host)
```
auto eth0
iface eth0 inet static
	address 192.212.24.3
	netmask 255.255.248.0
	gateway 192.212.24.1
```

- RohrRoad (1000 Host)
```
auto eth0
iface eth0 inet static
	address 192.212.8.2
	netmask 255.255.252.0
	gateway 192.212.8.1
```


- SchwerMountains (5 Host)
```
auto eth0
iface eth0 inet static
	address 192.212.0.42
	netmask 255.255.255.248
	gateway 192.212.0.41
```

- Denken
```
auto eth0
iface eth0 inet static
    address 192.212.0.14
    netmask 255.255.255.252

auto eth1
iface eth1 inet static
	address 192.212.0.41
	netmask 255.255.255.0
```


- RoyalCapital (63 Host)
```
auto eth0
iface eth0 inet static
	address 192.212.0.42
	netmask 255.255.255.0
	gateway 192.212.0.41
```


- WilleRegion (63 Host)
```
auto eth0
iface eth0 inet static
	address 192.212.0.43
	netmask 255.255.255.0
	gateway 192.212.0.41
```

- Eisen
```
auto eth0
iface eth0 inet static
    address 192.212.0.22
    netmask 255.255.255.252

auto eth1
iface eth1 inet static
    address 192.212.0.25
    netmask 255.255.255.252

auto eth2
iface eth2 inet static
    address 192.212.0.29
    netmask 255.255.255.252

auto eth3
iface eth3 inet static
    address 192.212.0.33
    netmask 255.255.255.252

auto eth4
iface eth4 inet static
    address 192.212.0.49
    netmask 255.255.255.248
```

- Linie
```
auto eth0
iface eth0 inet static
    address 192.212.0.34
    netmask 255.255.255.252

auto eth1
iface eth1 inet static
    address 192.212.4.1
    netmask 255.255.254.0

auto eth2
iface eth2 inet static
    address 192.212.0.37
    netmask 255.255.255.252
```

- GranzChannel (254 Host)
```
auto eth0
iface eth0 inet static
    address 192.212.4.2
    netmask 255.255.254.0
    gateway 192.212.4.1
```

- Lawine
```
auto eth0
iface eth0 inet static
    address 192.212.0.38
    netmask 255.255.255.252

auto eth1
iface eth1 inet static
    address 192.212.0.129
    netmask 255.255.255.192
```

-  BredtRegion (29 Host)
```
auto eth0
iface eth0 inet static
    address 192.212.0.130
    netmask 255.255.255.192
    gateway 192.212.0.129
```

- Heiter
```
auto eth0
iface eth0 inet static
    address 192.212.0.131
    netmask 255.255.255.192

auto eth1
iface eth1 inet static
    address 192.212.16.1
    netmask 255.255.252.0
```

- Sein
```
auto eth0
iface eth0 inet static
    address 192.212.16.2
    netmask 255.255.252.0
    gateway 192.212.16.1
```

- RiegelCanyon (510 Host)
```
auto eth0
iface eth0 inet static
    address 192.212.16.3
    netmask 255.255.252.0
    gateway 192.212.16.1
```

- Lugner
```
auto eth0
iface eth0 inet static
    address 192.212.0.30
    netmask 255.255.255.252

auto eth1
iface eth1 inet static
    address 192.212.12.1
    netmask 255.255.252.0

auto eth2
iface eth2 inet static
    address 192.212.2.1
    netmask 255.255.255.0
```

- TurkRegion (1000 Host)
```
auto eth0
iface eth0 inet static
    address 192.212.12.2
    netmask 255.255.252.0
    gateway 192.212.12.1
```

- GrobeForest (1000 Host)
```
auto eth0
iface eth0 inet static
    address 192.212.2.2
    netmask 255.255.255.0
    address 192.212.2.1
```

- Richter
```
auto eth0
iface eth0 inet static
    address 192.212.0.50
    netmask 255.255.255.248
    gateway 192.212.0.49
```

- Revolte
```
auto eth0
iface eth0 inet static
    address 192.212.0.51
    netmask 255.255.255.248
    gateway 192.212.0.49
```

- Stark
```
auto eth0
iface eth0 inet static
    address 192.212.0.26
    netmask 255.255.255.252
    gateway 192.212.0.25
```

### Routing GNS3

- Aura
```
# Kiri
route add -net 192.212.24.0 netmask 255.255.248.0 gw 192.212.0.10 #A1
route add -net 192.212.0.64 netmask 255.255.255.224 gw 192.212.0.10 #A2
route add -net 192.212.0.0 netmask 255.255.255.252 gw 192.212.0.10 #A3
route add -net 192.212.8.0 netmask 255.255.252.0 gw 192.212.0.10 #A4
route add -net 192.212.4.0 netmask 255.255.255.252 gw 192.212.0.10 #A5
route add -net 192.212.0.40 netmask 255.255.255.248 gw 192.212.0.10 #A9
route add -net 192.212.0.16 netmask 255.255.255.252 gw 192.212.0.10 #A10

# Kanan
route add -net 192.212.1.0 netmask 255.255.255.0 gw 192.212.0.14 #A10

# Bawah
route add -net 192.212.0.48 netmask 255.255.255.248 gw 192.212.0.14 #A11
route add -net 192.212.0.24 netmask 255.255.255.252 gw 192.212.0.14 #A13
route add -net 192.212.0.28 netmask 255.255.255.252 gw 192.212.0.14 #A14
route add -net 192.212.12.0 netmask 255.255.252.0 gw 192.212.0.14 #A15
route add -net 192.212.2.0 netmask 255.255.255.0 gw 192.212.0.14 #A16
route add -net 192.212.0.32 netmask 255.255.255.252 gw 192.212.0.14 #A17
route add -net 192.212.0.128 netmask 255.255.255.192 gw 192.212.0.14 #A18
route add -net 192.212.0.36 netmask 255.255.255.252 gw 192.212.0.14 #A19
route add -net 192.212.16.0 netmask 255.255.252.0 gw 192.212.0.14 #A20
route add -net 192.212.4.0 netmask 255.255.254.0 gw 192.212.0.14 #A21
```

- Frieren
```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.212.0.9 #default
route add -net 192.212.24.0 netmask 255.255.248.0 gw 192.212.4.2 #A1
route add -net 192.212.0.0 netmask 255.255.255.252 gw 192.212.4.2 #A3
route add -net 192.212.8.0 netmask 255.255.252.0 gw 192.212.4.2 #A4
route add -net 192.212.0.40 netmask 255.255.255.248 gw 192.212.4.2 #A9
route add -net 192.212.0.16 netmask 255.255.255.252 gw 192.212.4.2 #A10
```

- Flamme
```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.212.4.1 #default
route add -net 192.212.24.0 netmask 255.255.248.0 gw 192.212.0.2 #A1
route add -net 192.212.0.40 netmask 255.255.255.248 gw 192.212.0.18 #A9
```

- Fern
```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.212.0.1 #default
```

- Himmel
```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.212.0.17 #default
```

- Denken
```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.212.0.13 #default
```

- Eisen
```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.212.0.21 #default
route add -net 192.212.12.0 netmask 255.255.252.0 gw 192.212.0.30 #A15
route add -net 192.212.2.0 netmask 255.255.255.0 gw 192.212.0.30 #A16
route add -net 192.212.0.128 netmask 255.255.255.192 gw 192.212.0.34 #A18
route add -net 192.212.0.36 netmask 255.255.255.252 gw 192.212.0.34 #A19
route add -net 192.212.16.0 netmask 255.255.252.0 gw 192.212.0.34 #A20
route add -net 192.212.4.0 netmask 255.255.254.0 gw 192.212.0.34 #A21
```

- Lugner
```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.212.0.29 #default
```

- Linie
```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.212.0.33 #default
route add -net 192.212.0.128 netmask 255.255.255.192 gw 192.212.0.38 #A18
route add -net 192.212.16.0 netmask 255.255.252.0 gw 192.212.0.38 #A20
```

- Lawine
```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.212.0.37 #default
route add -net 192.212.16.0 netmask 255.255.252.0 gw 192.212.0.131 #A20
```

- Heiter
```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.212.0.129 #default
```

## CIDR pada CPT


### Penggabungan Subnet


### Tree CIDR


### Pembagian IP CIDR


### Config dan Routing CPT
