# Form-Pendaftaran-Siswa

# Aplikasi CRUD Pendaftaran Siswa (PHP & MySQL)

Ini adalah proyek aplikasi web sederhana untuk Pendaftaran Siswa Baru yang dibangun menggunakan PHP Native, database MySQL, dan antarmuka pengguna yang modern dengan Tailwind CSS. Aplikasi ini mengimplementasikan fungsionalitas **CRUD** (Create, Read, Update, Delete) secara penuh.

## ✨ Fitur Utama

* **Tambah Data Siswa:** Mendaftarkan siswa baru melalui formulir yang intuitif.
* **Tampilkan Data Siswa:** Melihat semua siswa yang telah terdaftar dalam format tabel yang rapi dan informatif.
* **Lihat Detail Siswa:** Menampilkan halaman profil lengkap untuk setiap siswa.
* **Ubah Data Siswa:** Memperbarui informasi siswa yang sudah ada.
* **Hapus Data Siswa:** Menghapus data siswa dari daftar dengan konfirmasi.
* **Upload Foto:** Mengunggah dan menampilkan foto profil untuk setiap siswa.
* **Antarmuka Responsif:** Desain yang bersih dan modern menggunakan Tailwind CSS.

## 📸 Tampilan Aplikasi

### Tampilan Utama
![Tampilan Utama](Hasil/Tampilan%20Halaman%20Utama.png)

### Halaman Detail Siswa
![Halaman Detail Siswa](Hasil/Halamam%20Detail%20Siswa.png)

### Tampilan Database (MySQL)
![Tampilan Database MySQL](Hasil/tampilan%20Mysql.png)

---

## 🎥 Demo Fungsionalitas (Video)

Karena file video tidak bisa ditampilkan langsung, berikut adalah link untuk melihat demo fungsionalitasnya:

* **[Lihat Demo Tampilan Daftar Siswa](Hasil/Tampilan%20Daftar%20siswa.mp4)**
* **[Lihat Demo Edit Data](Hasil/CRUD%20Edit.mp4)**
* **[Lihat Demo Hapus Data](Hasil/CRUD%20Delete.mp4)**

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
