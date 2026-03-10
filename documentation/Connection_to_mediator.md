[Inhaltsverzeichnis](/documentation/documentation.md)
<br>

>**Hinweis** <br>
>Bitte beachten: Wenn unterschwellige Bekanntmachungen weiterhin an service.bund.de gesendet werden, dürfen diese NICHT zusätzlich an den Vermittlungsdienst gesendet werden!

# Anbindung an den Vermittlungsdienst
Die Übermittlung von Bekanntmachungen an den Vermittlungsdienst kann über die [REST-API](#anbindung-per-rest-api) des Vermittlungsdienst oder über das [eDelivery-Network PEPPOL](#anbindung-per-peppol) erfolgen.
<br>

## Anbindung per REST-API
Unter https://ozg-vermittlungsdienst.de werden die REST-API und die dazugehörige Dokumentation der vorhandenen Endpoints zur Verfügung gestellt.
Für die Nutzung der API müssen einmalig Zugangsdaten beantragt werden. Die Autorisierung erfolgt über OAuth 2.0.
<br>

### Beantragen eines Accounts zum Einliefern von Bekanntmachungen

Die Einrichtung eines neuen Accounts erfolgt über das Self-Service-Portal (Produktionsumgebung: https://self-service.datenservice-oeffentlicher-einkauf.de). Ein Konto kann im Portal erstellt werden, indem eine E-Mail-Adresse und ein Passwort festgelegt werden. Nach Bestätigung der E-Mail-Adresse kann der Nutzer sich anmelden und das Antragsformular für einen neuen VD-Account ausfüllen. Pro Vergabeplattform ist ein separater Benutzer notwendig. <br>

Nach der Erstellung des Benutzers wird zur Überprüfung an die angegebene Benutzer-E-Mail-Adresse eine Authentifizierungs-E-Mail versendet, welche einen Link zur Authentifizierung und zur Erstellung des Passworts enthält. Werden z.B. 10 Accounts für eine Umgebung beantragt, werden auch 10 individuelle E-Mail-Adressen benötigt. Die E-Mail-Adresse dient zum Abruf der Tokens, die zur eindeutigen Authentifizierung mit dem Account erforderlich sind. Deshalb muss E-Mail-Adresse einzigartig sein.
<br><br>
Der Link ist 10 Tage gültig.<br>
Nach einem Klick auf den Link erscheinen Anweisungen zur Passwort-Erstellung.
<br><br>
Mit den erstellten Zugangsdaten können mit Hilfe der API ein Access-Token und ein Refresh-Token generiert werden.
<br><br>
Es ist zu beachten, dass pro Entwicklungsumgebung (Preview, Staging, Produktion) ein Zugang zu beantragen ist. Es wird keine Synchronisierung der Zugangsdaten durchgeführt. [Preview](https://self-service.preview.datenservice-oeffentlicher-einkauf.de/)- und [Staging](https://self-service.staging.datenservice-oeffentlicher-einkauf.de/)-Accounts können in der entsprechenden Self-Service-Portalumgebung angefordert werden.
<br>

### Authentifizierung und Autorisierung (Access-Token, Refresh-Token)
Der Endpunkt `POST /api/token` wird mit den zu übergebenden Parametern `username` und `password` genutzt, um einen `access_token` und `refresh_token` zu erhalten. `username` ist hierbei die angegebene E-Mail-Adresse. 

Der `access_token` ist 24 Stunden gültig und kann bei allen folgenden Anfragen im Header folgendermaßen zur Autorisierung genutzt werden: `Authorization: Bearer <<access_token>>`. Nach Ablauf der 24 Stunden ist eine erneute Authentifizierung nötig. Um eine regelmäßige Authentifizierung mit `username` und `password` zu vermeiden, kann mit Hilfe des `refresh_token` und dem Endpunkt `POST /api/token/refresh` ein neuer `access_token` generiert werden, ohne eine erneute vollständige Authentifizierung durchführen zu müssen. 

Durch das Anfragen eines neuen Tokens, wird der vorige Token nicht invalidiert. 

Beispielantwort der Endpunkte `POST /api/token` und `POST /api/token/refresh`: 

```
{
  "access_token": "eyJhbGciOikpXVCJ9.eyJzMDIyfQ.SflKxwRJSM",
  "expires_in": 36000,
  "refresh_expires_in": 36000,
  "refresh_token": "eyJhbGciOikpXVCJ9.eyJzMDIyfQ.SflKxwRJSM",
  "token_type": "Bearer",
  "not-before-policy": 0,
  "session_state": "e65f24ae-4e90-4635-8ae7-4fb89fe471bf",
  "scope": "profile email"
}
```
<br>

Weitere Informationen zum Konzept des Refresh-Token und Hinweise zur Umsetzung werden unter https://auth0.com/blog/refresh-tokens-what-are-they-and-when-to-use-them/ zur Verfügung gestellt.
<br>


## Anbindung per PEPPOL

Die Einlieferung von Bekanntmachungen an den **Datenservice Öffentlicher Einkauf** kann von Vergabeplattformen auch über die **Peppol-Infrastruktur** erfolgen.

### Nutzung der Peppol-Infrastruktur
In der Peppol-Infrastruktur registrierte Systeme können unter Verwendung des **Peppol-Profils „P008 – Publish Notices“** Bekanntmachungen an den Adressaten mit der **Peppol-ID „0204:994-DOEVD-83“ (Produktion)** senden.

- Weitere Informationen zum Peppol-Profil sind hier zu finden: [Peppol Documentation - Publish Notices](https://peppol.org/documentation/technical-documentation/pre-award-documentation)

### Kommunikation
Die Kommunikation erfolgt über die Verwendung eines **pre-award-fähigen AccessPoints**, der entweder
- von kommerziellen Anbietern bereitgestellt wird oder
- eigenständig Peppol-konform implementiert werden kann (ggf. auf Basis von Open Source).

**Wichtig:** Zur vollständigen pre-award-Fähigkeit des AccessPoints gehört die Unterstützung von **„REM Evidence“**, wie in der Dokumentation unter folgendem Link beschrieben:  
[Peppol BIS eDelivery Guide for Pre-Award v1.3](https://docs.peppol.eu/pracc/files/BIS-eDelivery-guide-for-pre-award-v1.3.pdf)

### Registrierung
Fragen zur Registrierung sind über eine **Peppol-Authority** zu klären:  
[Liste der Peppol-Authorities](https://peppol.org/members/peppol-authorities)

### Verbindung von Vergabeplattformen mit dem Vermittlungsdienst über PEPPOL

Die primäre Schnittstelle für die Übermittlung von Bekanntmachungen ist das PEPPOL-Netzwerk. Bekanntmachungen können wie folgt übermittelt werden:

### PEPPOL-Adresse des Vermittlungsdienstes (Participant ID)
- **Produktivumgebung**: `0204:994-doevd-83`
- **Staging**: `0204:994-doevdtest-85`

#### Übermittlung über den Geschäftsprozess mit der ID:
- `urn:fdc:peppol.eu:prac:bis:p008:1.2`
  - **Senden**: Der Sender übermittelt eine *Publish Notice Request* (Transaction ID: `urn:fdc:peppol.eu:prac:trns:t015:1.2`).
  - **Empfangen**: Der Vermittlungsdienst sendet eine *Notice Publication Response* (Transaction ID: `urn:fdc:peppol.eu:prac:trns:t016:1.2`).

### SMP Inbox Document Owner:
- **Produktivumgebung**: `oeffentliche-vergabe-peppol`
- **Staging**: `oeffentliche-vergabe-peppol-test`

#### URL:
- **Produktivumgebung**: [https://ws.b2brouter.com/transactions](https://ws.b2brouter.com/transactions)
- **Staging**: [https://ws-staging.b2brouter.com/transactions](https://ws-staging.b2brouter.com/transactions)

---

### Aufbau einer PEPPOL-Nachricht

PEPPOL-Nachrichten bestehen aus mehreren Schichten, die durch verschiedene Standards definiert sind. Jede Schicht umschließt die Daten der nächsten Schicht und erweitert sie um spezifische Aspekte, die erforderlich sind. Die Schichten von außen nach innen:

#### **1. Standard Business Document Header (SBDH):**
- Wird verwendet, um Nachrichten im PEPPOL-Netzwerk zu routen;
- Beinhaltet die PEPPOL-Absender- und Empfängeradressen;
- Zugangspunkte benötigen nur die Daten dieser Schicht für das Routing;
- SBDH ist ein XML-Format. Die nächste Schicht ist in einem XML-Tag Base64-kodiert enthalten.

#### **2. Associated Signature Containers (ASiC):**
- Ein ZIP-Archiv beliebiger Daten, die kryptographisch signiert sind;
- Enthält die Datei `META-INF/ASiCManifest.xml`, die alle enthaltenen Dateien mit Prüfsummen auflistet;
- Genau eine Datei ist in `META-INF/ASiCManifest.xml` mit `RootFile=true` markiert. Diese Datei ist das Geschäfts- oder Prozessdokument, das verarbeitet werden soll;
- Das Geschäfts- oder Prozessdokument kann andere Dateien im ASiC-Container referenzieren.

#### **3. Geschäftsdokument (Business document):**
- Enthält die technische Transaktion, die der Absender ausführen soll;
- Der Vermittlungsdienst kann *Publish Notice Requests* (Transaction ID: `urn:fdc:peppol.eu:prac:trns:t015:1.2`) empfangen, um Bekanntmachungen zu veröffentlichen;
- Als Antwort sendet der Vermittlungsdienst eine *Notice Publication Response* (Transaction ID: `urn:fdc:peppol.eu:prac:trns:t016:1.1`);
- Im Falle einer *Publish Notice Request* enthält das Geschäftsdokument relative Pfade zu BKMS-Dateien, die veröffentlicht werden sollen. Diese Pfade beziehen sich auf andere Dateien im ASiC-Container.

---

#### **Bekanntmachungsdokumente (bei Publish Notice Request):**
- Bekanntmachung im XML-eForms-Format;
- Es wird das *Peppol BIS Profile P008 Publish Notice* der Pre-Award-Version 1.2 verwendet. Frühere Versionen unterstützen den eForms DE-Standard noch nicht;
- Das Profil umfasst die Transaktionen:
  - **T015 Publish Notice**: Für die Übermittlung von Bekanntmachungen;
  - **T016 Notice Publication Response**: Für Statusinformationen, die der Vermittlungsdienst an den Absender zurücksendet.

---

### Der PEPPOL-Zugangspunkt
Der PEPPOL-Zugangspunkt für den Vermittlungsdienst und der Bekanntmachungsservice werden vom Beschaffungsamt des BMI (BeschA) betrieben.

---

### Webressourcen
- **Peppol-Startseite:**: [peppol.org](https://peppol.org)  
- **SBDH/UBL-Identifikatoren/Prozesse/Profile für Peppol:** [https://docs.peppol.eu/pracc/files/BIS-eDelivery-guide-for-pre-award-v1.2.pdf](https://docs.peppol.eu/pracc/files/BIS-eDelivery-guide-for-pre-award-v1.2.pdf)
- **PEPPOL Pre-Award-Standarddokumentation:** [https://docs.peppol.eu/pracc/](https://docs.peppol.eu/pracc/)
- **Peppol BIS Profile P008:** [https://docs.peppol.eu/pracc/profiles/p008/index.html](https://docs.peppol.eu/pracc/profiles/p008/index.html)
- **PEPPOL T015 - Publish Notice 1.2:** [https://docs.peppol.eu/pracc/transactions/T015/index.html](https://docs.peppol.eu/pracc/transactions/T015/index.html)
- **PEPPOL T016 - Notice Publication Response 1.2:** [https://docs.peppol.eu/pracc/transactions/T016/index.html](https://docs.peppol.eu/pracc/transactions/T016/index.html)

<br>



## Wie setzt man ein Benutzerpasswort in Keycloak zurück?

>**Hinweis** <br>
> Das Passwort des Benutzers ist gleichzeitig das Passwort, welches für die Einlieferung bei der Vermittlungsdienstschnittstelle genutzt wird! <br>
> Sollte das Passwort geändert werden, ist sicherzustellen, dass es auch in der Software zur Einlieferung in den Vermittlungsdienst geändert wird! 

1. Self-Service-Portal der gewünschten Umgebung aufrufen (zu finden unter [Systemumgebungen](/documentation/Development_environments.md) in der Zeile _Self Service Portal_ ).

2. Auf ‚Passwort vergessen?' klicken.<br>
![Auf Passwort vergessen](/documentation/images/kc_login.png)
<br>

3. E-Mail-Adresse eintragen und auf ‚Absenden' klicken.<br>
![E-Mail eintragen](/documentation/images/kc_passwort_vergessen.png)
<br>

4. Die Meldung ‚Sie sollten in Kürze eine E-Mail mit weiteren Instruktionen erhalten' wird angezeigt.<br>
![Meldung](/documentation/images/kc_nachricht_best%C3%A4tigungsemail.png)
<br>

5. Überprüfen der E-Mails: Ein Link zum Zurücksetzen der Anmeldeinformationen ist in der E-Mail erhalten.<br>
![Bestätigungs-E-Mail](/documentation/images/e-mail_passwort_zuruecksetzen.png)
<br>

6. Auf ‚Link zum Zurücksetzen von Anmeldeinformationen' klicken.
<br>

7. Der Benutzer wird auf die Seite ‚Passwort aktualisieren' umgeleitet.<br>
![PAsswort aktualisieren](/documentation/images/kc_passwort_aktualisieren.png)
<br>

8. Neues Passwort eintragen und bestätigen und auf ‚Absenden' klicken.<br>
Das Passwort muss aus mindestens 8 Zeichen bestehen, 1 Großbuchstaben und 1 Zahl enthalten.
<br>

9. Das Passwort muss in der Software des Fachverfahrensherstellers hinterlegt werden, um sicher zu gehen, dass die Verbindung mit dem Vermittlungsdienst funktioniert.
<br>

## Zugang löschen
Um einen Zugang zu löschen, ist eine E-Mail an den Support des Datenservices Öffentlicher Einkauf [support@datenservice-oeffentlicher-einkauf.de](mailto:support@datenservice-oeffentlicher-einkauf.de) zu senden.<br>
In der E-Mail müssen folgende Angaben enthalten sein:

- Systemumgebung, in der die Zugangsdaten gelöscht werden sollen
- E-Mail-Adresse, welche als Benutzername verwendet wird
- URL der Vergabeplattform
- Vor- und Nachname sowie die E-Mail-Adresse des Vertreters des Fachverfahrensherstellers
- Name des Fachverfahrensherstellers

Nach Prüfung der angegebenen Daten in der E-Mail werden die Löschung des Zugangs durchführt und eine Bestätigung per E-Mail versendet.





