# Damping — Paket Prototipe Dashboard Orang Tua & Keluarga

Paket ini berisi seluruh file prototipe interaktif antarmuka **Dashboard Orang Tua Damping** yang mengintegrasikan konsep pendampingan anak, misi belajar di rumah, dan eksplorasi satwa dari proyek awal Kidvera ke dalam ekosistem **Damping**.

Paket ini dirancang mandiri (*self-contained*), aman, dan terisolasi dari database produksi sehingga siap ditinjau secara lokal maupun diunggah ke GitHub untuk dibagikan kepada Papa Salam.

---

## 1. Daftar Isi File dalam Paket

| Nama File | Fungsi & Deskripsi |
| :--- | :--- |
| **`index.html`** | **File prototipe utama**. Siap dibuka langsung di browser dengan klik ganda atau dijadikan halaman utama jika diunggah ke GitHub Pages. |
| **`damping-parent-prototype.html`** | Salinan identik dari file prototipe dengan penamaan deskriptif. |
| **`README.md`** | Panduan penggunaan, ringkasan fitur, dan langkah mengunggah ke GitHub. |
| **`prototype_report.md`** | Laporan audit mendalam, evaluasi fitur Kidvera yang direkomendasikan vs ditunda, serta analisis arsitektur integrasi. |

---

## 2. Cara Membuka & Menjalankan Demo

1. Buka folder ini melalui **File Explorer** Windows.
2. Klik ganda (**double click**) pada file **`index.html`** (atau `damping-parent-prototype.html`).
3. File akan langsung terbuka di Google Chrome, Microsoft Edge, atau browser default Anda.
4. Anda dapat langsung menguji seluruh menu, mengganti profil anak, menjalankan timer misi belajar, mengisi screening, dan menulis catatan jurnal pengamatan.

---

## 3. Fitur Interaktif yang Dapat Dicoba dalam Demo

1. **Beranda Orang Tua:**
   - Sapaan hangat dan personal untuk orang tua.
   - Menjawab langsung 3 hal penting: proses belajar anak, apa yang bisa dilakukan hari ini, dan langkah berikutnya.
   - Stepper capaian pekan ini (3 dari 5 hari selesai) dan kartu catatan pencapaian kecil (*Small Wins*).
2. **Pemilihan Multi-Anak (Rafi 7 th & Alya 4 th):**
   - Mengganti anak pada dropdown langsung memperbarui seluruh tampilan: sapaan, rekomendasi misi, data profil, riwayat jurnal, dan statistik pencapaian.
3. **Misi Belajar di Rumah & Live Timer:**
   - Katalog 6 aktivitas rumah (*Detektif Daun, Perjalanan Kupu-kupu, Toko-tokoan di Rumah, Cerita Benda Favorit, Tantangan Bangun Menara, Misi Kebaikan Rahasia*).
   - Tombol **"Mulai Misi"** membuka modal interaktif dengan instruksi bertahap dan **Live Countdown Timer 15 Menit** (Play/Pause/Reset).
   - Tombol **"✓ Tandai Misi Selesai"** menambah counter aktivitas, mencatat *Small Win*, dan memunculkan notifikasi toast.
4. **Jurnal Orang Tua (Refleksi Privat):**
   - Formulir refleksi ramah keluarga (*aktivitas, hal yang membuat antusias, kesulitan, respon saat sulit, dan catatan berkesan*).
   - Submit formulir langsung menambahkan kartu jurnal baru ke dalam daftar riwayat dan tersimpan di memori browser.
5. **Screening Awal Pengamatan di Rumah:**
   - Kuesioner pengamatan non-diagnostik seputar respon tantangan, gaya belajar nyaman, dan sensibilitas lingkungan.
   - Tombol **"Simpan & Tampilkan Hasil Pemetaan"** langsung menampilkan rangkuman panduan pendampingan serta karakter satwa pendamping (**Bimo Si Beruang Kuat**).
