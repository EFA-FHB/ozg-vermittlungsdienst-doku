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

| Umgebung            | System         | Datum              | Zeit        | Kommentar                                                                                                      |
|---------------------|----------------|--------------------|-------------|----------------------------------------------------------------------------------------------------------------|
| Preview und Staging | DÖE exkl. BKMS | 07. September 2026 | 10:00-11:00 | Wartungsarbeiten beim DÖE: Sollte es nach den Wartungsarbeiten zu einem 401 Unauthorized kommen, bitte einen neuen Access Token anfordern bzw. die Anmeldung/Token-Aktualisierung erneut durchführen. |

## Bekannte Bugs und Störungen der letzten Monate

| System       | vorhanden seit | voraussichtliche Behebung | Fehler | Status                  |
|--------------|----------------|----------------------------|--------|-------------------------|
|--------------|----------------|----------------------------|--------|-------------------------|

## Hinweise

Die Preview-Umgebung ist ausschließlich zwischen 06:00 bis 20:00 Uhr erreichbar. Die Staging-Umgebung sollte auch für Testzwecke genutzt werden, sie ist rund um die Uhr verfügbar.

## Vergangene Wartungsfenster oder Störungen der letzten Monate

| Umgebung                         | System                                               | Datum            | Zeit                  | Kommentar                                                                                                                                                                               |
|----------------------------------|------------------------------------------------------|------------------|-----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Produktion                       | TED Publication API                                  | 27. August 2026  | 06:30-09:30           | Wartungsarbeiten bei TED: Publication API in der produktiven Umgebung wird vorübergehend nicht verfügbar sein                                                                           |
