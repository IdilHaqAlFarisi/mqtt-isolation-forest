# Deteksi Anomali MQTT Dataset menggunakan Isolation Forest

Proyek ini mengimplementasikan sistem deteksi anomali pada dataset MQTT menggunakan algoritma Isolation Forest dengan pendekatan Semi-Supervised Learning.

## 📋 Deskripsi

Sistem ini mendeteksi berbagai jenis serangan pada protokol MQTT, termasuk:
- **DoS (Denial of Service)**
- **Bruteforce**
- **Malformed**
- **Slowite**
- **Flood**

## 📁 Struktur Folder

```
tubes-skc/
├── dataset/
│   └── raw/
│       ├── train70_cleaned.csv
│       └── test30_cleaned.csv
├── isolation-forest-mqt-revisi.ipynb
├── environment.yml
└── README.md
```

## ⚙️ Instalasi & Setup

### Prasyarat
- [Miniconda](https://docs.conda.io/en/latest/miniconda.html) atau Anaconda

### Langkah Instalasi

1. **Clone atau download repository ini**

2. **Buat environment dari file `environment.yml`**
   ```bash
   conda env create -f environment.yml
   ```

3. **Aktifkan environment**
   ```bash
   conda activate anomaly_detection
   ```

4. **Buka file `isolation-forest-mqt-revisi.ipynb` di VS Code/Cursor**

## 📦 Dependencies

| Library | Kegunaan |
|---------|----------|
| pandas | Manipulasi data |
| numpy | Operasi numerik |
| matplotlib | Visualisasi |
| seaborn | Visualisasi statistik |
| scikit-learn | Machine Learning (Isolation Forest) |
| ipykernel | Jupyter kernel untuk notebook |

## 🚀 Cara Menjalankan

1. Pastikan environment `anomaly_detection` sudah aktif
2. Pastikan dataset sudah ada di folder `dataset/raw/`
3. Buka notebook `isolation-forest-mqt-revisi.ipynb`
4. Jalankan semua cell secara berurutan (Run All)

## 📊 Metodologi

1. **Data Preprocessing**: Encoding kategorikal, StandardScaler
2. **Semi-Supervised Learning**: Training hanya dengan data normal
3. **Hyperparameter Tuning**: Grid Search untuk parameter optimal
4. **Threshold Optimization**: Precision-Recall Curve
5. **Evaluasi**: Confusion Matrix, Classification Report, ROC-AUC

## 📝 Catatan

- Dataset MQTT digunakan dengan split 70% training dan 30% testing
- Model menggunakan pendekatan semi-supervised (training dengan data normal saja)

## 📄 Lisensi

Proyek ini dibuat untuk keperluan akademik (Tugas Besar SKC).
