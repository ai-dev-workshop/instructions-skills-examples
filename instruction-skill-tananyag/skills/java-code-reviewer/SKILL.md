---
name: java-code-reviewer
description: "Review Java or Spring changes against the original task and project conventions. Use for code reviews, pull requests, diffs, and Java snippets."
---

# Java kodreview

## Cel

A valtoztatas hibainak es a kovetelmenyektol valo eltereseinek feltarasa az
eredeti feladat kontextusaban. Ne talalj ki hibat, es ne terjeszd ki a review
scope-jat nem erintett kodra.

## Munkamenet

1. Olvasd el az eredeti feladatot vagy user storyt, ha rendelkezesre all.
   Eloszor azt ellenorizd, hogy a valtoztatas teljesiti-e a kovetelmenyt.
2. Olvasd el a relevans projektkonvenciokat, es vizsgald azok betartasat.
3. Review eseten a valtoztatas diffjet vizsgald, ne a teljes kodbazist. A
   felhasznalo altal megadott bazishoz viszonyits; ne feltetelezz branch-nevet
   vagy merge-base-t.
4. Ellenorizd a relevans szempontokat:
   - uzleti logika, hatarertekek, null-kezeles;
   - konkurencia es atomi muveletek;
   - penzkezeles, skala es kerekites;
   - kivetelkezeles es hibavalasz;
   - biztonsag, bemenetvalidacio es erzekeny adatok;
   - a valtoztatashoz szukseges tesztek.
5. Minden jelzett problemat tamassz ala konkret kodhellyel, es javasolj a
   scope-on beluli minimalis javitast. BLOCKER eseten adj reprodukalhato
   forgatokonyvet, ha ez ertelmezheto.
6. Ha nem talalsz hibat, mondd ki egyertelmuen. Ne gyarts talalatot csak azert,
   hogy legyen eredmeny.

## Kimenet

Magyarul valaszolj, kiveve ha a kerelmezo mas nyelvet ker. Talalat eseten
prioritas szerint rendezd:

| Sulyossag | Fajl / hely | Problema | Javaslat |
|---|---|---|---|
| BLOCKER | `src/.../Example.java:42` | Konkret, feladatot vagy helyesseget erinto hiba | Minimalis javitas |
| MAJOR | `src/.../Example.java:57` | Jelentos hianyossag vagy konvenciosertes | Javaslat |
| MINOR | `src/.../Example.java:68` | Alacsony kockazatu, de valos problema | Javaslat |

Sulyossagok:

- **BLOCKER** – hibas mukodes, adatvesztes, biztonsagi kockazat vagy sulyos
  konkurenciahiba; javitas nelkul ne merge-old.
- **MAJOR** – lenyeges hianyossag, peldaul a kovetelmeny egy resze vagy fontos
  tesztlefedettseg hianyzik.
- **MINOR** – valos, de alacsony kockazatu problema.

A tabla utan roviden add meg a talalatok szamat sulyossagonkent, es foglald
ossze, hogy a valtoztatas merge-elheto-e. Ha nincs talalat, irj rovid
osszegzest arrol, hogy mit vizsgaltal es nem talaltal javitando hibat.
