# 🎓 Tugas Pemrograman Web: Form & Manajemen Data Mahasiswa

Aplikasi web sederhana berbasis **HTML, CSS, dan Vanilla JavaScript** untuk mengelola data mahasiswa secara dinamis di sisi klien (Client-Side). Repositori ini berisi dua tahap pengembangan dari bentuk dasar hingga versi interaktif yang lebih aman dan responsif.

**Identitas Pengembang**
* **Nama:** Reyhan Pebian
* **NIM:** 202212062
* **Program Studi:** Teknik Informatika

---

## 📁 Struktur File

Di dalam proyek ini, terdapat dua buah file utama yang merepresentasikan tahap pembelajaran:

### 1. `index.html` (Versi Dasar)
File ini adalah prototipe awal yang berisi implementasi formulir standar dan fungsi CRUD (Create, Read, Update, Delete) sederhana. 
* **Kekurangan:** Penentuan jumlah hari pada kalender bersifat statis (selalu 31 hari), password ditampilkan secara *plain-text* di tabel, dan aksi pada tabel masih bergantung pada file gambar eksternal (`edit.png` dan `trash.png`).

### 2. `form data mahasiswa.html` (Versi Lanjutan / Final)
Merupakan penyempurnaan dari versi dasar dengan tambahan fitur keamanan, validasi, dan *User Experience* (UX) yang jauh lebih mulus. File ini dirancang agar mandiri (standalone) tanpa memerlukan *asset* eksternal.

---

## ✨ Fitur Unggulan (Versi Final)

Aplikasi pada `form data mahasiswa.html` memiliki beberapa fitur canggih yang dibangun murni menggunakan JavaScript DOM:

1.  **CRUD Client-Side yang Responsif**
    * **Tambah Data:** Input dari form langsung disuntikkan ke dalam tabel secara *real-time*.
    * **Edit Data:** Saat tombol *Edit* ditekan, data di dalam baris tabel akan diekstrak dan dikembalikan ke dalam form untuk diubah.
    * **Hapus Data:** Dilengkapi dengan *Confirmation Dialog* (`Apakah Anda yakin ingin menghapus data ini?`) untuk mencegah penghapusan tanpa sengaja.

2.  **Validasi Kalender Dinamis (Smart Date)**
    Tidak semua bulan memiliki 31 hari. Aplikasi ini memiliki fungsi yang akan mendengarkan (*listen*) perubahan pada *dropdown* Bulan dan Tahun, lalu secara otomatis menyesuaikan jumlah tanggal yang tersedia. *(Contoh: Jika Februari 2024 dipilih, tanggal maksimal adalah 29).*

3.  **Keamanan Visibilitas Password (Eye Toggle)**
    * Dilengkapi tombol interaktif berikon "mata" (menggunakan grafis **SVG** murni) untuk menyembunyikan atau menampilkan input password.
    * Di dalam tabel data, kolom password secara default disensor menjadi karakter asteris (`********`) untuk menjaga privasi, namun dapat diintip kembali dengan mengklik ikon mata di sebelahnya.

---

## 🛠️ Penjelasan Teknis Kodingan (Deep Dive)

Berikut adalah konsep teknis yang diterapkan di dalam kode JavaScript dan CSS:

* **Manipulasi DOM (Document Object Model):** Penggunaan `document.createElement("tr")` dan *Template Literals* (` ` ` `) untuk membangun struktur baris HTML secara dinamis sebelum disematkan ke dalam tabel (`tableBody.appendChild(row)`).
* **Event Handling:** Menggunakan `addEventListener("submit", ...)` pada form dengan `e.preventDefault()` agar halaman tidak mengalami *refresh* saat tombol submit ditekan.
* **Logika Objek Date:** Menggunakan rumus bawaan JS `new Date(year, month, 0).getDate()` untuk menghitung total hari pada bulan tertentu secara akurat.
* **Desain SVG Mandiri:** Alih-alih menggunakan tag `<img>` yang rentan rusak jika file gambar hilang, ikon pada versi final dibuat menggunakan kode SVG yang diinjeksi langsung ke elemen HTML menggunakan properti `innerHTML`.

---

## 🚀 Cara Menjalankan Aplikasi

Aplikasi ini berjalan sepenuhnya di browser (sisi klien) sehingga **tidak memerlukan web server, instalasi Node.js, atau konfigurasi database**.

1.  Pastikan semua file berada dalam satu direktori.
2.  Klik kanan pada file `form data mahasiswa.html`.
3.  Pilih **"Open with"** (Buka dengan), lalu pilih browser andalan Anda (Google Chrome, Firefox, Edge, dll).
4.  Aplikasi sudah siap digunakan untuk simulasi penginputan data!
