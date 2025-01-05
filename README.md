# 🎶 **Spotify Songs Analysis**

Proyek ini bertujuan untuk menganalisis faktor-faktor yang memengaruhi popularitas lagu di Spotify. Dengan memanfaatkan dataset Spotify, kami mengeksplorasi hubungan antara fitur audio seperti *danceability*, *energy*, *valence*, dan *tempo* dengan tingkat popularitas lagu. Proyek ini memberikan wawasan yang relevan bagi artis, produser musik, dan playlist creator.

---

## 📌 **Table of Contents**
1. [About](#about)  
2. [Dataset](#dataset)  
3. [Analysis and Code](#analysis-and-code)  
4. [Storyboard](#storyboard)  
5. [Dependencies](#dependencies)  
6. [Tutorial](#tutorial)  
7. [Summary](#summary)  
8. [Results](#results)  
9. [Team Members](#team-members)

---

## 💡 **About**

Musik adalah bagian penting dalam kehidupan kita sehari-hari. Analisis ini bertujuan untuk memahami faktor-faktor utama yang memengaruhi popularitas lagu di Spotify. Kami menganalisis fitur audio seperti *danceability*, *energy*, *valence*, dan *tempo* untuk mencari pola yang dapat membantu artis dan produser dalam menciptakan lagu yang sesuai dengan tren.  

Hasilnya menunjukkan bahwa genre **Pop** dan **EDM** mendominasi popularitas, sementara lagu dengan danceability dan valence tinggi memiliki kecenderungan untuk lebih disukai oleh pendengar. Metode yang digunakan meliputi statistik deskriptif, visualisasi data, dan pembuatan metrik seperti `popularity_score_per_year` untuk mengukur daya tahan popularitas lagu.

---

## 📊 **Dataset**

Dataset yang digunakan adalah **Spotify Dataset**, yang mencakup informasi seperti popularitas lagu, fitur audio, genre, dan tahun rilis. Dataset ini tersedia secara publik melalui komunitas *TidyTuesday*.  

- **Sumber**: [Spotify Dataset on TidyTuesday](https://github.com/rfordatascience/tidytuesday).  
- **Download Dataset**: [Klik di sini](https://www.dropbox.com/sh/qj0ueimxot3ltbf/AACzMOHv7sZCJsj3ErjtOG7ya?dl=1).  

Dataset ini telah dibersihkan dan disesuaikan untuk analisis lebih lanjut.

---

## 📈 **Analysis and Code**

Analisis dilakukan melalui beberapa langkah:
1. **Exploratory Data Analysis (EDA):**  
   - Analisis distribusi popularitas lagu.  
   - Hubungan antara fitur audio dan popularitas.  
   - Tren genre musik berdasarkan dekade.  

2. **Feature Engineering:**  
   - `popularity_score_per_year`: Mengukur daya tahan popularitas lagu.  
   - `danceability_score`: Kategori danceability (Low, Medium, High).  
   - `energy_acoustic_mix`: Kombinasi energy dan acousticness lagu.  

3. **Visualisasi Data:**  
   - Scatter plot untuk hubungan fitur audio.  
   - Line chart untuk tren genre berdasarkan waktu.  
   - Bar chart untuk genre populer.

Kode lengkap dapat ditemukan di direktori `notebooks/` dan `src/`.

---

## 🎨 **Storyboard**

1. **Definisi Masalah:**  
   Mengidentifikasi faktor yang memengaruhi popularitas lagu di Spotify.  

2. **EDA:**  
   Mengeksplorasi pola distribusi dan hubungan antar fitur.  

3. **Pembuatan Variabel Baru:**  
   Menambahkan kolom seperti `popularity_score_per_year` untuk menambah wawasan.  

4. **Visualisasi Hasil:**  
   Menyajikan data dalam bentuk grafik dan temuan utama.

---

## 🛠️ **Dependencies**

Proyek ini menggunakan pustaka berikut:  
- `pandas`  
- `numpy`  
- `matplotlib`  
- `seaborn`  
- `datetime`

Instal semua pustaka dengan perintah:
```bash
pip install -r requirements.txt
```

---

## 📚 **Tutorial**

1. Clone repositori ini:
   ```bash
   git clone https://github.com/Jasm1nPtr/Spotify-Songs-Data-Analysis.git
   cd spotify-songs-analysis
   ```
2. Jalankan analisis EDA:
   ```bash
   jupyter notebook notebooks/EDA.ipynb
   ```
3. Jalankan pembuatan variabel baru:
   ```bash
   jupyter notebook notebooks/feature_engineering.ipynb
   ```

---

## 📝 **Summary**

Proyek ini memberikan wawasan menarik tentang popularitas lagu di Spotify. Temuan utama:
- Genre **Pop** dan **EDM** adalah genre paling populer.  
- Lagu dengan danceability dan valence tinggi lebih cenderung populer.  
- Tren menunjukkan peningkatan popularitas lagu dengan energi tinggi sejak 2015.  

---

## 🏆 **Results**

1. **Danceability vs Popularity:**  
   Lagu dengan danceability tinggi memiliki rata-rata popularitas yang lebih tinggi.  

2. **Tren Musik Berdasarkan Waktu:**  
   Lagu dengan energi tinggi dan tempo cepat mengalami peningkatan popularitas sejak 2015.  

3. **Genre Populer:**  
   Genre Pop dan EDM mendominasi daftar lagu populer.  

---

## 👥 **Team Members**

1. [Jasmin Putri Jelita](https://github.com/Jasm1nPtr)  - 202110370311075
2. [Thyara Mahadewi](https://github.com/thyaraa)  - 202110370311069

---
