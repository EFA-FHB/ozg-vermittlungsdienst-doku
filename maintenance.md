- [Wichtige Hinweise zur Erstellung von eForms](#wichtige-hinweise-zur-erstellung-von-eforms)
- [Hinweise für Fachverfahrenshersteller](#hinweise-für-fachverfahrenshersteller)
- [Anstehende Wartungsfenster](#anstehende-wartungsfenster)
- [Bekannte Bugs und Störungen](#bekannte-bugs-und-störungen)
- [Hinweise](#hinweise)
- [Vergangene Wartungsfenster oder Störungen](#vergangene-wartungsfenster-oder-störungen)

## Wichtige Hinweise zur Erstellung von eForms 
Um eine reibungslose Einlieferung zu gewährleisten, beachten Sie bitte immer die folgenden Aspekte: 

- Das Feld **BT-05 Notice Dispatch date** **(IssueDate)** muss zum Zeitpunkt des Versands an den Vermittlungsdienst zwischen gestern und morgen liegen, sonst lehnt TED die Bekanntmachung ab. 
- Die Rolle **ted-esen** darf in Bekanntmachungen NICHT verwendet werden, weder als org-role noch als org-sub-role. 

- Das Feld **Preferred Publication Date BT-738 (RequestedPublicationDate)** kann laut deutschem Standard auf den selben Zeitpunkt wie das Notice Dispatch date oder bis zu 2 Tage nach dem Notice Dispatch date gesetzt werden. Bitte achten Sie darauf, für beide Werte die selbe Zeitzone anzugeben, da es sonst in Einzelfällen zu Ablehnungen bei TED kommen kann
- Die Befüllung des Feldes **BT-165 Winner Size (Winner Size)** wird derzeit nicht von den deutschen Regeln geprüft. Bitte stellen Sie selbstständig sicher, dass dieses Feld für die folgenden Notice Types korrekt befüllt wird: '25', '26', '27', '28', '29', '30', '31', '32', 'E4', '33', '34', '35', '36' & '37'
- Für die Befüllung der **BT-501 Identifikationsnummer (der Organisation)** beachten Sie bitte die Hinweise u. A. zur Leitweg-ID in unserer FAQ: https://github.com/EFA-FHB/ozg-vermittlungsdienst-doku/blob/main/faq.md#identifikationsnummer-organisation-bt-501
- Sollte ihr System nach dem doe_status INTERNAL_ERROR (welcher NICHT final ist) den Bekanntmachungsstatus nicht mehr automatisch aktualisieren, können Sie den Status auch über die Notices Tabelle im Self-Service Portal (portal.ozg-vermittlungsdienst.de) mit den Login Daten ihres Systems beim Vermittlungsdienst prüfen. Bekanntmachungen werden nicht im INTERNAL_ERROR Status verbleiben. Bitte eröffnen sie hierzu keine Tickets bei der BDR, sondern wenden Sie sich an Ihren Fachverfahrenshersteller. Lediglich der doe_status REJECTED is final, in diesem Fall müssen sie die Bekanntmachung mit einer neuen Notice-ID oder Version einliefern. 


## Hinweise für Fachverfahrenshersteller
- Der doe_status INTERNAL_ERROR ist KEIN finaler Status, egal mit welchem ted_status er kombiniert ist. Dieser bedeutet, dass sich unser Support die Bekanntmachung genauer anschaut und sie anschließend, je nach Fehlermeldung ( z.B. 502 Gateway Timeout von TED oder ein inhaltlicher Fehler wie oben genannt z.B. IssueDate falsch) entweder auf doe_status REJECTED setzt (final abgelehnt) oder auf doe_status ACCEPTED.  Dieser Prozess wird in Zukunft weiter optimiert und automatisiert, aber bitte hören Sie bei einem doe_status INTERNAL_ERROR nicht auf, den Status für die Bekanntmachung abzufragen. 

## Anstehende Wartungsfenster

| Umgebung    | System                           | Datum      | Zeit              | Kommentar           |
|-------------|----------------------------------|------------|-------------------|---------------------|
| Produktion | TED Apps for eForms | 03. September 2024 | 07:00-09:00 |Angekündigt von TED  |
| Produktion | TED Apps for eForms | 05. September 2024 | 07:00-10:30 |Angekündigt von TED  |
| Produktion | Alle Services des DÖE außer BKMS | 26-27 Oktober 2024 |  | Quartalswartungen (inkl. Zeitumstellung) |

## Bekannte Bugs und Störungen

| System       | vorhanden seit      | voraussichtliche Behebung   | Fehler           | Status           |
|--------------|--------------------------|-----------------------------|---------------------|----|
| Bekanntmachungsservice | 19.09.2024 | 20.09.2024 | Autorisierungsstörung beim BKMS: der Lieferprozess ist gestört, dabei alle übermittelte Bekanntmachungen werden umgehend weitergeleitet sobald BKMS sie wieder annimmt. | __Behoben__ |
| TED Apps for eForms | 06.09.2024 | 09.09.2024 | Technische Störung bei der Zuweisung von publicationIds von TED: Es wurden zunächst falsche publicationIds zugewiesen, die anschließend durch die korrekten ersetzt wurden. __Ein entsprechendes Update im DÖE ist derzeit aus technischen Gründen leider nicht möglich.__| __Behoben seitens TED__ |
| Alle Validatoren | 28.05.2024 | 10/2024 | __BR-DE-23__: Validierungsprozess bricht ab wenn eine Bekanntmachung unter _<cac:SubordinateAwardingCriterion>_ den Tag _<efac:AwardCriterionParameter>_ doppelt beinhaltet. Es wird ein __500 Internal Sever Error__ Fehler zurückgegeben | __In Arbeit__ |



## Hinweise

Die Preview-Umgebung ist ausschließlich zwischen 06:00 bis 20:00 Uhr erreichbar. Nutzen Sie bitte auch die Staging-Umgebung für Testzwecke, diese ist rund um die Uhr verfügbar.

Am 27.09.2023 wurde der API-Key für die Einlieferung bei TED angepasst. Aus diesem Grund werden Statusinformationen für Bekanntmachungen, die vor diesem Datum in Staging oder Preview eingeliefert wurden, nicht mehr bei TED abgefragt. Dies ist eine einmalige Anpassung und wird in Zukunft nicht wieder vorkommen. 

## Vergangene Wartungsfenster oder Störungen

| Umgebung                 | System              | Datum      | Zeit              | Kommentar           |
|--------------------------|---------------------|------------|-------------------|---------------------|
| Produktion | TED Apps for eForms | 20. August 2024 | 07:00-09:00 CET |Angekündigt von TED  |
| Produktion | Alle Services des DÖE außer BKMS (Staging) | 01.08.2024 |  | Technische Störung wegen Zertifikatserneuerung |
| Produktion | Alle Services des DÖE außer BKMS | 27-28 Juli 2024 |  |Quartalswartungen |
| Produktion | Bekanntmachungsservice | 30.07.2024 |  | Integrationsstörung zwischen Vermittlungsdienst und eSender aufgrund des Deployments der neuen Version des Bekanntmachungsservices |
| Preview | Vermittlungsdienst | 26.06.2024 | | Preview Umgebung ist nicht erreichbar |
|Produktion + Staging | Alle Services des DÖE außer BKMS (Produktion + Staging) | 14.06.2024 |  | Derzeit ist die Produktions- und Stagingumgebung nicht erreichbar aufgrung von Problemen im Rechenzentrum. Wir erwarten eine zeitnahe Behebung |
| Preview | Alle Services des DÖE außer BKMS | 22.05.2024 |  | Preview Umgebung ist nicht erreichbar |
| Preview | Alle Services des DÖE außer BKMS | 30.04.2024 |  | Preview Umgebung ist nicht erreichbar |
| Preview | Alle Services des DÖE außer BKMS | 22.04.2024 |  | Preview Umgebung ist nicht erreichbar |
| Produktion | Validator im Vermittlungsdienst | 02.04.2024 |  | Bei sehr großen Bekanntmachungen mit sehr vielen Regeln kommt es vereinzelt zu timeouts bei der Einlieferung |
| Produktion | Viewer | 02.04.2024 | | Teilweise können eFormsDE 1.2 Bekanntmachungen mit bestimmten Indicator-Werten nicht gerendert werden |
| Produktion | Integration mit BKMS   | 14.03.2024 |  | Authentifizierungsproblem beim BKMS führt zur Störungen während des Lieferungsprozesses |
| Produktion | Vermittlungsdienst | 29.02.2024 |  | Störungen bei der Verarbeitung einzelner Bekanntmachungen aufgrund von  starker Belastung |
| Alle Umgebungen          | Vermittlungsdienst | 31.05.2024 | ab 14:00 CEST | Infrastrukturwartung: entfernung von statischen IP-Adressen |
| Produktion               | TED Produktion | 16.05.2024 | 07:00 - 09:00 CEST | TED Infrastrukturwartung |
| Staging und Preview      | TED Preview | 15.05.2024 | 07:00 - 09:00 CEST | TED Infrastrukturwartung |
| Staging                  | Alle Services des DÖE außer BKMS | 22.05.2024 | 09:00 - 12:00 CEST | Infrastrukturwartung |
| Produktion               | Alle Services des DÖE außer BKMS | 29.05.2024 | 16:00 - 17:00 CEST | Infrastrukturwartung |
| Produktion               | Alle Services des DÖE außer BKMS | 27.-28.07.2024 | 20:00 - 20:00 CEST | Infrastrukturwartung |
| Produktion               | Alle Services des DÖE außer BKMS | 26.-27.10.2024 | 20:00 - 20:00 CEST | Infrastrukturwartung |
| Staging                  | Alle Services des DÖE außer BKMS | 18.04.2024 | 09:00 - 12:00 CEST | Infrastrukturwartung |
| Produktion               | Alle Services des DÖE außer BKMS | 21.03.2024 | 16:00 - 17:00 CEST | Wartungsarbeiten: Autorisierungstoken soll neu erstellt werden |
| Produktion               | Alle Services des DÖE außer BKMS | 27.-28.01.2024 | 20:00 - 20:00 CEST | Infrastrukturwartung |
| Staging                  | Alle Services des DÖE außer BKMS | 17.01.2024 | 19:00 - 20:00 CEST | Infrastrukturwartung | 
| Produktion und Staging   | Alle Services des DÖE außer BKMS | 09.01.2024 | 20:00 - 22:00 CEST | Infrastrukturwartung | 
| Preview                  | Alles Services des DÖE außer BKMS | 27.12.2023 - 02.01.2024 | | Vorübergehende Nichtverfügbarkeit, bitte in der Zwischenzeit für Tests die jeweiligen Services in der Staging Umgebung nutzen! | 
| Produktion               | Alle Services des Vermittlungsdienst inkl. eSender (nicht BKMS) | 21.11.2023 | 06:00 - 07:00 CEST | Infrastrukturwartung |
| Produktion               | Alle Services des Vermittlungsdienst inkl. eSender (nicht BKMS) | 11.12.2023 | 06:00 - 07:00 CEST | Infrastrukturwartung | 
| BKMS Produktion          | BKMS  | 27.10  | 27.10. 13:10 - 14:35 CEST | Online-Suchfunktion war nicht verfügbar |
| DÖE Produktion + Staging | alle Services außer BKMS | 25.10.2023 | 15:31 - 16:03 CEST | Nicht-Erreichbarkeit des Rechenzentrums |
| DÖE Produktion + Staging | alle Services außer BKMS               |23.10.2023 - 24.10.2023                | 17:00 - 09:00 CEST |  Aufgrund von Infrastrukturproblemen nicht verfügbar | 
| DÖE Produktion + Staging | alle Services außer BKMS | 20.10.2023 | 10:00 - 13:00 CEST | Deployment für Performanceverbesserungen | 
| DÖE Produktion + Staging | alle Services außer BKMS | 10.10.2023 | 09:00 - 12:00 CEST | Rechenzentrumswartung | 
| TED Preview              | TED Apps for eForms | 10.10.2023 | 07:00 - 10:00 CEST | Angekündigt von TED | 
| TED Production           | TED Apps for eForms | 11.10.2023 | 07:00 - 10:00 CEST | Angekündigt von TED | 
| TED Produktion + Preview | TED Developer Portal, TED Apps for eForms | 02.10.2023 | 07:00 - 09:00 CEST | Angekündigt von TED | 
| TED Produktion           | TED Apps for eForms | 27.09.2023 | 07:00 - 09:00 CEST | Angekündigt von TED |
| DÖE Produktion           | Vermittlungsdienst| 14.09.2023| 08:00 - 09:30 Uhr | vorrübergehend nicht erreichbar | 
| TED Produktion           | TED Apps for eForms | 30.08.2023 | 18:00-22:00 CEST | Angekündigt von TED | 
| TED Produktion           | TED Apps for eForms | 30.08.2023 | 18:00-22:00 CEST | Angekündigt von TED |
| TED Preview              | TED Apps for eForms | 28.08.2023 | 07:00-11:00 CEST  | Angekündigt von TED |
| TED Preview              | TED Apps for eForms | 24.08.2023 | 07:00-08:00 CEST  | Angekündigt von TED |
| TED Produktion           | TED Apps for eForms | 23.08.2023 | 07:00-08:00 CEST | Angekündigt von TED | 
