- [Hinweise für Fachverfahrenshersteller](#hinweise-für-fachverfahrenshersteller)
- [Anstehende Wartungsfenster](#anstehende-wartungsfenster)
- [Bekannte Bugs und Störungen der letzten Monate](#bekannte-bugs-und-störungen-der-letzten-monate)
- [Hinweise](#hinweise)
- [Vergangene Wartungsfenster oder Störungen der letzten Monate](#vergangene-wartungsfenster-oder-störungen-der-letzten-monate)

## Hinweise für Fachverfahrenshersteller
- Der doe_status INTERNAL_ERROR ist KEIN finaler Status, egal mit welchem ted_status er kombiniert ist. Dieser bedeutet, dass sich unser Support die Bekanntmachung genauer anschaut und sie anschließend, je nach Fehlermeldung (z.B. 502 Gateway Timeout von TED oder ein inhaltlicher Schematron-Fehler) entweder auf doe_status REJECTED setzt (final abgelehnt) oder auf doe_status ACCEPTED. Dieser Prozess ist teilweise automatisiert, sodass bei Verbindungsfehlern mit TED die Bekanntmachung automatisch erneut übermittelt wird.
- Sollte ihr System nach dem doe_status INTERNAL_ERROR (welcher NICHT final ist) den Bekanntmachungsstatus nicht mehr automatisch aktualisieren, können Sie den Status auch über die Notices Tabelle im Self-Service Portal (self-service.datenservice-oeffentlicher-einkauf.de) mit den Login Daten ihres Systems beim Vermittlungsdienst prüfen. Bekanntmachungen werden nicht im INTERNAL_ERROR Status verbleiben. Bitte eröffnen sie hierzu keine Support-Tickets, sondern wenden Sie sich an Ihren Fachverfahrenshersteller. Lediglich der doe_status REJECTED (auf dem Self-Service Portal auch als TED = Manually rejected bekannt ist) ist final, in diesem Fall müssen sie die Bekanntmachung mit einer neuen Notice-ID oder Version einliefern.

Weitere wichtige Hinweise zur Erstellung von eForms finden Sie in der von [KoSIT bereitgestellten FAQ](https://xeinkauf.de/eforms-de/faq/) 

## Anstehende Wartungsfenster

| Umgebung    | System                           | Datum      | Zeit              | Kommentar           |
|-------------|----------------------------------|------------|-------------------|---------------------|
| Produktion | Alle TED Apps und deren APIs | 07. Januar 2026 | 07:00-09:00 | Wartungsarbeiten: Alle TED-Anwendungen in produktiven Umgebungen sowie deren APIs können von Störungen betroffen sein |

## Bekannte Bugs und Störungen der letzten Monate

| System       | vorhanden seit | voraussichtliche Behebung | Fehler | Status |
|--------------|----------------|----------------------------|--------|--------|
|--------------|----------------|----------------------------|--------|--------|

## Hinweise

Die Preview-Umgebung ist ausschließlich zwischen 06:00 bis 20:00 Uhr erreichbar. Die Staging-Umgebung sollte auch für Testzwecke genutzt werden, sie ist rund um die Uhr verfügbar.

## Vergangene Wartungsfenster oder Störungen der letzten Monate

| Umgebung                 | System              | Datum      | Zeit              | Kommentar           |
|--------------------------|---------------------|------------|-------------------|---------------------|
| Produktion | Alle TED Apps und deren APIs | 27. November 2025 | 07:00-09:00 | Wartungsarbeiten: Alle TED-Anwendungen in produktiven Umgebungen sowie deren APIs können von Störungen betroffen sein |
| Produktion und Staging | DÖE inkl. BKMS | 25./26. Oktober 2025 | 07:00-12:00 | Quartalswartungen (inkl. Zeitumstellung) |
| Produktion und Staging | SSP-Portal |22-23. Oktober 2025 | -- |Die STOP-Funktion über das SSP-Portal ist aktuell nicht funktionsfähig. Es wird empfohlen, den direkten Aufruf des Vermittlungsdienstes zu verwenden https://ozg-vermittlungsdienst.de/q/swagger-ui/#/Lieferungen/stopPublication - Behoben am 23. Oktober 2025 |
| Staging | SSP-Portal | 06-17. Oktober 2025| -- | Authentifizierungsstörung - Behoben am 17. Oktober 2025 |
