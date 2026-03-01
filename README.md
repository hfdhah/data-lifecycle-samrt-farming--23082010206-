# 🌾 Smart Farming Sensor Dashboard

Dashboard monitoring data sensor pertanian berbasis IoT menggunakan Streamlit.

---

## 📋 Deskripsi Proyek

Proyek ini memvisualisasikan data sensor pertanian pintar (Smart Farming) tahun 2024
untuk memantau kondisi lahan secara real-time, mendeteksi anomali, dan menganalisis
faktor-faktor yang mempengaruhi hasil panen (yield).

---

## 📁 Struktur File

```
smart-farming-dashboard/
├── app.py                              # Aplikasi Streamlit utama
├── Smart_Farming_Crop_Yield_2024.csv   # Dataset utama (500 baris, 22 kolom)
├── requirements.txt                    # Daftar library Python
└── README.md                           # Dokumentasi proyek
```

---

## 📊 Dataset

- **Sumber**: Smart Farming Sensor Data — Kaggle
- **Link**: kaggle.com/datasets/atharvasoundankar/smart-farming-sensor-data-for-yield-prediction
- **Jumlah Data**: 500 baris, 22 kolom
- **Periode**: Januari — Juni 2024

### Kolom Utama yang Digunakan

| Kolom                  | Deskripsi                        | Satuan     |
|------------------------|----------------------------------|------------|
| soil_moisture_%        | Kelembaban tanah                 | %          |
| temperature_C          | Suhu udara                       | Celsius    |
| humidity_%             | Kelembaban udara                 | %          |
| soil_pH                | Tingkat keasaman tanah           | pH         |
| yield_kg_per_hectare   | Hasil panen per hektar           | kg/ha      |
| timestamp              | Waktu pencatatan sensor          | datetime   |
| crop_type              | Jenis tanaman                    | kategorik  |
| region                 | Wilayah pertanian                | kategorik  |

---

## 📈 Fitur Dashboard

1. **Time Series** — Tren rata-rata sensor per bulan
2. **Gauge Meter** — Status kondisi sensor saat ini dengan indikator warna
3. **Heatmap Korelasi** — Hubungan antar variabel sensor dan yield
4. **Alert System** — Deteksi otomatis data yang melanggar threshold

### Threshold yang Digunakan

| Sensor         | Threshold        | Keterangan          |
|----------------|------------------|---------------------|
| Soil Moisture  | < 25%            | Tanah terlalu kering|
| Humidity       | < 55%            | Kelembaban rendah   |
| Temperature    | > 35°C           | Suhu terlalu panas  |
| Soil pH        | < 5.5 atau > 7.5 | pH tidak ideal      |

---

## 📐 Data Quality Score

| Metrik        | Formula                          | Hasil  |
|---------------|----------------------------------|--------|
| Accuracy      | 1 - (missing values / total)     | ~100%  |
| Completeness  | non-null values / total values   | ~100%  |
| Timeliness    | % data dalam 30 hari terakhir    | ~17%   |

---

## 🚀 Cara Menjalankan

### Install dependencies
```bash
pip install streamlit pandas numpy plotly seaborn matplotlib
```

### Jalankan aplikasi
```bash
streamlit run app.py
```

Buka browser di: `http://localhost:8501`

---

## 🌐 Demo Online

Aplikasi dapat diakses secara publik melalui Streamlit Cloud:
```
https://[username]-smart-farming-dashboard.streamlit.app
```

---

## 🛠️ Teknologi yang Digunakan

- **Python 3.x**
- **Streamlit** — Framework dashboard
- **Pandas** — Manipulasi data
- **Plotly** — Visualisasi interaktif
- **Seaborn & Matplotlib** — Heatmap korelasi
- **NumPy** — Komputasi numerik

---

## 👤 Author

Dibuat sebagai bagian dari tugas Smart Farming IoT Data Analysis 2024.
