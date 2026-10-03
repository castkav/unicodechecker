# Unicode Checker

Online kontrola seznamu e-mailových adres oddělených středníkem. Po vložení textu aplikace hned ukáže znaky, kvůli kterým by e-mail neodešel, a nabídne opravený seznam ke zkopírování.

## Co ukazuje

Hned pod polem pro vložení jsou dvě sekce. Nic se automaticky neopravuje, aplikace jen ukazuje, kde je problém.

**Co brání odeslání**
- neviditelné znaky: mezera nulové šířky (ZWSP), nezlomitelná mezera (NBSP), BOM, měkký spojovník, řídicí znaky,
- diakritika a další znaky mimo ASCII (á, ž, ř…),
- písmena z cyrilice a řečtiny, znaky plné šířky, typografické pomlčky,
- řecký otazník nebo jiný „středník“ jako oddělovač,
- chyby formátu: chybějící nebo zdvojený zavináč, čárka v doméně, tečky na okraji, chybějící koncovka, více adres bez středníku.

U každého znaku je kód (např. `U+200B`), pozice v textu a tlačítko **Najít**, které znak označí ve vstupním poli.

**Možná špatně**
- překlepy v doménách českých i zahraničních schránek (`sezman.cz`, `gmail.co`, `seznam.com`…),
- jméno nesedí k příjmení: `martin.novakova` → nemá být `martina.novakova`?, `jana.dvorak` → nemá být `jana.dvorakova`?,
- duplicitní adresy.

## Soukromí

Vše běží jen v prohlížeči. Text se nikam neodesílá.

## Spuštění

Jde o jediný soubor `index.html` bez závislostí. Stačí ho otevřít v prohlížeči, nebo zapnout GitHub Pages (Settings → Pages → Deploy from a branch → `main` / root) a aplikace poběží na `https://castkav.github.io/unicodechecker/`.
