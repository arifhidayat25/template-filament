
-----

# 🚀 Laravel Filament Skeleton

Skeleton project untuk memulai aplikasi berbasis **Laravel + Filament v3** dengan cepat. Sudah dilengkapi dengan setup dasar untuk manajemen user, role, dan permission menggunakan **Filament Shield**.

[](https://laravel.com)
[](https://filamentphp.com)
[](https://www.php.net/)

-----

## ⚡️ Fitur Utama

  - **Laravel 11 & PHP 8.2+**: Dibangun di atas versi terbaru untuk performa dan keamanan maksimal.
  - **Filament v3.3 & Livewire v3**: Panel admin modern, reaktif, dan siap pakai.
  - **Manajemen Role & Permission**: Sudah terintegrasi dengan **Spatie Laravel Permission** dan **Filament Shield** untuk manajemen hak akses yang powerful.
  - **Resource Siap Pakai**: Termasuk resource untuk **Users**, **Roles**, dan **Permissions**.
  - **Developer Logins**: Mempercepat proses development dengan login cepat (hanya aktif di environment `local`).
  - **Dashboard Widgets**: Widget dasar seperti info user, jumlah total user, dan info Filament.

-----

## 📦 Instalasi

Ikuti langkah-langkah berikut untuk menjalankan proyek:

1.  **Clone Repository**

    ```bash
    git clone <repo-url> nama-proyek
    cd nama-proyek
    ```

2.  **Install Dependensi**

    ```bash
    composer install
    ```

3.  **Setup Environment**
    Salin file environment dan generate key aplikasi.

    ```bash
    cp .env.example .env
    php artisan key:generate
    ```

4.  **Konfigurasi Database**
    Buka file `.env` dan sesuaikan konfigurasi database Anda (`DB_DATABASE`, `DB_USERNAME`, `DB_PASSWORD`).

5.  **Jalankan Migrasi & Seeder**
    Perintah ini akan membuat semua tabel yang dibutuhkan dan seeder user default.

    ```bash
    php artisan migrate --seed
    ```

-----

## 🛡️ Setup Role & Permission (Filament Shield)

Setelah instalasi, Anda perlu men-generate permissions dan membuat user super admin.

1.  **Generate Policies & Permissions**
    Perintah ini akan membaca semua model Anda dan membuat permission (view, create, update, delete) secara otomatis.

    ```bash
    php artisan shield:generate --all
    ```

2.  **Buat Super Admin**
    Jalankan perintah interaktif berikut untuk membuat user dengan role `super_admin` yang memiliki akses penuh ke sistem.

    ```bash
    php artisan shield:super-admin
    ```

3.  **Assign Role ke User (Contoh)**
    Anda juga bisa memberikan role ke user secara manual melalui kode:

    ```php
    $user = User::find(1);
    $user->assignRole('super_admin');
    ```

-----

## 👨‍💻 Developer Logins

Untuk mempermudah login saat development, plugin ini sudah aktif.

  - Hanya muncul di environment `local`.
  - Menampilkan dropdown berisi daftar user di halaman login untuk masuk dengan satu klik.

-----

## 🚀 Menjalankan Aplikasi

1.  **Jalankan Development Server**

    ```bash
    php artisan serve
    ```

2.  **Akses Panel Admin**
    Buka browser Anda dan kunjungi:
    **👉 [http://127.0.0.1:8000/admin](http://127.0.0.1:8000/admin)**

Login menggunakan akun `super_admin` yang telah Anda buat pada langkah sebelumnya. Selamat bekerja\!

hapus git 

 ```bash
Remove-Item -Recurse -Force .git
    
