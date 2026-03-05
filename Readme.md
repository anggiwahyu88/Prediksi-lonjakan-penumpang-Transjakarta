# Prediksi Lonjakan Penumpang TransJakarta

Repositori ini berisi proyek praktik Data Engineering yang bertujuan untuk menganalisis dan memprediksi tingkat kepadatan penumpang armada TransJakarta, khususnya pada hari libur atau hari-hari tertentu. Proyek ini mengimplementasikan proses ETL (Extract, Transform, Load) dengan mengintegrasikan berbagai sumber data terbuka (Open Data).

## 👥 Tim Proyek
Proyek ini disusun oleh mahasiswa Politeknik Negeri Madiun:
* **Prima Afda Mukhlisan(Project Manager)**
* **Anggi Wahyu Saputra(Data Engineer)**
* **Azza Auliyaul Fitri(Data Analyst)**


## 🎯 Tujuan Proyek
* Membangun arsitektur integrasi data (Data Pipeline) yang tangguh.
* Menggabungkan data historis transaksi penumpang dengan kalender hari libur nasional.
* Menyediakan dataset yang bersih dan terstruktur untuk kebutuhan analisis lanjutan atau pemodelan Machine Learning guna memprediksi lonjakan penumpang.

## 📊 Sumber Data (Open Data Sources)
Proyek ini memanfaatkan empat jenis sumber data terbuka:
1. **Data Pemerintah (`data.go.id`)**: Data historis mengenai jumlah operasional bus dan volume penumpang harian.
2. **Kaggle Dataset**: Data transaksi detail dari transportasi publik TransJakarta.
3. **Public API (`libur deno` / API Hari Libur Nasional)**: Data kalender hari libur nasional Indonesia untuk menandai tanggal-tanggal merah atau cuti bersama.
4. **Open Research Data (`satudata.jakarta.go.id`)**: Data spasial dan master data mengenai rute serta jalur lintasan bus TransJakarta.

## ⚙️ Arsitektur Integrasi Data & ETL
1. **Extract**: Menarik data dari API hari libur, mengunduh dataset dari Kaggle dan portal Satu Data / Data.go.id.
2. **Transform**: 
   * Membersihkan data dari nilai *null* atau duplikat.
   * Menstandarkan format tanggal (*datetime*) dari berbagai sumber.
   * Menggabungkan (Join) data transaksi dengan data hari libur berdasarkan tanggal.
   * Memetakan data transaksi dengan master data rute TransJakarta.
3. **Load**: Memuat data yang telah ditransformasi ke dalam Data Warehouse atau format penyimpanan akhir (misal: CSV/Parquet) untuk dianalisis.

