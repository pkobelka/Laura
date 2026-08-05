# Laura – kvízy se strejdou Peťou

Sbírka jednoduchých webových kvízů a her pro děti. Každý kvíz je jeden
samostatný HTML soubor (žádné externí obrázky ani knihovny), takže stačí
otevřít v prohlížeči.

## Struktura

```
index.html                # Rozcestník – seznam všech kvízů
kvizy/                     # Sem patří jednotlivé kvízy
  _sablona.html                      # Šablona: matematika s klávesnicí (pro děti)
  _sablona-hospodsky-kviz.html       # Šablona: hospodský kvíz se soutěžními režimy
  laura-stitch-matematika.html
  hanum-hospodsky-kviz-01.html       # Hospodský kvíz – 1. rozehřívací díl (jeden průchod)
  hanum-hospodsky-kviz-02.html       # Hospodský kvíz – 2. díl (nové otázky)
```

## Dva typy kvízů

- **Matematika s klávesnicí** (`_sablona.html`) – dítě píše výsledek na
  číselné klávesnici, série s rostoucí obtížností.
- **Hospodský kvíz** – výběr z odpovědí A/B/C/D, okruhy, zvuk při správné
  odpovědi. Nový díl uděláš tak, že vhodný soubor zkopíruješ, přejmenuješ
  a nahoře ve `<script>` v bloku **① OTÁZKY** přepíšeš okruhy a otázky.
  Existují dvě verze:
  - `hanum-hospodsky-kviz-01.html` (a `-02`) – **rozehřívací díly**: jeden prostý
    průchod s jedním skóre, bez soutěžení.
  - `_sablona-hospodsky-kviz.html` – **soutěžní šablona** se třemi režimy:
    - *Hrát dohromady* – jedno skóre pro partu u stolu.
    - *Soupeřit v týmech* – 2–4 týmy se střídají na jednom mobilu, průběžné
      pořadí a vyhlášení vítěze.
    - *Závod na dvou mobilech* – každý tým hraje na svém telefonu. Hra začne
      až po zadání **startovního kódu** (`startovniKod` v bloku ① OTÁZKY),
      který pošleš oběma týmům ve smluvenou dobu (klidně naplánovanou SMS).
      Stejné otázky, běží čas; na konci se porovná skóre.

## Jak vyrobit nový kvíz ze šablony

1. Zkopíruj `kvizy/_sablona.html` a pojmenuj kopii podle vzoru
   `jmeno-tema.html`, např. `nikola-nasobilka.html`, `pavel-zvirata.html`.
2. V novém souboru nahoře v `<script>` najdi blok **① NASTAVENÍ** a přepiš:
   - `rod` – `"holka"` nebo `"kluk"` (hlídá české koncovky: šikovná/šikovný,
     zvládla/zvládl …),
   - `jmeno5pad` – oslovení, např. `"Pavle"` → „Ahoj Pavle!",
   - `avatar…` – emoji podle tématu (Stitch, auta, zvířátka …),
   - `uvodniText` – uvítací věty.
3. Chceš jiné otázky? Uprav funkci `generateProblem()` v bloku **④ OTÁZKY** –
   u každého typu se nastavuje `currentAnswer` (výsledek), text příkladu a
   nápověda.
4. Přidej kvíz do rozcestníku: otevři `index.html` a v seznamu
   `<ul class="quiz-list">` zkopíruj jeden `<li>` blok a uprav odkaz, emoji
   a jméno.

Soubory začínající podtržítkem (`_sablona.html`) jsou pomocné a do
rozcestníku se nedávají.
