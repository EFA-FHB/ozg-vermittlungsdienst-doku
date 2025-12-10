
# Häufig gestellte Fragen

- [Datenservice Öffentlicher Einkauf](#datenservice-öffentlicher-einkauf)
- [Standard eForms-DE und SDK-DE](#standard-eForms-DE-und-SDK-DE)
- [Allgemein](#allgemein)

### Anbindung

<details>
<summary>
Aus welchen Komponenten besteht der Datenservice Öffentlicher Einkauf und wo brauche ich einen Account?
</summary>
<br>

**[Redaktionssystem](https://resy.datenservice-oeffentlicher-einkauf.de/)**: Das Redaktionssystem ist ein Angebot für Vergabestellen und beispielsweise Dienstleister von öffentlichen Auftraggebern oder Zuwendungsempfängern, die kein elektronisches Vergabesystem nutzen. Mit dem Redaktionssystem können Bekanntmachungen zu Vergabeverfahren erfasst, bearbeitet, korrigiert und auf dem Bekanntmachungsservice publiziert werden, die bei europaweiten Vergabeverfahren auch über den Vermittlungsdienst des Datenservice Öffentlicher Einkauf vergaberechtskonform an die Plattform TED des Amtes für Veröffentlichungen der EU versendet werden. Zudem ist das Zurückziehen von Verfahren möglich.
<br>

**[Vermittlungsdienst](https://ozg-vermittlungsdienst.de/)**: Der Vermittlungsdienst nimmt als technische Komponente Bekanntmachungen von Vergabeplattformen im Format eForms-DE entgegen. Bekanntmachungen zu Vergabeverfahren oberhalb der EU-Schwellenwerte werden validiert und an den eSender-Hub des Datenservice Öffentlicher Einkauf weitergeleitet. Bekanntmachungen zu Vergabeverfahren unterhalb der EU-Schwellenwerte werden nach Validierung direkt an den Bekanntmachungsservice weitergeleitet.
<br>

**[Self-Service Portal](https://github.com/EFA-FHB/ozg-vermittlungsdienst-doku/blob/main/documentation/SSP.md)**: Das Self-Service-Portal bietet Betreibern von Vergabeplattformen die Möglichkeit, administrative Prozesse zur Entlastung des eigenen Betriebs selbst zu verwalten und sich jederzeit über den Bearbeitungsstatus von Bekanntmachungen im Bekanntmachungsprozess zu informieren.
<br>

**[Bekanntmachungsservice](https://oeffentlichevergabe.de/)**: Der Bekanntmachungsservice ist der zentrale Ort, an dem EU-weite und nationale Bekanntmachungen von Bund, Ländern und Kommunen gefunden werden können. Er bietet eine Vielzahl an Recherchemöglichkeiten, damit Bietende ihrem Leistungsspektrum entsprechend zielgenau Bekanntmachungen zu Vergabeverfahren öffentlicher Auftraggeber finden können. Mit der Nutzung von „Mein Unternehmenskonto“ (Das Unternehmenskonto auf der Basis von ELSTER) stehen zudem weitere komfortable Funktionen wie Speicherung von Suchfunktionen und Benachrichtigungsservices zur Verfügung. Des Weiteren können die Daten des Bekanntmachungsservice über eine Open-Data-Schnittstelle in den Formaten eForms-DE, CSV und OCDS genutzt werden. Außerdem können andere Server über die Peppol-Infrastruktur unter Nutzung des Peppol-Profils „Search Notice“ aktuelle Bekanntmachungsdaten vom Bekanntmachungsservice abrufen.
<br>

**eSender-HuB**: Der eSender-Hub ist eine interne technische Komponente, der als zentrale Stelle für die Kommunikation mit dem europaweiten Tenders Electronic Daily (TED) des Amtes für Veröffentlichungen der EU dient. Der eSender-Hub konvertiert die vom Vermittlungsdienst übermittelten Bekanntmachungen vom Format eForms-DE in das notwendige eForms-EU-Format und sendet diese an TED. Außerdem leitet der eSender-Hub die Bekanntmachungen zu Vergabeverfahren oberhalb der EU-Schwellenwerte weiter an den Bekanntmachungsservice.
</details>
<br>

<details>
<summary>
Pro Registrierung muss eine E-Mail Adresse als Benutzername angegeben werden. Ist es möglich dieselbe E-Mail-Adresse für mehrere Systeme anzugeben?
</summary>
<br>
Generell werden zwei E-Mail-Adressen pro Account erfragt (in der RST-API als Mandant bezeichnet): Eine E-Mail-Adresse zur Aktivierung des Accounts und eine Kontakt E-Mail-Adresse. Es wird eine individuelle E-Mail-Adresse pro Account zur Aktivierung benötigt, um das Passwort für den Account zu setzen und um eine eindeutige Authentifizierung mit der Kombination aus E-Mail und Passwort zu ermöglichen. Die Account E-Mail-Adresse kann auch ein Funktionspostfach sein und wird nur zur Verwaltung des Accounts benötigt. Die Kontakt E-Mail-Adresse wird genutzt, falls beim Betrieb Fragen aufkommen zu einer Bekanntmachung, die von diesem Account versendet wurde. Kontakt E-Mail-Adresse und Account E-Mail-Adresse dürfen identisch sein und dieselbe Kontakt E-Mail-Adresse (z.B. ein zentraler Ansprechpartner) darf bei mehreren Accounts verwendet werden. Für die drei Systemumgebungen Preview, Staging und Produktion kann dieselbe Account E-Mail-Adresse verwendet werden. Generell empfehlen wir einen Account pro Vergabeplattform.
</details>
<br>

<details>
<summary>
Bei der Accounterstellung muss eine Kontakt-E-Mail-Adresse eines Fachverfahrensherstellers angegeben werden. Wozu wird diese verwendet?
</summary>
<br>
Diese E-Mail-Adresse wird verwendet, um proaktiv auf Nutzer des Self-Service-Portals zugehen zu können. Dieses kann der Fall sein, wenn es beispielsweise Auffälligkeiten mit dem Account oder den eingelieferten Bekanntmachungen gibt oder wenn Informationen an alle Accountverantwortlichen versenden werden sollen. 
</details>
<br>

<details>
<summary>
Können für die einzelnen Systeme mehrere Accounts gleichzeitig beantragt werden? Wie viele Accounts sind für die Preview- und Staging-Umgebung jeweils empfehlenswert?
</summary>
<br>
Wir empfehlen, auf Staging exakt so viele Accounts zu verwenden, wie für die Produktion geplant sind. Zusätzlich sind beliebig viele Testaccounts auf Preview und Staging möglich.</details>
<br>

<details>
<summary>
Worin besteht der Unterschied zwischen der bei der Accounterstellung angefragten URL der Vergabeplattform und der Verlinkung zu den Vergabeunterlagen im eForms-Dokument?
</summary>
<br>
Die URL der Vergabeplattform dient rein der Zuordnung der Accounts / Mandanten, sie hat nichts mit der Verlinkung auf die Vergabeunterlagen zu tun. Manche Vergabeplattformen nutzen z.B. Dropbox oder Google Drive oder Ähnliches für das Hosten der Vergabeunterlagen, weshalb sich daraus nicht eindeutig die dahinterliegende Plattform identifizieren lässt. Aus diesem Grund ist die URL zusätzlich notwendig. Die Verlinkung zu den Vergabeunterlagen bleibt weiterhin im XML-Dokument. Der bei der Accounterstellung mitgegebene Link wird bei der Veröffentlichung im Bekanntmachungsservice, unter der Bekanntmachung selbst, als Quelle angezeigt.
</details>
<br>

<details>
<summary>
Werden auf Staging oder Preview der Veröffentlichungszyklus und die Validierung auf dieselbe Art wie in Produktion durchgeführt oder werden die Statuswechsel beschleunigt? Mit welchen Verzögerungen zwischen Annahme und Veröffentlichung ist zu rechnen? 
</summary>
<br>
In allen Umgebungen werden eine vollständige Validierung und alle Statuswechsel durchgeführt. Da neue eForms-Versionen zunächst auf Preview, dann auf Staging und zuletzt in Produktion ausgerollt werden, können kurzzeitig unterschiedliche Validierungsregeln angewendet werden.
Da die Bekanntmachungen bei TED auf Preview und Staging etwas schneller prozessiert werden, erfolgt auch die Veröffentlichung auf der Staging-Umgebung des Bekanntmachungsservice etwas schneller als in Produktion.
</details>
<br>

<details>
<summary>
Zur Anforderung von Accounts soll die URL der Vergabeplattform angegeben werden. Wozu dient diese Angabe?
</summary>
<br>
Die Angabe der URL dient dazu, die genannten Systeme voneinander unterscheiden zu können, den korrekten Zugang zum Bekanntmachungsservice zu ermöglichen und um Duplikate zu vermeiden. Mit der URL wird identifiziert, auf welcher Plattform Bekanntmachungen derzeit veröffentlicht und abrufbar sind. Je nach Struktur des Systems der jeweiligen Fachverfahrenshersteller kann es unterschiedliche Vorgehensweisen geben. Prinzipiell gilt, dass pro System, das zukünftig in den Vermittlungsdient einliefern soll ein Account benötigt wird. Bei Unsicherheiten, welche Systeme/ Plattformen an den Vermittlungsdienst anzuschließen sind, kann eine Klärung mit Nutzung des Kontaktformulars herbeigeführt werden https://self-service.datenservice-oeffentlicher-einkauf.de/contact. 
</details>
<br>

<details>
<summary>
Welche Systemumgebung ist die Umgebung, an die die Testsysteme der Fachverfahrenshersteller Bekanntmachungen versenden können? Worin besteht der Unterschied zwischen der Preview- und Staging-Umgebung?
</summary>
<br>
Die Preview-Umgebung dient nur zum Testen. Hier werden häufig Updates eingespielt und sie ist auch die Testumgebung für zukünftige Releases. Die Staging-Umgebung ist eine 100% Kopie der Produktionsumgebung und sollte nur für produktionsnahe Tests genutzt werden. Beide Umgebungen liefern in die Staging-Umgebung des Bekanntmachungsservices und TED Preview ein. Auf Staging sollten Tests genauso durchgeführt werden, wie es auch für Produktion vorgesehen ist. Prinzipiell sind aber beide Umgebungen zum Test geeignet.</details>
<br>

### Roadmap

<details>
<summary>
Gibt es eine Roadmap zu den Komponenten des Datenservice Öffentlicher Einkauf? </summary>
<br>
Ja. Die Informationen stehen hier: https://self-service.datenservice-oeffentlicher-einkauf.de/roadmap
</details>
<br>

### Kommunikationskanäle

<details>
<summary> 
Wie kann das Team des Datenservice Öffentlicher Einkauf erreicht werden?
</summary>

Das Team ist je nach Komponente über folgende Kontaktformulare zu erreichen: 
<br>
Fragen/Anmerkungen zum Vermittlungsdienst/Self-Service Portal auf https://self-service.datenservice-oeffentlicher-einkauf.de/contact 
<br>
Fragen/Anmerkungen zum Redaktionssystem auf https://resy.datenservice-oeffentlicher-einkauf.de/kontakt
<br>
Fragen/Anmerkungen zum Bekanntmachungsservice auf https://oeffentlichevergabe.de/ui/de/contact 
</details>
<br>

<details>
<summary>
Wie wird sichergestellt, dass Fachverfahrenshersteller regelmäßig über Neuigkeiten zum Datenservice Öffentlicher Einkauf informiert bleiben, insbesondere bzgl. neuer Versionen der Komponenten (Vermittlungsdienst, eSender-Hub, REST-API, usw.), neuer Features, einer Aktualisierung der Roadmap etc.?
</summary>
<br>
Es finden regelmäßig Informationstermine für die Fachverfahrenshersteller statt, diese werden per E-Mail angekündigt.
<br>
Eine aktuelle Roadmap ist hier zu finden: https://self-service.datenservice-oeffentlicher-einkauf.de/roadmap 
</details>

<br>
<details>
<summary>
Wie kann sichergestellt werden, dass Fachverfahrenshersteller regelmäßig über Neuigkeiten bzgl. des eForms-DE Standard/SDK-eForms-DE informiert bleiben.
</summary>
<br>
Die offizielle Publikation der KoSIT https://xeinkauf.de/eforms-de/zum Standard eForms-DE erfolgt auf https://xeinkauf.de/eforms-de/ 
<br>
Auf dieser Seite kann auch Kontakt mit der KoSIT aufgenommen werden.
Die Publikation des SDK-DE erfolgt auf https://gitlab.opencode.de/OC000008125155/SDK-eforms-de
<br>
Fragen zum SDK-DE sind über Issues im dortigen Repository zu eröffnen.


</details>
<br>

### Dokumentation

<details>
<summary>
Wo ist die aktuelle Dokumentation zum Datenservice Öffentlicher Einkauf zu finden? Inwieweit ist geplant, diese auf dem neusten Stand zu halten? Handelt es sich bei dieser GitHub-Dokumentation um die offizielle Bereitstellung von Informationen zu diesem Thema? 
</summary>
<br>

Die Github-Dokumentation (https://github.com/EFA-FHB/ozg-vermittlungsdienst-doku) wird weitergepflegt und ist die offizielle Dokumentation.
</details>
<br>

<details>
<summary>
Wie kann für ein Release ermittelt werden, welche eForms-Versionen die Teilkomponenten unterstützen?   
</summary>
<br>
Unter https://self-service.datenservice-oeffentlicher-einkauf.de/documentation/eForms_support ist dokumentiert, welche eForms-Versionen die Teilkomponenten unterstützen. Für jedes Release werden Release Notes veröffentlicht, aus denen hervorgeht, welche Komponente welche Version unterstützt.
</details>
<br>

<details>
<summary>
Ist die Dokumentation zum Vermittlungsdienst (https://github.com/EFA-FHB/ozg-vermittlungsdienst-doku) die offizielle Dokumentation?
</summary>
<br>
Ja, die Github-Dokumentation wird regelmäßig aktualisiert und ist bis auf weiteres die offizielle Dokumentation.
</details>
<br>

### API-Vermittlungsservice

<details>
<summary>
Wie können Fachverfahrenshersteller die Informationen des CVS-Reports der EU zu einer Bekanntmachung erhalten?
</summary>
<br>
Alle Fehler und Warnungen aus dem CVS Report werden in den Statusinformationen zur Bekanntmachung übergeben. Dabei werden die ID, der Pfad, der Inhalt und der Text jeder angeschlagenen Regel übergeben. Es ist nicht vorgesehen, den CVS Report als Datei zurückzugeben.
</details>
<br>

<details>
<summary>
In der REST-API-Beschreibung wird von "aktuellen Datenlieferungen" gesprochen. Was ist damit genau gemeint?
</summary>
<br>
Der Endpunkt v1/notices gibt Statusinformationen zu allen Bekanntmachungen zurück, die vom authentifizierten Mandanten erfolgreich eingeliefert wurden.
</details>
<br>

<details>
<summary>
Kann auch ein API-Key zur Authentifizierung genutzt werden oder nur die Authentifizierung über Token? 
</summary>
<br>
Die Authentifikation via API-Keys ist nicht mehr möglich, auch nicht auf Preview. Eine Authentifizierung ist nur über die Tokens mit Refresh alle 24 Stunden möglich.
</details>
<br>

<details>
<summary>
In der REST-API wird von Mandanten gesprochen. Bedeutet 1 Mandant = 1 Vergabeplattform? 
</summary>
<br>
Ja, das ist korrekt.
</details>
<br>

<details>
<summary>
In der REST-API-Beschreibung wird von "aktuellen Datenlieferungen" gesprochen. Was ist damit genau gemeint?
</summary>
<br>
Der Endpunkt v1/notices gibt Statusinformationen zu allen Bekanntmachungen zurück, die vom derzeit authentifizierten Mandanten erfolgreich eingeliefert wurden.
</details>
<br>

<details>
<summary>
Wie können Fachverfahrenshersteller die Informationen des CVS-Reports der EU zu einer Bekanntmachung erhalten, wenn diese weder in der Antwort bei Veröffentlichung (POST → /v2/notices), noch in den Statusinformationen (GET → /v1/notices/{trackingCode}) enthalten sind?
</summary>
<br>
Alle Fehler und Warnungen aus dem CVS Report werden in den Statusinformationen übergeben. Dabei übergeben wir die ID, den Pfad, den Inhalt und den Text jeder angeschlagenen Regel. Es ist nicht vorgesehen, den CVS Report als Datei zurückzugeben. 
</details>
<br>

<details>
<summary>
Ist es möglich, die online Validator API produktiv zu nutzen?
</summary>
<br>
Ja, die produktive Nutzung des Online Validators wird unterstützt. In der Produktivumgebung und in der Stagingumgebung wird die eforms-de-schematron Bugfix-Version immer die gleiche sein, wie auch im Vermittlungsdienst selbst. Auch die Nutzung des Offline-Validators (https://projekte.kosit.org/eforms/validator-edition-eforms-de) wird empfohlen.
</details>
<br>

### Akzeptierte SDK-DE-Versionen

<details>
<summary>
 Welche Versionen des Standards eForms-DE werden aktuell unterstützt?
</summary>
<br>
Ausführliche Informationen zur Unterstützung der eForms-Versionen stehen hier: https://self-service.datenservice-oeffentlicher-einkauf.de/documentation/eForms_support
</details>
<br>

## Standard eForms-DE und SDK-DE

[Zum Anfang](#häufig-gestellte-fragen)<br>

**Bitte beachten Sie, dass wir alle Fragen bezüglich des Standards eForms-DE gemäß unserem aktuellen Wissensstand beantworten. Änderungen der Informationen sind jederzeit möglich.**

**Bei weiteren Fragen zum <u>Standard eForms-DE</u> wenden Sie sich gerne per E-Mail an die Koordinierungsstelle für IT-Standards (KoSIT) als Betreiberin: eforms@finanzen.bremen.de. Zusätzliche Informationen sind in der von der KoSIT bereitgestellten [FAQ](https://xeinkauf.de/eforms-de/faq/) zu finden.** 

### Allgemeine Fragen

<details>
  <summary>
    Gibt es Formulare , die in eForms-DE nicht berücksichtigt werden?
  </summary>
  <br>
    Folgende Formulare sind im eForms-DE Standard nicht vorgesehen:
  
| Formular    | Typ                       | Beschreibung  | Grund für die Nichtumsetzung in eForms-DE |
|-------------|------------------------------|------------|---------------------|
| 1 | Planung | Bekanntmachung der Veröffentlichung einer Vorinformation in einem Beschafferprofil – allgemeine Richtlinie  | Informationen sind im Beschafferprofil enthalten |
| 2 | Planung | Bekanntmachung der Veröffentlichung einer regelmäßigen nicht verbindlichen Bekanntmachung in einem Beschafferprofil – __Sektorenrichtlinie__ | Informationen sind im Beschafferprofil enthalten |
| 3 | Planung | Bekanntmachung der Veröffentlichung einer Vorinformation in einem Beschafferprofil – Richtlinie für Beschaffung im Bereich Verteidigung | Informationen sind im Beschafferprofil enthalten |
| T01 | Planung | Vorinformation zu öffentlichen Personenverkehrsdiensten | Grundlage ist die Verordnung (EG) Nr. 1370/2007 diese gilt weiterhin mit Aktualisierungen. Aktuell erfolgt die Datenerfassung für T1 in der Anwendung „eNotices“ direkt bei TED. Die eForms-Verordnung ((EU) 2019/1780) die zentrale Grundlage für die seit 25.10.2023 gültige VgV. Die Verordnung (EG) Nr. 1370/2007 ist nicht Bestandteil der eForms-Verordnung. |
| T02 | Result | Bekanntmachung über vergebene Aufträge für öffentliche Personenverkehrsdienste | Grundlage ist die Verordnung (EG) Nr. 1370/2007 diese gilt weiterhin mit Aktualisierungen. Aktuell erfolgt die Datenerfassung für T2 in der Anwendung „eNotices“ direkt bei TED. Die eForms-Verordnung ((EU) 2019/1780) die zentrale Grundlage für die seit 25.10.2023 gültige VgV. Die Verordnung (EG) Nr. 1370/2007 ist nicht Bestandteil der eForms-Verordnung. |
</details>
<br>

### Fragen zum SDK-DE

<details>
<summary>
Wo ist die neueste Version des vom Datenservice Öffentlicher Einkauf unterstützten und zum deutschen Standard eForms-DE konformen SDK-DE zu finden?</summary>
<br>
Die Publikation des SDK-DE erfolgt auf https://gitlab.opencode.de/OC000008125155/SDK-eforms-de
</details>
<br>

## Allgemein
[Zum Anfang](#häufig-gestellte-fragen)

### eNotices Portal der EU

 <details> 
<summary>
Wie erfolgt die Kommunikation mit TED?

 </summary>

<br>

- Bei API-Übermittlungen muss die NoticeAuthorEmail die E-Mail des Beschaffers (Endanwender) sein
-	Der E-Mail-Autor der Bekanntmachung erhält Benachrichtigungen über Statusänderungen:
--> Einreichung, gestoppt, nicht veröffentlicht, veröffentlicht
-	Der eSender erhält eine Kopie der Bekanntmachung an die E-Mail-Adresse, die im EU-Login für den verwendeten API-Schlüssel hinterlegt ist
</details>
<br>

<details>
<summary>
Ist es möglich weiterhin Bekanntmachungen über eNotices2 einzuliefern?
</summary>
<br>
Seit dem 25.10.2023 müssen alle Bekanntmachungen oberhalb der EU-Schwellenwerte im eForms-DE Format über den Datenservice Öffentlicher Einkauf eingeliefert werden. Eine Einlieferung über eNotices2 ist somit nicht zulässig (Siehe auch VgV § 10a)
</details>
<br>

<details>
<summary>
Existiert ein Mapping von XVergabe auf eForms?
</summary>
<br>
Nein, im Datenservice Öffentlicher Einkauf wird kein Mapping von XVergabe auf eForms zur Verfügung gestellt. Der Standard XVergabe wird aktuell nicht weiterentwickelt und perspektivisch durch eForms-DE ersetzt. 
</details>
<br>

---
[Zum Anfang](#häufig-gestellte-fragen)





