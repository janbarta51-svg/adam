# Balažovičovic první túra

Webový deník pěší túry do Santiaga. Zachovává vzhled a ovládání webu Cesta do Istanbulu: mobilní zobrazení, rozbalovací zápisky, postranní menu, odkazy na mapu a fotografie i prohlížení snímků. Zatím neobsahuje žádný zápisek ani fotografie z původní cyklocesty.

## Zprovoznění

1. Projekt je určený pro kořen repozitáře `janbarta51-svg/adam`; stránka poběží na `https://janbarta51-svg.github.io/adam/`. Soubor `CNAME` sem záměrně nepatří, aby nový web nepřevzal doménu původní stránky.
2. V nastavení repozitáře otevři **Settings → Pages → Build and deployment** a zvol **GitHub Actions**. Workflow po nahrání sestaví a zveřejní web.
3. Na [Pages CMS](https://pagescms.org/) se přihlas přes GitHub, vyber nový repozitář a otevři **Denní zápisky**. Přístup CMS k repozitáři musí být povolen.
4. Vytvoř den: **Číslo dne**, **Nadpis dne**, **Datum**, **Odkud**, **Kam**, **Km**, **Popis**. Fotografie a přepínač **Publikovat** jsou navíc. Po uložení se spustí nové sestavení stránky.

Číslo dne určuje pořadí a název souboru `_days/den-N.md`; použij pro každý den nové číslo. Pole **Km** je číselné. Úvodní stránka nyní ukazuje informaci, že se zápisky připravují.

Odkazy na Google Fotky a Mapy.com jsou z původního webu. Až bude nová trasa a album, nahraď je v `index.html` v odkazech s třídami `journey-link--photos` a `journey-link--map`.

## Soubory

- `index.html` – vzhled, interakce a šablona deníku;
- `.pages.yml` – pole v Pages CMS;
- `_config.yml` a `_days/` – nastavení Jekyllu a nové zápisky;
- `media/` – loga odkazů a budoucí fotografie;
- `.github/workflows/pages.yml` – sestavení a nasazení GitHub Pages;
- `scripts/optimize-images.py` – úprava nahraných fotografií.
