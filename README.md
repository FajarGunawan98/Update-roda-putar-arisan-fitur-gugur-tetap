# Undian Arisan (PWA)

Aplikasi undian arisan (roda putar + globe bola) yang bisa dipasang seperti
aplikasi biasa di HP, lewat GitHub Pages.

## Isi folder

```
index.html          -> halaman utama
manifest.json        -> info aplikasi (nama, ikon, warna)
service-worker.js    -> supaya bisa dibuka tanpa internet setelah pertama kali dibuka
favicon.ico
icons/
  icon-192.png
  icon-512.png
  icon-512-maskable.png
  apple-touch-icon.png
```

## Cara pasang ke GitHub Pages (tanpa perlu ngoding)

1. Buka https://github.com, login atau buat akun dulu kalau belum punya.
2. Klik tombol **+** di kanan atas → **New repository**.
   - Repository name: bebas, misal `undian-arisan`.
   - Pilih **Public**.
   - Klik **Create repository**.
3. Di halaman repo yang baru dibuat, klik **uploading an existing file**
   (atau menu **Add file → Upload files**).
4. Seret (drag & drop) **semua isi folder ini** (bukan foldernya, tapi
   file-file dan folder `icons` di dalamnya) ke halaman upload itu.
5. Scroll ke bawah, klik **Commit changes**.
6. Masuk ke tab **Settings** (di repo yang sama) → menu **Pages** di sidebar
   kiri.
7. Di bagian **Build and deployment → Branch**, pilih branch `main` dan
   folder `/ (root)`, lalu klik **Save**.
8. Tunggu 1-2 menit, refresh halaman Settings → Pages tadi. Akan muncul
   link seperti:
   `https://<username-github-kamu>.github.io/undian-arisan/`
9. Buka link itu di HP.

## Cara pasang sebagai aplikasi di HP

**Android (Chrome):**
1. Buka link GitHub Pages di atas.
2. Ketuk menu titik tiga di pojok kanan atas Chrome.
3. Pilih **Tambahkan ke Layar Utama / Install aplikasi**.
4. Ikon "Undian Arisan" akan muncul di HP, bisa dibuka seperti aplikasi
   biasa (tanpa address bar).

**iPhone (Safari):**
1. Buka link GitHub Pages di atas lewat **Safari** (bukan Chrome).
2. Ketuk ikon **Share/Bagikan** (kotak dengan panah ke atas).
3. Pilih **Add to Home Screen / Tambah ke Layar Utama**.
4. Ikon akan muncul di layar utama.

## Update tampilan setelah sudah online

Kalau nanti mau mengubah undian-arisan (misalnya minta saya ubah lagi),
tinggal upload ulang file `index.html` yang baru dengan cara yang sama
(langkah 3-5 di atas, GitHub akan menimpa file lama). Setelah itu, di
`service-worker.js`, naikkan angka pada baris:

```
const CACHE = 'undian-arisan-v1';
```

menjadi `v2`, `v3`, dst — supaya HP yang sudah pernah membuka aplikasi ini
otomatis mengambil versi terbaru, bukan versi lama yang tersimpan.

## Catatan

- Karena berjalan di GitHub Pages (bukan server sendiri), data hasil
  undian tetap hanya tersimpan di browser/HP masing-masing orang yang
  membuka (seperti sebelumnya), bukan di GitHub.
- Repo boleh **Public**; tidak ada data pribadi yang tersimpan di kode ini.
