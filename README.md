# 📖 Laporan Resmi Jaringan Komputer Modul 1 E16 2021 

**Anggota Kelompok:**
 - Ishaq Adheltyo (05111940000167)

## 🏷️ Soal 1: Sebutkan webserver yang digunakan pada "ichimarumaru.tech"!

### ✍️ Langkah-Langkah Pengerjaan:
1. Isi wireshark display filter dengan **http.host eq "ichimarumaru.tech"**
![soal-1-1](https://user-images.githubusercontent.com/49280352/134523005-a2376f1b-9613-4581-905c-7d371beea26b.png)

2. Pilih salah satu (pilih yang Info GET / HTTP/1.1 karena ini webnya) dan klik kanan untuk follow http request
3. Search keyword "server"
![soal-1-2](https://user-images.githubusercontent.com/49280352/134523109-fba70b5a-6dad-4c71-906a-c0a25d922dd4.png)

### 🔑 Jawaban:
 - Filter Wireshark Expression: **http.host eq "ichimarumaru.tech"**
 - Server: **nginx/1.18.0 (Ubuntu)**

## 🏷️ Soal 2: Temukan paket dari web-web yang menggunakan basic authentication method!

### ✍️ Langkah-Langkah Pengerjaan:
1. Isi wireshark display filter dengan **http.authorization contains Basic**
![soal-2](https://user-images.githubusercontent.com/49280352/134523975-6896a5bc-6373-4e1a-b2b0-9a92b8e913e4.png)

### 🔑 Jawaban:
 - Filter Wireshark Expression: **http.authorization contains Basic**

## 🏷️ Soal 3: Ikuti perintah di basic.ichimarumaru.tech! Username dan password bisa didapatkan dari file .pcapng!

### ✍️ Langkah-Langkah Pengerjaan:
1. Isi wireshark display filter dengan **http.host eq “basic.ichimarumaru.tech”**
2. Lihat pada Hypertext **Transfer Protocol > Authorization > Credentials** untuk menemukan username dan password
![soal-3-1](https://user-images.githubusercontent.com/49280352/134525778-c607d646-91a8-4d81-adfd-458ec2f58fe0.png)

3. Buka Website basic.ichimarumaru.text kemudian login dengan username dan password yang telah didapatkan

### 🔑 Jawaban:
 - Filter Wireshark Expression: **http.authorization contains Basic**
 - Screenshot Perintah pada Website:
   ![soal-3-2](https://user-images.githubusercontent.com/49280352/134525812-98e50824-0447-4e56-818f-8d1052d1c007.png)


## 🏷️ Soal 4: Temukan paket mysql yang mengandung perintah query select!

### ✍️ Langkah-Langkah Pengerjaan:
1. Isi wireshark display filter dengan **mysql.query contains "select"**
![soal-4-1](https://user-images.githubusercontent.com/49280352/134526511-83b163ca-d5b9-44a6-9e87-6b3928d3edb5.png)

### 🔑 Jawaban:
 - Filter Wireshark Expression: **mysql.query contains "select"**

## 🏷️ Soal 5: Login ke portal.ichimarumaru.tech kemudian ikuti perintahnya! Username dan password bisa didapat dari query insert pada table users dari file .pcap!

### ✍️ Langkah-Langkah Pengerjaan:
1. Isi wireshark display filter dengan **mysql.query contains "INSERT"**
2. Dapatkan username dan password pada **MYSQL Protocol > Request Command Query > Statement **
![soal-5-1](https://user-images.githubusercontent.com/49280352/134527632-be1549c5-3935-436a-9282-4f2706a0f1d7.png)

3. Login ke portal.ichimarumaru.tech dan ikuti perintahnya

### 🔑 Jawaban:
 - Filter Wireshark Expression: **mysql.query contains "INSERT"**
 - Screenshot Perintah pada Website:
   ![soal-5-2](https://user-images.githubusercontent.com/49280352/134527654-67a46ea8-69e2-48cd-84e6-ddb658c0cf48.png)

## 🏷️ Soal 6: Cari username dan password ketika melakukan login ke FTP Server!

### ✍️ Langkah-Langkah Pengerjaan:
1. Isi wireshark display filter dengan **ftp.request.command eq "USER"**
![soal-6-1](https://user-images.githubusercontent.com/49280352/134529414-2854139d-82cd-4023-a664-61b11c17a6ba.png)

2. Isi wireshark display filter dengan **ftp.request.command eq "PASS"**
![soal-6-2](https://user-images.githubusercontent.com/49280352/134529442-16dfa2cf-c1cc-436e-97c9-77eb6d2f021b.png)

### 🔑 Jawaban:
 - Filter Wireshark Expression: **ftp.request.command eq "USER"** & **ftp.request.command eq "PASS"**
 - Username: **secretuser**
 - Password: **aku.pengen.pw.aja**

## 🏷️ Soal 7: Ada 500 file zip yang disimpan ke FTP Server dengan nama 0.zip, 1.zip, 2.zip, ..., 499.zip. Simpan dan Buka file pdf tersebut. (Hint = nama pdf-nya "Real.pdf")

### ✍️ Langkah-Langkah Pengerjaan:
1. Isi wireshark display filter dengan **frame contains "Real.pdf"**
![soal-7-1](https://user-images.githubusercontent.com/49280352/134530145-f7bb867a-44e3-4f10-af79-0b7d53ab72ae.png)

2. Follow TCP Stream
3. Ganti Show data as RAW
4. Save as file.zip
![soal-7-2](https://user-images.githubusercontent.com/49280352/134530186-add30a57-3a69-4b6d-8e17-19b8dff2ed5d.png)

5. Extract dan lihat filenya
![soal-7-3](https://user-images.githubusercontent.com/49280352/134530202-f23448cb-b30e-495a-af08-97cc1503c9f1.png)

### 🔑 Jawaban:
 - Filter Wireshark Expression: **frame contains "Real.pdf"**

## 🏷️ Soal 8: Cari paket yang menunjukan pengambilan file dari FTP tersebut!

### ✍️ Langkah-Langkah Pengerjaan:
1. Isi wireshark display filter dengan **ftp.request.command eq "RETR"**
![image](https://user-images.githubusercontent.com/49280352/134530929-9b072648-d814-4632-8b3d-c748f4b94e84.png)

### 🔑 Jawaban:
 - Filter Wireshark Expression: **ftp.request.command eq "RETR"**

## 🏷️ Soal 9: Dari paket-paket yang menuju FTP terdapat indikasi penyimpanan beberapa file. Salah satunya adalah sebuah file berisi data rahasia dengan nama "secret.zip". Simpan dan buka file tersebut!

### ✍️ Langkah-Langkah Pengerjaan:
1. Isi wireshark display filter dengan **ftp-data**
![image](https://user-images.githubusercontent.com/49280352/134531585-a1ca18da-1b9f-4794-858c-b1e602fbeccb.png)

2. Follow TCP Stream
3. Show data as RAW
4. Save as secret.zip
5. Buka File secret.zip yang telah di download tadi
![image](https://user-images.githubusercontent.com/49280352/134531865-1e9b11ea-540d-4684-8266-2657f62337a0.png)

### 🔑 Jawaban:
 - Filter Wireshark Expression: **ftp-data**
 - Isi File: **Wanted.pdf dan dilock sebuah password**
