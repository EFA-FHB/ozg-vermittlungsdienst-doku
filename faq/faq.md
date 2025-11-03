### Datenservice Öffentlicher Einkauf
# Häufig gestellte Fragen

- [Datenservice Öffentlicher Einkauf](#datenservice-öffentlicher-einkauf)
- [Standard eForms-DE und SDK-DE](#standard-eForms-DE-und-SDK-DE)
- [Allgemein](#allgemein)

## Datenservice Öffentlicher Einkauf

### Anbindung

<details>
<summary>
Aus welchen Komponenten besteht der Datenservice Öffentlicher Einkauf und wo brauche ich einen Account?
</summary>
<br>
**[Redaktionssystem](https://resy.datenservice-oeffentlicher-einkauf.de/)**: Das Redaktionssystem ist ein Angebot für Vergabestellen und beispielsweise Dienstleister von öffentlichen Auftraggebern oder Zuwendungsempfängern, die kein elektronisches Vergabesystem nutzen. 
Mit dem Redaktionssystem können Bekanntmachungen zu europaweiten Vergabeverfahren erfasst, bearbeitet, korrigiert und über den Vermittlungsdienst an TED versendet werden.
<br>
**[Vermittlungsdienst](https://ozg-vermittlungsdienst.de/)**: Der Vermittlungsdienst ist eine rein technische Schnittstelle zur Annahme, Validierung und Weiterleitung von Bekanntmachungen an TED und den Bekanntmachungsservice. 
Er bietet KEINE Oberfläche zum Erstellen von Bekanntmachungen! Es ist ausschließlich eine Maschine-zu-Maschine Kommunikation möglich, wie z.B. mit einer Vergabestellensoftware. Diese Anbindung wird durch den Fachverfahrenshersteller durchgeführt. 
<br>
**[Self-Service Portal](https://portal.ozg-vermittlungsdienst.de/)**: Das Self-Service-Portal (SSP) ist eine Web-Oberfläche für das Accountmanagement von Accounts des Vermittlungsdienstes. Primär genutzt wird es durch Fachverfahrenshersteller zur Ansicht der Statusinformationen von eingelieferten Bekanntmachungen in einem Dashboard.
<br>
**[Bekanntmachungsservice](https://oeffentlichevergabe.de/)**: Im Bekanntmachungsservice werden alle über den eSender-Hub versendeten EU-weiten und nationalen Bekanntmachungen veröffentlicht. Der Bekanntmachungsservice bietet eine Vielzahl an Recherchemöglichkeiten, damit Bietende ihrem Leistungsspektrum entsprechend zielgenau Bekanntmachungen finden können. Mit Nutzung des ELSTER-Unternehmenskontos stehen zudem weitere Komfortfunktionen wie Speicherung von Suchfunktionen und Benachrichtigungsservices zur Verfügung. Des Weiteren können die Daten des Bekanntmachungsservice über eine Open Data Schnittstelle in den Formaten eForms-DE, CSV und OCDS nachgenutzt werden. 
<br>
</details>
<br>

<details>
<summary>
Pro Registrierung muss eine E-Mail Adresse als Benutzername angegeben werden. Ist es möglich dieselbe E-Mail-Adresse für mehrere Systeme anzugeben?
</summary>
<br>
Generell werden zwei E-Mail-Adressen pro Account erfragt (teils auch als Mandant bezeichnet): Eine E-Mail-Adresse zur Aktivierung des Accounts und eine Kontakt E-Mail-Adresse. Es wird eine individuelle E-Mail-Adresse pro Account zur Aktivierung benötigt, um das Passwort für den Account zu setzen und um eine eindeutige Authentifizierung mit der Kombination aus E-Mail und Passwort zu ermöglichen. Die Account E-Mail-Adresse kann auch ein Funktionspostfach sein und wird nur zur Verwaltung des Accounts benötigt. Die Kontakt E-Mail-Adresse wird genutzt, falls beim Betrieb Fragen aufkommen zu einer Bekanntmachung, die von diesem Account versendet wurde. Kontakt E-Mail-Adresse und Account E-Mail-Adresse dürfen identisch sein und dieselbe Kontakt E-Mail-Adresse (z.B. ein zentraler Ansprechpartner) darf bei mehreren Accounts verwendet werden. Es kann allerdings für die drei Systemumgebungen Preview, Staging und Produktion dieselbe Account E-Mail-Adresse verwendet werden. Generell empfehlen wir einen Account pro Vergabeplattform. 
</details>
<br>

<details>
<summary>
Bei der Accounterstellung muss eine Kontakt-E-Mail-Adresse eines Fachverfahrensherstellers angegeben werden. Wozu wird diese verwendet?
</summary>
<br>
Diese E-Mail-Adresse wird verwendet, um proaktiv auf Nutzer des Self-Service-Portals zugehen zu können. Dieses kann der Fall sein, wenn es beispielsweise Auffälligkeiten mit dem Account oder den eingelieferten Bekanntmachungen gibt oder wenn generelle Informationen an alle Accountverantwortlichen versenden werden sollen. 
</details>
<br>

<details>
<summary>
Können für die einzelnen Systeme mehrere Accounts gleichzeitig beantragt werden? Wie viele Accounts für die Preview- und Staging-Umgebung jeweils empfehlenswert?
</summary>
<br>
Wir empfehlen, auf Staging exakt so viele Accounts zu verwenden, wie sie für Produktion planen, zu nutzen. Zusätzlich sind natürlich beliebig viele Testaccounts auf Preview und Staging möglich. 
</details>
<br>

<details>
<summary>
Worin besteht der Unterschied zwischen der bei der Accounterstellung angefragten URL der Vergabeplattform und der Verlinkung zu den Vergabeunterlagen im eForms-Dokument?
</summary>
<br>
Die URL der Vergabeplattform dient rein der Zuordnung der Accounts/ Mandanten, diese hat nichts mit der Verlinkung auf die Vergabeunterlagen zu tun. 
Manche Vergabeplattformen nutzen z.B. Dropbox oder Google Drive oder Ähnliches für das Hosten der Vergabeunterlagen, weshalb sich daraus nicht eindeutig die dahinterliegende Plattform identifizieren lässt. Aus diesem Grund ist die URL zusätzlich notwendig. Die Verlinkung zu den Vergabeunterlagen bleibt weiterhin im XML-Dokument. Der bei der Accounterstellung mitgegebene Link wird bei der Veröffentlichung im Bekanntmachungsservice, unter der Bekanntmachung selbst, als Disclaimer/Quelle angezeigt.
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
Die Angabe der URL dient dazu, die genannten Systeme voneinander unterscheiden zu können, den korrekten Zugang zu ermöglichen und Duplikate zu vermeiden. Vergabeplattformen sind die Systeme, in denen Bekanntmachungen veröffentlicht werden, die URL der Vergabeplattform kann so z.B. alpha.oeffentlichevergabe.de (Test-Umgebung des Bekanntmachungsservices) sein. Mit dieser URL wird identifiziert, auf welcher Plattform Bekanntmachungen derzeit veröffentlicht werden. Bei diesem Thema ist es klar, dass es hier unterschiedliche Vorgehensweisen je nach Struktur des Systems der jeweiligen FVH geben kann. Prinzipiell gilt, dass sie einen Account pro System benötigen, das zukünftig in den Vermittlungsdient einliefern soll. Bei Unsicherheiten, welche Systeme/ Plattformen an den Vermittlungsdienst anzuschließen sind, kann eine Klärung mit Nutzung des Kontaktformulars herbeigeführt werden https://portal.ozg-vermittlungsdienst.de/contact. 
</details>
<br>

<details>
<summary>
Welche Systemumgebung ist die Umgebung, an die die Testsysteme der Fachverfahrenshersteller Bekanntmachungen versenden können? Worin besteht der Unterschied zwischen der Preview- und Staging-Umgebung?
</summary>
<br>
Die Preview-Umgebung dient nur zum Testen. Hier werden häufig Updates eingespielt und dieses ist auch die Testumgebung für zukünftige Releases. Die Staging-Umgebung ist eine 100% Kopie der Produktionsumgebung und sollte nur für produktionsnahe Tests genutzt werden. Beide Umgebungen liefern in die Staging-Umgebung des Bekanntmachungsservices und TED Preview ein. Auf Staging sollten Tests genauso durchgeführt werden, wie sie es auch für Produktion vorgesehen ist. Prinzipiell sind aber beide Umgebungen zum Test geeignet.
</details>
<br>

### Roadmap

<details>
<summary>
Gibt es eine Roadmap zur Weiterentwicklung der Komponenten des Datenservice Öffentlicher Einkauf?
</summary>
<br>
Ja. Die Informationen stehen hier: https://portal.ozg-vermittlungsdienst.de/roadmap
</details>
<br>

### Kommunikationskanäle

<details>
<summary> 
Wie kann das Team des Datenservice Öffentlicher Einkauf erreicht werden?
</summary>
Das Team ist über das folgende Kontaktformular zu erreichen:
<br>
Fragen/Anmerkungen zum Vermittlungsdienst/Self-Service Portal auf https://portal.ozg-vermittlungsdienst.de/contact
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
</details>

<br>
<details>
<summary>
Wie kann sichergestellt werden, dass Fachverfahrenshersteller regelmäßig über Neuigkeiten bzgl. des eForms-DE Standard/SDK-eForms-DE informiert bleiben.
</summary>
<br>
Die offizielle Publikation zum Standard eForms-DE erfolgt auf https://xeinkauf.de/eforms-de/
<br>
Die Publikation des zugehörigen SDK-DE erfolgt auf https://gitlab.opencode.de/OC000008125155/SDK-eforms-de
<br>
Fragen zum SDK-DE sind über Issues im Repository zu eröffnen.

</details>
<br>

### Dokumentation

<details>
<summary>
Wo ist die aktuelle Dokumentation zum Datenservice Öffentlicher Einkauf zu finden? Inwieweit ist geplant, diese auf dem neusten Stand zu halten? Handelt es sich bei dieser GitHub-Dokumentation um die offizielle Bereitstellung von Informationen zu diesem Thema? 
</summary>
<br>

Die Github-Dokumentation (https://github.com/EFA-FHB/ozg-vermittlungsdienst-doku) wird weitergepflegt und ist die offizielle Dokumentation. Diese kann auch im Self-Service Portal des Datenservice Öffentlicher Einkauf gelesen werden.
</details>
<br>

<details>
<summary>
Wie kann für ein Release ermittelt werden, welche eForms-Versionen die Teilkomponenten unterstützen?   
</summary>
<br>
Unter https://portal.ozg-vermittlungsdienst.de/documentation/eForms_support ist dokumentiert, welche eForms-Versionen die Teilkomponenten unterstützen. Für jedes Release werden Release Notes veröffentlicht, um zu beschreiben, welche Komponente welche Version unterstützt.
</details>
<br>

<details>
<summary>
Ist die Dokumentation zum Vermittlungsdienst (https://github.com/EFA-FHB/ozg-vermittlungsdienst-doku) die offizielle Dokumentation?
</summary>
<br>

Ja, die Github-Dokumentation wird regelmäßig aktualisiert und ist bis auf weiteres die offizielle Dokumentation. Die Dokumentation wird zugleich im [Self-Service Portal](https://portal.ozg-vermittlungsdienst.de/) veröffentlicht.
</details>
<br>

### API-Vermittlungsservice

<details>
<summary>
Wie können Fachverfahrenshersteller die Informationen des CVS-Reports der EU zu einer Bekanntmachung erhalten?
</summary>
<br>
Alle Fehler und Warnungen aus dem CVS Report werden in den Statusinformationen übergeben. Dabei werden die ID, der Pfad, der Inhalt und der Text jeder angeschlagenen Regel übergeben. Es ist nicht vorgesehen, den CVS Report als Datei zurückzugeben.
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
Die Authentifikation via API-Keys ist nicht mehr möglich, auch auf Preview. Langfristig können Sie sich nur über die Tokens mit Refresh alle 24h authentifizieren.
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
Alle Fehler und Warnungen aus dem CVS Report werden in den Statusinformationen übergeben. Dabei übergeben wir die ID, den Pfad, den Inhalt und den Text jeder angeschlagenen Regel. Derzeit ist es nicht vorgesehen, den CVS Report als Datei zurückzugeben. 
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

### Akzeptierte SDK-Versionen

<details>
<summary>
 Welche Versionen des Standards eForms-DE werden aktuell unterstützt?
</summary>
<br>
Ausführliche Informationen zur Unterstützung der eForms-Versionen stehen hier: https://portal.ozg-vermittlungsdienst.de/documentation/eForms_support
</details>
<br>

## Standard eForms-DE und SDK-DE

[Zum Anfang](#häufig-gestellte-fragen)<br>

**Bitte beachten Sie, dass wir alle Fragen bezüglich des Standards eForms-DE gemäß unserem aktuellen Wissensstand beantworten. Änderungen der Informationen sind jederzeit möglich.**

**Bei weiteren Fragen zum <u>Standard eForms-DE</u> wenden Sie sich gerne per E-Mail an die Koordinierungsstelle für IT-Standards (KoSIT) als Betreiberin: eforms@finanzen.bremen.de. Zusätzliche Informationen sind in der von der KoSIT bereitgestellten [FAQ](https://xeinkauf.de/eforms-de/faq/) zu finden.** 

### Allgemeine Fragen

<details>
  <summary>
    Gibt es Vorgaben zur Sprache der Bekanntmachung oder Mehrsprachigkeit?
  </summary>
  <br>
  Es gibt zwar keine Aussage zur Wahl der Sprache von Ausschreibungen in der Vergabeordnung, jedoch ist nach § 23 Abs. 1 Verwaltungsverfahrensgesetz (VwVfG) die Amtssprache deutsch. Dementsprechend ist zu erwarten, dass deutsche Behörden ihre Unterlagen immer mindestens in deutscher Sprache ausfertigen müssen. Mehrsprachigkeit ist natürlich möglich und erlaubt. Für Veröffentlichende Entitäten, die nicht als Behörde klassifiziert werden, ist die Veröffentlichung auch ohne deutsche Sprache in Ordnung. 
</details>

<details>
  <summary>
    Gibt es Formulare , die in eForms-DE nicht berücksichtigt werden?
  </summary>
  <br>
    Folgende Formulare sind im eForms-DE Standard nicht vorgesehen:
  
| Formular    | Typ                           | Beschreibung  | Grund für die Nichtumsetzung in eForms-DE |
|-------------|----------------------------------|------------|---------------------|
| 1 | Plannung | Bekanntmachung der Veröffentlichung einer Vorinformation in einem Beschafferprofil – allgemeine Richtlinie  | Informationen sind im Beschafferprofil enthalten |
| 2 | Plannung | Bekanntmachung der Veröffentlichung einer regelmäßigen nicht verbindlichen Bekanntmachung in einem Beschafferprofil – __Sektorenrichtlinie__ | Informationen sind im Beschafferprofil enthalten |
| 3 | Plannung | Bekanntmachung der Veröffentlichung einer Vorinformation in einem Beschafferprofil – Richtlinie für Beschaffung im Bereich Verteidigung | Informationen sind im Beschafferprofil enthalten |
| T01 | Plannung | Vorinformation zu öffentlichen Personenverkehrsdiensten | Grundlage ist die Verordnung (EG) Nr. 1370/2007 diese gilt weiterhin mit Aktualisierungen. Aktuell erfolgt die Datenerfassung für T1 in der Anwendung „eNotices“ direkt bei TED. Die eForms-Verordnung ((EU) 2019/1780) die zentrale Grundlage für die seit 25.10.2023 gültige VgV. Die Verordnung (EG) Nr. 1370/2007 ist nicht Bestandteil der eForms-Verordnung. |
| T02 | Result | Bekanntmachung über vergebene Aufträge für öffentliche Personenverkehrsdienste | Grundlage ist die Verordnung (EG) Nr. 1370/2007 diese gilt weiterhin mit Aktualisierungen. Aktuell erfolgt die Datenerfassung für T2 in der Anwendung „eNotices“ direkt bei TED. Die eForms-Verordnung ((EU) 2019/1780) die zentrale Grundlage für die seit 25.10.2023 gültige VgV. Die Verordnung (EG) Nr. 1370/2007 ist nicht Bestandteil der eForms-Verordnung. |
</details>
<br>

### Fragen zum SDK-DE

<details>
<summary>
Wo ist die neueste Version des vom Datenservice Öffentlicher Einkauf (DÖE) unterstützten und zum deutschen Standard eForms-DE konformen SDK-DE zu finden?</summary>
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
-	Der eSender erhält eine Kopie an die E-Mail-Adresse, die von EU-Login für den API-Schlüssel verwendet wird.
</details>
<br>

<details>
<summary>
Ist es möglich weiterhin Bekanntmachungen über eNotices2 einzuliefern?
</summary>
<br>
Seit dem 25.10.2023 müssen rechtlich alle oberschwelligen Bekanntmachungen im eForms-DE Format über den Datenservice Öffentlicher Einkauf eingeliefert werden. Eine direkte Einlieferung über eNotices2 ist rechtlich nicht zulässig, da dort die Anpassungen des eForms-DE Standards nicht berücksichtig werden. (Siehe auch VgV § 10a) 
</details>
<br>

<details>
<summary>
Existiert ein Mapping von XVergabe auf eForms?
</summary>
<br>
Nein, im Datenservice Öffentlicher Einkauf wird kein Mapping von XVergabe auf eForms zur Verfügung gestellt.
Der Standard XVergabe wird dauerhaft durch eForms-DE ersetzt und nicht weiterentwickelt. 
</details>
<br>

---
[Zum Anfang](#häufig-gestellte-fragen)





