# Topic Modeling with BERTopic

## Deskripsi Proyek

## Struktur Direktori
Struktur direktori dalam proyek ini terbagi menjadi tiga bagian utama:
1. **Direktori `Scripts`** → Berisi semua kode atau notebook yang digunakan untuk melakukan proses ekstraksi, pembersihan, dan analisis data.
2. **Direktori `Data`** → Tempat menyimpan semua dataset hasil dari proses scraping dan preprocessing.
3. **Direktori `Backup Data`** → Berisi salinan dari `Data` sebagai backup jika terjadi kesalahan atau kehilangan data.


## Web Scraping
Pada tahap ini, pengembang melakukan ekstraksi informasi dengan mengeksekusi script. Script ini akan melakukan request ke web yang diinginkan. Web tersebut akan mengirimkan HTTP dimana script akan melakukan ekstraksi data sesuai dengan isinya.
### Constraint
Konstrain digunakann untuk membatasi area permasalahan. Kegunaan konstrain untuk memperjelas permasalahan apa yang ingin diselesaikan dan mempermudah peneliti untuk menyelesaikan masalah yang sudah didefinisikan. Berikut konstrain yang akan didefiniskan:
1. Pengumpulan data berupa judul penelitian
2. Penelitian yang dicari berupa penelitian yang diterbitkan dari rentang **tahun 2015** sampai **2024**
3. Script akan melakukan ekstraksi data dari repositori online **Google Scholar**
4. Proses scraping menggunakan browser **Microsoft Edge**
### Tools yang digunakan
Proses ekstraksi data di web menggunakan pustaka Python berikut:
- `selenium` → melakukan ekstraksi data 
- `pandas` → untuk membaca dan menyimpan dataset mentah  
### Proses Ekstraksi Data
1. **Setup Tools dan Browser** → Menyiapkan tools dan browser sebelum ekstraksi data
2. **Menyiapkan Constraint** → Mendefinisikan konstraint yang sudah dilampirkan di atas
3. **Iterasi Pencarian** → Menelusuri artikel mulai dari tahun **2024**. Setiap tahun akan dilakuan pencarian artikel sebanyak 100 halaman maksimal. 1 halaman berisi 10 artikel
4. **Ekstraksi Data** → Setiap halaman dilakukan ekstraksi judul penelitian dan dimasukkam ke dalam array `titles`.

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
