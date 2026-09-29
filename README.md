# Unicode Checker

Online kontrola seznamu e-mailových adres oddělených středníkem. Po vložení textu aplikace hned ukáže znaky, kvůli kterým by e-mail neodešel, a nabídne opravený seznam ke zkopírování.

## Co kontroluje

- **Neviditelné znaky:** mezera nulové šířky (ZWSP), nezlomitelná mezera (NBSP), BOM, měkký spojovník, řídicí znaky směru textu, řídicí znaky ASCII.
- **Znaky, které jen vypadají stejně:** písmena z cyrilice a řečtiny, zavináč a tečka plné šířky, typografické pomlčky a apostrofy, řecký otazník nebo jiný „středník“ jako oddělovač.
- **Diakritika a znaky mimo ASCII:** volitelně převede á → a, č → c apod.
- **Formát adresy:** chybějící nebo zdvojený zavináč, tečky na okraji, čárka v doméně, chybějící koncovka, délkové limity (RFC 5321), více adres bez středníku, překlepy typu `gmial.com`, duplicity.

Každý nález má pozici v textu a tlačítko **Najít**, které znak označí ve vstupním poli. Panel **Rentgen textu** zobrazí celý vložený text i s neviditelnými znaky.

## Soukromí

Vše běží jen v prohlížeči. Text se nikam neodesílá.

## Spuštění

Jde o jediný soubor `index.html` bez závislostí. Stačí ho otevřít v prohlížeči, nebo zapnout GitHub Pages (Settings → Pages → Deploy from a branch → `main` / root) a aplikace poběží na `https://castkav.github.io/unicodechecker/`.
