# STUDENT_TOOLKIT

![Versi Python](https://img.shields.io/badge/Python-3.8+-blue.svg)

Sebuah aplikasi program bantu mahasiswa berbasis terminal (CLI) yang dibuat menggunakan Python. Proyek ini dirancang untuk menyediakan berbagai alat bantu belajar dan produktivitas dalam satu program yang ringan dan mudah digunakan.

---

## Fitur Utama

Aplikasi ini memiliki 7 fitur utama yang dirancang untuk membantu kegiatan akademik:

1.  To-Do List
2.  Timer Pomodoro
3.  Manajemen Waktu Kuliah
4.  Quiz
5.  Flashcard
6.  Formatter Sitasi
7.  Word Counter

---

## Penjelasan Fitur

Berikut adalah penjelasan rinci dari setiap fitur:

### 1. To-Do List
* **Tambah Tugas:** Memungkinkan pengguna memasukkan tugas baru beserta prioritas (Tinggi/Sedang/Rendah), tanggal deadline (opsional), dan catatan.
* **Lihat Semua Tugas:** Menampilkan semua tugas yang belum selesai, diurutkan berdasarkan prioritas atau tanggal.
* **Tandai Selesai:** Memindahkan tugas dari daftar aktif ke daftar selesai.
* **Hapus Tugas:** Menghapus tugas secara permanen.
* **Liat Tugas Selesai:** Menampilkan riwayat tugas yang telah diselesaikan.

### 2. Timer Pomodoro
* Timer produktivitas berdasarkan Teknik Pomodoro.
* Pengguna dapat mengatur durasi sesi "Kerja" (default: 25 menit) dan sesi "Istirahat" (default: 5 menit).
* Pengguna dapat menentukan jumlah siklus yang ingin dijalankan.
* Aplikasi akan memberikan notifikasi hitungan mundur di terminal.

### 3. Manajemen Waktu Kuliah
* **Tambah Jadwal:** Menyimpan jadwal mata kuliah, termasuk nama mata kuliah, hari, jam mulai, jam selesai, ruangan, dan nama dosen.
* **Lihat Jadwal Hari Ini:** Secara otomatis mendeteksi hari ini dan menampilkan jadwal yang relevan.
* **Lihat Jadwal Minggu Ini:** Menampilkan semua jadwal yang tersimpan, dikelompokkan berdasarkan hari (Senin-Minggu).
* **Hapus Jadwal:** Menghapus jadwal mata kuliah dari daftar.

### 4. Quiz
* **Buat Quiz:** Pengguna dapat membuat set kuis baru dengan judul, pertanyaan, 4 pilihan jawaban (A/B/C/D), dan kunci jawaban yang benar.
* **Mulai Quiz:** Pengguna memilih kuis yang ada, menjawab pertanyaan, dan mendapatkan skor akhir.
* **Lihat Daftar Quiz:** Menampilkan semua kuis yang telah dibuat.
* **Hapus Quiz:** Menghapus set kuis dari penyimpanan.

### 5. Flashcard
* **Buat Flashcard:** Memungkinkan pengguna membuat set kartu berdasarkan kategori/topik. Setiap kartu memiliki sisi "Depan" (pertanyaan/istilah) dan "Belakang" (jawaban/definisi).
* **Belajar dengan Flashcard:** Memulai sesi belajar di mana aplikasi akan menampilkan sisi "Depan", dan pengguna dapat menekan Enter untuk melihat sisi "Belakang".
* **Lihat Semua Flashcard:** Menampilkan daftar semua set flashcard yang tersedia.
* **Hapus Flashcard:** Menghapus set flashcard.

### 6. Formatter Sitasi
* Alat bantu untuk memformat daftar pustaka sederhana dalam gaya APA (American Psychological Association).
* Menyediakan templat untuk:
    * Buku
    * Artikel Jurnal
    * Website
    * Artikel Online
* Pengguna memasukkan metadata (penulis, tahun, judul, dll.) dan aplikasi akan menghasilkan string sitasi yang sudah diformat.

### 7. Word Counter
* **Hitung dari Input:** Pengguna dapat mengetik atau menempel teks langsung ke terminal.
* **Hitung dari File:** Pengguna dapat memberikan path ke file teks (`.txt`), dan aplikasi akan membacanya.
* **Tampilkan Statistik:** Memberikan laporan yang berisi:
    * Jumlah Kata
    * Jumlah Karakter (dengan dan tanpa spasi)
    * Jumlah Baris
    * Jumlah Kalimat (perkiraan)

---

## Teknologi yang Digunakan

Proyek ini murni dibuat dengan **Python 3** dan hanya menggunakan modul *built-in* (standar pustaka Python).

* `os`: Untuk membersihkan layar terminal (`clear_screen`).
* `time`: Digunakan dalam fitur Timer Pomodoro.
* `json`: Untuk menyimpan dan memuat semua data pengguna (kuis, jadwal, dll.) dalam file `student_data.json`.
* `datetime`: Untuk memberi cap waktu pada data dan fitur jadwal.

---

## Instalasi dan Menjalankan

Proyek ini tidak memerlukan dependensi eksternal.

1.  **Clone repositori ini:**
    ```bash
    git clone (https://github.com/akiljhe/STUDENT_TOOLKIT)
    ```

2.  **Masuk ke direktori proyek:**
    ```bash
    cd (nama-folder)
    ```

3.  **Jalankan aplikasi:**
    ```bash
    python main.py
    ```
    (atau `python3 main.py` tergantung konfigurasi sistem Anda)

---

## Cara Penggunaan

* Setelah aplikasi dijalankan, Anda akan disambut oleh menu utama.
* Navigasi dengan memasukkan angka yang sesuai dengan menu yang ingin Anda akses.
* Ketik `0` untuk kembali ke menu sebelumnya atau keluar dari aplikasi.
* Semua data yang Anda buat akan secara otomatis disimpan ke dalam file `student_data.json`.

---


## Alur Kerja Tim (Kontribusi)

Untuk menjaga proyek tetap teratur, tim kami menggunakan alur kerja Git sederhana.

**JANGAN PUSH LANGSUNG KE `main`!**

1.  **Selalu Update `main`:** Sebelum mulai bekerja, pastikan branch `main` lokal Anda adalah yang terbaru.
    ```bash
    git checkout main
    git pull origin main
    ```

2.  **Buat Branch Baru:** Buat *branch* baru untuk fitur atau perbaikan yang Anda kerjakan.
    ```bash
    git checkout -b fitur/nama-fitur-baru
    ```

3.  **Kerjakan Kode:** Lakukan perubahan/penambahan kode di *branch* Anda.

4.  **Commit dan Push:** Setelah selesai, *commit* perubahan Anda dan *push* *branch* Anda ke repositori GitHub.
    ```bash
    git add .
    git commit -m "Pesan commit yang jelas"
    git push origin fitur/nama-fitur-baru
    ```

5.  **Buat Pull Request (PR):**
    * Buka halaman repositori GitHub.
    * Buat **Pull Request** baru dari *branch* Anda ke *branch* `main`.
    * Jelaskan perubahan apa yang Anda buat dan minta *review* dari rekan tim.

6.  **Review dan Merge:**
    * Setelah di-review dan disetujui, PR tersebut akan di-*merge* ke `main`.

---

## Tim Pengembang

Berikut adalah pembagian tugas untuk setiap fitur:

* **To-Do List**: Dillah
* **Timer Pomodoro**: Amel
* **Manajemen Waktu Kuliah**: Sabri
* **Quiz**: Aqil
* **Flashcard**: Dafa
* **Formatter Sitasi**: Marvin
* **Word Counter**: Ayla
