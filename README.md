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

## 📊 Jenis, Sumber Data, dan Preprocessing

- **Data jalan**: OpenStreetMap (diakses dengan `osmnx`)
- **Geolokasi pengguna**: Lokasi awal & tujuan dimasukkan manual lalu dikonversi menjadi koordinat dengan geopy
- **Kemacetan**: **Data dummy** yang disimulasikan berdasarkan node tertentu secara statis

### 📌 Catatan tentang data dummy:
> Kemacetan tidak diambil dari sumber real-time. Data ini **hanya simulasi** dan tidak mencerminkan kondisi aktual di Kota Bengkulu. Diperlukan integrasi API eksternal untuk mendukung prediksi kemacetan nyata.

---

## 📈 Strategi Evaluasi Model

- Evaluasi dilakukan dengan data historis lalu lintas menggunakan MSE (Mean Squared Error) sebagai metrik utama untuk prediksi kepadatan.  
- Akurasi dan recall digunakan untuk menilai kemampuan deteksi kemacetan.  
- Validasi model secara berkala dengan data real-time saat integrasi API selesai.

## 🚀 Pengembangan Lanjutan

- Integrasi data real-time dari sensor dan kamera lalu lintas.  
- Pengiriman notifikasi peringatan kemacetan ke pengguna secara langsung.  
- Pengembangan aplikasi mobile interaktif untuk kemudahan akses masyarakat.  
- Integrasi dengan sistem transportasi publik dan layanan ridesharing.

---

## 👥 Tim Pengembang

Ketua  :
Khaylilla Shafaraly Irnanda (G1A023079)

Member :
Aurel Moura Athanafisah  (G1A023001)   
Waridhania As Syifa      (G1A023075)   

---

## 📍 Daftar Lokasi yang Dapat Diakses

| No | Lokasi Populer (Patokan)     |
| -- | ---------------------------- |
| 1  | Kampus 1 Universitas Dehasen |
| 2  | SDIT Rabbani                 |
| 3  | SMA Negeri 5 Bengkulu        |
| 4  | Belakang RRI Bengkulu        |
| 5  | SD Negeri 5 Kota Bengkulu    |
| 6  | RSUD M. Yunus Bengkulu       |
| 7  | Perumahan Bentiring Permai   |
| 8  | Pantai Panjang               |
| 9  | SMPN 07 Kota Bengkulu        |
| 10 | Pasar Panorama               |
| 11 | Pasar Minggu                 |
| 12 | Universitas Bengkulu (UNIB)  |
| 13 | SMPIT Iqra Bengkulu          |
| 14 | Masjid Raya Baitul Izza      |

💡 Gunakan nama lokasi persis seperti tertulis untuk hasil terbaik

---

## ⚙️ Alur Sistem

<img src="https://raw.githubusercontent.com/username/repo-name/main/assets/alur-sistem.png" alt="Alur Sistem Smart City" width="100%" />

---

## 🚀 Ayo mulai!  
Jalankan kode, dan nikmati pengalaman navigasi yang lebih pintar untuk Kota Bengkulu.  
**Menuju kota cerdas yang lebih nyaman dan efisien.**
