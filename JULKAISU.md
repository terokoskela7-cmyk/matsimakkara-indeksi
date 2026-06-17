# Matsimakkara-indeksi — Julkaisuopas

## Vaihtoehto A: GitHub Pages (helpoin, 2 min)

### 1. Luo GitHub-tili
https://github.com/join

### 2. Luo uusi repo
- Mene https://github.com/new
- Repo name: `matsimakkara-indeksi`
- Visibility: **Public**
- ✅ Add a README file (valinnainen)
- Paina **Create repository**

### 3. Lisää tiedosto
- Klikkaa **Add file → Upload files**
- Drag & drop `matsimakkara.html` tähän repo:hon
- Commit message: "Initial release"
- Paina **Commit changes**

### 4. Käynnistä GitHub Pages
- Mene **Settings → Pages** (sivupalkista)
- Source: **Deploy from a branch**
- Branch: **main / root**
- Paina **Save**
- Odota 1-2 minuuttia
- Sivusi on: `https://YOURNAME.github.io/matsimakkara-indeksi/matsimakkara.html`

### 5. Custom domain (valinnainen)
- Pages-asetuksissa: **Custom domain** → kirjoita `matsimakkara.fi`
- Lisää DNS: `CNAME` → `YOURNAME.github.io`

---

## Vaihtoehto B: Firebase Hosting (nopein, sync)

### 1. Asenna Firebase CLI
```bash
npm install -g firebase-tools
```

### 2. Kirjaudu
```bash
firebase login
```

### 3. Alusta projekti
```bash
cd /Users/terokoskela/Documents/kimi/workspace/matsimakkara-indeksi
firebase init hosting
```
- Valitse: **Create a new project**
- Projektin nimi: `matsimakkara-indeksi`
- Public directory: `.` (nykyinen hakemisto)
- Single-page app: **No**

### 4. Kopioi index.html Firebaseen
```bash
# Vaihda tiedoston nimi Firebase-ystävälliseksi
cp matsimakkara.html index.html
firebase deploy
```
- Sivusi on: `https://matsimakkara-indeksi.web.app`

### 5. Päivitä myöhemmin
```bash
firebase deploy
```

---

## Vaihtoehto C: Netlify Drop (helpoin, ei tiliä)

### 1. Avaa
https://app.netlify.com/drop

### 2. Drag & drop
- Vedä `matsimakkara-indeksi` **koko hakemisto** (ei vain tiedostoa) drop zoneen
- Saat URL:n heti: `https://random-name.netlify.app`

---

## Suositus

| Tavoite | Valitse |
|---------|---------|
| Nopein, ei tiliä | **Netlify Drop** |
| Pysyvä, custom domain | **GitHub Pages** |
| Päivitykset CLI:stä | **Firebase** |
| Ilmainen, luotettavin | **GitHub Pages** |

**Suosittelen GitHub Pagesia** — se on ilmainen, pysyvä, ja custom domain on helppo lisätä.

---

## Päivitykset

Kun teet muutoksia `matsimakkara.html`:

**GitHub Pages:**
```bash
cd matsimakkara-indeksi
git add matsimakkara.html
git commit -m "Update: new features"
git push
# Päivitys näkyy 1-2 minuutissa
```

**Firebase:**
```bash
cd matsimakkara-indeksi
firebase deploy
# Päivitys näkyy heti
```

---

## Tiedoston polku
`/Users/terokoskela/Documents/kimi/workspace/matsimakkara-indeksi/matsimakkara.html`
