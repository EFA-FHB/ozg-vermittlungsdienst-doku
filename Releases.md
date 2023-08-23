### EfA-Umsetzungsprojekt "Zugang zur öffentlichen Vergabe"
# Releases
[Übersicht](/Readme.md)
<br>

## Geplantes Release für eForms-DE 1.1 und 1.0.1 schematron updates, transformation in eSender-Hub und unterstützung von der neuen BKMS Autorisierung - Vermittlungsdienst und eSender-Hub
| Umgebung Vermittlungsdienst  | Zeitraum              | BKMS                      | Status |
|------------|-----------------------|---------------------------|--------|
| Preview    | KW37                  | unterstützt in Alpha      |        |
| Staging    | KW38, spätestens KW39 | unterstützt in Alpha      |        |
| Produktion | KW39                  | unterstützt in Produktion |        |

Status: bereit für die Entwicklung<br>
<details>
<summary>Release notes (In Bearbeitung)</summary>

### Vermittlungsdienst
>**Umgebungen** <br>
>Preview Umgebung https://preview.ozg-vermittlungsdienst.de<br>
>Staging Umgebung https://staging.ozg-vermittlungsdienst.de<br>
>Production Umgebung https://ozg-vermittlungsdienst.de<br>

- Neue BKMS Autorisierung wurde implementiert
- ...

### eSender-Hub
- eFormsDE 1.1 -> eForms SDK 1.7 Mapping wurde hinzugefügt
- Neue transformation bezüglich 'requestedPublicationDate' wurden implementiert
- ...

### Validator
- Schematron updates für eFroms-DE 1.1 und 1.0.1 wurden hinzugefügt
- ...
</details>
<br>

## Geplantes Release für eForms-DE 1.1 - Vermittlungsdienst und eSender-Hub
| Umgebung Vermittlungsdienst  | Zeitraum              |  BKMS                      | Status         |
|------------|-----------------------|---------------------------|----------------|
| Preview    | KW34                  | noch nicht unterstützt    | veröffentlicht |
| Staging    | KW35, spätestens KW36 | unterstützt in Alpha      |                |
| Produktion | KW37                  | unterstützt in Produktion |                |

Status: In Entwicklung<br>
<details>
<summary>Release notes (In Bearbeitung)</summary>

### Vermittlungsdienst
>**Umgebungen** <br>
>Preview Umgebung https://preview.ozg-vermittlungsdienst.de<br>
>Staging Umgebung https://staging.ozg-vermittlungsdienst.de<br>
>Production Umgebung https://ozg-vermittlungsdienst.de<br>

- Unterstützung von eForms-DE 1.1 wurde implementiert
- Zertifikate wurden aus den Tenants ausgelagert und werden pro Umgebung verwendet
- Autorisation über apiKey in Tenant ist nicht mehr möglich
- Ein neuer Job für die re-sync von den Status wurde implementiert
- ...

### eSender-Hub
 - eFormsDE 1.1 -> eForms SDK 1.7 Mapping wurde hinzugefügt
 - Eine zusätzliche Log-Ebene wurde hinzugefügt
 - ...
</details>
<br>

## Release Offline-Validator für eForms-DE 1.0.1 und 1.1.0
Status: Veröffentlicht 14.08.2023<br>
https://github.com/EFA-FHB/eforms-validator-core/releases/tag/1.0.3
<br><br>
## Production Release Juni - Vermittlungsdienst & eSender-Hub
Status: Veröffentlicht 28.06.2023<br>
<details>
<summary>Release notes</summary>

### Vermittlungsdienst
>**Umgebungen** <br>
>Preview Umgebung https://preview.ozg-vermittlungsdienst.de<br>
>Staging Umgebung https://staging.ozg-vermittlungsdienst.de<br>
>Production Umgebung https://ozg-vermittlungsdienst.de<br>

>**Info** <br>
>Nach dem Produktionsrelease im Juni muss für die Produktions- und Stagingumgebung erneut ein User angefragt werden, auch wenn in Preview bereits ein User besteht. 

