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

1.	Installasi Ubuntu Server

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
