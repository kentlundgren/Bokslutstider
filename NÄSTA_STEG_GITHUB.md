# 🚀 Nästa steg: Pusha till GitHub

Git-repot är nu skapat lokalt! Här är stegen för att få upp det på GitHub:

## ✅ Vad som är klart

- ✅ Git-repo initierat lokalt
- ✅ `.gitignore` skapad (skyddar känsliga filer)
- ✅ README.md skapad (projektdokumentation)
- ✅ Första commit gjord: "Initial commit: Möteskalender 2026"
- ✅ Länkar mellan `index.html` och `GitHub.html` skapade

## 📝 Steg för att pusha till GitHub

### 1️⃣ Skapa ett GitHub-konto (om du inte har ett)

Gå till [github.com](https://github.com) och registrera dig.

### 2️⃣ Skapa ett nytt repository på GitHub

1. Logga in på GitHub
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

# Lägg till GitHub som "remote" (byt ut DIT-ANVÄNDARNAMN)
git remote add origin https://github.com/DIT-ANVÄNDARNAMN/bokslutstider.git

# Kontrollera att remote är tillagd
git remote -v

# Pusha till GitHub första gången
git push -u origin main
```

**VIKTIGT**: Byt ut `DIT-ANVÄNDARNAMN` mot ditt riktiga GitHub-användarnamn!

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
git config --global user.email "din.epost@exempel.se"
```

## 📚 Mer hjälp

- Öppna `GitHub.html` i din webbläsare för en komplett guide
- Läs `README.md` för projektdokumentation
- Besök [GitHub Docs (svenska)](https://docs.github.com/sv)

---

**Lycka till med Git och GitHub!** 🎉

Om du har frågor, se den detaljerade guiden i `GitHub.html`.
