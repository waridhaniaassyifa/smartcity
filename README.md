# 🚦 Smart City: Sistem Prediksi & Navigasi Kemacetan Bengkulu

Proyek ini merupakan bagian dari pengembangan sistem Smart City untuk Kota Bengkulu. Sistem ini bertujuan memberikan **peringatan dini terhadap kemacetan lalu lintas** dan merekomendasikan **rute alternatif** secara visual melalui peta interaktif.

## 📌 Studi Kasus

Skenario:
> Kota Bengkulu ingin mengembangkan sistem navigasi cerdas berbasis AI yang dapat memprediksi dan memperingatkan kemacetan secara visual, serta memberikan rekomendasi rute alternatif kepada masyarakat secara interaktif dan informatif.

---

## 🧠 Model AI yang Digunakan: Algoritma Dijkstra + Penalti Kemacetan

Dalam sistem ini, digunakan dua model AI untuk memprediksi tingkat kepadatan lalu lintas, yaitu menggunakan Random Forest Regressor dan LSTM (Long Short-Term Memory). Random Forest dipilih karena kemampuannya yang handal dalam mengolah data statis dan tabular, sehingga dapat memberikan prediksi yang akurat dengan waktu pelatihan yang relatif singkat. Sementara itu, LSTM digunakan untuk data deret waktu, seperti volume kendaraan yang tercatat per menit atau per jam. Karena dapat menangkap pola dan ketergantungan jangka panjang dalam data historis, LSTM memungkinkan prediksi yang lebih dinamis dan responsif terhadap perubahan pola lalu lintas dari waktu ke waktu.

Untuk menentukan rute terbaik, algoritma Dijkstra digunakan karena efisiensinya dalam menemukan jalur terpendek pada graf. Algoritma ini juga dapat dimodifikasi dengan menambahkan penalti pada bobot jalan yang diprediksi mengalami kemacetan, sehingga rute alternatif yang lebih cepat dan lancar dapat dihasilkan. Kombinasi antara model AI untuk memprediksi tingkat kemacetan dan algoritma Dijkstra untuk navigasi membuat sistem ini mampu memberikan rekomendasi rute yang optimal berdasarkan kondisi lalu lintas yang diprediksi.

---

## 📊 Jenis & Sumber Data

- **Data jalan**: OpenStreetMap (diakses dengan `osmnx`)
- **Geolokasi pengguna**: Input manual lokasi awal & tujuan (diubah menjadi koordinat via `geopy`)
- **Kemacetan**: **Data dummy** yang disimulasikan berdasarkan node tertentu secara statis

### 📌 Catatan tentang data dummy:
> Kemacetan tidak diambil dari sumber real-time. Data ini **hanya simulasi** dan tidak mencerminkan kondisi aktual di Kota Bengkulu. Diperlukan integrasi API eksternal untuk mendukung prediksi kemacetan nyata.

---

## ⚙️ Alur Sistem

```mermaid
graph TD
    A[User memasukkan lokasi awal & tujuan] --> B[Geolokasi via Geopy]
    B --> C[Bangun graf jalan Bengkulu via OSMnx]
    C --> D1[Rute utama dengan Dijkstra]
    C --> D2[Rute alternatif dengan penalti kemacetan dummy]
    D1 --> E[Bandingkan rute & deteksi kemacetan]
    D2 --> E
    E --> F[Tampilkan peta dengan folium]
    F --> G[Peta interaktif terbuka di browser]

---

![Traffic Map Example](https://example.com/traffic-map.png)

---

## 🚀 Ayo mulai!  
Jalankan kode, dan nikmati pengalaman navigasi yang lebih pintar.
