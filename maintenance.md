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
| Produktion | TED API | 28. April 2026 | 07:00-09:00 | Wartungsarbeiten: Alle TED-APIs in den produktiven Umgebungen werden vorübergehend nicht verfügbar sein |

## Bekannte Bugs und Störungen der letzten Monate

| System       | vorhanden seit | voraussichtliche Behebung | Fehler | Status |
|--------------|----------------|----------------------------|--------|--------|
| Vermittlungsdienst, eSender-Hub und alle Validatoren | 16. April 2026 | KW 19 2026 | Aktuell kann es in Einzelfällen zu Ablehnungen bei der Übermittlung an TED kommen. Die Validierung der Regel BR-BT-00720-0048 (BT-720-Tender) weicht derzeit von der TED-Validierung ab | In Arbeit |

## Hinweise

Die Preview-Umgebung ist ausschließlich zwischen 06:00 bis 20:00 Uhr erreichbar. Die Staging-Umgebung sollte auch für Testzwecke genutzt werden, sie ist rund um die Uhr verfügbar.

## Vergangene Wartungsfenster oder Störungen der letzten Monate

| Umgebung                 | System              | Datum      | Zeit              | Kommentar           |
|--------------------------|---------------------|------------|-------------------|---------------------|
| Produktion | TED API | 23. April 2026 | 07:00-09:00 |Wartungsarbeiten: Alle TED-APIs in produktiven Umgebungen können von Störungen betroffen sein |
| TED Publication API - Produktion | Alle TED Apps und deren APIs | 18. März 2026 | 13:50 Uhr - 16:00 Uhr | Übermittlung der Bekanntmachungen ist aktuell gestört - Behoben seitens TED |
| Produktion | Alle TED Apps und deren APIs | 23. Februar 2026 | 07:00-09:00 | Wartungsarbeiten: Alle TED-Anwendungen in produktiven Umgebungen sowie deren APIs können von Störungen betroffen sein |
| Produktion | Alle TED Apps und deren APIs | 19. Februar 2026 | 07:00-09:00 | Wartungsarbeiten: Alle TED-Anwendungen in produktiven Umgebungen sowie deren APIs werden nicht verfügbar |
| Produktion | Alle TED Apps und deren APIs | 30. Januar 2026 | 06:45-09:00 | Wartungsarbeiten: Alle TED-Anwendungen in produktiven Umgebungen sowie deren APIs werden nicht verfügbar |
| Produktion | Alle TED Apps und deren APIs | 07. Januar 2026 | 07:00-09:00 | Wartungsarbeiten: Alle TED-Anwendungen in produktiven Umgebungen sowie deren APIs können von Störungen betroffen sein 
