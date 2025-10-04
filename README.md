# Sistem Manajemen Data Mahasiswa dengan Docker Compose

Sebuah aplikasi web CRUD (Create, Read, Update, Delete) untuk mengelola data mahasiswa yang dibangun menggunakan PHP, MySQL, dan dideploy dengan Docker Compose.

## 📋 Informasi Project

-   **Nama**: I Kadek Rai Pramana
-   **NIM**: 2105551094
-   **Mata Kuliah**: Manajemen Jaringan dan Server (C)
-   **Dosen Pengampu**: Anak Agung Ketut Agung Cahyawan Wiranatha, ST, MT

## 🚀 Fitur

-   ✅ Tampil data mahasiswa dalam bentuk tabel
-   ✅ Tambah data mahasiswa baru
-   ✅ Update data mahasiswa yang sudah ada
-   ✅ Hapus data mahasiswa
-   ✅ Interface responsive menggunakan Bootstrap 5
-   ✅ DataTables untuk pencarian dan pagination
-   ✅ Validasi form dengan JavaScript
-   ✅ Containerized dengan Docker

## 🛠️ Teknologi yang Digunakan

-   **Backend**: PHP 8.0 dengan Apache
-   **Database**: MySQL 8.0
-   **Frontend**: HTML, CSS, JavaScript, Bootstrap 5
-   **Container**: Docker & Docker Compose
-   **Database Management**: phpMyAdmin

## 📁 Struktur Project

```
MJS-Docker-Compose/
├── docker-compose.yml      # Konfigurasi layanan Docker
├── Dockerfile             # Image untuk PHP Apache
├── README.md              # Dokumentasi project
└── src/
    ├── index.php          # Halaman utama
    ├── css/
    │   ├── styleForm.css  # Styling untuk form
    │   └── styleIndex.css # Styling untuk halaman utama
    ├── db/
    │   └── prodi.sql      # Database schema dan data
    ├── js/
    │   ├── dataTables.js  # Konfigurasi DataTables
    │   ├── validationAdd.js    # Validasi form tambah
    │   └── validationUpdate.js # Validasi form update
    └── php/
        ├── addData.php    # Form dan proses tambah data
        ├── connection.php # Konfigurasi koneksi database
        ├── deleteData.php # Proses hapus data
        └── updateData.php # Form dan proses update data
```

## 🐳 Layanan Docker

Project ini menggunakan 3 layanan Docker:

1. **app_env**: Aplikasi PHP dengan Apache (Port 8080)
2. **mysql_db**: Database MySQL (Internal)
3. **phpmyadmin**: Interface manajemen database (Port 8081)

## ⚡ Quick Start

### Prerequisites

-   Docker
-   Docker Compose

### Instalasi dan Menjalankan

1. **Clone repository**

    ```bash
    git clone https://github.com/rai-pramana/MJS-Docker-Compose.git
    cd MJS-Docker-Compose
    ```

2. **Jalankan dengan Docker Compose**

    ```bash
    docker-compose up -d
    ```

3. **Akses aplikasi**
    - **Aplikasi Web**: http://localhost:8080
    - **phpMyAdmin**: http://localhost:8081

### Kredensial Database

-   **Host**: mysql_db
-   **Database**: prodi
-   **Username**: rai-pramana
-   **Password**: rai123
-   **Root Password**: rai123

## 📊 Database Schema

### Tabel `mahasiswa`

| Field     | Type        | Description      |
| --------- | ----------- | ---------------- |
| NIM       | VARCHAR(10) | Primary Key      |
| Namamhs   | VARCHAR(30) | Nama Mahasiswa   |
| Alamatmhs | VARCHAR(80) | Alamat Mahasiswa |
| Kontakmhs | VARCHAR(12) | Kontak Mahasiswa |

## 🎯 Cara Menggunakan

1. **Melihat Data**: Halaman utama menampilkan semua data mahasiswa dalam tabel
2. **Tambah Data**: Klik tombol "Tambah Data" untuk menambah mahasiswa baru
3. **Update Data**: Klik tombol "Update" pada baris data yang ingin diubah
4. **Hapus Data**: Klik tombol "Hapus" pada baris data yang ingin dihapus

## 🛡️ Fitur Keamanan

-   Validasi input pada form
-   Prepared statements untuk mencegah SQL injection
-   Konfirmasi sebelum menghapus data

## 📱 Responsive Design

Aplikasi ini menggunakan Bootstrap 5 untuk memastikan tampilan yang responsive di berbagai perangkat (desktop, tablet, mobile).

## 🔧 Development

### Menghentikan Layanan

```bash
docker-compose down
```

### Rebuild Container

```bash
docker-compose up --build
```

### Melihat Logs

```bash
docker-compose logs -f
```

## 📝 Catatan

-   Database akan otomatis dibuat dan diisi dengan data contoh saat pertama kali dijalankan
-   File `prodi.sql` berisi schema dan data awal untuk testing
-   Aplikasi menggunakan mysqli untuk koneksi database

## 🤝 Kontribusi

Silakan buat issue atau pull request jika ada saran perbaikan untuk project ini.

## 📄 Lisensi

Project ini dibuat untuk keperluan akademik dalam mata kuliah Manajemen Jaringan dan Server.
