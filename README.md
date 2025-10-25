# 📂 Struktur Folder 1.0

## 🧱 Struktur Folder

```bash
.
├── Controller/
│   ├── AdminController.php      # Mengatur logika halaman admin & laporan
│   └── AuthController.php       # Mengatur proses login & autentikasi pengguna
│
├── Core/
│   ├── Controller.php           # Kelas dasar untuk semua controller
│   └── Database.php             # Koneksi ke database menggunakan PDO
│
├── Models/
│   ├── LaporanModel.php         # Model untuk data laporan
│   └── UserModel.php            # Model untuk data pengguna
│
├── Views/
│   ├── admin/
│   │   └── laporan.php          # Tampilan halaman laporan admin
│   └── Auth/
│       └── login.php            # Tampilan halaman login
│
├── config.php                   # File konfigurasi global (database, constants, dll)
└── index.php                    # Entry point utama aplikasi
```

---

## ⚙️ Penjelasan Singkat MVC

| Komponen | Deskripsi |
|-----------|------------|
| **Model** | Berisi logika data dan interaksi dengan database (CRUD). |
| **View** | Menampilkan data ke pengguna (HTML, PHP). |
| **Controller** | Menjembatani antara Model dan View; mengatur alur logika aplikasi. |
| **Core** | Berisi kelas dasar seperti `Controller.php` dan `Database.php`. |
| **index.php** | Pintu utama aplikasi yang memproses setiap request. |

---

## 🚀 Cara Menjalankan Proyek

1. Pindahkan folder proyek ini ke direktori server lokal kamu:  
   - **XAMPP:** `htdocs/`  
   - **Laragon:** `www/`

2. Sesuaikan konfigurasi database di file **config.php**:
   ```php
   define('DB_HOST', 'localhost');
   define('DB_NAME', 'nama_database');
   define('DB_USER', 'root');
   define('DB_PASS', '');
   ```

3. Jalankan server Apache & MySQL.

4. Akses aplikasi melalui browser:
   ```
   http://localhost/nama_folder_kamu/
   ```

5. Jalur akses utama:
   - **Login:** `/Auth/login`
   - **Dashboard Admin:** `/Admin/laporan`

---

## 💡 Contoh Alur

- **Login:**  
  `AuthController → UserModel → login.php`

- **Dashboard Admin:**  
  `AdminController → LaporanModel → laporan.php`

---

## 🧠 Tips & Catatan

- Pastikan session sudah diinisialisasi di `index.php` atau controller yang membutuhkan autentikasi.  
- Gunakan `spl_autoload_register()` untuk autoload file controller dan model secara otomatis.  
- Pisahkan logika database ke dalam model agar controller tetap bersih dan terstruktur.  
- Struktur ini dapat dikembangkan untuk proyek yang lebih kompleks (middleware, routing, dsb).

---

## 🛠️ Teknologi yang Digunakan

- **Bahasa:** PHP (Native)  
- **Database:** MySQL (PDO)  
- **Arsitektur:** MVC (Model–View–Controller)  
- **Server:** Apache / Nginx  

---

## 👨‍💻 Pengembang

**Gefi**  
Mahasiswa Sistem Informasi & UI/UX Designer  
💼 [Gefiranch](#)

---

⭐ *Kalau struktur ini membantu, jangan lupa kasih bintang di repo GitHub kamu!*
