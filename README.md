# Prediksi Risiko Komplain Pelanggan Layanan Logistik

Repositori ini berisi notebook Python untuk tugas besar mata kuliah Analitik Data Logistik Lanjut dan Praktikum. Proyek ini bertujuan membangun model prediksi risiko komplain pelanggan layanan logistik menggunakan dataset customer support ticket dan validasi survei pelanggan.

## Deskripsi Proyek

Penelitian ini menggunakan pendekatan machine learning untuk memprediksi risiko komplain pelanggan berdasarkan data tiket layanan pelanggan. Target prediksi dibentuk dari kolom `Customer Satisfaction Rating`, dengan ketentuan:

- Rating 1–2 dikategorikan sebagai risiko komplain tinggi.
- Rating 3–5 dikategorikan sebagai risiko komplain rendah.

Selain pemodelan, proyek ini juga menggunakan data survei pelanggan untuk memperkuat interpretasi hasil dan menghasilkan rekomendasi bisnis.

## Isi Repositori

Repositori ini terdiri dari beberapa file utama:

- `TUGAS_BESAR_FRI_029_2026.ipynb`  
  Notebook utama yang berisi preprocessing data, eksplorasi data, pemodelan machine learning, evaluasi model, analisis survei, dan visualisasi hasil.

- `customer_support_tickets.csv`  
  Dataset customer support ticket yang digunakan sebagai data utama penelitian.

- `Survei Kepuasan Pelanggan Layanan Logistik (Jawaban) - Form Responses.csv`  
  Data hasil survei pelanggan yang digunakan untuk validasi eksternal.

- `README.md`  
  Dokumentasi proyek, cara instalasi, cara menjalankan notebook, dan informasi reproducibility.

- `requirements.txt`  
  Daftar library Python yang dibutuhkan untuk menjalankan notebook.

## Kebutuhan Sistem

Disarankan menggunakan:

- Python 3.10 atau versi lebih baru
- Jupyter Notebook atau JupyterLab
- Git
- Visual Studio Code atau editor lain yang mendukung file `.ipynb`

## Cara Instalasi dan Menjalankan Notebook

### 1. Clone repository

```bash
git clone https://github.com/vieeeeerrraaa07/Prediksi-Risiko-Komplain-Pelanggan-Layanan-Logistik_ADLL.git
```

### 2. Masuk ke folder repository

```bash
cd Prediksi-Risiko-Komplain-Pelanggan-Layanan-Logistik_ADLL
```

### 3. Buat virtual environment

Untuk Windows:

```bash
python -m venv venv
venv\Scripts\activate
```

Untuk macOS/Linux:

```bash
python3 -m venv venv
source venv/bin/activate
```

### 4. Install library yang dibutuhkan

```bash
pip install -r requirements.txt
```

### 5. Jalankan Jupyter Notebook

```bash
jupyter notebook
```

Kemudian buka file:

```text
TUGAS_BESAR_FRI_029_2026.ipynb
```

Jalankan seluruh cell secara berurutan dari atas ke bawah.

## Alternatif Menjalankan di Google Colab

Notebook juga dapat dijalankan melalui Google Colab dengan langkah berikut:

1. Buka Google Colab.
2. Pilih menu `File`.
3. Pilih `Open notebook`.
4. Pilih tab `GitHub`.
5. Masukkan link repository ini.
6. Pilih file `TUGAS_BESAR_FRI_029_2026.ipynb`.
7. Jalankan cell secara berurutan.

Jika terdapat library yang belum tersedia, jalankan perintah berikut di cell awal notebook:

```python
!pip install pandas numpy matplotlib scikit-learn pdfplumber jupyter
```

## Dataset dan Etika Data

Dataset yang digunakan adalah Customer Support Ticket Dataset. Dataset ini dipilih karena sesuai dengan kasus prediksi risiko komplain pelanggan dalam konteks Customer Relationship Management layanan logistik.

Untuk menjaga etika data dan anonimisasi, kolom yang berpotensi mengandung informasi pribadi pelanggan tidak digunakan dalam proses pemodelan, seperti:

- `Ticket ID`
- `Customer Name`
- `Customer Email`

Kolom tersebut dihapus pada tahap preprocessing sebelum data digunakan untuk analisis dan pemodelan.

## Metode Machine Learning

Model machine learning yang digunakan dalam proyek ini adalah:

1. Logistic Regression
2. Decision Tree
3. K-Nearest Neighbors
4. Naive Bayes
5. Artificial Neural Network / Multilayer Perceptron

## Evaluasi Model

Evaluasi model dilakukan menggunakan beberapa metrik, yaitu:

- Accuracy
- Precision
- Recall
- F1-score
- AUC-ROC
- Confusion Matrix
- ROC Curve
- Cross-validation
- Threshold tuning

Pemilihan model final tidak hanya mempertimbangkan accuracy, tetapi juga F1-score dan recall karena tujuan utama penelitian adalah mendeteksi tiket yang berisiko menimbulkan komplain.

## Analisis Survei

Survei digunakan sebagai validasi eksternal untuk memahami faktor-faktor yang memengaruhi pelanggan dalam mengajukan komplain terhadap layanan logistik.

Instrumen survei terdiri dari:

- 7 pertanyaan tertutup berbasis skala Likert 1–5
- 2 pertanyaan terbuka

Analisis pertanyaan tertutup dilakukan menggunakan rata-rata, median, standar deviasi, dan persentase jawaban setuju. Sementara itu, pertanyaan terbuka dianalisis menggunakan pendekatan tematik berdasarkan kata kunci jawaban responden.

## Output Analisis

Notebook menghasilkan beberapa output utama, antara lain:

- Ringkasan missing value
- Hasil preprocessing
- Distribusi target risiko komplain
- Perbandingan performa model machine learning
- Confusion matrix model final
- ROC curve model final
- Threshold tuning
- Feature importance
- Analisis hasil survei Likert
- Analisis tematik jawaban terbuka
- Rekomendasi bisnis berbasis hasil model dan survei

## Catatan Reproducibility

Untuk mereplikasi hasil analisis, lakukan langkah berikut:

1. Clone repository ini.
2. Install seluruh library menggunakan file `requirements.txt`.
3. Pastikan file dataset tersedia dalam folder repository.
4. Jalankan notebook dari cell pertama hingga terakhir.
5. Gunakan random state yang sama seperti pada notebook.
6. Pastikan nama file dataset sesuai dengan yang dipanggil pada notebook.

## Rekomendasi Bisnis

Berdasarkan hasil model dan survei, beberapa rekomendasi bisnis yang dapat diberikan adalah:

1. Menerapkan prioritas tiket berbasis risiko komplain.
2. Memperkuat SLA respon awal dan penyelesaian tiket.
3. Memberikan notifikasi proaktif kepada pelanggan ketika terjadi keterlambatan.
4. Meningkatkan kualitas informasi tracking.
5. Menstandarkan komunikasi customer service agar lebih konsisten dan jelas.
6. Menambahkan fitur operasional seperti durasi keterlambatan, jumlah interaksi, dan histori komplain untuk meningkatkan kualitas model di masa depan.

## Anggota Kelompok

Kelompok FRI-029:

- Elvira Eka Ramadhani
- Christina Limbong
- Syafiq Kamaaluddin

## Mata Kuliah

Analitik Data Logistik Lanjut dan Praktikum  
Program Studi S1 Digital Supply Chain  
Universitas Telkom

## Lisensi

Proyek ini dibuat untuk keperluan akademik pada mata kuliah Analitik Data Logistik Lanjut dan Praktikum.
