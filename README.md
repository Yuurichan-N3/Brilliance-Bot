# Brilliance Bot

Selamat datang di **Brilliance Bot**, sebuah alat otomatisasi untuk melakukan registrasi, login, klaim, dan mining pada platform Brilliance Global. Bot ini dirancang untuk membantu pengguna mengotomatiskan tugas-tugas berulang dengan mudah dan efisien.

## Fitur
- **Registrasi Otomatis**: Membuat akun baru dengan email dan kata sandi acak menggunakan Faker.js.
- **Login Otomatis**: Masuk ke akun yang baru dibuat.
- **Klaim dan Mining**: Melakukan tugas klaim dan mining secara otomatis.
- **Dukungan Proxy**: Mendukung penggunaan proxy HTTP/HTTPS dan SOCKS dari file `proxy.txt`.
- **Antarmuka CLI Interaktif**: Memungkinkan pengguna untuk memasukkan kode referal dan jumlah loop.
- **Hitung Mundur**: Menampilkan hitung mundur untuk delay antar langkah atau iterasi.
- **Penyimpanan Kredensial**: Menyimpan email dan kata sandi ke file `information.json`.

## Prasyarat
Pastikan Anda memiliki hal-hal berikut sebelum menjalankan bot:
- **Node.js** (versi 16 atau lebih tinggi)
- **npm** (biasanya sudah terpasang bersama Node.js)
- File `proxy.txt` (opsional, untuk daftar proxy)
- Koneksi internet yang stabil

## Instalasi
1. **Clone Repository**:
   ```
   git clone https://github.com/Yuurichan-N3/Brilliance-Bot.git
   cd Brilliance-Bot
   ```

2. **Instal Dependensi**:
   ```
   npm install
   ```

3. **Siapkan File Proxy (Opsional)**:
   - Buat file `proxy.txt` di direktori proyek.
   - Tambahkan daftar proxy, satu per baris, dalam format:
     ```
     http://username:password@host:port
     socks5://username:password@host:port
     ```
   - Jika tidak menggunakan proxy, biarkan file kosong atau hapus.

4. **Jalankan Bot**:
   ```
   node bot.js
   ```

## Penggunaan
1. Jalankan perintah `node bot.js`.
2. Masukkan kode referal (default: `9afaeff2af` jika dikosongkan).
3. Masukkan jumlah loop (jumlah iterasi yang diinginkan).
4. Bot akan menjalankan proses registrasi, login, klaim, dan mining secara berulang sesuai jumlah loop yang ditentukan.
5. Kredensial akun akan disimpan di file `information.json`.

## Contoh File
- **proxy.txt**:
  ```
  http://user:pass@123.456.789.012:8080
  socks5://user:pass@123.456.789.013:1080
  ```

- **information.json** (dibuat otomatis):
  ```json
  [
    {
      "email": "example1@gmail.com",
      "password": "abc123xyz"
    },
    {
      "email": "example2@gmail.com",
      "password": "xyz789abc"
    }
  ]
  ```

## Catatan
- **Keamanan**: Jangan bagikan file `information.json` karena berisi kredensial akun.
- **Proxy**: Pastikan proxy yang digunakan valid dan cepat untuk menghindari kegagalan permintaan.
- **Error Handling**: Bot akan mencatat error untuk setiap iterasi yang gagal dan melanjutkan ke iterasi berikutnya.
- **Batasan API**: Perhatikan batasan API dari Brilliance Global untuk menghindari pemblokiran.

## Dependensi
- `node-fetch`: Untuk membuat permintaan HTTP.
- `@faker-js/faker`: Untuk menghasilkan data acak seperti email dan kata sandi.
- `https-proxy-agent` & `socks-proxy-agent`: Untuk dukungan proxy.
- `colors`: Untuk antarmuka CLI yang lebih menarik.
- `readline`: Untuk input pengguna.
- `fs`: Untuk operasi file.

## 📜 Lisensi  

Script ini didistribusikan untuk keperluan pembelajaran dan pengujian. Penggunaan di luar tanggung jawab pengembang.  

Untuk update terbaru, bergabunglah di grup **Telegram**: [Klik di sini](https://t.me/sentineldiscus).


---

## 💡 Disclaimer
Penggunaan bot ini sepenuhnya tanggung jawab pengguna. Kami tidak bertanggung jawab atas penyalahgunaan skrip ini.
