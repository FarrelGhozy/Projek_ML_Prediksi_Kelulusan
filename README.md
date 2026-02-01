### Projek_ML_Prediksi_Kelulusan

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
Tugas Pembauatn model Machine learning untuk projek akhir UAS, dengan bidang yang saya ambil adalah bbidang pendidikan. 

**Tujuan:**
Membangun model Machine Learning yang dapat mendeteksi siswa berisiko **"Gagal"** lebih awal dengan menganalisis faktor latar belakang (seperti waktu belajar, absensi, dan nilai awal), sehingga pihak sekolah dapat memberikan bimbingan khusus sebelum periode ujian berakhir. Atau bisa juga di jadikan sebagai predisi patokan kemampuan siswa untuk tahun depanya.

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
# Cara menjalankan 

```bash 

git clone https://github.com/FarrelGhozy/Projek_ML_Prediksi_Kelulusan.git 

pip install pandas numpy scikit-learn matplotlib

```

---

# Data Pembuat 

- Nama  : Farrel Ghzoy A
- NIM   : 452024611053
- Kelas : TI4 A1 





