# Projek_ML_Prediksi_Kelulusan

# 🎓 Student Performance Prediction (UAS Machine Learning)

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Scikit-Learn](https://img.shields.io/badge/Library-Scikit--Learn-orange)
![Status](https://img.shields.io/badge/Status-Completed-success)

Proyek ini adalah **Final Project Mata Kuliah Pembelajaran Mesin** yang bertujuan untuk memprediksi potensi keberhasilan atau kegagalan siswa berdasarkan data demografis dan akademik menggunakan pendekatan **Supervised Learning (Klasifikasi)**.

---

## 📋 Daftar Isi
- [Latar Belakang Masalah](#-latar-belakang-masalah)
- [Tentang Dataset](#-tentang-dataset)
- [Pendekatan & Metodologi](#-pendekatan--metodologi)
- [Struktur Proyek](#-struktur-proyek)
- [Hasil & Evaluasi](#-hasil--evaluasi)
- [Cara Menjalankan](#-cara-menjalankan)

---

## 🧐 Latar Belakang Masalah
Sekolah sering kali terlambat menyadari siswa yang berisiko gagal lulus. Biasanya, intervensi baru dilakukan setelah nilai akhir keluar, di mana hal tersebut sudah terlambat.

**Tujuan:**
Membangun model Machine Learning yang dapat mendeteksi siswa berisiko **"Gagal"** lebih awal dengan menganalisis faktor latar belakang (seperti waktu belajar, absensi, dan nilai awal), sehingga pihak sekolah dapat memberikan bimbingan khusus sebelum periode ujian berakhir.

---

## 📊 Tentang Dataset
Data yang digunakan adalah **Student Performance Dataset** dari UCI Machine Learning Repository.
- **Sumber:** [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Student+Performance)
- **Jumlah Data:** 395 baris (Siswa Matematika)
- **Fitur Utama:**
  - `G1`, `G2`: Nilai periode pertama dan kedua.
  - `failures`: Jumlah kegagalan kelas sebelumnya.
  - `studytime`: Waktu belajar mingguan.
  - `absences`: Jumlah ketidakhadiran.
  - `target`: Status kelulusan (Derived from `G3`).

---

## 🛠 Pendekatan & Metodologi

### 1. Mengapa Klasifikasi?
Meskipun data asli (`G3`) berbentuk angka (0-20), proyek ini mengubah masalah menjadi **Klasifikasi Biner** (`Lulus` vs `Gagal`).
- **Alasan:** Tujuan manajerial sekolah adalah pengambilan keputusan "Ya/Tidak" (apakah siswa ini butuh bantuan?), bukan menebak angka presisi. Regresi terlalu sensitif terhadap outlier untuk tujuan biner ini.

### 2. Algoritma
Model yang digunakan adalah **Decision Tree Classifier**.
- **Alasan:** Model ini dipilih karena kemampuannya menghasilkan keputusan yang dapat diinterpretasi (*interpretable*). Pihak sekolah dapat melihat alur logika (misal: "Jika absensi > 10, maka risiko tinggi").

### 3. Alur Kerja
1.  **Preprocessing:** Encoding variabel kategorikal & membagi data (80% Train, 20% Test).
2.  **Feature Engineering:** Membuat kolom target `Status_Kelulusan` (1 jika G3 $\ge$ 10, 0 jika < 10).
3.  **Modeling:** Melatih model dengan data training.
4.  **Evaluasi:** Mengukur performa menggunakan Accuracy, Confusion Matrix, dan Classification Report.

---

## 📂 Struktur Proyek

```bash
├── data/
│   └── student-mat.csv      # Dataset mentah
├── notebooks/
│   └── UAS_ML_Analysis.ipynb # Kode analisis utama (Jupyter Notebook)
├── README.md                # Dokumentasi proyek
└── requirements.txt         # Library yang dibutuhkan
```

Berikut adalah README.md yang profesional, terstruktur, dan siap pakai untuk repositori GitHub atau dokumentasi proyek UAS Anda.Template ini dirancang agar terlihat seperti portofolio Data Science yang serius, mencakup latar belakang masalah, alasan pemilihan metode, dan hasil evaluasi.Silakan salin kode di bawah ini:Markdown# 🎓 Student Performance Prediction (UAS Machine Learning)

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Scikit-Learn](https://img.shields.io/badge/Library-Scikit--Learn-orange)
![Status](https://img.shields.io/badge/Status-Completed-success)

Proyek ini adalah **Final Project Mata Kuliah Pembelajaran Mesin** yang bertujuan untuk memprediksi potensi keberhasilan atau kegagalan siswa berdasarkan data demografis dan akademik menggunakan pendekatan **Supervised Learning (Klasifikasi)**.

---

## 📋 Daftar Isi
- [Latar Belakang Masalah](#-latar-belakang-masalah)
- [Tentang Dataset](#-tentang-dataset)
- [Pendekatan & Metodologi](#-pendekatan--metodologi)
- [Struktur Proyek](#-struktur-proyek)
- [Hasil & Evaluasi](#-hasil--evaluasi)
- [Cara Menjalankan](#-cara-menjalankan)

---

## 🧐 Latar Belakang Masalah
Sekolah sering kali terlambat menyadari siswa yang berisiko gagal lulus. Biasanya, intervensi baru dilakukan setelah nilai akhir keluar, di mana hal tersebut sudah terlambat.

**Tujuan:**
Membangun model Machine Learning yang dapat mendeteksi siswa berisiko **"Gagal"** lebih awal dengan menganalisis faktor latar belakang (seperti waktu belajar, absensi, dan nilai awal), sehingga pihak sekolah dapat memberikan bimbingan khusus sebelum periode ujian berakhir.

---

## 📊 Tentang Dataset
Data yang digunakan adalah **Student Performance Dataset** dari UCI Machine Learning Repository.
- **Sumber:** [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Student+Performance)
- **Jumlah Data:** 395 baris (Siswa Matematika)
- **Fitur Utama:**
  - `G1`, `G2`: Nilai periode pertama dan kedua.
  - `failures`: Jumlah kegagalan kelas sebelumnya.
  - `studytime`: Waktu belajar mingguan.
  - `absences`: Jumlah ketidakhadiran.
  - `target`: Status kelulusan (Derived from `G3`).

---

## 🛠 Pendekatan & Metodologi

### 1. Mengapa Klasifikasi?
Meskipun data asli (`G3`) berbentuk angka (0-20), proyek ini mengubah masalah menjadi **Klasifikasi Biner** (`Lulus` vs `Gagal`).
- **Alasan:** Tujuan manajerial sekolah adalah pengambilan keputusan "Ya/Tidak" (apakah siswa ini butuh bantuan?), bukan menebak angka presisi. Regresi terlalu sensitif terhadap outlier untuk tujuan biner ini.

### 2. Algoritma
Model yang digunakan adalah **Decision Tree Classifier**.
- **Alasan:** Model ini dipilih karena kemampuannya menghasilkan keputusan yang dapat diinterpretasi (*interpretable*). Pihak sekolah dapat melihat alur logika (misal: "Jika absensi > 10, maka risiko tinggi").

### 3. Alur Kerja
1.  **Preprocessing:** Encoding variabel kategorikal & membagi data (80% Train, 20% Test).
2.  **Feature Engineering:** Membuat kolom target `Status_Kelulusan` (1 jika G3 $\ge$ 10, 0 jika < 10).
3.  **Modeling:** Melatih model dengan data training.
4.  **Evaluasi:** Mengukur performa menggunakan Accuracy, Confusion Matrix, dan Classification Report.

---

## 📂 Struktur Proyek

```bash
├── data/
│   └── student-mat.csv      # Dataset mentah
├── notebooks/
│   └── UAS_ML_Analysis.ipynb # Kode analisis utama (Jupyter Notebook)
├── README.md                # Dokumentasi proyek
└── requirements.txt         # Library yang dibutuhkan

```