- Stop-Endpoint zum stoppen von nationalen Bekanntmachungen im BKMS hinzugefügt
- Prüfung dass Aktualisierungen von Bekanntmachungen nicht möglich sind, wenn die vorherige Version nicht gestoppt wurde oder wenn sie bereits veröffentlicht ist
- Open-Api-Beschreibung angepasst
- Verbesserte Fehlermeldungen bei der Rückgabe von Informationen an FVH
- Metriken hinzugefügt, um die letzten erfolgreichen und erfolglosen Endpunktaufrufe zusammen mit den geplanten Jobläufen zu messen
- Mehrere Optimierungen und Fehlerbehebungen
- Einführung von Paging für geplante Jobs
- Prüfung von auftretenden Aktualisierungen von eSender verbessert
- Die Integration des internen Validator wurde verbessert, die Fehlertypen sind nun klarer klassifiziert.
- Die Antwort auf das Datum der letzten Aktualisierung der PSPs wurde aktualisiert und ist nun genauer.
- Geänderte Namen für Fehlergründe:
Anstelle von DELIVERY_NOT_FOUND steht NOTICE_NOT_FOUND
Anstelle von DELIVERY_ALREADY_PROCESSED steht NOTICE_ALREADY_PROCESSED
Anstelle von DELIVERY_METADATA_INVALID steht NOTICE_METADATA_INVALID
- Neuer Endpunkt /v1/notices/status erstellt - Gibt die Statusinformationen für Bekanntmachungen innerhalb eines bestimmten Zeitraums zurück.

### eSender-Hub
- Manueller Stopp in BKMS implementiert, wenn PSP die Benachrichtigung stoppt
- Automatische Stopp in BKMS aufgrund von TED NOT_PUBLISHED implementiert
- Aktualisierte Übersetzungen für Fehlermeldungen
- Transformationen umgesetzt: Versionsumwandlung von eform-de-1.0 nach eform-sdk-1.5 und Umwandlung von DE-Codelisten in EU-Codelisten
- Implementiert: Abrufen und Speichern des BKMS-Status PUBLISHED
- Jobs PROCESS_NOTICES und ALIGN_TED_STATUS verbessert
- Einführung einer Anwendung zur Kontoverwaltung
- Verbesserte Antwort für Vermittlungsdienst im Falle von Duplikaten
- API-Schlüssel für Produktions- und Staging-Benutzer wurden aktualisiert
- Performance Verbesserungen
- Mehrere Optimierungen und Fehlerbehebungen
</details>
<br>

## Preview Release Mai - Vermittlungsdienst & Validator Webservice
Status: Veröffentlicht 04.05.2023<br>
<details>
<summary>Release notes</summary>
<br>

### Vermittlungsdienst
Preview Umgebung https://bkms-mediator-app-preview.efa-fhb.apps-int.nortal.com
- Erweiterung der API Autorisierung um Refresh Token<br>
Details unter [Anbindung an den Vermittlungsdienst](/documentation/Connection_to_mediator.md)

- Erweiterung der Statusinformationen um Transferinformationen (Warnungen und Fehlermeldungen).<br> 
Details unter [Status- und Transferinformationen](/documentation/Status_information.md)
- Detailliertere Fehlermeldungen 
- Versionsprüfung erfolgt nun zusätzlich anhand der Daten des Bekanntmachungsservice<br>
Bei Übermittlung einer Änderungsmitteilung einer unterschwelligen Bekanntmachung erfolgen folgende Prüfungen:<br>
-Ist die zu ändernde Bekanntmachung im BKMS vorhanden?<br>
-Sind bereits mehrere Bekanntmachungen im BKMS vorhanden, deren verkettete noticeId und noticeVersion mit dem Change Notice Version Identifier übereinstimmen?<br>
-Ist eine Änderungsmitteilung im BKMS vorhanden, welche die zu ändernde Version bereits aktualisiert hat?<br>
Das heißt es wird nur die neueste Version in einer Kette von Bekanntmachungen aktualisiert.
- Im Bekanntmachungsservice veröffentlichte unterschwellige Bekanntmachungen erhalten den Status PUBLISHED.<br>
Der Status wird bei einer Statusabfrage entsprechend zurückgegeben.
- Mehrere Optimierungen und Fehlerbehebungen
<br><br>

### Validator
Preview Umgebung https://eforms-validator-preview.efa-fhb.apps-int.nortal.com 
- Erweiterung des Ergebnis-Reports um die Regelbezeichnung `rule` und die angewandte Regel `ruleContent` 

- Mehrere Optimierungen und Fehlerbehebungen
</details>
<br>
</details>
