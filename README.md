# Introduction to Machine Learning with Python
A Guide for Data Scientists - Andreas C. Muller & Sarah Guido

Repository ini berisi ringkasan dan implementasi kode dari buku
Introduction to Machine Learning with Python oleh Andreas C. Muller
& Sarah Guido (O'Reilly). Setiap bab disajikan dalam file Jupyter
Notebook terpisah yang berisi penjelasan konsep, kode yang dapat
dijalankan, dan visualisasi.

---

## Struktur Repository

├── 01.Introduction.ipynb
├── 02.Supervised_Learning.ipynb
├── 03.Unsupervised_Learning.ipynb
├── 04.Representing_Data.ipynb
├── 05.Model_Evaluation.ipynb
├── 06.Algorithm_Chains_and_Pipelines.ipynb
├── 07.Working_with_Text_Data.ipynb
├── 08.Wrapping_Up.ipynb
└── README.md

---

## Ringkasan Per Bab

---

### Bab 1 - Introduction
File: 01.Introduction.ipynb

Bab pembuka yang memperkenalkan ekosistem Machine Learning dengan Python.
Dijelaskan secara rinci kegunaan setiap library utama:

- NumPy       : operasi array, matriks, dan komputasi numerik yang efisien
- Pandas      : manipulasi dan analisis data tabular (DataFrame, Series)
- Matplotlib  : visualisasi data (line plot, scatter plot, histogram)
- SciPy       : komputasi ilmiah dan sparse matrix
- Scikit-learn: library ML utama dengan API konsisten (.fit, .predict, .score)

Dilanjutkan dengan pengenalan konsep supervised vs unsupervised learning,
pembagian data training/test set, dan implementasi model pertama menggunakan
k-Nearest Neighbors pada Iris dataset.

---

### Bab 2 - Supervised Learning
File: 02.Supervised_Learning.ipynb

Bab terpanjang yang membahas berbagai algoritma Supervised Learning secara
mendalam, mencakup klasifikasi dan regresi.

Algoritma yang dibahas:
- k-Nearest Neighbors      : pengaruh nilai k terhadap overfitting
- Linear/Ridge/Lasso       : regularisasi L1 dan L2
- Logistic Regression      : parameter C untuk regularisasi
- Decision Tree            : feature importance, max_depth
- Random Forest            : ensemble method, bagging
- Gradient Boosting        : boosting sekuensial, learning rate
- Support Vector Machine   : kernel trick, margin maximization
- Neural Network (MLP)     : hidden layers, activation function

Konsep kunci: overfitting, underfitting, regularisasi, dan feature importance.

---

### Bab 3 - Unsupervised Learning
File: 03.Unsupervised_Learning.ipynb

Membahas metode ML yang bekerja tanpa label, dibagi menjadi dua kelompok:

Preprocessing & Dimensionality Reduction:
- StandardScaler, MinMaxScaler, RobustScaler : normalisasi fitur
- PCA   : reduksi dimensi dengan memaksimalkan variansi
- NMF   : faktorisasi non-negatif, cocok untuk data gambar dan teks
- t-SNE : visualisasi data berdimensi tinggi ke 2D

Clustering:
- K-Means             : clustering cepat dengan Elbow Method
- Agglomerative       : hierarchical clustering dengan dendrogram
- DBSCAN              : clustering berbasis densitas, deteksi outlier otomatis

---

### Bab 4 - Representing Data and Engineering Features
File: 04.Representing_Data.ipynb

Membahas Feature Engineering, yaitu transformasi data mentah menjadi
representasi yang optimal untuk model ML.

Topik yang dicakup:
- One-Hot Encoding      : fitur nominal (kategori tanpa urutan)
- Ordinal Encoding      : fitur ordinal (kategori dengan urutan logis)
- Binning               : mengubah fitur kontinu menjadi interval diskrit
- Polynomial Features   : menangkap hubungan non-linear dengan model linear
- Transformasi Log/Sqrt : menormalisasi distribusi yang skewed
- Feature Selection     : Univariate, Model-based untuk memilih fitur terbaik
- Imputation            : menangani missing values

---

### Bab 5 - Model Evaluation and Improvement
File: 05.Model_Evaluation.ipynb

Membahas cara mengevaluasi model secara benar dan reliable, serta
cara meningkatkannya melalui hyperparameter tuning.

- Cross-Validation    : K-Fold dan Stratified K-Fold
- GridSearchCV        : exhaustive hyperparameter search
- RandomizedSearchCV  : hyperparameter search yang lebih efisien

Metrik evaluasi:
- Accuracy  : dataset seimbang
- Precision : minimasi false positive
- Recall    : minimasi false negative
- F1-Score  : keseimbangan precision dan recall
- ROC-AUC   : evaluasi di berbagai threshold
- MSE/MAE/R2: masalah regresi

---

### Bab 6 - Algorithm Chains and Pipelines
File: 06.Algorithm_Chains_and_Pipelines.ipynb

Membahas Pipeline sebagai solusi untuk menggabungkan preprocessing
dan model dalam satu alur yang bersih dan aman dari data leakage.

- Penjelasan data leakage dan cara mencegahnya
- Membuat pipeline dengan Pipeline dan make_pipeline
- Kombinasi Pipeline + GridSearchCV
- ColumnTransformer untuk data campuran numerik dan kategorik

Best Practice: Selalu gunakan Pipeline agar preprocessing dilakukan
secara benar di setiap fold cross-validation.

---

### Bab 7 - Working with Text Data
File: 07.Working_with_Text_Data.ipynb

Membahas cara merepresentasikan dan mengklasifikasikan data teks dengan ML.

- Bag of Words (CountVectorizer) : representasi teks sebagai frekuensi kata
- TF-IDF (TfidfVectorizer)       : pembobotan kata berdasarkan kelangkaannya
- N-Gram                         : menangkap konteks frasa multi-kata
- Text Classification Pipeline   : TF-IDF + Logistic Regression
- Analisis Sentimen              : klasifikasi ulasan berbahasa Indonesia
- Topic Modeling (LDA)           : menemukan topik tersembunyi tanpa label

---

### Bab 8 - Wrapping Up
File: 08.Wrapping_Up.ipynb

Bab penutup yang membahas cara berpikir dan bekerja sebagai
ML practitioner di dunia nyata.

- Checklist Proyek ML    : langkah sistematis dari framing hingga deployment
- Humans in the Loop     : peran manusia dan konsep Active Learning
- Prototype ke Production: menyimpan model dengan joblib, membungkus dalam API
- Testing Production     : unit test, A/B testing, monitoring concept drift
- Custom Estimator       : membuat transformer/classifier kompatibel sklearn
- Scaling Dataset Besar  : partial_fit, Dask, Spark, GPU acceleration
- Roadmap Belajar        : Deep Learning, NLP, Reinforcement Learning
