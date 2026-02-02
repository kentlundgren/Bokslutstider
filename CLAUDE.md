# 🤖 Claude-projektet: Bokslutstider

Detta dokument innehåller information om projektet för användning med Claude eller Claude Code.

## 📋 Projektöversikt

**Projektnamn:** Bokslutstider - Möteskalender 2026  
**Typ:** Webbapplikation (HTML/CSS/JavaScript)  
**Klient:** Kultur- och Fritidsförvaltningen, Simrishamns kommun  
**Utvecklare:** Kent Lundgren (med hjälp av Claude)  
**Skapad:** 2026-02-02  
**Version:** 1.0.0

### 🔗 Viktiga länkar

- **Live Demo:** https://kentlundgren.github.io/Bokslutstider/
- **GitHub Repo:** https://github.com/kentlundgren/Bokslutstider
- **GitHub Pages aktiverad:** Ja (publiceras automatiskt från main-branchen)

---

## 🎯 Vad projektet gör

En interaktiv möteskalender som visualiserar uppföljningsmöten med enhetschefer för februari-december 2026. Kalendern använder smart logik för att automatiskt anpassa mötesdatum när helgdagar krockar med standardschema (10:e, 11:e, 12:e varje månad).

### Huvudfunktioner

- ✅ Interaktiv årsöversikt med 11 månader
- ✅ Färgkodade enheter (Fritid, Kultur, Museet, Biblioteket, Chef)
- ✅ Automatisk helgdatumhantering
- ✅ Responsiv design (mobil, surfplatta, desktop)
- ✅ Modal-dialoger med detaljerad information
- ✅ Utskriftsfunktion
- ✅ Tooltips vid hover

---

## 📂 Projektstruktur

```
Bokslutstider/
├── index.html                      # Huvudfil (1677 rader)
├── GitHub.html                     # Git/GitHub-guide (694 rader)
├── README.md                       # Projektdokumentation
├── .gitignore                      # Git-ignorerade filer
├── CLAUDE.md                       # Denna fil
├── NÄSTA_STEG_GITHUB.md           # GitHub push-instruktioner
├── VILKET_GITHUB_KONTO.txt        # GitHub-kontoinformation
├── SKAPA_GITHUB_REPO_STEG_FÖR_STEG.md  # Repo-skapandemanual
└── Git_och_GitHub_i_Cursor.jpg    # Screenshot för Cursor-guide
```

---

## 🛠️ Teknisk stack

- **HTML5**: Semantisk markup, inga ramverk
- **CSS3**: Custom properties (CSS-variabler), Grid, Flexbox
- **JavaScript**: Vanilla ES6+, inga externa bibliotek
- **Typografi**: Google Fonts (Playfair Display, DM Sans)
- **Versionhantering**: Git + GitHub
- **Hosting**: GitHub Pages
- **IDE/Editor**: Cursor (VS Code-baserad)

### Designprinciper

- Mobile-first responsive design
- Tillgänglighetsfokus (WCAG-medveten)
- Skandinavisk färgpalett (havsblått, lavendel, bärnsten, skogsgrön, tegelröd)
- Print-optimerad CSS
- Inga externa JavaScript-dependencies

---

## 👤 Användarinformation

**Namn:** Kent Lundgren  
**Roll:** Ekonom/Controller  
**Organisation:** Kultur- och Fritidsförvaltningen, Simrishamns kommun  
**Arbetssätt:** Lär sig programmering och Git/GitHub med AI-assistans

### GitHub-konton

Kent har två GitHub-konton:

1. **kentlundgren** (https://github.com/kentlundgren/)
   - **E-post:** lundgren.kent@gmail.com
   - **Användning:** Personliga projekt ✅ DETTA PROJEKT
   - **Status:** Aktivt för Bokslutstider

2. **lundgren9** (https://github.com/lundgren9)
   - **Användning:** Poolia-relaterade projekt (jobbrelaterat)
   - **Status:** Inaktivt för detta projekt

### Git-konfiguration för detta projekt

```bash
git config user.name = "Kent Lundgren"
git config user.email = "lundgren.kent@gmail.com"
```

---

## 🎨 Kodningspreferenser (från Kent's regler)

### Allmänna regler

1. **Filstruktur**: Dela alltid upp kod i separata filer (HTML, CSS, JavaScript)
2. **Organisation**: HTML i index.html, CSS i styles.css, JS i script.js
3. **Länkning**: Extern länkning mellan filer (inte inbäddad kod)
4. **Kommentarer**: Tydliga kommentarer, särskilt vid viktiga funktioner
5. **Semantisk HTML5**: Använd semantiska taggar
6. **Responsiv design**: Mobile-first approach

### Uppdateringar och versionshantering

7. **Kommentarer vid ändringar**: Kommentera tydligt "här skedde en uppdatering..."
8. **Vid otydlighet**: Fråga användaren innan du fortsätter
9. **Filhantering**: Fråga om befintlig fil ska uppdateras eller om ny fil (_verX) ska skapas
10. **ES2023**: Säg till och kommentera när ES2023-funktionalitet används
11. **Fokus**: Vid uppdatering, fokusera på uppgiften - gör inget annat

### PowerShell-specifikt

12. **Shell**: Kent använder oftast PowerShell
13. **Kommandon**: Använd INTE `&&` i PowerShell (fungerar inte)
    - ❌ `cd mapp && ls`
    - ✅ `cd mapp` + `ls` (separata kommandon)
    - ✅ `cd mapp; ls` (semikolon fungerar)

### Projektinitiering

14. **Mappstruktur**: Fråga alltid var filerna ska ligga i början av nytt projekt
15. **Git-hantering**: 
    - Lägg till .gitignore i projektet
    - Förklara när och varför det görs

### Vite-specifikt (för framtida projekt)

16. **vite.config.js build-inställningar**:
```javascript
build: {
  outDir: 'dist',
  assetsDir: 'assets',
  emptyOutDir: true,  // Rensar dist-mappen helt innan varje ny build
  // Detta förhindrar att gamla assets-filer blir kvar
}
```

17. **Base-path**: Använd alltid `base: './'` i vite.config.js för relativa sökvägar

### UI/UX-preferenser

18. **Indata-fält**: Gul bakgrund för tydlig indikering av inmatningsfält

---

## 🔗 Viktigt: Länkar mellan GitHub och GitHub Pages

**STANDARDPOLICY FÖR ALLA FRAMTIDA PROJEKT:**

### I varje webbapplikation (index.html/huvudfil):

Lägg till i footer:

```html
<footer>
    <!-- ... annat innehåll ... -->
    <p>
        <a href="[GITHUB-REPO-URL]" target="_blank" rel="noopener noreferrer">
            <!-- GitHub-ikon -->
            GitHub Repo
        </a>
    </p>
</footer>
```

### I varje README.md:

Lägg till:

```markdown
## 🔗 Länkar

- **Live Demo:** [URL till GitHub Pages]
- **GitHub Repo:** [URL till GitHub-repo]
```

### Exempel för detta projekt:

- **Live:** https://kentlundgren.github.io/Bokslutstider/
- **Repo:** https://github.com/kentlundgren/Bokslutstider

**VIKTIGT:** Detta ska göras automatiskt i alla nya projekt!

---

## 🚀 Git & GitHub arbetsflöde

### Första gången (redan gjort för Bokslutstider):

```bash
# 1. Initiera repo
git init

# 2. Skapa .gitignore (se mallen nedan)

# 3. Första commit
git add .
git commit -m "Initial commit: Beskrivning"

# 4. Skapa repo på GitHub (via webbläsaren)

# 5. Koppla samman
git remote add origin https://github.com/kentlundgren/[REPO-NAMN].git

# 6. Pusha
git branch -M main
git push -u origin main
```

### Dagligt arbetsflöde:

```bash
# 1. Se ändringar
git status

# 2. Lägg till ändringar
git add .

# 3. Commit
git commit -m "Beskrivande meddelande"

# 4. Pusha
git push
```

### Bra commit-meddelanden:

- ✅ "Lagt till färgkodning för biblioteket"
- ✅ "Fixat stavfel i mötesnamn"
- ✅ "Uppdaterat CSS för mobilvy"
- ❌ "fix" (för vagt)
- ❌ "diverse ändringar" (inte beskrivande)

---

## 📝 .gitignore-mall

Används för alla projekt:

```gitignore
# Windows
Thumbs.db
Desktop.ini
*.lnk
$RECYCLE.BIN/

# MacOS
.DS_Store
.AppleDouble
._*

# Editors
.vscode/
*.code-workspace
.idea/
*.sublime-*

# Node.js
node_modules/
npm-debug.log*
package-lock.json

# Känsligt
.env
.env.local
secrets.json
credentials.json
config.private.js

# Build
dist/
build/
out/
*.min.js
*.min.css

# Logs
*.log
logs/

# Temp
tmp/
temp/
*.tmp
*.cache

# Backups
*.bak
*.backup
*.old
```

---

## 🐛 Vanliga problem och lösningar

### Problem: Cursor står och "snurrar" på push

**Orsak:** Git-process har hängt sig

**Lösning:**
```powershell
# Döda hängande Git-processer
taskkill /F /IM git.exe
```

Sedan:
- Starta om Cursor
- Eller pusha manuellt via PowerShell: `git push`

### Problem: Remote finns inte

**Lösning:**
```bash
git remote add origin https://github.com/kentlundgren/[REPO].git
```

### Problem: Fel GitHub-konto används

**Kontrollera:**
```bash
git config user.email
```

**Ändra:**
```bash
git config --global user.email "lundgren.kent@gmail.com"  # för kentlundgren
```

### Problem: "Permission denied" vid push

**Lösning:**
- Använd GitHub Desktop (enklast)
- Eller skapa Personal Access Token på GitHub → Settings → Developer settings

---

## 📊 Projektstatus

### Klart ✅

- [x] Möteskalender skapad med interaktiv funktionalitet
- [x] GitHub.html guide för Git/GitHub
- [x] README.md dokumentation
- [x] .gitignore-fil
- [x] Git-repo initierat lokalt
- [x] GitHub-repo skapat (kentlundgren/Bokslutstider)
- [x] Pushat till GitHub
- [x] GitHub Pages aktiverad och publicerad
- [x] Länkar mellan GitHub Pages och repo (båda riktningar)
- [x] CLAUDE.md skapad

### Potentiella framtida förbättringar

- [ ] Dela upp index.html i separata filer (HTML, CSS, JS) enligt Kents regler
- [ ] Lägg till SEO meta-taggar
- [ ] Förbättra tillgänglighet med ARIA-attribut
- [ ] localStorage för användarpreferenser
- [ ] Export till iCal/Google Calendar
- [ ] Mobilapp-version (PWA)

---

## 💬 Användning med Claude Code

När du öppnar detta projekt i Claude Code:

1. **Läs denna fil först** för att förstå kontexten
2. **Följ Kent's kodningsregler** (se ovan)
3. **Fråga vid otydlighet** - gör inga antaganden
4. **Kommentera alla ändringar** tydligt
5. **Lägg till länkar** mellan GitHub Pages och repo i nya projekt
6. **Tänk på PowerShell** - ingen `&&` i kommandon
7. **Kontrollera GitHub-konto** - kentlundgren ska användas (lundgren.kent@gmail.com)

### Vid nya projekt:

- [ ] Fråga om mappstruktur
- [ ] Skapa .gitignore automatiskt
- [ ] Dela upp i HTML/CSS/JS-filer
- [ ] Lägg till länkar GitHub ↔ GitHub Pages
- [ ] Använd gul bakgrund för input-fält
- [ ] Kommentera ES2023-funktionalitet

---

## 🎓 Lärdomar från detta projekt

### Git & GitHub

- Remote måste konfigureras innan push
- Repo måste existera på GitHub innan push
- E-post i Git-config avgör vilket GitHub-konto som används
- GitHub Pages publiceras automatiskt från main-branchen
- .gitignore är kritisk för säkerhet

### Cursor-specifikt

- "Initialize Repository" = `git init` (lokalt)
- "Publish to GitHub" = Gör allt automatiskt (rekommenderas)
- Git-processer kan hänga sig - döda med taskkill

### PowerShell-specifikt

- `&&` fungerar inte - använd separata kommandon eller `;`
- Sökvägar med mellanslag måste citeras: `"d:\Våra Filer\..."`

---

## 📞 Support och resurser

### När du kör fast:

1. **Läs guiderna i projektet:**
   - GitHub.html - Omfattande Git/GitHub-guide
   - NÄSTA_STEG_GITHUB.md - Push-instruktioner
   - VILKET_GITHUB_KONTO.txt - Kontoinformation
   - SKAPA_GITHUB_REPO_STEG_FÖR_STEG.md - Repo-guide

2. **Kolla online-resurser:**
   - [Git Bok (svenska)](https://git-scm.com/book/sv/v2)
   - [GitHub Docs (svenska)](https://docs.github.com/sv)
   - [GitHub Desktop](https://desktop.github.com/) - Enklare än CLI

3. **Fråga Claude** med kontext från CLAUDE.md

---

## 🏁 Slutsats

Detta projekt är ett komplett exempel på modern webbutveckling med Git/GitHub-integration. Använd det som mall för framtida projekt och följ alltid Kent's kodningsregler för konsistens.

**Viktigt att komma ihåg:**
- Dela alltid upp kod i separata filer
- Lägg till länkar mellan GitHub och GitHub Pages
- Kommentera ändringar tydligt
- Fråga vid otydlighet
- Använd korrekt GitHub-konto (kentlundgren)
- Tänk på PowerShell-begränsningar

---

**Skapad:** 2026-02-02  
**Författare:** Kent Lundgren med Claude  
**Senast uppdaterad:** 2026-02-02  
**För användning med:** Claude, Claude Code, eller andra AI-kodassistenter