6. **Profil & Potensi Anak:**
   - Memvisualisasikan minat (Alam, Merakit, Logika), area yang sedang ditumbuhkan (Resiliensi), serta modal formulir **"Edit Data Contoh"** yang bisa disimpan langsung.
7. **Eksplorasi Satwa & Luar Kelas:**
   - Panduan menghubungkan rekreasi keluarga (Kebun Binatang, Museum, Pasar Tradisional) dengan pelajaran sekolah (Sains, Hitung Praktis, Bahasa, Empati).
8. **Layanan Belajar Damping (Sinergi Rumah & Les Privat):**
   - Menampilkan kartu guru les aktif (**Miss Hasna**) dan tombol **"Buka Laporan Sesi Lengkap"** yang memunculkan laporan evaluasi sesi les privat Damping.
   - Simulasi konsultasi kebutuhan guru tambahan di Damping Marketplace.
9. **Pengaturan & Reset Demo:**
   - Pengaturan privasi berbagi laporan ke guru, serta tombol **"Reset Seluruh Data Demo"** untuk mengembalikan presentasi ke kondisi awal kapan saja.

---

## 4. Ketergantungan Aset (Koneksi Internet)

- **Logika & Tampilan:** Seluruh script interaksi, state multi-anak, timer hitung mundur, dan penyimpanan jurnal berjalan 100% lokal di browser Anda.
- **Koneksi Internet:** Diperlukan koneksi internet ringan saat pertama kali membuka halaman untuk memuat:
  1. Tailwind CSS CDN (tata letak dan warna).
  2. Google Fonts (*Plus Jakarta Sans* dan *Playfair Display*).
- **Database & Server:** Sama sekali **TIDAK** membutuhkan koneksi database atau server backend. Data tidak akan dikirim ke layanan eksternal mana pun.

---

## 5. Cara Mengunggah Paket Ini ke GitHub Melalui Browser (Tanpa Terminal)

Jika Anda ingin membagikan demo ini kepada Papa Salam agar bisa dibuka langsung lewat link web di HP atau laptopnya:

### Langkah A: Buat Repositori Baru di GitHub
1. Buka [github.com](https://github.com/) dan pastikan Anda sudah login ke akun `rahmaobseveranak-gif`.
2. Klik tombol **New** (atau ikon `+` di kanan atas lalu pilih **New repository**).
3. Beri nama repositori, misalnya: `damping-parent-prototype` atau `damping-dashboard-ortu`.
4. Pilih **Public**.
5. Centang opsi **Add a README file** (opsional), lalu klik **Create repository**.

### Langkah B: Unggah File Paket
1. Di halaman repositori baru tersebut, klik tombol **Add file** lalu pilih **Upload files**.
2. Buka folder `Damping-Parent-Prototype-Package` di File Explorer komputer Anda.
3. Tarik (*drag and drop*) file:
   - `index.html`
   - `README.md`
   - `prototype_report.md`
   ke dalam kotak upload di browser.
4. Pada bagian bawah, ketik pesan commit: `feat: add Damping parent dashboard prototype`.
5. Klik tombol hijau **Commit changes**.

### Langkah C: Aktifkan GitHub Pages (Agar Menjadi Link Web yang Bisa Diklik)
1. Di repositori GitHub tersebut, klik tab **Settings** (ikon roda gigi di kanan atas).
2. Di menu sebelah kiri, pilih **Pages**.
3. Pada bagian **Build and deployment** -> **Branch**:
   - Ganti *None* menjadi **`main`** (atau `master`).
   - Folder biarkan tetap **`/(root)`**.
   - Klik **Save**.
4. Tunggu 1–2 menit, GitHub akan menampilkan URL web aktif, misalnya:  
   `https://rahmaobseveranak-gif.github.io/damping-parent-prototype/`
5. Kirimkan link tersebut kepada Papa Salam. Beliau bisa langsung membuka, melihat desain, dan mencoba interaksinya di HP maupun laptop tanpa perlu menginstal apa pun.

---

*Damping — Dari Guru Indonesia, oleh Guru Indonesia, untuk Siswa dan Orang Tua di mana pun berada.*
