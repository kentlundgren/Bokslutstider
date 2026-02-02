# 🚀 SKAPA GITHUB REPO - STEG FÖR STEG

## 📌 PROBLEMET
När du försöker pusha står det och "tuggar" och inget händer. Det beror på att 
repot **inte finns på GitHub ännu**. Du måste skapa det först!

## ✅ LÖSNING: Skapa repot på GitHub

### STEG 1: Gå till GitHub
1. Öppna din webbläsare
2. Gå till: https://github.com/kentlundgren
3. **VIKTIGT:** Kontrollera att du är inloggad på **kentlundgren** (inte lundgren9)
   - Kolla i övre högra hörnet att det står "kentlundgren"

### STEG 2: Skapa nytt repository
1. Klicka på den **gröna knappen** "New" eller gå till: https://github.com/new
2. Fyll i formuläret:

```
Repository name: bokslutstider
Description: Möteskalender för Kultur- och Fritidsförvaltningen 2026

✅ Private (rekommenderat - innehåller intern info)
⭕ Public (om du vill att alla ska kunna se projektet)

❌ KRYSSA INTE I "Add a README file" - vi har redan en!
❌ KRYSSA INTE I "Add .gitignore" - vi har redan en!
❌ KRYSSA INTE I "Choose a license" - behövs inte nu

3. Klicka på "Create repository"
```

### STEG 3: Koppla lokalt repo till GitHub
Efter att repot är skapat visar GitHub denna sida:

```
…or push an existing repository from the command line
```

**Använd INTE de kommandon GitHub visar!** Vi har redan gjort `git remote add origin`.

Kör bara detta i PowerShell:

```powershell
# Gå till projektmappen
cd "d:\VåraFiler_primära_på_SSD\Kent_dokument\Data\HTML\kentlundgren_se\arbete\SK\Bokslutstider"

# Kontrollera att remote är korrekt satt
git remote -v

# Om remote INTE är satt, kör:
git remote add origin https://github.com/kentlundgren/bokslutstider.git

# Pusha till GitHub
git push -u origin main
```

### STEG 4: Autentisering
När du kör `git push` första gången kommer Windows att fråga efter autentisering.

**VAL 1: Logga in med webbläsare (enklast)**
- Ett fönster öppnas där du loggar in på GitHub
- Acceptera att ge Git tillgång
- Klart!

**VAL 2: Personal Access Token**
Om det inte fungerar, skapa en token:
1. Gå till: https://github.com/settings/tokens
2. Klicka "Generate new token (classic)"
3. Ge den ett namn: "Cursor Git Access"
4. Välj scopes: ✅ repo (alla under repo)
5. Klicka "Generate token"
6. **KOPIERA TOKEN** (visas bara en gång!)
7. När Git frågar efter lösenord, klistra in token istället

### STEG 5: Verifiera att det fungerat
1. Gå till: https://github.com/kentlundgren/bokslutstider
2. Du ska nu se alla dina filer där! 🎉
3. Du ska se två commits:
   - "Initial commit: Möteskalender 2026 med Git/GitHub guide"
   - "Uppdatering: GitHub-konton och Cursor-integration"

---

## 🔍 FELSÖKNING

### Problem: "remote origin already exists"
**Lösning:**
```powershell
# Ta bort gammal remote
git remote remove origin

# Lägg till ny
git remote add origin https://github.com/kentlundgren/bokslutstider.git
```

### Problem: "Repository not found"
**Möjliga orsaker:**
1. Du är inte inloggad på rätt GitHub-konto (kentlundgren)
2. Repot heter något annat än "bokslutstider"
3. Repot är inte skapat ännu på GitHub

**Lösning:**
- Kontrollera att du är på https://github.com/kentlundgren
- Se till att repot "bokslutstider" finns där

### Problem: "Permission denied"
**Lösning:**
Använd GitHub Desktop istället:
1. Ladda ner: https://desktop.github.com/
2. Installera och logga in (kentlundgren)
3. Klicka "Add" → "Add existing repository"
4. Välj: d:\VåraFiler_primära_på_SSD\Kent_dokument\Data\HTML\kentlundgren_se\arbete\SK\Bokslutstider
5. Klicka "Publish repository"
6. Välj Private/Public
7. Klart!

### Problem: Det står bara och "tuggar"
**Orsak:** Repot finns inte på GitHub ännu!

**Lösning:** Gå tillbaka till STEG 1 och skapa repot på GitHub först.

---

## 🎯 SAMMANFATTNING

Problemet är att du försöker pusha till ett repo som inte finns. Det är som att 
försöka skicka ett brev till en adress som inte existerar.

**Lösningen:**
1. ✅ Skapa repot på GitHub (via webbläsaren)
2. ✅ Pusha dina commits till det nya repot

Det är allt! Repot måste finnas på GitHub innan du kan pusha till det.

---

**Lycka till!** 🚀

Om något är oklart, fråga gärna!
