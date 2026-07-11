# POS Warung Salem

Web App Kasir (Point of Sale) untuk Warung Salem.

## Fitur (V2)
- Login Admin
- Manajemen Produk (nama, harga, kategori, stok)
- Keranjang belanja
- Riwayat Transaksi
- Laporan (Daily, Weekly, Monthly, Yearly)
- Update stok otomatis setelah transaksi

## Tech Stack
- HTML + Tailwind CSS + JavaScript
- Firebase (Firestore + Authentication)
- Hosting: Cloudflare Pages

## Cara Setup Firebase

1. Buka [Firebase Console](https://console.firebase.google.com/)
2. Buat project baru
3. Aktifkan **Firestore Database** (production mode)
4. Aktifkan **Authentication** → Email/Password
5. Buat user admin di Authentication
6. Copy konfigurasi Firebase ke file `index.html` (ganti bagian `firebaseConfig`)

## Cara Menjalankan

1. Ganti `firebaseConfig` di `index.html`
2. Deploy ke Cloudflare Pages atau buka langsung via Live Server

## Struktur File

```
pos-warung-salem/
├── index.html
└── README.md
```