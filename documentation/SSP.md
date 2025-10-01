
### Datenservice Öffentlicher Einkauf
[Inhaltsverzeichnis](/documentation/documentation.md)
<br>

# Self-Service-Portal des Datenservice Öffentlicher Einkauf

Unter der URL https://portal.ozg-vermittlungsdienst.de/ ist das Self-Service-Portal des Datenservice Öffentlicher Einkauf für die Produktionsumgebung verfügbar.
Des Weiteren gibt es das Portal für die Staging-Umgebung https://portal.staging-ozg-vermittlungsdienst.de/ und das Portal für die Preview-Umgebung https://portal.preview-ozg-vermittlungsdienst.de/. 
<br><br>
Das Self-Service-Portal (SSP) bietet als Betriebs- und Supportplattform einen benutzerfreundlichen Zugang zu allen [Unterlagen](https://portal.ozg-vermittlungsdienst.de/documentation) des Datenservice Öffentlicher Einkauf (DÖE).

## Rollen im SSP
### Wichtige Informationen zum Release am 11.12.2023

Für den Login im Portal muss Nutzer angelegt werden, indem über einen Klick auf 'Registrieren' ein neuer Account erstellt wird. Ist bereits einen SSP-Portal-Account vorhanden, kann dieser genutzt werden. Dieser Nutzer kann nun über einen neuen Prozess verifizieren. Im Verifizierungsprozess kann ebenfalls ein PDF mit einer Verpflichtungserklärung hochgeladen werden. Hierfür gibt es aber keine feste Vorlage. Mit diesem Dokument wird versichert, dass die dort benannte Person befugt ist, Accounts für ihre Firma als Fachverfahrenshersteller zu verwalten.

> **WARNUNG** <br>
> Für den SSP-Admin-Account bitte die E-Mail-Adresse eines Postfachs nutzen, jedoch keine persönliche, damit auch andere Personen aus der Organisation die Vermittlungsdienst-Accounts und Dashboard-Accounts verwalten können.
> Der SSP-Admin-Account ist per 2FA per E-Mail geschützt, weshalb für berechtigte Personen der Zugriff auf das Postfach unbedingt notwendig ist.

Nach Verifizierung des SSP-Admin-Accounts können mit diesem Account sogenannte Dashboard-Nutzer und Vermittlungsdienst-Nutzer mit eigener E-Mail und Passwort erstellt werden. Für jeden Dashboard-Nutzer kann explizit ausgewählt werden, von welchen einliefernden Systemen (Vermittlungsdienst-Accounts) dieser Nutzer die Bekanntmachungen einsehen können soll.

> **TIP** <br>
> Nur Dashboard-Nutzer können die Bekanntmachungstabelle sehen, NICHT SSP-Admin-User oder Vermittlungsdienst-Nutzer. Für einen SSP-Admin muss somit zusätzlich einen Dashboard-Nutzer mit einer separaten E-Mail-Adresse eingerichtet werden, wenn er selbst die Bekanntmachungsübersicht sehen möchte.

### Rollen-Übersicht

> **WICHTIG** <br>
> Alle Accounts brauchen eine einzigartige E-Mail-Adresse. Es wird empfohlen, für den SSP-Admin-Account KEINE persönlichen E-Mail-Adressen zu nutzen!

Folgende Rollen gibt es im Self-Service-Portal:
| Rolle im SSP        | Beschreibung | In SSP verfügbare Aktionen |
|---------------------|--|--|
| SSP-Admin | Verantwortlich für alle Nutzeraccounts der FVH; Admin für den FVH <br> Muss von Support verifiziert sein, um alle Nutzerverwaltungsrechte freizuschalten <br><br> <b>Wichtig: Um alle Funktionen der Nutzerverwaltung freizuschalten, müssen Sie uns mitteilen, welcher VD-Account mit Ihrem SSP-Admin-Account verknüpft sein soll</b> | <ul><li>Anlegen von neuen VD-Accounts (Anbindungen an den Vermittlungsdienst)</li> <li>Anlegen von neuen Dashboard-Nutzern</li><li> Nutzerverwaltung für Ihre eigene Organisation</li><li>Dokumentation ansehen</li></ul>|
| Dashboard-Nutzer    | Service-Mitarbeiterin/Kundenbetreuungskonto mit Übersicht aller Bekanntmachungen der verknüpften VD-Accounts | <ul><li>Übersicht über alle Bekanntmachungen der verknüpften VD-Accounts</li> <li>Ein Nutzer kann mit mehreren VD-Accounts verknüpft sein</li><li>Dokumentation ansehen</li></ul>| |
| VD-Account          | Nur für die technische Anbindung an den Vermittlungsdienst | <ul><li>Dokumentation ansehen</li></ul> |

## Verfügbare Services

Das Portal bietet folgende Hauptfunktionen:
* Dokumentation ansehen
* Anlegen von Admin-Accounts im SSP für Fachverfahrenshersteller (SSP-Admin-Accounts)
* Nach erfolgreicher Verifizierung: Mit SSP-Admin-Account VD-Accounts und Dashboard-Benutzer anlegen (ersetzt die Account-Erstellung per E-Mail)
* Mit Dashboard-Nutzer-Account: Übersicht von Bekanntmachungen ansehen
* SSP-Admin-Account kann Nutzerverwaltung und Rechtevergabe durchführen (z.B. Nutzer anlegen, die Bekanntmachungen einsehen können) <br>

## Benutzerinformationen
### Konto anlegen
Um ein Konto im SSP anzulegen, reicht ein Klick oben rechts auf das Benutzer-Icon mit anschließender Auswahl von "Registrieren". Anschließend besteht die Möglichkeit, ein Konto mit einer E-Mail-Adresse und einem Passwort anzulegen. Eine Bestätigungs-E-Mail wird kurz darauf an die eingegebene E-Mail-Adresse gesendet. Über den dort enthaltenen Link kann die Anlage des Kontos bestätigt werden. Danach ist mit den Zugangsdaten das Einloggen möglich und es besteht Zugriff auf das Registrierungsformular für eine Verifizierung als SSP-Admin. Das Formular wird an den Support zur Prüfung gesendet.

### Neuen technischen Vermittlungsdienst-Account anlegen
Nachdem ein Admin-Konto im SSP angelegt und vom Support verifiziert wurde (siehe oben) und der Nutzer eingeloggt ist, kann er das Formular für die Anlage eines technischen Vermittlungsdienst-Accounts ausfüllen. Dieses geschieht auf der Startseite und im Menü oben links unter „Registrierung VD-Account". Eine E-Mail mit den Kontodetails wird anschließend an die eingegebene E-Mail-Adresse geschickt.

### Neuen Dashboard-User anlegen
Es besteht auch die Möglichkeit, neue Dashboard-User anzulegen. Dazu muss der SSP-Admin-User zur "Registrierung Dashboard-User" navigieren und das Formular ausfüllen. Unter "Verknüpfter VD-Account" können ein oder mehrere VD-Accounts ausgewählt sein. Eine E-Mail wird an die eingegebene E-Mail-Adresse mit den Kontodetails geschickt und der Dashboard-User kann sich anmelden und alle von dem verknüpften Konto gesendeten Benachrichtigungen sowie deren aktuellen Status einsehen. 

### Gesendete Bekanntmachungen (Notice-Tabelle) ansehen
Mit einem Dashboard-User-Account (siehe oben) kann man sich im Portal anmelden und alle von dem verknüpften Konto bzw. den verknüpften Kontos gesendeten Benachrichtigungen sowie deren aktuellen Status und (falls vorhanden) Fehlermeldungen einsehen. Der Dashboard-User kann auch die XML-Datei aus der Tabelle der eingereichten Bekanntmachungen herunterladen und mit einem konfigurierbaren Recht Bekanntmachungen in der Notice-Tabelle stoppen.
