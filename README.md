# 📈 TRADING-ANALISIS-FREE-MOBILE
> **Mobile Quant Technical Analyzer & AI Prompt Generator (Zero AI Token Edition)**

Aplikasi web mobile ultra-ringan untuk analisis teknikal pasar Forex dan Gold (XAU/USD). Dirancang khusus untuk menghasilkan data struktur harga multi-timeframe terformat dan prompt cerdas siap pakai ke AI browser (ChatGPT, Claude, Gemini) **tanpa memerlukan saldo API / kuota token AI berbayar**.

🔗 **Live Web App:** [ashtersai.github.io/TRADING-ANALISIS-FREE-MOBILE](https://ashtersai.github.io/TRADING-ANALISIS-FREE-MOBILE/)

---

## ✨ Fitur Unggulan

- **Zero AI Token Cost:** Pemrosesan data pasar dilakukan di sisi browser. Hasil dikirim langsung ke AI browser favorit Anda lewat satu kali klik salin (*Copy to Clipboard*).
- **Multi-Timeframe Structure (MTF):** Menganalisis pasar menggunakan hierarki institusional:
  - **D1 / H4:** Tren dominan & level Major Support/Resistance.
  - **H1:** Struktur market (*Swing HH/HL/LH/LL, BOS, CHoCH*).
  - **M15:** Area *entry*, *breakout/retest*, dan konfirmasi penutupan candle (*completed candle close*).
- **Twelve Data API Integration:** Menarik harga terkini dan histori pasar secara langsung dan akurat.
- **Mode Simulasi Offline:** Tetap dapat digunakan untuk latihan dan pengujian prompt tanpa perlu memasukkan API key.
- **Rule Strict Pending Orders:** Format instruksi mengunci AI agar hanya merekomendasikan *Pending Order* (*BUY STOP, SELL STOP, BUY LIMIT, SELL LIMIT*) dengan rasio **Risk-to-Reward (RR) minimal 1:2**.
- **Validator Respon AI & Kalkulator RR:** Dilengkapi parser lokal untuk memverifikasi validitas JSON balasan AI dan menghitung kepatuhan rasio RR secara otomatis.
- **Mobile-First & Private:** Dioptimalkan untuk layar smartphone Android/iOS. API Key disimpan secara lokal di `localStorage` perangkat dan tidak dikirim ke server pihak ketiga mana pun.

---

## 🚀 Alur Kerja (Workflow)

```mermaid
graph LR
    A[Pilih Pair] --> B[Ambil Data Pasar]
    B --> C[Salin Prompt Otomatis]
    C --> D[Tempel ke ChatGPT / Claude]
    D --> E[Tempel Balasan JSON ke Web]
    E --> F[Validasi Setup & Kalkulasi RR]

Pilih Instrumen: Pilih pair yang diinginkan (misal XAU/USD atau EUR/USD).Ambil Data: Klik tombol Ambil Data untuk menarik harga terkini (via Twelve Data atau Mode Simulasi).Salin Prompt: Klik tombol 📋 SALIN KE CLIPBOARD.Jalankan di AI: Buka web ChatGPT, Claude, atau Gemini, lalu tekan Paste (Ctrl + V).Validasi Setup: Salin kembali hasil format JSON dari AI ke kolom Validasi Balasan AI untuk memastikan rasio Risk/Reward $\ge 1:2$ sebelum mengeksekusi order.🛠️ Format Standar JSON Balasan AIAI akan mengembalikan respon terstruktur murni dalam format JSON berbahasa Indonesia:

{
  "instrument": "XAU/USD",
  "signal": "BUY STOP",
  "entry": 2745.50,
  "sl": 2738.00,
  "tp": 2761.00,
  "warningLevel": 2742.00,
  "biasReversalLevel": 2735.00,
  "status": "VALID SETUP",
  "reason": "Breakout resistance H1 didukung kelanjutan tren D1 di atas EMA20.",
  "confirmationCondition": "Candle M15 close di atas level 2745.50 dengan momentum bersih.",
  "cancellationCondition": "Harga drop dan close kembali di bawah 2738.00 sebelum entry terpicu."
}

⚙️ Pemasangan & Penggunaan Mandiri
Repositori ini murni menggunakan HTML5, CSS3 murni, dan Vanilla JavaScript tanpa dependencies pihak ketiga (Node.js/npm tidak diperlukan):

Clone repository:

Bash
git clone [https://github.com/ashtersai/TRADING-ANALISIS-FREE-MOBILE.git](https://github.com/ashtersai/TRADING-ANALISIS-FREE-MOBILE.git)
Jalankan:
Cukup klik dua kali berkas index.html untuk membuka di browser apa pun, atau aktifkan GitHub Pages di repositori Anda.

⚠️ Disclaimer
Aplikasi ini dibuat murni untuk tujuan analisis teknikal, edukasi strategi, dan prompt engineering. Segala keputusan eksekusi order trading di pasar finansial merupakan tanggung jawab penuh masing-masing individu. Selalu terapkan manajemen risiko yang ketat.
