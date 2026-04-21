🚀 Material 3 Expressive + Monochrome Design System (Single Source)

<!--
INI SATU FILE DOANG.
Copy semua → jadi README.md atau docs/design-system.md di repo lo.

Fitur:
- Generate full theme dari 1 warna (HSL)
- Support expressive & monochrome
- CSS variables siap pakai
- Typography, spacing, motion, components included
-->---

🧠 Theme Generator (JS)

function generateTheme(accentH, type="expressive", accentS=80, accentL=50){
  const clamp = (v,min,max)=>Math.min(Math.max(v,min),max);
  const H = accentH;
  const S = type==="mono"?10:accentS;
  const L = accentL;

  return {
    primary: `hsl(${H}, ${S}%, ${L}%)`,
    onPrimary: `hsl(${H}, ${S}%, ${clamp(L<50?100-L:10,0,100)}%)`,
    primaryContainer: `hsl(${H}, ${S}%, ${clamp(L+40,0,100)}%)`,
    onPrimaryContainer: `hsl(${H}, ${S}%, ${clamp(L-10,0,100)}%)`,

    secondary: `hsl(${(H + (type==="mono"?0:30)) % 360}, ${clamp(S-(type==="mono"?0:20),0,100)}%, ${clamp(L-10,0,100)}%)`,
    onSecondary: `hsl(${(H + (type==="mono"?0:30)) % 360}, ${clamp(S-(type==="mono"?0:20),0,100)}%, ${clamp(L<50?100-L:10,0,100)}%)`,
    secondaryContainer: `hsl(${(H + (type==="mono"?0:30)) % 360}, ${clamp(S-(type==="mono"?0:20),0,100)}%, ${clamp(L+30,0,100)}%)`,
    onSecondaryContainer: `hsl(${(H + (type==="mono"?0:30)) % 360}, ${clamp(S-(type==="mono"?0:20),0,100)}%, ${clamp(L-10,0,100)}%)`,

    tertiary: `hsl(${(H + (type==="mono"?0:60)) % 360}, ${clamp(S-(type==="mono"?0:30),0,100)}%, ${clamp(L-20,0,100)}%)`,
    onTertiary: `hsl(${(H + (type==="mono"?0:60)) % 360}, ${clamp(S-(type==="mono"?0:30),0,100)}%, ${clamp(L<50?100-L:10,0,100)}%)`,

    error: `hsl(0, 75%, 50%)`,
    onError: `#FFFFFF`,

    neutral: `hsl(${H}, 10%, 95%)`,
    onNeutral: `hsl(${H}, 10%, 10%)`,
    neutralVariant: `hsl(${H}, 10%, 80%)`,
    onNeutralVariant: `hsl(${H}, 10%, 20%)`
  };
}

// contoh
const theme = generateTheme(240, "expressive");
console.log(theme);

---

🎨 CSS Variables (Auto Apply)

:root {
  --primary: hsl(240, 80%, 50%);
  --on-primary: hsl(240, 80%, 50%);
  --primary-container: hsl(240, 80%, 90%);
  --on-primary-container: hsl(240, 80%, 40%);

  --secondary: hsl(270, 60%, 40%);
  --on-secondary: hsl(270, 60%, 50%);
  --secondary-container: hsl(270, 60%, 70%);
  --on-secondary-container: hsl(270, 60%, 40%);

  --tertiary: hsl(300, 50%, 30%);
  --on-tertiary: hsl(300, 50%, 70%);

  --error: hsl(0, 75%, 50%);
  --on-error: #FFFFFF;

  --neutral: hsl(240, 10%, 95%);
  --on-neutral: hsl(240, 10%, 10%);
  --neutral-variant: hsl(240, 10%, 80%);
  --on-neutral-variant: hsl(240, 10%, 20%);
}

---

🔠 Typography

:root {
  --font-display-large: 57px;
  --font-headline-medium: 28px;
  --font-title-medium: 16px;
  --font-body-large: 16px;
  --font-label-small: 11px;

  --font-weight-bold: 700;
  --font-weight-medium: 500;
  --font-weight-regular: 400;
}

---

📐 Spacing & Layout

:root {
  --spacing-base: 8px;
  --padding-standard: 16px;

  --radius-small: 8px;
  --radius-medium: 16px;
  --radius-large: 24px;
}

---

🎞️ Motion

:root {
  --motion-fast: 100ms;
  --motion-medium: 250ms;
  --motion-slow: 400ms;

  --motion-ease: ease-in-out;
  --motion-emphasized: cubic-bezier(0.2,0,0,1);
}

---

🧩 Components

/* Button */
.btn-filled {
  background: var(--primary);
  color: var(--on-primary);
  border-radius: 20px;
  padding: 12px 24px;
  transition: transform var(--motion-fast);
}
.btn-filled:active {
  transform: scale(0.95);
}

/* Card */
.card {
  background: var(--neutral);
  border-radius: var(--radius-medium);
  padding: var(--padding-standard);
  box-shadow: 0 2px 6px rgba(0,0,0,0.1);
}

/* Input */
.input {
  height: 56px;
  border-radius: 12px;
  border: 1px solid var(--neutral-variant);
  padding: 0 16px;
}

/* Navbar */
.navbar {
  height: 80px;
  background: var(--neutral);
}
.navbar .active { color: var(--primary); }
.navbar .inactive { color: var(--neutral-variant); }

---

⚠️ Rules (Biar AI Lo Gak Ngaco)

- Jangan nambah warna manual → semua dari generator
- Jangan animasi lebay → ikutin motion token
- Jangan ubah spacing system → pakai 8px base
- Prioritas: jelas > keren

---

🧾 Cara Pakai

1. Tentuin 1 warna (Hue)
2. Generate pakai "generateTheme()"
3. Inject ke CSS variables
4. Selesai

---

💥 Intinya

Lo gak perlu design lagi.
Cukup:

- kirim file ini
- AI lo jalan

Kalau masih jelek?
Berarti AI lo bego… bukan sistemnya 😌
