# Matsimakkara-indeksi — GitHub Pages Julkaisu

## Miksi GitHub Pages?

| Ominaisuus | GitHub Pages |
|------------|-------------|
| Hinta | **Ilmainen** |
| Custom domain | Kyllä (esim. `matsimakkara.fi`) |
| HTTPS | Kyllä (automaattinen) |
| Päivitykset | `git push` → live 1-2 min |
| Luotettavuus | 99.9%+ (GitHubin infra) |
| CDN | Kyllä (Cloudflare) |

---

## Asennusohje (10 min)

### 1. Luo GitHub-tili
https://github.com/signup

### 2. Luo repo
- Mene https://github.com/new
- **Repository name:** `matsimakkara-indeksi`
- **Visibility:** Public
- ✅ **Add a README file**
- Paina **Create repository**

### 3. Lisää tiedosto
- Repo:ssa klikkaa **Add file → Upload files**
- Vedä `matsimakkara.html` upload-alueelle
- **Commit message:** `feat: initial release`
- Paina **Commit changes**

### 4. Käynnistä GitHub Pages
- Mene **Settings → Pages** (vasen sivupalkki)
- **Source:** Deploy from a branch
- **Branch:** `main` / `root`
- Paina **Save**
- Odota 1-2 minuuttia
- Sivusi on: `https://YOURNAME.github.io/matsimakkara-indeksi/matsimakkara.html`

### 5. Custom domain (valinnainen)
- Pages-asetuksissa: **Custom domain**
- Kirjoita: `matsimakkara.fi`
- DNS-palveluntarjoajassa lisää:
  - `CNAME` record: `matsimakkara.fi` → `YOURNAME.github.io`
- GitHub tarkistaa DNS automaattisesti
- HTTPS tulee automaattisesti (Cloudflare CDN)

---

## Päivitykset

Kun teet muutoksia `matsimakkara.html`:

### GitHub Web UI (helpoin)
1. Mene repo → klikkaa `matsimakkara.html`
2. Klikkaa **Edit** (kynä-ikoni)
3. Tee muutokset
4. **Commit message:** `fix: update layout`
5. Paina **Commit changes**
6. Päivitys näkyy 1-2 minuutissa

### Git CLI (jos asennettu)
```bash
cd /Users/terokoskela/Documents/kimi/workspace/matsimakkara-indeksi
git clone https://github.com/YOURNAME/matsimakkara-indeksi.git
cd matsimakkara-indeksi
cp ../matsimakkara.html .
git add matsimakkara.html
git commit -m "feat: new features"
git push origin main
```

---

## Tiedoston sijainti
`/Users/terokoskela/Documents/kimi/workspace/matsimakkara-indeksi/matsimakkara.html`

---

## Vinkit

- **Repo-nimi** = URL:n osa: `YOURNAME.github.io/matsimakkara-indeksi`
- Jos haluat **root-tason URL:n**: nimeä repo `YOURNAME.github.io`
- **index.html** = automaattinen etusivu. Nimeä `matsimakkara.html` → `index.html` jos haluat suoran URL:n ilman tiedostonimeä
- **Custom domain** aktivoi HTTPS automaattisesti
- GitHub Pages **ei tue** server-side code (PHP, Node) — tämä on vain HTML/JS, joten toimii täydellisesti

---

## Haluatko teen valmiiksi?

Voin alustaa GitHub-repon ja pushata tiedoston sinne, jos annat:
1. GitHub-käyttäjänimesi
2. Haluatko repo:n nimeksi `matsimakkara-indeksi` vai jotain muuta?

Tarvitsen GitHub Personal Access Tokenin (classic) tehdäkseni tämän puolestasi.

Luo token: https://github.com/settings/tokens → Generate new token (classic) → scopes: `repo`
