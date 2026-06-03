# Tugas Pemrograman Web - Authentication Laravel Breeze


* **Nama:** Imam Aryanta Ramadhan
* **NIM:** 2411532001
* **Program Studi:** Informatika
* **Fakultas:** Teknologi Informasi
* **Universitas:** Universitas Andalas

---

## 🚀 Fitur Utama
* **Authentication System:** Registrasi pengguna baru, login, dan logout yang aman.
* **Password Management:** Fitur lupa password dan reset password via link email.
* **Profile Management:** Pengguna dapat memperbarui nama, alamat email, dan mengubah password mereka.
* **Email Verification:** Memastikan pengguna mendaftar dengan email aktif (opsional/bisa diaktifkan).
* **Responsive UI:** Antarmuka responsif menggunakan Tailwind CSS bawaan Laravel Breeze.

---

## 🛠️ Prasyarat (Prerequisites)
Sebelum menjalankan project ini secara lokal, pastikan perangkat kamu sudah terinstal:
* PHP (versi >= 8.2 direkomendasikan)
* Composer
* Node.js & NPM
* Database Server (MySQL / MariaDB / XAMPP)

---

## 💻 Langkah Instalasi & Menjalankan Project

Ikuti langkah-langkah berikut untuk menjalankan project ini di komputer lokal kamu:

### 1. Clone Repositori
```bash
git clone [https://github.com/RyantRamadhan/auth-breeze.git](https://github.com/RyantRamadhan/auth-breeze.git)
cd auth-breeze

2. Install Dependencies PHP (Composer)
Mengunduh library framework Laravel:
```bash
composer install
```

3. Install Dependencies Frontend (NPM)
Mengunduh library untuk tampilan dan melakukan build:
```bash
npm install
npm run build
```

4. Konfigurasi Environment (.env)
Duplikat file .env.example dan ubah namanya menjadi .env menggunakan perintah:
```bash
cp .env.example .env
```

5. Generate Application Key
```bash
php artisan key:generate
```

6. Konfigurasi Database
Buka XAMPP dan jalankan MySQL.
Buka phpMyAdmin (http://localhost/phpmyadmin) dan buat database kosong baru dengan nama auth_demo.
Buka file .env di teks editor, lalu sesuaikan konfigurasi database-nya:
```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=auth_demo
DB_USERNAME=root
DB_PASSWORD=
```

7. Jalankan Migrasi Database
Membentuk tabel ke dalam database beserta kolom-kolom baru (no_hp dan role) yang sudah dikonfigurasi:
```bash
php artisan migrate
```

8. Jalankan Development Server
```bash
php artisan serve
```
Aplikasi dapat diakses melalui browser di alamat: http://127.0.0.1:8000

---

## Panduan Pengujian (Testing) Fitur

Untuk memeriksa hasil pengerjaan tugas, Pengguna dapat melakukan skenario berikut:

### Skenario 1: Testing Role "User Biasa" (Tugas 1 dan 2)
1. Buka http://127.0.0.1:8000/register.
2. Lakukan pendaftaran. Isi formulir pendaftaran, isi kolom No. HP, dan pastikan pada combobox Daftar Sebagai pengguna memilih User Biasa.
3. Setelah register, pengguna akan diarahkan ke Dashboard. (Tugas 1 Selesai: Info No. HP tampil di Dashboard, dan tabel daftar pengguna tidak terlihat).
4. Klik menu Profile di sudut kanan atas.
5. Coba ubah Nomor HP pengguna lalu klik Save. Pastikan data berhasil diperbarui. (Tugas 2 Selesai).
6. Logout.

### Skenario 2: Testing Role "Administrator" (Tugas 3)
1. Buka http://127.0.0.1:8000/register.
2. Lakukan pendaftaran akun baru, namun kali ini pada combobox Daftar Sebagai pilih Administrator.
3. Setelah berhasil masuk ke Dashboard, pengguna akan melihat tampilan yang berbeda. Di bagian bawah informasi profil admin, akan muncul Panel Admin berupa Tabel Daftar Semua Pengguna yang terdaftar di database. (Tugas 3 Selesai).
