
# Proyek Akhir Data Science
## Analisis dan Prediksi Pembatalan Reservasi Hotel: Pendekatan Data Science untuk Mengidentifikasi Faktor Risiko dan Mendukung Strategi Overbooking

### Kelompok Aliansi Cinta dan Jagung Bakar NO 23

| No. | Nama | NIM |
|---|---|---|
| 1 | Vania Christabella | 123240235 |
| 2 | Jelita Syahwa Nabila | 123240243 |
| 3 | Mutiara Rahmawati Zalsa | 123240257 |
| 4 | Aliffa Izza Ferryna | 123240258 |

---

## Deskripsi Proyek

Proyek ini membahas permasalahan pembatalan reservasi hotel yang dapat memengaruhi ketersediaan kamar dan potensi pendapatan hotel. Pembatalan reservasi, terutama yang terjadi mendekati tanggal kedatangan, berpotensi menyebabkan kamar tidak terjual kembali.

Penelitian ini menggunakan pendekatan Data Science untuk menganalisis pola pembatalan berdasarkan karakteristik reservasi dan membangun model klasifikasi yang dapat memprediksi kemungkinan pembatalan.

Dua algoritma klasifikasi yang digunakan adalah **Support Vector Machine (SVM) dengan kernel Linear** dan **Random Forest**. Hasil pemodelan dibandingkan menggunakan metrik evaluasi klasifikasi untuk menentukan model yang lebih sesuai dalam mengidentifikasi risiko pembatalan reservasi hotel.

## Tujuan Proyek

1. Mengidentifikasi faktor dan karakteristik reservasi yang memiliki keterkaitan dengan pembatalan reservasi hotel melalui Exploratory Data Analysis (EDA).
2. Membangun model klasifikasi untuk memprediksi kemungkinan pembatalan reservasi hotel.
3. Membandingkan performa algoritma Support Vector Machine (SVM) dan Random Forest.
4. Menginterpretasikan hasil prediksi sebagai bahan pertimbangan dalam pengelolaan risiko pembatalan reservasi dan strategi overbooking.

## Rumusan Masalah

1. Faktor dan karakteristik reservasi apa saja yang memiliki keterkaitan dengan pembatalan reservasi hotel berdasarkan hasil EDA?
2. Seberapa baik model Support Vector Machine (SVM) dan Random Forest dalam memprediksi pembatalan reservasi hotel berdasarkan informasi yang tersedia saat reservasi dibuat?

## Dataset

Dataset yang digunakan adalah **Hotel Booking Demand Dataset** yang diperoleh dari Kaggle.

- **Sumber:** Kaggle
- **Dataset:** Hotel Booking Demand
- **Link:** https://www.kaggle.com/datasets/jessemostipak/hotel-booking-demand
- **Jumlah data asli:** 119.390 baris
- **Jumlah kolom:** 32 kolom
- **Jumlah data sampel:** 50.000 baris
- **Teknik sampling:** Random Sampling
- **Random State:** 42
- **Variabel target:** `is_canceled`

Dataset berisi informasi historis reservasi pada City Hotel dan Resort Hotel. Variabel target `is_canceled` menunjukkan status pembatalan reservasi:

- `0` = Reservasi tidak dibatalkan.
- `1` = Reservasi dibatalkan.

## Metodologi

Proyek ini mengikuti tahapan Data Science sebagai berikut:

### 1. Business Understanding
- Identifikasi latar belakang permasalahan.
- Perumusan masalah.
- Penentuan tujuan proyek.
- Penentuan pendekatan penyelesaian.
- Pemilihan metode klasifikasi dan metrik evaluasi.

### 2. Data Gathering
- Mengidentifikasi sumber dan kredibilitas dataset.
- Memahami deskripsi dataset.
- Menyusun kamus data untuk 32 variabel.
- Memuat dataset menggunakan Pandas.
- Mengambil sampel sebanyak 50.000 baris menggunakan Random Sampling.

### 3. Data Understanding dan Exploratory Data Analysis (EDA)
- Pemeriksaan struktur dataset dan tipe data.
- Statistik deskriptif dan distribusi variabel.
- Pemeriksaan missing values dan data duplikat.
- Pemeriksaan distribusi variabel target.
- Pemeriksaan nilai tidak wajar dan kandidat outlier.
- Analisis distribusi status pembatalan dan jenis hotel.
- Analisis Lead Time terhadap pembatalan.
- Analisis karakteristik reservasi.
- Analisis pembatalan berdasarkan bulan kedatangan.
- Analisis pembatalan berdasarkan negara asal tamu.
- Analisis korelasi antarvariabel numerik.
- Analisis representativitas dan potensi bias sampel.

### 4. Data Cleaning dan Preprocessing
- Persiapan dataset.
- Penghapusan data duplikat.
- Penanganan missing values.
- Pemeriksaan dan penanganan nilai tidak wajar.
- Pemeriksaan kandidat outlier menggunakan metode IQR.
- Validasi hasil Data Cleaning.
- Feature Selection.
- Pencegahan Data Leakage.
- Penentuan fitur prediktor dan variabel target.
- Validasi akhir dataset.
- Penyimpanan dataset hasil preprocessing.

### 5. Modeling
Menggunakan dua algoritma klasifikasi:

**Support Vector Machine (SVM) Linear**
- Menggunakan kernel Linear.
- Menggunakan StandardScaler untuk fitur numerik.
- Menggunakan One-Hot Encoding untuk fitur kategorikal.
- Melakukan Hyperparameter Tuning menggunakan GridSearchCV.

**Random Forest**
- Menggunakan algoritma ensemble berbasis Decision Tree.
- Menggunakan 100 estimators pada konfigurasi baseline.
- Menggunakan preprocessing fitur kategorikal.
- Melakukan Hyperparameter Tuning menggunakan GridSearchCV.

