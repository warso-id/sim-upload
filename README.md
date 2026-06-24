# SIM Upload - Portal Akademik

Aplikasi untuk mengelola layanan upload dokumen akademik dengan fitur lengkap.

## 🚀 Fitur
- Tampilan carousel interaktif dengan efek 3D
- Filter kategori, pencarian, dan mode grid/carousel
- Favorit dan penghitung klik per layanan
- Leaderboard popularitas
- Tema terang/gelap
- **Admin Dashboard** untuk mengelola konten (CRUD)

## 🔧 Instalasi

1. Clone repository ini
2. Buka `index.html` di browser

## 🔐 Admin Backend

### Deployment Google Apps Script
1. Buka [script.google.com](https://script.google.com)
2. Buat project baru, tempelkan `code.gs`
3. Klik **Deploy** → **New Deployment** → **Web App**
4. Set **Execute as** = `Me`, **Who has access** = `Anyone`
5. Copy URL Web App
6. **Jalankan fungsi `setAdminCredentials()` sekali** untuk menyimpan username/password
7. Update `GAS_URL` di `admin-login.html` dengan URL Web App

### Login Admin
- Username: `admin` (default, bisa diubah via fungsi `setAdminCredentials()`)
- Password: `admin123` (default, segera ganti!)

## 📁 Struktur File
- `index.html` - Halaman utama (data dari localStorage)
- `admin-login.html` - Halaman login admin
- `admin-dashboard.html` - Dashboard CRUD
- `code.gs` - Backend Google Apps Script (JANGAN diupload ke GitHub!)
- `.gitignore` - File yang tidak boleh diupload

## 🛡️ Keamanan
- Credentials disimpan di **Google Apps Script Properties** (bukan di kode)
- Session menggunakan `sessionStorage`
- File `code.gs` **tidak boleh diupload** ke GitHub (gunakan .gitignore)

## 📝 Maintenance
- Tambah/edit/hapus konten melalui dashboard admin
- Data disimpan di `localStorage` browser dengan kunci `simupload_data`

## 📄 Lisensi
MIT