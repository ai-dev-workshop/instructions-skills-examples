---
description: "Use when auditing source code, configuration, dependencies, or REST APIs for common security and governance requirements."
---

# Biztonsagi es REST ellenorzesi szabalyok

Auditkor minden megallapitast egy szabalyazonositohoz es konkret kodhelyhez
kapcsolj. A szabalyok oktatasi mintak; a celprojekt jovahagyott szabalyzata az
iranyado.

## Hitelesito adatok

- **SEC-01** – Jelszo, token, API-kulcs vagy mas hitelesito adat ne keruljon
  forraskodba, konfiguracios fajlba vagy verziozott allomanyba. Hivatkozz
  titokkezelo bejegyzesre vagy titkot nem tartalmazo kornyezeti valtozonevre.
- **SEC-02** – Ne legyen kodban beagyazott hitelesito adat, beleertve a
  tartalekertekkent hasznalt kulcsot vagy tokent is.

## Adatbazis, naplozas es hibavalasz

- **SEC-03** – Felhasznaloi bemenet ne keruljon SQL-utasitasba karakterlanc
  osszefuzesekent. Hasznalj parameterezett lekerdezest vagy a keretrendszer
  megfelelo parameterezeset.
- **SEC-04** – Jelszo, PIN, teljes szamlaszam, egyenleg es mas vedett adat ne
  keruljon naploba. Ha az uzleti cel megkoveteli egy azonosito naplozasat, a
  projekt adatmaszkolo szabalyat alkalmazd.
- **SEC-05** – Kliensnek kuldott hibavalasz ne tartalmazzon stack trace-t,
  kivetelosztalyt vagy belso implementacios adatot. Hasznalj dokumentalt,
  egyseges hibavalasz-formatumot.

## Kriptografia, validacio es fuggosegek

- **SEC-06** – Jelszo tarolasahoz erre a celra keszult, megfeleloen konfiguralt
  jelszohashelo eljarast hasznalj. Elavult, gyors hash-algoritmust ne alkalmazz
  jelszavak vedelmere.
- **SEC-07** – Kliens felol erkezo adatot a feldolgozas elott validalni kell.
- **SEC-08** – Ne hasznalj ismert, javitatlan sebezhetoseget tartalmazo
  fuggosegverziot. A verzioallapotot a projekt altal elfogadott ellenorzessel
  igazold; ne kovetkeztess CVE-erintettsegre pusztan a csomagnev alapjan.

## REST

- **SEC-09** – A publikus REST vegpontok kovessek a projekt API-verziozasi
  konvenciojat.
- **SEC-10** – CORS-beallitasban ne engedelyezz minden origint indokolatlanul;
  hasznalj jovahagyott, kifejezett origin-listat.
- **SEC-11** – Jelszo es mas titkos hitelesitesi adat ne keruljon URL-be vagy
  query parameterbe. Hasznald a megfelelo, titkositott kommunikacioval vedett
  request body-t.

## Audit kimenete

Minden talalathoz add meg:

1. szabalyazonosito;
2. fajl es sor vagy kodhely;
3. sulyossag (KRITIKUS / MAGAS / KOZEPES);
4. rovid indoklas es minimalis javitasi javaslat.

A vegi osszefoglaloban sorold fel a szabalyazonositokat, es jelold azt is,
amelyikre nem talaltal elterest. Ne allits megfeleloseget olyan allomanyokrol,
amelyeket nem vizsgaltal.
