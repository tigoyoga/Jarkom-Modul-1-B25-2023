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
- Pertama kita melakukan filtering dengan search **ftp contains STOR** dimana di dalam modul tertera mengupload file ke FTP server itu menggunakan kata perintah **STOR**

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





