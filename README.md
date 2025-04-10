# 🧠 Analisis Sentimen Aplikasi Dana

Proyek ini dibuat berdasarkan banyaknya keluhan dan pengalaman pengguna yang beredar di platform **Threads** terkait aplikasi **Dana**, terutama mengenai layanan, sistem, dan keamanan. Dari sanalah muncul ide untuk melakukan **analisis sentimen** terhadap ulasan pengguna aplikasi Dana yang tersedia di Google Play Store.

---

## 📌 Deskripsi Proyek

Proyek ini bertujuan untuk:
- Mengambil data ulasan pengguna aplikasi Dana dari Google Play Store.
- Melakukan preprocessing teks ulasan.
- Melatih beberapa model deep learning (CNN, LSTM, GRU) untuk klasifikasi sentimen.
- Melakukan inferensi untuk memprediksi sentimen dari ulasan baru.

---
## 🛠️ Teknologi yang Digunakan

Proyek ini menggunakan berbagai teknologi dan pustaka Python untuk mendukung proses pengumpulan data, pemrosesan teks, pelatihan model, hingga inferensi:

### 📌 Bahasa dan Platform
- **Python 3** – Bahasa pemrograman utama.
- **Jupyter Notebook** – Untuk eksperimen, visualisasi, dan dokumentasi proses.

### 📚 Library dan Framework
- **TensorFlow & Keras** – Untuk membangun dan melatih model deep learning (CNN, LSTM, GRU).
- **scikit-learn** – Untuk evaluasi model, pembagian data, dan preprocessing tambahan.
- **Pandas & NumPy** – Untuk manipulasi data dan operasi numerik.
- **Matplotlib & Seaborn** – Untuk visualisasi data dan hasil evaluasi model.
- **Sastrawi** – Untuk preprocessing teks Bahasa Indonesia (stopword removal, stemming).
- **Google Play Scraper (`google-play-scraper`)** – Untuk scraping data ulasan aplikasi Dana dari Play Store.
- **Pickle** – Untuk menyimpan dan memuat tokenizer yang digunakan dalam preprocessing.

> Semua dependensi dapat ditemukan dan diinstal melalui file `requirements.txt`.

---
## 🧠 Model Deep Learning

Tiga model utama yang digunakan dalam proyek ini:

- **CNN (Convolutional Neural Network)**  
  Model ini efektif dalam menangkap fitur lokal dari teks ulasan. Cocok digunakan untuk mendeteksi pola-pola pendek seperti frasa sentimen.

- **LSTM (Long Short-Term Memory)**  
  LSTM dirancang untuk memahami dependensi jangka panjang dalam teks, sehingga sangat baik dalam menangkap konteks ulasan yang lebih panjang.

- **GRU (Gated Recurrent Unit)**  
  GRU mirip dengan LSTM namun memiliki struktur yang lebih sederhana, dan seringkali memberikan performa setara dengan waktu pelatihan yang lebih cepat.

> Ketiga model tersebut dilatih menggunakan dataset yang berisi **12.000 ulasan aplikasi Dana** dalam Bahasa Indonesia yang diambil dari Google Play Store.

---
## ✅ Ringkasan Hasil Prediksi

| No | Ulasan                                                                                   | Prediksi LSTM | Prediksi GRU | Prediksi CNN |
|----|-------------------------------------------------------------------------------------------|---------------|---------------|---------------|
| 1  | Aplikasi ini sangat membantu dan tampilannya menarik sekali!                             | Netral        | Netral        | Netral        |
| 2  | Cukup baik, tapi ada kendala saat masuk aplikasi.                                        | Netral        | Netral        | Netral        |
| 3  | Saya kecewa, aplikasinya sering error dan lambat.                                         | Negatif       | Negatif       | Negatif       |
| 4  | Aplikasinya bagus, nyaman dan juga sangat mudah digunakan dan transfer cukup cepat       | Positif       | Positif       | Positif       |
| 5  | Keren, saya sudah lama menggunakan aplikasi Dana, tidak ada kendala                      | Netral        | Positif       | Netral        |

---

## 📁 Struktur Direktori

Submission/ 
├── Dataset/ 
│ └── ulasan_dana_12000.csv 
├── Model/
│ ├── model_cnn.h5 
│ ├── model_gru.h5 
│ ├── model_lstm.h5 
│ └── tokenizer.pkl
├── Inference_Zaenal_Syamsyul_Arief.ipynb
├── Scrapping_Data_Ulasan_Dana_Zaenal_Syamsyul_Arief.ipynb
├── Submission_Analisis_Sentiment_Aplikasi_Dana_Zaenal_Syamsyul_Arief.ipynb
└── requirements.txt


---

## 🚀 Cara Menjalankan

1. **Clone repositori ini:**
   ```bash
   git clone https://github.com/username/Analisis-Sentimen-Aplikasi-Dana.git
   cd Analisis-Sentimen-Aplikasi-Dana
    `install dependensi:`
     `pip install -r requirements.txt`
