# 🧪 Lab11 - CodeIgniter 4 Web Development (Lab8Web)

Repositori ini berisi proyek praktikum (Lab) pengembangan web menggunakan framework **CodeIgniter 4 (CI4)**. Proyek ini bertujuan untuk mempelajari dasar-dasar MVC (Model-View-Controller), routing, dan interaksi dengan database pada lingkungan pengembangan lokal.

## 📋 Daftar Isi
- [Fitur Utama](#-fitur-utama)
- [Prasyarat Sistem](#-prasyarat-sistem)
- [Panduan Instalasi](#-panduan-instalasi)
- [Struktur Direktori](#-struktur-direktori)
- [Penggunaan dan Menjalankan Aplikasi](#-penggunaan-dan-menjalankan-aplikasi)
- [Referensi](#-referensi)

---

## 🌟 Fitur Utama
*(Isi bagian ini dengan fitur spesifik dari aplikasi web yang sedang dikembangkan pada Lab ini. Misalnya: CRUD Artikel, Login User, dll.)*
- Implementasi arsitektur MVC pada CodeIgniter 4.
- Konfigurasi sistem _Routing_ dan URI.
- Interaksi Database menggunakan Query Builder / Model.
- Struktur URL yang aman dengan mengarahkan Document Root ke folder `public/`.

---

## 💻 Prasyarat Sistem

Sebelum menjalankan proyek ini, pastikan komputer Anda telah memenuhi persyaratan berikut:
- **PHP** versi `8.2` atau yang lebih baru.
- Ekstensi PHP yang wajib diaktifkan:
  - `intl`
  - `mbstring`
  - `json` (aktif secara default)
  - `mysqlnd` (untuk koneksi ke database MySQL)
  - `libcurl` (jika menggunakan HTTP/CURLRequest)
- **Web Server** seperti Apache atau Nginx (dapat menggunakan XAMPP/Laragon).
- **Database Server** MySQL atau MariaDB.
- **Composer** (Opsional tapi disarankan, untuk manajemen dependensi).

---

## 🛠 Panduan Instalasi

1. **Clone Repositori**  
   Clone repositori ini ke dalam direktori server lokal Anda (misalnya `htdocs` untuk XAMPP).
   ```bash
   git clone https://github.com/FelixSitinjak/Lab8Web.git lab11_ci
   cd lab11_ci
   ```

2. **Pengaturan Environment**  
   Ubah nama file `env` menjadi `.env`:
   - Pada Windows/Command Prompt: `ren env .env`
   - Pada Linux/Mac: `cp env .env`

3. **Konfigurasi Lingkungan (.env)**  
   Buka file `.env` dan atur mode environment ke mode pengembangan untuk melihat pesan error (berguna saat _debugging_):
   ```env
   CI_ENVIRONMENT = development
   ```

4. **Konfigurasi Database**  
   Di dalam file `.env`, atur juga konfigurasi koneksi database Anda:
   ```env
   database.default.hostname = localhost
   database.default.database = nama_database_anda
   database.default.username = root
   database.default.password = 
   database.default.DBDriver = MySQLi
   database.default.DBPrefix =
   database.default.port = 3306
   ```

5. **Update Dependensi (Jika Menggunakan Composer)**  
   Jalankan perintah ini di terminal (opsional jika folder `vendor` sudah ada):
   ```bash
   composer install
   ```

---

## 🚀 Penggunaan dan Menjalankan Aplikasi

CodeIgniter 4 menyediakan local development server yang sangat praktis. Untuk menjalankan proyek ini, ikuti langkah berikut:

1. Buka terminal atau command prompt pada direktori proyek (`lab11_ci`).
2. Jalankan perintah *Spark*:
   ```bash
   php spark serve
   ```
3. Buka web browser Anda dan akses:  
   👉 **http://localhost:8080**

> **Peringatan Keamanan Penting**:
> Jika Anda menggunakan XAMPP tanpa `php spark serve`, **JANGAN** mengakses URL root aplikasi seperti `http://localhost/lab11_ci/`. 
> Hal ini merupakan praktik keamanan yang buruk. Anda harus mengakses melalui folder `public`: 
> `http://localhost/lab11_ci/public/`
> atau lebih baik lagi, konfigurasikan *Virtual Host* di Apache yang langsung mengarah ke `c:\xampp\htdocs\lab11_ci\public`.

---

## 📁 Struktur Direktori

Berikut ini adalah struktur direktori utama proyek yang perlu Anda ketahui:

- `app/` : Berisi source code inti dari aplikasi (Controllers, Models, Views, Config). Anda akan paling sering bekerja di dalam folder ini.
- `public/` : Menjadi *document root* dari aplikasi web. Semua aset publik (CSS, JS, gambar) dan file `index.php` ditempatkan di sini. Folder ini adalah satu-satunya yang boleh diakses dari luar/browser.
- `system/` : Berisi core files dari framework CodeIgniter 4. Jangan ubah apapun di sini.
- `writable/` : Digunakan untuk menyimpan file yang dihasilkan oleh sistem (seperti cache, log, session).
- `spark` : File command line (CLI) bawaan CodeIgniter.

---

## 📚 Referensi

- [Situs Resmi CodeIgniter](https://codeigniter.com)
- [Dokumentasi CodeIgniter 4 (User Guide)](https://codeigniter.com/user_guide/)
- [Forum CodeIgniter](https://forum.codeigniter.com)

---
*Dibuat untuk keperluan pembelajaran Pengembangan Aplikasi Web.*
