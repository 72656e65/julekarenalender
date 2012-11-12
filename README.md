Julekarenalender
=============

De første versjonene av Julekarenalenderen ble utviklet og vedlikeholdt av Arne C. Jervell på NAV Arena prosjektet med Visma Consulting (den gang TietoEnator) som hovedleverandør og Computas som underleverandør. Julekarenalenderen har blitt brukt i mange år på NAV Arena, hvor både leverandør og kunde har fått være med på trekning.

Senere versjoner har blitt vedlikeholdt av Esben Stenwig (Visma Consulting) og Lotta Nordling.

Siste oppdateringer er gjort av Joakim Bjørnstad (Visma Consulting).

Bygging
-----------
* Bygg og pakk applikasjonen med **mvn clean install assembly:single**
* Bygget pakkes som en zip-fil i target mappen

Konfigurasjon
-----------
1. Extract zip-filen i target mappen til ønsket sted
1. Samle sammen bilder som representerer alle i teamet i **jpg** format
1. Endre julekarenalender.csv
  * Filen har 4 semikolon ; separerte kolonner
  * Første kolonne har navnet til deltakeren. Fornavn holder her
  * Andre kolonne har **jpg** bildefilen til deltakeren. Unngå mellomrom
  * Tredje kolonne har hvilken dag vedkommende vant. Denne skal være blank under førstegangskonfigurasjon. Denne kolonnen utelukker at deltakeren kan trekkes etter den dagen.
  * Fjerde kolonne er reservert notater og blir ikke lest av applikasjonen
1. **jpg** bildefiler legges i img undermappen
1. (Valgfritt) Man kan konfigurere de 3 bildene i bonushjulet (det lille hjulet til høyre) ved å legge bilder "bonus0.jpg", "bonus1.jpg" og "bonus_1.jpg" i **img** mappen. På denne måten kan man skreddersy applikasjonen til prosjektet. Hvis ikke disse bildene finnes, vil standard bli brukt:
  * bonus0.jpg overstyrer et bilde av en jokerlue
  * bonus1.jpg overstyrer et bilde av en pakke
  * bonus_1.jpg overstyrer et bilde av Joakim Lystad (NAV direktør)

Bruksanvisning
-----------
1. **Forrige dags vinner** snurrer det store hjulet for å finne en vinner. Dette gjøres ved å ta tak i det store hjulet, hvor man tar tak i det og drar ned i en vertikal bevegelse og slipper. Deltakeren hjulet stopper på er dagens vinner
  * Hvis vedkommende ikke er til stede til å motta gaven, kan det store hjulet snurres på nytt for å finne en annen vinner
1. Når en vinner er funnet for dagen får vedkommende sin gave, samt har anledning til å snurre på bonushjulet
  * På Arena ble bonushjulet brukt til å få bonusgave hvis man fikk bildet av pakken. Her er det åpent for andre ritualer, avhengig av teamet. Det kan være et bilde for gevinst eller "straff"
1. Etter at bonushjulet har landet, blir vinneren for dagen registrert i csv filen. Man får ikke snurre på nytt
1. De som tidligere har fått gave (har fått registert dag nummer i csv filen) blir utelatt i hjulet for videre trekninger