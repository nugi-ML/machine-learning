# 📋 Requirements & Environment Setup Guide

Dokumen ini berisi panduan spesifikasi sistem, daftar dependensi, pustaka (*libraries*), serta instruksi langkah-demi-langkah untuk menyiapkan *environment* lokal agar seluruh *notebook* dan eksperimen dalam repositori ini dapat dijalankan tanpa kendala (*reproducible*).

---

## 💻 1. Persyaratan Sistem (System Requirements)

| Komponen | Spesifikasi Minimum | Spesifikasi Rekomendasi |
| :--- | :--- | :--- |
| **Sistem Operasi** | Windows 10/11, macOS 12+, Ubuntu 20.04+ LTS | Windows 11 / macOS / Ubuntu |
| **Python** | `>= 3.12` | `3.12.x` |
| **RAM** | 4 GB | 8 GB atau lebih |
| **Penyimpanan** | 2 GB ruang kosong | 5 GB ruang kosong (termasuk virtualenv & cache) |
| **Arsitektur** | x64 / ARM64 | Multi-core processor (quad-core+) |

---

## 📦 2. Rincian Pustaka & Dependensi (Package Dependencies)

Daftar pustaka utama yang digunakan beserta peruntukannya dalam modul-modul pembelajaran:

| Pustaka / Library | Versi Minimum | Kategori | Peran & Penggunaan dalam Modul |
| :--- | :--- | :--- | :--- |
| **`python`** | `>= 3.12` | Runtime | Bahasa pemrograman utama |
| **`scikit-learn`** | `>= 1.5.0` | Machine Learning | Algoritma klasifikasi, regresi, clustering, pipeline, dan evaluasi metrik |
| **`pandas`** | `>= 2.2.0` | Data Manipulation | Pengolahan DataFrame, manipulasi data tabular, dan data cleaning |
| **`numpy`** | `>= 2.0.0` | Numerical Computing | Komputasi matriks, array multidimensi, dan operasi matematika |
| **`matplotlib`** | `>= 3.8.0` | Data Visualization | Plotting statis, kurva pembelajaran (*learning curve*), dan grafik analisis |
| **`seaborn`** | `>= 0.13.0` | Data Visualization | Visualisasi statistik tingkat tinggi, *heatmap*, korelasi, dan *pairplot* |
| **`imbalanced-learn`** | `>= 0.12.0` | Feature Engineering | Penanganan data tidak seimbang (*class imbalance*) menggunakan SMOTE (**Modul 05**) |
| **`yellowbrick`** | `>= 1.5` | Clustering Diagnostic | Penentuan jumlah klaster optimal (*Elbow method visualizer*) (**Modul 04**) |
| **`scikit-optimize`** | `>= 0.10.2` | Hyperparameter Tuning | Optimasi Bayesian (`BayesSearchCV`) untuk penalaan parameter model (**Modul 07**) |
| **`joblib`** | `>= 1.4.0` | Model Persistence | Penyimpanan dan pemuatan model (*serialization*) format `.joblib` & `.pkl` |
| **`ipykernel`** | `>= 6.29.0` | Jupyter Runtime | Kernel interaktif untuk menjalankan notebook `.ipynb` di VS Code / JupyterLab |
| **`ipywidgets`** | `>= 8.1.0` | Interactive UI | Kontrol interaktif di dalam *notebook* (*progress bar*, slider) |
| **`flask`** | `>= 3.0.0` | Deployment (Opsional) | Framework web mikro untuk *serving* model machine learning sebagai REST API |

---

## 🚀 3. Panduan Instalasi (Step-by-Step Installation)

Pilih salah satu metode berikut untuk menyiapkan *environment* kerja Anda:

### 🔹 Opsi A: Menggunakan `uv` (Direkomendasikan - Sangat Cepat)
Proyek ini telah dikonfigurasi menggunakan [uv](https://github.com/astral-sh/uv), package manager berbasis Rust yang jauh lebih cepat dibandingkan pip standar.

1. **Clone repositori:**
   ```bash
   git clone https://github.com/nugi-ML/machine-learning.git
   cd machine-learning
   ```

2. **Sinkronisasi dependensi secara otomatis:**
   ```bash
   # uv akan membuat virtual environment dan menginstal seluruh package sesuai uv.lock
   uv sync
   ```

3. **Aktifkan virtual environment:**
   - **Windows (PowerShell):**
     ```powershell
     .venv\Scripts\Activate.ps1
     ```
   - **Windows (Command Prompt):**
     ```cmd
     .venv\Scripts\activate.bat
     ```
   - **Linux / macOS:**
     ```bash
     source .venv/bin/activate
     ```

---

### 🔹 Opsi B: Menggunakan Standard `venv` & `pip`
Jika Anda belum menginstal `uv`, Anda dapat menggunakan Python bawaan:

1. **Clone repositori:**
   ```bash
   git clone https://github.com/nugi-ML/machine-learning.git
   cd machine-learning
   ```

2. **Buat Virtual Environment:**
   ```bash
   python -m venv .venv
   ```

3. **Aktifkan Virtual Environment:**
   - **Windows (PowerShell):**
     ```powershell
     .venv\Scripts\Activate.ps1
     ```
   - **Linux / macOS:**
     ```bash
     source .venv/bin/activate
     ```

4. **Upgrade pip & instal dependensi:**
   ```bash
   python -m pip install --upgrade pip
   pip install -r requirements.txt
   ```

5. **Daftarkan Kernel ke Jupyter:**
   ```bash
   python -m ipykernel install --user --name=ml-dicoding --display-name="Python (ML Dicoding)"
   ```

---

## 🔍 4. Verifikasi Instalasi

Jalankan perintah berikut pada terminal di dalam *environment* aktif untuk memverifikasi bahwa pustaka inti telah terpasang dengan benar:

```bash
python -c "import sklearn, pandas, numpy, seaborn, matplotlib, imblearn, yellowbrick; print('Semua dependensi berhasil dimuat!')"
```

Jika output menampilkan teks `Semua dependensi berhasil dimuat!`, maka *environment* Anda siap digunakan.

---

## 🛠️ 5. Menjalankan Notebook di VS Code

1. Buka folder repositori di Visual Studio Code:
   ```bash
   code .
   ```
2. Pastikan ekstensi **Python** dan **Jupyter** sudah terpasang di VS Code.
3. Buka salah satu file `.ipynb` (misalnya pada folder `01 Machine Learning Workflow/main.ipynb`).
4. Klik tombol **Select Kernel** di pojok kanan atas notebook, lalu pilih:
   - Python Environment `.venv` yang telah dibuat.
5. Klik **Run All** untuk mengeksekusi semua sel.

---

## ❓ 6. Penanganan Masalah Umum (Troubleshooting)

- **PowerShell Execution Policy Error saat aktivasi `.venv`:**
  ```powershell
  Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
  ```
- **Modul `scikit-optimize` error saat kompilasi:**
  Pastikan `setuptools` dan `wheel` sudah terinstal versi terbaru (`pip install --upgrade setuptools wheel`).
- **Peringatan `yellowbrick` / `scikit-learn` kompatibilitas:**
  Jika muncul pesan peringatan terkait visualizer, pastikan menggunakan versi scikit-learn yang kompatibel seperti yang tercantum dalam `requirements.txt`.

