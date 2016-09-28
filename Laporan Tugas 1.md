# Laporan Tugas 1 PKSJ Kelompok 13

Anggota Kelompok:
Andre Abdirrosyid (5112100186)

Muhammad Adnan Yusuf (5113100001)

Adian Latifa Nurrohman (5113100031)

Tomson Panagua Krisasandi Pangaribuan (5113100048)

## PENDAHULUAN

Tugas ini dibuat untuk menyelesaikan tugas Mata Kuliah Perancangan Keamanan Sistem dan Jaringan (PKSJ) Tahun 2016/2017, Teknik Informatika, Institut Teknologi Sepuluh Nopember, Surabaya.

Penjelasan tugas:

Tugas 1: Uji Penetrasi 1

-	Install sebuah virtual OS dengan Ubuntu Server
-	Install SSH Server dengan konfigurasi default
-	Install satu lagi virtual OS dengan OS bebas, misalnya Kali Linux atau Ubuntu Desktop
-	Pastikan tools untuk SSH brute force attack sudah terinstall
-	Lakukan uji penetrasi 1 dengan THC-Hydra atau Ncrack dan catat hasil uji penetrasi 1

Tugas 2: Uji Penetrasi 2

-	Install fail2ban pada Ubuntu Server yang telah diinstall SSH Servernya
-	Konfigurasilah SSH Server agar tidak default lagi
-	Lakukan uji penetrasi 2 dengan tools yang sama dan catat hasilnya

## LANDASAN TEORI

a.	OS yang digunakan

- Ubuntu Server

  Ubuntu Server adalah sistem operasi turunan dari Linux Ubuntu yang didesain khusus dengan kernel yang telah dikustomisasi untuk bekerja sebagai sistem operasi server.
 
- Kali Linux

  Kali Linux adalah sebuah distro linux yang dikembangkan oleh Offensive Security yang mempunyai fungsi untuk kebutuhan professional penetration tester.

b.	Tools yang digunakan

Attacking Tools

- THC Hydra

 THC-Hydra adalah sebuah tools untuk security tester dengan mencoba semua password yangk ita siapkan dalam sebuah list atau yang kita   tentukan sebelumnya. Lebih tepatnya dengan menggunakan teknik bruteforce.

- Ncrack

 Ncrack adalah sebuah tool untuk membobol proses autentikasi dari suatu jaringan dengan kecepatan tinggi. Perusahaan biasanya menggunakan tool ini untuk melakukan tes pada host dan perangkat suatu jaringan yang menggunakan password yang lemah.

Defending Tools

- Fail2ban

 Fail2ban adalah package keamanan yang digunakan untuk mencegah serangan bruteforce dan DDoS pada linux.


## UJI PENETRASI 1

### 1.	Installasi Ubuntu Server

  1 . Pilih 'New' untuk membuat Virtual Machine yang baru
  
