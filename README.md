# 📈 TRADING-ANALISIS-FREE-MOBILE
> **Mobile Quant Technical Analyzer, MTF Charts & AI Prompt Generator (Zero AI Token Edition)**

Aplikasi web mobile ultra-ringan untuk analisis teknikal pasar Forex dan Gold (XAU/USD). Dirancang khusus untuk menghasilkan data struktur harga multi-timeframe terformat, prompt cerdas siap pakai ke AI browser (ChatGPT, Claude, Gemini) **tanpa memerlukan saldo API / kuota token AI berbayar**, dilengkapi visualisasi chart interaktif dan kalkulator broker profesional.

🔗 **Live Web App:** [ashtersai.github.io/TRADING-ANALISIS-FREE-MOBILE](https://ashtersai.github.io/TRADING-ANALISIS-FREE-MOBILE/)

---

## ✨ Fitur & Pembaruan Terbaru

- **🚀 Web AI Launchers:** Pintasan cepat di bilah navigasi untuk membuka ChatGPT, Claude, Gemini, atau Custom Web AI dalam satu ketukan. Dilengkapi modal pengaturan (`⚙`) untuk mengubah dan menyimpan alamat URL web AI secara permanen di browser (`localStorage`).
- **📊 Visualisasi TradingView Lightweight Charts:** 
  - **Tab 1 (Validator Chart):** Merender chart candlestick secara dinamis beserta garis horizontal level **Entry (Biru)**, **Take Profit (Hijau)**, **Stop Loss (Merah)**, dan **Level Referensi/Resistance (Kuning)** berdasarkan hasil analisis JSON dari AI.
  - **Tab 2 (Multi-Timeframe Charts):** Menampilkan 5 grafik interaktif terpisah untuk **D1, H4, H1, M15, dan M5** lengkap dengan indikator EMA 20/50, zona *Supply & Demand*, serta titik penanda struktur *CHoCH*.
- **💼 Kalkulator Broker & Posisi Aktif Lengkap:**
  - Menghitung posisi (BUY/SELL), lot, modal, pilihan leverage (`1:100` hingga `1:1000`), dan biaya komisi broker per lot.
  - Menghitung secara otomatis **Floating P/L Kotor & Bersih (Net)**, **Harga Break-Even Point (BEP)**, **Used Margin**, **Equity**, **Free Margin**, **Margin Level (%)** dengan indikator status keamanan akun, serta jarak ketahanan poin (*Stop Out distance*).
  - Data posisi dan manajemen risiko langsung diintegrasikan ke dalam teks prompt AI.
- **📋 Tombol Quick Paste & Clear:** Tombol instan di kotak validator untuk menempelkan (*paste*) teks JSON dari clipboard dan membersihkan layar (*clear*) dengan satu kali klik.
- **💡 Penjelasan Edukatif & Glosarium AI:** Prompt dikunci agar AI tidak hanya memberikan angka, tetapi juga menjabarkan istilah teknikal (*CHoCH, BOS, Rejection Wick, Retrace*) ke dalam Bahasa Indonesia yang mudah dipahami disertai kamus istilah.
- **Zero AI Token Cost & Mobile-First:** Pemrosesan data dilakukan di sisi klien. API Key Twelve Data dan konfigurasi tersimpan aman di penyimpanan lokal perangkat Anda.

---

## 📑 Struktur Navigasi Aplikasi

1. **Tab 1: 📑 GENERATOR PROMPT AI & VALIDATOR**
   - Menarik data OHLC, menyusun prompt multi-timeframe, menyalin prompt ke clipboard, serta memvalidasi balasan JSON dari AI dan merender chart level order.
2. **Tab 2: 📈 MARKET ANALYSIS & DATA OHLC**
   - Menampilkan ringkasan dan 5 grafik visual multi-timeframe (`D1`, `H4`, `H1`, `M15`, `M5`) untuk memverifikasi tren, zona *supply*, dan struktur *CHoCH*.
3. **Tab 3: 💼 MY POSITION & KALKULATOR BROKER**
   - Mengelola status posisi terbuka, menghitung margin, leverage, komisi, dan titik impas BEP.

---

## 🚀 Alur Kerja (Workflow)

```mermaid
graph LR
    A[Pilih Pair] --> B[Ambil Data Pasar]
    B --> C[Salin Prompt Otomatis]
    C --> D[Buka Web AI & Tempel Prompt]
    D --> E[Salin JSON Balasan AI]
    E --> F[Paste ke Web & Validasi Chart]
