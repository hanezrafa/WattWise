# ⚡ WattWise — Kalkulator Efisiensi Energi
> Hitung estimasi tagihan listrik bulanan sebelum kaget di akhir bulan.

---

## Tentang Proyek

Tagihan listrik yang membengkak seringkali bukan karena boros, tapi karena tidak tahu perangkat mana yang paling banyak mengonsumsi daya. WattWise membantu pengguna menghitung estimasi konsumsi dan biaya listrik berdasarkan daftar perangkat yang mereka gunakan sehari-hari, disesuaikan dengan golongan PLN masing-masing.

Proyek ini lahir dari konteks proyek IoT sebelumnya setelah membangun sistem monitoring suhu dan efisiensi AC, saya ingin membuat tool yang bisa digunakan siapa saja untuk memahami konsumsi energi perangkat mereka tanpa perlu hardware apapun.

---

## Fitur

- **6 Golongan PLN** — R-1/450 VA hingga R-2/3.500–5.500 VA dengan tarif 2024
- **Preset Perangkat** — AC, kulkas, TV, laptop, dan lainnya bisa ditambah dalam satu klik
- **Kalkulasi Real-time** — Biaya per hari, minggu, dan bulan dihitung otomatis
- **Meter Efisiensi** — Indikator visual konsumsi dengan threshold hemat/boros
- **Deteksi Perangkat Boros** — Otomatis menampilkan perangkat dengan konsumsi tertinggi
- **Persistent Storage** — Data tersimpan di localStorage, tidak hilang saat tab ditutup
- **Tips Hemat** — Rekomendasi praktis untuk mengurangi tagihan

---

## Tech Stack

Proyek ini dibangun dengan **vanilla HTML, CSS, dan JavaScript** — tanpa framework, tanpa build tools, tanpa dependencies. Satu file, langsung jalan di browser.

| Layer | Teknologi |
|---|---|
| Markup | HTML5 |
| Styling | CSS3 (Custom Properties, CSS Grid) |
| Logic | Vanilla JavaScript (ES6+) |
| Storage | localStorage API |
| Deploy | GitHub Pages |

---

## Cara Menjalankan

**Lokal:**
```bash
# Clone repo
git clone https://github.com/[username]/wattwise.git

# Buka di browser — tidak perlu server
open index.html
```

**Atau langsung buka** `index.html` di browser manapun — tidak ada dependency yang perlu diinstall.

---

## Logika Kalkulasi

```
kWh per bulan = (Watt / 1000) × Jam per hari × 30
Biaya per bulan = kWh per bulan × Tarif golongan (Rp/kWh)
```

Meter efisiensi menggunakan referensi 300 kWh/bulan sebagai baseline konsumsi rata-rata rumah tangga R-1/1300 VA.

> **Catatan:** Tarif berdasarkan regulasi PLN 2024. Tagihan aktual dapat berbeda karena pajak, biaya beban, dan biaya admin.

---
