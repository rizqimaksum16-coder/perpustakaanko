# Sistem Perpustakaan Digital Kampus

Aplikasi web untuk manajemen perpustakaan kampus yang dibangun menggunakan framework Laravel 13. Aplikasi ini memungkinkan petugas dan admin mengelola data buku, anggota perpustakaan, serta transaksi peminjaman dan pengembalian buku.

## Fitur Utama

- CRUD Kategori Buku
- CRUD Data Buku  
- CRUD Data Anggota Perpustakaan
- Manajemen Transaksi Peminjaman & Pengembalian
- Autentikasi Petugas/Admin
- REST API untuk integrasi
- Dashboard Statistik

## Teknologi yang Digunakan

- **Framework**: Laravel 13
- **Database**: MySQL
- **ORM**: Eloquent
- **Frontend**: Blade Templating
- **Version Control**: Git & GitHub

## Cara Menjalankan Project

### Prasyarat
- PHP >= 8.2
- Composer
- MySQL
- Node.js & NPM (opsional untuk frontend build)
- Git

### Instalasi

1. Clone repository:
\\\ash
git clone https://github.com/USERNAME/app-perpustakaan.git
cd app-perpustakaan
\\\

2. Install dependencies:
\\\ash
composer install
\\\

3. Copy file environment:
\\\ash
cp .env.example .env
\\\

4. Generate application key:
\\\ash
php artisan key:generate
\\\

5. Konfigurasi database di file .env:
\\\env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=db_perpustakaan
DB_USERNAME=root
DB_PASSWORD=
\\\

6. Jalankan migration (membuat tabel database):
\\\ash
php artisan migrate
\\\

7. Jalankan development server:
\\\ash
php artisan serve
\\\

8. Buka browser dan akses: http://127.0.0.1:8000

## Struktur Project

- \pp/Models/\ - Model Eloquent untuk representasi data
- \pp/Http/Controllers/\ - Controller untuk menangani request
- \esources/views/\ - View Blade untuk tampilan frontend
- \outes/web.php\ - Definisi route aplikasi
- \database/migrations/\ - File untuk membuat/modifikasi struktur database

## Penjelasan MVC Architecture

Aplikasi ini menggunakan pola **MVC (Model-View-Controller)**:

- **Model**: Bertanggung jawab untuk mengakses dan memanipulasi data dari database. Setiap Model merepresentasikan satu tabel database. Sebagai contoh, Model \Book\ menangani semua operasi terkait data buku.

- **View**: Bertanggung jawab untuk menampilkan data kepada pengguna dalam bentuk HTML. View menerima data dari Controller dan menampilkannya sesuai template yang sudah dirancang. Di Laravel, file View menggunakan Blade templating.

- **Controller**: Bertanggung jawab untuk menerima request dari user, memproses logika bisnis, berkomunikasi dengan Model untuk mengambil/mengubah data, dan mengirimkan hasil ke View untuk ditampilkan. Controller adalah "penghubung" antara Model dan View.

## Alur Kerja

Saat user mengakses aplikasi:
1. Request masuk ke route (routes/web.php)
2. Route mengarahkan ke method tertentu di Controller
3. Controller menggunakan Model untuk query database
4. Controller mengirim data ke View
5. View merender HTML dan mengirimnya ke browser

## Progress Pembelajaran

- [x] **Pertemuan 1**: Framework, MVC & Setup Proyek
- [ ] **Pertemuan 2**: Routing & Request Lifecycle
- [ ] **Pertemuan 3**: Controller, Request & Validation
- [ ] **Pertemuan 4**: Blade Templating & Layout System
- [ ] **Pertemuan 5**: Migration, Eloquent Model & CRUD
- [ ] **Pertemuan 6**: UTS Checkpoint
- [ ] **Pertemuan 7**: Eloquent Relationships
- [ ] **Pertemuan 8**: Authentication & Middleware
- [ ] **Pertemuan 9**: REST API Dasar
- [ ] **Pertemuan 10**: Dashboard & Integration
- [ ] **Pertemuan 11**: UAS Final Project

## Tim Pengembang

- Nama: Kiro AI Assistant
- Institusi: Universitas
- NIM: -

## Lisensi

Project ini adalah bagian dari pembelajaran Pemrograman Framework di universitas.

---

**Terakhir diupdate**: Pertemuan 1
