# 📊 Analisis Sentimen Ulasan Walmart (Logistic Regression + TF-IDF)

Proyek ini melakukan **analisis sentimen** terhadap ulasan pelanggan Walmart menggunakan model **Logistic Regression** dan **TF-IDF Vectorization**. Tujuannya adalah untuk mengklasifikasikan ulasan sebagai **positif** atau **negatif** berdasarkan isi teks ulasan.

---

## 📁 Dataset

Dataset yang digunakan bernama `Walmart.csv`, yang terdiri dari dua kolom utama:
- `content`: Teks ulasan pelanggan
- `score`: Label sentimen (misalnya: `positive`, `negative`)

---

## 🔧 Library yang Digunakan

- `pandas` untuk manipulasi data
- `nltk` untuk preprocessing teks (opsional)
- `scikit-learn` untuk machine learning dan evaluasi
- `matplotlib` dan `seaborn` untuk visualisasi

---

## 🚀 Alur Proyek

1. **Membaca dan Mengecek Data**
   - Dataset dibaca menggunakan `pandas`
   - Distribusi label dicek menggunakan `value_counts()`

2. **Preprocessing**
   - Data dibagi menjadi data latih dan data uji (60% latih, 40% uji)

3. **Vektorisasi TF-IDF**
   - Mengubah teks ulasan menjadi fitur numerik menggunakan TF-IDF dengan maksimal 3000 fitur

4. **Pelatihan Model**
   - Model Logistic Regression dilatih dengan batas iterasi maksimal 1000

5. **Evaluasi Model**
   - Menampilkan **confusion matrix**, **classification report**, dan **akurasi**
   - ROC Curve dikomentari karena tidak cocok untuk multi-class
   - Visualisasi confusion matrix dengan `seaborn`

---

## 📊 Contoh Hasil Evaluasi

- **Akurasi**: Sekitar 68%
- **Confusion Matrix**:
  - Performa tinggi pada kelas dominan
  - Performa rendah pada kelas minoritas
- **Laporan klasifikasi**: Menampilkan precision, recall, dan f1-score

---

## ⚠️ Catatan

- ROC Curve dinonaktifkan karena dataset kemungkinan memiliki lebih dari dua label (bukan hanya positif/negatif)
- Untuk meningkatkan performa, perlu dilakukan pembersihan data dan penyeimbangan kelas

---

## 🔄 Pengembangan Lanjutan

- Mencoba model lain seperti Naive Bayes atau SVM
- Menambahkan preprocessing lanjutan (lemmatization, stemming, dll)
- Menyeimbangkan jumlah data di tiap label
- Mengembangkan model untuk analisis multi-class (misalnya skala bintang 1–5)

---

## ▶️ Cara Menjalankan

```bash
pip install pandas nltk scikit-learn matplotlib seaborn
python sentiment_analysis.py
