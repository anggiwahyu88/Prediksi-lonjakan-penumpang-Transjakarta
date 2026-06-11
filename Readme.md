# Executive Summary
Project Name: Prediksi Lonjakan Penumpang Transjakarta pada Hari Kerja, Hari Libur atau Hari Tertentu Created By: Data Engineering Team 3
Date:  February, 2026  Version: 1.0


# 1. Executive Summary

### 1.1 Project Overview

* **Tujuan Project:** Memprediksi tingkat kepadatan penumpang TransJakarta untuk mendukung optimalisasi layanan dan kapasitas operasional.
* **Scope Project:** Integrasi data tanggal, tipe hari, dan jumlah penumpang berbasis open data untuk analisis pola pergerakan.
* **Expected Outcomes:** Dashboard Visualisasi Kepadatan Penumpang berdasarkan tipe hari.
* **Timeline:** Februari - Juni

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

**Source Details**
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


### 2.2 Public APIs

**Source Details**
* **API Name:**  libur deno API
* **Endpoint URL:**  [https://api-hari-libur.vercel.app/api](https://api-hari-libur.vercel.app/api?year=2023)
* **Provider:** libur deno
* **Authentication Method:** -

**API Analysis**
* **Response Format:** JSON
* **Rate Limits:** 60 calls/minute
* **Reliability:** 99.9% uptime
* **Documentation Quality:** Cukup Lengkap
* **Cost:** Gratis 


