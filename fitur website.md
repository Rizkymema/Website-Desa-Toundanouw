# 🏘️ Daftar Fitur Website Resmi Desa Toundanouw

Website Resmi Desa Toundanouw adalah portal informasi dan pelayanan digital desa berbasis Next.js (React) dan Supabase. Website ini dirancang dengan antarmuka premium, responsif, dan dinamis, terbagi menjadi dua area utama: **Halaman Publik (Umum)** dan **Admin Panel (Pengelolaan)**.

---

## 🌐 1. Fitur Halaman Publik (Umum / Warga)

Halaman ini dapat diakses oleh seluruh warga dan masyarakat umum secara terbuka untuk memperoleh informasi seputar Desa Toundanouw:

### A. Beranda (Homepage - `/`)
- **Hero Slider**: Slide gambar selamat datang dinamis yang diatur dari database, dilengkapi teks deskripsi dengan *dark overlay* kontras tinggi agar mudah dibaca.
- **Menu Navigasi Cepat**: Akses cepat ke Profil Desa, Potensi Desa, Berita Desa, dan E-Surat.
- **Profil Singkat**: Menampilkan informasi singkat mengenai lokasi geografis, statistik jumlah penduduk, dan luas wilayah.
- **Berita & Pengumuman Terbaru**: Grid kartu berita terbaru yang terbit otomatis dengan badge kategori (Kegiatan, Pembangunan, Pengumuman, dll.).
- **Layanan E-Surat Mandiri**: Panduan singkat cara mengurus surat mandiri beserta status ketersediaan template surat.
- **Galeri Foto Kegiatan**: Menampilkan dokumentasi foto kegiatan desa terpopuler (*Featured*).
- **Kontak & Jam Layanan Cepat**: Menampilkan alamat kantor, WhatsApp, email resmi, dan jam operasional layanan secara terintegrasi.

### B. Profil Desa (`/profil`)
- **Profil Umum & Deskripsi Geografis**: Informasi umum letak geografis wilayah, batasan wilayah, dan pembagian jaga (dusun).
- **Visi & Misi Desa**: Arah pembangunan desa yang ditampilkan secara terstruktur dan elegan.
- **Struktur Pemerintahan**: Bagan dan daftar nama perangkat desa lengkap dengan foto, jabatan, NIP, serta email kontak masing-masing perangkat.
- **Galeri Foto & Dokumentasi Terkait**: Foto-foto suasana desa dan fasilitas publik.

### C. Jelajahi Desa (Fitur Tambahan)
- **Sejarah Desa (`/jelajahi/sejarah`)**: Alur waktu (*timeline*) sejarah berdirinya Desa Toundanouw beserta daftar nama Hukum Tua (Kepala Desa) yang menjabat dari masa ke masa.
- **Wilayah Desa (`/jelajahi/wilayah`)**: Peta wilayah terintegrasi Google Maps, batas administratif wilayah, serta grafik penggunaan lahan (pemukiman, sawah, perkebunan).
- **Penduduk & Demografi (`/jelajahi/penduduk`)**: Dashboard infografis kependudukan meliputi:
  - Jumlah total jiwa dan Kepala Keluarga (KK).
  - Grafik perbandingan jenis kelamin (laki-laki/perempuan).
  - Pembagian rentang umur (balita, anak-anak, remaja, produktif, lansia).
  - Statistik mata pencaharian/pekerjaan warga.
  - Statistik tingkat pendidikan warga.
- **Organisasi Desa (`/jelajahi/organisasi`)**: Daftar organisasi kemasyarakatan yang aktif di desa (PKK, Karang Taruna, LPM, BPD, dll.) lengkap dengan nama pengurus inti dan jumlah anggota.

### D. Potensi Desa (`/potensi`)
- **Katalog Potensi Lokal**: Menampilkan komoditas utama (pertanian/perkebunan seperti jagung, kelapa, padi) serta potensi pariwisata lokal yang dimiliki Desa Toundanouw.
- **Detail Potensi**: Deskripsi produk/lokasi, pemilik/pengelola, estimasi nilai ekonomi, dan dokumentasi foto.

### E. Berita Desa (`/berita` & `/berita/[slug]`)
- **Portal Berita Lengkap**: Daftar berita lengkap dengan fitur pencarian dan filter berdasarkan kategori (Pengumuman, Kegiatan, Pembangunan, Bansos).
- **Halaman Detail Berita**: Halaman artikel berita yang SEO-friendly, dilengkapi info penulis, tanggal terbit, jumlah tayangan (*view count*), dan integrasi gambar.

