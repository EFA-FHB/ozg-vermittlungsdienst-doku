**EfA-Umsetzungsprojekt "Zugang zur öffentlichen Vergabe"**
### Dokumentation Vermittlungsdienst
[Inhaltsverzeichnis](/documentation/documentation.md)
<br>

# Self-Service Portal des DöE

Unter der URL https://portal.ozg-vermittlungsdienst.de/ ist der Self-Serivce Portal des Datenservice Öffentlicher Einkauf für die Produktionsumgebung verfügbar.
Des weiteren gibt es das Portal für die Staging Umgebung https://portal.staging-ozg-vermittlungsdienst.de/ und das Portal für die Preview Umgebung https://portal.preview-ozg-vermittlungsdienst.de/. 
<br><br>
Das Self-Service-Portal (SSP) bietet einen benutzerfreundlichen Zugang zu allen [Unterlagen](https://portal.ozg-vermittlungsdienst.de/documentation) des Datenservice Öffentlicher Einkauf (DöE).

Das Portal wird ein Betriebs- und Supportplattform für Nutzer. Es wird Ihnen bei der Übergang helfen und erlaubt Ihnen, von Emails wegkommen. Es bietet zukünftig mehr Möglichkeiten, Nutzer und Zugang selbst zu verwalten.

## Ab 11.12.23: Rollen in SSP
### Wichtige Informationen zum Release am 11.12.
Am 11.12. gibt es ein neues release des SSP. Ihr technischer VD-Account wird ab diesem Zeitpunkt nicht mehr zum Login im SSP funktionieren, sondern dient nur noch zur technischen Authentifizierung des Systems. Sie müssen sich im Portal einen Nutzer anlegen. Klicken Sie dazu im Portal einfach auf „Registrieren“ und erstellen Sie sich einen neuen Account. Wenn Sie bereits einen SSP Portal Account besitzen, können Sie diesen nutzen. Ab 11.12. können Sie diesen Nutzer dann über einen neuen Prozess verifizieren. Im Verifizierungsprozess können Sie dann ebenfalls ein PDF mit einer Verpflichtungserklärung hochladen. Hierfür gibt es aber keine feste Vorlage. Das Dokument dient nur dazu, dass Sie uns gegenüber versichern, dass Sie befugt sind, Accounts für Ihre Firma als Fachverfahrenshersteller zu verwalten. Bitte senden Sie uns nach Erstellung Ihres Accounts schnellstmöglich eine Liste all Ihrer technischen VD-Accounts (bestehende Accounts von einliefernden Systemen), welche von diesem neuen SSP Admin Account verwaltet werden sollen. Die Liste soll die jeweilige VD-Account-Email und die zugehörige Plattform URL enthalten und an versendet werden, damit wir Ihren Account entsprechend mit den VD-Systemaccounts verknüpfen können. Nach Verifizierung Ihres SSP Admin Accounts können Sie wie ebenfalls im FVH Treffen erläutert mit diesem Account sogenannte Dashboard Accounts mit eigener Email und Passwort erstellen. Sie können für jeden Dachboard-Nutzer explizit auswählen, von welchen einliefernden Systemen (VD-Accounts) dieser Nutzer die Bekanntmachungen einsehen können soll. WICHTIG: Nur Dashboard-User können die Bekanntmachungstabelle sehen, NICHT SSP Admin User oder VD-Accounts. Sie müssen sich also ggf. als SSP Admin zusätzlich einen Dashboard User einrichten, wenn Sie selbst die Bekanntmachungsübersicht sehen möchten.

### Rollen-Übersicht
Ab 11.12.23 werden folgende Rollen im Self-Service-Portal existieren:
| Rolle im SSP        | Beschreibung | In SSP verfügbare Aktionen |
|---------------------|--|--|
| SSP (-Admin)-Nutzer | Verantwortlich für alle Nutzeraccounts der FVH; Admin für den FVH <br> Muss von Support verifiziert sein, um alle Nutzerverwaltung Rechte freizuschalten <br><br> <b>Wichtig: Um alle Funktionen der Nutzerverwaltung freizuschalten, müssen Sie uns mitteilen, welcher VD-Account mit Ihrem SSP-Admin-Account verknüpft sein soll</b> | <ul><li>Anlegen von neuen VD-Accounts (Anbindungen an den Vermittlungsdienst)</li> <li>Anlegen von neuen Dashboard-Nutzer</li><li> Nutzerverwaltung für Ihre eigene Organisation</li><li>Dokumentation ansehen</li></ul>|
| Dashboard-Nutzer    | Service-Mitarbeiterin/Kundenbetreuungskonto mit Übersicht aller Bekanntmachungen der verknüpften VD-Accounts | <ul><li>Übersicht über alle Bekanntmachungen der verknüpften VD-Accounts</li> <li>Ein Nutzer kann mit mehreren VD-Accounts verknüpft sein</li><li>Dokumentation ansehen</li></ul>| |
| VD-Account          | Nur für die technische Anbindung an den Vermittlungsdienst | <ul><li>Darf in SSP nicht einloggen</li><li>Dokumentation ansehen</li></ul> |


## Verfügbare Services
### Ab Oktober 2023:
Das Portal bietet folgende Hauptfunktionen:
* Dokumentation ansehen
  * *Es wird langfristig geplant, die Dokumentation, die sich derzeit in Github befindet, in das Portal zu übertragen. Das SSP wird dann später zu zentraler Kommunikationskanal fürs DöE*
* Eigenes Anlegen von Admin-Account in SSP für Fachverfahrenshersteller (SSP-Admin-Accounts)
* Mit SSP-Admin-Account VD-Nutzer beantragen (ersetzt die Account-Erstellung per E-Mail)
* Übersicht von Bekanntmachungen ansehen
<br>

### Zukünftige geplante Features (Umsetzung 2023):
* SSP-Admin-Account kann Nutzerverwaltung und Rechtevergabe durchführen (z.B. Nutzer anlegen, die Bekanntmachungen einsehen können)
* Erweitertes Management technischer VD-Accounts (z.B. Passwort für angebundene Systeme zurücksetzen)

## Benutzerinformationen
### Konto anlegen
Um ein Konto in SSP anzulegen, klicken Sie bitte oben rechts auf das Benutzer-Icon und wählen Sie "Registrieren". Anschließend haben Sie die Möglichkeit, ein Konto mit einer E-Mail-Adresse und einem Passwort anzulegen. Eine Bestätigungsemail wird in Kürze an die eingegebene E-Mail-Adresse gesendet. Bitte bestätigen Sie Ihr Konto mit dem enthaltenen Link. Danach können Sie sich mit Ihren Zugangsdaten einloggen und haben Zugriff auf das Registrierungsformular für eine Vermittlungsdienst-Anbindung.

### Neuen technischen VD-Account beantragen
Nachdem ein Admin-Konto in SSP angelegt wurde (siehe oben) und der Nutzer eingeloggt ist, kann er das Formular für die Beantragung eines technischen VD-Accounts ausfüllen. Die Möglichkeit dazu finden Sie im Menü oben links unter "Registrierung". Das Formular wird an den Support zur Prüfung und gegebenenfalls zur Genehmigung gesendet. Nach erfolgreicher Genehmigung wird eine Email an die eingegebene Email-Adresse mit den Kontodetails geschickt.

### Gesendete Bekanntmachungen (Notice Tabelle) ansehen
Nachdem Sie ein bestätigtes VD-Account für den Versand von Bekanntmachungen an das DöE haben, können Sie mit den Zugangsdaten* im Portal anmelden. Wenn Sie dann im Menü oben Links auf "Bekanntmachungen" klicken, haben Sie Zugriff auf eine Tabelle mit allen von diesem Konto gesendeten Bekanntmachungen sowie deren aktuellen Status.

**Bitte beachten Sie: Dies sind die technischen Daten und die Anmeldung zur SSP damit dient als Übergangslösung und ist nicht langfristig geplant. Zu einem späteren Zeitpunkt werden separate Zugangsdaten für die Übersichtstabelle verwendet, und diese technischen Daten sollten ausschließlich für den Versand von Bekanntmachungen verwendet werden.*

## Zukünftige geplante Features
In Zukunft werden diese Nutzerprozesse anders gestaltet sein. Die Account-Struktur wird dem SSP-Admin-Nutzer des Fachverfahrensherstellers mehr Rechte und administrative Funktionen ermöglichen.

Zunächst muss der SSP-Admin-Nutzer verifiziert sein. Der Nutzer füllt ein Formular aus, in dem er nachweist, dass er für den Fachverfahrenshersteller verantwortlich ist. Diese Überprüfung erfolgt noch manuell durch den Support.

Nach erfolgreicher Verifizierung kann der SSP-Admin-Nutzer VD-Accounts ohne weitere Prüfung erstellen und sein eigenes Account-Struktur dazu anpassen.

Zusätzlich wird es separate Dashboard-Nutzer geben, unabhängig von den technischen VD-Accounts. Diese Nutzer werden vom SSP-Admin erstellt und mit einem technischen VD-Account verknüpft sein und erhalten dadurch Zugriff auf eine Übersicht der Bekanntmachungen aus ihrem zugeordneten VD-Account im Portal.
