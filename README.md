<h1 align="center">Spotify Songs Analysis</h1>
<p align="center">
  <img src="https://github.com/user-attachments/assets/4b615d47-5f0d-4c30-8183-4a1f917f75cb" width="400" height="200" alt="Spotify Logo">
</p>



Proyek ini bertujuan untuk menganalisis faktor-faktor yang memengaruhi popularitas lagu di Spotify. Dengan memanfaatkan dataset Spotify, kami mengeksplorasi hubungan antara fitur audio seperti *danceability*, *energy*, *valence*, dan *tempo* dengan tingkat popularitas lagu. Proyek ini memberikan wawasan yang relevan bagi artis, produser musik, dan playlist creator.

---

## **Table of Contents**
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

##**About**

Musik adalah bagian penting dalam kehidupan kita sehari-hari. Analisis ini bertujuan untuk memahami faktor-faktor utama yang memengaruhi popularitas lagu di Spotify. Kami menganalisis fitur audio seperti *danceability*, *energy*, *valence*, dan *tempo* untuk mencari pola yang dapat membantu artis dan produser dalam menciptakan lagu yang sesuai dengan tren.  

Hasilnya menunjukkan bahwa genre **Pop** dan **EDM** mendominasi popularitas, sementara lagu dengan danceability dan valence tinggi memiliki kecenderungan untuk lebih disukai oleh pendengar. Metode yang digunakan meliputi statistik deskriptif, visualisasi data, dan pembuatan metrik seperti `popularity_score_per_year` untuk mengukur daya tahan popularitas lagu.

---

## **Dataset**

Dataset yang digunakan adalah **Spotify Dataset**, yang mencakup informasi seperti popularitas lagu, fitur audio, genre, dan tahun rilis. Dataset ini tersedia secara publik melalui komunitas *TidyTuesday*.  

- **Sumber**: [Spotify Dataset on TidyTuesday](https://github.com/rfordatascience/tidytuesday).  
- **Download Dataset**: [Klik di sini](https://www.dropbox.com/sh/qj0ueimxot3ltbf/AACzMOHv7sZCJsj3ErjtOG7ya?dl=1).  

Variable utama yang digunakan dalam analisis ini: 

| Column Name     | Description                                                        |
|-----------------|--------------------------------------------------------------------|
| `track_id`      | ID unik yang mewakili setiap lagu dalam database Spotify.          |
| `track_name`    | Nama dari lagu yang dianalisis.                                    |
| `artist_name`   | Nama artis atau grup yang membawakan lagu.                         |
| `popularity`    | Skor popularitas lagu berdasarkan metrik Spotify (skala 0-100).    |
| `danceability`  | Ukuran sejauh mana sebuah lagu cocok digunakan sebagai musik dansa (nilai 0 hingga 1). |
| `energy`        | Tingkat intensitas atau semangat sebuah lagu (nilai 0 hingga 1).   |
| `acousticness`  | Tingkat kemungkinan bahwa sebuah lagu adalah akustik (nilai 0 hingga 1). |
| `tempo`         | Kecepatan beat lagu dalam satuan BPM (beats per minute).           |
| `duration_ms`   | Lama durasi sebuah lagu dalam satuan milidetik.                   |
| `release_year`  | Tahun perilisan lagu.      

Kolom baru yang dibuat untuk analisis:
# Additional Dataset Columns Description

| Column Name              | Description                                                                                       |
|--------------------------|---------------------------------------------------------------------------------------------------|
| `release_decade`         | Dekade rilis lagu berdasarkan `release_year`, dihitung dengan membulatkan tahun rilis ke dekade terdekat. |
| `danceability_score`     | Kategori danceability: Low (<0.4), Medium (0.4-0.7), High (≥0.7)|
| `popularity_segment`     | Kategori popularitas berdasarkan skor: Low (<33), Medium (33-66), High (≥66)|
| `energy_acoustic_mix`    |Menggabungkan `energy` dan `acousticness` untuk klasifikasi lagu|
| `popularity_score_per_year` | Rasio skor popularitas lagu terhadap jumlah tahun sejak dirilis|

---

## **Analysis and Code**

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

## **Storyboard**

1. **Definisi Masalah:**  
   Mengidentifikasi faktor yang memengaruhi popularitas lagu di Spotify.  

2. **EDA:**  
   Mengeksplorasi pola distribusi dan hubungan antar fitur.  

3. **Pembuatan Variabel Baru:**  
   Menambahkan kolom seperti `popularity_score_per_year` untuk menambah wawasan.  

4. **Visualisasi Hasil:**  
   Menyajikan data dalam bentuk grafik dan temuan utama.

---

## **Dependencies**

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
2. Install Repositoris:
   ```bash
   jupyter notebook notebooks/EDA.ipynb
   ```
3. Jalankan pembuatan variabel baru:
   ```bash
   jupyter notebook notebooks/feature_engineering.ipynb
   ```

---

##**Summary**

Proyek ini memberikan wawasan menarik tentang popularitas lagu di Spotify. Temuan utama:
- Genre **Pop** dan **EDM** adalah genre paling populer.  
- Lagu dengan danceability dan valence tinggi lebih cenderung populer.  
- Tren menunjukkan peningkatan popularitas lagu dengan energi tinggi sejak 2015.  

---

## **Results**

1. **Danceability vs Popularity:**  
   Lagu dengan danceability tinggi memiliki rata-rata popularitas yang lebih tinggi.  

2. **Tren Musik Berdasarkan Waktu:**  
   Lagu dengan energi tinggi dan tempo cepat mengalami peningkatan popularitas sejak 2015.  

3. **Genre Populer:**  
   Genre Pop dan EDM mendominasi daftar lagu populer.  

---

## **Team Members**

1. [Jasmin Putri Jelita](https://github.com/Jasm1nPtr)  - 202110370311075
2. [Thyara Mahadewi](https://github.com/thyaraa)  - 202110370311069

---
