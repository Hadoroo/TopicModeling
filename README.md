# Topic Modeling with BERTopic

## Deskripsi Proyek

## Struktur Direktori

## Web Scraping

## Data Cleaning
### Tools yang digunakan
Proses pembersihan data menggunakan beberapa pustaka Python, yaitu:  
- `pandas` → untuk membaca dan menyimpan dataset  
- `nltk` → untuk tokenisasi, stopwords, stemming, dan lemmatization  
- `langdetect` → untuk mendeteksi bahasa dalam judul penelitian  
- `Sastrawi` → untuk stemming bahasa Indonesia
### Proses Pembersihan
1. **Menghilangkan nilai NaN** → Mengisi judul kosong dengan string kosong  
2. **Tokenisasi** → Memecah kalimat menjadi kata-kata  
3. **Menghapus karakter non-alfanumerik** → Hanya menyimpan huruf dan angka  
4. **Deteksi bahasa** → Menggunakan `langdetect` untuk menentukan bahasa  
5. **Stopword removal** → Menghapus kata-kata umum yang tidak bermakna  
6. **Lemmatization (untuk Inggris)** → Mengubah kata ke bentuk dasarnya  
7. **Stemming (untuk Indonesia)** → Mengubah kata ke akar katanya  
