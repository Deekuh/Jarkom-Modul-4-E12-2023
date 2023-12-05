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

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/2410c8b9-a1a4-43c1-8868-5f03ed4407b7)

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/09181499-0806-4045-9047-846213b32399)
  
  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/cbef7c14-69aa-44ce-a614-68830d8d3860)
  
  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/6b6d1425-1f23-44fd-be2f-a1e908ca415a)

- Frieren

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/ff4c6778-bbfe-4a36-8a88-28e567aa806c)

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/57ce775c-834b-440c-aae4-1c82de012736)

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/cca633e4-2a7d-4b95-bf64-49936d39a5cd)
  
  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/12f18359-0eae-4ad4-b467-31ae11017f16)
 
- Flamme

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/f579cf7d-7f7c-4b91-8bec-d3589eabb5d3)

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/21537638-cb62-4145-b9a6-84c9a51f4326)

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/d08527bd-dbc0-49a0-8c3e-6bbf54172ea1)
  
  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/e0328fe2-c0d6-4b9a-96b3-751bbb027ea2)
  
  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/a7d0ff11-9cf1-47bb-8d7e-0702073dc697) 

- Fern

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/d39c82d4-2a8d-460f-b01b-94daf1059655)

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/c1999a36-9cef-490f-a590-1bd7973cbbd1)

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/0c5560a3-a8e1-4ab0-92df-06166e1116b2)

- Himmel

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/39c51e7e-b623-4dce-a09f-79e6dfb00ee1)

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/2df9c285-0c86-4aaf-972b-e7c7129789f1)

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/8b055e55-b064-4018-a0e5-d012547748e0)

- Denken

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/29965f06-b2c0-4444-99e0-68a7a7de5d0f)

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/bfd43f5e-03ca-49f8-bc45-f616061390d1)

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/535be668-253e-45f0-be34-1f939d2c7e68)

- Eisen

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/e4ff89f9-11ea-45fa-a8b0-f16f3f03192c)

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/f348a63f-86d2-4d2c-b79a-d9f749049bea)

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/d6cece01-46e9-4abf-9193-30333e4e4d4f)
  
  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/f543aa35-b316-4e04-b3d3-fd195f02ff09)

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/70ee53c8-94d5-48e9-8ea4-ef30665aa370)

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/e0b471b1-79c3-4e79-adcd-a1f5ba0947a7)

- Lugner

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/480eaea6-f5d6-452b-bc25-e5c98603e613)

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/61868701-1fbb-432a-b8df-bd12b3a05efc)

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/971f2b26-8e65-4ee3-94b0-2af5b18f6b3c)
  
  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/18a5076b-72d2-49cd-a80c-3204d03d7193)

- Linie

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/f4bc1cc7-255b-4fb7-8ef4-2392477ea99b)

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/18e651f1-c95d-489b-9a68-6477a19511c8)

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/ba84fe8c-ec64-4990-ac24-12d31f21548e)
  
  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/7e0062ac-685a-43d8-90be-f032d153f90b)

- Lawine

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/256db597-53bd-40cb-83e8-787b62b0da02)

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/caae3524-1dee-4ac8-8b52-720ab9a9ae15)

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/fb7751e0-3ba3-47a9-b52f-64be55ba69f7)

- Heiter

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/f46df75f-4f00-479a-b07a-5caff2d0b7ff)

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/5887989c-eeca-4d85-9a57-ab8e5e35814f)

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/50600168-6b59-4276-8bfb-e30f24e6be78)

- LaubHills

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/9b80a295-213b-46f0-a6ce-2951fccca7b6)

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/261dbbc4-c25d-4577-891d-418ab25d5cd0)

- AppetitRegion

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/52685f0d-3493-4364-bb9f-ca8ed34cd1db)

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/416061d6-8f78-4a84-9f71-5b1e216dffd3)
  
- RohrRoad

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/6ff29f8b-0d8b-42dd-ab49-4cd6ae176dc5)

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/7cc9106b-dd27-459c-898a-7a0bd9702d3a)

- SchwerMountains

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/e57d8150-93a1-4e99-8e94-a95de1416b4f)

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/42c3f853-68f6-4458-955a-f0a023825225)

- BredtRegion

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/8fc25376-89ca-4ae7-af03-66f6a8297850)

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/da0f53a4-ac21-41dc-9382-39074ed1e10e)
  
- RiegelCanyon

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/8bca7692-fe15-4f48-ad07-6a9abea80056)

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/bcf01e0c-9036-4566-80c2-fe0f76feedb7)
 
- LakeKorridor

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/c92aef19-dc45-4790-9a4f-e41e503483f9)

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/8d6963f7-a3e3-4f28-84c8-6730f5a5ad90)
  
- GranzChannel

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/60d7d955-7aeb-4a19-8cfd-2464ad0494f0)

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/60720759-74e5-476b-bca1-11168c3d087e)

- GrobeForest

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/b5472c04-ec96-40b4-a76a-4326d6881f96)

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/259e2276-6a4f-4bae-94bd-15055102e70d)
  
- TurkRegion

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/bfcfd99a-15c6-43f7-a426-2df2ddc48fd8)

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/0c45891f-4478-427c-83f0-e29c10d42c2a)

- WilleRegion

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/2aab1672-6ad1-44c9-9ba7-fd7aaa4500a4)

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/6cec51cc-3908-4f31-a10d-14e636dd0ff8)

- RoyalCapital

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/fb883e5b-a4ac-49f6-8c15-45964ca2d374)

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/9f4bee3a-c033-420c-852a-446b75c24745)

- Richter

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/45e30229-2833-4c6a-bbe6-d91343cd87d8)

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/8386b115-8014-4e50-b400-3a754b956442)

- Revolte

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/7387bac6-ab3f-4110-a425-1dd5a24a9d34)

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/895f2bff-e596-4059-a6f3-c70d220e4204)

- Stark

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/3e732bf6-8457-4ef9-aec0-ce344b036854)

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/6ffaea17-1b7e-4527-8ac7-e32e503e5e2a)

- Sein

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/7fbeca35-0959-4083-87ab-c1f52765f259)

  ![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/114421539/b4bae955-2201-4577-9c6b-b7351d577959)
 
### Testing

Di sini kami melakukan ping dari client **AppetitRegion** ke client **GranzChannel**, dari client **SchwerMountains** ke client **WilleRegion**, dari client **LakeKorridor** ke server **Sein**, dan dari client **GrobeForest** ke client **SchwerMountains** dengan hasil sebagai berikut.

![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/90295688/f5669d04-4ea9-4851-9c53-fc3abb2975b3)

![image](https://github.com/Deekuh/Jarkom-Modul-4-E12-2023/assets/90295688/1229735b-e11e-4410-9d0f-efc704867edb)
