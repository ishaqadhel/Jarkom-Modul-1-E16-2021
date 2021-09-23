# 📖 Laporan Resmi Jaringan Komputer Modul 1 E16 2021 

**Anggota Kelompok:**
 - Ishaq Adheltyo (05111940000167)

## 📍 Soal 1: Sebutkan webserver yang digunakan pada "ichimarumaru.tech"!

### ✍️ Langkah-Langkah Pengerjaan:
1. Isi wireshark display filter dengan **http.host eq "ichimarumaru.tech"**
![soal-1-1](https://user-images.githubusercontent.com/49280352/134523005-a2376f1b-9613-4581-905c-7d371beea26b.png)

2. Pilih salah satu (pilih yang Info GET / HTTP/1.1 karena ini webnya) dan klik kanan untuk follow http request
3. Search keyword "server"
![soal-1-2](https://user-images.githubusercontent.com/49280352/134523109-fba70b5a-6dad-4c71-906a-c0a25d922dd4.png)

### 🔑 Jawaban:
 - Filter Wireshark Expression: **http.host eq "ichimarumaru.tech"**
 - Server: **nginx/1.18.0 (Ubuntu)**
