# 🍱 KantinKu – Aplikasi Pemesanan Makanan Kantin

> Aplikasi mobile web untuk memesan makanan kantin secara digital, lengkap dengan autentikasi, menu, keranjang belanja, dan riwayat transaksi.

---

## 📋 Deskripsi Proyek

**KantinKu** adalah aplikasi mobile-first berbasis HTML/CSS/JavaScript yang memungkinkan pengguna untuk:
- Login & registrasi akun menggunakan **FakeStoreAPI**
- Melihat dan mencari **daftar menu makanan**
- Menambahkan item ke **keranjang** dan menghitung **total pesanan**
- Melakukan checkout dan melihat **riwayat transaksi**

---

## ✨ Fitur Utama

| Fitur | Keterangan |
|-------|-----------|
| 🔐 **Autentikasi** | Login & Register via FakeStoreAPI (`/auth/login`, `/users`) |
| 🍜 **List Menu** | Menampilkan produk dari FakeStoreAPI dengan nama menu lokal |
| 🔍 **Search & Filter** | Cari menu berdasarkan nama; filter berdasarkan kategori |
| 🛒 **Keranjang** | Tambah, kurangi, hapus item; perhitungan subtotal + biaya layanan |
| 💳 **Checkout** | Pemrosesan pesanan dengan nomor order unik |
| 📋 **Riwayat** | Daftar semua transaksi dengan status pesanan |
| 👤 **Profil** | Informasi akun + statistik belanja |

---

## 🛠️ Teknologi yang Digunakan

- **HTML5** – Struktur halaman
- **Tailwind CSS** (CDN) – Styling & layout responsif
- **Vanilla JavaScript** – Logic aplikasi
- **Google Fonts** (Sora + Inter) – Tipografi
- **FakeStoreAPI** – Backend autentikasi & data produk

---

## 📡 Integrasi FakeStoreAPI

```
Base URL: https://fakestoreapi.com

Endpoints yang digunakan:
- POST /auth/login       → Login pengguna
- POST /users            → Registrasi pengguna baru
- GET  /users            → Ambil data user (untuk profil)
- GET  /products         → Ambil daftar menu
```

### Contoh Request Login:
```json
POST https://fakestoreapi.com/auth/login
{
  "username": "johnd",
  "password": "m38rmF$"
}
```

### Response:
```json
{
  "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9..."
}
```

---

## 🚀 Cara Menjalankan

### Opsi 1: Buka Langsung
```bash
# Clone repository
git clone https://github.com/[username]/kantinku-app.git
cd kantinku-app

# Buka di browser
open index.html
# atau double-click file index.html
```

### Opsi 2: Dengan Live Server (VS Code)
1. Install ekstensi **Live Server** di VS Code
2. Klik kanan `index.html` → **Open with Live Server**

### Opsi 3: Dengan Python HTTP Server
```bash
python3 -m http.server 8080
# Buka: http://localhost:8080
```

---

## 📱 Demo Akun

Gunakan akun demo FakeStoreAPI:
```
Username : johnd
Password : m38rmF$
```

---

## 📁 Struktur File

```
kantinku-app/
├── index.html          # Aplikasi utama (single file)
├── README.md           # Dokumentasi proyek
└── screenshot/         # (opsional) Screenshot aplikasi
```

---

## 🎨 Desain UI

- **Warna Utama**: Gradient oranye-kuning (`#FF6B35` → `#FFCD3C`)
- **Font**: Sora (judul), Inter (teks)
- **Layout**: Mobile-first, max-width 384px, bottom navigation
- **Komponen**: Card menu, modal detail, toast notification, skeleton loading

---

## 🔄 Alur Aplikasi

```
[Splash / Auth]
    ↓ Login / Register (FakeStoreAPI)
[Home]
    → Browse menu per kategori
    → Search menu
    → Klik item → Modal detail → Tambah ke keranjang
    ↓
[Keranjang]
    → Edit qty item
    → Lihat total & biaya layanan
    → Checkout → Modal sukses
    ↓
[Riwayat]
    → Daftar semua pesanan
    → Tandai selesai
    ↓
[Profil]
    → Info akun & statistik belanja
    → Logout
```

---

## 👨‍💻 Dibuat Oleh

Dibuat sebagai proyek tugas pengembangan aplikasi mobile.

---

## 📄 Lisensi

MIT License – bebas digunakan dan dimodifikasi.