![alt text](https://github.com/panagua/PKSJ_Kelompok_x/blob/master/instalasi-ubuntu-server/1.PNG "Logo Title Text 1")

  2 . Masukkan nama,tipe,dan versi OS yang sesuai dengan OS yang akan diinstall kemudian aturlah jumlah RAM yang akan digunakan sesuai dengan kebutuhan OS dan pilih 'create a virtual hard disk now'.
  
![alt text](https://github.com/panagua/PKSJ_Kelompok_x/blob/master/instalasi-ubuntu-server/2.PNG "Logo Title Text 2")

  3 . Masukkan size virtual disk yang dibutuhkan kemudian pilih 'VDI' untuk tipe file hard disk.
  
![alt text](https://github.com/panagua/PKSJ_Kelompok_x/blob/master/instalasi-ubuntu-server/3.PNG "Logo Title Text 3")

  4 . Pilih 'setting' untuk membuka menu setting kemudian pilih 'storage'
  
![alt text](https://github.com/panagua/PKSJ_Kelompok_x/blob/master/instalasi-ubuntu-server/4.PNG "Logo Title Text 4")

  5 . Pilih file ISO OS yang ingin digunakan
  
![alt text](https://github.com/panagua/PKSJ_Kelompok_x/blob/master/instalasi-ubuntu-server/5.PNG "Logo Title Text 5")

  6 . Klik 'Ubuntu Server' dan klik start untuk menjalankan VM.
  
![alt text](https://github.com/panagua/PKSJ_Kelompok_x/blob/master/instalasi-ubuntu-server/6.PNG "Logo Title Text 6")

  7 . Plih bahasa yang akan digunakan.
  
![alt text](https://github.com/panagua/PKSJ_Kelompok_x/blob/master/instalasi-ubuntu-server/7.PNG "Logo Title Text 7")

  8 . Plih 'Install Ubuntu Server'.
  
![alt text](https://github.com/panagua/PKSJ_Kelompok_x/blob/master/instalasi-ubuntu-server/8.PNG "Logo Title Text 8")

  9 . Plih bahasa yang akan digunakan.
 
![alt text](https://github.com/panagua/PKSJ_Kelompok_x/blob/master/instalasi-ubuntu-server/9.PNG "Logo Title Text 9")

  10 . Pilih negera tempat tinggalmu.(karena tidak ada pilihan 'Indonesia',maka pilih 'Other')
  
![alt text](https://github.com/panagua/PKSJ_Kelompok_x/blob/master/instalasi-ubuntu-server/10.PNG "Logo Title Text 10")

  11 . Pilih benua tempat tinggalmu.
  
![alt text](https://github.com/panagua/PKSJ_Kelompok_x/blob/master/instalasi-ubuntu-server/11.PNG "Logo Title Text 11")

  12 . Pilih negara tempat tinggalmu. 
  
![alt text](https://github.com/panagua/PKSJ_Kelompok_x/blob/master/instalasi-ubuntu-server/12.PNG "Logo Title Text 12")

  13 . Pilih negara yang menjadi basis locale 
  
![alt text](https://github.com/panagua/PKSJ_Kelompok_x/blob/master/instalasi-ubuntu-server/13.PNG "Logo Title Text 13")

  14 . Pilih 'no' pada detect keyboard layout
  
![alt text](https://github.com/panagua/PKSJ_Kelompok_x/blob/master/instalasi-ubuntu-server/14.PNG "Logo Title Text 14")

  15 . Pilih negara yang ingin dijadikan keyboard layout

![alt text](https://github.com/panagua/PKSJ_Kelompok_x/blob/master/instalasi-ubuntu-server/15.PNG "Logo Title Text 15")

  16 . Pilih keyboard layout
  
![alt text](https://github.com/panagua/PKSJ_Kelompok_x/blob/master/instalasi-ubuntu-server/16.PNG "Logo Title Text 16")

  17 . Masukkan hostname yang ingin digunakan
  
![alt text](https://github.com/panagua/PKSJ_Kelompok_x/blob/master/instalasi-ubuntu-server/17.PNG "Logo Title Text 17")

  18 . Masukkan full name yang ingin digunakan
  
![alt text](https://github.com/panagua/PKSJ_Kelompok_x/blob/master/instalasi-ubuntu-server/18.PNG "Logo Title Text 18")

  19 . Masukkan username yang ingin digunakan
  
![alt text](https://github.com/panagua/PKSJ_Kelompok_x/blob/master/instalasi-ubuntu-server/19.PNG "Logo Title Text 19")
 
  20 . Masukkan password yang ingin digunakan
 
![alt text](https://github.com/panagua/PKSJ_Kelompok_x/blob/master/instalasi-ubuntu-server/20.PNG "Logo Title Text 20")

  21 . Masukkan password untuk verifikasi
  
![alt text](https://github.com/panagua/PKSJ_Kelompok_x/blob/master/instalasi-ubuntu-server/21.PNG "Logo Title Text 21")

  22 . Pilih 'no' untuk tidak mengenkripsi direktori home
  
![alt text](https://github.com/panagua/PKSJ_Kelompok_x/blob/master/instalasi-ubuntu-server/22.PNG "Logo Title Text 22")

  23 . Pilihlah Time Zone yang sesuai dengan lokasi tempat tinggal
  
![alt text](https://github.com/panagua/PKSJ_Kelompok_x/blob/master/instalasi-ubuntu-server/23.PNG "Logo Title Text 23")
 
  24 . Pilihlah opsi untuk mempartisi disk
 
![alt text](https://github.com/panagua/PKSJ_Kelompok_x/blob/master/instalasi-ubuntu-server/24.PNG "Logo Title Text 24") 

  25 . Pilih disk yang akan dipartisi
  
![alt text](https://github.com/panagua/PKSJ_Kelompok_x/blob/master/instalasi-ubuntu-server/25.PNG "Logo Title Text 25")

  26 . Pilih 'yes' untuk memulai proses partisi
 
![alt text](https://github.com/panagua/PKSJ_Kelompok_x/blob/master/instalasi-ubuntu-server/26.PNG "Logo Title Text 26")

  27 . Masukkan HTTP Proxy jika ada
  
![alt text](https://github.com/panagua/PKSJ_Kelompok_x/blob/master/instalasi-ubuntu-server/27.PNG "Logo Title Text 27")

  28 . Pilih 'install security updates automatically
  
![alt text](https://github.com/panagua/PKSJ_Kelompok_x/blob/master/instalasi-ubuntu-server/28.PNG "Logo Title Text 28")
 
  29 . Pilih sofware yang akan diinstall sesuai dengan kebutuhan

![alt text](https://github.com/panagua/PKSJ_Kelompok_x/blob/master/instalasi-ubuntu-server/29.PNG "Logo Title Text 29")

  30 . Pilih 'yes' untuk menginstall GRUB loader
  
![alt text](https://github.com/panagua/PKSJ_Kelompok_x/blob/master/instalasi-ubuntu-server/30.PNG "Logo Title Text 30")

  31 . Tampilan instalasi selesai,pilih 'continue' untuk melakukan reboot
  
![alt text](https://github.com/panagua/PKSJ_Kelompok_x/blob/master/instalasi-ubuntu-server/31.PNG "Logo Title Text 31")

  32 . Masukkan username yang sudah dibuat
  
![alt text](https://github.com/panagua/PKSJ_Kelompok_x/blob/master/instalasi-ubuntu-server/32.PNG "Logo Title Text 32")

  33 . Tampilan home Ubuntu Server
  
![alt text](https://github.com/panagua/PKSJ_Kelompok_x/blob/master/instalasi-ubuntu-server/33.PNG "Logo Title Text 33")

### 2. Instalasi SSH Server

  1.Instal ssh server dengan mengetik :"sudo apt-get install openssh-server"

![alt text](https://github.com/panagua/PKSJ_Kelompok_x/blob/master/Instalasi-ssh-server/1.PNG "Logo Title Text 1")

  2.Tampilan proses instalasi

![alt text](https://github.com/panagua/PKSJ_Kelompok_x/blob/master/Instalasi-ssh-server/2.PNG "Logo Title Text 2")
  
  3.Jalankan ssh server dengan mengetik :"sudo service ssh start"
  
![alt text](https://github.com/panagua/PKSJ_Kelompok_x/blob/master/Instalasi-ssh-server/3.PNG "Logo Title Text 3")
  
  4.Tampilan proses start ssh server
  
![alt text](https://github.com/panagua/PKSJ_Kelompok_x/blob/master/Instalasi-ssh-server/4.PNG "Logo Title Text 4")
  
### 3. Instalasi Ubuntu Server
  1 . Pilih 'New' untuk membuat Virtual Machine yang baru
  
![alt text](https://github.com/panagua/PKSJ_Kelompok_x/blob/master/Instalasi-Kali-Linux/1.PNG "Logo Title Text 1")

  2 . Masukkan nama,tipe,dan versi OS yang sesuai dengan OS yang akan diinstall kemudian aturlah jumlah RAM yang akan digunakan sesuai dengan kebutuhan OS dan pilih 'create a virtual hard disk now'.
  
![alt text](https://github.com/panagua/PKSJ_Kelompok_x/blob/master/Instalasi-Kali-Linux/2.PNG "Logo Title Text 2")
  
  3 . Masukkan size virtual disk yang dibutuhkan kemudian pilih 'VDI' untuk tipe file hard disk.
  
![alt text](https://github.com/panagua/PKSJ_Kelompok_x/blob/master/Instalasi-Kali-Linux/3.PNG "Logo Title Text 3")

  4 . Pilih 'setting' untuk membuka menu setting kemudian pilih 'storage'

![alt text](https://github.com/panagua/PKSJ_Kelompok_x/blob/master/Instalasi-Kali-Linux/4.PNG "Logo Title Text 4")

  5 . Pilih file ISO OS yang ingin digunakan
  
![alt text](https://github.com/panagua/PKSJ_Kelompok_x/blob/master/Instalasi-Kali-Linux/5.PNG "Logo Title Text 5")

  6 . Klik 'Kali Linux' dan klik start untuk menjalankan VM.
  
![alt text](https://github.com/panagua/PKSJ_Kelompok_x/blob/master/Instalasi-Kali-Linux/6.PNG "Logo Title Text 6")

  7 . pilih opsi 'Graphical Install'
  
![alt text](https://github.com/panagua/PKSJ_Kelompok_x/blob/master/Instalasi-Kali-Linux/7.PNG "Logo Title Text 7")

  8 . Plih bahasa yang akan digunakan.
  
![alt text](https://github.com/panagua/PKSJ_Kelompok_x/blob/master/Instalasi-Kali-Linux/8.PNG "Logo Title Text 8")

  9 . Pilih negera tempat tinggalmu.(karena tidak ada pilihan 'Indonesia',maka pilih 'Other')
 
![alt text](https://github.com/panagua/PKSJ_Kelompok_x/blob/master/Instalasi-Kali-Linux/9.PNG "Logo Title Text 9")

  10 . Pilih benua tempat tinggalmu.
  
![alt text](https://github.com/panagua/PKSJ_Kelompok_x/blob/master/Instalasi-Kali-Linux/10.PNG "Logo Title Text 10")

  11 . Pilih negara tempat tinggalmu.
  
![alt text](https://github.com/panagua/PKSJ_Kelompok_x/blob/master/Instalasi-Kali-Linux/11.PNG "Logo Title Text 11")

  12 . Pilih negara yang menjadi basis locale
  
![alt text](https://github.com/panagua/PKSJ_Kelompok_x/blob/master/Instalasi-Kali-Linux/12.PNG "Logo Title Text 12")

  13 . Pilih Keymap yang ingin digunakan
  
![alt text](https://github.com/panagua/PKSJ_Kelompok_x/blob/master/Instalasi-Kali-Linux/13.PNG "Logo Title Text 13")

  14 . Masukkan hostname yang ingin digunakan
  
![alt text](https://github.com/panagua/PKSJ_Kelompok_x/blob/master/Instalasi-Kali-Linux/14.PNG "Logo Title Text 14")

  15 . Masukkan domain yang ingin digunakan

![alt text](https://github.com/panagua/PKSJ_Kelompok_x/blob/master/Instalasi-Kali-Linux/15.PNG "Logo Title Text 15")

  16 . Masukkan password root yang ingin digunakan sebanyak dua kali
  
![alt text](https://github.com/panagua/PKSJ_Kelompok_x/blob/master/Instalasi-Kali-Linux/16.PNG "Logo Title Text 16")

  17 . Pilihlah Time Zone yang sesuai dengan lokasi tempat tinggal
  
![alt text](https://github.com/panagua/PKSJ_Kelompok_x/blob/master/Instalasi-Kali-Linux/17.PNG "Logo Title Text 17")

  18 . Pilihlah opsi untuk mempartisi disk
  
![alt text](https://github.com/panagua/PKSJ_Kelompok_x/blob/master/Instalasi-Kali-Linux/18.PNG "Logo Title Text 18")

  19 . Pilih disk yang akan dipartisi
  
![alt text](https://github.com/panagua/PKSJ_Kelompok_x/blob/master/Instalasi-Kali-Linux/19.PNG "Logo Title Text 19")
 
  20 . Pilih skema partisi yang ingin digunakan
 
![alt text](https://github.com/panagua/PKSJ_Kelompok_x/blob/master/Instalasi-Kali-Linux/20.PNG "Logo Title Text 20")

  21 . Pilih 'Finish partitioning and writes changes to disk'
  
![alt text](https://github.com/panagua/PKSJ_Kelompok_x/blob/master/Instalasi-Kali-Linux/21.PNG "Logo Title Text 21")

  22 . Pilih 'yes' untuk memulai proses partisi
  
![alt text](https://github.com/panagua/PKSJ_Kelompok_x/blob/master/Instalasi-Kali-Linux/22.PNG "Logo Title Text 22")

  23 . Pilih 'yes' untuk menggunakan network mirror
  
![alt text](https://github.com/panagua/PKSJ_Kelompok_x/blob/master/Instalasi-Kali-Linux/23.PNG "Logo Title Text 23")
 
  24 . Masukkan HTTP Proxy jika ada
 
![alt text](https://github.com/panagua/PKSJ_Kelompok_x/blob/master/Instalasi-Kali-Linux/24.PNG "Logo Title Text 24") 

  25 . Pilih 'yes' untuk menginstall GRUB loader
  
![alt text](https://github.com/panagua/PKSJ_Kelompok_x/blob/master/Instalasi-Kali-Linux/25.PNG "Logo Title Text 25")

  26 . Pilih lokasi device yang ingin diinstall GRUB loader
 
![alt text](https://github.com/panagua/PKSJ_Kelompok_x/blob/master/Instalasi-Kali-Linux/26.PNG "Logo Title Text 26")

  27 . Tampilan instalasi selesai,pilih 'continue' untuk melakukan reboot
  
![alt text](https://github.com/panagua/PKSJ_Kelompok_x/blob/master/Instalasi-Kali-Linux/27.PNG "Logo Title Text 27")

  28 . Masukkan username yang sudah dibuat
  
![alt text](https://github.com/panagua/PKSJ_Kelompok_x/blob/master/Instalasi-Kali-Linux/28.PNG "Logo Title Text 28")
 
  29 . Masukkan password

![alt text](https://github.com/panagua/PKSJ_Kelompok_x/blob/master/Instalasi-Kali-Linux/29.PNG "Logo Title Text 29")

  30 . tampilan desktop Kali Linux
  
![alt text](https://github.com/panagua/PKSJ_Kelompok_x/blob/master/Instalasi-Kali-Linux/30.PNG "Logo Title Text 30")




