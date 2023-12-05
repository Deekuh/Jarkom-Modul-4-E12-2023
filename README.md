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

![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/90295688/831128a7-9e39-4ad3-b301-75553269cca0)

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

### Testing

Di sini kami melakukan ping dari client **AppetitRegion** ke client **GranzChannel** dengan IP Address 192.212.4.2.

![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/90295688/122f0f5c-cb44-4df7-9258-1f159a1df685)


## CIDR pada CPT


### Penggabungan Subnet

- Langkah 1

![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/90295688/c411cd18-2b18-460a-bbb4-1836789ccf44)

![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/90295688/7e64ff29-6cd5-4914-8d4a-6b71874856c4)

- Langkah 2

![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/90295688/4748fcde-c8c6-4aaf-b760-e32e7ec69096)

![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/90295688/28cd647f-90fd-4c1d-8208-203645294652)

- Langkah 3

![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/90295688/f3dda6d0-6435-4773-ac94-4e3106a5a985)

![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/90295688/bea0d78d-fdd6-4bfc-bee6-db12e14884f4)

- Langkah 4

![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/90295688/80bb014a-c75c-466a-a3af-f9af0fc68a5f)

![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/90295688/48006d0f-a41f-4c6f-81f5-8c72d16ec7ea)

- Langkah 5

![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/90295688/191e0414-6209-4674-8654-759f25271774)

![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/90295688/6562e7f3-ecea-43a4-ac03-6fed3fb21873)

- Langkah 6

![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/90295688/680d6f8d-ff08-4f5e-b5c8-62c3a889a25e)

![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/90295688/99031ec1-5f22-4c95-9968-f91d087cd359)

- Langkah 7

![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/90295688/56ffaad9-b6d1-4cc6-bae2-91e3aaa7e4ec)

![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/90295688/65cce67e-8821-42e2-b9b2-0b24825e34c4)

- Langkah 8

![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/90295688/9139afe4-0a1b-41e5-afb4-0da6c8d91f45)

![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/90295688/c1e70a00-cf0a-44a2-9205-ad30c01006c5)

### Tree CIDR

![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/90295688/eb8f37ab-2a01-43fe-a4a6-8f07076d69b9)

### Pembagian IP CIDR

![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/90295688/eb220455-0b18-49bd-a15f-5e8596183422)

### Config dan Routing CPT

- Aura

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/0981b801-30d1-43cb-8b1d-ce4ef7b9a366)

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/f91c4636-1d5b-4f1c-8bcf-fc8df2689f2c)
  
  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/60a86857-dd81-47ba-9d26-4af0ea798a62)
  
  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/ff94de05-fd44-4c3e-b30f-f1bdd99cf6a2)

- Frieren

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/f9e3b5e7-3b0b-41da-9bd4-8d8d6fea6105)

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/1e1f1f47-a6d0-41b5-a777-23edfac5f0ab)
  
  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/6e26dec5-8cf6-43c7-b562-146a00176bdb)
  
  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/b16cffd6-2cfb-47fa-a319-f368ba4fd9f9)
 
- Flamme

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/9b480d91-326b-4bfa-8baa-50048d1d9e99)

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/e5a1be34-feec-46af-b113-9c030ae2202f)
  
  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/20a85591-f46f-4fad-9514-f49f133a0b26)
  
  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/39259da3-8331-4b54-bb28-56e16db67161)

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/12c8b565-9beb-4fd0-9125-2c772408744f)

- Fern

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/73223912-476a-4c97-9f05-f1290710c581)

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/b15bfa4a-dc11-4fb1-9c05-8e38d2440927)
  
  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/8134d380-5579-40d4-8e6a-8616431ce029)

- Himmel

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/9794fa6e-131a-4f60-b1a6-ba6d66c95dc5)

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/9edc634a-a574-43c6-b6d9-97f3d751cacb)
  
  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/94674bda-6ccd-4915-83e6-eacba429c7bb)

- Denken

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/56e3b120-5507-494f-9d61-1d7b5f1ae24b)

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/58eeb778-3d0c-431d-949b-2c6dc248c3cf)
  
  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/a4f50bf1-27bc-4f57-9314-842c235e4be6)

- Eisen

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/3b71277f-218b-4864-95be-ecb565c7f914)

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/d85384ab-ed04-4b5d-9e5e-d95ae7dd2f16)
  
  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/144c4983-b169-4258-8f35-0be23833cdf1)

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/051e402f-6572-4eef-a25f-d9a1060870e9)

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/cff7a480-c048-439a-9ad5-ac511992055b)
  
  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/85b9f7fb-eaae-4cf6-97a2-3d2e97464219)

- Lugner

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/9d92eb97-df76-4f2f-a5ab-80b020242719)

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/7eb260ae-b3fe-4b55-9efb-8f2b334c3dc6)
  
  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/eb28a29f-c32b-41c5-9a37-0c1f8dd7d02d)

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/244a6954-fc70-47b5-bc6e-fbd9a054a55f)

- Linie

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/d5896f9e-47c9-4eac-b9a9-29eb7582b3f6)

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/87fd7fc3-a5d8-4b39-9f34-140f869a9f67)
  
  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/98970cac-4aa6-4ee4-8616-01ec5b766693)

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/2640b911-999f-49e8-bf9f-73037ec2a92e)

- Lawine

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/7fb03659-d65f-4438-81f7-10cc07e61c6e)

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/f0a85cb5-8cdb-477d-b278-2cb34f28cd07)
  
  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/c3b2b072-d1ba-4d3f-96d3-7a9ba8522d05)

- Heiter

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/831854e6-3246-470d-bbd0-de1b3e36ac16)

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/09b29002-5b7b-49a8-af2a-8ade2f0a98bf)
  
  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/32afa6a1-63ab-4f68-95f5-102adc48de38)
 
### Testing

Di sini kami melakukan ping dari client **AppetitRegion** ke client **GranzChannel**, dari client **SchwerMountains** ke client **WilleRegion**, dari client **LakeKorridor** ke server **Sein**, dan dari client **GrobeForest** ke client **SchwerMountains** dengan hasil sebagai berikut.

![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/90295688/f5669d04-4ea9-4851-9c53-fc3abb2975b3)

![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/90295688/1229735b-e11e-4410-9d0f-efc704867edb)
