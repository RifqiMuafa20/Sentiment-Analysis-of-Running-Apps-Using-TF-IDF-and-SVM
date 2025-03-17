# **Analisis Sentimen Aplikasi Lari (Nike, Adidas, Strava)**

## **Deskripsi Proyek**
Proyek ini bertujuan untuk melakukan analisis sentimen terhadap ulasan pengguna pada tiga aplikasi lari: **Nike Running, Adidas Running, dan Strava**. Analisis ini menggunakan metode **TF-IDF** sebagai teknik representasi teks dan **Support Vector Machine (SVM)** sebagai model klasifikasi sentimen.

## **Struktur Repository**
```
├── cleaned_data_to_evaluate_model  # Data bersih untuk menguji model
│   ├── data_clean_adidas.xlsx
│   ├── data_clean_nike.xlsx
│   ├── data_clean_strava.xlsx
│
├── cleaning_data_testing  # Kode untuk scrapping dan cleaning data uji
│   ├── adidas.ipynb
│   ├── nike.ipynb
│   ├── strava.ipynb
│
├── scrapped_data  # Data hasil scrapping awal untuk membangun model
│   ├── scrapped_data_adidas.xlsx
│   ├── scrapped_data_nike.xlsx
│   ├── scrapped_data_strava.xlsx
│
├── scrapped_data_to_testing  # Data hasil scrapping untuk menguji model
│   ├── adidas_review.xlsx
│   ├── nike_review.xlsx
│   ├── strava_review.xlsx
│
├── scrapping_data_code  # Kode untuk scraping data
│   ├── scrapAdidasRun.ipynb
│   ├── scrapNikeRun.ipynb
│   ├── scrapStrava.ipynb
│   ├── data_cleaning.xlsx  # Hasil preprocessing data
│
├── index.ipynb  # Notebook utama untuk preprocessing, pelatihan, evaluasi, dan testing model
├── result_filtered.xlsx  # Hasil gabungan data scrapping yang telah diberi label
├── slangword.txt  # Kumpulan slang word untuk preprocessing
```

## **Tahapan Analisis**
### **1. Preprocessing Data**
- Cleaning data
- Tokenisasi kata
- Normalisasi
- Stopwords removal
- Stemming
- Pembuatan word cloud

### **2. Pembobotan Fitur**
- Menggunakan **TF-IDF** untuk merepresentasikan teks sebagai vektor numerik

### **3. Model Klasifikasi**
- **Support Vector Machine (SVM)** digunakan untuk mengklasifikasikan sentimen
- Data dibagi menjadi training dan testing set

### **4. Evaluasi Model**
- **Confusion Matrix**
- **Accuracy, Precision, Recall, dan F1-Score**

## **Hasil Evaluasi Model**
Dari hasil evaluasi, model memiliki performa sebagai berikut:
- **Akurasi:** 89.06%
- **Presisi:** 89.38%
- **Recall:** 89.11%
- **F1-Score:** 89.05%

Model menunjukkan performa yang cukup baik dengan keseimbangan antara presisi dan recall.

## **Analisis Sentimen per Aplikasi**
### **Nike Running**

![image](https://github.com/user-attachments/assets/06988ee8-568e-4f0b-8d47-27ebcac3693b)

- Sentimen negatif dan positif cenderung fluktuatif.
- Lonjakan sentimen positif terjadi pertengahan 2023.
- Sentimen negatif meningkat pada pertengahan hingga akhir 2024, kemungkinan karena masalah teknis atau fitur baru yang tidak disukai.

### **Adidas Running**

![image](https://github.com/user-attachments/assets/7c0b424c-0fd3-40b0-83aa-d8d8abea19fc)

- Sentimen positif lebih dominan dibandingkan negatif.
- Tren positif stabil sejak pertengahan 2023 hingga 2024.
- Menunjukkan bahwa pengguna lebih puas dengan aplikasi ini dibandingkan yang lain.

### **Strava**

![image](https://github.com/user-attachments/assets/d6ebd47e-ab47-4e10-8a0d-f0f2ce576b75)

- Memiliki jumlah sentimen lebih tinggi dibandingkan Nike dan Adidas.
- Awal 2025 mengalami peningkatan sentimen negatif, yang dapat mengindikasikan adanya perubahan fitur atau masalah pada aplikasi.

## **Kesimpulan**
- **Model memiliki akurasi tinggi (89.06%)**, menunjukkan kemampuan yang baik dalam klasifikasi sentimen.
- **Nike Running** mengalami fluktuasi tinggi, terutama lonjakan negatif di 2024.
- **Adidas Running** memiliki tren positif yang lebih stabil.
- **Strava** menunjukkan kenaikan sentimen negatif pada awal 2025, yang bisa menjadi perhatian bagi pengembang aplikasi.

**Catatan:**
Hasil analisis ini dapat digunakan oleh tim pengembang aplikasi untuk memahami sentimen pengguna dan meningkatkan kualitas layanan mereka.
