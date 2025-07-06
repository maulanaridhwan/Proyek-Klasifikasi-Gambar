# Intel Image Classification

Klasifikasi 6 jenis pemandangan alam menggunakan CNN di Keras  
Dataset: Intel Image Classification (17.000 gambar, 6 kelas)

---

## Deskripsi
Proyek ini membangun model Convolutional Neural Network untuk mengenali 6 kategori pemandangan alam:

- `buildings`  
- `forest`  
- `glacier`  
- `mountain`  
- `sea`  
- `street`

Menggunakan dataset Intel Image Classification yang berisi 25.000 gambar berukuran 150×150 piksel.

---

## Setup Lingkungan
1. Buat virtual environment dan aktifkan:
   ```bash
   python -m venv venv-classification
   source venv-classification/bin/activate   # Mac/Linux
   venv-classification\Scripts\activate      # Windows

2. Install dependencies:
pip install -r requirements.txt

---

## Menjalankan Notebook
Pastikan venv aktif.

Jalankan:
```bash
jupyter notebook notebook.ipynb

---

## Arsitektur Model
- Sequential dengan 3 blok Conv2D + MaxPooling2D
- Flatten → Dense(256, ReLU) → Dropout(0.5) → Dense(6, Softmax)

---

## Training & Validasi
- Epochs: 30
- Optimizer: Adam
- Loss: Categorical Crossentropy
- Callbacks: EarlyStopping, ReduceLROnPlateau, ModelCheckpoint

---
