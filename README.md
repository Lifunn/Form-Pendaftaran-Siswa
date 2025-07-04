# Form-Pendaftaran-Siswa

# Aplikasi CRUD Pendaftaran Siswa (PHP & MySQL)

Ini adalah proyek aplikasi web sederhana untuk Pendaftaran Siswa Baru yang dibangun menggunakan PHP Native, database MySQL, dan antarmuka pengguna yang modern dengan Tailwind CSS. Aplikasi ini mengimplementasikan fungsionalitas **CRUD** (Create, Read, Update, Delete) secara penuh.

![Halaman Utama](Screenshot%202025-07-04%20224451.png)

## ✨ Fitur Utama

* **Tambah Data Siswa:** Mendaftarkan siswa baru melalui formulir yang intuitif.
* **Tampilkan Data Siswa:** Melihat semua siswa yang telah terdaftar dalam format tabel yang rapi dan informatif.
* **Lihat Detail Siswa:** Menampilkan halaman profil lengkap untuk setiap siswa.
* **Ubah Data Siswa:** Memperbarui informasi siswa yang sudah ada.
* **Hapus Data Siswa:** Menghapus data siswa dari daftar dengan konfirmasi.
* **Upload Foto:** Mengunggah dan menampilkan foto profil untuk setiap siswa.
* **Antarmuka Responsif:** Desain yang bersih dan modern menggunakan Tailwind CSS.

## 📸 Tampilan Aplikasi

Berikut adalah tampilan dari setiap halaman utama pada aplikasi.

### Halaman Daftar Siswa
Halaman ini menampilkan semua data siswa yang sudah terdaftar dalam bentuk tabel. Dari sini, pengguna dapat mengakses aksi lihat detail, edit, dan hapus.
![Halaman Daftar Siswa](Screenshot%202025-07-04%20224809.png)

### Halaman Detail Siswa
Menampilkan informasi pribadi yang lebih lengkap dari seorang siswa yang dipilih.
![Halaman Detail Siswa](Screenshot%202025-07-04%20224825.jpg)

### Halaman Edit Siswa
Menyajikan formulir yang sudah terisi dengan data siswa saat ini, memungkinkan pengguna untuk melakukan pembaruan informasi.
![Halaman Edit Siswa](Screenshot%202025-07-04%20224841.png)

### Proses Hapus Data
Ketika ikon hapus diklik, sebuah dialog konfirmasi dari browser akan muncul untuk memastikan tindakan tersebut. Jika disetujui, data akan dihapus dari database oleh skrip `hapus.php`.
![Konfirmasi Hapus](peweb%20backend%20hapus.mp4)

---

## 📂 Struktur File

Proyek ini disusun dengan struktur file sebagai berikut untuk memisahkan setiap fungsi ke dalam filenya masing-masing:
## 🛠️ Teknologi yang Digunakan

* **Backend:** PHP Native
* **Database:** MySQL
* **Frontend:** HTML
* **Styling:** Tailwind CSS
* **Icons:** Font Awesome
* **Web Server:** XAMPP (Apache & MySQL)

## ⚙️ Panduan Instalasi dan Setup

Untuk menjalankan proyek ini di lingkungan lokal Anda, ikuti langkah-langkah berikut:

1.  **Clone Repositori**
    ```bash
    git clone [https://github.com/username/nama-repositori.git](https://github.com/username/nama-repositori.git)
    ```

2.  **Pindahkan ke Direktori Web Server**
    Pindahkan folder proyek ke dalam direktori `htdocs` dari instalasi XAMPP Anda.

3.  **Jalankan XAMPP**
    Buka XAMPP Control Panel dan jalankan modul **Apache** dan **MySQL**.

4.  **Buat Database**
    * Buka browser dan akses `http://localhost/phpmyadmin`.
    * Buat database baru dengan nama `pendaftaran_siswa`.

5.  **Buat Tabel Siswa**
    * Pilih database `pendaftaran_siswa` yang baru dibuat.
    * Buka tab **SQL** dan jalankan query berikut untuk membuat tabel `calon_siswa`:
    ```sql
    CREATE TABLE `calon_siswa` (
      `id` int(11) NOT NULL AUTO_INCREMENT,
      `nama` varchar(64) NOT NULL,
      `alamat` varchar(255) NOT NULL,
      `jenis_kelamin` varchar(16) NOT NULL,
      `agama` varchar(16) NOT NULL,
      `sekolah_asal` varchar(64) NOT NULL,
      `foto` varchar(255) DEFAULT NULL,
      PRIMARY KEY (`id`)
    ) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;
    ```

6.  **Konfigurasi Koneksi (Opsional)**
    File `config.php` sudah diatur untuk koneksi standar XAMPP. Jika konfigurasi database Anda berbeda, sesuaikan isinya.
    ```php
    <?php 
    $server = "localhost";
    $username = "root";
    $password = "";
    $database = "pendaftaran_siswa";
    // ...
    ?>
    ```

7.  **Jalankan Aplikasi**
    Buka browser dan akses `http://localhost/nama-folder-proyek/`.

## 📂 Struktur File

Berikut adalah penjelasan singkat tentang file-file utama dalam proyek ini:
.
├── uploads/            // Direktori untuk menyimpan foto siswa yang diunggah
├── config.php          // File konfigurasi dan koneksi ke database
├── form-daftar.php     // Halaman form untuk mendaftar siswa baru
├── form-edit.php       // Halaman form untuk mengubah data siswa
├── hapus.php           // Skrip untuk memproses penghapusan data
├── index.php           // Halaman utama / beranda aplikasi
├── list-siswa.php      // Halaman untuk menampilkan daftar semua siswa
├── proses-pendaftaran.php // Skrip untuk memproses data pendaftaran baru
├── proses-edit.php     // Skrip untuk memproses perubahan data
└── show.php            // Halaman untuk menampilkan detail satu siswa

---

## 🗃️ Tampilan Backend (phpMyAdmin)

Berikut adalah tampilan struktur dan isi dari tabel `calon_siswa` di dalam database `pendaftaran_siswa` yang dikelola melalui phpMyAdmin.

![Tampilan Tabel di phpMyAdmin](Screenshot%202025-07-04%20224935.png)
