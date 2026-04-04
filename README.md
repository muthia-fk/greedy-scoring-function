# Greedy Scoring Function — Web App

Aplikasi web penjadwalan tugas akademik berbasis Algoritma Greedy Multi-Kriteria.

## Fitur
- Input tugas (nama, deadline, prioritas, durasi, bobot)
- Penjadwalan otomatis dengan Greedy Scoring Function
- Visualisasi 4 grafik (Chart.js)
- Perbandingan Greedy vs Random
- Download hasil ke CSV

## Cara Deploy ke Vercel

### 1. Install Vercel CLI
```bash
npm install -g vercel
```

### 2. Login Vercel
```bash
vercel login
```

### 3. Deploy
```bash
cd greedy-scoring-function
vercel
```
Ikuti promptnya, pilih **No** untuk semua override. Vercel akan otomatis detect Flask.

### 4. Deploy ke production
```bash
vercel --prod
```

## Cara Run Lokal
```bash
pip install flask
cd greedy-scoring-function
python api/index.py
```
Buka http://localhost:5000

## Struktur Project
```
greedy-scoring-function/
├── api/
│   └── index.py          # Flask backend + algoritma greedy
├── templates/
│   └── index.html        # Frontend (HTML + CSS + JS)
├── requirements.txt      # Dependencies Python
├── vercel.json           # Konfigurasi Vercel
└── README.md
```

## Algoritma
```
score(t) = 0.4 * (1/deadline) + 0.4 * priority + 0.2 * (weight/duration)

Time Complexity  : O(n log n)
Space Complexity : O(n)
```
