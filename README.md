# lung cancer prediction
my thesis research <br>
source code : https://github.com/yashlan/lung-cancer-prediction/blob/main/thesis_lung_cancer_prediction.ipynb

## Paper
coming soon

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

## Future Research
Sebagai bentuk komitmen terhadap transparansi dan kolaborasi ilmiah, seluruh kode sumber, data, dan hasil penelitian ini telah diunggah ke GitHub dan dapat diakses secara terbuka oleh semua pihak. Tidak ada manipulasi data; seluruh hasil disajikan sebagaimana adanya.<br><br>
Penelitian ini berkontribusi dalam memperluas pemahaman mengenai pemanfaatan machine learning untuk diagnosis medis berbasis real-time, terutama di lingkungan layanan kesehatan yang terbatas. Penelitian selanjutnya disarankan untuk mengeksplorasi metode ensemble lanjutan seperti XGBoost atau LightGBM, serta mengintegrasikan pendekatan Explainable AI (XAI) guna meningkatkan transparansi dan kepercayaan pengguna terhadap model yang dikembangkan.<br><br>
Validasi menggunakan data klinis nyata juga sangat penting agar model yang dibangun dapat digeneralisasi dengan baik ke dalam praktik medis sehari-hari. Pengujian di berbagai institusi kesehatan dengan kondisi operasional yang beragam juga direkomendasikan untuk menilai ketahanan (robustness) dan adaptabilitas sistem.<br><br>
Saya akan sangat menghargai apabila ada pihak yang melakukan koreksi terhadap studi ini, menjadikannya sebagai jurnal pembanding, memperluas kajian dengan pendekatan atau variabel yang berbeda, ataupun mengaplikasikan temuan studi ini dalam konteks atau wilayah yang lain. Setiap bentuk pengembangan atau kritik terhadap penelitian ini akan menjadi kontribusi berarti bagi kemajuan bidang ini secara kolektif.
