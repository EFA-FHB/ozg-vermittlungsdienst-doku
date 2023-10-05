### EfA-Umsetzungsprojekt "Zugang zur öffentlichen Vergabe"
# Releases
[Übersicht](/Readme.md)
<br>


## Release für Self-Service Portal - Portal-Account, Registrierungsform für einen separaten Vermittlungsdienst-Account
| Umgebung Vermittlungsdienst  | Zeitraum  | Status         |
|------------|-----------------------------|----------------|
| Preview    | Doku + Registrierungsformular: **KW38** , Statusübersicht: **KW39**         | veröffentlicht |
| Staging    | Doku + Registrierungsformular: **KW39**  , Statusübersicht: **KW40**        | veröffentlicht |
| Produktion | Doku + Registrierungsformular: **KW40** , Statusübersicht **KW41**          | veröffentlicht |

Status: Veröffentlicht <br>
<details>
<summary>Release Notes</summary>

### Self-Service Portal
>**Umgebungen** <br>
>NEU: Preview https://portal.preview-ozg-vermittlungsdienst.de <br>
>NEU: Staging https://portal.staging-ozg-vermittlungsdienst.de <br>
>NEU: Production https://portal.ozg-vermittlungsdienst.de<br>

### Feature Dokumentation anzeigen + Registrierungsformular
- Volle Dokumentation im Portal inkl. Releases und Maintenance Seiten
- Registrierungsformular für Beantragung neuer Vermittlungsdienst Accounts
  1.  Erstellen eines neuen Portal-Accounts
  2.  Ausfüllen der Registrierungsform für einen separaten Vermittlungsdienst-Account

### Feature Statusübersicht von Bekanntmachungen
- Statusübersicht aller eingelieferten Bekanntmachungen für Vermittlungsdienst Accounts 
  
</details>
<br>


## Release für RequestedPublicationDate Fix + Notice-Viewer - Vermittlungsdienst, eSender-Hub, Notice-Viewer
| Umgebung Vermittlungsdienst  | Zeitraum              | BKMS                      | Status |
|------------|-----------------------|---------------------------|--------|
| Preview    | nur RequestedPublicationDate Fix: **KW37**,  Alles andere: **KW39**                 | unterstützt in Alpha      | veröffentlicht |
| Staging    | verschoben: **KW40**    | unterstützt in Alpha      | veröffentlicht |
| Produktion | verschoben: **KW41**                  | unterstützt in Produktion | veröffentlicht |

Status: Veröffentlicht <br>
<details>
<summary>Release notes</summary>

### Vermittlungsdienst
>**Umgebungen** <br>
>NEU: Preview Umgebung https://preview-ozg-vermittlungsdienst.de<br>
>NEU: Staging Umgebung https://staging-ozg-vermittlungsdienst.de<br>
>Production Umgebung https://ozg-vermittlungsdienst.de<br>

- Integration mit neuem BKMS-Endpunkt
- Neue Benennung der Benachrichtigungs-XML-Datei im ASIC-Container: anstatt 'notice.xml' jetzt 'uuid.eforms.xml'
- Peppol-Integration mit B2Brouter
- 'PublicationID' von TED wird jetzt bearbeitet und im Vermittlungsdienst gespeichert

### Notice-Viewer
>**Umgebungen** <br>
>NEU: Preview Umgebung https://viewer.preview-ozg-vermittlungsdienst.de<br>
>NEU: Staging Umgebung https://viewer.staging-ozg-vermittlungsdienst.de<br>
>NEU: Production Umgebung https://viewer.ozg-vermittlungsdienst.de<br>

- Autorisierung und Integration mit dem Mediator
- Unterstützung von eForms-DE 1.1.0 und -DE 1.0.1
- Neuste DE-SDK-Version hinzugefügt – 1.1.0 – 1.7.1
- Entfernung von Dateien, die 24 Stunden älter sind

Verfügbar als Standalone Webservice mit Token-Authentifizierung (gleicher Token wie im Vermittlungsdienst kann genutzt werden) für Upload von XML Dateien und als Endpunkt im Vermittlungsdienst für Rendering von bereits eingelieferten Bekanntmachungen anhand der 

### eSender-Hub
- Neue Transformation von eForms-DE zu eForms-EU bezüglich 'requestedPublicationDate', ausführliche Erklärung [hier](/documentation/eForms_Erstellung.md)

### Validator
>**Umgebungen** <br>
>NEU: Preview Umgebung https://validator.preview-ozg-vermittlungsdienst.de<br>
>NEU: Staging Umgebung https://validator.staging-ozg-vermittlungsdienst.de<br>
>Production Umgebung https://ozg-vermittlungsdienst.de<br>

- Schematron Updates für eForms-DE 1.1 (https://projekte.kosit.org/eforms/eforms-de-schematron/-/releases/v0.6.2) und 1.0.1 (https://projekte.kosit.org/eforms/eforms-de-schematron/-/releases/v0.5.3)
- Token-Autorisierung für externen Validator
</details>
<br>

## Release für eForms-DE 1.1 - Vermittlungsdienst und eSender-Hub
| Umgebung Vermittlungsdienst  | Zeitraum              |  BKMS                      | Status         |
|------------|-----------------------|---------------------------|----------------|
| Preview    | **KW34** | unterstützt in Alpha      | veröffentlicht |
| Staging    | **KW35** | unterstützt in Alpha      | veröffentlicht |
| Produktion | **KW37** | unterstützt in Produktion | veröffentlicht |

Status: veröffentlicht am 13.09.2023 <br>
<details>
<summary>Release Notes</summary>

### Vermittlungsdienst
>**Umgebungen** <br>
>Preview Umgebung **bis 15.09.2023**: https://preview.ozg-vermittlungsdienst.de, ab 30.08.2023: https://preview-ozg-vermittlungsdienst.de <br>
>Staging Umgebung **bis 15.09.2023**: https://staging.ozg-vermittlungsdienst.de,  ab 30.08.2023: https://staging-ozg-vermittlungsdienst.de <br>
>Production Umgebung https://ozg-vermittlungsdienst.de<br>

- Initiale Unterstützung von eForms-DE 1.1 (Schematron https://projekte.kosit.org/eforms/eforms-de-schematron/-/releases/v0.6.0)
- Neuer DEMO Endpunkt für Visualisierung von eingelieferten eForms-DE Dokumenten /notice-viewer/{trackingCode} (gibt aktuell nur Beispieldokument zurück)
- Neuer Job für re-sync von Statusinformationen
- Diverse Verbesserungen beim Statuswechsel von Bekanntmachungen und bei der Authentifizierung

### eSender-Hub
 - Initiale eForms-DE 1.1 -> eForms-EU 1.7 Transformation  
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
