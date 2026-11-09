---
name: pr-description-generator
description: "Create a complete pull request description from a code diff, commit history, or change summary. Use when preparing a PR for review."
---

# Pull request leiras generalo

## Bemenet es tenyszeruseg

- Hasznald a megadott diffet, taskot, commitlistat es projekt PR-sablont.
- Ne talalj ki ticketazonositot, teszteredmenyt, erintett modult vagy kockazatot.
  Ismeretlen tickethez hasznalj `TICKET-XXXX` helyorzo nevet, ha a
  projektsablon megkoveteli.
- A leiras scope-ja a felhasznalo altal megadott bazis es a jelenlegi
  valtoztatas. Ne tulajdonits a valtoztatasnak elozo, nem erintett technikai
  adossagot.
- Commitlista generalasakor ne feltetelezz cel-branch-et. Ha az nem derul ki a
  kontextusbol, kerdezd meg; ne talalj ki merge-base-t vagy commitot.
- A tesztrol csak a tenylegesen megadott vagy lefuttatott informaciot ird le.

## Osszeallitas

1. Azonositsd a valtoztatas celjat es a fo technikai megoldast.
2. Sorold fel az osszes erintett modult, ha ezek a diffbol megbizhatoan
   megallapithatok.
3. Emeld ki a valos mellekhatasokat es kockazatokat, peldaul API-torest,
   adatformatum-valtozast, cache- vagy navigacios hatast. Ha nincs ismert
   kockazat, ezt ovatosan fogalmazd meg.
4. Toltsd ki a projekt osszes kotelezo PR-sablonreszet. Az opcionális szakaszt
   csak akkor hagyd el, ha a sablon ezt megengedi.
5. Cimnel kovess egy letezo projektformatumot. Ha nincs ilyen, keszits rovid,
   cselekvo megfogalmazasu cimet (legfeljebb 72 karakter), es ne gyarts hamis
   modulprefixet.
6. A szoveg nyelvet igazitsd a felhasznalo keresehez; kodnevek, fajlutak es
   modulazonositok maradjanak valtozatlanok.

## Kimeneti sablon

## Osszefoglalo
Rovid leiras arrol, mi valtozott es miert.

## Motivacio
Ticketazonosito vagy a technikai indok. Ismeretlen azonosito eseten jelold
helyorzo szoveggel.

## Megoldas
A megkozelites es a fontos implementacios dontesek.

## Erintett modulok
Vesszovel elvalasztott lista, ha megallapithato.

## Commitok
Az osszes commit az ellenorzott tartomanybol, a tartomany elso commitjat is
beleertve, ha a commitlista rendelkezesre all.

## Tesztek
- [ ] Uj tesztek
- [ ] Meglevo tesztek modositva vagy torolve (indoklas)
- [ ] Nem szukseges teszt (indoklas)

## Mellekhatasok es kockazatok
Csak igazolt vagy a diffbol egyertelmuen kovetkezo hatasokat sorolj fel.

## Ellenorzolista
Csak a celprojekt tenyleges kovetelmenyeit tartalmazza; a nem relevans pontokat
ne hagyd benne automatikusan.

## Architektura
Ha a valtoztatas tobb komponens kozotti flow-t erint, adj rovid ASCII diagramot.
Egyszeru, egyetlen komponensre korlatozodo valtoztatasnal csak akkor szerepeljen,
ha a projekt PR-sablonja megkoveteli.
