<p align="center"> <img src="URL_GAMBAR_BANNER" alt="Smart City Bengkulu" width="100%" /> 
</p>

# 🚦 Smart City: Sistem Prediksi & Navigasi Kemacetan Bengkulu

Proyek ini merupakan bagian dari pengembangan sistem Smart City untuk Kota Bengkulu. Sistem ini bertujuan memberikan **peringatan dini terhadap kemacetan lalu lintas** dan merekomendasikan **rute alternatif** secara visual melalui peta interaktif.

## 📌 Studi Kasus

> Kota Bengkulu ingin mengembangkan sistem navigasi cerdas berbasis AI yang dapat memprediksi dan memperingatkan kemacetan secara visual, serta memberikan rekomendasi rute alternatif kepada masyarakat secara interaktif dan informatif.

---

## 🧠 Model AI yang Digunakan: Algoritma Dijkstra + Penalti Kemacetan

🔍 Prediksi Kemacetan
Menggunakan dua model pembelajaran mesin untuk memprediksi tingkat kepadatan lalu lintas:

Random Forest Regressor
Cocok untuk data tabular dan statis. Memberikan prediksi cepat dan akurat terhadap kondisi jalan pada waktu tertentu.

LSTM (Long Short-Term Memory)
Digunakan untuk data deret waktu (time series) seperti volume kendaraan per jam/menit. Mampu mengenali pola jangka panjang dalam data historis lalu lintas.

🧭 Navigasi Rute
Menggunakan algoritma:

Dijkstra
Efisien untuk mencari jalur terpendek dari titik awal ke tujuan.
→ Dimodifikasi dengan penalti kemacetan untuk memprioritaskan jalan yang lebih lancar.

---

## 📊 Jenis & Sumber Data

- **Data jalan**: OpenStreetMap (diakses dengan `osmnx`)
- **Geolokasi pengguna**: Lokasi awal & tujuan dimasukkan manual → dikonversi menjadi koordinat dengan geopy
- **Kemacetan**: **Data dummy** yang disimulasikan berdasarkan node tertentu secara statis

### 📌 Catatan tentang data dummy:
> Kemacetan tidak diambil dari sumber real-time. Data ini **hanya simulasi** dan tidak mencerminkan kondisi aktual di Kota Bengkulu. Diperlukan integrasi API eksternal untuk mendukung prediksi kemacetan nyata.

---

## ⚙️ Alur Sistem

<img src="https://raw.githubusercontent.com/username/repo-name/main/assets/alur-sistem.png" alt="Alur Sistem Smart City" width="100%" />

---

![Traffic Map Example](https://example.com/traffic-map.png)

---

## 🚀 Ayo mulai!  
Jalankan kode, dan nikmati pengalaman navigasi yang lebih pintar.
