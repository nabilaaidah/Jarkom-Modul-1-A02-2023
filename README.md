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


# Nomor 3
3. Dapin sedang belajar analisis jaringan. Bantulah Dapin untuk mengerjakan soal berikut:

    a. Berapa banyak paket yang tercapture dengan IP source maupun destination address adalah 239.255.255.250 dengan port 3702?

    b. Protokol layer transport apa yang digunakan?

## Jawaban

### 3a. Berapa banyak paket yang tercapture dengan IP source maupun destination address adalah 239.255.255.250 dengan port 3702?

