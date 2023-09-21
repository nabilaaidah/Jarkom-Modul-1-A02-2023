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

