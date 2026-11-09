# Instruction- es skill-mintatar

Oktatasi celra keszult, altalanositott mintacsomag. A pelda egy fiktiv Java/Spring
szolgaltatas konvencioira epul; szervezet-, projekt- es belso rendszerneveket nem
tartalmaz. Atvetel elott igazitsd a sajat technologiai stackhez, fejlesztesi
szabalyokhoz es review-folyamathoz.

## Tartalom

### Instructions

- `instructions/java-project-conventions.instructions.md` – architektura, penzkezeles,
  hibakezeles, konfiguracio, ido es teszteles.
- `instructions/security-governance.instructions.md` – ellenorizheto biztonsagi
  szabalyok es az audit kimeneti formatuma.
- `instructions/engineering-workflow.instructions.md` – tervezes, biztonsagos
  valtoztatas, teszteles es blokkolok kezelese.

### Skills

- `skills/java-code-reviewer/SKILL.md` – taskhoz kotott, rangsorolt kodreview.
- `skills/java-test-generator/SKILL.md` – implementaciobol levezetett, fokozatos
  tesztgeneralo munkamenet.
- `skills/pr-description-generator/SKILL.md` – diff es commitok alapjan keszulo
  PR-leiras.

## Felhasznalas

Ezek tananyagminta-fajlok, nem aktiv projektkonfiguraciok. Copilot workspace-be
illeszteskor az instructionok a `.github/instructions/` ala, a skillek pedig a
`.github/skills/<skill-nev>/SKILL.md` utvonalra masolhatok. Az instructionok
`description` mezoi on-demand betoltest tesznek lehetove; a Java-konvencio pelda
csak Java-fajlokra illeszkedik.

## Atvetel elotti ellenorzes

1. Csereld le a pelda architektura-, nyelv- es tesztkonvencioit a celprojekt valos
   szabalyaira.
2. Egyeztesd a biztonsagi pontokat a jovahagyott szervezeti szabalyzattal; a minta
   nem helyettesit biztonsagi vagy jogi felulvizsgalatot.
3. Ellenorizd, hogy a skill-leirasok, mappanevek es frontmatter mezok egyeznek-e.
4. Proba review-val es tesztgeneralo feladattal ellenorizd, hogy a kimenet a
   kivant formatumot koveti-e.
