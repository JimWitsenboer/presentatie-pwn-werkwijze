# NAVARA — House Style

> Samengesteld uit de [navara.nl](https://navara.nl) website CSS en het Keynote-thema `NAVARA Style 1.4.kth`.
> Laatste update: 2026-06-30

---

## 1. Merkidentiteit

| Element | Waarde |
|---|---|
| **Tagline** | "Engineering business performance" — Data, Software & AI |
| **Motto** | "For the win." |
| **Logo** | Woordmerk — beschikbaar in **navy** (`#000b3b`) en **white** (`#ffffff`) |
| **Logobestanden** | `nav_logo_navy_rgb.pdf`, `nav_logo_white_rgb.pdf` |

---

## 2. Kleurenpalet

### 2.1 Primaire kleuren

| Naam | Hex | RGB | CSS Variable |
|---|---|---|---|
| **Blue** (primair) | `#3665ff` | `54, 101, 255` | `--color-blue` |
| **Navy** (donker) | `#000b3b` | `0, 11, 59` | `--color-navy` |
| **Black** (tekst) | `#0b1433` | `11, 20, 51` | `--color-black` |
| **White** | `#ffffff` | `255, 255, 255` | `--color-white` |

### 2.2 Blue ramp (actie, highlights, lichte vlakken)

| Tint | Hex | CSS Variable | Gebruik |
|---|---|---|---|
| Full | `#3665ff` | `--color-blue` | Buttons, links, primaire accenten |
| 400 | `#5e84ff` | `--color-blue-400` | |
| 300 | `#86a3ff` | `--color-blue-300` | |
| 200 | `#afc1ff` | `--color-blue-200` | |
| 100 | `#d7e0ff` | `--color-blue-100` | Lichte accentvlakken |
| 50 | `#ebf0ff` | `--color-blue-50` | Zeer lichte accenten (Keynote: "Light Blue") |
| 25 | `#f6f8ff` | `--color-blue-25` | Bijna witte tint |

### 2.3 Navy ramp (donkere vlakken, footers)

| Tint | Hex | CSS Variable | Gebruik |
|---|---|---|---|
| Full | `#000b3b` | `--color-navy` | Dark sections, footer, Keynote "Dark" slides |
| 400 | `#333c62` | `--color-navy-400` | |
| 300 | `#666d89` | `--color-navy-300` | |
| 200 | `#999db1` | `--color-navy-200` | |
| 100 | `#ccced8` | `--color-navy-100` | |
| 50 | `#e6e7eb` | `--color-navy-50` | |
| 25 | `#f5f6f6` | `--color-navy-25` | |

### 2.4 Aanvullende kleuren

| Naam | Waarde | Gebruik |
|---|---|---|
| Mark highlight | `#ff0` (yellow) | Tekst-markering |
| Tag overlay | `rgba(0, 11, 59, 0.302)` | Tags, cards overlay |
| Gradient overlay | `rgba(49, 52, 65, 0.6)` → `rgba(49, 52, 65, 0)` | Gradients |
| Hover state | `hsla(0, 0%, 100%, 0.8)` | Lichte hover |
| Placeholder | `hsla(180, 5%, 96%, 0.5)` | Input placeholder |

---

## 3. Typografie

### 3.1 Lettertypen

| Font | Gebruik | Formaat | Gewichten |
|---|---|---|---|
| **Mirador** | Koppen (h1–h4), quotes, bold display | `.woff2` / `.woff` | Regular (400), Semibold (600) |
| **Be Vietnam Pro** | Broodtekst, body, knoppen, navigatie | Google Fonts / system | Light (300), Regular (400), Medium (500), Semibold (600), Bold (700), Black (900) |
| **Monospace** | Code, pre, kbd, samp | System | Regular (400) |

### 3.2 Kopgroottes (fluid: schaalt tussen 375px en 1440px viewport)

| Element | Min (375px) | Max (1440px) | Gewicht | Letter-spacing | Line-height |
|---|---|---|---|---|---|
| h1 / `.h1` | 56px | 90px | 600 (Semibold) | `-0.01em` | `1.1` → `1.05` |
| h2 / `.h2` | 42px | 64px | 600 | `-0.01em` | `1.2` → `1.05` |
| h3 / `.h3` | 32px | 48px | 600 | `-0.01em` | `1.3` → `1.1` |
| h4 / `.h4` | 22px | 28px | 600 | `-0.01em` | `1.2` |
| `.text-quote` | 24px | 36px | 400 (Mirador) | `-0.01em` | `1.4` |

### 3.3 Body & overige tekst

| Element | Min (375px) | Max (1440px) | Gewicht | Letter-spacing | Line-height |
|---|---|---|---|---|---|
| Body / p / div | 18px | 20px | 300 (Light) | `-0.025em` → `-0.03em` | `1.55` → `1.4` |
| `.text-bold` | 22px | 30px | 600 | `normal` | `1.2` |
| `.text-small` | 16px | 18px | 300 | — | `1.5` |
| `.text-link` | 1.8rem (fixed) | — | 600 | `-0.01em` | `1.2` |
| `.c-tag` | 14px | 16px | 400 | `-0.015em` | `1.2` |
| Footer copyright | 1.8rem | 2rem | 400 | — | — |
| Footer menu links | 2rem | 2.4rem | — | — | — |

### 3.4 Font-weight utility classes

`.font-thin` (100) · `.font-light` (300) · `.font-regular` (400) · `.font-medium` (500) · `.font-semibold` (600) · `.font-bold` (700) · `.font-black` (900)

---

## 4. Keynote Thema — Template Slides (24 stuks)

Het thema `NAVARA Style 1.4.kth` bevat 24 template slides in drie kleurvarianten:

### 4.1 Overzicht slides

| # | Naam | Variant | Beschrijving |
|---|---|---|---|
| 1 | Titel | — | Cover/titel slide |
| 2 | Ondertitel presentatie | — | Subtitel slide |
| 3 | Agenda | — | Agenda/overzicht |
| 4 | Leeg | — | Lege slide |
| 5 | Leeg met logo | — | Leeg met Navara logo |
| 6 | Hoofdstuk | **Dark** | Sectie-divider |
| 7 | Hoofdstuk & toelichting | **Dark** | Sectie-divider met toelichting |
| 8 | Bulletpoints | **Light** | Opsomming, lichte achtergrond |
| 9 | Bulletpoints | **Light Blue** | Opsomming, lichtblauwe achtergrond |
| 10 | Bulletpoints | **Dark** | Opsomming, donkere achtergrond |
| 11 | Bulletpoints & foto | **Light** | Opsomming met foto |
| 12 | Bulletpoints & foto | **Dark** | Opsomming met foto, donker |
| 13 | Titel & tekst | **Light** | Titel met tekstblok |
| 14 | Titel & tekst | **Light Blue** | Titel met tekstblok, lichtblauw |
| 15 | Titel & tekst | **Dark** | Titel met tekstblok, donker |
| 16 | Titel & bulletpoints | **Light** | Titel met opsomming |
| 17 | Bulletpoints & quotes | **Light** | Opsomming met quotes |
| 18 | Quote | **Blue** | Quote, blauwe achtergrond |
| 19 | Quote | **Dark** | Quote, donkere achtergrond |
| 20 | Functietitel | **Light** | Team/functiepresentatie |
| 21 | Functietitel | **Light Blue** | Team/functiepresentatie |
| 22 | Functietitel | **Blue** | Team/functiepresentatie |

### 4.2 Kleurvarianten

| Variant | Achtergrond | Tekstkleur | Gebruik |
|---|---|---|---|
| **Light** | `#ffffff` | `#0b1433` | Standaard slides |
| **Light Blue** | `#ebf0ff` (blue-50) | `#0b1433` | Subtiele accent-slides |
| **Blue** | `#3665ff` | `#ffffff` | Impact-slides, quotes |
| **Dark** | `#000b3b` (navy) | `#ffffff` | Sectie-dividers, impact-slides |

### 4.3 Keynote specifieke eigenschappen

| Eigenschap | Waarde |
|---|---|
| **Standaard lettertype** | HelveticaNeue (Keynote-beperking; in web: Be Vietnam Pro + Mirador) |
| **Logo's** | Navy RGB (`#000b3b`) en White RGB — embedded als PDF |
| **Beeldmateriaal** | Kantoorfoto's (PandNavara), motion backgrounds, abstracte vormen |
| **Schaduw** | Formal Shadow op elementen |
| **Gradients** | Diffuse en lineaire gradient fills beschikbaar |
| **Data lettertype** | HelveticaNeue (voor charts/tabellen) |

---

## 5. Web — Design Tokens

### 5.1 Knoppen

| Eigenschap | Waarde |
|---|---|
| **Border-radius** | `8px` |
| **Primaire knop** | `__primary` — solid blue (`#3665ff`) op wit |
| **Secundaire knop** | `__secondary` — varianten met blue/white/grey + SVG pijlen |
| **Letter-spacing** | `-0.015em` |
| **Line-height** | `0.7` |

### 5.2 Tags & labels

| Eigenschap | Waarde |
|---|---|
| **Border-radius** | `100px` / `30px` / `20px` |
| **Achtergrond** | `rgba(0, 11, 59, 0.302)` overlay |
| **Tekstgrootte** | 14px → 16px |
| **Letter-spacing** | `-0.015em` |

### 5.3 Formulieren

| Eigenschap | Waarde |
|---|---|
| **Input border-radius** | `8px` |
| **Placeholder** | `hsla(180, 5%, 96%, 0.5)` |
| **Fieldset border** | `silver` |

### 5.4 Navigatie

| Eigenschap | Waarde |
|---|---|
| **Header padding** | 14px (mobile) / 20px (desktop); affixed 10px |
| **Sub-menu border-radius** | `6px` |
| **Hamburger lijnen** | `2px` border-radius |
| **Z-index header** | `88` |
| **Z-index background** | `-1` |

### 5.5 Layout & spacing

| Eigenschap | Waarde |
|---|---|
| **Wrapper max-widths** | `1368px`, `1440px`, `934px`/`1006px`, `1142px`/`1214px`, `1210px`/`1282px`, `1968px`/`2040px` |
| **Grid gaps** | `16px`, `24px`, `32px`, `40px`, `48px`, `56px`, `60px`, `64px`, `70px`, `114px`, `155px` |
| **Section padding** | `100px` (mobile) / `140px` (desktop) |
| **Box shadow** | `rgba(0, 0, 0, 0.2)` |

### 5.6 Transities & animatie

| Eigenschap | Waarde |
|---|---|
| **Standaard** | `0.3s ease` |
| **Snel** | `0.35s` |
| **Langzaam** | `0.8s ease`, `1s ease` |
| **Parallax/scroll** | `1.5s cubic-bezier(0.07, 0.6, 0, 1.04)` |

---

## 6. Samenvatting — Snel Refereren

### Kleuren

```
Blue:   #3665ff    ████████
Navy:   #000b3b    ████████
Black:  #0b1433    ████████
White:  #ffffff    ████████
```

### Lettertypen

```
Koppen:    Mirador (serif)      — Semibold 600
Broodtekst: Be Vietnam Pro       — Light 300
Code:      Monospace (system)    — Regular 400
Keynote:   HelveticaNeue         — (fallback)
```

### Kernregels

1. **Blauw** (`#3665ff`) is de primaire actiekleur — buttons, links, impact
2. **Navy** (`#000b3b`) is de donkere basis — footers, dark mode, dividers
3. **Mirador** (serif) alléén voor koppen en quotes, nooit voor broodtekst
4. **Be Vietnam Pro** voor alle lopende tekst, navigatie, en UI-elementen
5. Fluid typografie: tekst schaalt mee tussen 375px en 1440px viewport
6. Drie presentatie-varianten: Light, Light Blue, Dark — met Blue voor impact
7. Border-radius consistent op `8px` voor interactieve elementen
