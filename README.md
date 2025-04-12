# Proyek Machine Learning: Optimisasi Limit Kartu Kredit Berdasarkan Perilaku Transaksi

## Deskripsi

Proyek ini mengimplementasikan machine learning untuk mengoptimalkan penetapan limit kartu kredit dengan menganalisis perilaku transaksi nasabah. Dengan memanfaatkan data transaksi bank, proyek ini bertujuan untuk mengelompokkan nasabah berdasarkan pola penggunaan dan perilaku keuangan mereka. Hasil segmentasi digunakan untuk menetapkan limit kartu kredit yang optimal. Pendekatan ini tidak hanya membantu meningkatkan profitabilitas bank melalui peningkatan pendapatan bunga, tetapi juga mengurangi risiko kredit macet dan meningkatkan kepuasan nasabah dengan penawaran yang lebih personal.

## Tujuan Bisnis

- **Meningkatkan Profitabilitas:**  
  Dengan menyesuaikan limit kartu kredit sesuai dengan profil penggunaan dan risiko masing-masing nasabah, bank dapat meningkatkan pendapatan bunga dan mengurangi kredit bermasalah.
- **Mengurangi Risiko Kredit Macet:**  
  Penetapan limit yang optimal membantu bank dalam meminimalkan risiko gagal bayar serta memperkuat manajemen risiko kredit.
- **Meningkatkan Kepuasan Nasabah:**  
  Limit yang sesuai kebutuhan memberikan fleksibilitas lebih kepada nasabah, yang pada gilirannya meningkatkan loyalitas dan kepuasan.
- **Personalisasi Penawaran Produk:**  
  Hasil segmentasi memungkinkan bank untuk merancang produk dan penawaran perbankan yang lebih sesuai dengan karakteristik dan perilaku tiap segmen nasabah.

## Pendekatan Proyek

Proyek ini dibagi ke dalam dua tahap utama, yang masing-masing mendukung tujuan bisnis secara langsung:

1. **Clustering (Unsupervised Learning):**

   - **Tujuan:**  
     Mengelompokkan nasabah berdasarkan perilaku transaksi untuk mendapatkan insight terkait profil risiko dan potensi profitabilitas.
   - **Fitur Utama:**
     - Jumlah dan frekuensi transaksi
     - Nilai transaksi rata-rata dan total
     - Durasi transaksi dan interval antar transaksi
     - Informasi demografis (misalnya, usia nasabah)
     - Data tambahan seperti lokasi transaksi dan perangkat yang digunakan
   - **Output:**  
     Setiap nasabah mendapatkan label cluster yang menggambarkan kelompok perilaku transaksi serupa, yang kemudian digunakan untuk analisis lebih lanjut.

2. **Optimisasi Limit Kartu Kredit (Klasifikasi dan Penerapan Aturan):**

   - **Tujuan:**  
     Menetapkan limit kartu kredit yang optimal untuk setiap segmen nasabah berdasarkan karakteristik dan risiko yang telah teridentifikasi.
   - **Pendekatan:**
     - **Analisis Segmentasi:**  
       Melakukan evaluasi mendalam pada tiap cluster untuk memahami profil risiko dan perilaku transaksi.
     - **Penerapan Model/Aturan:**  
       Mengembangkan model supervised learning (misalnya, regresi atau decision tree) atau menetapkan aturan heuristik untuk menghitung limit optimal berdasarkan pola historis dan karakteristik masing-masing cluster.
   - **Output:**  
     Rekomendasi limit kartu kredit yang diharapkan dapat meningkatkan profitabilitas, mengurangi risiko kredit macet, dan memberikan pengalaman yang lebih personal bagi nasabah.

Proyek ini terdiri dari dua notebook Jupyter yang saling mendukung:

- **Clustering Notebook:**  
  Menangani preprocessing data, segmentasi nasabah melalui clustering, dan analisis karakteristik tiap cluster guna mengidentifikasi profil risiko.
- **Klasifikasi Notebook:**  
  Mengintegrasikan hasil clustering untuk membangun model atau menetapkan aturan optimisasi limit, kemudian mengevaluasi performa sistem rekomendasi sesuai dengan tujuan bisnis.

## Instalasi

Pastikan Anda memiliki Python (minimal versi 3.7) terpasang di sistem Anda.

### 1. Membuat Virtual Environment

Di direktori root proyek, buat virtual environment dengan perintah:

```bash
python3 -m venv myvenv
```

atau

```bash
python -m venv myvenv
```

### 2. Mengaktifkan Virtual Environment

Aktifkan virtual environment:

- **Linux/MacOS:**
  ```bash
  source myvenv/bin/activate
  ```
- **Windows:**
  ```bash
  myvenv\Scripts\activate
  ```

> **Catatan:** Pastikan virtual environment aktif di direktori root proyek agar path dataset dapat diakses dengan benar.

### 3. Instalasi Dependencies

Setelah virtual environment aktif, instal dependensi dengan:

```bash
pip install -r requirements.txt
```

File `requirements.txt` harus mencakup:

- numpy
- pandas
- matplotlib
- seaborn
- scikit-learn
- jupyter

## Cara Menjalankan Proyek

### Menjalankan Jupyter Notebook

1. **Clustering Notebook:**

   - Jalankan perintah:
     ```bash
     jupyter notebook [Clustering]_Submission_Akhir_BMLP_Alif_Nurhidayat_(Updated).ipynb
     ```
   - Buka file `[Clustering]_Submission_Akhir_BMLP_Alif_Nurhidayat_(Updated).ipynb` untuk melakukan segmentasi nasabah dan analisis profil risiko.

2. **Klasifikasi Notebook:**
   - Jalankan perintah:
     ```bash
     jupyter notebook [Klasifikasi]_Submission_Akhir_BMLP_Alif_Nurhidayat.ipynb
     ```
   - Buka file `[Klasifikasi]_Submission_Akhir_BMLP_Alif_Nurhidayat.ipynb` untuk mengembangkan model atau aturan optimisasi limit berdasarkan hasil segmentasi.

**Urutan Eksekusi:**

- Jalankan **Clustering Notebook** terlebih dahulu untuk menghasilkan label segmentasi nasabah.
- Lanjutkan dengan **Klasifikasi Notebook** untuk membangun dan mengevaluasi sistem rekomendasi limit yang mendukung tujuan bisnis.

## Struktur Folder Proyek

```
├── bank_transaction_dataset.csv   # Dataset mentah
├── bank_transaction_segmented.csv # Dataset dengan label cluster
├── [Clustering]_Submission_Akhir_BMLP_Alif_Nurhidayat_(Updated).ipynb   # Notebook untuk clustering/segmentasi
├── [Klasifikasi]_Submission_Akhir_BMLP_Alif_Nurhidayat.ipynb           # Notebook untuk optimisasi limit
├── LICENSE                            # Lisensi
├── README.md                          # Dokumentasi proyek
└── requirements.txt                   # Daftar dependensi
```

## Kontak

Dibuat oleh **Alif Nurhidayat (KillerKing93)**  
Email: [alifnurhidayatwork@gmail.com](mailto:alifnurhidayatwork@gmail.com)

## Lisensi

Proyek ini dilisensikan di bawah [Modified Apache License 2.0 – Non Commercial](LICENSE). Lisensi ini membatasi penggunaan komersial kecuali dengan izin tertulis dan pembayaran loyalty fee sesuai ketentuan. Lihat file LICENSE untuk detail lengkap.
