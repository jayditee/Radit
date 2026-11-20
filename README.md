# AKSESTAMA — Mobile UI/UX Prototype (GOVTHINK UNESA 2026)

Struktur proyek ini dipisah secara modular agar rapi, mudah dibaca, dan nyaman diedit di **Visual Studio Code**.

## Struktur Folder
```text
aksestama-mobile-vscode/
├── index.html      # Struktur utama antarmuka mobile & komponen layar
├── css/
│   └── style.css   # Styling Neo-Civic Spatial UI, Glassmorphism & Mode Kontras Tinggi WCAG AAA
├── js/
│   └── app.js      # Logika multi-aktor, Audit Pintar demo lokal, Inklusi+, & Budget Lock APBD
└── README.md       # Panduan penggunaan di VS Code
```

## Cara Menjalankan di Visual Studio Code
1. Ekstrak file ZIP ini ke dalam satu folder.
2. Buka folder tersebut di **VS Code** (`File > Open Folder...`).
3. Klik kanan pada file `index.html`, lalu pilih **Open with Live Server** (atau buka langsung `index.html` di browser).

## Navigasi Aplikasi
- Navigasi bawah memiliki lima menu: **Beranda**, **Peta**, **Lapor**, **Aksi Muda**, dan **Profil**.
- Halaman **Profil** menyediakan akses ke pusat akun serta pintasan menuju fitur **Inklusi+** dan dashboard pemerintah **APBD**.

## Aksesibilitas Antarmuka
- Pembesaran halaman browser tidak dikunci. Navigasi utama dan kontrol penting memiliki target sentuh yang diperbesar serta indikator fokus keyboard.
- Teks informasi kecil diperbesar agar lebih mudah dibaca; mode kontras tinggi dan pengurangan animasi dari preferensi perangkat didukung.

## Audit Pintar
- Gunakan **Ambil Foto** untuk kamera perangkat atau **Dari Galeri** untuk memilih gambar JPG, PNG, atau WebP (maksimal 10 MB).
- Isi nama dan jenis fasilitas, deskripsi kerusakan, serta alamat. Lokasi perangkat hanya diminta setelah tombol lokasi ditekan; alamat juga dapat dimasukkan manual.
- Analisis gambar berjalan lokal di browser dengan pengukuran variasi tekstur sederhana. Ini **bukan model AI terlatih dan bukan deteksi kerusakan yang tervalidasi**; hasil tingkat ringan/sedang/berat hanya indikasi demo dan perlu pemeriksaan manusia.
- Laporan beserta foto disimpan di `localStorage` browser perangkat ini dan tidak dikirim ke server. Data bisa hilang jika data situs/browser dihapus atau penyimpanan perangkat penuh.
- Untuk memakai kamera dan geolokasi di ponsel, jalankan melalui Live Server/localhost atau situs HTTPS dan berikan izin perangkat yang diminta.

## Peta Akses
- Buka menu **Peta** dari navigasi bawah untuk melihat penanda fasilitas, memfilter lokasi ramah akses/perlu perhatian, dan memilih lokasi dari peta atau daftar.
- Detail lokasi menampilkan kondisi trotoar, guiding block, ramp, serta rekomendasi rute dan langkah-langkahnya.
- Peta, kondisi, jarak, dan rute saat ini bersifat ilustrasi/demo; belum terhubung ke peta geografis, koordinat fasilitas terverifikasi, GPS, maupun layanan navigasi.

## Aksi Muda
- Tab **Aksi Muda** menampilkan detail profil kontribusi, poin, level, badge, leaderboard, riwayat, dan misi mingguan.
- Laporan Audit Pintar berstatus menunggu belum mendapat poin. Dalam demo, peran Bappeda dapat mensimulasikan validasi; laporan valid memberi 50 poin dan progres misi dapat memberi bonus.
- Progres disimpan lokal per peran di browser. Validasi dan leaderboard belum memakai server atau akun terotorisasi, sehingga bukan catatan resmi dan tidak aman untuk produksi.

## Dashboard Pemerintah
- Pilih **Profil > Dashboard Pemerintah · APBD** untuk melihat statistik status laporan, peta persebaran skematis, daftar dan detail laporan, klasifikasi prioritas, serta rekap untuk evaluasi kebijakan.
- Dashboard menggabungkan data contoh dengan laporan Audit Pintar di browser ini. Peran Bappeda dapat mengubah status tindak lanjut demo menjadi **Menunggu**, **Diproses**, atau **Selesai**; perubahan disimpan lokal.
- Peta, klasifikasi, status, dan rekap bukan data resmi atau inspeksi teknis. Integrasi produksi memerlukan sumber data terverifikasi, koordinat nyata, backend, dan autentikasi/otorisasi server.

## Fitur Pendukung
- Login tetap dapat digunakan sebagai demo tanpa registrasi. Jika email terdaftar di browser ini, kata sandi diverifikasi; akun baru dari **Daftar** langsung masuk. Akun disimpan lokal dan kata sandi tersimpan sebagai hash PBKDF2, bukan teks biasa.
- Pilih menu **Profil** atau ketuk avatar di header untuk membuka **Pusat Akun**: ubah nama profil, lihat notifikasi dan riwayat Audit Pintar, atur tema/kontras/bantuan suara serta preferensi notifikasi, atau buka FAQ.
- Notifikasi dibentuk dari status laporan lokal dan aktivitas Aksi Muda demo. Riwayat dan preferensi tidak tersinkron ke perangkat lain.
- Autentikasi, pemilihan peran, validasi Bappeda, notifikasi, dan data profil sepenuhnya berupa simulasi browser. Ini bukan sistem akun yang aman untuk produksi; jangan gunakan kata sandi penting. Jangan mencatat data sensitif karena penyimpanan browser dapat diakses atau dihapus oleh pengguna perangkat.
