# Proyek Machine Learning: Optimisasi Limit Kartu Kredit Berdasarkan Perilaku Transaksi

## Deskripsi

Proyek ini merupakan implementasi machine learning untuk mengoptimalkan penetapan limit kartu kredit dengan menganalisis perilaku transaksi nasabah. Dengan memanfaatkan data transaksi bank, proyek ini bertujuan untuk mengelompokkan nasabah berdasarkan pola penggunaan kartu kredit dan perilaku keuangan mereka. Hasil segmentasi ini kemudian digunakan untuk menetapkan limit kartu kredit yang optimal, sehingga dapat meningkatkan kepuasan nasabah dan mengurangi risiko kredit macet.

## Tujuan Bisnis

- **Meningkatkan Profitabilitas:** Menyesuaikan limit kartu kredit sesuai dengan profil penggunaan dan risiko masing-masing nasabah agar dapat meningkatkan pendapatan bunga dan mengurangi kredit bermasalah.
- **Mengurangi Risiko Kredit Macet:** Dengan menentukan limit yang optimal, bank dapat meminimalkan risiko gagal bayar dan meningkatkan manajemen risiko.
- **Meningkatkan Kepuasan Nasabah:** Penetapan limit yang tepat akan memberikan fleksibilitas bagi nasabah yang membutuhkan, sehingga meningkatkan loyalitas dan kepuasan.
- **Personalisasi Penawaran Produk:** Hasil segmentasi dapat digunakan untuk merancang penawaran produk perbankan yang lebih sesuai dengan kebutuhan dan perilaku masing-masing segmen.

## Pendekatan

Proyek ini dibagi ke dalam dua tahap utama:

1. **Clustering (Unsupervised Learning):**

   - **Tujuan:** Mengelompokkan nasabah berdasarkan perilaku transaksi menggunakan algoritma clustering (misalnya, K-Means).
   - **Fitur Utama:** Fitur yang digunakan dapat mencakup:
     - Jumlah dan frekuensi transaksi
     - Nilai transaksi rata-rata dan total
     - Durasi transaksi dan interval antar transaksi
     - Informasi demografis seperti usia nasabah (jika tersedia)
     - Data tambahan (misalnya, informasi lokasi transaksi, perangkat yang digunakan, dll.)
   - **Output:** Setiap nasabah akan mendapatkan label cluster yang menunjukkan kelompok perilaku transaksi serupa.

2. **Optimisasi Limit Kartu Kredit:**
   - **Tujuan:** Menetapkan limit kartu kredit yang optimal berdasarkan karakteristik dan risiko masing-masing cluster.
   - **Pendekatan:**
     - Melakukan analisis terhadap karakteristik masing-masing cluster untuk menentukan profil risiko.
     - Menetapkan aturan atau menggunakan model supervised learning (misalnya, regresi atau decision tree) yang mengkalkulasi limit optimal berdasarkan pola historis.
   - **Output:** Rekomendasi limit kartu kredit yang dapat diterapkan pada masing-masing segmen nasabah.

Proyek ini terbagi dalam dua notebook Jupyter:

- **Clustering Notebook:** Melakukan preprocessing data, segmentasi nasabah melalui clustering, dan analisis karakteristik tiap cluster.
- **Optimization Notebook:** Menggunakan hasil segmentasi untuk membangun model atau aturan optimisasi limit, serta melakukan evaluasi performa sistem rekomendasi limit.

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

1. **Clustering Notebook**:

   - Jalankan perintah:
     ```bash
     jupyter notebook notebooks/[Clustering]_Submission_Akhir_BMLP_Alif_Nurhidayat_(Updated).ipynb
     ```
   - Buka file `[Clustering]_Submission_Akhir_BMLP_Alif_Nurhidayat_(Updated).ipynb` di antarmuka Jupyter Notebook untuk melakukan segmentasi nasabah.

2. **Optimization Notebook**:
   - Jalankan perintah:
     ```bash
     jupyter notebook notebooks/[Optimization]_Submission_Akhir_BMLP_Alif_Nurhidayat.ipynb
     ```
   - Buka file `[Optimization]_Submission_Akhir_BMLP_Alif_Nurhidayat.ipynb` di antarmuka Jupyter Notebook untuk melakukan optimisasi limit kartu kredit berdasarkan hasil clustering.

**Urutan Eksekusi:**

- Jalankan **Clustering Notebook** terlebih dahulu untuk menghasilkan label segmentasi nasabah.
- Lanjutkan dengan **Optimization Notebook** untuk membangun model atau aturan optimisasi limit berdasarkan segmentasi tersebut.

## Struktur Folder Proyek

```
├── data/
│   ├── bank_transaction_dataset.csv   # Dataset mentah
│   └── bank_transaction_segmented.csv # Dataset dengan label cluster
├── notebooks/
│   ├── [Clustering]_Submission_Akhir_BMLP_Alif_Nurhidayat_(Updated).ipynb   # Notebook untuk clustering/segmentasi
│   └── [Optimization]_Submission_Akhir_BMLP_Alif_Nurhidayat.ipynb           # Notebook untuk optimisasi limit
├── LICENSE                            # Lisensi
├── README.md                          # Dokumentasi proyek
└── requirements.txt                   # Daftar dependensi
```

## Kontak

Dibuat oleh **Alif Nurhidayat (KillerKing93)**
Email: [alifnurhidayatwork@gmail.com](mailto:alifnurhidayatwork@gmail.com)

## Lisensi

Proyek ini dilisensikan di bawah [Modified Apache License 2.0 – Non Commercial](LICENSE). Lisensi ini membatasi penggunaan komersial kecuali dengan izin tertulis dan pembayaran loyalty fee sesuai ketentuan. Lihat file LICENSE untuk detail lengkap.
