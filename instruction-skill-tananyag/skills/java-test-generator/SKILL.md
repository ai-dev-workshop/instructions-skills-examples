---
name: java-test-generator
description: "Generate or extend Java unit and component tests. Use when asked to write tests, identify edge cases, or create tests from an API contract."
---

# Java tesztgeneralo

## Alapelv

Minden elvart viselkedest a vizsgalt implementaciobol, a kovetelmenybol vagy
egy kifejezett API-kontraktusbol vezess le. Ne talalj ki visszateresi erteket,
hibakezelest vagy uzleti szabalyt.

## Munkamenet

1. Azonositsd a vizsgalt osztalyt (SUT), a feladatot es a projekt tesztkonvencioit.
2. Tesztiras elott olvasd el a SUT teljes implementaciojat es a kozvetlen
   fuggosegeit. Ha valamelyik viselkedes nem allapithato meg, kerdezz ra, vagy
   jelold kifejezetten a bizonytalansagot; ne kovetkeztesd ki talalgatassal.
3. Rovid osszefoglaloban sorold fel a relevans viselkedeseket es fuggosegeket.
   Ha a felhasznalo csak elemzest kert, itt allj meg.
4. Hasznald a projekt altal mar alkalmazott tesztkeretrendszert, assert
   konyvtarat, elnevezesi es fixture-mintakat. Ne vezess be uj fuggoseget
   indoklas nelkul.
5. Ird meg a teszteket 3-5 tesztes csoportokban, majd minden csoport utan allj
   meg, hogy a felhasznalo ellenorizhesse az eredmenyt, mielott folytatod.
6. Minden teszt egy viselkedest ellenorizzen. Parameterezett tesztet hasznalj,
   ha tobb adat ugyanazt a szabalyhalmazt ellenorzi.
7. Mockot kulso hatarfeluletre hasznalj; ne mockold a SUT sajat uzleti logikajat.
8. Idofuggo logikahoz a projekt mintaja szerinti fix `Clock`-ot adj meg. A
   Java/Spring oktatasi mintaban JUnit 5 es AssertJ hasznalatos; masik
   projektben a helyi tesztkonvencio az iranyado.
9. API-kontraktus tesztelesekor a kontraktust ellenorizd, ne az implementacio
   belso reszleteit. Kulso szolgaltatast csak a megfelelo hataron stubold.
10. Futtasd a legszukebb relevans tesztparancsot, ha a kornyezet lehetove teszi.
    A sikert vagy hibat a tenyleges futtatas alapjan jelentsd.

## Ellenorizendo esetek

A SUT viselkedese alapjan merlegeld a kovetkezoket: ervenyes alaphelyzet,
hatarertekek, null vagy hianyzo bemenet, ervenytelen ertekek, hiba a
fuggosegben, idozona, kerekites, illetve konkurencia, ha az osztaly allapotot
oszt meg. Csak azokat a viselkedeseket teszteld, amelyek a kovetelmeny vagy
implementacio reszei.

## Kimenet

- Add meg, mely tesztfajlt hoztad letre vagy modositottad.
- A tesztkod utan roviden listazd a lefedett viselkedeseket es a futtatott
  ellenorzest.
- Ha a teszt nem futtathato, nevezd meg a blokkolot; ne allitsd, hogy zold.
