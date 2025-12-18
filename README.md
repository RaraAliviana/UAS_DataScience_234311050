# 📘 Analisis Kepuasan Pengguna Terhadap Resep Masakan Berdasarkan Ulasan Teks Menggunakan Machine Learning dan LSTM Deep Learning

## 👤 Informasi Proyek
- **Nama:** Rara Aliviana Gumaranti  
- **Repository:** (isi link GitHub)  
- **Video Demo / Presentasi:** (isi link video)  

---

## 🎯 Ringkasan Proyek
Proyek ini bertujuan untuk melakukan analisis sentimen terhadap ulasan pengguna pada dataset *Recipe Reviews and User Feedback*.  
Analisis dilakukan dengan membandingkan tiga pendekatan berbeda, yaitu:
1. **Baseline Model** (Logistic Regression)
2. **Advanced Machine Learning Model** (Random Forest)
3. **Deep Learning Model** (LSTM)

Setiap model dievaluasi menggunakan metrik klasifikasi untuk menentukan model dengan performa terbaik.

---

## 📄 Problem Statement
- Dataset ulasan tidak memiliki label sentimen eksplisit.
- Data berbentuk teks tidak terstruktur dan mengandung noise.
- Terdapat ketidakseimbangan kelas antara sentimen positif dan negatif.

---
<<<<<<< HEAD
## 📁 Struktur Folder
```
Project/
│
├── data/
│ └── Recipe Reviews and User Feedback Dataset
│
├── images/
│ ├── Confusion Matrix LTSM.png
│ ├── Confusion Matrix Random Forest.png
│ ├── Distribusi Rating Bintang.png
│ ├── Logistic Regression.png
│ ├── Panjang Teks Ulasan.png
│ ├── Perbandingan Performa Model.png
│ ├── Training & Validation Loss.png
│ ├── Training vs Validation Accuracy.png
│ └── WordCloud Ulasan Pengguna.png
│
├── models/
│ ├── model_baseline.pkl
│ ├── model_rf.pkl
│ └── model_lstm_keras
│
├── notebooks/
│ └── UAS_DataScience.ipynb
│
├── src/
│
├── Checklist Submit.md
├── Laporan Proyek Machine Learning.md
├── LAPORAN TUGAS PRAKTIKUM.docx
├── LICENSE
└── README.md
```
---

## 🎯 Goals
- Mengklasifikasikan sentimen ulasan menjadi **positif** dan **negatif**.
- Membandingkan performa model baseline, machine learning, dan deep learning.
- Menentukan model terbaik berdasarkan hasil evaluasi.

>>>>>>> e1233e303e26238de7cf2c345b3665c7303646b1
---

## 📊 Dataset
- **Sumber:** UC Irvine Machine Learning Repository – *Recipe Reviews and User Feedback Dataset*
- **Jumlah Data:** 18.180 ulasan (setelah data cleaning)
- **Tipe Data:** Teks ulasan dan rating bintang

### Fitur Utama
| Fitur | Deskripsi |
|------|----------|
| `text` | Teks ulasan pengguna |
| `stars` | Rating bintang (1–5) |
| `sentiment` | Label sentimen hasil konversi rating |
| `clean_text` | Teks hasil preprocessing |

---

## 🔧 Data Preparation
Tahapan data preparation yang dilakukan:
- **Data Cleaning:** Menghapus data kosong dan kolom tidak relevan
- **Labeling Sentimen:** Konversi rating bintang menjadi label sentimen
- **Text Preprocessing:** Lowercase, penghapusan angka dan tanda baca
- **Feature Extraction:** TF-IDF untuk model ML
- **Tokenization & Padding:** Untuk model LSTM
- **Data Splitting:** Train–test split (80:20) dengan stratifikasi
- **Data Balancing:** Class weighting untuk menangani data imbalanced

---

## 🤖 Modeling
Model yang digunakan dalam proyek ini:
- **Model 1 – Baseline:** Logistic Regression (TF-IDF)
- **Model 2 – Advanced ML:** Random Forest (TF-IDF)
- **Model 3 – Deep Learning:** LSTM (Embedding + Bidirectional LSTM)

---

## 🧪 Evaluation
Metrik evaluasi yang digunakan:
- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix

### Hasil Evaluasi
| Model | Accuracy | F1-Score | Catatan |
|------|----------|----------|---------|
| Logistic Regression | 0.8188 | 0.8324 | Stabil sebagai baseline |
| Random Forest | **0.8504** | **0.8517** | Performa terbaik |
| LSTM | 0.8386 | 0.8422 | Baik, namun belum optimal |

---

## 🏁 Kesimpulan
- **Model Terbaik:** Random Forest  
- **Alasan:** Memberikan performa tertinggi dan stabil, serta mampu menangkap hubungan non-linear pada data TF-IDF  
- **Insight:**  
  - Model ML klasik masih sangat kompetitif untuk analisis sentimen  
  - Model deep learning membutuhkan tuning dan data lebih besar agar optimal  

---

## 🔮 Future Work
- [ ] Menambah jumlah dan variasi data
- [ ] Hyperparameter tuning lebih lanjut
- [ ] Menggunakan model pretrained (BERT)
- [ ] Deployment menggunakan Streamlit atau Gradio

---

## 📁 Struktur Folder

## 🔁 Reproducibility

Untuk memastikan hasil eksperimen dapat direproduksi dengan baik, proyek ini dijalankan menggunakan environment dan dependensi berikut:

### Python Version
- Python 3.10+

### Dependencies
```txt
numpy==1.26.4
pandas==2.1.4
scikit-learn==1.4.1
matplotlib==3.8.3
seaborn==0.13.2

# Natural Language Processing
nltk==3.8.1
regex==2023.12.25

# Deep Learning
tensorflow==2.15.0
keras==2.15.0

# Utilities
joblib==1.3.2
tqdm==4.66.2

