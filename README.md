# Analisis Sentimen Media Sosial Berbahasa Indonesia

Proyek portofolio untuk membangun pipeline NLP yang dapat direproduksi: pengumpulan teks publik berbahasa Indonesia, pembersihan dan anotasi, lalu klasifikasi sentimen **positif**, **negatif**, dan **netral**. Topik awal yang diusulkan adalah sentimen publik terhadap kendaraan listrik di Indonesia.

> **Status:** tahap setup lingkungan. Dataset belum dikumpulkan, belum ada data yang dianotasi, dan belum ada model yang dilatih.

## Tujuan pembelajaran

- Mendokumentasikan sumber, metode, tanggal, dan batasan pengumpulan data.
- Membersihkan dan menormalisasi teks tanpa menghilangkan sinyal seperti negasi dan emoji.
- Menyusun pedoman anotasi dan memeriksa kualitas label.
- Membandingkan TF-IDF + Logistic Regression dengan FastText embeddings + LSTM.
- Melaporkan evaluasi, analisis kesalahan, batasan, serta pertimbangan privasi dan lisensi.

## Struktur proyek

```text
.
├── data/
│   ├── raw/          # Data sumber; tidak dilacak Git
│   ├── interim/      # Hasil antara pembersihan
│   └── processed/    # Data siap analisis/model
├── models/           # Artefak model; tidak dilacak Git
├── notebooks/        # Eksplorasi dan eksperimen
├── reports/figures/  # Grafik dan keluaran laporan
├── src/              # Kode Python yang dapat digunakan ulang
├── .gitignore
└── requirements.txt
```

Folder data mentah dan model dikecualikan dari Git. Sebelum membagikan data atau artefak apa pun, tinjau lisensi, ketentuan platform, privasi, dan batas redistribusinya. Jangan menaruh kredensial atau token akses di repository.

## Setup lokal

Dijalankan di PowerShell dari folder proyek:

```powershell
py -3.11 -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install -r requirements.txt
```

Untuk membuka JupyterLab:

```powershell
python -m jupyter lab
```

Di VS Code, pilih interpreter/kernel `.venv\Scripts\python.exe` untuk proyek ini.

## Rencana eksperimen

1. Setup lingkungan dan dokumentasi.
2. Menentukan sumber data dan metode pengumpulan yang diizinkan.
3. Membersihkan data serta menyimpan tahapan pemrosesan.
4. Menganotasi sampel dengan pedoman yang konsisten dan pemeriksaan kualitas.
5. Membuat baseline TF-IDF + Logistic Regression.
6. Melatih FastText + LSTM setelah data dan baseline siap.
7. Mengevaluasi model dengan precision, recall, F1-score, confusion matrix, dan analisis kesalahan.

Belum ada hasil eksperimen atau metrik model yang diklaim pada tahap ini.
