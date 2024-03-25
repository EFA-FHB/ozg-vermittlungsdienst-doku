### Datenservice Öffentlicher Einkauf
# Releases

<br />

- März 2024
  - [Hotfix Release für eForms-DE-v1.2 Patch](#Release-for-DE-1.2-patch)
- Februar 2024
  - [Release Standard eForms-DE v1.2.0 und SDK-DE](#Release-Standard-eForms-DE-v1.2.0-und-SDK-DE)
- Januar 2024
  - [Release für Vermittlungsdienst, Self-Service Portal, eSender, Notice-Viewer und Validator](#Release-für-Self-Service-Portal,-Vermittlungsdienst,-eSender,-Notice-Viewer-und-Validator)
- Dezember 2023
  - [Release für Validierung (eForms-DE 1.1 Mehrsprachigkeit)](#Release-für-Validierung)
  - [Release für Self-Service Portal, Vermittlungsdienst, eSender, Notice-Viewer und Validator](#Release-für-Self-Service-Portal,-Vermittlungsdienst,-eSender,-Notice-Viewer-und-Validator)
- November 2023
  - [Hotfix Release für Vermittlungsdienst und eSender](#Release-für-Vermittlungsdienst-und-eSender)
  - [Hotfix Release für Validator, Vermittlungsdienst und eSender](#Release-für-Validator-Mediator-und-eSender)  
  - [Hotfix Release für Notice-Viewer, Validator und Vermittlungsdienst](#Release-für-notice-Viewer-Mediator-und-Validator)
- Oktober 2023
  - [Release für Notice-Viewer - PDF Dokumente + synchrone Aufrufe](#Release-für-Notice-Viewer-PDF-Dokumente-+-synchrone-Aufrufe)
  - [Release für Self-Service Portal, Registrierungsform für einen separaten Vermittlungsdienst-Account](#Release-für-Self-Service-Portal,-Registrierungsform-für-einen-separaten-Vermittlungsdienst-Account)
- September 2023
  - [Release für RequestedPublicationDate Fix + Notice-Viewer - Vermittlungsdienst, eSender-Hub, Notice-Viewer](#Release-für-RequestedPublicationDate-Fix-+-Notice-Viewer-Vermittlungsdienst,-eSender-Hub,-Notice-Viewer)
  - [Release für eForms-DE 1.1 - Vermittlungsdienst und eSender-Hub](#Release-für-eForms-DE-1.1-Vermittlungsdienst-und-eSender-Hub)
- August 2023
  - [Release Offline-Validator für eForms-DE 1.0.1 und 1.1.0](#Release-Offline-Validator-für-eForms-DE-1.0.1-und-1.1.0)
- Juni 2023
  - [Production Release Juni - Vermittlungsdienst & eSender-Hub](#Production-Release-Juni-Vermittlungsdienst-&-eSender-Hub)
- Mai 2023
  - [Preview Release Mai - Vermittlungsdienst & Validator Webservice](#Preview-Release-Mai-Vermittlungsdienst-&-Validator-Webservice)

<br />

<a id=Release-for-DE-1.2-patch></a>
## Hotfix Release für eForms-DE-v1.2 Patch (eForms-DE 1.2 Neue Regeln)
| Umgebung Vermittlungsdienst  | Zeitraum  | Status         |
|------------|-----------------------------|----------------|
| Preview    | 25.03.2024                  | veröffentlicht |
| Staging    | 26.03.2024                  | ausstehend     |
| Produktion | 27.03.2024                  | ausstehend     |

Status: Veröffentlicht in Preview am 25.03.2024 <br>
<details>
<summary>Release Notes</summary>

### Validator (Webservice + Open-Source)
- Nutzung von eForms-DE Schematron 0.8.2 für eForms-DE 1.2 (https://projekte.kosit.org/eforms/eforms-de-schematron/-/releases/v0.8.2)

### Vermittlungsdienst
- Nutzung von eForms-DE Schematron 0.8.2 für eForms-DE 1.2 (https://projekte.kosit.org/eforms/eforms-de-schematron/-/releases/v0.8.2)
- Abschaffung der Nutzung von api-key für Authentifizierung

### Self-Service Portal 
- Aktualisieren von Erklärung der Barrierefreiheit im SSP


</details>

<a id=Release-Standard-eForms-DE-v1.2.0-und-SDK-DE></a>
## Release Standard eForms-DE v1.2.0 und SDK-DE

Die Veröffentlichung des Standards eForms-DE v1.2.0 konnte nicht wie geplant vor Weihnachten 2023 als Preview-Version veröffentlicht werden.

Die neue Release-Planung sieht wie folgt aus:

| Datum              | Beschreibung                                                 | Status     |
| ------------------ | ------------------------------------------------------------ | ------ |
| 02.02.2024         | **Release eForms-DE v1.2.0** auf Basis SDK-EU 1.10.1         | Fertig |
| 02.02 - 23.02.2024 | Feedbackphase zu eForms-DE v1.2.0 (schriftlich über eforms@finanzen.bremen.de) | Fertig |
| 23.02.2024         | **Geplante Veröffentlichung SDK-DE 1.2.0_1.10.1**            | Fertig |
| 23.02.2024         | **Geplante Unterstützung eForms-DE 1.2 in DÖE Preview (BKMS Alpha + VD Preview)** | Veröffentlicht |
| 29.02.2024         | **Geplante Unterstützung eForms-DE 1.2 in DÖE Staging (BKMS Alpha + VD Staging)** | Veröffentlicht |
| 20.03.2024         | Geplante Veröffentlichung eines Patches zu eForms-DE v1.2.0 | Fertig |
| 22.03.2024         | Geplante Veröffentlichung eines Patches zu SDK-DE 1.2.0_1.10.1 | Fertig |
| ~ 27.03.2024       | **Geplante Unterstützung eForms-DE 1.2 in DÖE Produktion** | In QS |
| **30.09.2024**     | Akzeptanz von eForms-DE v1.1.0 (basierend auf eForms-EU 1.7) läuft aus       | Ausstehend         |

**<u>Wichtig</u>: Der Datenservice Öffentlicher Einkauf (DÖE) wird sowohl die Versionen 1.2.0 von eForms-DE (bzw. die Versionen 1.2.0_1.10.1 und zukünftige Patches des SDK-DE) unterstützen.

Schriftliches Feedback zu eForms-DE **v.1.2.0** kann bis zum 23.02.2024 eingereicht werden an: eforms@finanzen.bremen.de

<details>
<summary>Release Notes</summary> 

### Self-Service Portal 
- Nachdem eine Bekanntmachung veröffentlicht wurde, werden jetzt direkte Links zum DÖE bzw. TED auf der Bekanntmachungstabelle beim Dashboard-User dargestellt
- Das Geschäftzeichen und der Titel sind jetzt auf der Bekanntmachungstabelle beim Dashboard-User dargestellt
- Diverse Fehler wurden behoben

### Vermittlungsdienst
- Unterstützung von eForms-DE 1.2 Standard wurde hinzugefügt
- Ein neuer GET _/v1/notices/by-notice/{noticeId}/{version}_ Endpunkt wurde implementiert. Jetzt kann der Status einer Bekanntmachung anhand NoticeID und Version aufgerufen werden
- Diverse Fehler wurden behoben

### eSender
- Unterstützung von eForms-DE 1.2 Standard wurde hinzugefügt
 
### Validator (Webservice + Open-Source)
- Unterstützung von eForms-DE 1.2 Standard wurde hinzugefügt

### Notice-Viewer
- Unterstützung von eForms-DE 1.2 Standard wurde hinzugefügt
- Diverse Fehler wurden behoben

<br />
</details>

<a id=Release-für-Self-Service-Portal,-Vermittlungsdienst,-eSender,-Notice-Viewer-und-Validator></a>
## Release für Vermittlungsdienst, Self-Service Portal, eSender, Notice-Viewer und Validator
| Umgebung Vermittlungsdienst  | Zeitraum  | Status         |
|------------|-----------------------------|----------------|
| Preview    | 15.01.2024        | veröffentlicht |
| Staging    | 22.01.2024        | veröffentlicht |
| Produktion | 31.01.2024        | veröffentlicht |

> **WICHTIG** <br>
Folgende eForms Versionen werden nicht mehr vom Vermittlungsdienst unterstützt:
- eForms DE-1.0.1
- eForms SDK-1.5.5

Status: Veröffentlicht am 31.01.2024<br>
<details>
<summary>Release Notes</summary> 

### Self-Service Portal 
- Umfangreiche Verbesserungen der GUI:
  - Jetzt ist es möglich von der Anmeldungseite per Knopfdruck auf die Hauptseite zurückzukehren;
  - Die Datumauswahl in der Filter wurde geändert;
  - Verbesserte Darstellung von Fehlermeldungen;
  - Anzeige des Absenders der Bekanntmachung;
  - Darstellung und Filterung von Change Notices in der Notice-Tabelle;
  - Anzeige des zugewiesenen VD-Nuzter an einem Dashboard-Nutzer;
  - Kopieren von ID's auf der Notice-Tabelle ist jetzt möglich;
  - Angemeldeter Nutzertyp wird jetzt dargestellt;
  - Nicht per E-mail bestätigte Nutzer sind jezt entsprechend gekennzeichnet;
  - Jetzt ist die SDK Version in Bekanntmachungstabelle für jede Bekanntmachung sichbar;  
- Stoppen von Bekanntmachungen in der Notice-Tabelle ist jetzt möglich
- Herunterladen der Bekanntmachungen wurde implementiert
- Editieren von E-Mail beim Dashboard-Nutzer ist nicht mehr erlaubt
- Diverse Fehler wurden behoben

### Vermittlungsdienst
- Verarbeitung von T01/02 eForms-Formularen wurde implementiert
- eForms Versionen: DE-1.0.1 und SDK 1.5.5 sind jetzt nicht mehr unterstützt
- Jetzt werden die Veröffentlichungslinks von TED und BKMS zur Verfügung gestellt
- Veralteter POST _v1/notices_ API Endpunkt wurde entfernt

### eSender
- Verarbeitung von T01/02 eForms-Formularen wurde implementiert
- Transformationen von eForms wurden geändert und verbessert
- Fehlerhandlung wurde verbessert

### Validator (Webservice + Open-Source)
- T01/02 eForms-Formulare sind jetzt unterstüzt

### Notice-Viewer
- Diverse Fehler wurden behoben

</details>

<a id=Release-für-Validierung></a>
## Hotfix Release für Validierung (eForms-DE 1.1 Mehrsprachigkeit)
| Umgebung Vermittlungsdienst  | Zeitraum  | Status         |
|------------|-----------------------------|----------------|
| Preview    | 18.11.2023                  | veröffentlicht |
| Staging    | 19.11.2023                  | veröffentlicht |
| Produktion | 20.11.2023                  | veröffentlicht |

Status: Veröffentlicht am 20.12.2023 <br>
<details>
<summary>Release Notes</summary>

### Validator (Webservice + Open-Source)
- Nutzung von eForms-DE Schematron 0.7.2 für eForms-DE 1.1 (https://projekte.kosit.org/eforms/eforms-de-schematron/-/releases/v0.7.2)
- ermöglicht volle Unterstützung von mehrsprachigen eForms-DE Dokumenten

### Vermittlungsdienst
- Nutzung von eForms-DE Schematron 0.7.2 für eForms-DE 1.1 (https://projekte.kosit.org/eforms/eforms-de-schematron/-/releases/v0.7.2)
- ermöglicht volle Unterstützung von mehrsprachigen eForms-DE Dokumenten
- Überprüfung von Annahme von Change Notices wurde verbessert


</details>

<a id=Release-für-Self-Service-Portal,-Vermittlungsdienst,-eSender,-Notice-Viewer-und-Validator></a>
## Release für Self-Service Portal, Vermittlungsdienst, eSender, Notice-Viewer und Validator
| Umgebung Vermittlungsdienst  | Zeitraum  | Status         |
|------------|-----------------------------|----------------|
| Preview    | 28.11.2023        | veröffentlicht |
| Staging    | 04.12.2023        | veröffentlicht |
| Produktion | 11.12.2023        | veröffentlicht |

Status: Veröffentlicht am 11.12.2023 <br>
<details>
<summary>Release Notes</summary>

> **Hinweis** <br>
Anmeldung auf dem Self-Service Portal mit einem Vermittlungsdienst-Nutzer*/in ist nicht mehr möglich. 

### Self-Service Portal 
- Nach der Genehmigung kann ein SSP-Nutzer*/in jetzt selbst eigene Vermittlungsdienst- und Dashboard- Nutzer*/innen erstellen
- SSP-Nutzer*/in können mehrere Vermittlungsdienst-Nutzer*/innen zu einem Dashboard-Nutzer*/in verlinken
- Alle erstellten Vermittlungsdienst- und Dashboard-Nutzer*/innen können gelöscht, bearbeitet und deaktiviert werden
- Alle übermittelten Bekanntmachungen stehen ab jetzt für den Dashboard-Nutzer*/in zur Verfügung

### Vermittlungsdienst
- Bei wiederholter Zustellung an BKMS im Fall eines Dublikates wird jetzt der richtige Status gesetzt
- Konfigurierbare Statuszuordnungstabelle implementiert
- Die Meldung wurde eingefügt, wenn der Benutzer die Benachrichtigung erfolgreich gestoppt hat
- Ablauf von Löschen der Tenant wurde geändert 
- Endpunkt für die Erstellung von Tenant und Dashboard-Benutzern verbessert
- Ein neuer PATCH Endpunkt für die Aktualisierung von eSender-Integration und Schematron-Validierung eingeführt
- Der Endpunkt zur Aktualisierung von Tenant-Benutzern in Keycloak wurde verbessert
- Change-Notice Checks werden wieder eingeführt
- Diverse Statusbeschreibungen wurden verbessert
- XSD-Fehlerdetails über die fehlgeschlagene Regel werden in die Antwort aufgenommen
- Das Validierungsmodell von 'business_document' wurde eingeführt
- Obligatorische lineDescription in PEPPOL Message (T016) wurde verbessert
- Endpunkt für Benutzererstellung/-aktualisierung wurde verbessert
- Beschreibungen für Notice Viewer Endpunkte in Swagger aktualisiert
- Die Fehlermeldung bei der Übermittlung einer Bekanntmachung wurde verbessert, um den Fehlerfall anzuzeigen
- Diverse Leistungsverbesserungen und Fehlerbehebungen 

### eSender
- Wiederholung der Zustellung ist jetzt implementiert, wenn BKMS nicht antwortet
- BKMS Integration wurde verbessert
- Diverse Leistungsverbesserungen und Fehlerbehebungen 

### Validator (Webservice + Open-Source)
- Bugfix für CR-DE-BT-165 und IssueDate angewendet
- Diverse Leistungsverbesserungen und Fehlerbehebungen  

### Notice-Viewer
- Verbessertes Rendering von BT-801, BT-92, BT-93
- Caching für generierte Dokumente eingeführt
- Platzhalter.html für gelöschte Dateien hinzugefügt
- Aktualisierte Beschreibung für Notice Viewer Endpunkt in Swagger (gilt auch für den Vermittlungsdienst)
- Diverse Leistungsverbesserungen und Fehlerbehebungen  

</details>

<a id=Release-für-Vermittlungsdienst-und-eSender></a>
## Hotfix Release für Vermittlungsdienst und eSender
| Umgebung Vermittlungsdienst  | Zeitraum  | Status         |
|------------|-----------------------------|----------------|
| Preview    | 20.11.2023        | veröffentlicht |
| Staging    | 21.11.2023        | veröffentlicht |
| Produktion | 21.11.2023        | veröffentlicht |

Status: Veröffentlicht am 21.11.2023 <br>
<details>
<summary>Release Notes</summary>

### eSender und Vermittlungsdienst
- Verbesserte technische Konfiguration der Apps und Erneuerung von Zertifikaten


</details>

<a id=Release-für-Validator-Mediator-und-eSender></a>
## Hotfix Release für Validator, Vermittlungsdienst und eSender
| Umgebung Vermittlungsdienst  | Zeitraum  | Status         |
|------------|-----------------------------|----------------|
| Preview    | 13.11.2023        | veröffentlicht |
| Staging    | 15.11.2023       | veröffentlicht |
| Produktion | 16.11.2023      | veröffentlicht |

Status: Veröffentlicht am 16.11.2023 <br>
<details>
<summary>Release Notes</summary>

### eSender
- Verbesserte Integration mit TED: wenn TED nicht verfügbar ist oder ein Timeout zu lange dauert
- Sprachproblem (BT-500-Organization-Company): mehrere Sprachen sind jetzt unterstützt
  
### Validator (Webservice + Open-Source)
- eForms SDK 1.5.5 Version wurde implementiert

### Vermittlungsdienst
- Die Anzahl der zulässigen Domain Name Zeichen beim 'authorEmail' Parameter des POST v2/notices Endpunkts wurde erhöht und unterstützt nun von 2 bis 18 Zeichen.


</details>

<a id=Release-für-notice-Viewer-Mediator-und-Validator></a>
## Hotfix Release für Notice-Viewer, Validator und Vermittlungsdienst
| Umgebung Vermittlungsdienst  | Zeitraum  | Status         |
|------------|-----------------------------|----------------|
| Preview    | 08.11.2023        | veröffentlicht |
| Staging    | 09.11.2023       | veröffentlicht |
| Produktion | 09.11.2023      | veröffentlicht |

Status: Veröffentlicht am 09.11.2023 <br>
<details>
<summary>Release Notes</summary>

### Notice-Viewer
- Improvement zur Visualisierung von monetären Werten, Komma als Trennzeichen für tausender Werte entfernt
- Erhöhung maximale Dateigröße auf 2MB
  
### Validator (Webservice + Open-Source)
- Nutzung von eForms-EU SDK 1.7.2 für eForms-DE 1.1 (https://github.com/OP-TED/eForms-SDK/releases/tag/1.7.2)
- Erhöhung maximale Dateigröße auf 2MB

### Vermittlungsdienst
- Erhöhung maximale Dateigröße auf 2MB


</details>

<a id=Release-für-Notice-Viewer-PDF-Dokumente-+-synchrone-Aufrufe></a>
## Release für Notice-Viewer - PDF Dokumente + synchrone Aufrufe
| Umgebung Vermittlungsdienst  | Zeitraum  | Status         |
|------------|-----------------------------|----------------|
| Preview    | 17.10.2023        | veröffentlicht |
| Staging    | 18.10.2023       | veröffentlicht |
| Produktion | 20.10.2023      | veröffentlicht |

> **Hinweis** <br>
> Bei der Nutzung dieses API-Endpunkts möchten wir darauf Aufmerksam machen, dass die Performance momentan noch optimiert wird. Bitte berücksichtigen Sie dies bei intensiver Anfragefrequenz und planen Sie entsprechende Toleranzen in Ihren Abläufen ein. Wir arbeiten aktiv an Verbesserungen und danken für Ihr Verständnis.

Status: Veröffentlicht am 20.10.2023 <br>
<details>
<summary>Release Notes</summary>

### Notice-Viewer
>**Umgebungen** <br>
> Preview https://viewer.preview-ozg-vermittlungsdienst.de <br>
> Staging https://viewer.staging-ozg-vermittlungsdienst.de <br>
> Production https://viewer.ozg-vermittlungsdienst.de<br>

- Rückwärtskompatibilität mit ursprünglichem `/view` Endpunkt
- Neue Endpunkte für asynchrone HTML und PDF Generierung, gleiches Verhalten wie bisheriger `view` Endpunkt, Response wird sofort zurückgegeben, Dokument wird im Hintergrund erstellt. 
  - `/view/async/html` und `/view/async/pdf`
- Neue Endpunkte für synchrone HTML und PDF Generierung, Response mit Link wird erst zurückgegeben, wenn Dokument erstellt ist.
  - `/view/sync/html` und `/view/sync/pdf`

</details>

<a id=Release-für-Self-Service-Portal,-Registrierungsform-für-einen-separaten-Vermittlungsdienst-Account></a>
## Release für Self-Service Portal, Registrierungsform für einen separaten Vermittlungsdienst-Account
| Umgebung Vermittlungsdienst  | Zeitraum  | Status         |
|------------|-----------------------------|----------------|
| Preview    | Doku + Registrierungsformular: **KW38** , Statusübersicht: **KW39**         | veröffentlicht |
| Staging    | Doku + Registrierungsformular: **KW39**  , Statusübersicht: **KW40**        | veröffentlicht |
| Produktion | Doku + Registrierungsformular: **KW40** , Statusübersicht **KW41**          | veröffentlicht |

Status: Veröffentlicht am 4.10.2023 <br>
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

<a id=Release-für-RequestedPublicationDate-Fix-+-Notice-Viewer-Vermittlungsdienst,-eSender-Hub,-Notice-Viewer></a>
## Release für RequestedPublicationDate Fix + Notice-Viewer - Vermittlungsdienst, eSender-Hub, Notice-Viewer
| Umgebung Vermittlungsdienst  | Zeitraum              | BKMS                      | Status |
|------------|-----------------------|---------------------------|--------|
| Preview    | nur RequestedPublicationDate Fix: **KW37**,  Alles andere: **KW39**                 | unterstützt in Alpha      | veröffentlicht |
| Staging    | verschoben: **KW40**    | unterstützt in Alpha      | veröffentlicht |
| Produktion | verschoben: **KW41**                  | unterstützt in Produktion | veröffentlicht |

Status: veröffentlicht am 11.10.2023 <br>
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
- Neue Transformation von eForms-DE zu eForms-EU bezüglich 'requestedPublicationDate', ausführliche Erklärung [hier](/documentation/eForms_creation.md)

### Validator
>**Umgebungen** <br>
>NEU: Preview Umgebung https://validator.preview-ozg-vermittlungsdienst.de<br>
>NEU: Staging Umgebung https://validator.staging-ozg-vermittlungsdienst.de<br>
>Production Umgebung https://ozg-vermittlungsdienst.de<br>

- Schematron Updates für eForms-DE 1.1 (https://projekte.kosit.org/eforms/eforms-de-schematron/-/releases/v0.6.2) und 1.0.1 (https://projekte.kosit.org/eforms/eforms-de-schematron/-/releases/v0.5.3)
- Token-Autorisierung für externen Validator
</details>
<br>

<a id=Release-für-eForms-DE-1.1-Vermittlungsdienst-und-eSender-Hub></a>
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

<a id=Release-Offline-Validator-für-eForms-DE-1.0.1-und-1.1.0></a>
## Release Offline-Validator für eForms-DE 1.0.1 und 1.1.0
Status: Veröffentlicht 14.08.2023<br>
https://github.com/EFA-FHB/eforms-validator-core/releases/tag/1.0.3
<br><br>

<a id=Production-Release-Juni-Vermittlungsdienst-&-eSender-Hub></a>
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

<a id=Preview-Release-Mai-Vermittlungsdienst-&-Validator-Webservice></a>
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
