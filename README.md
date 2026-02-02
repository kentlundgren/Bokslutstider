# 📅 Bokslutstider - Möteskalender 2026

Ett interaktivt kalendersystem för Kultur- och Fritidsförvaltningen, Simrishamns kommun.

## 📋 Beskrivning

Detta projekt innehåller en elegant webbbaserad möteskalender för att planera och visualisera månatliga uppföljningsmöten med enhetschefer under 2026 (februari-december).

### Funktioner

- ✅ **Interaktiv årsöversikt** med 11 månader
- ✅ **Färgkodning** för olika enheter/avdelningar
- ✅ **Smart möteslogik** som automatiskt anpassar datum vid helgkrockar
- ✅ **Responsiv design** för desktop, surfplatta och mobil
- ✅ **Modal-dialoger** med detaljerad mötesinformation
- ✅ **Utskriftsfunktion** för papperskalender
- ✅ **Tooltips** med snabbinformation vid hover

## 👥 Mötesstruktur

Kalendern hanterar möten med följande enheter:

| Enhet | Ansvarig | Tid | Ansvarsnummer |
|-------|----------|-----|---------------|
| **Fritid** | Emmy & Viktor | 09:00-10:30 (Dag 1) | 41000 |
| **Allmän kultur** | Elisabeth | 13:00-14:30 (Dag 1) | 42000 |
| **Museet** | Egil | 09:00-10:30 (Dag 2) | 46000 |
| **Biblioteket** | Katrin | 13:00-14:30 (Dag 2) | 47000 |
| **Förvaltningschef** | Gunilla | 09:00-09:30 (Dag 3) | 40000 |

## 📊 Bokningslogik

### Standardregel
Möten hålls den **10:e, 11:e och 12:e** varje månad.

### Vid helgkrock
Om något av dessa datum är helg, flyttas alla tre mötesdagar – oftast tidigare i veckan, ibland senare.

### Färgkodning
- 🟢 **Grönt** = Standarddatum (10-12:e)
- 🟠 **Orange** = Anpassat datum (på grund av helgkrock)
- 🔴 **Rött** = Helgdagar (ej tillgängliga)

## 🚀 Komma igång

### 🌐 Live Demo

**Besök den publicerade versionen:** [https://kentlundgren.github.io/Bokslutstider/](https://kentlundgren.github.io/Bokslutstider/)

### Förutsättningar

- En modern webbläsare (Chrome, Firefox, Edge, Safari)
- Ingen installation krävs - projektet är rent HTML/CSS/JavaScript

### Installation

1. Klona projektet:
```bash
git clone https://github.com/kentlundgren/bokslutstider.git
```

2. Öppna `index.html` i din webbläsare:
```bash
cd bokslutstider
start index.html  # Windows
# eller
open index.html   # macOS
```

### Användning

- **Navigera**: Scrolla genom månaderna
- **Visa detaljer**: Klicka på färgade datum för att se mötesdetaljer
- **Skriv ut**: Klicka på "Skriv ut"-knappen för en utskriftsvänlig version
- **Läs guide**: Klicka på "Git och GitHub Guide" i footern för versionhantering

## 📁 Projektstruktur

```
bokslutstider/
│
├── index.html          # Huvudfil med möteskalendern
├── GitHub.html         # Guide för Git och GitHub
├── README.md           # Denna fil
└── .gitignore          # Git-ignorerade filer
```

## 🎨 Design

Projektet använder:
- **Typografi**: Playfair Display (rubriker) + DM Sans (brödtext)
- **Färgpalett**: Inspirerad av sydöstra Skånes landskap
  - Havsblått (#3498db) - Fritid
  - Lavendel (#9b59b6) - Allmän kultur
  - Bärnsten (#e67e22) - Museet
  - Skogsgrön (#27ae60) - Biblioteket
  - Tegelröd (#c0392b) - Förvaltningschef

## 📊 Statistik 2026

- **55** möten totalt
- **33** mötesdagar
- **71,5** mötestimmar
- **6** månader med anpassade datum

## 🔧 Teknisk information

- **HTML5**: Semantisk markup
- **CSS3**: Custom properties, Grid, Flexbox, Animationer
- **JavaScript (ES6+)**: Vanilla JS, ingen externa dependencies
- **Responsiv**: Mobile-first approach
- **Print-optimerad**: Särskild CSS för utskrift
- **Tillgänglighet**: WCAG-medveten design

## 🤝 Bidra

Detta är ett internt projekt för Simrishamns kommun. För förslag på förbättringar, kontakta Kent Lundgren.

## 📝 Licens

© 2026 Simrishamns kommun - Kultur- och Fritidsförvaltningen

## 👨‍💼 Kontakt

**Kent Lundgren**  
Ekonom/Controller  
Kultur- och Fritidsförvaltningen  
Simrishamns kommun

## 🔗 Länkar

- **Live Demo:** [https://kentlundgren.github.io/Bokslutstider/](https://kentlundgren.github.io/Bokslutstider/)
- **GitHub Repo:** [https://github.com/kentlundgren/Bokslutstider](https://github.com/kentlundgren/Bokslutstider)
- **Git och GitHub Guide:** [GitHub.html](GitHub.html) - Lär dig versionhantering
- **Simrishamns kommun:** [simrishamn.se](https://simrishamn.se)

---

**Skapad**: 2026-02-02  
**Senast uppdaterad**: 2026-02-02  
**Version**: 1.0.0
