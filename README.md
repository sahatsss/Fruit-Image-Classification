
# Fruit Image Classifier Project

Proyek ini bertujuan membangun model klasifikasi gambar buah menggunakan TensorFlow dan transfer learning. Model telah dilatih untuk mengenali 10 jenis buah:

- Apple
- Orange
- Avocado
- Kiwi
- Mango
- Pineapple
- Strawberries
- Banana
- Cherry
- Watermelon

---

## Struktur Direktori

```
submission/
├── tfjs_model/
│   ├── group1-shard1of22.bin
|   |── group1-shard2of22.bin
|   |── group1-shard3of22.bin
|   |── group1-shard4of22.bin
|   |── group1-shard5of22.bin
|   |── group1-shard6of22.bin
|   |── group1-shard7of22.bin
|   |── group1-shard8of22.bin
|   |── group1-shard9of22.bin
|   |── group1-shard10of22.bin
|   |── group1-shard11of22.bin
|   |── group1-shard12of22.bin
|   |── group1-shard13of22.bin
|   |── group1-shard14of22.bin
|   |── group1-shard15of22.bin
|   |── group1-shard16of22.bin
|   |── group1-shard17of22.bin
|   |── group1-shard18of22.bin
|   |── group1-shard19of22.bin
|   |── group1-shard20of22.bin
|   |── group1-shard21of22.bin
|   |── group1-shard22of22.bin
│   └── model.json
├── tflite/
│   ├── model.tflite
│   └── label.txt
├── saved_model/
│   ├── saved_model.pb
│   └── variables/
│       ├── variables.data-00000-of-00001
│       └── variables.index
├── notebook.ipynb
├── README.md
└── requirements.txt
```

---

## Setup environment

1. **Aktifkan environment:**
   ```bash
   python -m venv env
   env\Scripts\activate  
   pip install -r requirements.txt
   ```

2. **Jalankan notebook:**
   - File `notebook.ipynb` yang berisi seluruh proses:
     - Pemrosesan data
     - Pelatihan model
     - Evaluasi

---

## Arsitektur Model

Model menggunakan transfer learning:
- Backbone: EfficientNetB0 / InceptionV3 (pretrained)
- GlobalAveragePooling2D
- Dense(256) + ReLU
- Dropout(0.5)
- Dense(10) + Softmax

---

## Ekspor Model

| Format        | Lokasi                   
|---------------|---------------------------|
| SavedModel    | `submission/saved_model/` | 
| TFLite        | `submission/tflite/`      | 
| TensorFlow.js | `submission/tfjs_model/`  | 

---

## Dependencies

Lihat `requirements.txt` untuk daftar library yang digunakan.

---
