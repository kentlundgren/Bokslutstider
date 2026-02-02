# 🚀 Nästa steg: Pusha till GitHub

Git-repot är nu skapat lokalt! Här är stegen för att få upp det på GitHub:

## ✅ Vad som är klart

- ✅ Git-repo initierat lokalt
- ✅ `.gitignore` skapad (skyddar känsliga filer)
- ✅ README.md skapad (projektdokumentation)
- ✅ Första commit gjord: "Initial commit: Möteskalender 2026"
- ✅ Länkar mellan `index.html` och `GitHub.html` skapade
- ✅ Git-konfiguration: Kopplad till **kentlundgren**-kontot

## 👥 Dina två GitHub-konton

Du har två GitHub-konton och det är viktigt att veta vilket som används!

| Konto | Användning | E-post | Status |
|-------|-----------|---------|--------|
| **[kentlundgren](https://github.com/kentlundgren/)** | Personliga projekt | lundgren.kent@gmail.com | ✅ **AKTIV NU** |
| **[lundgren9](https://github.com/lundgren9)** | Poolia-projekt (jobb) | (Annan e-post) | Inaktiv |

### 🔍 Kontrollera vilket konto som används:

```powershell
# Kolla ditt namn
git config user.name

# Kolla din e-post (detta avgör vilket GitHub-konto!)
git config user.email
```

**Ditt nuvarande konto:**
- Namn: `Kent Lundgren`
- E-post: `lundgren.kent@gmail.com`
- GitHub: **https://github.com/kentlundgren/**

✅ Detta betyder att när du pushar detta projekt kommer det hamna på **kentlundgren**-kontot!

### 🔄 Vill du byta konto?

Om du vill pusha till **lundgren9**-kontot istället:

```powershell
# Ändra globalt (för alla projekt)
git config --global user.name "Kent på Poolia"
git config --global user.email "din-poolia-epost@exempel.se"

# ELLER ändra bara för detta projekt (rekommenderat)
cd "d:\VåraFiler_primära_på_SSD\Kent_dokument\Data\HTML\kentlundgren_se\arbete\SK\Bokslutstider"
git config user.name "Kent Lundgren"
git config user.email "lundgren.kent@gmail.com"
```

**⚠️ VIKTIGT:** E-postadressen måste matcha den som är registrerad på ditt GitHub-konto!

## 📝 Steg för att pusha till GitHub

### 1️⃣ Logga in på rätt GitHub-konto

Gå till [github.com](https://github.com) och logga in på **kentlundgren**-kontot (eftersom det är det din Git är konfigurerad för).

### 2️⃣ Skapa ett nytt repository på GitHub

1. Se till att du är inloggad på **kentlundgren**-kontot
2. Klicka på den gröna knappen **"New"** (eller går till: https://github.com/new)
3. Fyll i:
   - **Repository name**: `bokslutstider`
   - **Description**: "Möteskalender för Kultur- och Fritidsförvaltningen 2026"
   - Välj **Public** eller **Private** (rekommenderar Private för internt projekt)
   - **VIKTIGT**: Välj INTE "Add a README file" (vi har redan en)
   - **VIKTIGT**: Välj INTE "Add .gitignore" (vi har redan en)
4. Klicka **"Create repository"**

### 3️⃣ Koppla ditt lokala repo till GitHub

När repot är skapat visar GitHub instruktioner. Använd dessa kommandon i PowerShell:

```powershell
# Gå till projektmappen (om du inte redan är där)
cd "d:\VåraFiler_primära_på_SSD\Kent_dokument\Data\HTML\kentlundgren_se\arbete\SK\Bokslutstider"

# Lägg till GitHub som "remote" (använd kentlundgren-kontot)
git remote add origin https://github.com/kentlundgren/bokslutstider.git

# Kontrollera att remote är tillagd
git remote -v

# Pusha till GitHub första gången
git push -u origin main
```

**📌 OBS:** URL:en ovan använder **kentlundgren** eftersom det är kontot du är kopplad till. Om du vill använda **lundgren9** istället, byt till:
```
https://github.com/lundgren9/bokslutstider.git
```

### 4️⃣ Autentisering

När du kör `git push` första gången kommer du behöva autentisera dig. Du har två alternativ:

#### Alternativ A: GitHub Desktop (Enklast för nybörjare) ⭐ REKOMMENDERAS

1. Ladda ner [GitHub Desktop](https://desktop.github.com/)
2. Installera och logga in
3. Klicka "Add" → "Add existing repository"
4. Välj din `Bokslutstider`-mapp
5. Klicka "Publish repository" i GitHub Desktop

#### Alternativ B: Personal Access Token (PAT)

1. Gå till GitHub → Settings → Developer settings → Personal access tokens → Tokens (classic)
2. Generera ny token med **repo**-rättigheter
3. Kopiera token (visas bara en gång!)
4. När du kör `git push`, använd token som lösenord

## 📅 Dagligt arbetsflöde efter första push

När allt är uppsatt, använd detta enkla flöde:

```powershell
# 1. Gå till projektmappen
cd "d:\VåraFiler_primära_på_SSD\Kent_dokument\Data\HTML\kentlundgren_se\arbete\SK\Bokslutstider"

# 2. Se vad som ändrats
git status

# 3. Lägg till alla ändringar
git add .

# 4. Commit med beskrivande meddelande
git commit -m "Beskrivning av vad du ändrat"

# 5. Pusha till GitHub
git push
```

## 💡 Exempel på bra commit-meddelanden

✅ **Bra:**
- `"Lagt till påskmöte i april-kalendern"`
- `"Fixat stavfel i mötesnamn"`
- `"Uppdaterat färger för bättre kontrast"`
- `"Ändrat tider för biblioteksmöten"`

❌ **Dåligt:**
- `"fix"` (för vagt)
- `"uppdatering"` (inte beskrivande)
- `"diverse ändringar"` (för brett)

## 🎯 Viktiga PowerShell-tips

⚠️ **Kom ihåg**: I PowerShell fungerar INTE `&&` för att kedja kommandon!

**FEL:**
```powershell
cd bokslutstider && git status  ❌
```

**RÄTT:**
```powershell
cd bokslutstider
git status  ✅
```

eller använd semikolon:
```powershell
cd bokslutstider; git status  ✅
```

## 📊 Användbara Git-kommandon

```powershell
# Se historik
git log --oneline

# Se ändringar som inte är committade
git diff

# Ångra ändringar i en fil (innan git add)
git checkout -- filnamn.html

# Se remote-adress
git remote -v

# Hämta senaste från GitHub
git pull
```

## 🆘 Felsökning

### Problem: "Permission denied"
**Lösning**: Använd GitHub Desktop eller konfigurera Personal Access Token (se ovan)

### Problem: "Git is not recognized"
**Lösning**: Installera Git från [git-scm.com](https://git-scm.com/)

### Problem: "Please tell me who you are"
**Lösning**:
```powershell
git config --global user.name "Kent Lundgren"
git config --global user.email "lundgren.kent@gmail.com"
```

### Problem: "Fel GitHub-konto används"
**Symptom**: Commits dyker upp på fel GitHub-konto eller du får access denied.

**Lösning**: Kontrollera och ändra din e-post:
```powershell
# Kolla nuvarande konfiguration
git config user.email

# Om den är fel, ändra den
git config --global user.email "lundgren.kent@gmail.com"  # För kentlundgren
# eller
git config --global user.email "din-poolia-epost@exempel.se"  # För lundgren9
```

### Problem: "Repository redan finns"
**Symptom**: GitHub säger att repot redan existerar på ditt konto.

**Lösning**: 
1. Välj ett annat namn, t.ex. `bokslutstider-2026`
2. Eller ta bort det gamla repot på GitHub först (om det är tomt)

### Problem: Commits visar fel författare på GitHub
**Orsak**: E-postadressen i din Git-config matchar inte den på GitHub.

**Lösning**: Se till att e-posten matchar:
```powershell
# Kontrollera vilken e-post som är registrerad på GitHub
# Gå till: GitHub → Settings → Emails

# Ändra Git-config till samma e-post
git config --global user.email "DEN-EPOST-SOM-FINNS-PÅ-GITHUB"
```

## 📚 Mer hjälp

- Öppna `GitHub.html` i din webbläsare för en komplett guide
- Läs `README.md` för projektdokumentation
- Besök [GitHub Docs (svenska)](https://docs.github.com/sv)

---

**Lycka till med Git och GitHub!** 🎉

Om du har frågor, se den detaljerade guiden i `GitHub.html`.
