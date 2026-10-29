[ 🌐 عربي ](README.ar.md) | [ 🇩🇪 Deutsch ](README.de.md) | [ 🇫🇷 Français ](README.fr.md) | [ 🇳🇱 Nederlands ](README.nl.md) | [ 🇪🇸 Español ](README.sp.md) | [ 🇬🇧 English ](README.md)

# Excel-sjabloon voor een 16-weekse doorlopende kasstroomprognose: liquiditeitsplanner volgens de directe methode, tracker van PO-verbintenissen & werkkapitaalmodel

<div align="center">

![License](https://img.shields.io/badge/license-Apache%202.0-blue)
![Platform](https://img.shields.io/badge/platform-Microsoft%20Excel-217346)
![Focus](https://img.shields.io/badge/focus-Working%20Capital%20%26%20Treasury-orange)

**Een spreadsheet voor een 16-weekse doorlopende kasstroomprognose volgens de directe methode, gebouwd in Microsoft Excel voor groothandel-, import/export-, e-commercevoorraad- en productiebedrijven die openstaande inkooporders (PO's), leveranciersvooruitbetalingen, klantdeposito's en kortetermijnwerkkapitaal beheren.**

[Bekijk de demo van de interactieve simulator voor de 16-weekse doorlopende kasstroom](https://hyvoid.github.io/rolling-cashflow-forecast/) ·

[Download het volledige Excel-werkboek voor de 16-weekse doorlopende kasstroomprognose](https://www.theseusworkshop.com/l/16wcashflow?utm_source=github&utm_medium=GitHub%20README&utm_campaign=readme%20new%20launch&utm_content=rolling-16-week-cashflow)

</div>

Het **16-Week Rolling Cash Flow Forecast Workbook** is een geautomatiseerde **Microsoft Excel-planner voor kortetermijnliquiditeit** en een **kas-tracker voor open verbintenissen**. Het gaat verder dan standaard **13-weekse kasstroommodellen** door de volledige levertijden van 110 dagen voor voorraad en productie te dekken, en consolideert **debiteuren (AR)**, **crediteuren (AP)**, **niet-gefactureerde verkooporders (SO)** en **toegezegde inkooporders (PO)** in één wekelijkse kas-tijdlijn — met signalering van werkkapitaaltekorten en doorbraken van de minimale cashbuffer weken vóór de vervaldatums van betalingen.

---

## Visuele preview: 16-weekse kas-tijdlijn & drempelwaarschuwingsdashboard

<img width="1672" height="941" alt="16-Week Rolling Cash Flow Forecast Excel Template showing weekly cash inflows, supplier PO prepayments, net liquidity balance, and shortfall alerts" src="https://github.com/user-attachments/assets/d43699bc-4a15-470c-901e-7b372c953861" />

> Test de wekelijkse verbintenismapping en de drempelwaarschuwingen voor liquiditeit in je browser: [Interactieve demo van de 16-weekse kasstroomprognose volgens de directe methode](https://hyvoid.github.io/rolling-cashflow-forecast/)

---

## Waarom accrual-boekhouding geen kortetermijnkastekorten voorkomt

Winstgevende groothandel-, productie- en fysieke productbedrijven ondervinden routinematig acute liquiditeitsproblemen tijdens groeifasen. Deze kastekorten ontstaan doordat **klantdeposito's**, **mijlpalenfacturering over de voortgang**, **contractuele leveranciersvooruitbetalingen** en **gestaffelde Net 30/60/90-betaalvoorwaarden** weken vóór het moment plaatsvinden waarop een boekhoudkundige factuur ooit op de algemene grootboek wordt geboekt.

**De reactieve workflow rond banksaldo & AR/AP (hoog risico op wanbetaling):**

```text
Supplier wire due date arrives
-> Finance checks current bank balance and billed AP aging
-> Unbilled PO prepayments and freight commitments overlooked
-> Working capital shortfall discovered 48 hours before wire deadline

```

**De proactieve 16-weekse workflow voor verbintenissenprognoses (controle vóór de beslissing):**

```text
New customer order or supplier Purchase Order (PO) proposed
-> Prepayment and balance milestones logged once in the commitment ledger
-> 16-week rolling cash flow timeline updates automatically
-> Liquidity gap and minimum buffer breach flagged 6–12 weeks in advance

```

Financiële managers, controllers en operationele leidinggevenden hebben zicht op liquiditeit nodig vóórdat beslissingen vallen. Voordat een leveranciersinkooporder wordt ondertekend of Net 60-voorwaarden aan een groothandelafnemer worden verleend, moeten operators verifiëren dat het wekelijkse cash-dal boven de minimale operationele kasreserve van het bedrijf blijft.

---

## De bedrijfslogica & methodologie: verbintenissenprognoses volgens de directe methode

Dit werkboek lost het **probleem van werkkapitaalblindheid vóór facturatie** op door **doorlopende kasstroomprognoses volgens de directe methode** te combineren met **ontdubbeling van verbintenissen van order tot factuur**.

### Het commerciële probleem: de timingkloof tussen accrual en kas in fysieke toeleveringsketens

Standaard boekhoudsoftware (QuickBooks, Xero, NetSuite GL) erkent financiële gebeurtenissen pas wanneer een **verkoopfactuur** of **inkoopfactuur** wordt uitgegeven. In productie-, groothandelsdistributie- en importactiviteiten is het geld echter al juridisch toegezegd op het **orderniveau**:

1. **Kasuitstromen bij inkoop:** Een fabriek eist een aanbetaling van 30% bij het uitgeven van de inkooporder (PO) en een saldo van 70% bij de vrachtbrief (B/L) of de aankomst in het magazijn — weken voordat een formele AP-inkoopfactuur wordt geboekt.
2. **Kasinstromen uit verkoop:** Een B2B-klant betaalt een aanbetaling van 25% bij bevestiging van de verkooporder (SO) en de resterende 75% vóór verzending of op basis van Net 30/60-voorwaarden na levering.
3. **Waarom 16 weken beter is dan standaard 13-weekse modellen:** Een standaard 13-weekse (90-daagse) kasprognose voor bedrijven eindigt precies vóórdat een productierun van 60 dagen plus 30 dagen zeetransport plus de incasso van de klant op Net 30-basis is afgerond. Door het doorlopende venster uit te breiden naar **16 weken (112 dagen)** wordt de volledige kasconversiecyclus vastgelegd, van de eerste PO-aanbetaling tot de laatste klantincasso.

### De kernmethodologie: deterministische kasmapping in drie fasen

In plaats van kas te projecteren op basis van gemiddelden uit de omzetregel van de P&L, voert het werkboek een deterministische berekening in drie fasen uit over een schuivend venster van 16 weken ($t \in [1, 16]$):

1. **Ontdubbelingsengine van verbintenis naar factuur:**

$$\text{Active Cash Events} = \{ \text{Billed AR} \} \cup \{ \text{Billed AP} \} \cup \{ \text{Open SOs} \setminus \text{Invoiced SOs} \} \cup \{ \text{Open POs} \setminus \text{Billed POs} \}$$



*Bedrijfseffect:* Zodra een inkooporder in je boekhoudsysteem is omgezet in een formele leveranciersfactuur, sluit de ontdubbelingsvlag de oorspronkelijke PO-regel uit, zodat de kasuitstroom nooit dubbel wordt meegeteld.
2. **Vertaling van mijlpalen naar datumoffsets:**
Elke actieve verbintenis wordt opgesplitst in discrete kasfasen (bijv. aanbetalingstranche + saldostranche) die op basis van operationele triggerdatums (orderdatum, geschatte verzenddatum, geschatte aankomstdatum of factuurdatum) plus contractuele betaalvoorwaarden ($\Delta \text{Days}$) aan doelweken op de kalender worden toegewezen.
3. **Evaluatie van doorlopende wekelijkse liquiditeit & bufferdoorbraken:**

$$\text{Ending Cash}_{w} = \text{Opening Cash}_{w} + \sum \text{Committed Inflows}_{w} - \sum \text{Committed Outflows}_{w}$$


$$\text{Liquidity Variance}_{w} = \text{Ending Cash}_{w} - \text{Minimum Safe Cash Threshold}$$



*Bedrijfseffect:* Elke week waarin $\text{Ending Cash}_{w} < \text{Minimum Safe Cash Threshold}$ geldt, activeert onmiddellijk een visuele waarschuwing en isoleert de exacte PO of de vertraagde AR-regel die het cash-dal in het werkkapitaal veroorzaakt.

---

## Drie werkkapitaalvalkuilen in handmatige kasstroomspreadsheets

### Valkuil 1: Vertrouwen op maandelijkse P&L- en gefactureerde AR/AP-verouderingsrapportages voor liquiditeit

Standaard verouderingsrapportages voor debiteuren en crediteuren tonen alleen **gefactureerde transacties**.

Denk aan een importeur die $80,000 aan niet-gefactureerde klantorderdeposito's aanhoudt en volgende maand wordt geconfronteerd met $60,000 aan contractuele fabriekssaldobetalingen bij de aankomst van de container. Geen van beide verplichtingen verschijnt op de P&L of in het standaard AP-verouderingsrapport totdat de voorraad is aangekomen en de leveranciersfacturen zijn ingevoerd. Wie de wekelijkse treasury beheert op basis van maandelijkse accrualoverzichten, blijft met het financiële team vier tot zes weken achter de werkelijke kasverbintenissen aan.

### Valkuil 2: Gescheiden tracking tussen verkooporders (CRM) en inkooporders (inkoop)

Wanneer het verkoopteam maandag een klantdeposito van 30% accepteert en het inkoopteam donderdag een leveranciersvooruitbetaling van 40% toezegt, putten beide acties uit dezelfde operationele bankrekening. Toch leven verkoopverbintenissen bij de meeste mkb-bedrijven in een CRM of orderblad, terwijl leveranciers-PO's in een aparte inkooptracker staan.

Het bijhouden van losse spreadsheets voor klantinstromen en leveranciersuitstromen verhindert dat operators de **netto wekelijkse kaspositie** zien wanneer leverdatums zelfs maar één week verschuiven.

### Valkuil 3: Cash-dalen binnen de maand die verborgen zitten in positieve maandtotalen

Een maandelijks kasstroomoverzicht kan op maandafsluiting een gezond positief netsaldotonen, terwijl zich erin een fatale meerdaagse roodstand verbergt in week 2 of week 3.

Wekelijkse kastekorten ontstaan uit de timingmismatch tussen zes operationele variabelen:

* Openingsaldo van de operationele bankrekening
* Ontvangstdatums van klantdeposito's en mijlpalen
* Incassovoorwaarden voor het laatste klantsaldo (bijv. Vóór verzending vs. Net 30)
* Datums van leveranciers-PO-vooruitbetalingen en overboekingen bij goederenontvangst
* Uitgaven voor vracht, invoerrechten en douaneafhandeling
* Versnelling van ordervolumes tijdens piekseizoenopbouwen

Door elke verbintenis toe te wijzen aan een specifieke emmer van 7 dagen komen cash-dalen binnen de maand bloot te liggen, terwijl je nog 6 tot 10 weken hebt om over leveranciersvoorwaarden te onderhandelen, klantincasso's te versnellen of een doorlopend krediet aan te boren.

---

## Voor wie dit Excel-sjabloon voor een 16-weekse doorlopende kasstroomprognose bedoeld is

Ontworpen voor operationele financiële teams en bedrijfseigenaren die **treasuryprognoses volgens de directe methode in Microsoft Excel** nodig hebben zonder de kosten van enterprise-TMS-software:

| Rol & zoekpersoon | Specifiek operationeel scenario & sjabloonuse case |
| --- | --- |
| **Financiële managers & controllers** *(Excel-sjabloon voor 16-weekse / 13-weekse kasstroomprognose)* | Vervang handmatige bankafstemmingen op vrijdag door een doorlopende 16-weekse liquiditeitsprognose volgens de directe methode die bufferdoorbraken 6–12 weken van tevoren signaleert. |
| **Supply chain- & operationeel directeuren** *(kasstroom van inkooporders & tracker voor vooruitbetalingen)* | Simuleer de exacte wekelijkse kasimpact van het plaatsen van een grote seizoens-PO bij een fabriek of het uitstellen van een verzenddatum vóór het ondertekenen van leverancierscontracten. |
| **Oprichters & CEO's met zware voorraad** *(werkkapitaal- & runwayprognose-spreadsheet)* | Onderhoud één vooruitkijkend dashboard van de netto operationele liquiditeit tijdens snelle SKU-uitbreiding, groothandelsafwikkeling en voorraadopbouwcycli. |
| **Inkoop- & aanschafteamleads** *(planner voor leveranciersaanbetalingen & betaalvoorwaarden)* | Weeg eisen voor leveranciersvooruitbetalingen (bijv. 30/70- vs. 50/50-splitsvoorwaarden) af tegen de werkelijk geprojecteerde wekelijkse kasbeschikbaarheid. |
| **Interim-CFO's & adviserende CPA's** *(kortetermijntreasury- & turnaroundkasmodel)* | Zet een gestandaardiseerd, audit-klaar wekelijks kasstroombeheersinstrument in voor mkb-klanten met krap werkkapitaal of rapportagecovenants van kredietverstrekkers. |

---

## Praktijkgevallen: scenario's rond werkkapitaal & liquiditeit vóór facturatie oplossen

### Scenario A: Import-/export- & groothandelsdistributeurs met 30/70-fabrieksvooruitbetalingen

Importeurs betalen routinematig 30% bij het plaatsen van de PO en 70% bij de vrachtbrief of aankomst in de haven, terwijl groothandel- en retailafnemers Net 30 of Net 60 betalen na magazijnlevering. Door open PO's en groothandel-SO's vast te leggen in de **16-weekse kas-tijdlijn** ziet de controller het exacte werkkapitaal-cash-dal van 4 tot 8 weken tussen het betalen van de overzeese fabriek en het incasseren bij de binnenlandse retailer.

### Scenario B: Contractfabrikanten & bouwers van maatwerkapparatuur die mijlpalenfacturering volgen

Fabrikanten die meerfasenopdrachten draaien, incasseren voortgangsbetalingen van klanten (bijv. 40% aanbetaling, 30% bij subassemblage, 30% vóór verzending) terwijl ze vooraf grondstoffen inkopen. Wanneer een productiemijlpaal twee weken opschuift, verschuift het bijwerken van de geschatte verzenddatum in het werkboek automatisch de stroomafwaartse kasinstroom van de klant en wordt zichtbaar of de betalingen voor grondstoffen de minimale kasreserve zullen doorbreken.

### Scenario C: Interim-CFO's die wekelijkse kaswar-rooms draaien & covenantrapportage voor kredietverstrekkers

Tijdens werkkapitaalturnarounds of seizoensopnames op de kredietlijn eisen banken en managementteams een transparante wekelijkse directe kasprognose (vaak gevraagd als een rapport van 13 of 16 weken doorlopende kasstroom). Dit sjabloon biedt drill-downs op transactieniveau die precies laten zien welke klantfacturen en leveranciers-PO's de netto kasstroom van elke week aandrijven.

---

## Wat het werkboek bijhoudt: mapping van pijnpunt naar oplossing

| Pijnpunt in treasury & kasbeheer | Veelgezocht zoekvereiste | Ingebouwde oplossing van het Excel-werkboek |
| --- | --- | --- |
| **Niet-gefactureerde PO's ontbreken in kasprognoses** | *Open inkooporders opnemen in kasstroomprognose in Excel* | **Uniform register van open verbintenissen:** Legt gefactureerde AR, gefactureerde AP, niet-gefactureerde verkooporders en openstaande inkooporders vast in één gestructureerde invoertabel. |
| **Dubbel tellen van PO's na facturatie** | *Dubbele PO- en factuurregistraties in kasprojectie voorkomen* | **Geautomatiseerde ontdubbeling van PO naar factuur:** Identificeert en sluit inkooporders uit die al zijn omgezet in formele AP-facturen, zodat elke dollar precies één keer wordt geteld. |
| **Roodstanden binnen de maand & onverwachte tekorten** | *Sjabloon voor wekelijkse doorlopende kasstroomprognose met waarschuwingen bij laag kassaldo* | **Configureerbare drempelwaarschuwingslaag:** Vergelijkt de geprojecteerde weekafsluitende kas met je eigen Minimale Veilige Kassaldo en markeert overtredingsweken in realtime. |
| **Verouderde verzend- & leveringsschattingen** | *Dynamisch kasstroommodel op basis van verzenddatums en betaalvoorwaarden* | **Geautomatiseerde mapping van voorwaarde naar week:** Vertaalt operationele datums (geschatte verzenddatum, aankomstdatum, factuurdatum) en betaalvoorwaarden naar exacte wekelijkse kas-emmers. |
| **Trage goedkeuringscontroles vóór toezegging** | *Kasimpact van een nieuwe leveranciersinkooporder testen vóór de aankoop* | **Liquiditeitssandbox vóór de beslissing:** Voer een voorgestelde PO of klantorder in en zie onmiddellijk of de nieuwe verbintenis 6–16 weken verderop een kastekort creëert. |

---

## Casestudy: maandelijkse accrualblindheid vs. zicht op 16 weken doorlopende kas

**Bedrijfsprofiel:** Importeur van consumentengoederen met een jaaromzet van $2M–$10M, actief met gemengde klantdepositovoorwaarden, overzeese leveranciersvooruitbetalingsschema's en een slank financiële team met één manager.

**Waar het operationeel misging:** Elke week besteedde de financiële manager twee uur aan het kruisverwijzen van CRM-verkooporders, ontvangen klantdeposito's, open fabrieks-PO's en vrachtaankomstschema's over losse spreadsheets. Ondanks een positieve maandelijkse netto kasstroom op papier kreeg het bedrijf in één kwartaal twee noodgevallen van kastekort — beide ontdekt minder dan 48 uur voordat de internationale leveranciersoverboekingen vervielen.

### Vergelijking: losse AR/AP-spreadsheets vs. geautomatiseerd 16-weeks verbintenissenmodel

| Treasuryoperatie | Handmatige losse spreadsheets (voor) | Geautomatiseerd werkboek voor 16-weekse doorlopende kasstroom (na) |
| --- | --- | --- |
| **Data-architectuur van verbintenissen** | Gescheiden CRM-verkoopbladen, inkoop-PO-trackers en AR/AP-exporten uit de boekhouding | **Eén uniform verbintenissenregister** met AR, AP, open SO's en open PO's, inclusief ontdubbeling |
| **Voorbereidingstijd van de wekelijkse prognose** | ~2 uur handmatige VLOOKUP's en datumkruisverwijzingen elke vrijdag | **Minder dan 5 minuten per week**; het doorlopende 16-weekse venster wordt dynamisch bijgewerkt zodra datums worden ingevoerd |
| **Zicht op vooruitbetalingen vóór facturatie** | Blind voor leveranciersaanbetalingen en mijlpaalsaldi totdat leveranciersfacturen worden geboekt | **Volledige mijlpaalmapping** over aanbetalingstranches, betalingen vóór verzending en leveringsoverboekingen |
| **Detectievenster van liquiditeitstekorten** | Ontdekt 24–48 uur vóór de vervaldatum van de overboeking (gedwongen noodkredietopnames) | **6–12 weken van tevoren gesignaleerd** via geautomatiseerde waarschuwingen bij het doorbreken van de minimale kasdrempel |

### Het exacte kantelpunt dat dit werkboek blootlegt

Denk aan een **klantenverkooporder van $100,000** en de gekoppelde **leveranciersinkooporder van $50,000**, startend vanaf een **openingskassaldo van $10,000**:

* **Leveranciers-PO-saldo ($30,000 uitstroom):** 60% vervalt bij goederenontvangst in **week 5**.
* **Klant-SO-saldo ($70,000 instroom):** 70% vervalt vóór magazijnverzending in **week 6**.

| Rapportagegranulariteit | Nettokaspositie week 5 | Nettokaspositie week 6 | Operationele conclusie |
| --- | --- | --- | --- |
| **Traditioneel maandelijks kasoverzicht** | *Verborgen in het maandtotaal* | **+$50,000 kas op maandafsluiting** | Vals groen licht; de financiële afdeling keurt voorwaarden goed zonder de wanbetaling halverwege de maand te zien |
| **16-weeks doorlopend weekmodel** | **−$20,000 kastekort** ($10K − $30K) | **+$50,000 herstel** (−$20K + $70K) | **Signaleert het week 5-tekort van $20,000 5 weken van tevoren**, zodat het team de leveranciersoverboekingsvoorwaarden kan afstemmen op de klantontvangst |

---

## Treasurynormen achter doorlopende kasprognoses volgens de directe methode

Treasuryteams van bedrijven vertrouwen op **kortetermijn-doorlopende kasstroomprognoses volgens de directe methode**, omdat accrual-resultatenrekeningen winstgevendheid meten in plaats van kasliquiditeit. Snel groeiende productbedrijven genereren vaak sterke boekhoudkundige marges terwijl ze door de timing van voorraadvooruitbetalingen zonder operationele kas komen te zitten.

De directe methode omzeilt accrual-aanpassingen en wijst **100% van de verwachte bruto kasontvangsten en bruto kasuitgaven** toe aan specifieke wekelijkse emmers:

| Traditionele rapportagemethode | Structurele beperking in de operatie | Hoe het 16-weekse directe-methode-model dit oplost |
| --- | --- | --- |
| **Indirecte kasschatting via P&L** | Vermengt boekhoudkundige nettowinst met liquide bankmiddelen; verbergt werkkapitaalpieken binnen de maand | Wijst **werkelijke gedateerde kasontvangsten en overboekingsuitgaven** week voor week toe |
| **Dagelijkse controle van het banksaldo** | Puur achteruitkijkend; toont vereffende kas terwijl $100K+ aan toegezegde komende PO-overboekingen wordt genegeerd | Projecteert **vooruitlopende kassaldi** over de komende 16 opeenvolgende weken |
| **Maandelijkse AR/AP-verouderingsrapportages** | Sluit niet-gefactureerde inkooporders en klantmijlpalen vóór verzending uit | Integreert **ordertoezeggingen vóór facturatie** naast gefactureerde debiteuren en crediteuren |

**Geraadpleegde gezaghebbende treasury- & kasbeheerraamwerken:**

* [AICPA: kasstroomprognoses volgens de directe methode & werkkapitaalbeheer](https://www.aicpa-cima.com)
* [Association for Financial Professionals (AFP): normen voor kortetermijntreasury & doorlopende kasprognoses](https://www.afponline.org)

---

## Hoe de doorlopende horizon van 16 weken & de datumoffsetmapping werken

De prognosehorizon van 16 weken schuift week na week vooruit. Elke open order of factuur wordt aan een specifieke toekomstige kasweek toegewezen door de **operationele mijlpaaldatum** te combineren met de **contractuele betaalvoorwaarde**:

| Operationele mijlpaalinvoer | Contractuele betaalvoorwaarde | Afgeleide wekelijkse kasstroomgebeurtenis in het model |
| --- | --- | --- |
| **Geschatte verzenddatum van de klant** | *Saldo vervalt vóór verzending* | **Kasinstroom (ontvangst)** toegewezen aan de week onmiddellijk vóór de geschatte verzending |
| **Geschatte aankomstdatum van de goederen (ETA)** | *Saldo vervalt bij levering / aankomst* | **Kasuitstroom (leveranciersoverboeking)** toegewezen aan de geschatte aankomstweek in het magazijn/de haven |
| **Uitgiftedatum van de klantfactuur** | *Krediettermijn van Net 30 dagen* | **Kasinstroom (ontvangst)** toegewezen 4 weken vooruit vanaf de factuurdatum |

**Waarom de prognosenauwkeurigheid splitst tussen de nabije horizon (weken 1–8) en de buitenhorizon (weken 9–16):**

* **Weken 1–8 (uitvoeringsvenster met hoge betrouwbaarheid):** Gedreven door bevestigde facturen, vastgelegde scheepvaartschema's en actieve inkooporders die al in productie zijn. Gebruikt voor strakke betalingsschema's, goedkeuringen van overboekingen en beslissingen over kredietlijnopnames.
* **Weken 9–16 (venster voor strategische planning & inkoop):** Gedreven door geschatte productielevertijden en verkooporders in de pijplijn. Gebruikt om te stresstesten of nieuwe leveranciers-PO's kunnen worden gefinancierd uit de interne kasstroom voordat contracten worden getekend.

---

## Snelle start: hoe je in 7 stappen je 16-weekse doorlopende kasstroomprognose bouwt

Volg deze stapsgewijze workflow om je financiële en operationele team van reactieve banksaldocontroles naar proactief 16-weeks liquiditeitsbeheer te brengen:

1. **Test verbintenissscenario's in de interactieve browserdemo**
Open de [interactieve websimulator voor de 16-weekse doorlopende kasstroom](https://hyvoid.github.io/rolling-cashflow-forecast/) om te ontdekken hoe open PO's, klantdeposito's en verzendvertragingen de wekelijkse kas saldi in realtime verschuiven.
2. **Configureer het openingskassaldo en de minimale veilige cashbuffer**
Voer je huidige operationele banksaldo in, definieer je startprognosedatum op maandag en stel de **Minimale Veilige Kasdrempel** van je bedrijf in (bijv. $25,000 of 1 maand vaste loonkosten/opex).
3. **Leg gefactureerde debiteuren (AR) en crediteuren (AP) vast**
Voer openstaande klantfacturen en leveranciersfacturen in met hun contractuele vervaldatums om je basis-kas-tijdlijn na facturatie vast te leggen.
4. **Voer niet-gefactureerde verkooporders (SO) en openstaande inkooporders (PO) in**
Registreer bevestigde klantorders en actieve leveranciers-PO's samen met aanbetingspercentages, saldospercentages, geschatte verzend-/aankomstdatums en betaalvoorwaarden.
5. **Voer de geautomatiseerde ontdubbeling van PO naar factuur uit**
Markeer of koppel inkooporders die al door leveranciers zijn gefactureerd, zodat de ontdubbelingsengine ze uit de open verbintenissen sluit en dubbeltelling voorkomt.
6. **Bekijk wekelijkse drempeloverschrijdingswaarschuwingen en diagnoseer cash-dalen**
Doorloop de 16-weekse kas-tijdlijn om elke week onder je minimale buffer te vinden, filter vervolgens de verbintenistabel op dat weeknummer om de exacte leveranciers-PO of de vertraagde klantincasso te identificeren die het gat veroorzaakt.
7. **Standaardiseer je wekelijkse kasreview met het herbruikbare Excel-werkboek**
Zodra je de logica in de webpreview van één sessie hebt getest, **[download je het volledige, herbruikbare Excel-sjabloon voor de 16-weekse doorlopende kasstroom](https://www.theseusworkshop.com/l/16wcashflow?utm_source=github&utm_medium=GitHub%20README&utm_campaign=readme%20new%20launch&utm_content=rolling-16-week-cashflow)** om je lopende bedrijfsgegevens op te slaan, de tracking van tegenpartijen aan te passen en je wekelijkse liquiditeitsreview van 5 minuten offline in Microsoft Excel uit te voeren.

*Disclaimer: dit werkboek is een model voor operationele kasplanning en beslissingsondersteuning. Het vult — in plaats van vervangt — formele GAAP/IFRS-boekhoudsoftware, gecontroleerde jaarrekeningen en gelicentieerd treasury- of financieringsadvies aan.*

---

## Download het volledige Excel-sjabloon

Klaar om onverwachte tekorten op betaaldatums te elimineren en je AR, AP en open orderverbintenissen in één doorlopende tijdlijn te verenigen?

👉 **[Download het volledige Excel-werkboek voor de 16-weekse doorlopende kasstroomprognose](https://www.theseusworkshop.com/l/16wcashflow?utm_source=github&utm_medium=GitHub%20README&utm_campaign=readme%20new%20launch&utm_content=rolling-16-week-cashflow)**

---

## Technische reikwijdte & operationele beperkingen

* **Afhankelijkheid van actuele data:** De prognosenauwkeurigheid hangt af van actuele operationele schattingen; niet-geregistreerde leveranciers-PO's of verouderde vrachtaankomstdatums onderschatten of verstoren de wekelijkse kasuitstromen.
* **Wekkelijks doorlopend onderhoudsritme:** Ontworpen voor een wekelijkse verversing van 5 minuten (openingskas bijwerken, de startdatum vooruitschuiven en verschoven verzend-ETA's bijstellen).
* **Beslissingsondersteuningslaag (geen boekhoudkundig grootboek):** Gebouwd voor vooruitkijkende liquiditeitsplanning; vervangt geen ERP-systemen, dubbele-boekhoudsoftware of wettelijke belastingregistraties.
* **Deterministische datummapping:** Modelleert elke verbintenisstranche op een specifieke doeldatum en een specifiek bedrag; probabilistische kortingen voor late betalingen of stresstests voor orderannuleringen vereisen handmatige aanpassingen van datum/bedrag.
* **Variantie in de buitenhorizon (weken 9–16):** Weken 1–8 weerspiegelen bijna vastgelegde verbintenissen, terwijl weken 9–16 operationele schattingen weerspiegelen die onderhevig zijn aan verschuivingen in levertijden van de toeleveringsketen.
* **Architectuur met één basisvaluta:** Leveranciers-PO's in meerdere valuta's (bijv. USD vs. EUR/CNY) dienen te worden ingevoerd tegen je gebudgetteerde of termijnafgedekte wisselkoers in de basisvaluta.
* **Aanbevolen operationele schaal:** Geoptimaliseerd voor mkb-bedrijven die **5 tot 50 gelijktijdige open orders/PO's** per doorlopende cyclus actief beheren in Microsoft Excel.

---

## Over Theseus Workshop

Wij bouwen praktische, audit-klaar financiële en operationele Microsoft Excel-modellen voor groothandel-, productie- en operatorgedreven bedrijven die institutionele controle op treasury en boekhouding nodig hebben binnen standaard spreadsheets.

Elk werkboek gebruikt transparante native Excel-formules zonder zwarte-doos-macro's, waardoor financiële en operationele teams volledig inzicht hebben in elke wekelijkse kasberekening.

Los je complexe problemen op het gebied van werkkapitaal, voorraadinkoop of kapitaalallocatie op in spreadsheets? **[Ontdek onze volledige collectie financiële & operationele Excel-sjablonen bij Theseus Workshop →](https://www.theseusworkshop.com)**

---

## Licentie

Gedistribueerd onder de [Apache License 2.0 open-sourcelicentie](https://www.apache.org/licenses/LICENSE-2.0).

