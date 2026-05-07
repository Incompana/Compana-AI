# Compana-AI System Plan

## Overview
Tujuan utama sistem untuk menganalisis teks, mengidentifikasi masalah, memberikan rekomendasi, serta mengevaluasi perkembangan pengguna.

---

## ML Modules & Techniques

### 1. Problem Classifier
**Tujuan:** Mengklasifikasikan jenis permasalahan dari input teks pengguna.

**Teknik yang digunakan:**
- Natural Language Processing (NLP)
- TF-IDF (Feature Extraction)
- Naive Bayes (Classification)

**Output:**
- Kategori masalah pengguna

---

### 2. Skill Gap Analyzer
**Tujuan:** Menganalisis kesenjangan antara kondisi pengguna saat ini dengan target yang diinginkan.

**Teknik yang digunakan:**
- TF-IDF (Vectorization)
- Cosine Similarity

**Output:**
- Tingkat kemiripan / gap antar skill

---

### 3. Assessment Generator
**Tujuan:** Menghasilkan pertanyaan atau evaluasi berdasarkan konteks pengguna.

**Teknik yang digunakan:**
- Recurrent Neural Network (RNN) / LSTM

**Output:**
- Pertanyaan atau assessment dinamis

---

### 4. Action Plan Generator
**Tujuan:** Memberikan rekomendasi langkah yang harus dilakukan pengguna.

**Teknik yang digunakan:**
- Rule-based system
- Lightweight Machine Learning (optional)

**Output:**
- Rencana aksi (action plan)

---

### 5. Task Evaluator
**Tujuan:** Mengevaluasi jawaban atau task yang diberikan oleh pengguna.

**Teknik yang digunakan:**
- TF-IDF
- Cosine Similarity

**Output:**
- Nilai evaluasi / feedback

---

### 6. Progress Tracker
**Tujuan:** Melacak perkembangan pengguna dari waktu ke waktu.

**Teknik yang digunakan:**
- Time Series Analysis
- Regression Model

**Output:**
- Tren perkembangan (improvement tracking)

---

## System Flow

Setiap fitur dalam sistem tidak menggunakan seluruh modul secara bersamaan. Modul digunakan secara selektif sesuai dengan kebutuhan fitur:

- Input teks → Problem Classifier  
- Analisis skill → Skill Gap Analyzer  
- Generate pertanyaan → Assessment Generator  
- Rekomendasi → Action Plan Generator  
- Evaluasi → Task Evaluator  
- Monitoring → Progress Tracker  

---

## Requirements
 
Python **3.10** ke atas.
 
Install dependencies:
 
```bash
pip install numpy pandas joblib scikit-learn
```
 
Untuk stemmer Bahasa Indonesia (opsional tapi direkomendasikan):
 
```bash
pip install PySastrawi
```
 
> **Catatan untuk pengguna VS Code:** Pastikan interpreter Python yang dipilih adalah Python 3.10 tempat library terinstall.
> Tekan `Ctrl+Shift+P` → **Python: Select Interpreter** → pilih Python 3.10.
> Cek path-nya dengan: `py -3.10 -c "import sys; print(sys.executable)"`
