# Matsimakkara-indeksi 2.0 — Laajennus & Redesign

## Tavoite
Uudistetaan Matsimakkara-indeksi: 6 uutta toiminnallisuutta + visuaalinen redesign.

## Vaiheet

### Phase 1 — Toiminnallisuudet (päivitä index.html)
1. **Lisää stadioneita**: 15 uutta (Mikkeli, Hämeenlinna, Kuopio, Seinäjoki, Jyväskylä, Kemi, Imatra, Kajaani, Kokkola, Mariehamn, Tornio, Salo, Kemiö, Riihimäki, Kerava)
2. **Haku**: Search bar yläpalkkiin, filtteröi stadionit reaaliajassa
3. **Kommentit**: Arvosteluihin voi lisätä kommentteja (nimi + teksti + aikaleima)
4. **Käyttäjätilit**: LocalStorage-pohjainen auth — kirjautuminen nimellä/sähköpostilla, avatar (emoji), oma profiili
5. **Jaa ranking**: "Kopioi linkki" -nappi joka generoi URL hashissa ranking-datan
6. **Ottelut**: Mock-otteludata Veikkausliiga 2025 + fetch-piste oikealle API:lle

### Phase 2 — Design (tee design.md)
Suunnitellaan uusi visuaalinen identiteetti:
- Warm food-stadium vibes
- Dark premium feel
- Animations & transitions
- Card redesign
- Hero section
- Color palette: deep burgundy, warm gold, charcoal, cream

### Phase 3 — Rakenna uusi frontend
Rakenna koko appi uudelleen design.md:n mukaan. Single-file HTML.

## Tekniset rajaukset
- Client-side only (localStorage)
- Ei backendia, ei oikeaa authia
- Mock-ottelut (Veikkausliiga 2025), fetch-piste valmiina
- Yksittäinen index.html

## Data-muutokset
- Stadiums: 25 kpl
- Reviews: {stadiumId, criteria[5], overall, comment, author, timestamp, comments[]}
- Users: {id, name, email, avatar, createdAt}
- Matches: {stadiumId, home, away, date, league, source}
- Images: {stadiumId, dataUrl, author, caption, id}
- Share: URL-encoded ranking snapshot

## Värisuunnittelu (Phase 2)
- Primary: #c9a84c (warm gold)
- Secondary: #8B3A3A (deep burgundy/stadium red)
- Background: #0f0f0f (near black)
- Surface: #1a1a1a (dark card)
- Surface-elevated: #242424
- Text-primary: #f5f0e6 (warm white)
- Text-secondary: #a09a8e (muted warm)
- Success: #6b9e6b (muted green)
- Warning: #c9a84c (gold)
- Error: #b55a5a (muted red)

## Fontit
- Headings: 'Space Grotesk' (bold, modern, slightly industrial)
- Body: 'Inter' (clean, readable)
- Stadium names: 'Bebas Neue' (stadium marquee feel)

## Komponentit
- Hero section: isolla "Matsimakkara-indeksi" + tausta-animaatio
- Floating search bar
- Masonry grid / dense card layout
- Stadium detail drawer (ei modaali, vaan slide-in)
- Map with animated markers
- Leaderboard strip
- User profile badge
- Match ticker

## Animaatiot
- Staggered card entrance (IntersectionObserver)
- Score counter animation (animate from 0 to value)
- Map marker pulse
- Hover lift + glow
- Drawer slide-in from right
- Page transition fade
