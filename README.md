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

## 📐 4. Flexbox Utilities (Layout Mobile-First)

Focus UI telah meninggalkan sistem Grid kuno dan beralih menggunakan **Flexbox Utility Classes**. Pendekatan ini membuat pengembangan *Mobile Web App* menjadi jauh lebih cepat, lincah, dan tidak membebani performa browser.

Cukup tambahkan kelas-kelas ini langsung ke dalam tag HTML (atau komponen Van.js) kamu untuk menata tata letak dalam hitungan detik.

### 🧱 Base & Direction (Dasar Flexbox)
| Kelas | Kegunaan (CSS Setara) |
| :--- | :--- |
| `.flex` | Mengaktifkan mode flexbox (`display: flex;`). Wajib dipakai! |
| `.flex-col` | Menyusun elemen berderet ke bawah / vertikal (`flex-direction: column;`). |
| `.flex-row` | Menyusun elemen berderet ke samping / horizontal (`flex-direction: row;`). |
| `.flex-wrap` | Membuat elemen turun ke baris baru jika tidak muat (`flex-wrap: wrap;`). |

### 📏 Sizing (Ukuran Otomatis)
| Kelas | Kegunaan |
| :--- | :--- |
| `.flex-1` | Memaksa elemen untuk membagi sisa ruang secara adil dan rata. |
| `.flex-auto` | Elemen menyesuaikan ukurannya sendiri secara dinamis. |
| `.flex-none` | Mengunci ukuran elemen agar tidak bisa membesar/mengecil. |
| `.w-full` | Lebar penuh 100%. |
| `.h-full` | Tinggi penuh 100%. |

### 🧲 Justify (Perataan Utama)
Mengatur posisi elemen di sepanjang sumbu utama (Horizontal jika `flex-row`, Vertikal jika `flex-col`).

| Kelas | Kegunaan |
| :--- | :--- |
| `.justify-start` | Merapatkan elemen ke awal (Kiri/Atas). |
| `.justify-end` | Merapatkan elemen ke akhir (Kanan/Bawah). |
| `.justify-center` | Memposisikan elemen pas di tengah. |
| `.justify-between` | Mendorong elemen ke ujung, menyisakan jarak kosong di tengah. |
| `.justify-around` | Memberikan jarak kosong yang sama rata di sekeliling elemen. |

### 🎯 Align (Perataan Berpotongan)
Mengatur posisi elemen di sumbu silang (Atas-bawah jika `flex-row`, Kiri-kanan jika `flex-col`).

| Kelas | Kegunaan |
| :--- | :--- |
| `.align-start` | Menempel di sisi atas/kiri. |
| `.align-end` | Menempel di sisi bawah/kanan. |
| `.align-center` | Berada tepat di tengah (vertikal/horizontal). |
| `.align-stretch` | Memaksa elemen ditarik penuh memenuhi wadah. |

### 🌌 Spacing & Gaps (Jarak & Ruang Napas)
Utility untuk memberikan jarak antar elemen tanpa menggunakan CSS kustom. Gunakan ukuran `sm` (8px), `md` (16px), atau `lg` (24px).

| Tipe | Contoh Kelas | Kegunaan |
| :--- | :--- | :--- |
| **Gap** | `.gap-sm`, `.gap-md`, `.gap-lg` | Memberi jarak *hanya di antara* elemen-elemen flex. (Sangat direkomendasikan!) |
| **Padding** | `.p-sm`, `.p-md` | Ruang kosong di bagian *dalam* elemen. |
| **Margin Top** | `.mt-sm`, `.mt-md` | Jarak dorong ke arah *atas*. |
| **Margin Bottom** | `.mb-sm`, `.mb-md` | Jarak dorong ke arah *bawah*. |

---

## 🪟 5. Efek Kaca (Glassmorphism)

Focus UI dilengkapi dengan kelas utilitas khusus untuk menciptakan efek kaca melayang yang elegan dan kekinian.

| Kelas | Kegunaan |
| :--- | :--- |
| `.ff-glass` | Memberikan latar belakang transparan ringan dengan efek *blur* sebesar 20px dan garis tepi (*border*) putih tipis. Sangat cocok untuk panel menu atau *overlay*. |

```html
<div class="ff-glass p-md border-radius-lg">
    <p>Teks ini berada di atas panel kaca melayang.</p>
</div>
```

