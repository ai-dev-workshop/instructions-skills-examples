---
description: "Use when implementing multi-step code changes, refactoring, or tests. Covers planning, scope control, verification, and handling blockers."
---

# Biztonsagos fejlesztesi munkamenet

## Feladat ertelmezese es tervezese

- Eloszor foglald ossze a kovetelmenyt, az erintett modulokat es a vart
  viselkedest.
- Tobbfajlos, kockazatos vagy tobbfele megoldast igenylo valtoztatas elott
  mutass rovid tervet, es varj jovahagyasra, ha a felhasznalo ezt keri vagy a
  valasztas erdemben befolyasolja a megoldast.
- Ne kezdj el nem kert, kapcsolodo refaktoralast.
- Ha a feladat kovetelmenye vagy a kodbazis viselkedese nem egyertelmu, tisztazd
  a kerdeses reszt, mielott olyan dontest hozol, ami megvaltoztatja a termek
  viselkedeset.

## Valtoztatas

- Olvasd el a modositando kodot es a kozvetlenul kapcsolodo mintakat.
- Kis, attekintheto lepesekben dolgozz; a meglevo architekturahoz, segedekhez,
  nevkonvenciakhoz es formazashoz igazodj.
- Ne lepjen ervenybe atmeneti szabalysertes csendben. Ha egy refaktor koztes
  allapota ideiglenesen nem felel meg egy architekturalis szabalynak, jelold
  egyertelmuen, es a befejezeskor ellenorizd, hogy az ideiglenes jelolesek
  eltuntek.
- Uj teszt irasa elott olvasd el a teljes vizsgalt implementaciot es a relevans
  kozvetlen fuggosegeket. Az elvart ertekeket a tenyleges viselkedesbol vezesd
  le, ne feltetelezesbol.

## Ellenorzes es blokkolok

- Futtasd a valtoztatast legjobban lefedo meglevo tesztet, lintet vagy
  tipusellenorzest; az eredmenyt pontosan jelentsd.
- Ne allits sikeres ellenorzesrol, ha az nem futott le.
- Ha blokkoloba utkozol, peldaul hianyzo kovetelmenybe, ellentmondo szabalyba
  vagy nem vart kodbazis-strukturaba, allj meg az erintett dontes elott, es
  mondd el, milyen informacio hianyzik.
- A valaszban foglald ossze a modositott fajlokat, a lenyegi donteseket es az
  ellenorzes eredmenyet.
