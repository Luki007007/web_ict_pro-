Zkontroluj změny v projektu a proveď commit + push na GitHub podle níže uvedených pravidel.

## Pravidla pro tento projekt

**Repo:** `https://github.com/Luki007007/web_ict_pro-.git`  
**Větev:** `main` (jediná větev, GitHub Pages nasazuje z `main`)  
**Žádný build krok** – soubory se commitují přímo, žádné `npm run build` ani podobné.

## Postup

1. Spusť `git status` – zjisti, které soubory se změnily.
2. Spusť `git diff` – projdi konkrétní změny, aby commit message byla přesná.
3. Přidej soubory **jmenovitě** (nikdy `git add -A` nebo `git add .` – hrozí náhodné přidání citlivých souborů):
   ```
   git add index.html style.css main.js ...
   ```
4. Vytvoř commit message podle formátu:
   - `fix: popis opravy chyby`
   - `feat: popis nové funkce nebo stránky`
   - `style: úprava vzhledu bez změny funkce`
   - `docs: změna dokumentace`
   - `content: aktualizace textového obsahu`
   - Zpráva v češtině nebo angličtině, max ~72 znaků na prvním řádku.
5. Commitni:
   ```
   git commit -m "typ: popis"
   ```
6. Pushni na GitHub:
   ```
   git push
   ```
7. Potvrď, že push proběhl (`git log --oneline -3`).

## Co NIKDY nepřidávat do commitu

- `.env` soubory nebo soubory s hesly/klíči
- `node_modules/` (zde neexistuje, ale pro jistotu)
- Dočasné soubory editoru (`.DS_Store`, `Thumbs.db`, `*.tmp`)

## Po úspěšném push

GitHub Pages se automaticky nasadí do ~1–2 minut.  
Živý web: `https://luki007007.github.io/web_ict_pro-/`

Pokud uživatel nezadal konkrétní commit message, navrhni ji na základě `git diff` a zeptej se na potvrzení před samotným commitem.
