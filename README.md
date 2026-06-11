 KantinKu

Aplikasi mobile web pemesanan makanan kantin modern, cepat, dan mudah digunakan Tentang Proyek

KantinKu adalah aplikasi pemesanan makanan kantin berbasis mobile web(single HTML file) yang dibangun sebagai proyek tugas pengembangan aplikasi mobile. Pengguna dapat login, memilih menu, menambahkan ke keranjang, melakukan checkout, dan melihat riwayat transaksi  semua dalam satu halaman yang responsif.



Fitur

 1  Autentikasi Login & Register menggunakan FakeStoreAPI 
 2  List Menu 20 menu kantin dengan foto makanan nyata (Unsplash) 
 3   Search & Filter  Cari menu by nama; filter by kategori (Makanan, Minuman, Snack, Dessert) 
 4   Keranjang Tambah/kurangi/hapus item dengan perhitungan total otomatis 
 5  Checkout| Pesan dengan nomor order unik + modal konfirmasi sukses 
 6   Riwayat Transaksi Histori semua pesanan beserta detail & status 
 7   Profil  Info akun, statistik belanja, dan tombol logout


 Teknologi

 Teknologi | Kegunaan 
 HTML5  Struktur aplikasi
 Tailwind CSS CDN  Styling & layout responsif mobile-first 
Vanilla JavaScript Logic aplikasi tanpa framework
Google Fonts Sora & Inter  Tipografi 
FakeStoreAP Autentikasi (login & register) 
Unsplash Foto makanan untuk tiap menu 

---

Integrasi API

FakeStoreAPI  Autentikasi

Base URL: https://fakestoreapi.com


 Method | Endpoint | Fungsi |
 `POST`  `/auth/login`  Login pengguna, mendapat JWT token |
 `POST`  `/users` Registrasi akun baru 
 `GET`   `/users` Ambil data profil pengguna 

Contoh request login:
json
POST https://fakestoreapi.com/auth/login
Content-Type: application/json

{
  "username": "johnd",
  "password": "m38rmF$"
}


Response sukses:
json
{
  "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9"
}

Catatan: Jika API tidak dapat dijangkau, aplikasi otomatis masuk mode offline dan tetap bisa digunakan.

Cara Menjalankan

Opsi 1 Buka Langsung di Browser
bash
git clone https://github.com/[username]/kantinku-app.git
cd kantinku-app 
Double-click index.html, atau:
open index.html

Opsi 2 Live Server (VS Code)
1. Install ekstensi Live Server
2. Klik kanan `index.html` → Open with Live Server

Opsi 3  Python HTTP Server
bash
python3 -m http.server 8080 
Buka: http://localhost:8080

 Akun Demo

Username : johnd
Password : m38rmF$



Struktur Proyek

kantinku-app/
├── index.html       Seluruh aplikasi (HTML + CSS + JS)
└── README.md     Dokumentasi ini

Aplikasi dibuat sebagai single file agar mudah di-deploy dan dijalankan tanpa build step apapun.

Kategori Menu

| Kategori | Jumlah | Contoh |
Makanan 8 item  Nasi Goreng, Ayam Bakar, Rendang 
Minuman 4 item  Es Teh, Jus Alpukat, Kopi Gula Aren 
Snack 4 item Risol Mayo, Siomay, Batagor 
Dessert  4 item Klepon, Puding Cokelat, Pisang Goreng 


Desain UI

- Warna utama Gradient oranye → kuning `#FF6B35` → `#FFCD3C`
- Font: Sora (heading), Inter (body)
- Layout: Mobile-first, max-width 384px, bottom navigation bar
- Animasi: Slide-up modal, fade-in screen, skeleton loading, toast notification
- Komponen: Card menu grid, modal detail item, keranjang interaktif, riwayat transaksi

Alur Aplikasi

  Auth Screen   ← Login / Register via FakeStoreAPI
┌─────────────┐
│    Home      │  ← Browse menu, search, filter kategori
│              │  ← Klik item → Modal detail → Tambah ke keranjang
└──────┬──────┘
       ↓
┌─────────────┐
│  Keranjang   │  ← Edit qty, lihat subtotal + biaya layanan
│              │  ← Checkout → Modal sukses + nomor order
└──────┬──────┘
       ↓
┌─────────────┐
│   Riwayat   │  ← Daftar semua pesanan + status
└──────┬──────┘
       ↓
┌─────────────┐
│   Profil    │  ← Info akun, statistik, logout
└─────────────┘

Dibuat Oleh

Dibuat sebagai proyek tugas mata kuliah Pengembangan Aplikasi Mobile.


Lisensi

[MIT License](LICENSE) — bebas digunakan dan dimodifikasi.