---

## 🧩 6. Komponen UI (Statis & Bebas Animasi)

Semua komponen Focus UI didesain murni **statis** (tanpa animasi transisi bawaan CSS). Ini sengaja dilakukan agar kamu bisa bebas menyuntikkan animasi tingkat lanjut menggunakan JavaScript (seperti **GSAP** atau **Van.js**) tanpa mengalami bentrok atau *lag* di perangkat *mobile*.

### 🔘 Tombol (Buttons)
Bentuknya membulat, solid, dan memiliki perubahan warna yang instan saat disentuh/diklik.

| Kelas | Kegunaan |
| :--- | :--- |
| `.btn` | Kelas dasar wajib untuk semua tombol. Berwarna lavender lembut (*secondary*). |
| `.btn-primary` | Warna ungu pekat (*primary*) dengan bayangan melayang yang kuat. |
| `.btn-pill` | Membuat tombol berbentuk kapsul/pil (lengkungan 100px). |
| `.btn-icon` | Membuat tombol berbentuk bulat sempurna (45x45px) khusus untuk 1 ikon. |

```html
<div class="flex gap-sm">
    <button class="btn btn-primary btn-pill">Simpan</button>
    <button class="btn btn-icon">X</button>
</div>
```

### 📝 Input Form (Form Control)
Input teks yang membesar secara otomatis dan berubah warna batasnya (*border*) saat sedang diketik.

| Kelas | Kegunaan |
| :--- | :--- |
| `.form-control` | Kelas dasar untuk elemen `<input>` atau `<textarea>`. Melengkung lembut dengan jarak *padding* yang ramah sentuhan jari. |

```html
<input type="text" class="form-control" placeholder="Tulis tugasmu hari ini...">
```

### 🃏 Kartu (Cards)
Wadah utama untuk menampilkan konten di Focus UI.

| Kelas | Kegunaan |
| :--- | :--- |
| `.card` | Kotak putih bersih dengan lengkungan tajam 30px dan efek bayangan ungu melayang (`shadow-soft`). |

### 🧭 Navigasi (Navbar)
Bilah menu yang menempel di bagian atas layar agar selalu bisa diakses.

| Kelas | Kegunaan |
| :--- | :--- |
| `.navbar` | Bilah navigasi transparan (*glassmorphism*) yang secara otomatis memosisikan dirinya diam (`sticky`) di bagian paling atas layar dan memiliki `z-index` tinggi agar tidak tertutup elemen lain. |

```html
<nav class="navbar">
    <h3>Focus App</h3>
    <button class="btn btn-icon">⚙️</button>
</nav>
```

### 🚨 Modals (Kotak Dialog)
Sistem *modal* yang muncul di tengah layar dengan latar belakang gelap. Didesain untuk diatur penampilannya lewat JavaScript (menggunakan manipulasi kelas `.show`).

| Kelas | Kegunaan |
| :--- | :--- |
| `.modal-overlay` | Latar belakang hitam transparan yang menutupi seluruh layar. Default-nya disembunyikan (`display: none`). |
| `.modal-overlay.show` | Tambahkan kelas `.show` via JavaScript untuk memunculkan modalnya. |
| `.modal-content` | Kotak kartunya yang berada tepat di tengah layar. |

```html
<div class="modal-overlay" id="myModal">
    <div class="modal-content flex flex-col gap-md align-center">
        <h3>Peringatan!</h3>
        <p>Apakah kamu yakin ingin menghapus data ini?</p>
        <button class="btn btn-primary w-full">Tutup</button>
    </div>
</div>
```

### 💡 Contoh Penggunaan Super Cepat

Daripada membuat file CSS baru, kamu bisa membangun komponen yang rapi seperti ini hanya dengan utility:

```html
<div class="container flex flex-col justify-center align-center h-full">
            <div
                class="card flex flex-col gap-md"
                style="width: 100%; max-width: 400px; margin-top: 50px"
            >
                <div class="flex flex-row justify-between align-center">
                    <h3 class="flex-1">Task Manager</h3>
                    <button class="btn btn-primary btn-pill">Tambah</button>
                </div>

                <p class="mt-sm">Fokus selesaikan satu per satu, ya!</p>
            </div>
        </div>
```


