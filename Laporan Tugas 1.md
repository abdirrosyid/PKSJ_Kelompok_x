# Laporan Tugas 1 PKSJ Kelompok 13

Anggota Kelompok:
Andre Abdirrosyid (5112100186)
Muhammad Adnan Yusuf (5113100001)
Adian Latifa Nurrohman (5113100031)
Tomson Panagua Krisasandi Pangaribuan (5113100048)

PENDAHULUAN
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

LANDASAN TEORI
1.	OS yang digunakan
a.	Ubuntu Server
Ubuntu Server adalah sistem operasi turunan dari Linux Ubuntu yang didesain khusus dengan kernel yang telah dikustomisasi untuk bekerja sebagai sistem operasi server.
b.	Kali Linux
Kali Linux adalah sebuah distro linux yang dikembangkan oleh Offensive Security yang mempunyai fungsi untuk kebutuhan professional penetration tester.

2.	Tools yang digunakan
Attacking Tools
- THC Hydra
THC-Hydra adalah sebuah tools untuk security tester dengan mencoba semua password yangk ita siapkan dalam sebuah list atau yang kita tentukan sebelumnya. Lebih tepatnya dengan menggunakan teknik bruteforce.

- Ncrack
Ncrack adalah sebuah tool untuk membobol proses autentikasi dari suatu jaringan dengan kecepatan tinggi. Perusahaan biasanya menggunakan tool ini untuk melakukan tes pada host dan perangkat suatu jaringan yang menggunakan password yang lemah.

Defending Tools
- Fail2ban
Fail2ban adalah package keamanan yang digunakan untuk mencegah serangan bruteforce dan DDoS pada linux.


UJI PENETRASI 1
1.	Installasi Ubuntu Server


![alt text](https://github.com/panagua/PKSJ_Kelompok_x/blob/master/Instalasi-Kali-Linux/1.PNG "Logo Title Text 1")

