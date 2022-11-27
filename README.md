# Jarkom-Modul-4-E03-2022

## Kelompok E03
- Pedro T. Korwa              05111940007003
- Made Rianja Richo Dainino   5025201236
- Syaiful Bahri Dirgantara    5025201203

### A. Metode VLSM dengan tools CPT

- Membuat Topologi dan membagi subnet

![image](https://user-images.githubusercontent.com/82220673/204090988-a661b92f-a838-40df-9310-7b06acd6162c.png)

- Membuat tabel untuk menentukan netmask

![image](https://user-images.githubusercontent.com/82220673/204091066-550a995b-5cc2-43d4-8246-fa553f9c2195.png)

- Membuat tree menggunakan metode VLSM

![image](https://user-images.githubusercontent.com/82220673/204091077-b62c6c64-dc45-4fc0-a989-8e06cf7ba7b0.png)

- Membuat tabel alamat IP

![image](https://user-images.githubusercontent.com/82220673/204091105-2a0be8b5-41b5-461e-9133-e707922b31ed.png)

![image](https://user-images.githubusercontent.com/82220673/204091119-fabdfc29-040b-4748-9248-db64daf492e9.png)

![image](https://user-images.githubusercontent.com/82220673/204091136-bf179273-d94c-4745-a9e6-7c87316ddad4.png)

- Mengkonfigurasi tiap node/device

![image](https://user-images.githubusercontent.com/82220673/204091177-609b518a-834e-47db-a250-e5e6f881ae18.png)

- Melakukan Routing

![image](https://user-images.githubusercontent.com/82220673/204091208-a8556f2a-7ecd-4d60-b69e-f0f81141ccdc.png)

- Melakukan Testing

![image](https://user-images.githubusercontent.com/82220673/204091242-febb38cd-3ae6-4c0f-a6e3-6fb1b921c5fb.png)


### B. Metode CIDR dengan tools GNS3

- Membuat Topologi

![1](https://user-images.githubusercontent.com/82220673/204124523-f43ae8a0-3fb4-4313-8cb3-91464870d132.jpg)

- Membuat subnet-subnet dari terkecil dan terjauh dari The Resonance hingga membentuk 1 subnet besar sesuai metode CIDR

![1](https://user-images.githubusercontent.com/82220673/204124585-bb8df135-5e89-4bed-b8e3-d16e9373bee0.jpg)

![2](https://user-images.githubusercontent.com/82220673/204124592-a437c285-ce77-4296-bd82-0b0f0634de7c.jpg)

![3](https://user-images.githubusercontent.com/82220673/204124596-076fd7d6-068d-44da-9b31-a672f1cacdf6.jpg)

![4](https://user-images.githubusercontent.com/82220673/204124602-095f5ba7-b58d-41cc-8bf5-e71e850f2f51.jpg)

![5](https://user-images.githubusercontent.com/82220673/204124607-769a0b35-9dd3-4d2b-b715-f1d137e6482d.jpg)

![6](https://user-images.githubusercontent.com/82220673/204124609-86bfcc97-4433-43c3-b807-4f90b910db32.jpg)

![7](https://user-images.githubusercontent.com/82220673/204124612-141b3cf2-8423-4866-b772-06374c4be866.jpg)

![8](https://user-images.githubusercontent.com/82220673/204124615-9cd9ece8-e989-4864-a792-261740443450.jpg)

- Membuat tabel dan tree sesuai metode CIDR

![image](https://user-images.githubusercontent.com/82220673/204124731-122bd553-a8c9-47e2-b48c-37bfe2ffb7ba.png)

![image](https://user-images.githubusercontent.com/82220673/204124746-b4e9c7fe-4f95-4b1f-afaf-b47163570b99.png)

![image](https://user-images.githubusercontent.com/82220673/204124753-e6432ce9-986a-4f75-8739-26fde41b1cfa.png)

![image](https://user-images.githubusercontent.com/82220673/204124772-e738cdd0-705b-4134-a84f-9bdb28fa3d56.png)

- Melakukan Konfigurasi Alamat IP sesuai tree yang sudah dibuat

Konfigurasi IP sebagai berikut :

1. The Resonance
auto eth0
iface eth0 inet dhcp

auto eth1
iface eth1 inet static
        address 10.23.144.1
	netmask 255.255.255.252

	
auto eth2
iface eth2 inet static
        address 10.23.160.1
	netmask 255.255.255.252
	
auto eth3
iface eth3 inet static
        address 10.23.32.1
	netmask 255.255.255.252
	
auto eth4
iface eth4 inet static
	address 10.23.64.1
	netmask 255.255.255.252

2. The Order
auto eth0
iface eth0 inet static
	address 10.23.32.2
	netmask 255.255.255.252

auto eth1
iface eth1 inet static
	address 10.23.16.1
	netmask 255.255.255.192

auto eth2
iface eth2 inet static
	address 10.23.8.1
	netmask 255.255.255.252

3. Ashaf
auto eth0
iface eth0 inet static
	address 10.23.16.2
	netmask 255.255.255.192
	gateway 10.23.16.1

4. The Minister
auto eth0
iface eth0 inet static
	address 10.23.8.2
	netmask 255.255.255.252

auto eth1
iface eth1 inet static
	address 10.23.4.1
	netmask 255.255.252.0

auto eth2
iface eth2 inet static
	address 10.23.1.1
	netmask 255.255.255.252

5. Guideau
auto eth0
iface eth0 inet static
	address 10.23.4.2
	netmask 255.255.252.0
	gateway 10.23.4.1

6. The Dauntless
auto eth0
iface eth0 inet static
	address 10.23.1.2
	netmask 255.255.255.252

auto eth1
iface eth1 inet static
	address 10.23.0.1
	netmask 255.255.255.0

7. Johan
auto eth0
iface eth0 inet static
	address 10.23.0.2
	netmask 255.255.255.0
	gateway 10.23.0.1

8. Phanora
auto eth0
iface eth0 inet static
	address 10.23.0.3
	netmask 255.255.255.0
	gateway 10.23.0.1

9. The Beast
auto eth0
iface eth0 inet static
	address 10.23.64.2
	netmask 255.255.255.252
	gateway 10.23.64.1

10. The Magical
auto eth0
iface eth0 inet static
	address 10.23.160.2
	netmask 255.255.255.252

auto eth1
iface eth1 inet static
	address 10.23.162.1
	netmask 255.255.254.0

11. Haines
auto eth0
iface eth0 inet static
	address 10.23.162.3
	netmask 255.255.254.0
	gateway 10.23.162.1

12. Corvekt
auto eth0
iface eth0 inet static
	address 10.23.162.2
	netmask 255.255.254.0
	gateway 10.23.162.1

13. The Instrument
auto eth0
iface eth0 inet static
	address 10.23.144.2
	netmask 255.255.255.252

auto eth1
iface eth1 inet static
	address 10.23.138.1
	netmask 255.255.255.128

auto eth2
iface eth2 inet static
	address 10.23.132.1
	netmask 255.255.255.252

auto eth3
iface eth3 inet static
	address 10.23.137.1
	netmask 255.255.255.252

14. Matt Cugat
auto eth0
iface eth0 inet static
	address 10.23.138.2
	netmask 255.255.255.128
	gateway 10.23.138.1

15. The Profound
auto eth0
iface eth0 inet static
	address 10.23.137.2
	netmask 255.255.255.252

auto eth1
iface eth1 inet static
	address 10.23.136.1
	netmask 255.255.255.128

auto eth2
iface eth2 inet static
	address 10.23.136.129
	netmask 255.255.255.128

16. Spendrow
auto eth0
iface eth0 inet static
	address 10.23.136.130
	netmask 255.255.255.128
	gateway 10.23.136.129

17. Helga
auto eth0
iface eth0 inet static
	address 10.23.136.2
	netmask 255.255.255.128
	gateway 10.23.136.1

18. The Firefist
auto eth0
iface eth0 inet static
	address 10.23.132.2
	netmask 255.255.255.252

auto eth1
iface eth1 inet static
        address 10.23.130.1
	netmask 255.255.254.0

auto eth2
iface eth2 inet static
	address 10.23.128.1
	netmask 255.255.255.0

19. Oakleave
auto eth0
iface eth0 inet static
	address 10.23.130.2
	netmask 255.255.254.0
	gateway 10.23.130.1

20. Keith
auto eth0
iface eth0 inet static
	address 10.23.128.2
	netmask 255.255.255.0
	gateway 10.23.128.1

21. The Queen
auto eth0
iface eth0 inet static
	address 10.23.128.2
	netmask 255.255.255.0

auto eth1
iface eth1 inet static
	address 10.23.129.1
	netmask 255.255.255.252

22. The Witch
auto eth0
iface eth0 inet static
	address 10.23.129.2
	netmask 255.255.255.252
	gateway 10.23.129.1

- Melakukan Routing sesuai tree yang telah dibuat

1. The Resonance
route add -net 10.23.4.0 netmask 255.255.252.0 gw 10.23.32.2
route add -net 10.23.1.0 netmask 255.255.255.252 gw 10.23.32.2
route add -net 10.23.0.0 netmask 255.255.255.0 gw 10.23.32.2
route add -net 10.23.8.0 netmask 255.255.255.252 gw 10.23.32.2
route add -net 10.23.16.0 netmask 255.255.255.192 gw 10.23.32.2
route add -net 10.23.138.0 netmask 255.255.255.128 gw 10.23.144.2
route add -net 10.23.132.0 netmask 255.255.255.252 gw 10.23.144.2
route add -net 10.23.128.0 netmask 255.255.255.0 gw 10.23.144.2
route add -net 10.23.129.0 netmask 255.255.255.252 gw 10.23.144.2
route add -net 10.23.130.0 netmask 255.255.254.0 gw 10.23.144.2
route add -net 10.23.137.0 netmask 255.255.255.252 gw 10.23.144.2
route add -net 10.23.136.0 netmask 255.255.255.128 gw 10.23.144.2
route add -net 10.23.136.128 netmask 255.255.255.128 gw 10.23.144.2
route add -net 10.23.162.0 netmask 255.255.254.0 gw 10.23.160.2

2. The Order
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.23.32.1
route add -net 10.23.4.0 netmask 255.255.252.0 gw 10.23.8.2
route add -net 10.23.1.0 netmask 255.255.255.252 gw 10.23.8.2
route add -net 10.23.0.0 netmask 255.255.255.0 gw 10.23.8.2

3. The Minister
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.23.8.1
route add -net 10.23.0.0 netmask 255.255.255.0 gw 10.23.1.2

4. The Dauntless
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.23.1.1

5. The Magical
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.23.160.1

6. The Instrument
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.23.144.1
route add -net 10.23.128.0 netmask 255.255.255.0 gw 10.23.132.2
route add -net 10.23.129.0 netmask 255.255.255.252 gw 10.23.132.2
route add -net 10.23.130.0 netmask 255.255.254.0 gw 10.23.132.2
route add -net 10.23.136.0 netmask 255.255.255.128 gw 10.23.137.2
route add -net 10.23.136.128 netmask 255.255.255.128 gw 10.23.137.2

7. The Profound
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.23.137.1

8. The Firefist
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.23.132.1
route add -net 10.23.129.0 netmask 255.255.255.252 gw 10.23.128.2

9. The Queen
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.23.128.1

- Melakukan testing

1. Ping google di The Witch

![image](https://user-images.githubusercontent.com/82220673/204124867-103a6f38-e865-4167-82f4-32854f79303c.png)

2. Ping Oakleave ke The Instrument

![image](https://user-images.githubusercontent.com/82220673/204124969-96180c25-bb5c-4753-bdfd-5bdb7f1e3373.png)

3. Ping Guideau ke Matt Cugat

![image](https://user-images.githubusercontent.com/82220673/204125073-204394f6-55d3-4c90-b64a-3f895b753080.png)


### Kendala

Kendala yang kami alami yakni pada masa pengerjaan kami hanya mampu menyelesaikan VLSM dengan konfigurasi pada CPT. Proses revisi pengerjaan CIDR baru dapat kami selesaikan dengan tambahan waktu dari asisten penguji yakni hari minggu dikarenakan kebingungan kami pada perhitungan dan konfigurasi.
