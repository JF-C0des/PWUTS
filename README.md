# Website IT Services (Laravel, Filament, SELECAO Template)

Ini adalah proyek pengembangan website untuk penyedia layanan IT. Proyek ini dibangun untuk menggantikan proses pemesanan manual (melalui iklan/media sosial) menjadi platform digital yang terstruktur, profesional, dan mudah dikelola.

Fokus utama adalah menyediakan antarmuka yang bersih dan profesional bagi pelanggan (menggunakan template SELECAO) dan panel admin yang kuat bagi pemilik bisnis (menggunakan Laravel Filament) untuk mengelola pesanan dan konten.

## 🚀 Teknologi Utama (Tech Stack)

* **Backend:** Laravel 11
* **Admin Panel:** Filament 3.x
* **Frontend:** Bootstrap 5 (diadaptasi dari Template SELECAO)
* **Database:** MySQL / MariaDB
* **Asset Bundling:** Vite

## ✨ Fitur Utama (Key Features)

### Frontend (Area Publik - Template SELECAO)

* **Halaman Beranda:** Menampilkan ringkasan layanan, portofolio, dan testimoni.
* **Daftar Layanan:** Halaman khusus yang menampilkan semua layanan IT yang ditawarkan, lengkap dengan deskripsi dan estimasi harga.
* **Portofolio:** Galeri proyek-proyek yang pernah dikerjakan.
* **Formulir Pemesanan:** Formulir kontak/pemesanan sederhana yang memungkinkan pelanggan mengirim permintaan layanan.

### Backend (Area Admin - Laravel Filament)

* **Manajemen Layanan:** Fitur CRUD (Create, Read, Update, Delete) penuh untuk semua layanan yang ditampilkan di *frontend*.
* **Manajemen Pesanan:** Melihat dan mengelola daftar pesanan/permintaan yang masuk dari pelanggan.
* **Manajemen Pengguna:** Mengelola akun admin yang dapat mengakses *backend*.

## 🛠️ Instalasi & Setup Lokal (Getting Started)

Berikut adalah langkah-langkah untuk menjalankan proyek ini di lingkungan lokal.

1.  **Clone Repositori**
    ```bash
    git clone [URL_REPOSITORY_ANDA]
    cd [NAMA_FOLDER_PROYEK]
    ```

2.  **Install Dependensi PHP**
    ```bash
    composer install
    ```

3.  **Setup Environment**
    * Salin file `.env.example` menjadi `.env`.
    ```bash
    cp .env.example .env
    ```
    * Buat kunci aplikasi (APP_KEY).
    ```bash
    php artisan key:generate
    ```

4.  **Konfigurasi Database**
    * Buka file `.env` dan sesuaikan pengaturan `DB_*` (nama database, username, password) sesuai dengan konfigurasi MySQL/MariaDB lokal Anda.
    ```
    DB_CONNECTION=mysql
    DB_HOST=127.0.0.1
    DB_PORT=3306
    DB_DATABASE=db_it_services
    DB_USERNAME=root
    DB_PASSWORD=
    ```

5.  **Migrasi Database**
    * Jalankan migrasi untuk membuat semua tabel di database.
    ```bash
    php artisan migrate
    ```

6.  **Install Dependensi Node.js & Build Assets**
    ```bash
    npm install
    npm run build
    ```
    *(Atau `npm run dev` untuk development)*

7.  **Jalankan Server Lokal**
    ```bash
    php artisan serve
    ```

## 💻 Penggunaan (Usage)

Setelah server berjalan, Anda dapat mengakses dua bagian utama aplikasi:

* **Website (Frontend):**
    * URL: `http://127.0.0.1:8000`

* **Admin Panel (Backend):**
    * URL: `http://127.0.0.1:8000/admin`
    * **Penting:** Untuk membuat user admin pertama Anda, jalankan perintah Filament berikut di terminal dan ikuti instruksinya:
    ```bash
    php artisan make:filament-user
    ```

## 🖼️ (Opsional) Tangkapan Layar

*(Tambahkan beberapa tangkapan layar di sini untuk menunjukkan tampilan website dan panel admin Anda)*



[Image of Frontend Homepage]



[Image of Admin Panel Dashboard]


## 📄 Lisensi

Proyek ini dilisensikan di bawah [MIT License](LICENSE.md).