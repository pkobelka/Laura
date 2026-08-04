# Laura – kvízy se strejdou Peťou

Sbírka jednoduchých webových kvízů a her pro děti. Každý kvíz je jeden
samostatný HTML soubor (žádné externí obrázky ani knihovny), takže stačí
otevřít v prohlížeči.

## Struktura

```
index.html                # Rozcestník – seznam všech kvízů
kvizy/                     # Sem patří jednotlivé kvízy
  laura-stitch-matematika.html
```

## Jak přidat nový kvíz

1. Vytvoř nový HTML soubor ve složce `kvizy/`. Pojmenuj ho podle vzoru
   `jmeno-tema.html`, např. `nikola-nasobilka.html`, `pavel-zvirata.html`.
2. Otevři `index.html` a do seznamu `<ul class="quiz-list">` zkopíruj
   jeden `<li>` blok. Uprav v něm odkaz (`href`), ikonu (emoji) a jméno.
3. Hotovo – nový kvíz se objeví na hlavní stránce.
