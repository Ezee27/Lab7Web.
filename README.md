# Laporan Praktikum Pemrograman Web 2
**Nama:** ZAENAL MAULANA RIZKI  
**NIM:** 312410332
**Kelas:** I241D
**Universitas:** Universitas Pelita Bangsa, Bekasi

Repository ini dibuat untuk memenuhi tugas mata kuliah Pemrograman Web 2, mencakup praktikum modul 1 hingga modul 4 menggunakan Framework **CodeIgniter 4**.

---

## Daftar Isi
1. [Modul 1: PHP Framework (Codeigniter)
2. [Modul 2: Framework Lanjutan (CRUD)
3. [Modul 3: View Layout dan View Cell
4. [Modul 4: Framework Lanjutan (Modul Login)

---

<a name="modul-1"></a>
## 1. Modul 1: Pengenalan CI4 & Halaman Statis
Pada modul ini, dilakukan instalasi CodeIgniter 4 dan pembuatan halaman statis (Home, About, Contact).

**Langkah-langkah:**
* Instalasi CI4 menggunakan Composer atau manual.
* Membuat Controller `Page.php` untuk mengatur navigasi.
* Membuat View untuk header, footer, dan konten halaman.

> **Screenshot:** > ![Home Page]
> <img width="1094" height="745" alt="image" src="https://github.com/user-attachments/assets/425bda0e-a455-4d0e-8665-f81137247c92" />

---

<a name="modul-2"></a>
## 2. Modul 2: Database & CRUD
Fokus pada pengolahan data artikel yang disimpan di database MySQL.

**Langkah-langkah:**
* Membuat database `lab_ci4` dan tabel `artikel`.
* Konfigurasi koneksi database di file `.env`.
* Membuat `ArtikelModel.php` dan Controller `Artikel.php`.
* Implementasi fungsi Tambah, Ubah, dan Hapus artikel.

> **Screenshot:** > ![Daftar Artikel]
> <img width="983" height="368" alt="image" src="https://github.com/user-attachments/assets/4da8070e-1e1d-425a-87a7-bdd77f0864be" />


---

<a name="modul-3"></a>
## 3. Modul 3: View Layout & View Cell
Mengoptimalkan tampilan agar lebih modular menggunakan fitur Layout dan View Cell.

**Langkah-langkah:**
* Membuat base layout di `app/Views/layout/main.php`.
* Menggunakan `$this->extend` dan `$this->section` pada setiap view.
* Membuat komponen widget "Artikel Terkini" menggunakan View Cell agar bisa dipanggil di halaman mana saja.

---

<a name="modul-4"></a>
## 4. Modul 4: Sistem Login & Auth Filter
Menambahkan sistem autentikasi untuk membatasi akses halaman admin.

**Langkah-langkah:**
* Membuat tabel `user` dengan password yang di-hash.
* Membuat Controller `User.php` untuk fungsi `login` dan `logout`.
* Membuat Filter `Auth.php` di `app/Filters/`.
* Mendaftarkan filter pada `app/Config/Filters.php` dan menerapkannya pada route grup `admin` di `app/Config/Routes.php`.

**Hasil Pengujian:**
1. Akses halaman `/admin/artikel` tanpa login akan otomatis dialihkan ke halaman login.
2. Login menggunakan email dan password yang sesuai di database.
3. Logout akan menghapus session dan kembali ke halaman login.

> **Screenshot Login:** > ![Halaman Login]
> <img width="1168" height="501" alt="image" src="https://github.com/user-attachments/assets/51758824-11ba-4b7e-b92b-dbfb369a37d7" />


---

## Cara Menjalankan Project
1. Clone repository ini.
2. Jalankan `composer update`.
3. Import file database (jika ada) ke MySQL.
4. Sesuaikan konfigurasi database di file `.env`.
5. Jalankan perintah `php spark serve`.
