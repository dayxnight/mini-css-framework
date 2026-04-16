# ✨ Focus UI Framework
**Lightweight, Mobile-First, and Glassmorphism-based CSS Framework.** 💜

Focus UI adalah kerangka kerja CSS minimalis yang dirancang khusus untuk membangun aplikasi web *mobile* yang estetik dengan sangat cepat. Berfokus pada kelembutan visual (radius 30px) dan efisiensi performa melalui sistem *Flexbox*.

---

## 🚀 Instalasi (Quick Start)

Gunakan layanan **jsDelivr** agar browser dapat membaca file CSS ini dengan benar (menghindari masalah *MIME Type*). Salin baris ini ke dalam tag `<head>` file HTML kamu:

```html
<link rel="stylesheet" href="[https://cdn.jsdelivr.net/gh/](https://cdn.jsdelivr.net/gh/)[USERNAME-GITHUB-MU]/[NAMA-REPO]@main/focusUI.css">

<link href="[https://fonts.googleapis.com/css2?family=Poppins:wght@400;600&display=swap](https://fonts.googleapis.com/css2?family=Poppins:wght@400;600&display=swap)" rel="stylesheet">
```
atau download file css Focus UI melalui github ini

---

## 🎨 1. Konfigurasi (CSS Variables)

Ubah nilai pada variabel `:root` untuk melakukan kustomisasi tema (*theming*) secara instan.

| Variabel | Fungsi |
| :--- | :--- |
| `--primary` | Warna ungu utama untuk tombol aktif. |
| `--secondary` | Warna ungu muda untuk elemen pendukung. |
| `--bg-color` | Warna latar belakang aplikasi. |
| `--radius-lg` | Radius lengkungan kartu (Default: 30px). |
| `--shadow-soft` | Efek bayangan lembut khas lavender. |

---

## 📐 2. Tata Letak (Flexbox Utility)

Focus UI tidak menggunakan sistem *Grid* yang berat. Gunakan utilitas *Flexbox* untuk menyusun elemen dengan lincah.

### Base & Direction
- `.flex`: Mengaktifkan mode Flexbox.
- `.flex-col`: Menyusun elemen menumpuk ke bawah (vertikal).
- `.flex-row`: Menyusun elemen berderet ke samping (horizontal).

### Perataan (Justify & Align)
- `.justify-center`: Rata tengah secara utama.
- `.justify-between`: Elemen tersebar ke ujung kiri dan kanan.
- `.align-center`: Rata tengah secara silang (vertikal/horizontal).

### Jarak (Spacing & Gaps)
Gunakan ukuran `sm` (8px), `md` (16px), atau `lg` (24px).
- `.gap-md`: Memberi jarak antar elemen di dalam flex.
- `.mt-md` / `.mb-md`: Margin atas atau bawah.
- `.p-md`: Padding di dalam elemen.

---

## 🧩 3. Komponen UI

### 🔘 Tombol (Buttons)
- `.btn`: Tombol standar lavender.
- `.btn-primary`: Tombol utama ungu pekat.
- `.btn-pill`: Tombol berbentuk kapsul sempurna.
- `.btn-icon`: Tombol bulat khusus untuk satu ikon.

### 🃏 Kartu (Cards)
- `.card`: Kotak putih bersih dengan radius 30px dan bayangan lembut.

### 📝 Input Form
- `.form-control`: Gaya input teks modern yang ramah sentuhan jari di HP.

### 🧭 Navbar & Modals
- `.navbar`: Bilah menu atas yang menempel (*sticky*) dengan efek kaca.
- `.modal-overlay`: Latar belakang gelap untuk kotak dialog (Gunakan kelas `.show` untuk memunculkan).

---

## 🪟 4. Efek Kaca (Glassmorphism)

Gunakan kelas `.ff-glass` untuk memberikan efek kaca buram pada elemen apa pun.

```html
<div class="ff-glass p-md border-radius-lg">
    <h3>Hello World</h3>
    <p>Efek kaca transparan yang modern.</p>
</div>
```

---

## ⚡ Catatan Performa
Focus UI didesain murni **statis**. Tidak ada animasi transisi di dalam CSS untuk mencegah *lag* pada perangkat mobile. Sangat disarankan untuk menggunakan framework animasi seperti **GSAP** untuk menangani interaksi elemen agar tetap mulus (60 FPS).

---

### dibuat oleh:
> dayxnight
