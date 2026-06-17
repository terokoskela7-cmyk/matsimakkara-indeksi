# Matsimakkara-indeksi — Design System

## Filosofia
Stadionmakkaraindeksi on **premium-ruokasovellus** eikä pelkkä lista. Visuaalinen kieli viestii lämpöä, laatua ja suomalaista jalkapallokulttuuria. Dark UI luo elokuvamaisen tunnelman — kuin katsoisi stadionvalojen loistetta illan ottelussa.

## Värit
| Nimi | Hex | Käyttö |
|------|-----|--------|
| Warm Gold | `#c9a84c` | Primary accent, tähdet, korostukset, CTA |
| Gold Light | `#e8c87a` | Hover states, star hover |
| Deep Burgundy | `#8B3A3A` | Secondary accent, harvoin |
| Near Black | `#0f0f0f` | Tausta |
| Dark Surface | `#1a1a1a` | Kortit, alapalkit |
| Elevated Surface | `#242424` | Hover, modaalit |
| Warm White | `#f5f0e6` | Pääteksti |
| Muted Warm | `#a09a8e` | Toissijainen teksti |
| Success | `#6b9e6b` | Hyvä arvosana (≥4) |
| Warning | `#c9a84c` | OK arvosana (3–4) |
| Error | `#b55a5a` | Huono arvosana (<3) |

## Typography
- **Otsikot**: `Bebas Neue` — stadionmainostaulujen henkinen, kapea, iso, vaikuttava
- **Alaotsikot / UI**: `Space Grotesk` — moderni, hieman teollinen, selkeä
- **Body**: `Inter` — luettavuus, skaalautuvuus

## Komponentit

### Hero
- Isolla: MATSIMÄKKÄRÄINDEKSI (Bebas Neue, 3.5rem+)
- Alateksti: "Suomen stadionmakkaroiden kattavin arvostelualusta."
- 3 stat-laatikkoa: stadionien määrä, arvostelujen määrä, ykkönen
- Gradient-tausta: gold → transparent (subtle)

### Card
- Tumma pinta (`#1a1a1a`), pyöristetyt reunat (16px)
- Hover: lift 6px + gold-glow shadow + top gradient line
- Animaatio: staggered entrance (IntersectionObserver/animation-delay)
- Badge: 🥇🥈🥉 pop-in animaatio

### Drawer (Slide-in Panel)
- Korvaa modaalin: työntyy oikealta
- Max-width: 680px, full-height
- Overlay: blur + dark
- Tabit: border-bottom indicator
- Sisältö: fade-in animaatio

### Map Markers
- Pyöreät, värikoodatut (green/yellow/red)
- Sisällä arvosana (Bebas Neue)
- Hover: scale(1.15)
- Popup: dark themed, linkki draweriin

### Stars
- Interaktiivinen: hover preview + click lock
- Väri: gold (#c9a84c) filled, dark (#333) empty
- Koko: 1.5rem

## Animaatiot
- **Card enter**: opacity 0→1, translateY 20→0, 0.5s cubic-bezier(0.4,0,0.2,1), staggered delay
- **Drawer**: translateX 100%→0, 0.35s cubic-bezier(0.4,0,0.2,1)
- **Overlay**: opacity 0→1, 0.2s
- **Rank badge**: scale(0)→scale(1), bounce easing
- **Bar fill**: width animate, 0.6s ease
- **Marker hover**: scale(1.15), 0.3s

## Responsive
- Mobile: single column, drawer full-width, search narrower, hero h1 2.5rem
- Tablet: 2 columns
- Desktop: 3+ columns, max 1300px container

## Assets
- Logo: Font Awesome hotdog icon + text
- No external images (all user-generated)
- Icons: Font Awesome 6
- Map: Leaflet + CartoDB Dark Matter tiles

## Interaction Patterns
- Click card → open drawer
- Search filters in real-time
- Star rating: hover preview, click to confirm
- Upload: drag not supported, file picker + canvas resize
- Share: clipboard API, fallback alert
- User auth: localStorage only, no security
