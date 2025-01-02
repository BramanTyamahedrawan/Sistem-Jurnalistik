# Sistem-Jurnalistik

## Deskripsi
Sistem ini terdiri dari dua bagian:
1. **Backend**: Dibangun menggunakan Laravel dengan Filament Admin. Backend ini menyediakan API untuk digunakan oleh frontend.
2. **Frontend**: Dibangun menggunakan NuxtJS untuk menampilkan data dari backend.

---

## Cara Instalasi dan Setup

### Prasyarat
Pastikan Anda telah menginstal:
- PHP >= 8.1
- Composer
- Node.js >= 16.x dan npm/yarn
- MySQL (atau database lain yang kompatibel)

### Backend (api-news)
1. **Clone Repository**
   ```bash
   git clone <repository-url>
   cd api-news
   ```

2. **Install Dependencies**
   ```bash
   composer install
   ```

3. **Setup File Environment**
   - Salin file `.env.example` menjadi `.env`.
     ```bash
     cp .env.example .env
     ```
   - Edit file `.env` untuk menyesuaikan pengaturan database Anda.

4. **Generate Application Key**
   ```bash
   php artisan key:generate
   ```

5. **Migrasi Database**
   ```bash
   php artisan migrate
   ```

6. **Menjalankan Server Lokal**
   ```bash
   php artisan serve
   ```
   Akses backend di: [http://localhost:8000](http://localhost:8000)

7. **Menambahkan Data Dummy (Opsional)**
   Jika Anda ingin data awal untuk testing, gunakan:
   ```bash
   php artisan db:seed
   ```

### Frontend (fe-news-nuxt)
1. **Clone Repository**
   ```bash
   git clone <repository-url>
   cd fe-news-nuxt
   ```

2. **Install Dependencies**
   ```bash
   npm install
   # atau jika menggunakan yarn
   yarn install
   ```

3. **Setup File Environment**
   - Salin file `.env.example` menjadi `.env`.
     ```bash
     cp .env.example .env
     ```
   - Edit file `.env` untuk menyesuaikan pengaturan API backend, misalnya:
     ```env
     API_BASE_URL=http://localhost:8000/api
     ```

4. **Menjalankan Server Lokal**
   ```bash
   npm run dev
   # atau jika menggunakan yarn
   yarn dev
   ```
   Akses frontend di: [http://localhost:3000](http://localhost:3000)

---

## Struktur Proyek
- **api-news**: Folder untuk backend dengan Laravel.
- **fe-news-nuxt**: Folder untuk frontend dengan NuxtJS.

---

## Catatan Penting
- Pastikan backend dan frontend berjalan di port yang sesuai dan API_BASE_URL di frontend sudah benar.
- Gunakan `php artisan serve` untuk backend dan `npm run dev`/`yarn dev` untuk frontend selama pengembangan.

---

## .me

### Informasi Tambahan
- Backend: Dibangun dengan Laravel dan menggunakan Filament untuk pengelolaan admin.
- Frontend: Menggunakan NuxtJS untuk SPA dan SSR.
- Fitur Utama:
  - Backend menyediakan API RESTful untuk data jurnalistik.
  - Frontend menampilkan data yang didapat dari API backend.
- Dokumentasi lebih lanjut tersedia di folder masing-masing proyek.

Jika ada masalah, silakan buka issue di repository atau hubungi tim pengembang.

