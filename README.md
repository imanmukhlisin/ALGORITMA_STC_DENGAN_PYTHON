# Clustering Tweet dengan Suffix Tree Clustering (STC)

Repositori ini berisi implementasi sederhana Suffix Tree Clustering (STC) untuk mengelompokkan tweet hasil crawling dari Twitter berdasarkan kemiripan frasa. Proses ini menggunakan Python dan beberapa library seperti pandas, scikit-learn, dan Sastrawi untuk preprocessing bahasa Indonesia.

## Struktur Folder

```
.
├── crawing_data_tweter.py
├── kelompok1_22230020.csv
├── implementasi_STC/
│   ├── Algoritma_STC.py
│   └── hasil_cluster_22230020csv
├── hasil_clustering.csv
└── ...
```

## Langkah Implementasi

### 1. Crawling Data Twitter

Gunakan [`crawing_data_tweter.py`](crawing_data_tweter.py) untuk mengambil data tweet dari Twitter API dan menyimpannya ke file CSV (`kelompok1_22230020.csv`).  
Pastikan sudah memiliki Bearer Token Twitter API.

### 2. Clustering dengan STC

Jalankan script [`implementasi_STC/Algoritma_STC.py`](implementasi_STC/Algoritma_STC.py) untuk melakukan:
- Preprocessing tweet (hapus link, simbol, dan stopword Indonesia)
- Ekstraksi frasa dari tweet
- Pengelompokan tweet berdasarkan frasa yang sering muncul (minimal di 5 tweet)
- Menyimpan hasil cluster ke file CSV (`hasil_cluster_22230020csv`)

### 3. Hasil

Hasil clustering berupa file CSV yang berisi kolom `Cluster` (nama frasa) dan `Tweet` (isi tweet asli).

## Kebutuhan

- Python 3.x
- Library: pandas, Sastrawi, re, collections

Install dependensi dengan:
```sh
pip install pandas Sastrawi
```

## Catatan

- File input tweet: `kelompok1_22230020.csv` (pastikan sudah ada sebelum menjalankan clustering)
- Threshold jumlah dokumen per cluster dapat diubah pada variabel `min_docs_per_cluster` di script STC.
