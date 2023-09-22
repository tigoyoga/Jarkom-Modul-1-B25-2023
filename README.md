# Jarkom-Modul-1-B25-2023

Anggota Kelompok:
- Muhamad Faiz Fernanda (5025211186)
- Tigo S Yoga (5025211125)

## Soal 1
User melakukan berbagai aktivitas dengan menggunakan protokol FTP. Salah satunya adalah mengunggah suatu file.<br />
a. Berapakah sequence number (raw) pada packet yang menunjukkan aktivitas tersebut? <br />
b. Berapakah acknowledge number (raw) pada packet yang menunjukkan aktivitas tersebut? <br />
c. Berapakah sequence number (raw) pada packet yang menunjukkan response dari aktivitas tersebut?<br />
d. Berapakah acknowledge number (raw) pada packet yang menunjukkan response dari aktivitas tersebut?<br />

## Penyelesaian 
![No Image](https://github.com/tigoyoga/Jarkom-Modul-1-B25-2023/blob/main/Image/1.ab.png)

<div align="center">
  <p>Untuk pilihan a dan b</p>
</div>

- Pertama kita melakukan filtering dengan search **ftp contains"STOR"**,dimana di dalam modul tertera mengupload file ke FTP server itu menggunakan kata perintah **STOR**

![No Image](https://github.com/tigoyoga/Jarkom-Modul-1-B25-2023/blob/main/Image/Modul1.png)
- lalu kita klik server tersebut sehingga muncul beberapa pilihan. setelah itu kita memilih pada bagian Transmission Control Protocol lalu akan muncul beberapa informasi yang akan kita gunakan seperti sequence number (raw) dan Acknowledgment number (raw)

![No Image](https://github.com/tigoyoga/Jarkom-Modul-1-B25-2023/blob/main/Image/1.cd.png)
<div align="center">
  <p>Untuk pilihan c dan d</p>
</div>

- Sedangkan untuk mencari yang bagian c dan d (respon) saya mencari filtering dengan **ftp contains “c75-Grab”**,hal ini saya dapatkan dari isi info dari request dan response sama sehingga saya melakukan filtering **c75-Grab k**
 
- Lalu kita klik yang bagian response lalu muncul dari informasi yang akan kita gunakan seperti sequence number (raw) dan Acknowledgment number (raw).

- Berikut bukti ketika mendapatkan flag : 

![No Image](https://github.com/tigoyoga/Jarkom-Modul-1-B25-2023/blob/main/Image/no%201.png)

## Soal 2
Sebutkan web server yang digunakan pada portal praktikum Jaringan Komputer!

## Penyelesaian 
![No Image](https://github.com/tigoyoga/Jarkom-Modul-1-B25-2023/blob/main/Image/2.ab.jpeg)

- Pertama kita melakukan filtering dengan  **http contains “10.21.78.111”**

- lalu kita mencari yang memiliki keterangan ok.

- lalu kita pilih di hypertext nya dan ketemu jawaban dari server yang di gunakan.

- Berikut bukti saya mendapatkan flag:
  ![No Image](https://github.com/tigoyoga/Jarkom-Modul-1-B25-2023/blob/main/Image/no.2.png)

## Soal 3
Dapin sedang belajar analisis jaringan. Bantulah Dapin untuk mengerjakan soal berikut:<br />
a. Berapa banyak paket yang tercapture dengan IP source maupun destination address adalah 239.255.255.250 dengan port 3702?<br />
b. Protokol layer transport apa yang digunakan?<br />
## Penyelesaian
 ![No Image](https://github.com/tigoyoga/Jarkom-Modul-1-B25-2023/blob/main/Image/no.3ab.png)

- Pertama kita melakukan filtering menggunakan **(ip.src == 239.255.255.250 && udp.port == 3702) || (ip.dst == 239.255.255.250 && udp.port == 3702)**
- Dimana hal di atas akan memfilter sesuai keinginan soal,Lalu kita menghitung jumlah ip yang ada, yang mana terdapat 21 paket.
- Sedangkan untuk mencari protocol nya tinggal lihat pada keterangan protocol yang muncul yaitu **UDP**
- Berikut Flag yang saya dapatkan :
   ![No Image](https://github.com/tigoyoga/Jarkom-Modul-1-B25-2023/blob/main/Image/no.3.png)








