# 💼 Case Study Portfolio: ETK Global Web Platform
Pelatihan Bahasa Inggris Korporat & Akselerasi IELTS Band 9 - Yogyakarta

## 📌 1. Deskripsi Proyek
Membangun ulang (*rebuilding*) dan mengintegrasikan arsitektur mading digital serta portal informasi untuk ETK Global Yogyakarta ke dalam satu file HTML tunggal (*single-file deployment*) guna memastikan sinkronisasi aset 100%.

## 🛠️ 2. Tantangan Teknis & Solusi (Case Study)

### Kasus 1: Sinkronisasi Aset Gambar GitHub (CORS & Broken Links)
* **Masalah:** Menggunakan URL standar GitHub (`github.com/.../blob/...`) pada tag `<img>` menyebabkan gambar tidak muncul karena proteksi intermitten halaman HTML biasa.
* **Solusi:** Mengonversi seluruh tautan mentah menjadi jalur distribusi CDN resmi GitHub (`https://raw.githubusercontent.com/`).

### Kasus 2: Kompatibilitas Tata Letak Navigasi *Teal Integrated Bar*
* **Masalah:** Memasang gambar latar belakang `etk_future.png` tepat di koordinat 0 tepi kiri, 0 atas, dan 0 bawah bar navigasi tanpa merusak elemen menu teks.
* **Solusi:** Menerapkan sistem layer independen dengan CSS modern:
  ```css
  .header-bg-backdrop-layer {
      position: absolute;
      left: 0; top: 0; bottom: 0;
      width: 450px;
      z-index: 1;
  }
