# Executive Summary
Project Name: Prediksi Lonjakan Penumpang Transjakarta pada Hari Libur atau Hari Tertentu Created By: Data Engineering Team 3
Date:  February, 2026  Version: 1.0


# 1. Executive Summary

### 1.1 Project Overview

* **Tujuan Project:** Memprediksi tingkat kepadatan penumpang TransJakarta untuk mendukung optimalisasi layanan dan kapasitas operasional.
* **Scope Project:** Integrasi data transaksi, rute, halte, dan pengguna berbasis open data untuk analisis pola pergerakan.
* **Expected Outcomes:** Dashboard Visualisasi Kepadatan Penumpang dan Model Prediksi Tren Perjalanan.
* **Timeline:** Februari - Mei

### 1.2 Stakeholders

* **Project Owner:** Program Studi / Institusi (Politeknik Negeri Madiun)
* **Team Members:** * **Data Engineer:** Anggi Wahyu
    * **Data Analyst:** Azza Auliyaul Fitri
    * **Project Manager:** Prima Afda
* **End Users:**
    * PT Transportasi Jakarta (TransJakarta)
    * Dinas Perhubungan DKI Jakarta
    * Analis Data Transportasi

---

# 2. Data Source Analysis

### 2.1 Data Pemerintah (data.go.id)

a. **Source Details**
* **Dataset Name:** Data Jumlah Bus yang Beroperasi dan Jumlah Penumpang Layanan Transjakarta

* **URL/Access Point:** https://data.go.id/dataset/dataset/data-jumlah-bus-yang-beroperasi-dan-jumlah-penumpang-layanan-transjakarta

* **Data Owner:** Provinsi DKI Jakarta

* **Update Frequency:** Triwulan


**Data Analysis**
* **Format Data:** CSV, Excel
* **Volume Data:** 4,03 KB
* **Time Coverage:** Oktober 2023 - September 2025
* **Data Quality:**
    * **Completeness:** 100% 
    * **Accuracy:**  High (data resmi pemerintah DKI Jakarta)
    * **Consistency:** Good (format standar)
    * **Timeliness:**  Updates every 3 month    

b. **Source Details**
* **Dataset Name:** Jumlah Penumpang Angkutan Umum yang Terlayani per Hari Tahun 2023

* **URL/Access Point:** https://data.go.id/dataset/dataset/jumlah-penumpang-angkutan-umum-yang-terlayani-per-hari-tahun-2023?utm_source

* **Data Owner:** Provinsi DKI Jakarta
* **Update Frequency:**  Dayly

**Data Analysis**
* **Format Data:** CSV, Excel
* **Volume Data:** 4,03 KB
* **Time Coverage:** Januari 2023 - Desember 2023
* **Data Quality:**
    * **Completeness:** 98% 
    * **Accuracy:**  High (data resmi pemerintah DKI Jakarta)
    * **Consistency:** Good (format standar)
    * **Timeliness:**  Updates everyday 


### 2.2 Dataset Kaggle

**Source Details**
* **Dataset Name:** Transjakarta - Public Transportation Transaction
* **URL/Access Point:** https://www.kaggle.com/datasets/dikisahkan/transjakarta-transportation-transaction
* **Creator/Publisher:**  dikisahkan (Kaggle Contributor)
* **Last Update:**  April, 2023

**Data Analysis**
* **Format Data:** CSV
* **Size & Dimensions:**  8.98MB, 37.000 rows.
* **Data Fields:**
    * `transID`
    * `payCardID`
    * `payCardBank`
    * `payCardName`
    * `payCardSex`
    * `payCardBirthDate`
    * `corridorID`
    * `corridorName`
    * `direction`
    * `tapInStops`
    * `tapInStopsName`
    * `tapInStopsLat`
    * `tapInStopsLon`
    * `tapInTime`
    * `tapOutStops`
    * `tapOutStopsName`
    * `tapOutStopsLat`
    * `tapOutStopsLon`
    * `tapOutTime`
    * `payAmount`
* **Quality Metrics:**
    * **Missing Values:**  3–6% (mainly in tap-out related fields)
    * **Data Types:** Properly formatted and structured according to standard tabular.
    * **Consistency:** High
    * **Documentation Quality:**  Good - From official open data portal of PT Transportasi Jakarta 

### 2.3 Public APIs

**Source Details**
* **API Name:**  libur deno API
* **Endpoint URL:**  https://libur.deno.dev/api
* **Provider:** libur deno
* **Authentication Method:** -

**API Analysis**
* **Response Format:** JSON
* **Rate Limits:** 60 calls/minute
* **Reliability:** 99.9% uptime
* **Documentation Quality:** Cukup Lengkap
* **Cost:** Gratis 

### 2.4 Open Research Data

**Source Details**
* **Dataset Name:** Data Rute Jalur Transjakarta 
* **Repository:**  satudata.jakarta.go.id - Data Rute Jalur Transjakarta

* **Research Institution / Publisher:** BPBUMD (Provinsi DKI Jakarta)
* **Publication Date:** Maret 2024

**Data Analysis**
* **Format & Structure:** CSV 
* **Data Volume:** 49,7 Kb
* **Data Quality:** High (Data resmi PT Trans Jakarta)
* **Citation Requirements:** Pemerintah Provinsi DKI Jakarta. (2025). Data Rute Jalur TransJakarta. Satu Data Jakarta. https://satudata.jakarta.go.id/open-data/detail/data-rute-jalur-transjakarta (acces: 15 Februari 2026)
