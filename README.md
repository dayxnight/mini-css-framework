# Focus ui
dibuat dengan bantuan AI dan dengan beberapa customisasi sesuai dengan selera dan kebutuhan

# 🎨 Panduan Variabel Focus UI

Focus UI dibangun menggunakan **CSS Variables** (`:root`) untuk memudahkan kustomisasi tema secara instan tanpa perlu membongkar seluruh baris kode CSS. Cukup ubah nilai pada variabel di bawah ini untuk menciptakan suasana aplikasi yang berbeda.

---

## 💜 1. Palette Warna (Monochrome Lavender)
Warna dasar Focus UI menggunakan skema *Monochrome Lavender* yang memberikan kesan tenang dan profesional.

| Nama Variabel | Nilai Default | Kegunaan |
| :--- | :--- | :--- |
| `--bg-color` | `#f8f7ff` | Warna latar belakang utama halaman. |
| `--text-color` | `#4527a0` | Warna teks utama agar tetap kontras dan mudah dibaca. |
| `--primary` | `#9575cd` | Warna identitas utama (tombol, elemen aktif). |
| `--primary-dark` | `#7e57c2` | Warna primer yang lebih gelap (untuk efek klik/tekan). |
| `--secondary` | `#d1c4e9` | Warna pendukung untuk elemen yang lebih lembut. |
| `--secondary-transparent` | `rgba(209, 196, 233, 0.5)` | Versi transparan untuk efek *Glassmorphism*. |

---

## 📐 2. Sudut & Bentuk (The "Focus" Look)
Kekuatan utama Focus UI ada pada lengkungan sudutnya yang sangat konsisten dan membulat.

| Nama Variabel | Nilai Default | Kegunaan |
| :--- | :--- | :--- |
| `--radius-base` | `20px` | Lengkungan standar untuk elemen input/form. |
| `--radius-lg` | `30px` | Lengkungan khas Focus UI untuk kartu (Card). |
| `--radius-pill` | `100px` | Membuat bentuk kapsul sempurna pada tombol atau badge. |

---

## ☁️ 3. Bayangan & Jarak (Shadow & Spacing)
Mengatur kedalaman elemen agar terlihat melayang di atas latar belakang.

| Nama Variabel | Nilai Default | Kegunaan |
| :--- | :--- | :--- |
| `--shadow-soft` | `0 8px 30px rgba(149, 117, 205, 0.3)` | Bayangan lembut khas lavender untuk kartu. |
| `--space-sm` | `8px` | Jarak antar elemen kecil (gap). |
| `--space-md` | `16px` | Jarak standar antar elemen layout. |
| `--space-lg` | `24px` | Jarak lebar untuk padding di dalam kartu. |

---

## 🛠️ Cara Melakukan Kustomisasi (Theming)

Jika kamu ingin mengubah tema Focus UI menjadi warna lain (misalnya Hijau Matcha), kamu tidak perlu menghapus CSS asli. Cukup tambahkan kode berikut di file CSS pribadimu atau di dalam tag `<style>` di bawah pemanggilan `style.css`:

```css
/* Contoh mengubah tema ke Matcha Green secara instan */
:root {
    --primary: #81c784;
    --primary-dark: #66bb6a;
    --secondary: #c8e6c9;
    --text-color: #1b5e20;
    --bg-color: #f1f8e9;
    --shadow-soft: 0 8px 30px rgba(129, 199, 132, 0.3);
}
```

---

## ⚡ Catatan untuk Developer
Focus UI dirancang murni untuk **Gaya Visual**. Untuk interaksi yang lebih hidup, sangat disarankan menggunakan framework animasi seperti **GSAP** atau **Van.js** untuk menggerakkan elemen-elemen yang sudah diatur oleh variabel di atas.
