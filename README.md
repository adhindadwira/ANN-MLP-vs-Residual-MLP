# Klasifikasi Epilepsi Menggunakan ANN MLP dan Residual MLP pada Dataset EEG BEED

## Deskripsi Tugas Besar

Tugas besar ini merupakan klasifikasi kondisi epilepsi berdasarkan sinyal EEG (Electroencephalography) menggunakan dataset **Bangalore EEG Epilepsy Dataset (BEED)**.

Penelitian ini membandingkan performa dua arsitektur jaringan saraf, yaitu:

- Artificial Neural Network Multi Layer Perceptron (ANN MLP)
- Residual Multi Layer Perceptron (Residual MLP)

Tujuan utama proyek adalah mengetahui apakah penambahan residual connection dapat meningkatkan kemampuan model dalam mengenali pola sinyal EEG dan mengklasifikasikan kondisi epilepsi secara lebih akurat.

---

## Dataset

Dataset yang digunakan adalah **Bangalore EEG Epilepsy Dataset (BEED)** yang berisi data sinyal EEG dari beberapa kondisi neurologis.

### Kelas Data

| Label | Kategori |
|---------|---------|
| 0 | Healthy Subject |
| 1 | Generalized Seizure |
| 2 | Focal Seizure |
| 3 | Seizure Event |

### Karakteristik Dataset

- Jumlah Sampel: 8.000
- Jumlah Fitur EEG: 16 (X1 – X16)
- Jumlah Kelas: 4
- Distribusi Data Seimbang

---

## Tahapan Analisis

### 1. Exploratory Data Analysis (EDA)

Analisis data dilakukan untuk memahami karakteristik dataset melalui:

- Pemeriksaan missing value
- Analisis distribusi kelas
- Statistik deskriptif
- Visualisasi distribusi fitur
- Analisis korelasi antar fitur
- Identifikasi outlier

---

### 2. Preprocessing Data

Tahapan preprocessing yang dilakukan meliputi:

- Pemisahan data train, validation, dan test
- Standardisasi fitur menggunakan StandardScaler
- One-Hot Encoding untuk label kelas

---

### 3. Model ANN MLP

Model pertama menggunakan arsitektur Artificial Neural Network Multi Layer Perceptron sebagai baseline.

Komponen utama:

- Dense Layer
- Batch Normalization
- ReLU Activation
- Dropout
- Softmax Output Layer

---

### 4. Model Residual MLP

Model kedua menggunakan Residual MLP yang menerapkan konsep skip connection seperti pada arsitektur ResNet.

Keunggulan pendekatan ini:

- Memperbaiki aliran gradien
- Mengurangi kehilangan informasi
- Mempermudah proses pembelajaran
- Meningkatkan performa klasifikasi

---

## Evaluasi Model

Model dievaluasi menggunakan metrik berikut:

- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix

---

## Hasil Penelitian

Perbandingan performa menunjukkan bahwa model **Residual MLP** memberikan hasil yang lebih baik dibandingkan ANN MLP pada sebagian besar metrik evaluasi.

Temuan utama:

- Data Healthy Subject memiliki karakteristik yang paling mudah dibedakan.
- Generalized Seizure menunjukkan pola fitur yang cukup khas.
- Focal Seizure dan Seizure Event merupakan kelas yang paling sulit dibedakan.
- Residual MLP mampu meningkatkan kemampuan model dalam mengenali pola EEG yang kompleks.

---

## Teknologi yang Digunakan

- Python
- TensorFlow / Keras
- Scikit-Learn
- Pandas
- NumPy
- Matplotlib
- Seaborn

---

## Struktur Repository

```text
├── Analisis Model.ipynb
├── Dataset EEG
└── README.md
```

---

## Cara Menjalankan Proyek

---

## Visualisasi

### Distribusi Kelas

(<img width="690" height="490" alt="image" src="https://github.com/user-attachments/assets/d0249fb9-d225-4efe-99eb-a4ff38180a7d" />
)

### Heatmap Korelasi

<img width="737" height="590" alt="image" src="https://github.com/user-attachments/assets/8534810d-d21c-470e-a35e-c935fffbc35d" />


### Confusion Matrix ANN MLP vs Residual MLP

<img width="1099" height="495" alt="image" src="https://github.com/user-attachments/assets/fdb41dec-31ad-4599-b0db-e467c5057cbb" />


---

## Kesimpulan

Berdasarkan eksperimen yang dilakukan, model Residual MLP menunjukkan performa yang lebih baik dibandingkan ANN MLP dalam tugas klasifikasi epilepsi menggunakan data EEG.

Penerapan residual connection membantu model mempelajari representasi fitur yang lebih efektif sehingga menghasilkan akurasi dan kemampuan klasifikasi yang lebih tinggi.

---

## Referensi 

[MLP](https://journaljamcs.com/index.php/JAMCS/article/view/2025/4153)

[Residual MLP](https://journaljamcs.com/index.php/JAMCS/article/view/2025/4153)

[Robust Scaler](https://publikasi.dinus.ac.id/index.php/technoc/article/view/10463/4505)

---

## Anggota kelompok:

### Nashwa Aqeela Irtisa Rudin

### Nisrina Hibatullah

### Annisa Sofia Albana

### Auliya Nisa' Nur Rohmah

### Adhinda Dwi Rahmadilla 

### Talitha Ineztasia

