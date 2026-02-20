# tugas-kaggle-colab
Tugas Analisis Data - Prediksi Customer Churn
# Prediksi Prestasi Siswa (Student Performance Classification Project)
Proyek ini dibuat untuk memenuhi tugas Analisis Data pada program studi **Pendidikan Matematika**.  
Dataset yang digunakan diambil dari Kaggle dengan topik **Student Performance in Secondary Education**.  
Analisis dilakukan menggunakan **Google Colab** dengan bahasa pemrograman Python.

## Deskripsi Dataset
Dataset ini berisi informasi tentang **prestasi akademik siswa sekolah menengah di Portugal**,  
dengan data yang dikumpulkan melalui laporan sekolah dan kuesioner.  
Tujuan utama dari proyek ini adalah untuk **memprediksi nilai akhir (G3)** atau **menentukan apakah siswa akan lulus atau tidak**  
berdasarkan faktor-faktor sosial, demografi, dan akademik.
Terdapat dua dataset:
- `student-mat.csv` → performa siswa dalam mata pelajaran **Matematika**
- `student-por.csv` → performa siswa dalam mata pelajaran **Bahasa Portugis**

## Variabel Penting
| Variabel | Keterangan |
|-----------|------------|
| school | Sekolah siswa (`GP` = Gabriel Pereira, `MS` = Mousinho da Silveira) |
| sex | Jenis kelamin (`F` = perempuan, `M` = laki-laki) |
| age | Usia siswa |
| address | Tipe alamat (`U` = urban, `R` = rural) |
| studytime | Waktu belajar mingguan (1–4) |
| failures | Jumlah kegagalan sebelumnya |
| absences | Jumlah ketidakhadiran |
| G1 | Nilai periode pertama |
| G2 | Nilai periode kedua |
| G3 | Nilai akhir (target prediksi) |

---

## Langkah Analisis
1. **Eksplorasi Data (EDA)**  
   - Melihat distribusi data, outlier, dan hubungan antar variabel  
   - Visualisasi menggunakan `seaborn` dan `matplotlib`
2. **Preprocessing Data**  
   - Menangani data kategorikal (Label Encoding)  
   - Menghapus kolom yang tidak relevan (jika perlu)  
   - Menangani missing value
3. **Modeling**  
   - Membagi data menjadi *train set* dan *test set*  
   - Menggunakan algoritma **Random Forest Classifier** dan **Logistic Regression**
4. **Evaluasi Model**  
   - Menggunakan metrik: Akurasi, Precision, Recall, F1-score  
   - Visualisasi *Confusion Matrix*

---

## Hasil Model
Hasil model menunjukkan performa klasifikasi yang baik dalam memprediksi kelulusan siswa.

| Metrik | Nilai |
|---------|-------|
| Akurasi | 0.87 |
| Precision (Lulus) | 0.84 |
| Recall (Lulus) | 0.90 |
| F1-Score (Lulus) | 0.87 |

---

## Interpretasi
- **Faktor penting:** `G2`, `studytime`, `failures`, dan `absences` sangat berpengaruh terhadap nilai akhir siswa.  
- **Waktu belajar lebih lama** dan **absensi yang sedikit** berhubungan dengan prestasi akademik yang lebih baik.  
- Model ini mampu membantu pihak sekolah dalam mengidentifikasi siswa yang berpotensi **tidak lulus**  
  sehingga dapat diberikan **bimbingan atau dukungan belajar lebih awal**.

---

## Kesimpulan
Analisis ini menunjukkan bahwa pendekatan *machine learning* dapat digunakan untuk memahami dan memprediksi prestasi akademik siswa.  
Model yang dibuat memiliki tingkat akurasi yang cukup baik dan dapat diterapkan untuk **pengambilan keputusan pendidikan**,  
seperti pemberian intervensi belajar bagi siswa dengan risiko rendah.

---

## File dalam Repository
- `introduction-to-eda-and-machine-learning.ipynb` → notebook analisis di Google Colab  
- `README.md` → penjelasan proyek dan hasil analisis  

---

## 👩‍🎓 Identitas Penulis
**Nama:** Azifah Mutia Rakhmi  
**NIM:** 2304020170  
**Program Studi:** Pendidikan Matematika  
