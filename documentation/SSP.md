
### Datenservice Öffentlicher Einkauf
[Inhaltsverzeichnis](/documentation/documentation.md)
<br>

# Self-Service-Portal des DÖE

Unter der URL https://portal.ozg-vermittlungsdienst.de/ ist das Self-Serivce-Portal des Datenservice Öffentlicher Einkauf für die Produktionsumgebung verfügbar.
Des Weiteren gibt es das Portal für die Staging-Umgebung https://portal.staging-ozg-vermittlungsdienst.de/ und das Portal für die Preview-Umgebung https://portal.preview-ozg-vermittlungsdienst.de/. 
<br><br>
Das Self-Service-Portal (SSP) bietet einen benutzerfreundlichen Zugang zu allen [Unterlagen](https://portal.ozg-vermittlungsdienst.de/documentation) des Datenservice Öffentlicher Einkauf (DÖE).

Das Portal wird eine Betriebs- und Supportplattform für Nutzer. Es wird Ihnen beim Übergang helfen und erlaubt Ihnen, von E-Mails wegzukommen. Es bietet zukünftig mehr Möglichkeiten, Nutzer und Zugang selbst zu verwalten.

## Ab 11.12.23: Rollen im SSP
### Wichtige Informationen zum Release am 11.12.


Am 11.12. gibt es ein neues Release des SSP. Ihr technischer VD-Account wird ab diesem Zeitpunkt nicht mehr zum Login im SSP funktionieren, sondern dient nur noch zur technischen Anbindung an Vermittlungsdienst, Validator und Viewer. 
<br> <br>Für den Login im Portal müssen Sie sich einen Nutzer anlegen. Klicken Sie dazu im Portal einfach auf „Registrieren“ und erstellen Sie sich einen neuen Account. Wenn Sie bereits einen SSP-Portal-Account besitzen, können Sie diesen nutzen. Sie können jetzt diesen Nutzer über einen neuen Prozess verifizieren. Im Verifizierungsprozess können Sie ebenfalls ein PDF mit einer Verpflichtungserklärung hochladen. Hierfür gibt es aber keine feste Vorlage. Das Dokument dient nur dazu, dass Sie uns gegenüber versichern, dass Sie befugt sind, Accounts für Ihre Firma als Fachverfahrenshersteller zu verwalten.

> **WARNUNG** 
> Für den SSP-Admin-Account bitte die E-Mail-Adresse eines Postfachs nutzen, keine persönliche, damit auch andere Personen aus Ihrer Organisation die VD-Accounts und Dashboard-Accounts verwalten können.
> Der SSP-Admin-Account ist per 2FA per E-Mail geschützt, weshalb für berechtigte Personen der Zugriff auf das Postfach unbedingt notwendig ist.

Bitte senden Sie uns nach Erstellung Ihres Accounts schnellstmöglich eine Liste all Ihrer technischen VD-Accounts (bestehende Accounts von einliefernden Systemen), welche von diesem neuen SSP-Admin-Account verwaltet werden sollen. Die Liste soll die jeweilige VD-Account-E-Mail und die zugehörige Plattform-URL enthalten und an Support versendet werden, damit wir Ihren Account entsprechend mit den VD-Systemaccounts verknüpfen können.
<br><br>Nach Verifizierung Ihres SSP-Admin-Accounts können Sie mit diesem Account sogenannte Dashboard-Nutzer mit eigener E-Mail und Passwort erstellen. Sie können für jeden Dashboard-Nutzer explizit auswählen, von welchen einliefernden Systemen (VD-Accounts) dieser Nutzer die Bekanntmachungen einsehen können soll.

> **TIP**
> Nur Dashboard-Nutzer können die Bekanntmachungstabelle sehen, NICHT SSP-Admin-User oder VD-Accounts. Sie müssen sich also ggf. als SSP-Admin zusätzlich einen Dashboard-Nutzer mit einer separaten E-Mail Adresse einrichten, wenn Sie selbst die Bekanntmachungsübersicht sehen möchten.

### Rollen-Übersicht

> **WICHTIG**
> Alle Accounts brauchen eine einzigartige E-Mail-Adresse. Wir empfehlen, für den SSP-Admin-Account KEINE persönlichen E-Mail-Adressen zu nutzen!

Ab 11.12.23 werden folgende Rollen im Self-Service-Portal existieren:
| Rolle im SSP        | Beschreibung | In SSP verfügbare Aktionen |
|---------------------|--|--|
| SSP-Admin | Verantwortlich für alle Nutzeraccounts der FVH; Admin für den FVH <br> Muss von Support verifiziert sein, um alle Nutzerverwaltungsrechte freizuschalten <br><br> <b>Wichtig: Um alle Funktionen der Nutzerverwaltung freizuschalten, müssen Sie uns mitteilen, welcher VD-Account mit Ihrem SSP-Admin-Account verknüpft sein soll</b> | <ul><li>Anlegen von neuen VD-Accounts (Anbindungen an den Vermittlungsdienst)</li> <li>Anlegen von neuen Dashboard-Nutzern</li><li> Nutzerverwaltung für Ihre eigene Organisation</li><li>Dokumentation ansehen</li></ul>|
| Dashboard-Nutzer    | Service-Mitarbeiterin/Kundenbetreuungskonto mit Übersicht aller Bekanntmachungen der verknüpften VD-Accounts | <ul><li>Übersicht über alle Bekanntmachungen der verknüpften VD-Accounts</li> <li>Ein Nutzer kann mit mehreren VD-Accounts verknüpft sein</li><li>Dokumentation ansehen</li></ul>| |
| VD-Account          | Nur für die technische Anbindung an den Vermittlungsdienst | <ul><li>Darf sich in SSP nicht einloggen</li><li>Dokumentation ansehen</li></ul> |


## Verfügbare Services

Das Portal bietet folgende Hauptfunktionen:
* Dokumentation ansehen
  * *Es wird langfristig geplant, die Dokumentation, die sich derzeit in Github befindet, in das Portal zu übertragen. Das SSP wird dann später zum zentralen Kommunikationskanal fürs DÖE*
* Eigenes Anlegen von Admin-Accounts im SSP für Fachverfahrenshersteller (SSP-Admin-Accounts)
* Nach erfolgreicher Verifizierung: Mit SSP-Admin-Account VD-Accounts und Dashboard-Benutzer anlegen (ersetzt die Account-Erstellung per E-Mail)
* Mit Dashboard-Nutzer-Account: Übersicht von Bekanntmachungen ansehen
* SSP-Admin-Account kann Nutzerverwaltung und Rechtevergabe durchführen (z.B. Nutzer anlegen, die Bekanntmachungen einsehen können) <br>

## Benutzerinformationen
### Konto anlegen
Um ein Konto im SSP anzulegen, klicken Sie bitte oben rechts auf das Benutzer-Icon und wählen Sie "Registrieren". Anschließend haben Sie die Möglichkeit, ein Konto mit einer E-Mail-Adresse und einem Passwort anzulegen. Eine Bestätigungs-E-Mail wird in Kürze an die eingegebene E-Mail-Adresse gesendet. Bitte bestätigen Sie Ihr Konto mit dem enthaltenen Link. Danach können Sie sich mit Ihren Zugangsdaten einloggen und haben Zugriff auf das Registrierungsformular für eine Verifizierung als SSP-Admin. Das Formular wird an den Support zur Prüfung und gegebenenfalls zur Genehmigung gesendet.

### Neuen technischen VD-Account anlegen
Nachdem ein Admin-Konto im SSP angelegt und vom Support verifiziert wurde (siehe oben) und der Nutzer eingeloggt ist, kann er das Formular für die Anlegung eines technischen VD-Accounts ausfüllen. Die Möglichkeit dazu finden Sie auf der Startseite und im Menü oben links unter "Registrierung VD-Account". Eine E-Mail wird an die eingegebene E-Mail-Adresse mit den Kontodetails geschickt.

### Neuen Dashboard-User anlegen
Es besteht auch die Möglichkeit, neue Dashboard-User anzulegen. Dazu muss der SSP-Admin-User zur "Registrierung Dashboard-User" navigieren und das Formular ausfüllen. Unter "Verknüpfter VD-Account" können ein oder mehrere VD-Accounts ausgewählt sein. Eine E-Mail wird an die eingegebene E-Mail-Adresse mit den Kontodetails geschickt und der Dashboard-User kann sich anmelden und alle von dem verknüpften Konto gesendeten Benachrichtigungen sowie deren aktuellen Status einsehen. 

### Gesendete Bekanntmachungen (Notice-Tabelle) ansehen
Mit einem Dashboard-User-Account (siehe oben) kann man sich im Portal anmelden und alle von dem verknüpften Konto bzw. Kontos gesendeten Benachrichtigungen sowie deren aktuellen Status und (falls vorhanden) Fehlermeldungen einsehen. Der kann auch die XML-Datei aus der Tabelle der eingereichten Bekanntmachungen herunterladen und mit einem konfigurierbaren Recht Bekanntmachungen in der Notice-Tabelle stoppen.
