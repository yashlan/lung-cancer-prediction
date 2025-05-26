# lung cancer prediction
thesis research

## Komparasi Distribusi Label (Tahap Split Data)
<img src="https://github.com/yashlan/lung-cancer-prediction/blob/main/ss/st_comparasion.png" width="600" />
Grafik diatas menggambarkan perbedaan distribusi antara memakai stratify (Stratified ShuffleSplit) dengan yg tidak memakai stratify (hanya ShuffleSplit). Menggunakan stratify membuat proposi data train dan test menjadi lebih seimbang.<br>
Definisi Stratified ShuffleSplit: Validator silang atau cross validator yang menyediakan indikator latih/uji untuk membagi data dalam set latih/uji. Objek cross validation ini merupakan gabungan dari StratifiedKFold dan ShuffleSplit, yang mengembalikan lipatan acak bertingkat. Lipatan dibuat dengan mempertahankan persentase sampel untuk setiap kelas. sumber: https://scikit-learn.org/stable/modules/generated/sklearn.model_selection.StratifiedShuffleSplit.html


## Hasil ROC AUC (Tahap Evaluasi Model)
<img src="https://github.com/yashlan/lung-cancer-prediction/blob/main/ss/roc_auc.png" width="600" />
Model Decision Tree saat menggunakan stratified performanya mengalami kenaikan yang cukup signifikan, yaitu dari 0.74xx ke 0.90xx. Sedangkan Model Random Forest mengalami penurunan sekitar 0.01xx.

## Dataset
balanced: https://www.kaggle.com/datasets/chandanmsr/more-accurate-lung-cancer-dataset <br>
imbalanced: https://www.kaggle.com/datasets/mysarahmadbhat/lung-cancer
