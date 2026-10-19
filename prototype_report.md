# Laporan Prototype UI/UX Dashboard Orang Tua Damping

> [!NOTE]
> Prototype ini dibuat sebagai pengujian visual dan alur interaksi antarmuka orang tua yang terisolasi dari database produksi, migration, dan dashboard guru Damping. Seluruh state demo berjalan mandiri di memori browser lokal (*Client-Side State Engine*).

---

## 1. Lokasi File & Cara Menjalankan Prototype

Prototype telah disediakan dalam bentuk file HTML mandiri (*self-contained*) yang dapat dibuka langsung melalui browser mana pun tanpa memerlukan instalasi dependensi tambahan:

- **Lokasi Utama (Langsung Klik & Buka di Browser):**  
  [damping-parent-prototype.html](file:///c:/Users/User/Downloads/kidvera-parent-guide-main%20%284%29/kidvera-parent-guide-main/public/damping-parent-prototype.html)
- **Salinan di Folder Proyek Damping:**  
  [damping-parent-prototype/index.html](file:///c:/Users/User/Downloads/lesapp-main%20%2854%29/damping-parent-prototype/index.html)  
  [lesapp-main/public/damping-parent-prototype.html](file:///c:/Users/User/Downloads/lesapp-main%20%2854%29/lesapp-main/public/damping-parent-prototype.html)

### Cara Membuka:
1. **Cara 1 (Paling Mudah):** Klik tautan file di atas atau klik ganda file `damping-parent-prototype.html` di File Explorer Windows Anda. File akan langsung terbuka di Google Chrome atau browser default Anda.
2. **Cara 2 (Jika Dev Server Vite Damping Sedang Berjalan):** Buka URL:
   `http://localhost:5173/damping-parent-prototype.html`

---

## 2. Galeri Hasil Pengujian Interaksi Browser

Sesi pengujian interaktif telah dijalankan dan direkam melalui browser automation subagent.

````carousel
![Beranda Orang Tua Damping (Tema Hijau Sage & Krem Hangat)](file:///C:/Users/User/.gemini/antigravity-ide/brain/85e24381-49ce-4e25-8c01-63901f81fe98/dashboard_initial_1792365287976.png)
<!-- slide -->
![Beralih Profil Anak Aktif: Alya (4 tahun)](file:///C:/Users/User/.gemini/antigravity-ide/brain/85e24381-49ce-4e25-8c01-63901f81fe98/dashboard_alya_1792365305957.png)
<!-- slide -->
![Modal Misi Belajar: Langkah demi Langkah & Live Countdown Timer](file:///C:/Users/User/.gemini/antigravity-ide/brain/85e24381-49ce-4e25-8c01-63901f81fe98/timer_started_1792365360888.png)
<!-- slide -->
![Formulir Jurnal Pengamatan Orang Tua & Submit Catatan Baru](file:///C:/Users/User/.gemini/antigravity-ide/brain/85e24381-49ce-4e25-8c01-63901f81fe98/jurnal_saved_1792365483765.png)
<!-- slide -->
![Hasil Screening Awal Pengamatan di Rumah](file:///C:/Users/User/.gemini/antigravity-ide/brain/85e24381-49ce-4e25-8c01-63901f81fe98/screening_report_1792365549069.png)
<!-- slide -->
![Integrasi Guru Damping: Preview Laporan Sesi Les Privat #12](file:///C:/Users/User/.gemini/antigravity-ide/brain/85e24381-49ce-4e25-8c01-63901f81fe98/tutor_report_modal_open_1792365623027.png)
<!-- slide -->
![Tampilan Responsif Mobile (375x812) dengan Bottom Navigation](file:///C:/Users/User/.gemini/antigravity-ide/brain/85e24381-49ce-4e25-8c01-63901f81fe98/mobile_view_1792365647221.png)
````

---

## 3. Fitur yang Berfungsi Penuh vs Fitur Simulasi

| Menu / Fitur | Status dalam Prototype | Keterangan Interaksi |
| :--- | :---: | :--- |
| **Navigasi Antarmenu (9 Menu)** | **Berfungsi Penuh** | Sidebar desktop & bottom bar mobile berpindah layar instan tanpa reload halaman (*Single Page App*). |
| **Pemilihan Multi-Anak (Rafi / Alya)** | **Berfungsi Penuh** | Memilih anak langsung memperbarui sapaan, 3 jawaban penting, rekomendasi misi, data profil, riwayat jurnal, dan statistik capaian. |
| **Player Misi & Live Timer** | **Berfungsi Penuh** | Modal misi menampilkan langkah instruksi, timer hitung mundur 15 menit (Play/Pause/Reset), serta tombol *Tandai Selesai* yang otomatis menambah counter dan mencatat *small win*. |
| **Jurnal Orang Tua Interaktif** | **Berfungsi Penuh** | Form pencatatan refleksi dapat dibuka/tutup, diisi, dan saat disubmit langsung menambahkan kartu entri baru di arsip jurnal (tersimpan di *localStorage*). |
| **Screening Awal Pengamatan** | **Berfungsi Penuh** | Kuesioner pilihan ganda + textarea catatan bebas. Saat disubmit, langsung menghasilkan kartu analisis panduan pendampingan & karakter satwa. |
| **Edit Profil Anak** | **Berfungsi Penuh** | Modal edit dapat memperbarui nama, usia, jenjang sekolah, dan tujuan pendampingan orang tua secara dinamis. |
| **Reset Data Demo** | **Berfungsi Penuh** | Tombol reset mengembalikan seluruh data anak, jurnal, dan status misi ke kondisi awal presentasi. |
| **Laporan Guru Damping** | *Simulasi Representatif* | Menampilkan modal pratinjau laporan sesi les privat guru (Miss Hasna) untuk mendemonstrasikan bagaimana data guru bersinergi dengan data rumah. |
| **Eksplorasi Satwa & Luar Kelas** | *Simulasi Edukatif* | Kartu kategori tema eksplorasi alam, museum, dan panduan akhir pekan tanpa transaksi komersial. |

---

## 4. Analisis Rekomendasi Fitur Kidvera untuk Damping

### A. Fitur yang Direkomendasikan Segera Diintegrasikan ke Damping
1. **Katalog Misi Belajar Mandiri di Rumah:**  
   Sangat melengkapi sesi les privat Damping. Guru les mengajar 1–2 kali seminggu, sementara orang tua memiliki panduan bermain 15 menit di hari-hari lainnya.
2. **Jurnal Refleksi & Catatan Pencapaian Kecil (*Small Wins*):**  
   Memberikan rasa tenang bagi orang tua dan menjadi dokumentasi berharga yang bisa (secara opsional) dibagikan rangkumannya kepada guru les Damping.
3. **Karakter Pendamping Edukatif (Bimo, Rara, Mimi, Tomo):**  
   Memberikan sentuhan hangat dan metafora yang mudah dipahami anak tanpa membuat anak merasa sedang diuji.
4. **Dual Mode Portal Orang Tua:**  
   Orang tua yang ingin cepat cukup memasukkan kode 6 digit untuk bayar SPP & lihat nilai (fitur Damping lama), sedangkan orang tua yang ingin pendampingan holistik dapat mendaftar akun Damping Keluarga.

### B. Fitur yang Sebaiknya Ditunda / Tidak Dimasukkan
1. **Label Psikiatri / Sensoris Kaku (*Hyper / Hypo*):**  
   Dihindari karena berisiko memicu kecemasan orang tua tanpa diagnosa profesional. Digantikan dengan istilah yang lebih ramah seperti *"Sensibilitas Lingkungan"* dan *"Kecenderungan Eksplorasi"*.
2. **Generasi Gambar AI Real-Time via Edge Function:**  
   Menambah latensi dan biaya API. Lebih baik menggunakan ilustrasi statis berkualitas tinggi yang dirancang oleh tim desain.
3. **Sistem Co-Parenting / Family Invites Kompleks:**  
   Ditunda ke fase berikutnya agar tidak memperumit skema autentikasi awal.

---

## 5. Komponen Damping yang Dapat Digunakan Kembali

Ketika integrasi ke dalam codebase TanStack Start Damping dimulai:
- **`PhoneShell` & `BottomNavOrtu` (`src/components/ui-kit.tsx`):** Dapat langsung membungkus antarmuka mobile dashboard orang tua.
- **`ParentDashboardTabs.tsx`:** Tab *Misi Rumah*, *Jurnal*, dan *Eksplorasi* dapat ditambahkan sebagai tab baru bersanding dengan tab *Sesi Les*, *Tugas Suara*, dan *Pembayaran SPP*.
- **Desain Token Damping (`tailwind.config`):** Warna Sage (`#2D5A43`), Cream (`#FBF9F5`), dan tipografi *Plus Jakarta Sans* sudah 100% selaras dengan identitas Damping.

---

## 6. Konfirmasi Batasan Keamanan

> [!IMPORTANT]
> **KONFIRMASI INTEGRITAS PRODUKSI:**
> - Database produksi Damping (`biezfryhywjnjdoqecow`) **SAMA SEKALI TIDAK TERSENTUH**.
> - Tidak ada migration SQL yang dijalankan.
> - Tidak ada schema atau tabel database yang diubah.
> - Dashboard guru (`/guru`) dan sistem pembayaran yang berjalan tetap 100% utuh tanpa modifikasi.
> - File prototype disimpan secara terisolasi sebagai aset HTML statis.
