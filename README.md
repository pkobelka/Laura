# Laura – kvízy se strejdou Peťou

Sbírka jednoduchých webových kvízů a her pro děti. Každý kvíz je jeden
samostatný HTML soubor (žádné externí obrázky ani knihovny), takže stačí
otevřít v prohlížeči.

## Struktura

```
index.html                # Rozcestník – seznam všech kvízů
kvizy/                     # Sem patří jednotlivé kvízy
  _sablona.html           # Prázdná šablona ke kopírování
  laura-stitch-matematika.html
```

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
