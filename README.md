# ICT pro – Vzdělávací agentura

Statický web vzdělávací agentury **ICT pro** zaměřené na IT dovednosti pro moderní pracovní trh.

**Live:** https://luki007007.github.io/web_ict_pro-/

---

## Kurzy

| Kurz | Délka | Cena |
|---|---|---|
| [Analýza dat – Power BI](kurz-powerbi.html) | 24 h / 8 modulů | 9 900 Kč |
| [Programování pomocí Claude](kurz-claude.html) | 20 h / 6 modulů | 8 900 Kč |
| [T-SQL snadno a rychle](kurz-tsql.html) | 18 h / 7 modulů | 7 900 Kč |

---

## Technologie

Čistý statický web – žádný framework, žádný build krok.

- **HTML / CSS / JS** – vanilla, bez závislostí
- **Google Fonts** – Inter (načítáno přes CDN)
- **GitHub Pages** – automatický deploy z větve `main`

---

## Soubory

```
index.html          # Hlavní stránka
kurz-powerbi.html   # Detail kurzu Power BI
kurz-claude.html    # Detail kurzu Claude
kurz-tsql.html      # Detail kurzu T-SQL
style.css           # Globální styly
kurz.css            # Styly pro stránky kurzů
main.js             # Navigace a hamburger menu
.nojekyll           # Zabraňuje Jekyll zpracování na GitHub Pages
```

---

## Lokální vývoj

Žádná instalace není potřeba. Stačí otevřít soubory přímo v prohlížeči nebo použít libovolný lokální server:

```powershell
# Například pomocí Python
python -m http.server 8000
```

---

## Deployment

Push do větve `main` → GitHub Pages automaticky nasadí změny.

```powershell
git add <soubory>
git commit -m "popis změny"
git push
```

> Soubor `.nojekyll` musí zůstat v kořeni – zabraňuje GitHub Pages spustit Jekyll.

---

## Kontakt

📧 info@ictpro.cz  
🌐 https://luki007007.github.io/web_ict_pro-/
