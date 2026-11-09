---
description: "Use when creating or changing Java code in a Spring-style service. Covers layering, dependency injection, money, errors, configuration, time, and tests."
applyTo: "**/*.java"
---

# Java szolgaltatas projektkonvencioi

Ezek a mintaprojekt alapkonvencioi. Meglevo projektben eloszor ellenorizd a
kodbazist es annak dokumentalt szabalyait; azok elveznek elsobbseget.

## Architektura

- Tartsd a fuggosegi iranyt: `controller` -> `service` -> `repository`.
- A controller HTTP-kapcsolatot kezeljen, uzleti logikat ne.
- Fuggosegeket konstruktoron keresztul adj at; ne hasznalj mezos injektalast.
- DTO-k es valtoztathatatlan domain-adatok eseten reszesitsd elonyben a `record`
  tipust, ha az illik a projekthez.

## Penz es numerikus ertekek

- Penzosszeget `BigDecimal` tipussal kezelj, ne binaris lebegopontos tipussal.
- `BigDecimal` ertekeket `compareTo`-val hasonlits ossze; az `equals` a skala
  kulonbsege miatt mas eredmenyt adhat.
- Kerekitesi modot es skalat csak a kovetelmeny vagy a meglevo domain-szabaly
  alapjan valassz; ne talalj ki uzleti szabalyt.

## Hibakezeles

- Varhato uzleti hibakhoz hasznalj a projekt mintajat koveto, tipizalt kivetelt.
- A HTTP-hibavalaszokat kozos kezelo alakitja a dokumentalt formatumra, peldaul
  `errorCode`, `message` es `timestamp` mezokkel.
- Uj hibakodot a projekt nevkonvencioja szerint vezess be; ne adj vissza belso
  stack trace-t vagy implementacios reszletet a kliensnek.

## Konfiguracio

- Kulso beallitasokat a projekt konfiguracios rendszeret hasznalva kezelj, egyedi
  projekt-prefix alatt.
- Ne irj konfiguracios erteket, kulcsot vagy titkot forraskodba.
- Keruld a nev nelkuli, szetszort konstansokat; a valtoztathato ertekeket
  konfiguraciobol, az uzleti allandokat jol nevezett konstanskent kezeld.

## Ido

- Idozona-fuggo uzleti logikaban hasznalj explicit `ZoneId`-t; ne hagyatkozz a
  gep alapertelmezett idozonajara.
- Az aktualis idot injektalhato `Clock`-on keresztul kerdezd le, hogy a viselkedes
  determinisztikusan tesztelheto legyen.

## Tesztek es nyelv

- Kovetsd a projekt tesztkeretrendszeret es assert-konyvtarat.
- Egy teszt egy jol korulhatarolt viselkedest ellenorizzen; mockot kulso
  rendszerekre vagy hatarfeluletre hasznalj, ne a vizsgalt logika helyett.
- A tesztnevek legyenek beszedesek, es fejezzek ki a helyzetet es az elvart
  viselkedest.
- A kodazonositok nyelvet es a kommentek stilusat a projekt meglvo konvencioja
  szerint valaszd.
