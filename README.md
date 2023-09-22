# Jarkom-Modul-1-A02-2023
<table>
    <tr>
        <th colspan=2> Kelompok A02 </th>
    </tr>
    <tr>
        <th>NRP</th>
        <th>Nama Anggota</th>
    </tr>
    <tr>
        <td>5025211032</td>
        <td>Nabila A'idah Diani</td>
    </tr>
</table>


# Nomor 1
1. User melakukan berbagai aktivitas dengan menggunakan protokol FTP. Salah satunya adalah mengunggah suatu file.
   
    a. Berapakah sequence number (raw) pada packet yang menunjukkan aktivitas tersebut? 
    
    b. Berapakah acknowledge number (raw) pada packet yang menunjukkan aktivitas tersebut? 
    
    c. Berapakah sequence number (raw) pada packet yang menunjukkan response dari aktivitas tersebut?
    
    d. Berapakah acknowledge number (raw) pada packet yang menunjukkan response dari aktivitas tersebut?

## Jawaban

Pada nomor ini, terdapat informasi bahwa ada aktivitas dengan protokol FTP dan mengunggah suatu file, maka langkah pertama yang dilakukan adalah menuliskan
```
ftp
```
pada filtering
![image](https://github.com/nabilaaidah/Jarkom-Modul-1-A02-2023/assets/110476969/63b58dc5-8c3b-4b5d-b248-440d4bbf6880)

Setelah itu, mencari packet yang mengunggah suatu file, dan dapat ditemukan pada packet no 147 terdapat aktivitas pengunggahan file

![image](https://github.com/nabilaaidah/Jarkom-Modul-1-A02-2023/assets/110476969/995ef19e-8f10-4488-9a39-584a82e46207)

### 1a. Berapakah sequence number (raw) pada packet yang menunjukkan aktivitas tersebut?

Sequence number (raw) terlihat saat packet diklik

![image](https://github.com/nabilaaidah/Jarkom-Modul-1-A02-2023/assets/110476969/7dd10a95-bca9-4755-a3fc-d69ef9cdda39)

### 1b. Berapakah acknowledge number (raw) pada packet yang menunjukkan aktivitas tersebut? 

Acknowledge number (raw) terlihat saat packet diklik

![image](https://github.com/nabilaaidah/Jarkom-Modul-1-A02-2023/assets/110476969/56f634e9-b246-4be5-b819-819ebc9aa2e5)

### 1c. Berapakah sequence number (raw) pada packet yang menunjukkan response dari aktivitas tersebut?

Sequence number (raw) dari response aktivitas tersebut dapat terlihat dari packet 149

![image](https://github.com/nabilaaidah/Jarkom-Modul-1-A02-2023/assets/110476969/002c337c-c4aa-4fb3-9a8e-c49ee95222ef)

Sequence number (raw) terlihat saat packet diklik

![image](https://github.com/nabilaaidah/Jarkom-Modul-1-A02-2023/assets/110476969/8728784c-6ace-42e1-83aa-5bf4fc0996f6)

### 1d. Berapakah acknowledge number (raw) pada packet yang menunjukkan response dari aktivitas tersebut?

Acknowledge number (raw) terlihat saat packet diklik

![image](https://github.com/nabilaaidah/Jarkom-Modul-1-A02-2023/assets/110476969/3c6e61f2-0b05-40b8-8ad1-4cf5f6c35ebc)


Berikut adalah hasilnya

![image](https://github.com/nabilaaidah/Jarkom-Modul-1-A02-2023/assets/110476969/a4c82bfe-2fca-4201-997e-4a81163e8a24)

![image](https://github.com/nabilaaidah/Jarkom-Modul-1-A02-2023/assets/110476969/b8e1a8fd-4653-4eed-b20b-be3a962be417)


# Nomor 2
2. Sebutkan web server yang digunakan pada portal praktikum Jaringan Komputer!

## Jawaban

Langkah awal yang dapat dilakukan adalah mencari packet melalui jaringan yang ada dari OpenVPN

![image](https://github.com/nabilaaidah/Jarkom-Modul-1-A02-2023/assets/110476969/ba727543-bbaa-415d-b96f-f0e88ac1c9db)

Langkah selanjutnya adalah mencari protokol HTTP pada filtering lalu klik pada packet yang menunjukkan aktivitas portal praktikum Jaringan Komputer

![image](https://github.com/nabilaaidah/Jarkom-Modul-1-A02-2023/assets/110476969/5ad47036-4be0-4423-bef7-71e5a8a6b2ba)

Langkah berikutnya adalah klik follow lalu cari HTTP stream. Setelah itu, klik pada HTTP stream dan akan terbuka pop up seperti berikut

![image](https://github.com/nabilaaidah/Jarkom-Modul-1-A02-2023/assets/110476969/a49ef58e-458a-4300-91ba-4600beaed00a)

Lalu, terlihat nama server adalah `gunicorn`

Berikut adalah hasilnya

![image](https://github.com/nabilaaidah/Jarkom-Modul-1-A02-2023/assets/110476969/45ac0147-1436-460d-abe9-32dfdab2e64f)

![image](https://github.com/nabilaaidah/Jarkom-Modul-1-A02-2023/assets/110476969/84ed4cf1-87ef-47fa-9fef-7437ce1294e4)

# Nomor 3
3. Dapin sedang belajar analisis jaringan. Bantulah Dapin untuk mengerjakan soal berikut:

    a. Berapa banyak paket yang tercapture dengan IP source maupun destination address adalah 239.255.255.250 dengan port 3702?

    b. Protokol layer transport apa yang digunakan?

## Jawaban

### 3a. Berapa banyak paket yang tercapture dengan IP source maupun destination address adalah 239.255.255.250 dengan port 3702?

Langkah pertama yang dilakukan adalah filtering dengan menggunakan
```
(ip.dst==239.255.255.250 || ip.src==239.255.255.250) && udp.port==3702
```
![image](https://github.com/nabilaaidah/Jarkom-Modul-1-A02-2023/assets/110476969/74a80cff-08df-44a3-b43a-71ca93f353ca)

Langkah selanjutnya adalah masuk ke statistic lalu ke endpoint untuk melakukan cek jumlah packet yang tercapture sehingga dapat diketahui terdapat 21 packet

![image](https://github.com/nabilaaidah/Jarkom-Modul-1-A02-2023/assets/110476969/eee71fa9-5314-43ac-9d42-8175ce783c1b)

### 3b. Protokol layer transport apa yang digunakan?

Dapat diketahui bahwa protokol layer yang digunakan adalah UDP

Berikut adalah hasilnya

![image](https://github.com/nabilaaidah/Jarkom-Modul-1-A02-2023/assets/110476969/6bb572c4-8ec6-4a9e-9c17-1b84d87db3b9)

![image](https://github.com/nabilaaidah/Jarkom-Modul-1-A02-2023/assets/110476969/d7122295-cbd8-4355-85f7-243501e9df9b)

# Nomor 4

4. Berapa nilai checksum yang didapat dari header pada paket nomor 130?

## Jawaban

Langkah pertama adalah mencari packet dengan nomor 130

![image](https://github.com/nabilaaidah/Jarkom-Modul-1-A02-2023/assets/110476969/fdc807f4-ef92-47f1-91c1-c14892d59bf7)

Langkah kedua adalah mencari checksum

![image](https://github.com/nabilaaidah/Jarkom-Modul-1-A02-2023/assets/110476969/1f0716bf-0381-431b-85b9-4f3ddc4f2d58)

Berikut adalah hasilnya

![image](https://github.com/nabilaaidah/Jarkom-Modul-1-A02-2023/assets/110476969/aae4eeab-43b8-4e4e-9e10-34995686e7e6)

![image](https://github.com/nabilaaidah/Jarkom-Modul-1-A02-2023/assets/110476969/78719126-fa57-4838-b50b-8e3ca6bb4abd)

# Nomor 5

5.Elshe menemukan suatu file packet capture yang menarik. Bantulah Elshe untuk menganalisis file packet capture tersebut.
    a. Berapa banyak packet yang berhasil di capture dari file pcap tersebut?
    b. Port berapakah pada server yang digunakan untuk service SMTP?
    c. Dari semua alamat IP yang tercapture, IP berapakah yang merupakan public IP?

## Jawaban

Dikarenakan belum terdapat netcat, maka kita harus mencari nc nya terlebih dahulu. Di dalam soal terdapat file unzip yang akan me-lead ke dalam nc yang dicari. Namun, untuk membuka file tersebut, diharuskan bisa melakukan unlock dengan password

![image](https://github.com/nabilaaidah/Jarkom-Modul-1-A02-2023/assets/110476969/8cb38ded-89b1-452b-8a5c-f2cd27b9bbd2)

Untuk mendapatkan password tersebut, maka kita akan mencari packet dengan protocol smtp pada file pcap

![image](https://github.com/nabilaaidah/Jarkom-Modul-1-A02-2023/assets/110476969/c30034e4-4ae0-416e-a5e7-dfa442cf30e6)

Setalah itu, pilih salah satu packet dan buka tcp streamnya, dan dapat terlihat bahwa terdapat password mencurigakan

![image](https://github.com/nabilaaidah/Jarkom-Modul-1-A02-2023/assets/110476969/31dbc76c-fbb4-49a3-b05c-9332496a5e43)

Mengikuti perintah yang terdapat pada tcp stream, password di-decode dan didapatkan `5implePas5word` lalu dimasukkan untuk melakukan unlock. Dan hasilnya mengarah dengan nc yang dipakai pada soal ini

![image](https://github.com/nabilaaidah/Jarkom-Modul-1-A02-2023/assets/110476969/9194bbd8-9ea3-4e74-9e8b-7020a3976849)

### 5a. Berapa banyak packet yang berhasil di capture dari file pcap tersebut?

Pada file pcap terlihat terdapat 60 packet yang tercapture

![image](https://github.com/nabilaaidah/Jarkom-Modul-1-A02-2023/assets/110476969/97dfeb46-5da3-4a32-a916-35c59cb59b93)

### 5b. Port berapakah pada server yang digunakan untuk service SMTP?

Port default yang digunakan untuk service SMTP adalah `25`

### 5c. Dari semua alamat IP yang tercapture, IP berapakah yang merupakan public IP?

Pada packet yang ditujukan terdapat ip src dan dst seperti berikut

![image](https://github.com/nabilaaidah/Jarkom-Modul-1-A02-2023/assets/110476969/406b947c-6426-494a-a7cc-05f0e14f1184)

Dari kedua ip tersebut, dapat diketahui bahwa ip publicnya adalah `74.53.140.153` dikarenakan juga ip private ranging dari berikut

![image](https://github.com/nabilaaidah/Jarkom-Modul-1-A02-2023/assets/110476969/06cfe61d-52c8-4b54-8892-0e8614a85687)

Hasilnya adalah sebagai berikut

![image](https://github.com/nabilaaidah/Jarkom-Modul-1-A02-2023/assets/110476969/c8ddd6d4-03e0-4abb-a131-5705c6678a97)

![image](https://github.com/nabilaaidah/Jarkom-Modul-1-A02-2023/assets/110476969/74c0f417-4fc9-45b0-8da0-1624be7ac780)


# Nomor 6

6. Seorang anak bernama Udin Berteman dengan SlameT yang merupakan seorang penggemar film detektif. sebagai teman yang baik, Ia selalu mengajak slamet untuk bermain valoranT bersama. suatu malam, terjadi sebuah hal yang tak terdUga. ketika udin mereka membuka game tersebut, laptop udin menunjukkan sebuah field text dan Sebuah kode Invalid bertuliskan "server SOURCE ADDRESS 7812 is invalid". ketika ditelusuri di google, hasil pencarian hanya menampilkan a1 e5 u21. jiwa detektif slamet pun bergejolak. bantulah udin dan slamet untuk menemukan solusi kode error tersebut.

Beserta hint:

![image](https://github.com/nabilaaidah/Jarkom-Modul-1-A02-2023/assets/110476969/325c736f-e050-4cce-9384-0e8895f5b2de)

## Jawaban

Pada soal terdapat tulisan bahwa `server SOURCE ADDRESS 7812 is invalid`, sehingga hal pertama yang dapat dilakukan adalah mencari packet bernomor 7812

![image](https://github.com/nabilaaidah/Jarkom-Modul-1-A02-2023/assets/110476969/b7a5a121-94ae-4a80-9406-849625d58630)

Dikarenakan pada hint tertulis bahwa source address adalah kunci, maka dapat dilihat bahwa source addressnya adalah 104.18.14.101. Lalu, pada hint kedua dan ketiga merupakan hint terdapat cypher a1z26 dengan rentang A-R dan 1-18 yang berarti A = 1, B = 2, dst sampai dengan R = 18. Pada hint juga tertulis bahwa jawabannya 6 huruf sehingga source address dapat dipenggal menjadi 10 4 18 14 10 1 yang jika dicypher menjadi JDRNJA.

Berikut merupakan hasilnya

![image](https://github.com/nabilaaidah/Jarkom-Modul-1-A02-2023/assets/110476969/fb60eeea-1120-4776-8eae-189d55d291b2)

![image](https://github.com/nabilaaidah/Jarkom-Modul-1-A02-2023/assets/110476969/b32b00ef-6a87-4ab0-9bf9-7733c2da5d46)


# Nomor 7
7. Berapa jumlah packet yang menuju IP 184.87.193.88?

## Jawaban 

Hal pertama yang dilakukan adalah melakukan filtering dengan `ip.dst==184.87.193.88`, lalu lihat jumlah packet dengan jara ke statistic > endpoint

![image](https://github.com/nabilaaidah/Jarkom-Modul-1-A02-2023/assets/110476969/3aa9f1c3-d30a-4a77-a53a-410d7f5ef7ef)

Berikut merupakan hasilnya

![image](https://github.com/nabilaaidah/Jarkom-Modul-1-A02-2023/assets/110476969/3600761b-c9cc-4e14-8967-34f60858ac9c)


# Nomor 8
8. Berikan kueri filter sehingga wireshark hanya mengambil semua protokol paket yang menuju port 80! (Jika terdapat lebih dari 1 port, maka urutkan sesuai dengan abjad)

## Jawaban

Dalam mengambil semua protokol paket yang menuju port 80 dapat dilakukan dengan filtering `tcp.dstport==80 || udp.dstport==80`

![image](https://github.com/nabilaaidah/Jarkom-Modul-1-A02-2023/assets/110476969/30e583fd-76df-4185-a864-39d13c2e9bc0)

Berikut merupakan hasilnya

![image](https://github.com/nabilaaidah/Jarkom-Modul-1-A02-2023/assets/110476969/d3a76055-8e26-4737-a02a-a766726cb1a0)


# Nomor 9

9. Berikan kueri filter sehingga wireshark hanya mengambil paket yang berasal dari alamat 10.51.40.1 tetapi tidak menuju ke alamat 10.39.55.34!

## Jawaban

Masukkan `ip.src==10.51.40.1 && ip.dst!=10.39.55.34` untuk filtering

![image](https://github.com/nabilaaidah/Jarkom-Modul-1-A02-2023/assets/110476969/342c9c81-05a4-4a5d-be77-09bdbc3b80e4)

Berikut merupakan hasilnya

![image](https://github.com/nabilaaidah/Jarkom-Modul-1-A02-2023/assets/110476969/063322fb-540e-4d48-a7af-8f88e809ffb4)


# Nomor 10

10. Sebutkan kredensial yang benar ketika user mencoba login menggunakan Telnet

## Jawaban

Langkah pertama adalah mencari packet dengan protokol telnet yang memiliki kredensial

![image](https://github.com/nabilaaidah/Jarkom-Modul-1-A02-2023/assets/110476969/50513e4c-3238-487a-ad67-42f264185b21)

Dan dari tcp stream tersebut dapat diketahui username dan passwordnya

Berikut merupakan hasilnya

![image](https://github.com/nabilaaidah/Jarkom-Modul-1-A02-2023/assets/110476969/b67da66a-ca27-4480-893a-0af2033ddfc9)


# Kendala
- Jawaban ternyata case sensitive, sehingga jawaban yang benar harus diinput berkali2 karena tidak sesuai dengan yang diinginkan.
- Terdapat jawaban yang benar dengan penulisan yang sama, tapi satu ditolak dan satunya diterima.

Yang ditolak:

![image](https://github.com/nabilaaidah/Jarkom-Modul-1-A02-2023/assets/110476969/2ca78134-29d1-4872-9752-fe4f3efd0958)

Yang diterima:

![image](https://github.com/nabilaaidah/Jarkom-Modul-1-A02-2023/assets/110476969/eac5eb0d-5602-4cba-b84c-4b5f3c4a5280)

- Melakukan pendownloadan file, tetapi file yang didownload tidak lengkap dan saat didownload kedua kalinya baru lengkap

Yang tidak lengkap:

![image](https://github.com/nabilaaidah/Jarkom-Modul-1-A02-2023/assets/110476969/1ebb4e15-eb09-4f15-9929-310329aa750a)

Yang lengkap:

![image](https://github.com/nabilaaidah/Jarkom-Modul-1-A02-2023/assets/110476969/98078c9b-6c9d-4f58-b369-6ebbab10b975)



