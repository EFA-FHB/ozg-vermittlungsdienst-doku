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
- Sollte ihr System nach dem doe_status INTERNAL_ERROR (welcher NICHT final ist) den Bekanntmachungsstatus nicht mehr automatisch aktualisieren, können Sie den Status auch über die Notices Tabelle im Self-Service Portal (portal.ozg-vermittlungsdienst.de) mit den Login Daten ihres Systems beim Vermittlungsdienst prüfen. Bekanntmachungen werden nicht im INTERNAL_ERROR Status verbleiben. Bitte eröffnen sie hierzu keine Support-Tickets, sondern wenden Sie sich an Ihren Fachverfahrenshersteller. Lediglich der doe_status REJECTED (auf dem Self-Service Portal auch als TED = Manually rejected bekannt ist) is final, in diesem Fall müssen sie die Bekanntmachung mit einer neuen Notice-ID oder Version einliefern. 


## Hinweise für Fachverfahrenshersteller
- Der doe_status INTERNAL_ERROR ist KEIN finaler Status, egal mit welchem ted_status er kombiniert ist. Dieser bedeutet, dass sich unser Support die Bekanntmachung genauer anschaut und sie anschließend, je nach Fehlermeldung ( z.B. 502 Gateway Timeout von TED oder ein inhaltlicher Schematron-Fehler) entweder auf doe_status REJECTED setzt (final abgelehnt) oder auf doe_status ACCEPTED. Dieser Prozess ist teilweise automatisiert, sodass bei Verbindungsfehlern mit TED die Bekanntmachung automatisch erneut übermittelt wird.

## Anstehende Wartungsfenster

| Umgebung    | System                           | Datum      | Zeit              | Kommentar           |
|-------------|----------------------------------|------------|-------------------|---------------------|
| Produktion | Alle TED Apps und deren APIs | 28. August 2025 | 07:00-09:00 | Wartungsarbeiten: Alle TED-Anwendungen in produktiven Umgebungen sowie deren APIs können von Störungen betroffen sein |
| Produktion und Staging | DÖE inkl. BKMS | 25./26. Oktober 2025 | 07:00-12:00 | Quartalswartungen (inkl. Zeitumstellung) |

## Bekannte Bugs und Störungen der letzten Monate

| System       | vorhanden seit | voraussichtliche Behebung | Fehler | Status |
|--------------|----------------|----------------------------|--------|--------|
| DÖE Staging außer BKMS | 05. September 2025 | 11. September 2025 | Authentifizierungsstörung | In Arbeit |

## Hinweise

Die Preview-Umgebung ist ausschließlich zwischen 06:00 bis 20:00 Uhr erreichbar. Nutzen Sie bitte auch die Staging-Umgebung für Testzwecke, diese ist rund um die Uhr verfügbar.

## Vergangene Wartungsfenster oder Störungen der letzten Monate

| Umgebung                 | System              | Datum      | Zeit              | Kommentar           |
|--------------------------|---------------------|------------|-------------------|---------------------|
| Produktion und Staging | DÖE  | 31. Juli 2025 | ab 16:00 | Ende der Supportfrist für eForms v1.2: Ab diesem Zeitpunkt werden Bekanntmachungen im Format v1.2 nicht mehr angenommen. Alle bis dahin akzeptierten und gültigen Bekanntmachungen werden weiterhin an TED und den Bekanntmachungsservice übermittelt und dort veröffentlicht. |
| Produktion und Staging | DÖE inkl. BKMS | 26./27. Juli 2025 | 07:00-12:00 | Quartalswartungen |
| Produktion | DÖE exkl. BKMS | 17. Juni 2025 | 18:00-22:00 | Quartalswartungen: Im angegebenen Zeitraum stehen betroffene Services nicht zur Verfügung |
| Staging | DÖE exkl. BKMS | 13. Mai 2025 | 09:00-13:00 | Quartalswartungen: Im angegebenen Zeitraum stehen betroffene Services nicht zur Verfügung |
