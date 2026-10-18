[ 🌐 عربي ](README.ar.md) | [ 🇩🇪 Deutsch ](README.de.md) | [ 🇫🇷 Français ](README.fr.md) | [ 🇳🇱 Nederlands ](README.nl.md) | [ 🇪🇸 Español ](README.sp.md) | [ 🇬🇧 English ](README.md)
# Voorkom liquiditeitstekorten voordat ze de betaaldatum bereiken

<div align="center">

![License](https://img.shields.io/badge/license-Apache%202.0-blue)
![Platform](https://img.shields.io/badge/platform-Microsoft%20Excel-217346)
![Focus](https://img.shields.io/badge/focus-Operations--Stage%20Business-orange)

**Ontworpen voor bedrijven in consume-goederen, groothandel en productie die toegezegde kasbewegingen, vooruitbetalingsverplichtingen en rollende liquiditeit moeten volgen voordat een tekort ontstaat.**

[Live preview](https://hyvoid.github.io/rolling-cashflow-forecast/) · [Koop de volledige Excel-versie](https://www.theseusworkshop.com/l/16wcashflow?utm_source=github&utm_medium=GitHub%20README&utm_campaign=readme%20new%20launch&utm_content=rolling-16-week-cashflow)

</div>

Volg open orderkasverplichtingen, detecteer liquiditeitsgaten weken vooruit en behoud één vooruitkijkende bron van waarheid voor de kortetermijnkasvatbaarheid.

---

## Snelle preview

<img width="1672" height="941" alt="ChatGPT Image May 25, 2026, 03_53_03 PM" src="https://github.com/user-attachments/assets/d43699bc-4a15-470c-901e-7b372c953861" />

> Bekijk de interactieve werkboekpreview: [16-weeks kasstromendemo](https://hyvoid.github.io/rolling-cashflow-forecast/)

---

## Waarom dit bestaat

De meeste kastekorten in groeiende bedrijven worden niet veroorzaakt door onrendabele operaties.

Ze gebeuren meestal omdat vooruitbetalingen van klanten, mijlpaalonvangsten, toegezegde inkooporders en gestaffelde betalingstermijnen moeilijk handmatig te consolideren zijn — en standaard boekhoudkundige registraties structureel blind voor zijn tot er een factuur wordt gesteld.

Het risico is simpel:

```
Payment due date arrives
-> Manual bank balance check
-> Prior commitments missed
-> Shortfall discovered at the wire
```

Dit werkboek is ontworpen om de workflow te veranderen:

```
New order or supplier PO considered
-> Commitment entered once
-> 16-week cash timeline updated automatically
-> Liquidity gap flagged before it becomes a crisis
```

Het commerciële probleem is niet alleen kasbeheer. Het is operationele zichtbaarheid. Financiële teams en operators moeten weten of het bedrijf zijn volgende verplichting kan dekken — voordat betalingstermijnen worden overeengekomen.

---

## Drie kasvallen die groeiende bedrijven te pakken krijgen

### Val 1 — Maandoverzichten worden verkeerd gelezen als een liquiditeitsbeeld

Standaard AR/AP-rapportages weerspiegelen wat is gefactureerd. Ze weerspiegelen niet wat is toegezegd.

Een bedrijf dat 80.000 dollar aan bevestigde klantdeposito's en 60.000 dollar aan contractuele leveranciersvooruitbetalingen houdt die volgende maand vervallen, toont geen van beide in zijn resultatenrekening tot de goederen bewegen en facturen worden gesteld. Het financiële team ziet vandaag een gezond banksaldo. Het komende tekort is onzichtbaar.

Financiële teams die kas beheren vanuit maandoverzichten werken routineel met een beeld dat structureel vier tot zes weken achter de werkelijkheid loopt. Het mentale model voelt compleet; de data zijn dat niet.

### Val 2 — Vooruitbetalingen en inkooporders worden bijgehouden in gescheiden systemen

Wanneer hetzelfde bedrijf maandag een aanbetaling van 30% van een klant ontvangt en donderdag een leveranciersvooruitbetaling van 40% doet, beïnvloeden beide transacties dezelfde kaspool — maar ze leven doorgaans in verschillende systemen, verschillende spreadsheets of verschillende teams.

Operaties die gescheiden bijhouding voeren voor verkoopverplichtingen en inkoopverplichtingen — een natuurlijke workflowverdeling — zien systematisch niet de nettokaspositie. De regelgeving erkent die operationele grens niet. De bankrekening evenmin.

### Val 3 — Gaten worden ontdekt op de betaaldatum

Handmatige verificatie gebeurt doorgaans wanneer een betaling vervalt of wanneer iemand de bankrekening bekijkt. Tegen de tijd dat een gat wordt geïdentificeerd, is het venster voor actie gesloten. Reactieve antwoorden — noodkredieten, heronderhandelingen met leveranciers, uitgestelde loonbetalingen — dragen echte kosten en echte relatieschade.

Onderschepping vóór het gat vereist dat liquiditeitsrisico weken voor de vervaldatum van de verplichting zichtbaar is — wat vereist dat alle open verplichtingen actueel zijn en alle timingberekeningen automatisch lopen op het moment van planning.

Het gat zit meestal verborgen in de relatie tussen:

- openingskassaldo
- timing van ontvangst van deposito's en vooruitbetalingen
- ontvangstdatums van klantsaldi
- vervaldatums van leveranciersbetalingen
- contractuele betalingstermijnen
- ordervolume en groeisnelheid

Daarom brengt handmatige afstemming het probleem vaak te laat aan het licht — of mist het volledig.

---

## Voor wie dit tool is

| Gebruiker | Praktisch gebruiksscenario |
|---|---|
| Financiële managers | Liquiditeitsgaten 6–16 weken vooruit identificeren voordat ze crises worden |
| Operationele managers | De kasimpact van een nieuwe order of leveranciers-PO begrijpen voordat wordt toegezegd |
| Oprichters en CEO's | Één vooruitkijkend beeld van kasvatbaarheid behouden naarmate het bedrijf schaalt |
| Inkoopteams | Vooruitbetalings-eisen afwegen tegen werkelijk beschikbare liquiditeit |
| Externe accountants | Kortetermijnkasadvies geven zonder een model vanaf nul te bouwen |

Het best geschikt voor bedrijven met gemengde klantvooruitbetalings- en leveranciersvooruitbetalingsstructuren, waar treasurysoftware te kostbaar is maar handmatige benaderingen niet meer schalen.

---

## Wat het werkboek doet

### Loggen van open verplichtingen
Één datainvoerpunt voor alle AR, AP, open verkooporders en open inkooporders. Teams voeren basisinformatie over verplichting en timing eenmaal in; de berekeningen van de kastijdlijn lopen automatisch op de achtergrond.

### 16-weeks kastijdlijn
Automatische mapping van elke open verplichting naar een specifieke week en kasrichting. Het rollende venster werkt elke week bij naarmate nieuwe invoeren worden toegevoegd en vorige weken afsluiten.

### Liquiditeitsstatus vóór de beslissing
Het geprojecteerde kassaldo van elke week is zichtbaar voordat een nieuwe order wordt geaccepteerd of een nieuwe leveranciersvoorwaarde wordt overeengekomen. Geen handmatig kruisverwijzen. Geen ontdekking op de betaaldag.

### Deduplicatielogica
Inkooporders die al naar facturen zijn geconverteerd worden automatisch geïdentificeerd en uitgesloten — zodat elke verwachte kasbeweging precies één keer wordt geteld en het beeld van open verplichtingen schoon blijft.

### Drempellaag voor waarschuwingen
Een minimaal veilig kassaldo wordt door het bedrijf geconfigureerd. Het model benadrukt welke weken de drempel doorbreken en welke specifieke transacties elk gat aandrijven — teams krijgen een diagnose op transactieniveau, niet alleen een rode vlag.

### Auditklare structuur
Elke invoer is vanaf dag één gestructureerd en traceerbaar. Het volledige 16-weeks verplichtingsrecord kan worden gefilterd op richting, tegenpartij of week en bekeken zonder nabewerking.

---

## Voorbeeldscenario

**Bedrijfsprofiel:** Importeur van consume-goederen. Gemengde klantvooruitbetalingsvoorwaarden en leveranciersvooruitbetalingsvereisten. Één financiële functie.

**Het probleem:** Elke week kruist de financiële manager handmatig open verkooporders, openstaande klantdeposito's, hangende leveranciersfacturen en verwachte goedsonvangstdatums om beschikbare kas te schatten. Klantverplichtingen worden bijgehouden in de CRM. Leveranciersverplichtingen worden bijgehouden in het inkoopblad. Beiden afstemmen tot een nettokaspositie kost twee uur en levert een beeld op dat al een week oud is.

Over een kwartaal van operaties werden twee liquiditeitsgaten geïdentificeerd — beide binnen 48 uur na de betaaldatum.

| | Voor | Na |
|---|---|---|
| Verplichtingsstructuur | Twee gescheiden bladen, één per team | Één uniform werkboek |
| Wekelijkse kascontroletijd | ~2 uur over alle open posities | Minder dan 5 minuten per week |
| Consolidatie van vooruitbetalingen | Handmatige kruisverwijzing | Automatisch over AR, AP, verkooporders, PO's |
| Gatersontdekking | Op de betaaldatum; reactief antwoord | 6–8 weken vooruit; gepland antwoord |

**Het specifieke keerpunt dat deze tool aan het licht brengt:**

Een klantorder van 100.000 dollar draagt een saldo van 70% dat vóór verzending vervalt, geschat week 6. De gerelateerde leveranciers-PO draagt een saldo van 60% dat vervalt bij ontvangst van de goederen, geschat week 5. Openingskassaldo: 10.000 dollar.

Netto positie week 5: 10.000 − 30.000 = **−20.000.** Er is een gat.
Netto positie week 6: −20.000 + 70.000 = **50.000.** Opgelost.

Een maandbeeld laat de maand netto-positief zien. Het weekvenster laat een echt tekort van 20.000 in week 5 zien dat actie vereist voordat het arriveert — niet erna.

---

## Waarom kortetermijnkasprognoses op deze manier werken

Rollende kasstroomprognoses — directe methode, korte vooruitblikkende horizon — zijn een standaard treasurydiscipline die door de meeste grote bedrijven als kernoperationele functie wordt onderhouden. In grotere bedrijven wordt het beheerd door dedicated treasuryfuncties met specialistische software.

De directe methode werkt door werkelijke verwachte kasbewegingen — geen boekhoudkundige boekingen — toe te wijzen aan specifieke datums. Elke toegezegde in- en uitstroom wordt vertaald naar een week, een richting en een bedrag. Het lopende saldo op elk moment weerspiegelt wat het bedrijf werkelijk verwacht te houden, niet wat zijn boekhoudkundige registraties laten zien.

Deze benadering is structureel onderscheiden van:

- **Op P&L gebaseerde kasschatting** — verwart rentabiliteit met liquiditeit; een bedrijf kan tegelijkertijd rendabel en illiquide zijn
- **Banksaldobeheer** — weerspiegelt alleen wat al is bewogen; toegezegde toekomstige uitstromen zijn onzichtbaar
- **Maandelijkse AR/AP-rapportage** — sluit voorfactuurverplichtingen volledig uit; systematisch blind voor de operationele laag

De reden dat de meeste groeiende bedrijven dit beeld missen is niet complexiteit. Het is de afwezigheid van een gestructureerd mechanisme om operationele verplichtingen — die over verkoop, inkoop en financiën verdeeld leven — te consolideren in één kastijdlijn.

Nuttige referentiecontext:
- [AICPA: Direct Method Cash Flow Forecasting](https://www.aicpa.org)
- [AFP: Treasury Management Fundamentals](https://www.afponline.org)

---

## Hoe het 16-weeks venster werkt

Het 16-weeks venster schuift elke week vooruit, niet elke maand. Elke nieuwe invoer wordt toegewezen aan een specifieke toekomstige week op basis van geschatte operationele datums en contractuele betalingstermijnen.

| Operationele invoer | Afgeleide kasgebeurtenis |
|---|---|
| Geschatte verzenddatum + voorwaarde "betaling vóór verzending" | Klantontvangst in de week vóór de geschatte verzending |
| Geschatte goedsonvangstdatum + voorwaarde "betaling bij levering" | Leveranciersuitstroom in de geschatte ontvangstweek |
| Factuurdatum + voorwaarde "Net 30" | Klantontvangst ongeveer 4 weken vooruit |

**De val in cijfers:**

Een bedrijf dat 10 open orders tegelijk runt — elk met eigen stortingsstructuur, saldobetalingstiming en leveranciersvooruitbetalingsschema — draagt op elk moment meer dan 30 interacterende kasgebeurtenissen. Elke gebeurtenis hangt af van een actuele operationele schatting om accuraat te blijven. Handmatige consolidatie introduceert bij elke stap fouten.

Het maandelijkse reset-mentale model keurt posities goed die het rollende weekvenster niet goedkeurt. De berekening is structureel, niet subjectief. Automatisering elimineert die foutklasse volledig.

**Waarom de betrouwbaarheid van de prognose aan de buitenhorizon vervaagt:** De nabije horizon van weken 1–8 is bevolkt met verplichtingen die al in beweging zijn — verzenddatums en betalingstermijnen die bevestigd of bijna bevestigd zijn. Weken 9–16 hangen af van operationele schattingen die materieel kunnen verschuiven naarmate orders worden geplaatst of vertraagd. Het model is het meest betrouwbaar binnen de 6–8 weekse nabije horizon. Het buitenvenster is directioneel nuttig voor planning; het is geen garantie.

---

## Werkboeklogica

Het werkboek is georganiseerd rond een praktische kasplanningworkflow:

1. Voer alle open AR, AP, verkooporders en inkooporders in met geschatte datums en betalingstermijnen.
2. Pas deduplicatie toe om inkooporders die al naar facturen zijn geconverteerd te identificeren en uit te sluiten.
3. Wijs elke open verplichting toe aan zijn verwachte kasweek en richting.
4. Bereken het lopende 16-weeks saldo vooruit vanaf de openingskaspositie.
5. Vergelijk het geprojecteerde saldo van elke week met de minimaal veilige drempel.
6. Markeer gatweken en identificeer de specifieke transacties die elk gat aandrijven.
7. Bewaar het verplichtingsrecord voor wekelijkse rollende review en teamcommunicatie.

Het werkboek is bedoeld als een beslissingsondersteunings- en planningsinstrument. Het vervangt geen boekhoudsoftware, auditeerbare financiële registraties of professioneel advies voor complexe financieringsbeslissingen.

---

## Aankoop

Gebruik hier het volledige Excel-werkboek:

[Koop het volledige Excel-werkboek →](https://www.theseusworkshop.com/l/16wcashflow?utm_source=github&utm_medium=GitHub%20README&utm_campaign=readme%20new%20launch&utm_content=rolling-16-week-cashflow)

---

## Beperkingen

- **Invoerafhankelijkheid** — de nauwkeurigheid van de prognose wordt begrensd door de kwaliteit van de ingevoerde data; verouderde verzendschattingen of ontbrekende verplichtingen produceren zonder waarschuwing een vals gevoel van zichtbaarheid
- **Handmatige verversing vereist** — het model werkt niet automatisch bij; zonder consistente wekelijkse onderhoud degradeert het rollende venster en worden gaten weer onzichtbaar
- **Geen systeem van record** — dit is een beslissingsondersteuningslaag; het vervangt geen boekhoudsoftware, geen ERP of auditeerbare financiële registraties
- **Deterministisch, niet probabilistisch** — elke kasgebeurtenis wordt gemodelleerd als een vaste datum en een vast bedrag; betalingsvertragingsrisico, valutabewegingen en orderannuleringsscenario's vereisen een handmatige overlay
- **Betrouwbaarheid buitenhorizon** — weken 10–16 hangen af van operationele schattingen die materieel kunnen verschuiven; het model is het meest betrouwbaar binnen de 6–8 weekse nabije horizon
- **Multi-currency niet gemodelleerd** — bedrijven met significante valutablootstelling moeten wisselkoersaannames als handmatige overlay toepassen
- **Schaalcontext** — ontworpen voor bedrijven die 5–50 gelijktijdige open posities beheren; daarbuiten vereist het handmatige invoermodel structurele aanpassing

---

## Over dit project

Dit werkboek maakt deel uit van een bredere inspanning om complexe operationele en financiële vereisten te vertalen naar lichtgewicht tools die kleine en middelgrote organisaties echt kunnen gebruiken.

Geen ERP. Geen treasurysoftware-abonnement. Geen maatwerkontwikkelingsproject.

Alleen heldere bedrijfslogica, gestructureerde data en herhaalbare beslissingsondersteuning — geleverd in software die je team al heeft.

Als jouw operatie kasbeheer, inkoopcycli of klantfactureringsstructuren omvat die nu in het hoofd van iemand of in een losgekoppeld spreadsheet leven, [bekijk wat er nog meer beschikbaar is →](https://www.theseusworkshop.com)

---

## Licentie

Gedistribueerd onder de [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0).
