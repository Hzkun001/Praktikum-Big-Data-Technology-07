# Big Data Praktikum 7 - Smart City Traffic Prediction

Repository ini berisi implementasi Praktikum Big Data 7 untuk analisis dan prediksi lalu lintas (traffic) pada skenario smart city.

Jika pada praktikum sebelumnya (Praktikum 6) fokusnya adalah tahap sebelumnya, maka pada Praktikum 7 ini alur dibuat lengkap dari:
1. Data cleaning
2. Training model machine learning
3. Visualisasi dan prediksi melalui dashboard interaktif

## Tujuan Praktikum

1. Membersihkan data traffic mentah agar siap dianalisis.
2. Melatih model regresi untuk memprediksi jumlah kendaraan.
3. Menyajikan metrik, grafik tren, dan fitur prediksi pada dashboard Streamlit.

## Struktur Proyek

```
bigdata-praktikum7/
├── analytics/
│   └── traffic_ml_model_v1.py
├── dashboard/
│   └── traffic_dashboard_v1.py
├── data/
│   ├── clean/
│   │   └── traffic_smartcity_clean_v1.csv
│   └── raw/
│       └── traffic_smartcity_v1.csv
├── models/
│   └── traffic_model_v1.pkl
└── scripts/
    └── traffic_data_cleaning_v1.py
```

## Teknologi yang Digunakan

1. Python
2. Pandas
3. Scikit-learn
4. Joblib
5. Streamlit
6. Matplotlib

## Persiapan Environment

Disarankan menggunakan virtual environment.

1. Buat dan aktifkan virtual environment:

```bash
python -m venv venv
source venv/bin/activate
```

2. Install dependensi:

```bash
pip install pandas scikit-learn joblib streamlit matplotlib
```

## Cara Menjalankan Praktikum 7

Jalankan perintah berikut secara berurutan dari root folder proyek.

1. Data Cleaning

```bash
python scripts/traffic_data_cleaning_v1.py
```

Output:
- File bersih: `data/clean/traffic_smartcity_clean_v1.csv`

2. Training Model

```bash
python analytics/traffic_ml_model_v1.py
```

Output:
- Model tersimpan: `models/traffic_model_v1.pkl`

3. Menjalankan Dashboard

```bash
streamlit run dashboard/traffic_dashboard_v1.py
```

Dashboard menampilkan:
1. Nilai rata-rata traffic
2. Nilai maksimum traffic
3. Grafik tren traffic
4. Fitur prediksi traffic berdasarkan jam, hari, dan traffic sebelumnya

## Alur Data

1. Data mentah dibaca dari folder `data/raw`.
2. Data dibersihkan dan disimpan ke folder `data/clean`.
3. Data bersih digunakan untuk feature engineering dan training model.
4. Model hasil training dipakai oleh dashboard untuk prediksi real-time sederhana.

## Catatan

1. Pastikan file data mentah tersedia pada `data/raw/traffic_smartcity_v1.csv`.
2. Jalankan proses training ulang jika data berubah.
3. Jika model belum ada, dashboard tidak dapat melakukan prediksi.

