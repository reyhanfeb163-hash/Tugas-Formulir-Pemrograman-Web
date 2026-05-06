# Tugas-Formulir-Pemrograman-Web
Repository ditujukan untuk tugas 1 Pemrograman Web

# 🎓 Sistem Manajemen Data Mahasiswa (Vanilla JS)

Aplikasi web sederhana berbasis HTML, CSS, dan Vanilla JavaScript untuk mengelola input data mahasiswa. Proyek ini dibangun dengan fokus pada manipulasi DOM (Document Object Model), penanganan *event* (Event Handling), dan validasi form yang interaktif.

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-323330?style=for-the-badge&logo=javascript&logoColor=F7DF1E)

---

## ✨ Fitur Utama

Aplikasi ini tidak hanya menampilkan formulir statis, melainkan dilengkapi dengan berbagai fitur cerdas dan dinamis:

* **📝 Operasi CRUD Dasar:** Mendukung operasi *Create* (menambah), *Read* (menampilkan di tabel), *Update* (mengedit), dan *Delete* (menghapus) data secara lokal (*client-side*).
* **📅 Kalender Dinamis (Smart TTL):** Dropdown tanggal lahir otomatis menyesuaikan jumlah hari berdasarkan bulan dan tahun yang dipilih. Secara cerdas mendeteksi bulan yang berakhir di tanggal 28, 30, atau 31, termasuk **Tahun Kabisat**.
* **👁️ Keamanan Kata Sandi (Hide/Show):** Dilengkapi fitur untuk menyembunyikan atau melihat kata sandi dengan ikon mata (SVG) yang interaktif, baik pada form input maupun di dalam baris tabel data.
* **🛡️ Proteksi Hapus Data:** Integrasi *pop-up* konfirmasi (Confirmation Box) sebelum data dihapus untuk mencegah *human error* (salah klik).
* **🔄 Sinkronisasi Edit Presisi:** Saat mode "Edit" diaktifkan, data *Radio Button* (Jenis Kelamin) dan *Dropdown* (Tanggal Lahir) akan dipulihkan secara otomatis dan presisi ke dalam form, tidak hanya elemen teks saja.

## 🚀 Cara Menjalankan (Instalasi)

Proyek ini dibangun murni menggunakan teknologi *front-end* standar tanpa memerlukan instalasi *framework* atau server tambahan.

1. *Clone* repository ini ke komputer lokal Anda:
   ```bash
   git clone [https://github.com/username/repo-data-mahasiswa.git](https://github.com/username/repo-data-mahasiswa.git)
