# 🧠 Machine Learning Mastery: Dari Fondasi Teori ke Penerapan Praktis

[![Python Version](https://img.shields.io/badge/python-3.12%2B-blue.svg?logo=python&logoColor=white)](https://www.python.org/)
[![Scikit-Learn](https://img.shields.io/badge/scikit--learn-1.5%2B-F7931E.svg?logo=scikit-learn&logoColor=white)](https://scikit-learn.org/)
[![Pandas](https://img.shields.io/badge/pandas-2.2%2B-150458.svg?logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![NumPy](https://img.shields.io/badge/numpy-2.0%2B-013243.svg?logo=numpy&logoColor=white)](https://numpy.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg?logo=jupyter&logoColor=white)](https://jupyter.org/)
[![Dicoding](https://img.shields.io/badge/Dicoding-BMLP%20Completed-2A73CC.svg)](https://www.dicoding.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Repositori ini mendokumentasikan perjalanan pembelajaran dan implementasi praktis konsep-konsep **Machine Learning (ML)** berdasarkan kurikulum **Dicoding Academy (Belajar Machine Learning Untuk Pemula)**. 

Di dalam repositori ini tercakup kurikulum komprehensif mulai dari *end-to-end ML workflow*, pemodelan *Supervised Learning* (Klasifikasi & Regresi), *Unsupervised Learning* (Clustering), teknik rekayasa fitur (*Feature Engineering*), penanganan *Bias-Variance Tradeoff* (*Overfitting & Underfitting*), optimasi parameter (*Hyperparameter Tuning*), hingga proyek akhir (*Capstone Submission*) berupa sistem deteksi anomali & penipuan transaksi finansial berbasis *Clustering-to-Classification*.

---

## 📑 Daftar Isi

- [🎯 Gambaran Umum](#-gambaran-umum)
- [📂 Struktur Repositori](#-struktur-repositori)
- [📚 Silabus & Rincian Modul Pembelajaran](#-silabus--rincian-modul-pembelajaran)
  - [Modul 01: Machine Learning Workflow](#modul-01-machine-learning-workflow)
  - [Modul 02: Supervised Learning - Klasifikasi](#modul-02-supervised-learning---klasifikasi)
  - [Modul 03: Supervised Learning - Regresi](#modul-03-supervised-learning---regresi)
  - [Modul 04: Unsupervised Learning - Clustering](#modul-04-unsupervised-learning---clustering)
  - [Modul 05: Teknik Feature Engineering](#modul-05-teknik-feature-engineering)
  - [Modul 06: Overfitting dan Underfitting](#modul-06-overfitting-dan-underfitting)
  - [Modul 07: Hyperparameter Tuning](#modul-07-hyperparameter-tuning)
  - [Submission Akhir: Proyek Terintegrasi BMLP](#submission-akhir-proyek-terintegrasi-bmlp)
- [💻 Tech Stack & Ekosistem](#-tech-stack--ekosistem)
- [🚀 Panduan Memulai & Instalasi](#-panduan-memulai--instalasi)
- [🛠️ Menjalankan Notebook](#️-menjalankan-notebook)
- [💡 Temuan & Wawasan Kunci](#-temuan--wawasan-kunci)
- [👤 Penulis & Lisensi](#-penulis--lisensi)

---

## 🎯 Gambaran Umum

Tujuan utama dari repositori ini adalah:
1. **Memahami Alur Kerja Machine Learning:** Menguasai siklus hidup data sains dari *Data Ingestion*, *Exploratory Data Analysis (EDA)*, *Data Cleaning*, *Feature Engineering*, *Model Training*, *Evaluation*, hingga *Model Persistence*.
2. **Eksplorasi Algoritma Standar Industri:** Mengimplementasikan dan membandingkan performa beragam algoritma ML klasik (*KNN*, *Decision Tree*, *Random Forest*, *SVM*, *Naive Bayes*, *Linear Regression*, *Gradient Boosting*, *K-Means*, *DBSCAN*).
3. **Praktek Terbaik Rekayasa Data:** Menguasai teknik transformasi fitur seperti penanganan *missing values*, *categorical encoding*, standardisasi/normalisasi, penanganan *class imbalance* dengan **SMOTE**, serta penyusunan *pipeline* otomatis.
4. **Validasi Model yang Kuat:** Mendiagnosis kurva belajar (*learning curves*), menggunakan *K-Fold Cross-Validation*, dan melakukan penalaan *hyperparameter* secara sistematis (*Grid Search*, *Random Search*, dan *Bayesian Optimization*).
5. **Aplikasi Nyata:** Menyelesaikan kasus riil deteksi anomali finansial (*fraud detection*) yang menggabungkan *clustering* untuk pelabelan unsupervised dilanjutkan klasifikasi prediktif.

---

## 📂 Struktur Repositori

```text
machine-learning/
│
├── 01 Machine Learning Workflow/           # End-to-end pipeline regresi harga rumah
│   ├── house-prices-advanced-regression/   # Dataset Kaggle (train, test, deskripsi)
│   ├── main.ipynb                          # Notebook alur lengkap ML
│   ├── gbr_model.joblib                    # Model tersimpan format joblib
│   └── gbr_model.pkl                       # Model tersimpan format pickle
│
├── 02 Supervised Learning Klasifikasi/      # Klasifikasi Customer Churn Perbankan
│   └── main.ipynb                          # Eksplorasi KNN, Decision Tree, RF, SVM, Naive Bayes
│
├── 03 Supervised Learning Regresi/          # Prediksi Probabilitas Risiko Banjir
│   ├── data/                               # Dataset train, test, sample submission
│   ├── main.ipynb                          # Model Linear Regression & Gradient Boosting
│   └── submission.csv                      # Output prediksi
│
├── 04 Unsupervised Learning Clustering/    # Segmentasi Pelanggan (Customer Segmentation)
│   └── notebook.ipynb                      # K-Means, DBSCAN, Elbow Visualizer, Silhouette
│
├── 05 Teknik Feature Engineering/           # Rekayasa & Transformasi Fitur Tingkat Lanjut
│   └── notebook.ipynb                      # SelectKBest, SMOTE, Scaler, ColumnTransformer & Pipeline
│
├── 06 Overfitting dan Underfitting/        # Diagnosis Bias-Variance Tradeoff
│   ├── overfitting.ipynb                   # Simulasi overfit, Cross-Validation & Learning Curves
│   └── underfitting.ipynb                  # Simulasi underfit & optimasi kapasitas model
│
├── 07 Hyperparameter Tuning/                # Optimasi Parameter Model ML
│   ├── klasifikasi.ipynb                   # Grid, Random & Bayes Search pada German Credit data
│   └── regresi.ipynb                       # Hyperparameter tuning pada California Housing data
│
├── Submission/                              # Proyek Akhir Dicoding BMLP
│   ├── [Clustering]_Submission_Akhir_BMLP_Nugie_Saputra.ipynb
│   ├── [Klasifikasi]_Submission_Akhir_BMLP_Nugie_Saputra.ipynb
│   ├── data_clustering.csv                 # Data hasil clustering
│   ├── data_clustering_inverse.csv         # Data hasil reverse-transform
│   └── *.h5 / model artifacts             # Model clustering, PCA, & klasifikasi tersimpan
│
├── requirements.md                         # Panduan detail spesifikasi & instalasi dependensi
├── requirements.txt                        # File dependensi standar pip
├── pyproject.toml                          # Konfigurasi dependensi proyek modern
├── uv.lock                                 # Lockfile dependensi UV
└── README.md                               # Dokumentasi utama repositori
```

---

## 📚 Silabus & Rincian Modul Pembelajaran

### [Modul 01: Machine Learning Workflow](01%20Machine%20Learning%20Workflow/)
- **Fokus Studi:** Memahami siklus menyeluruh proyek ML dari data mentah hingga artefak model siap pakai.
- **Kasus / Dataset:** *House Prices: Advanced Regression Techniques* (Kaggle).
- **Aktivitas Utama:**
  - Eksplorasi statistik dan distribusi data fitur perumahan.
  - Penanganan nilai kosong (*missing values*) dan *outliers*.
  - Transformasi fitur kategorikal (*One-Hot Encoding*) dan penskalaan numerik.
  - Pelatihan model regresi berbasis ensemble: `GradientBoostingRegressor`.
  - Serialisasi model menggunakan `joblib` dan `pickle` untuk *deployment*.

---

### [Modul 02: Supervised Learning - Klasifikasi](02%20Supervised%20Learning%20Klasifikasi/)
- **Fokus Studi:** Penerapan berbagai algoritma klasifikasi biner dan multi-kelas serta perbandingan kinerjanya.
- **Kasus / Dataset:** *Bank Customer Churn Modeling* (Prediksi nasabah yang berpotensi berhenti berlangganan).
- **Algoritma yang Diterapkan:**
  - $K$-Nearest Neighbors (KNN)
  - Decision Tree Classifier
  - Random Forest Classifier
  - Support Vector Machine (SVC / SVM)
  - Gaussian Naive Bayes (GaussianNB)
- **Metrik Evaluasi:** *Confusion Matrix*, *Accuracy*, *Precision*, *Recall*, dan *F1-Score*.

---

### [Modul 03: Supervised Learning - Regresi](03%20Supervised%20Learning%20Regresi/)
- **Fokus Studi:** Prediksi variabel kontinu berdasarkan banyak prediktor lingkungan dan geografis.
- **Kasus / Dataset:** *Flood Prediction Dataset* (Prediksi probabilitas banjir berdasarkan intensitas monsun, drainase, deforestasi, dll.).
- **Algoritma yang Diterapkan:**
  - Regresi Linier (*Linear Regression*)
  - *Gradient Boosting Regressor*
- **Metrik Evaluasi:** *Mean Squared Error* (MSE), *Root Mean Squared Error* (RMSE), *Mean Absolute Error* (MAE), dan koefisien determinasi ($R^2$ Score).

---

### [Modul 04: Unsupervised Learning - Clustering](04%20Unsupervised%20Learning%20Clustering/)
- **Fokus Studi:** Pengelompokan data tanpa label (*unlabeled data*) untuk menemukan pola tersembunyi.
- **Kasus / Dataset:** Segmentasi profil pelanggan (*Customer Segmentation*).
- **Algoritma yang Diterapkan:**
  - **K-Means Clustering:** Pengelompokan berbasis centroid.
  - **DBSCAN:** Pengelompokan berbasis kepadatan spasial (*density-based*) yang mampu menangani *outliers* / noise.
- **Evaluasi Klaster:**
  - Penentuan nilai $k$ optimal dengan *Elbow Method* menggunakan `yellowbrick.cluster.KElbowVisualizer`.
  - Pengukuran kekompakan dan separasi klaster dengan *Silhouette Score*.

---

### [Modul 05: Teknik Feature Engineering](05%20Teknik%20Feature%20Engineering/)
- **Fokus Studi:** Memaksimalkan kualitas representasi data untuk meningkatkan performa model pembelajaran mesin.
- **Metode & Teknik:**
  - **Feature Selection:** Seleksi fitur terbaik menggunakan `SelectKBest` dengan uji ANOVA F-test (`f_classif`).
  - **Feature Scaling:** `StandardScaler` dan `MinMaxScaler`.
  - **Encoding:** `OneHotEncoder` dan `LabelEncoder` untuk variabel kategorik.
  - **Diskretisasi / Binning:** `KBinsDiscretizer` untuk mengubah fitur kontinu menjadi interval diskret.
  - **Handling Imbalanced Data:** *Synthetic Minority Over-sampling Technique* (**SMOTE**) via `imbalanced-learn`.
  - **Pipelines & ColumnTransformer:** Membangun alur pra-pemrosesan data yang otomatis, bersih, dan bebas dari *data leakage*.

---

### [Modul 06: Overfitting dan Underfitting](06%20Overfitting%20dan%20Underfitting/)
- **Fokus Studi:** Mendiagnosis dan mengatasi masalah *bias-variance tradeoff*.
- **Kasus / Dataset:** *California Housing Dataset*.
- **Metode Analisis:**
  - Demonstrasi model *overfitting* (kedalaman pohon tak terbatas) vs model *underfitting* (kapasitas terlalu sederhana).
  - Pemanfaatan **Learning Curves** (`sklearn.model_selection.learning_curve`) untuk memantau performa data latih vs data validasi seiring pertambahan sampel.
  - Evaluasi ketahanan model dengan **K-Fold Cross-Validation** (`cross_val_score`).
  - Strategi penanganan: Pembatasan kompleksitas model (`max_depth`, `min_samples_split`) dan regularisasi.

---

### [Modul 07: Hyperparameter Tuning](07%20Hyperparameter%20Tuning/)
- **Fokus Studi:** Penalaan sistematis parameter model untuk mencapai akurasi atau batas kesalahan optimal.
- **Kasus / Dataset:** *German Credit Data* (Klasifikasi Risiko Kredit) & *California Housing* (Regresi).
- **Strategi Optimasi:**
  1. **Grid Search (`GridSearchCV`):** Pencarian menyeluruh pada kombinasi grid parameter.
  2. **Randomized Search (`RandomizedSearchCV`):** Sampling acak berdistribusi untuk efisiensi komputasi tinggi.
  3. **Bayesian Optimization (`scikit-optimize` / `BayesSearchCV`):** Pencarian probabilistik terarah berbasis *Gaussian Process*.

---

### [Submission Akhir: Proyek Terintegrasi BMLP](Submission/)
**Studi Kasus:** *Financial Fraud Detection & Transaction Anomaly Clustering*  
Proyek ini mengintegrasikan pembelajaran *unsupervised* dan *supervised* secara berkesinambungan:

1. **Tahap 1: Unsupervised Clustering (`[Clustering]_Submission_Akhir_BMLP_Nugie_Saputra.ipynb`)**
   - Menganalisis 2.512 data riwayat transaksi finansial nasabah (demografi, saldo, durasi, jumlah percobaan login).
   - Pembersihan data, deteksi anomali, standardisasi fitur, dan reduksi dimensi dengan **PCA**.
   - Pengelompokan nasabah/transaksi ke dalam klaster perilaku menggunakan **K-Means**.
   - Penyimpanan artefak model clustering dan ekspor data berlabel (`data_clustering.csv`).

2. **Tahap 2: Supervised Classification (`[Klasifikasi]_Submission_Akhir_BMLP_Nugie_Saputra.ipynb`)**
   - Memanfaatkan label hasil clustering sebagai target kelas untuk mendeteksi potensi penipuan atau anomali transaksi baru.
   - Pembangunan model klasifikasi menggunakan **Decision Tree** dan **Random Forest**.
   - Optimasi hyperparameter dengan *Grid Search* dan *Random Search*.
   - Evaluasi menyeluruh menggunakan matriks klasifikasi dan *Classification Report*.
   - Ekspor model akhir siap inferensi (`.h5`).

---

## 💻 Tech Stack & Ekosistem

| Bidang | Teknologi / Pustaka |
| :--- | :--- |
| **Bahasa Utama** | Python 3.12+ |
| **Machine Learning** | `scikit-learn`, `imbalanced-learn`, `scikit-optimize` |
| **Manipulasi Data** | `pandas`, `numpy` |
| **Visualisasi Data** | `matplotlib`, `seaborn`, `yellowbrick` |
| **Model Persistence** | `joblib`, `pickle` |
| **Interaktif & Notebook** | `jupyter`, `ipykernel`, `ipywidgets` |
| **Package Management** | `uv` (modern high-speed package manager) / `pip` |

---

## 🚀 Panduan Memulai & Instalasi

> 💡 **Informasi Lengkap:** Untuk panduan dependensi, spesifikasi perangkat keras, dan troubleshooting mendalam, silakan baca [requirements.md](requirements.md).

### 1. Klon Repositori
```bash
git clone https://github.com/nugi-ML/machine-learning.git
cd machine-learning
```

### 2. Penyiapan Environment

#### Opsi A: Menggunakan `uv` (Direkomendasikan)
Jika Anda menggunakan [uv](https://github.com/astral-sh/uv):
```bash
# Otomatis membuat virtual environment dan memasang dependensi
uv sync

# Aktifkan virtual environment
# Windows (PowerShell):
.venv\Scripts\Activate.ps1
# Linux / macOS:
source .venv/bin/activate
```

#### Opsi B: Menggunakan Standard `venv` & `pip`
```bash
# Buat virtual environment
python -m venv .venv

# Aktifkan virtual environment (Windows PowerShell)
.venv\Scripts\Activate.ps1
# Atau Linux / macOS:
source .venv/bin/activate

# Upgrade pip dan pasang pustaka
python -m pip install --upgrade pip
pip install -r requirements.txt
```

### 3. Verifikasi Pemasangan
```bash
python -c "import sklearn, pandas, numpy, seaborn, matplotlib, imblearn, yellowbrick; print('Environment siap digunakan!')"
```

---

## 🛠️ Menjalankan Notebook

1. Buka repositori pada editor favorit Anda (disarankan **Visual Studio Code**):
   ```bash
   code .
   ```
2. Pasang ekstensi **Python** dan **Jupyter** di VS Code.
3. Buka salah satu file notebook `.ipynb`.
4. Pada pojok kanan atas editor, klik **Select Kernel** $\rightarrow$ pilih environment `.venv` yang telah dibuat.
5. Jalankan sel kode satu per satu atau klik **Run All**.

---

## 💡 Temuan & Wawasan Kunci

1. **Pentingnya Feature Engineering:** Penanganan *missing values* yang tepat dan seleksi fitur yang relevan seringkali memberikan lonjakan akurasi yang lebih signifikan dibandingkan sekadar mengganti algoritma model.
2. **Penanganan Imbalanced Dataset:** Pada kasus klasifikasi langka (seperti *churn* atau *fraud*), penggunaan metrik **F1-Score** dan teknik sampling seperti **SMOTE** jauh lebih representatif dibandingkan hanya mengandalkan *Accuracy*.
3. **Pencegahan Overfitting:** Membatasi kompleksitas model (seperti membatasi `max_depth` pada pohon keputusan) serta validasi silang (*Cross-Validation*) sangat krusial agar model memiliki generalisasi yang baik terhadap data baru.
4. **Efisiensi Hyperparameter Tuning:** *Randomized Search* dan *Bayesian Optimization* mampu menemukan titik konfigurasi parameter optimal dengan waktu komputasi yang jauh lebih hemat dibandingkan *Grid Search* pada ruang pencarian yang besar.

---

## 👤 Penulis & Lisensi

- **Penulis:** Nugie Saputra ([@nugi-ML](https://github.com/nugi-ML))
- **Program:** Dicoding Academy - Belajar Machine Learning Untuk Pemula
- **Lisensi:** Repositori ini dilisensikan di bawah [MIT License](LICENSE). Bebas digunakan untuk referensi pembelajaran dan studi mandiri.

---
<p align="center">
  Dibuat dengan dedikasi untuk pembelajaran dan eksplorasi dunia kecerdasan buatan. ⭐ Jangan lupa beri bintang jika repositori ini bermanfaat!
</p>
