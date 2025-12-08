Tanggal: 8 Desember 2025
Topik: Cryptography

---

## 🎯 Tujuan Belajar Hari Ini
- Memahami apaitu Kriptografi secara konseptual dan praktis, dapat membedapak apaitu
  Symmetric vs Asymmetric encryption, serta bisa membedakan Encodeing, Encryption, dan Hashing.

---

## 🧠 Teori Inti (Versi Singkat + Padat)
- kriptografi adalah suatu kegiatan mengamankan informasi atau data agar tidak dapat dibaca
  atau dilihat oleh sembarangan orang, kriptografi ini bisa kita analogikan sebagai proses kantor
  pos mengirimkan surat yang kita titipkan. kriptografi disini aku analogikan sebagai amplop,
  tanpa kriptografi atau enkripsi, surat yang di kirim lewat kantor pos dapat dibaca oleh oranglain
  dan bahkan oranglain dapat mengubah isinya tanpa kita ketahui, oleh karena itu peran kriptografi disini
  adalah sebagai pembungkus supaya data kita aman dan tetap privat sampai tujuan.

---

## 🔧 Tools yang Digunakan
- Terminal/Shell

---

## 🧪 Praktik / Lab
### 1. Setup
Langkah awal:
- OS : `Linux Mint`
- Tools : `Comand Shell`

### 2. Eksekusi

#### Encoding & Decoding Base64
- Encode : `echo "belajar-crypto" | base64`
    -> Hasil : YmVsYWphci1jcnlwdG8K

- Decode : `echo "YmVsYWphci1jcnlwdG8" | base64 -d`
    -> Hasil : belajar-crypto

#### Hashing MD5 & SHA256
- MD5 : `echo -n "password123" | md5sum`
    -> Hasil : 482c811da5d5b4bc6d497ffa98491e38  -

- SHA256 : `echo -n "password123" | sha256sum`
    -> Hasil : ef92b778bafe771e89245b89ecbc08a44a4e166c06659911881f383d4473e94f  -

#### *Perbandingan*
- md5 dan sha256 menghasilkan output yang berbeda.
- sha256 membuat sebuah hash yang lebih panjang dibandingkan denggan md5.
- Jika salah satu huruf di ubah maka hash yang dihasilkan akan berubah signifikan,
  contohnya pada sha256 pada kata "password123" denggan hasil hash 
  `ef92b778bafe771e89245b89ecbc08a44a4e166c06659911881f383d4473e94f  -`
  saat aku ganti menjadi "pxssword123" maka hash yang dihasilkan adalah `dfe7c935cca97894e8a9a796539994b898f9b03edfdf91f0de6dd9f3770a1396  -`

-- 

## ❗Error & Masalah yang Ditemui
- Pada latihan dan analisis kaliini aku tidak menemukan eror apapun, aku bisa melakukan praktik ini
  denggan Linux mint bahkan tanpa mengisntall tools tambahan.

---

## 🔐 Security Insight (Wajib)
- *Bahaya penggunaan md5 :*
   Bahaya utama menggunakan hash MD5 adalah kerentanannya yang signifikan terhadap serangan tabrakan 
   (collision attacks), Ini adalah kelemahan paling kritis. Peneliti keamanan telah menunjukkan 
   cara praktis untuk membuat dua input (misalnya, dua file atau kata sandi) yang berbeda, 
   namun menghasilkan nilai hash MD5 yang persis sama. Hal ini sangat berbahaya karena 
   penyerang dapat memalsukan data (misalnya, sertifikat digital atau dokumen penting) 
   dan membuatnya tampak sah karena memiliki hash yang sama dengan dokumen asli.

- *Alasan Base64 Bukan Termasuk Enkripsi*
   Base64 bukan enkripsi karena tujuannya hanya untuk mengubah data biner menjadi format teks agar 
   mudah ditransmisikan (misalnya dalam email), bukan untuk mengamankan atau menyembunyikan isi data. 
   Data Base64 sangat mudah dibalik (decode) kembali ke bentuk aslinya tanpa kunci, 
   sehingga tidak memberikan kerahasiaan atau keamanan seperti enkripsi yang menggunakan 
   algoritma dan kunci rahasia untuk perlindungan data sensitif.

- *Alasan password tidak boleh di-encrypt tapi di-hash*
  Enkripsi: Mengonversi data ke dalam format aman yang hanya dapat diakses 
  dengan kunci dekripsi. Enkripsi melindungi data saat dikirim dan disimpan. 
  Sementara itu...
  Hashing: Mengubah data menjadi string karakter berukuran tetap dan umumnya 
  digunakan untuk memverifikasi integritas data dan menyimpan kata sandi dengan aman

- *Kenapa asymmetric lebih aman untuk komunikasi publik*
  Dalam komunikasi publik, sulit untuk mendistribusikan kunci rahasia tunggal (seperti pada kriptografi simetris) 
  kepada semua peserta tanpa risiko penyadapan. Kriptografi asimetris memungkinkan Anda membagikan kunci publik 
  Anda secara terbuka kepada siapa saja

---

## 🧠 Catatan Pribadi
- Aku cukup paham denggan materi kaliini, materi ini seru dan membuatku harus berfikir keras serta
  fokus tinggi untuk mentyelesaikan materi awal ini, aku belajar banyak dari topik kaliini termasuk
  `Shift-Cipher` dan `Subtitution-Cipher`, aku belajar kedua rumus ini melalui Youtube denggan teori
  dan praktik yang sangat mudah di fahami namun tetap perlu ketelitian dan kesabaran dalam menyelesaikan
  tantangannya, hasil belajarku tentang kedua materi ini ada di file [Shift-Cipher.txt & Subtitution_Cipher.txt].
  Materi ini memang sulit, tapi untuk mengatasi ini aku hanya perlu mencari sumber lain baik dari Youtube ataupun
  tulisan oranglain yang dibagikan di internet yang aku rasa itu lebih mudah untuk difahami akan tetapi
  tetap memberikan output yang sama.

- Rencana besok : Aku akan mencoba mempelajari PASSWORD SECURITY, SALT, & TOOLS CRACKING (HASHCAT & JOHN)