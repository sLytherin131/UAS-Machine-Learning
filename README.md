Prediksi Kualitas Udara: Program ini memprediksi kualitas udara dengan menggunakan parameter seperti PM2.5, PM10, SO2, CO, O3, dan NO2, untuk mengklasifikasikan kategori kualitas udara menjadi Good, Medium, atau Unhealthy. 
Dataset yang digunakan adalah AirQualityJakartaData.xlsx.

Fitur Utama
Input: PM2.5, PM10, SO2, CO, O3, NO2
Output: Kategori kualitas udara (Good, Medium, Unhealthy)
Langkah-langkah Proses

1. Preprocessing Data
Memilih kolom penting dari dataset (PM10, PM2.5, SO2, CO, O3, NO2, kategori).
Mengkonversi nilai relevan menjadi numerik dan menghapus nilai kosong.
Melakukan normalisasi data menggunakan MinMaxScaler untuk memastikan fitur berada dalam rentang nilai yang seragam.
Jika kategori AQI bersifat non-numerik, dilakukan encoding menggunakan LabelEncoder.

2. Visualisasi Data
Heatmap: Untuk melihat korelasi antar parameter.
Distribusi: Untuk melihat distribusi nilai dari setiap fitur.
Scatter Plot: Untuk melihat hubungan antar fitur seperti PM10, PM2.5, dan AQI.

3. Modeling
Model yang digunakan untuk klasifikasi dan regresi:
Random Forest Classifier dan XGBoost Classifier untuk klasifikasi kategori AQI.
Linear Regression untuk regresi nilai AQI.
Pembagian data menggunakan train_test_split dengan beberapa perbandingan:
70% untuk training dan 30% untuk testing.
80% untuk training dan 20% untuk testing.
90% untuk training dan 10% untuk testing.

5. Evaluasi Model
Untuk klasifikasi, metrik yang digunakan meliputi:
Akurasi, Precision, Recall, F1-Score, dan laporan klasifikasi.
Untuk regresi, digunakan metrik:
Mean Squared Error (MSE) dan R-squared.

6. Hasil
Ditemukan bahwa model XGBoost menghasilkan kinerja terbaik. Model, scaler, dan label encoder disimpan untuk digunakan dalam prediksi.

7. Prediksi dan Deploy
Program prediksi menggunakan model, scaler, dan label encoder yang telah disimpan.
Program ini kemudian diekspor dari Google Colab ke Visual Studio Code (VSCode) dan dikemas menjadi file app.py untuk dideploy di Streamlit.

![image](https://github.com/user-attachments/assets/59425287-c269-41b1-a1b3-ef27e016d7ec)

