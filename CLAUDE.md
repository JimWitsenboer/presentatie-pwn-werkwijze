# Instructies — NAVARA Presentatie

> Bestand: `presentatie-werkwijze.html` · 17 slides · NAVARA-huisstijl · PWN

---

## Bestandenoverzicht

| Bestand | Rol |
|---|---|
| `presentatie-werkwijze.html` | De presentatie — één self-contained HTML-bestand |
| `NAVARA_HOUSE_STYLE.md` | Volledige huisstijlgids (kleuren, fonts, tokens) |
| `NAVARA_TEMPLATE_SLIDES.md` | Keynote template slide overzicht |
| `images/navara.svg` | NAVARA-logo — wit (voor dark/blue slides) |
| `images/navara-dark.svg` | NAVARA-logo — navy `#000b3b` (voor light slides) |
| `images/pwn.svg` | PWN-logo — rechtsboven op elke slide |
| `images/DX-drivers.png` | DX drivers top 25 — gebruikt op slide 6 |
| `images/DX-snapshot.png` | DX snapshot — gebruikt op slide 7 |
| `images/release-notes.png` | Release notes — slide 11 |
| `images/teams-bericht.png` | Teams bericht — slide 11 |
| `images/Maak_van_deze_afbeelding_een_f.mp4` | Video slide 15 |
| `images/tot-ziens.mp4` | Video slide 17 |

---

## Kleurenpalet

```
Blue:   #3665ff    ████████  (primair, actiekleur)
Navy:   #000b3b    ████████  (donkere basis)
Black:  #0b1433    ████████  (tekst op light)
White:  #ffffff    ████████  (tekst op dark)
L-Blue: #ebf0ff    ████████  (light-blue achtergrond)
```

---

## Slide-varianten

| Klasse | Achtergrond | Tekst | Gebruik |
|---|---|---|---|
| `.slide--dark` | `#000b3b` | wit | Cover, dividers, afsluiting |
| `.slide--blue` | `#3665ff` | wit | Quote, cultuur |
| `.slide--light` | `#ffffff` | `#0b1433` | Standaard content |
| `.slide--light-blue` | `#ebf0ff` | `#0b1433` | Subtiele variatie |

---

## Een slide toevoegen

Minimale structuur:

```html
<section class="slide slide--light" id="slide-X">
  <img class="slide__logo" src="images/navara-dark.svg" alt="NAVARA">
  <img class="slide__partner" src="images/pwn.svg" alt="PWN">
  <div class="slide__page">X / 17</div>
  <div class="water-wave"></div>
  <div class="water-droplet-left">💧</div>
  <div class="slide-inner">
    <!-- content hier -->
  </div>
</section>
```

Let op per variant:
- **Light/light-blue slides**: `navara-dark.svg` als logo
- **Dark/blue slides**: `navara.svg` als logo
- **Droplet**: wissel `-left` en `-right` af per slide

Daarna:
1. Update alle slide `id=""` en paginanummers vanaf de nieuwe slide
2. Update `const totalSlides = X;` in het JavaScript-blok onderaan
3. Check `grep 'id="slide-' presentatie-werkwijze.html` op duplicaten

---

## Herbruikbare elementen

### Water-decoraties (op elke slide)
```html
<div class="water-wave"></div>
<div class="water-droplet-left">💧</div>  <!-- of -right -->
```

### Jumping fish (alleen slide 1)
```html
<div class="jumping-fish">🐟</div>
<div class="splash-effect">💦</div>
```

### Video smaller (slide 15)
```html
<video class="slide-video" autoplay loop muted playsinline>
  <source src="images/bestand.mp4" type="video/mp4">
</video>
```

### Video full-screen (slide 17)
```html
<video class="slide-video-full" autoplay loop muted playsinline>
  <source src="images/bestand.mp4" type="video/mp4">
</video>
```

### Afbeelding met schaduw
```html
<img src="images/bestand.png" alt="" style="max-width:100%; max-height:55vh; height:auto; border-radius:var(--radius-lg); box-shadow:0 4px 24px rgba(0,0,0,0.1); object-fit:contain;">
```

### Twee-koloms layout
```html
<div style="display:grid; grid-template-columns:1fr 1fr; gap:var(--spacing-xl); align-items:center; margin-top:var(--spacing-lg);">
  <div>links</div>
  <div>rechts</div>
</div>
```

---

## Belangrijke regels

1. **Geen em-dashes (`—`)** — gebruik komma's of dubbele punten
2. **`height: 100dvh` + `overflow: hidden`** — slides mogen niet scrollen, alles moet in het scherm passen
3. **`max-height` op afbeeldingen** — `55vh` voor losse images, `65vh` voor side-by-side, anders past het niet
4. **Font: Inter** — via Google Fonts, géén Mirador of Be Vietnam Pro in de HTML
5. **Titels consequent** — alle slides gebruiken `<h2>` als titel, behalve slide 1 (`<h1>`) en slide 3 (`.quote-slide__text`)
6. **Geen losse tekstwijzigingen op slides** — contentwijzigingen alleen via de gebruiker
7. **Pagina-nummers altijd bijwerken** — bij toevoegen/verwijderen van slides
8. **Logo's per slide-variant** — wit logo op donker, navy logo op licht

---

## Navigatie

- **Pijltjestoetsen, Page Up/Down** — vorige/volgende slide
- **Home/End** — eerste/laatste slide
- **Swipe/scroll** — native scroll-snap
- **Dots rechts** — klik op stip om direct te navigeren

---

## Typografie (CSS custom properties)

```css
--text-h1:    clamp(3.2rem, 6vw, 6.5rem)   /* Slide 1 cover */
--text-h2:    clamp(2.2rem, 4vw, 3.8rem)   /* Alle slide-titels */
--text-h3:    clamp(1.6rem, 3vw, 2.4rem)   /* Subtitels */
--text-body:  clamp(1.15rem, 1.7vw, 1.4rem) /* Lopende tekst */
--text-small: clamp(0.95rem, 1.2vw, 1.1rem) /* Bijschriften */
```

Font-weight: **300** (body), **600** (koppen), **700** (h1), **900** (cover)
