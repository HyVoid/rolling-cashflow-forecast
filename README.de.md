[ 🌐 عربي ](README.ar.md) | [ 🇩🇪 Deutsch ](README.de.md) | [ 🇫🇷 Français ](README.fr.md) | [ 🇳🇱 Nederlands ](README.nl.md) | [ 🇪🇸 Español ](README.sp.md) | [ 🇬🇧 English ](README.md)

# 16-Wochen-rollierende Cashflow-Forecast-Excel-Vorlage: Direktmethoden-Liquiditätsplaner, PO-Verbindlichkeiten-Tracker & Working-Capital-Modell

<div align="center">

![License](https://img.shields.io/badge/license-Apache%202.0-blue)
![Platform](https://img.shields.io/badge/platform-Microsoft%20Excel-217346)
![Focus](https://img.shields.io/badge/focus-Working%20Capital%20%26%20Treasury-orange)

**Eine Direktmethoden-16-Wochen-rollierende Cashflow-Forecast-Tabelle, erstellt in Microsoft Excel für Großhandels-, Import/Export-, E-Commerce-Inventar- und Fertigungsunternehmen, die offene Bestellungen (POs), Lieferantenvorauszahlungen, Kundenanzahlungen und kurzfristiges Working Capital verwalten.**

[Interaktive Demo des 16-Wochen-rollierenden Cashflow-Simulators starten](https://hyvoid.github.io/rolling-cashflow-forecast/) ·

[Die vollständige 16-Wochen-rollierende Cashflow-Excel-Arbeitsmappe herunterladen](https://www.theseusworkshop.com/l/16wcashflow?utm_source=github&utm_medium=GitHub%20README&utm_campaign=readme%20new%20launch&utm_content=rolling-16-week-cashflow)

</div>

**16-Wochen-rollierende Cashflow-Forecast-Arbeitsmappe** ist ein automatisierter **Microsoft Excel Kurzfrist-Liquiditätsplaner** und **Tracker für offene Verbindlichkeiten**. Sie geht über übliche **13-Wochen-Cashflow-Modelle** hinaus und deckt volle 110 Tage Inventar- und Produktionsvorlaufzeit ab; sie konsolidiert **Debitoren (AR)**, **Kreditoren (AP)**, **nicht fakturierte Verkaufsaufträge (SO)** und **zugesagte Bestellungen (PO)** in einer einzigen wöchentlichen Cash-Zeitachse — und meldet Working-Capital-Engpässe sowie Verletzungen des minimalen Cash-Puffers Wochen vor den Fälligkeitsterminen.

---

## Visuelle Vorschau: 16-Wochen-Cash-Zeitachse & Schwellen-Alarm-Dashboard

<img width="1672" height="941" alt="16-Week Rolling Cash Flow Forecast Excel Template showing weekly cash inflows, supplier PO prepayments, net liquidity balance, and shortfall alerts" src="https://github.com/user-attachments/assets/d43699bc-4a15-470c-901e-7b372c953861" />

> Testen Sie das wöchentliche Verbindlichkeiten-Mapping und die Liquiditätsschwellen-Alarme in Ihrem Browser: [Interaktive 16-Wochen-Direktmethoden-Cashflow-Forecast-Demo](https://hyvoid.github.io/rolling-cashflow-forecast/)

---

## Warum Periodenrechnung kurzfristige Cash-Engpässe nicht verhindert

Profitable Großhandels-, Fertigungs- und physische Produktunternehmen erleben in Wachstumsphasen routinemäßig akute Liquiditätsengpässe. Diese Cash-Engpässe entstehen, weil **Kundenanzahlungen**, **meilensteinbasierte Zwischenabrechnungen**, **vertraglich zugesagte Lieferantenvorauszahlungen** und **gestaffelte Net 30/60/90-Zahlungsbedingungen** Wochen eintreten, bevor überhaupt eine Rechnung in das Hauptbuch gebucht wird.

**Der reaktive Bankkonto- und AR/AP-Workflow (hohes Ausfallrisiko):**

```text
Supplier wire due date arrives
-> Finance checks current bank balance and billed AP aging
-> Unbilled PO prepayments and freight commitments overlooked
-> Working capital shortfall discovered 48 hours before wire deadline

```

**Der proaktive 16-Wochen-Verbindlichkeiten-Forecasting-Workflow (Kontrolle vor der Entscheidung):**

```text
New customer order or supplier Purchase Order (PO) proposed
-> Prepayment and balance milestones logged once in the commitment ledger
-> 16-week rolling cash flow timeline updates automatically
-> Liquidity gap and minimum buffer breach flagged 6–12 weeks in advance

```

Finanzmanager, Controller und Operations-Leiter benötigen Liquiditätstransparenz vor der Entscheidung. Bevor sie eine Lieferantenbestellung unterzeichnen oder einem Großhandelsabnehmer Net 60-Bedingungen einräumen, müssen Operatoren verifizieren, dass das wöchentliche Cash-Tief über der minimalen operativen Cash-Reserve des Unternehmens bleibt.

---

## Die Geschäftslogik & Methodik: Verbindlichkeiten-Forecasting nach Direktmethode

Diese Arbeitsmappe löst das **Problem der Working-Capital-Blindheit vor der Fakturierung**, indem sie **rollierendes Cashflow-Forecasting nach der Direktmethode** mit **Order-to-Invoice-Deduplizierung von Verbindlichkeiten** kombiniert.

### Das kommerzielle Problem: Die Timing-Lücke zwischen Periodenrechnung und Cash in physischen Lieferketten

Standard-Buchhaltungssoftware (QuickBooks, Xero, NetSuite GL) erfasst finanzielle Ereignisse erst, wenn eine **Rechnung** oder **Lieferantenrechnung** ausgestellt wird. In Fertigung, Großhandelsvertrieb und Importgeschäft wird Cash jedoch rechtlich auf der **Auftragsebene** zugesagt:

1. **Beschaffungs-Cash-Abflüsse:** Eine Fabrik verlangt 30% Anzahlung bei Erteilung der Bestellung (PO) und 70% Restbetrag bei Frachtbrief (B/L) oder Wareneingang im Lager — Wochen, bevor eine formelle Kreditorenrechnung gebucht wird.
2. **Verkaufs-Cash-Zuflüsse:** Ein B2B-Kunde zahlt 25% Anzahlung bei Bestätigung des Verkaufsauftrags (SO) und die restlichen 75% entweder vor dem Versand oder zu Net 30/60-Bedingungen nach der Lieferung.
3. **Warum 16 Wochen übliche 13-Wochen-Modelle schlagen:** Eine übliche unternehmerische 13-Wochen-Cash-Prognose (90 Tage) endet genau, bevor ein 60-tägiger Produktionslauf plus 30-tägiger Seetransport plus Net 30-Kundeneinziehung abgeschlossen ist. Die Erweiterung des rollierenden Fensters auf **16 Wochen (112 Tage)** erfasst den gesamten Cash Conversion Cycle von der ersten PO-Anzahlung bis zum letzten Kundeneingang.

### Die Kernmethodik: Dreistufiges deterministisches Cash-Mapping

Statt Cash aus GuV-Durchschnittswerten hochzurechnen, führt die Arbeitsmappe eine deterministische dreistufige Berechnung über ein gleitendes 16-Wochen-Fenster aus ($t \in [1, 16]$):

1. **Deduplizierungs-Engine für Verbindlichkeiten zu Rechnungen:**

$$\text{Active Cash Events} = \{ \text{Billed AR} \} \cup \{ \text{Billed AP} \} \cup \{ \text{Open SOs} \setminus \text{Invoiced SOs} \} \cup \{ \text{Open POs} \setminus \text{Billed POs} \}$$



*Geschäftswirkung:* Sobald eine Bestellung in Ihrem Buchhaltungssystem in eine formelle Lieferantenrechnung umgewandelt wird, schließt das Deduplizierungs-Flag die ursprüngliche PO-Position aus, sodass der Cash-Abfluss nie doppelt gezählt wird.
2. **Übersetzung von Meilensteindaten in Datumsversätze:**
Jede aktive Verbindlichkeit wird in diskrete Cash-Tranchen zerlegt (z. B. Anzahlungs-Tranche + Restbetrags-Tranche), die basierend auf operativen Auslösedaten (Auftragsdatum, voraussichtliches Versanddatum, voraussichtliches Ankunftsdatum oder Rechnungsdatum) zuzüglich vertraglicher Zahlungsbedingungen ($\Delta \text{Days}$) Ziel-Kalenderwochen zugeordnet werden.
3. **Rollierende wöchentliche Liquiditäts- und Pufferbruch-Bewertung:**

$$\text{Ending Cash}_{w} = \text{Opening Cash}_{w} + \sum \text{Committed Inflows}_{w} - \sum \text{Committed Outflows}_{w}$$


$$\text{Liquidity Variance}_{w} = \text{Ending Cash}_{w} - \text{Minimum Safe Cash Threshold}$$



*Geschäftswirkung:* Jede Woche, in der $\text{Ending Cash}_{w} < \text{Minimum Safe Cash Threshold}$ gilt, löst einen sofortigen visuellen Alarm aus und isoliert die exakte Lieferanten-PO oder verzögerte AR-Position, die das Working-Capital-Tief verursacht.

---

## Drei Working-Capital-Fallen in manuellen Cashflow-Tabellen

### Falle 1: Liquiditätssteuerung über monatliche GuV und fakturierte AR/AP-Aging-Berichte

Standard-Aging-Berichte für Debitoren (AR) und Kreditoren (AP) zeigen nur **fakturierte Transaktionen**.

Betrachten Sie einen Importeur, der $80,000 an nicht fakturierten Kundenauftragsanzahlungen hält und nächsten Monat bei Containerankunft $60,000 an vertraglich zugesagten Fabrik-Restzahlungen gegenübersieht. Keine der beiden Verpflichtungen erscheint in der GuV oder im üblichen AP-Aging-Bericht, bevor die Ware eintrifft und Lieferantenrechnungen erfasst werden. Wer das Treasury wöchentlich über monatliche Periodenabschlüsse steuert, liegt mit dem Finanzteam vier bis sechs Wochen hinter den realen Cash-Zusagen zurück.

### Falle 2: Getrennte Verfolgung zwischen Verkaufsaufträgen (CRM) und Bestellungen (Beschaffung)

Wenn das Vertriebsteam am Montag eine 30%-Kundenanzahlung annimmt und das Einkaufsteam am Donnerstag eine 40%-Lieferantenvorauszahlung zusagt, schöpfen beide Aktionen aus demselben operativen Bankkonto. In den meisten KMU leben Vertriebszusagen jedoch in einem CRM oder Auftragsblatt, während Lieferanten-POs in einem separaten Beschaffungs-Tracker liegen.

Getrennte Tabellen für Kundenzuflüsse und Lieferantenabflüsse zu pflegen verhindert, dass Operatoren die **netto-wöchentliche Cash-Position** sehen, wenn sich Erfüllungsdaten auch nur um eine Woche verschieben.

### Falle 3: Cash-Tiefs innerhalb des Monats, versteckt in positiven Monatssummen

Eine monatliche Cashflow-Zusammenfassung kann am Monatsende einen gesunden positiven Netto-Cash-Bestand ausweisen und gleichzeitig einen fatalen mehrtägigen Overdraft in Woche 2 oder Woche 3 verbergen.

Wöchentliche Cash-Engpässe entstehen aus dem Timing-Mismatch zwischen sechs operativen Variablen:

* Anfangsbestand des operativen Bankkontos
* Eingangsdaten von Kundenanzahlungen und Meilensteinen
* Einzugsbedingungen für Kunden-Restbeträge (z. B. Vor Versand vs. Net 30)
* Überweisungstermine für Lieferanten-PO-Vorauszahlungen und Zahlung bei Wareneingang
* Ausgaben für Fracht, Zölle und Zollabfertigung
* Beschleunigtes Auftragsvolumen während saisonaler Spitzenproduktion

Das Zuordnen jeder Verbindlichkeit zu einem konkreten 7-Tage-Bucket legt Cash-Tiefs innerhalb des Monats offen, während Sie noch 6 bis 10 Wochen Zeit haben, Lieferantenbedingungen neu zu verhandeln, Kundeneinzüge zu beschleunigen oder eine revolvierende Kreditlinie in Anspruch zu nehmen.

---

## Für wen diese 16-Wochen-rollierende Cashflow-Excel-Vorlage gedacht ist

Entwickelt für operative Finanzteams und Unternehmensinhaber, die **Treasury-Forecasting nach der Direktmethode in Microsoft Excel** ohne Kosten für Enterprise-TMS-Software benötigen:

| Rolle & Suchpersona | Konkretes Operationsszenario & Vorlagen-Anwendungsfall |
| --- | --- |
| **Finanzmanager & Controller** *(16-Wochen-/13-Wochen-Cashflow-Forecast-Excel-Vorlage)* | Ersetzen Sie manuelle Freitag-Bankabstimmungen durch eine rollierende 16-Wochen-Direktmethoden-Liquiditätsprognose, die Cash-Puffer-Verletzungen 6–12 Wochen im Voraus meldet. |
| **Supply-Chain- & Operations-Direktoren** *(Bestellungs-Cashflow- & Vorauszahlungs-Tracker)* | Simulieren Sie die exakte wöchentliche Cash-Auswirkung einer großen saisonalen Fabrik-PO oder einer verzögerten Versandterminierung, bevor Sie Lieferantenverträge unterzeichnen. |
| **Inventarintensive Gründer & CEOs** *(Working-Capital- & Runway-Forecast-Tabelle)* | Pflegen Sie ein einziges zukunftsgerichtetes Dashboard der operativen Nettoliquidität über schnelle SKU-Expansion, Großhandelserfüllung und Inventaraufbauzyklen hinweg. |
| **Beschaffungs- & Einkaufsleiter** *(Planer für Lieferantenanzahlungen & Zahlungsbedingungen)* | Bewerten Sie Forderungen nach Lieferantenvorauszahlungen (z. B. 30/70- vs. 50/50-Aufteilung) gegen die tatsächlich prognostizierte wöchentliche Cash-Verfügbarkeit. |
| **Fractional CFOs & beratende CPAs** *(Kurzfrist-Treasury- & Turnaround-Cash-Modell)* | Stellen Sie KMU-Klienten mit knappem Working Capital oder Lender-Reporting-Covenants ein standardisiertes, prüfungsfähiges wöchentliches Cashflow-Kontrollinstrument zur Verfügung. |

---

## Anwendungsfälle aus der Praxis: Working-Capital- und Liquiditätsszenarien vor der Fakturierung lösen

### Szenario A: Im-/Export und Großhändler mit 30/70-Fabrikvorauszahlungen

Importeure zahlen routinemäßig 30% bei PO-Erteilung und 70% bei Frachtbrief oder Hafeneingang, während Großhandelseinzelhändler Net 30 oder Net 60 nach Lagerauslieferung zahlen. Indem offene POs und Großhandels-SOs in die **16-Wochen-Cash-Zeitachse** eingetragen werden, sieht der Controller das exakte Working-Capital-Tief von 4 bis 8 Wochen zwischen der Zahlung an die ausländische Fabrik und dem Einzug beim inländischen Händler.

### Szenario B: Lohnfertiger und Sondermaschinenbauer, die Meilensteinabrechnung verfolgen

Fertiger mit mehrstufigen Aufträgen ziehen Kunden-Abschlagszahlungen ein (z. B. 40% Anzahlung, 30% bei Teilbaugruppe, 30% vor Versand) und kaufen Rohmaterial im Voraus. Verschiebt sich ein Produktionsmeilenstein um zwei Wochen, verschiebt das Aktualisieren des voraussichtlichen Versanddatums in der Arbeitsmappe automatisch die nachgelagerten Kundenzuflüsse und zeigt, ob Rohmaterial-Verbindlichkeiten die minimale Cash-Reserve verletzen würden.

### Szenario C: Fractional CFOs mit wöchentlichen Cash-War-Rooms und Lender-Covenant-Reporting

Bei Working-Capital-Sanierungen oder saisonalen Kreditlinien-Ziehungen verlangen Banken und Führungsteams eine transparente wöchentliche Direkt-Cash-Prognose (häufig als 13-Wochen- oder 16-Wochen-rollierender Cashflow-Report angefragt). Diese Vorlage liefert Transaktions-Drilldowns, die genau zeigen, welche Kundenrechnungen und Lieferanten-POs den Netto-Cashflow der jeweiligen Woche treiben.

---

## Was die Arbeitsmappe verfolgt: Mapping von Schmerzpunkt zu Lösung

| Treasury- & Cash-Management-Schmerzpunkt | Häufige Suchanforderung | Eingebaute Excel-Arbeitsmappen-Lösung |
| --- | --- | --- |
| **Nicht fakturierte POs fehlen in Cash-Forecasts** | *Wie man offene Bestellungen in Excel-Cashflow-Forecasts einbezieht* | **Einheitliches Register offener Verbindlichkeiten:** Erfasst fakturierte AR, fakturierte AP, nicht fakturierte Verkaufsaufträge und offene Bestellungen in einer einzigen strukturierten Eingabetabelle. |
| **Doppeltes Zählen von POs nach der Fakturierung** | *Doppelte PO- und Rechnungseinträge in der Cash-Projektion verhindern* | **Automatisierte PO-zu-Rechnung-Deduplizierung:** Identifiziert und schließt Bestellungen aus, die bereits in formelle AP-Rechnungen umgewandelt wurden, sodass jeder Dollar genau einmal gezählt wird. |
| **Overdrafts innerhalb des Monats & überraschende Engpässe** | *Wöchentliche rollierende Cashflow-Forecast-Vorlage mit Niedrig-Cash-Alarmen* | **Konfigurierbare Schwellen-Alarm-Ebene:** Vergleicht die projizierte Wochenend-Cash mit Ihrer benutzerdefinierten minimalen sicheren Cash-Balance und hebt Verletzungswochen in Echtzeit hervor. |
| **Veraltete Versand- & Lieferdaten** | *Dynamisches Cashflow-Modell auf Basis von Versanddaten und Zahlungsbedingungen* | **Automatisiertes Bedingung-zu-Woche-Mapping:** Übersetzt operative Daten (voraussichtliches Versanddatum, Ankunftsdatum, Rechnungsdatum) und Zahlungsbedingungen in exakte wöchentliche Cash-Buckets. |
| **Langsame Prüfungen vor der Zusage** | *Cash-Auswirkung einer neuen Lieferantenbestellung vor dem Einkauf testen* | **Liquiditäts-Sandbox vor der Entscheidung:** Geben Sie eine geplante PO oder einen Kundenauftrag ein und sehen Sie sofort, ob die neue Zusage in 6–16 Wochen ein Cash-Defizit erzeugt. |

---

## Fallstudie: Monatliche Periodenrechnungs-Blindheit vs. 16-Wochen-rollierende Cash-Sichtbarkeit

**Unternehmensprofil:** Importeur von Konsumgütern mit $2M–$10M Jahresumsatz, operierend mit gemischten Kundenanzahlungsbedingungen, ausländischen Lieferanten-Vorauszahlungsplänen und einem schlanken Finanzteam unter einem einzigen Manager.

**Der operative Zusammenbruch:** Jede Woche verbrachte der Finanzmanager zwei Stunden damit, CRM-Verkaufsaufträge, Kundeneinzahlungseingänge, offene Fabrik-POs und Frachtankunftspläne über getrennte Tabellen hinweg abzugleichen. Trotz positiver monatlicher Netto-Cashflows auf dem Papier erlitt das Unternehmen zwei Notfall-Cash-Engpässe in einem einzigen Quartal — beide entdeckt weniger als 48 Stunden, bevor internationale Lieferantenüberweisungen fällig waren.

### Vergleich: Getrennte AR/AP-Tabellen vs. automatisiertes 16-Wochen-Verbindlichkeiten-Modell

| Treasury-Operation | Manuelle getrennte Tabellen (Vorher) | Automatisierte 16-Wochen-rollierende Cashflow-Arbeitsmappe (Nachher) |
| --- | --- | --- |
| **Verbindlichkeiten-Datenarchitektur** | Getrennte CRM-Verkaufsblätter, Beschaffungs-PO-Tracker und Buchhaltungs-AR/AP-Exporte | **Ein einziges einheitliches Verbindlichkeiten-Register** für AR, AP, offene SOs und offene POs mit Deduplizierung |
| **Zeitaufwand für die wöchentliche Prognose** | ~2 Stunden manuelle VLOOKUPs und Datumsabgleiche jeden Freitag | **Unter 5 Minuten pro Woche**; das rollierende 16-Wochen-Fenster aktualisiert sich bei Datumseingabe dynamisch |
| **Sichtbarkeit von Vorauszahlungen vor der Fakturierung** | Blind für Lieferantenanzahlungen und Meilenstein-Restbeträge, bis Lieferantenrechnungen gebucht sind | **Vollständiges Meilenstein-Mapping** über Anzahlungs-Tranchen, Zahlungen vor Versand und Lieferüberweisungen |
| **Erkennungsfenster für Liquiditätsengpässe** | Entdeckt 24–48 Stunden vor Fälligkeit der Überweisung (erzwungene Notfallkreditlinien-Ziehungen) | **6–12 Wochen im Voraus gemeldet** durch automatisierte Alarme bei Verletzung der minimalen Cash-Schwelle |

### Der exakte Wendepunkt, den diese Arbeitsmappe aufdeckt

Betrachten Sie einen **$100,000-Kundenauftrag** und die zugehörige **$50,000-Lieferantenbestellung** ausgehend von einem **Anfangs-Cash-Bestand von $10,000**:

* **Lieferanten-PO-Restbetrag ($30,000 Abfluss):** 60% fällig bei Wareneingang in **Woche 5**.
* **Kunden-SO-Restbetrag ($70,000 Zufluss):** 70% fällig vor Warenausgang aus dem Lager in **Woche 6**.

| Berichtsdetailtiefe | Netto-Cash-Position in Woche 5 | Netto-Cash-Position in Woche 6 | Operationale Schlussfolgerung |
| --- | --- | --- | --- |
| **Traditionelle monatliche Cash-Zusammenfassung** | *Versteckt in der Monatssumme* | **+$50,000 Monatsend-Cash** | Falsches Grünlicht; die Finanzen genehmigen Bedingungen, ohne den Monatsmitte-Ausfall zu sehen |
| **16-Wochen-rollierendes Wochenmodell** | **−$20,000 Cash-Engpass** ($10K − $30K) | **+$50,000 Erholung** (−$20K + $70K) | **Meldet das $20,000-Defizit der Woche 5 fünf Wochen im Voraus**, sodass das Team die Lieferanten-Überweisungsbedingungen an den Kundeneingang anpassen kann |

---

## Treasury-Standards hinter dem rollierenden Cash-Forecasting nach Direktmethode

Corporate-Treasury-Teams setzen auf **kurzfristiges rollierendes Cashflow-Forecasting nach der Direktmethode**, weil periodenrechnungsbasierte Erfolgsrechnungen Rentabilität statt Cash-Solvenz messen. Schnell wachsende Produktunternehmen erwirtschaften häufig starke Buchhaltungsmargen, gehen aber aufgrund des Timings von Inventarvorauszahlungen operativer Cash aus.

Die Direktmethode umgeht die Anpassungen der Periodenrechnung und mappt **100% der erwarteten Brutto-Cash-Eingänge und Brutto-Cash-Abgänge** auf konkrete wöchentliche Buckets:

| Traditionelle Berichtsmethode | Strukturelle Einschränkung im Betrieb | Wie das 16-Wochen-Direktmethoden-Modell sie löst |
| --- | --- | --- |
| **Indirekte GuV-Cash-Schätzung** | Vermischt buchhalterischen Nettogewinn mit liquiden Bankmitteln; verbirgt Working-Capital-Spitzen innerhalb des Monats | Mappt **tatsächlich datierte Cash-Eingänge und Überweisungs-Abgänge** Woche für Woche |
| **Tägliche Bankkonto-Kontrolle** | Rein rückwärtsgerichtet; zeigt abgewickeltes Cash und ignoriert $100K+ an zugesagten künftigen PO-Überweisungen | Projiziert **vorlaufende Cash-Bestände** über die nächsten 16 aufeinanderfolgenden Wochen |
| **Monatliche AR-/AP-Aging-Berichte** | Schließen nicht fakturierte Bestellungen und Kundenmeilensteine vor dem Versand aus | Integrieren **Auftragsverbindlichkeiten vor der Fakturierung** neben fakturierten Forderungen und Verbindlichkeiten |

**Referenzierte maßgebliche Treasury- & Cash-Management-Frameworks:**

* [AICPA: Direktmethoden-Cashflow-Forecasting & Working-Capital-Management](https://www.aicpa-cima.com)
* [Association for Financial Professionals (AFP): Standards für kurzfristiges Treasury & rollierendes Cash-Forecasting](https://www.afponline.org)

---

## Wie der 16-Wochen-rollierende Horizont & das Datumsversatz-Mapping funktionieren

Der 16-Wochen-Prognosehorizont rolliert Woche für Woche vorwärts. Jeder offene Auftrag oder jede Rechnung wird durch die Kombination aus ihrem **operativen Meilensteindatum** und ihrer **vertraglichen Zahlungsbedingung** einer konkreten künftigen Cash-Woche zugeordnet:

| Operativer Meilenstein-Input | Vertragliche Zahlungsbedingung | Abgeleitetes wöchentliches Cashflow-Ereignis im Modell |
| --- | --- | --- |
| **Voraussichtliches Versanddatum an den Kunden** | *Restbetrag fällig vor Versand* | **Cash-Zufluss (Eingang)** gemappt auf die Woche unmittelbar vor dem voraussichtlichen Versand |
| **Voraussichtliches Wareneingangsdatum (ETA)** | *Restbetrag fällig bei Lieferung / Ankunft* | **Cash-Abfluss (Lieferantenüberweisung)** gemappt auf die voraussichtliche Lager-/Hafen-Ankunftswoche |
| **Ausstellungsdatum der Kundenrechnung** | *Net 30-Kreditbedingung* | **Cash-Zufluss (Eingang)** gemappt 4 Wochen nach dem Rechnungsdatum |

**Warum sich die Prognosegenauigkeit zwischen Nahhorizont (Wochen 1–8) und äußerem Horizont (Wochen 9–16) aufteilt:**

* **Wochen 1–8 (Ausführungsfenster mit hoher Konfidenz):** Getrieben von bestätigten Rechnungen, fixierten Schiffsplänen und aktiven Bestellungen, die sich bereits in Produktion befinden. Verwendet für verbindliche Zahlungsplanung, Überweisungsfreigaben und Entscheidungen über Kreditlinien-Ziehungen.
* **Wochen 9–16 (Strategisches Planungs- & Beschaffungsfenster):** Getrieben von geschätzten Produktionsvorlaufzeiten und Pipeline-Verkaufsaufträgen. Verwendet für Stresstests, ob neue Lieferanten-POs aus dem internen Cashflow finanziert werden können, bevor Verträge unterzeichnet werden.

---

## Schnellstart-Tutorial: Ihre 16-Wochen-rollierende Cashflow-Prognose in 7 Schritten bauen

Folgen Sie diesem Schritt-für-Schritt-Workflow, um Ihr Finanz- und Operationsteam von reaktiven Bankkonto-Kontrollen zu proaktivem 16-Wochen-Liquiditätsmanagement zu führen:

1. **Verbindlichkeitsszenarien in der interaktiven Browser-Demo testen**
Öffnen Sie den [Interaktiven 16-Wochen-rollierenden Cashflow-Websimulator](https://hyvoid.github.io/rolling-cashflow-forecast/), um zu erkunden, wie offene POs, Kundenanzahlungen und Versandverzögerungen wöchentliche Cash-Bestände in Echtzeit verschieben.
2. **Anfangs-Cash-Bestand und minimalen sicheren Cash-Puffer konfigurieren**
Geben Sie Ihren aktuellen operativen Bankbestand ein, definieren Sie Ihr Startdatum (Montag) der Prognose und legen Sie die **Minimale Sichere Cash-Schwelle** Ihres Unternehmens fest (z. B. $25,000 oder 1 Monat fixer Lohn-/Opex-Kosten).
3. **Fakturierte Debitoren (AR) und Kreditoren (AP) erfassen**
Geben Sie ausstehende Kundenrechnungen und Lieferantenrechnungen mit ihren vertraglichen Fälligkeitsdaten ein, um Ihre Baseline-Cash-Zeitachse nach der Fakturierung zu etablieren.
4. **Nicht fakturierte Verkaufsaufträge (SO) und offene Bestellungen (PO) eingeben**
Halten Sie bestätigte Kundenaufträge und aktive Lieferanten-POs nebst Anzahlungsprozenten, Restbetragsprozenten, voraussichtlichen Versand-/Ankunftsdaten und Zahlungsbedingungen fest.
5. **Automatisierte PO-zu-Rechnung-Deduplizierung ausführen**
Markieren oder verknüpfen Sie Bestellungen, die bereits von Lieferanten fakturiert wurden, damit die Deduplizierungs-Engine sie aus den offenen Verbindlichkeiten ausschließt und Doppelzählungen verhindert.
6. **Wöchentliche Schwellen-Verletzungs-Alarme prüfen und Cash-Tiefs diagnostizieren**
Prüfen Sie die 16-Wochen-Cash-Zeitachse auf jede Woche, die unter Ihren minimalen Puffer fällt, und filtern Sie dann die Verbindlichkeitstabelle nach dieser Wochennummer, um die exakte Lieferanten-PO oder verzögerte Kundeneinziehung zu identifizieren, die die Lücke verursacht.
7. **Ihre wöchentliche Cash-Prüfung mit der wiederverwendbaren Excel-Arbeitsmappe standardisieren**
Sobald Sie die Logik in der Webvorschau für eine Einzelsitzung getestet haben, **[laden Sie die vollständige, wiederverwendbare 16-Wochen-rollierende Cashflow-Excel-Vorlage herunter](https://www.theseusworkshop.com/l/16wcashflow?utm_source=github&utm_medium=GitHub%20README&utm_campaign=readme%20new%20launch&utm_content=rolling-16-week-cashflow)**, um Ihre laufenden Unternehmensdaten zu speichern, das Gegenparteien-Tracking anzupassen und Ihre wöchentliche 5-Minuten-Liquiditätsprüfung offline in Microsoft Excel durchzuführen.

*Haftungsausschluss: Diese Arbeitsmappe ist ein operatives Cash-Planungs- und Entscheidungsunterstützungsmodell. Sie ergänzt — sie ersetzt nicht — formelle GAAP/IFRS-Buchhaltungssoftware, geprüfte Finanzabschlüsse sowie lizenzierte Treasury- oder Finanzierungsberatung.*

---

## Die vollständige Excel-Vorlage herunterladen

Bereit, überraschende Engpässe am Zahlungstermin zu beseitigen und Ihre AR-, AP- und offenen Auftragsverbindlichkeiten in einer rollierenden Zeitachse zu vereinen?

👉 **[Holen Sie sich die vollständige 16-Wochen-rollierende Cashflow-Forecast-Excel-Arbeitsmappe](https://www.theseusworkshop.com/l/16wcashflow?utm_source=github&utm_medium=GitHub%20README&utm_campaign=readme%20new%20launch&utm_content=rolling-16-week-cashflow)**

---

## Technischer Umfang & operationelle Einschränkungen

* **Abhängigkeit von der Datenaktualität:** Die Prognosegenauigkeit hängt von aktuellen operativen Schätzungen ab; nicht erfasste Lieferanten-POs oder veraltete Frachtankunftsdaten unterschätzen oder verschieben wöchentliche Cash-Abflüsse.
* **Wöchentliche rollierende Pflegekadenz:** Entwickelt für eine 5-Minuten-Wochenaktualisierung (Anfangs-Cash aktualisieren, das Startdatum vorrollen und verschobene Versand-ETAs anpassen).
* **Entscheidungsunterstützungsebene (kein Buchhaltungs-Hauptbuch):** Für zukunftsorientierte Liquiditätsplanung gebaut; ersetzt keine ERP-Systeme, keine Buchhaltungssoftware mit doppelter Buchführung und keine gesetzlichen Steuerunterlagen.
* **Deterministisches Datumsmapping:** Modelliert jede Verbindlichkeitstranche mit einem konkreten Zieldatum und Betrag; probabilistische Zahlungsverzugs-Abschläge oder Stresstests für Auftragsstornierungen erfordern manuelle Datums-/Betragsüberschreibungen.
* **Abweichung am äußeren Horizont (Wochen 9–16):** Die Wochen 1–8 spiegeln nahezu fixierte Verbindlichkeiten wider, während die Wochen 9–16 operative Schätzungen darstellen, die Verschiebungen der Lieferketten-Vorlaufzeiten unterliegen.
* **Architektur mit einer einzigen Basiswährung:** Lieferanten-POs in Fremdwährungen (z. B. USD vs. EUR/CNY) sollten zu Ihrem budgetierten oder forward-gesicherten Wechselkurs in der Basiswährung erfasst werden.
* **Empfohlene operationelle Skala:** Optimiert für KMU, die pro rollierendem Zyklus aktiv **5 bis 50 gleichzeitige offene Aufträge/POs** in Microsoft Excel verwalten.

---

## Über Theseus Workshop

Wir erstellen praxisnahe, prüfungsfähige Finanz- und Operations-Microsoft-Excel-Modelle für Großhandels-, Fertigungs- und operator-geführte Unternehmen, die institutionelle Treasury- und Buchhaltungskontrolle in Standard-Tabellenkalkulationen benötigen.

Jede Arbeitsmappe verwendet transparente native Excel-Formeln ohne Black-Box-Makros und gibt Finanz- und Operationsteams vollständige Einblick in jede wöchentliche Cash-Berechnung.

Lösen Sie komplexe Working-Capital-, Inventarbeschaffungs- oder Kapitalallokationsprobleme in Tabellenkalkulationen? **[Entdecken Sie unsere vollständige Kollektion von Finanz- & Operations-Excel-Vorlagen bei Theseus Workshop →](https://www.theseusworkshop.com)**

---

## Lizenz

Vertrieben unter der [Apache License 2.0 Open Source License](https://www.apache.org/licenses/LICENSE-2.0).