Pembagian dataset dilakukan menggunakan:
- 80% data training.
- 20% data testing.
- Stratified Sampling untuk mempertahankan proporsi kelas.

### 6. Evaluasi Model
Evaluasi dilakukan menggunakan:
- Accuracy
- Precision
- Recall
- F1-Score
- Classification Report
- Confusion Matrix

### 7. Konklusi
- Menjawab rumusan masalah.
- Menginterpretasikan hasil evaluasi.
- Menentukan model terbaik.
- Menjelaskan keputusan pemilihan model.
- Mengidentifikasi keterbatasan penelitian.


## Teknologi dan Library

| Teknologi / Library | Kegunaan |
|---|---|
| Python | Bahasa pemrograman |
| Jupyter Notebook | Lingkungan pengembangan |
| Pandas | Pengolahan data |
| NumPy | Operasi numerik |
| Matplotlib | Visualisasi data |
| Seaborn | Visualisasi statistik |
| Scikit-learn | Preprocessing, modeling, dan evaluasi |

## Struktur Repository

```text
Proyek-Akhir-DataScience/
│
├── DATA/
│   └── hotel_bookings.csv
│
├── Proyek_Akhir_DataScience.ipynb
│
├── hotel_bookings_clean.csv
│
└── README.md
```

Keterangan:
- `DATA/hotel_bookings.csv` merupakan dataset asli.
- `Proyek_Akhir_DataScience.ipynb` merupakan notebook utama yang berisi seluruh tahapan proyek.
- `hotel_bookings_clean.csv` merupakan dataset hasil preprocessing.
- `README.md` merupakan dokumentasi proyek.

## Panduan Menjalankan Proyek

### 1. Clone Repository

```bash
git clone <URL-REPOSITORY-GITHUB>
```

### 2. Masuk ke Direktori Proyek

```bash
cd Proyek-Akhir-DataScience
```

### 3. Instalasi Library

Pastikan Python dan Jupyter Notebook telah terinstal, kemudian jalankan:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

### 4. Menyiapkan Dataset

Unduh dataset melalui Kaggle:

https://www.kaggle.com/datasets/jessemostipak/hotel-booking-demand

Letakkan file `hotel_bookings.csv` pada direktori:

```text
DATA/hotel_bookings.csv
```

### 5. Menjalankan Notebook

Jalankan perintah berikut:

```bash
jupyter notebook
```

Buka file `Proyek_Akhir_DataScience.ipynb`, kemudian jalankan seluruh cell secara berurutan dari awal hingga akhir.

Pastikan dataset telah ditempatkan pada direktori yang sesuai agar proses pembacaan data dapat berjalan dengan baik.

## Anggota Kelompok

**Kelompok: Aliansi Cinta dan Jagung Bakar**

| No. | Nama | NIM |
|---|---|---|
| 1 | Vania Christabella | 123240235 |
| 2 | Jelita Syahwa Nabila | 123240243 |
| 3 | Mutiara Rahmawati Zalsa | 123240257 |
| 4 | Aliffa Izza Ferryna | 123240258 |


## Rincian Kontribusi Anggota

### 1. Vania Christabella
- Mengidentifikasi permasalahan dan tujuan proyek.
- Memahami karakteristik dan atribut dataset.
- Berkontribusi dalam proses data preparation dan cleaning.
- Melakukan analisis eksplorasi dan visualisasi data.
- Membantu proses feature engineering.

### 2. Jelita Syahwa Nabila
- Berkontribusi dalam pemeriksaan dan pembersihan data.
- Melakukan analisis eksplorasi data.
- Membantu pembangunan dan pengujian model.
- Berkontribusi dalam evaluasi hasil pemodelan.
- Mengelola dokumentasi proyek, penyusunan README, dan repository GitHub.

### 3. Mutiara Rahmawati Zalsa
- Membantu persiapan dan pembersihan dataset.
- Melakukan analisis distribusi dan hubungan antarvariabel.
- Membuat visualisasi data.
- Melakukan feature engineering.
- Berkontribusi dalam pembangunan dan pengujian model.

### 4. Aliffa Izza Ferryna
- Membantu persiapan dan pengolahan dataset.
- Berkontribusi dalam feature engineering.
- Membangun dan mengembangkan model Machine Learning.
- Melakukan evaluasi dan perbandingan performa model.
- Membantu interpretasi hasil pemodelan.

## Tanggung Jawab Bersama

1. Seluruh anggota terlibat dalam setiap tahapan pengembangan proyek.
2. Seluruh anggota berkontribusi dalam proses pengolahan dan pemeriksaan data.
3. Setiap anggota memahami proses dan hasil dari seluruh tahapan proyek.
4. Seluruh anggota ikut melakukan pemeriksaan dan revisi notebook serta laporan.
5. Seluruh anggota berkontribusi dalam pengembangan proyek sesuai tanggung jawab masing-masing.


## Penutup

Proyek ini menerapkan tahapan Data Science untuk menganalisis dan memprediksi pembatalan reservasi hotel. Berdasarkan hasil eksperimen, Support Vector Machine (SVM) dengan kernel Linear menunjukkan performa yang lebih baik dibandingkan Random Forest dalam mendeteksi reservasi yang dibatalkan.

Hasil penelitian diharapkan dapat menjadi bahan pertimbangan bagi pihak hotel dalam mengidentifikasi risiko pembatalan reservasi dan mendukung pengambilan keputusan terkait pengelolaan kamar serta strategi overbooking.

---

**Program Studi Informatika**  
**Fakultas Teknik dan Sains**  
**Universitas Pembangunan Nasional "Veteran" Yogyakarta**  
**Praktikum Data Science 2026/2027**
