# Proyek Data Mining - UTS Submission: Batik Classification - Hyperparameter Tuning

**Nama**: Rama Syailana Dewa  
**NIM**: 22.11.5017  

---
TODO : 
1. Applicated Grid Search dan Genetic Algorithm
2. Fast API
3. Docker setup and deploy

| **Aspek** | **Deskripsi** |
|----------|---------------|
| **Dataset** | [Mendeley Data: Batik Nitik 960](https://data.mendeley.com/datasets/sgh484jxzy/3) + [Mendeley Data : Batik Nitik Sarimbit 120](https://data.mendeley.com/datasets/cx5sr2dgrr/1) Grouping 2 dataset |
| **Solusi Machine Learning** | Dibangun model klasifikasi citra berbasis MobileNetV2 untuk mengenali 60 kelas Batik. Model ini diharapkan dapat membantu dalam mengetahui motif Batik secara cepat dan efisien. |
| **Pengolahan Data** | Dataset dibagi ke dalam train (70%), validation (15%), dan test (15%). Data augmentasi dilakukan menggunakan `ImageDataGenerator` (rotasi, zoom, shear, shift, flip, brightness). Gambar dinormalisasi (`rescale=1./255`) dan diubah ukurannya ke 224x224 piksel. Label dikonversi ke one-hot encoding. |
| **Arsitektur Model** | Menggunakan pre-trained **MobileNetV2** (tanpa `include_top`) sebagai feature extractor. Ditambahkan layer `Conv2D`, `MaxPooling2D`, `GlobalAveragePooling2D`, dan `Dense` untuk klasifikasi. Output layer menggunakan `softmax` dengan 60 neuron. |
| **Hyperparameter Tuning** | Menggunakan RandomSearch (nantinya akan mengguakan Grid Seach dan Genetic Algorithm  |
| **Metrik Evaluasi** | Menggunakan `categorical_accuracy`. Visualisasi training & validation dilakukan melalui grafik akurasi dan loss. Dan juga Confusion Matrix|
| **Performa Model** | Akurasi mencapai **97.78%** Non Tuned, **98.88%** with Tuned menunjukkan bahwa performa Tuned lebih baik. |
| **Kesimpulan** | Model berhasil dikembangkan untuk klasifikasi Batik dengan akurasi validasi tinggi. Sistem ini dapat dikembangkan lebih lanjut untuk aplikasi Website dan mendukung masyarakat digital untuk melestarikan budaya Batik. |

---
> 📌 *Code ini dibuat untuk memenuhi tugas uts kelas Proyek Data Mining.*
