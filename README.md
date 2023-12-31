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

- Sedangkan untuk mencari yang bagian c dan d (respon) saya mencari filtering dengan **ftp contains “c75-Grab”**,hal ini saya dapatkan dari isi info dari request dan response sama sehingga saya melakukan filtering **c75-Grab**
 
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

## Soal 4
Berapa nilai checksum yang didapat dari header pada paket nomor 130?
## Penyelesaian
![no-4](https://github.com/tigoyoga/Jarkom-Modul-1-B25-2023/assets/88433109/0b4574bb-6533-4e16-932d-230bc224a6c2)

- Cari paket no 130, bisa dengan scroll manual atau dengan query filter `frame.number == 130`.
- Buka Detail dari paket tersebut.
- Klik pada bagian header **User Datagram Protocol**.
- Terdapat nilai checksum yaitu `0x18e5`.

- Bukti flag :
![image](https://github.com/tigoyoga/Jarkom-Modul-1-B25-2023/assets/88433109/bdeb99ff-c0b6-482f-a696-e3ed75934ad1)


## Soal 5
Elshe menemukan suatu file packet capture yang menarik. Bantulah Elshe untuk menganalisis file packet capture tersebut.
  a. Berapa banyak packet yang berhasil di capture dari file pcap tersebut?
  b. Port berapakah pada server yang digunakan untuk service SMTP?
  c. Dari semua alamat IP yang tercapture, IP berapakah yang merupakan public IP?

## Penyelesaian
- Terdapat 2 file yaitu file .zip yang berisi connext.txt dan memerlukan sebuah password, dan file pcap untuk mencari password tersebut.
- Pilih paket nomor 25 dan klik analisis TCP Stream.
![image](https://github.com/tigoyoga/Jarkom-Modul-1-B25-2023/assets/88433109/78f17141-98a1-4c03-a89b-d87315062dad)
- Pada paket tersebut ditemukan sebuah password `NWltcGxlUGFzNXdvcmQ=`, namun kita harus decode dengan base64.
- Setelah di decode, menghasilkan string `5implePas5word`.
![image](https://github.com/tigoyoga/Jarkom-Modul-1-B25-2023/assets/88433109/690cb9d8-71da-49fe-b9f4-d214e21b16f1)
- Setelah membuka `connect.txt` dengan password diatas, berikut isi filenya.
![image](https://github.com/tigoyoga/Jarkom-Modul-1-B25-2023/assets/88433109/e66baffc-5d36-4782-92fe-8dab8975e764)
- Untuk menjawab soal pertama, yaitu berapa banyak packet, kita buka file pcap dan terlihat jumlah total packet pada bagian pojok kanan bawah, yaitu `packets : 60 - Displayed : 60`
![image](https://github.com/tigoyoga/Jarkom-Modul-1-B25-2023/assets/88433109/4aa6704a-13d9-4da2-b32a-dc45ff697e57)
- Untuk menjawab soal kedua, yaitu port berapa yang digunakan service SMTP, kita bisa memilih salah satu paket yang memiliki protocol `SMTP`, lalu klik detail pada bagian Transmission Control Protocol, dan tertulis `Source Port : 25`.
![image](https://github.com/tigoyoga/Jarkom-Modul-1-B25-2023/assets/88433109/dbf22f38-f601-4f74-9ca8-9ac55d454d40)
- Untuk menjawab soal ketiga, yaitu berapakah yang merupakan public IP, kita bisa melihat range public IP yaitu selain `10.x.x.x` dan `192.x.x.x`, jadi jawabannya adalah `74.53.140.153`.

- Bukti flag :
![limaaa](https://github.com/tigoyoga/Jarkom-Modul-1-B25-2023/assets/88433109/83d731fb-bd69-48ef-ae68-fbdb13296d8b)

## Soal 6 
Soal 6-7 menggunakan file pcap yang sama. Seorang anak bernama Udin Berteman dengan SlameT yang merupakan seorang penggemar film detektif. sebagai teman yang baik, Ia selalu mengajak slamet untuk bermain valoranT bersama. suatu malam, terjadi sebuah hal yang tak terdUga. ketika udin mereka membuka game tersebut, laptop udin menunjukkan sebuah field text dan Sebuah kode Invalid bertuliskan "server SOURCE ADDRESS 7812 is invalid". ketika ditelusuri di google, hasil pencarian hanya menampilkan a1 e5 u21. jiwa detektif slamet pun bergejolak. bantulah udin dan slamet untuk menemukan solusi kode error tersebut.

## Penyelesaian 
- Pertama melakukan filtering **frame.number==7812**
- lalu kita klik pilihan ip tersebut,lalu muncul informasi ip source nya
![No Image](https://github.com/tigoyoga/Jarkom-Modul-1-B25-2023/blob/main/Image/6.png)
- Setelah itu kita melakukan _Decrypt_ pada ip source nya
   - 10 = J
   - 4 = D
   - 18 = R
   - 14 = N
   - 10 = J
   - 1 = A
- Dan hasilnya yaitu **JDRNJA**
- Berikut bukti flag:
  ![No Image](https://github.com/tigoyoga/Jarkom-Modul-1-B25-2023/blob/main/Image/soal%20no%206.a.png)

## Soal 7
Berapa jumlah packet yang menuju IP 184.87.193.88?

## Penyelesaian
- Untuk mengetahui jumlah paket yang menuju suatu IP, kita bisa menggunakan query filter `ip.dst == 184.87.193.88` yang menampilkan paket dengan ip destination 184.87.193.88.
- Hasilnya yaitu terdapat 6 paket.
![image](https://github.com/tigoyoga/Jarkom-Modul-1-B25-2023/assets/88433109/67e8d0f0-23b5-4a23-8271-f9e4302e70c0)

- Bukti flag :
![tujuhh](https://github.com/tigoyoga/Jarkom-Modul-1-B25-2023/assets/88433109/c5269f9f-0969-4085-a3ca-db5ac20f74b0)

## Soal 8
Berikan kueri filter sehingga wireshark hanya mengambil semua protokol paket yang menuju port 80! (Jika terdapat lebih dari 1 port, maka urutkan sesuai dengan abjad).

## Penyelesaian
- Untuk mengambil paket yang menuju port 80 kita bisa menggunakan query filter sesuai perintah soal yaitu `tcp.dstport == 80 || udp.dstport == 80` yang berarti melihat semua paket yang dikirim atau diterima oleh perangkat yang menggunakan port 80 baik melalui protokol TCP maupun UDP.

- Bukti flag :
  ![image](https://github.com/tigoyoga/Jarkom-Modul-1-B25-2023/assets/88433109/d71c961b-da34-4677-907b-d3616a4152fe)


## Soal 9
Berikan kueri filter sehingga wireshark hanya mengambil paket yang berasal dari alamat 10.51.40.1 tetapi tidak menuju ke alamat 10.39.55.34!

## Penyelesaian
- Untuk mengambil paket yang berasal dan menuju dari suatu alamat, kita bisa menggunakan query filter `ip.src == 10.51.40.1 && ip.dst != 10.39.55.34` yang berarti melihat semua paket yang dikirim dari alamat IP 10.51.40.1 ke alamat IP selain 10.39.55.34.

- Bukti flag :
![image](https://github.com/tigoyoga/Jarkom-Modul-1-B25-2023/assets/88433109/9853ac60-cb92-4be2-a352-968bd35fd0f0)

## Soal 10
Sebutkan kredensial yang benar ketika user mencoba login menggunakan Telnet.

## Penyelesaian
- Untuk menampilkan paket yang memiliki protocol telnet, kita query filter `telnet`.
- Setelah dicoba satu per satu dengan analyze TCP Stream atau bisa melihat detail -> Telnet, maka ditemukan string sesuai format [username]:[password], yaitu `dhafin:kesayangannyak0k0`.
![image](https://github.com/tigoyoga/Jarkom-Modul-1-B25-2023/assets/88433109/6e95b73f-b904-4d79-8461-45df3fec7a69)

- Bukti flag :
![image](https://github.com/tigoyoga/Jarkom-Modul-1-B25-2023/assets/88433109/7df065f6-1995-4160-b23b-c3c88e20da20)