### F. Layanan E-Surat Mandiri (`/surat`)
- **Download Template Mandiri**: Warga dapat mengunduh secara gratis dokumen template surat administrasi desa (format `.docx` / Word) seperti:
  - Surat Keterangan Domisili
  - Surat Keterangan Usaha (SKU)
  - Surat Pengantar SKCK
  - Surat Keterangan Tidak Mampu (SKTM)
- **Pencarian & Filter**: Mempermudah pencarian surat berdasarkan nama dan kategori.
- **FAQ E-Surat**: Kolom tanya jawab seputar tata cara pengurusan, tanda tangan Hukum Tua, dan legalisasi berkas.

### G. Kontak Kami (`/kontak`)
- **Form Kirim Pesan**: Pengunjung/warga dapat mengirimkan pesan, saran, atau aduan langsung ke database admin.
- **Detail Jam Layanan**: Jam operasional kantor desa (Senin - Jumat, 08:00 - 15:00 WITA).
- **Google Maps Embed**: Peta interaktif penunjuk arah menuju Kantor Hukum Tua Desa Toundanouw.

---

## 🔐 2. Fitur Admin Panel (Pengelolaan - `/admin/*`)

Halaman khusus pengelola/perangkat desa untuk memelihara konten website secara mandiri tanpa coding:

### A. Autentikasi & Keamanan (`/admin/login`)
- **Secure Login**: Proteksi halaman dengan hashing sandi dan session token.
- **Role-Based Access Control (RBAC)**:
  - **Super Admin**: Akses penuh ke semua modul, termasuk manajemen akun admin lain.
  - **Admin**: Akses pengelolaan konten (berita, galeri, surat, potensi), tanpa akses edit pengguna admin.
- **Registrasi Akun Baru**: Untuk mendaftarkan perangkat desa baru sebagai administrator.

### B. Dashboard Utama (`/admin/dashboard`)
- **Statistik Cepat**: Panel ringkasan jumlah berita aktif, total views artikel, jumlah template surat terunduh, dan data kependudukan.
- **Aktivitas Terkini**: Daftar perubahan konten terbaru yang dilakukan oleh sesama admin.
- **Pintasan Cepat**: Tombol sekali klik untuk menulis berita baru atau mengunggah template surat baru.

### C. Manajemen Berita
- **CRUD Berita**: Tambah, baca, ubah, dan hapus artikel berita secara visual.
- **Media Upload**: Upload foto *thumbnail* berita langsung ke server penyimpanan (Supabase Storage).
- **Status Draft/Publish**: Menyimpan berita sebagai draf terlebih dahulu sebelum dipublikasikan ke publik.
- **Auto-Slug & SEO**: Pembuatan otomatis URL ramah mesin pencari berdasarkan judul berita.

### D. Pengelolaan Konten Desa (Profil, Sejarah, Penduduk, Potensi, Galeri)
- **Profil & Pemerintahan**: Edit profil desa, visi misi, serta tambah/edit/hapus daftar perangkat desa (foto, nama, jabatan, NIP).
- **Sejarah & Timeline**: Kelola pencapaian dan sejarah desa per tahun.
- **Data Penduduk**: Input dan perbarui data statistik demografis, pekerjaan, umur, dan pendidikan penduduk.
- **Potensi Desa**: Tambah katalog potensi pertanian, kuliner, pariwisata desa beserta fotonya.
- **Galeri Foto**: Upload, hapus, dan atur urutan foto-foto kegiatan desa agar muncul di halaman publik.

### E. Manajemen Template E-Surat
- **Upload File Template**: Upload file template surat baru (`.docx`/`.pdf`).
- **Kategori & Deskripsi**: Tentukan kategori surat dan berikan panduan pengisian singkat untuk warga.
- **Status Aktif/Nonaktif**: Mengarsipkan sementara template surat agar tidak bisa diunduh warga tanpa menghapusnya dari database.
- **Log Unduhan**: Memantau jumlah total unduhan warga untuk masing-masing surat.

### F. Inbox & Kotak Pesan (`/admin/pesan`)
- **Manajemen Aduan/Pesan**: Membaca pesan masuk dari form kontak warga.
- **Status Read/Unread**: Menandai pesan yang sudah diproses atau dibalas.
- **Hapus Pesan**: Membersihkan kotak masuk dari spam.

### G. Log Aktivitas Admin (`/admin/activity-log`)
- **Audit Trail**: Mencatat setiap tindakan admin (misal: "Admin A mengubah Berita B" lengkap dengan waktu, tindakan, dan alamat IP). Sangat berguna untuk keamanan data desa.

### H. Pengaturan Web & Hero Slides
- **Hero Slider Settings**: Mengatur gambar latar belakang slider di halaman utama, urutan tampil, dan tombol navigasi cepat.
- **Kontak Global**: Edit alamat kantor, WhatsApp, email desa secara terpusat agar langsung tersinkronisasi di seluruh halaman website publik.
