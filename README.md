# lung cancer prediction
thesis research

## Info Studi 1
ini adalah penjelasan dari : https://github.com/yashlan/lung-cancer-prediction/blob/main/thesis_lung_cancer_prediction.ipynb

## Dataset
dataset: https://www.kaggle.com/datasets/mysarahmadbhat/lung-cancer <br>
jumlah data (baris): 309

## Distribusi Data
<img src="https://github.com/yashlan/lung-cancer-prediction/blob/main/ss/distribusi.png" width="400" />
Berdasarkan grafik diatas, datanya tidak seimbang. Lebih dominan pada kelas YES. bagusnya tambahkan metode SMOTE atau lainnya. namun studi ini tidak fokus kesana, jadi tidak dibuat.

## Hasil Split Data
<img src="https://github.com/yashlan/lung-cancer-prediction/blob/main/ss/st_comparasion.png" width="600" />
Grafik diatas menggambarkan perbedaan distribusi antara memakai stratify (Stratified ShuffleSplit) dengan yg tidak memakai stratify (hanya ShuffleSplit). Menggunakan stratify membuat proposi data train dan test menjadi lebih seimbang.<br>
Definisi Stratified ShuffleSplit: Validator silang atau cross validator yang menyediakan indikator latih/uji untuk membagi data dalam set latih/uji. Objek cross validation ini merupakan gabungan dari StratifiedKFold dan ShuffleSplit, yang mengembalikan lipatan acak bertingkat. Lipatan dibuat dengan mempertahankan persentase sampel untuk setiap kelas. sumber: https://scikit-learn.org/stable/modules/generated/sklearn.model_selection.StratifiedShuffleSplit.html

## Performa Klasifikasi
| Model      | Stratified | Accuracy | Precision YES | Precision NO | Recall YES | Recall NO | F1-score YES | F1-score NO | AUC  |
|----------------|------------|----------|---------------|--------------|------------|-----------|---------------|--------------|------|
| Decision Tree  | No         | 97%      | 98%           | 50%          | 98%        | 50%       | 98%           | 50%          | 0.74 |
| Decision Tree  | Yes        | 92%      | 98%           | 64%          | 93%        | 88%       | 95%           | 74%          | 0.90 |
| Random Forest  | No         | 97%      | 98%           | 50%          | 98%        | 50%       | 98%           | 50%          | 0.95 |
| Random Forest  | Yes        | 92%      | 96%           | 67%          | 94%        | 75%       | 95%           | 71%          | 0.94 |

## Performa Komputasi
| Algorithm      | Stratified | Execution Time (s) | RAM Usage (MB)    | CPU Energy (J)     |
|----------------|------------|---------------------|--------------------|---------------------|
| Decision Tree  | No         | 0.0011 – 0.0096     | 0.0009 – 0.0069    | 0.0105 – 0.1183     |
| Decision Tree  | Yes        | 0.0011 – 0.0112     | 0.0009 – 0.0037    | 0.0051 – 0.1133     |
| Random Forest  | No         | 0.1126 – 0.2220     | 0.0633 – 0.0721    | 1.0331 – 3.7964     |
| Random Forest  | Yes        | 0.1121 – 0.2306     | 0.0653 – 0.0724    | 1.0371 – 2.6858     |

## Grafik ROC AUC
<img src="https://github.com/yashlan/lung-cancer-prediction/blob/main/ss/roc_auc.png" width="600" />
Model Decision Tree saat menggunakan stratified performanya mengalami kenaikan yang cukup signifikan, yaitu dari 0.74xx ke 0.90xx. Sedangkan Model Random Forest mengalami penurunan sekitar 0.01xx.

---
---
---
---

## Info Studi 2
ini adalah penjelasan dari : https://github.com/yashlan/lung-cancer-prediction/blob/main/thesis_lung_cancer_prediction_newww.ipynb

## Dataset
dataset: https://www.kaggle.com/datasets/chandanmsr/more-accurate-lung-cancer-dataset <br>
jumlah data (baris): 1157

## Distribusi Data
<img src="https://github.com/yashlan/lung-cancer-prediction/blob/main/ss_2/distribusi.png" width="400" />
Data dalam grafik diatas tidak seimbang, lebih dominan pada kelas NO. Namun masih ok, tidak terlalu ekstrem.

## Cross-Validation
Studi ini menggunakan 10-fold cross-validation untuk memastikan bahwa hasil evaluasi model bersifat lebih stabil. Dalam metode ini, data dibagi menjadi 10 bagian yang sama besar, kemudian proses pelatihan dan pengujian dilakukan sebanyak 10 kali, dengan masing-masing bagian secara bergantian digunakan sebagai data uji dan sisanya sebagai data latih. selengkapnya cek: https://scikit-learn.org/stable/modules/cross_validation.html

## Performa Klasifikasi
| Metric         | Decision Tree | Random Forest |
|----------------|---------------|----------------|
| Accuracy (%)   | 93.3%         | 93.3%          |
| Precision (%)  | 97%           | 95.9%          |
| Recall (%)     | 87.9%         | 88.8%          |
| F1-Score (%)   | 92.1%         | 92.2%          |
| AUC (0.00)     | 0.91          | 0.94           |

## Performa Komputasi
| Model         | Training Time (s) | Testing Time (s) | Training Memory Current (MB) | Training Memory Peak (MB) | Testing Memory Current (MB) | Testing Memory Peak (MB) | Training CPU Energy (J) | Training DRAM Energy (J) | Testing CPU Energy (J) | Testing DRAM Energy (J) |
|---------------|----------------|----------------|--------------------------|----------------------|-------------------------|---------------------|------------------------|-------------------------|-----------------------|------------------------|
| Decision Tree | 0.0140         | 0.0066         | 0.0027                   | 0.1860               | 0.0012                  | 0.0230              | 0.0627                 | 0.0177                  | 0.0369                | 0.0121                 |
| Random Forest | 0.7139         | 0.0386         | 0.0699                   | 0.2270               | 0.0087                  | 0.0248              | 2.8809                 | 1.1854                  | 0.1721                | 0.0666                 |

