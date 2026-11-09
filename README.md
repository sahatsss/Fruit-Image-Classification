# Fruit Image Classification

Klasifikasi gambar 10 jenis buah dengan transfer learning di TensorFlow. Model diekspor ke format SavedModel, TFLite, dan TensorFlow.js.

Kelas: apple, avocado, banana, cherry, kiwi, mango, orange, pineapple, strawberries, watermelon.

## Model

```
Pretrained backbone (EfficientNetB0 / InceptionV3)
→ GlobalAveragePooling2D
→ Dense(256, ReLU)
→ Dropout(0.5)
→ Dense(10, Softmax)
```

Data training diaugmentasi dengan `ImageDataGenerator`.

## Hasil

| Metrik | Nilai |
|---|---|
| Validation accuracy (terbaik) | 0.886 |
| Test accuracy | 0.860 |

## Ekspor

| Format | Kegunaan |
|---|---|
| SavedModel | Serving di server (TensorFlow Serving) |
| TFLite | Aplikasi mobile dan edge device |
| TensorFlow.js | Inference di browser |

File model tidak disimpan di repository karena ukurannya besar. Jalankan notebook untuk menghasilkan ketiga format tersebut.

## Menjalankan

```bash
python -m venv env
source env/bin/activate      # Windows: env\Scripts\activate
pip install -r requirements.txt
jupyter notebook notebook.ipynb
```
