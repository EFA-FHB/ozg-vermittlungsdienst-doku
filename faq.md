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

**[Redaktionssystem](https://resy.datenservice-oeffentlicher-einkauf.de/)**: Web-Oberfläche zum Erstellen von Bekanntmachungen und der Veröffentlichung bei TED sowie im Bekanntmachungsservice. 
Haben Sie in Ihrer Vergabestelle keine Software eines Fachverfahrensherstellers zum Erstellen von Bekanntmachungen, unterstützt diese nicht alle von Ihnen benötigte Formulare oder haben Sie bisher die eNotices2 von TED genutzt? Dann ist das Redaktionssystem richtig!
<br>
**[Vermittlungsdienst](https://ozg-vermittlungsdienst.de/)**: Rein technische Schnittstelle zur Annahme, Validierung und Weiterleitung von Bekanntmachungen an TED und den Bekanntmachungsservice. 
Bietet KEINE Oberfläche zum Erstellen von Bekanntmachungen! Es ist ausschließlich Maschine-zu-Maschine Kommunikation möglich, wie z.B. von einer Vergabestellensoftware. Diese Anbindung wird meist durch den Fachverfahrenshersteller durchgeführt. 
<br>
**[Self-Service Portal](https://github.com/EFA-FHB/ozg-vermittlungsdienst-doku/blob/main/documentation/SSP.md)**: Web-Oberfläche für das Accountmanagement von Accounts des Vermittlungsdienstes. 
Hauptsächlich genutzt durch Fachverfahrenshersteller. Dashboard Accounts sind möglich zur Ansicht der Statusinformationen von eingelieferten Bekanntmachungen, dazu wenden Sie sich bitte an Ihren Fachverfahrenshersteller!
<br>
**[Bekanntmachungsservice](https://oeffentlichevergabe.de/)**: Im Bekanntmachungsservice werden sämtliche Bekanntmachung, welche über den Datenservice Öffentlicher Einkauf versendet werden, veröffentlicht. Der Bekanntmachungsservice bietet eine Vielzahl an Recherchemöglichkeiten, damit Bietende ihrem Leistungsspektrum entsprechend zielgenau Bekanntmachungen finden können. Mit Nutzung des ELSTER-Unternehmenskontos stehen zudem weitere komfortable Funktionen wie Speicherung von Suchfunktionen und Benachrichtigungsservices zur Verfügung. Des Weiteren können die Daten des Bekanntmachungsservice über eine Open Data Schnittstelle in den Formaten eForms-DE, CSV und OCDS nachgenutzt werden.
<br>
</details>
<br>

<details>
<summary>
Welche Informationen werden benötigt, um einen Account zu beantragen? (aktualisiert am 11.10.23)
</summary>
<br>

Seit dem 04.10.2023 sollen Accounts im [Self-Service Portal](https://portal.ozg-vermittlungsdienst.de) beantragt werden. Alle benötigte Informationen werden im Registrierungsformular für einen VD Account abgefragt. Diese sind:

<br>

- Systemumgebung, für die Zugangsdaten beantragt werden (Preview, Staging, Produktion). Die Registrierung im Portal erfolgt für die entsprechende Umgebung, d. h. wenn ein Konto für die Staging-Umgebung erforderlich ist, sollte dieses im Staging-Portal beantragt werden.

-  E-Mail-Adresse, welche als Benutzername verwendet werden soll (diese muss pro Umgebung eindeutig sein, keine Dopplungen erlaubt)
  
- URL der Vergabeplattform auf der die Bekanntmachungen veröffentlicht werden
  
- Vor- und Nachname sowie die E-Mail-Adresse des Vertreters des FVH (Fachverfahrenshersteller)
  
- Name des FVH
</details>
<br>

<details>
<summary>
Pro Registrierung muss eine E-Mail Adresse als Benutzername angegeben werden. Ist es möglich dieselbe E-Mail-Adresse für mehrere Systeme anzugeben?
</summary>
<br>
Generell erfragen wir zwei Emails pro Account (teils auch als Mandant bezeichnet): Eine Accountemail zur Aktivierung des Accounts und eine Kontaktemail. Es wird eine individuelle Email pro Account zur Aktivierung benötigt, um das Passwort für den Account zu setzen und eine eindeutige Authentifizierung mit der Kombination aus Email und Passwort zu ermöglichen. Die Account-Email kann aber auch ein Funktionspostfach sein und wird nur zur Verwaltung des Accounts benötigt. Die Kontakt-Emailadresse wird nur genutzt, falls beim Betrieb Fragen aufkommen zu einer Bekanntmachung, die von diesem Account versendet wurden. Kontakt-Email und Account Email dürfen bei Bedarf identisch sein und dieselbe Kontakt-Email (z.b. ein zentraler Ansprechpartner) darf bei mehreren Accounts verwendet werden. Es können allerdings zwischen den Systemumgebungen Ihre Account E-Mail je einmal wiederverwenden, zum Beispiel dieselbe Account Mail-Adresse für Preview, Staging und Production. Generell empfehlen wir einen Account pro Vergabeplattform.
</details>
<br>

<details>
<summary>
Bei der Accounterstellung muss eine Kontakt-E-Mmail-Adresse eines FVH angegeben werden. Wozu wird diese verwendet?
</summary>
<br>
Diese Email wird verwendet, wenn wir proaktiv auf Sie zugehen wollen. Dies kann der Fall sein, wenn es beispielsweise Auffälligkeiten mit ihrem Account oder den eingelieferten Bekanntmachungen gibt oder wir generelle Informationen an alle Accountverantwortlichen versenden. 
</details>

<br>

<details>
<summary>
Können mehrere Accounts gleichzeitig beantragt werden? Wie viele Accounts empfehlen sich jeweils für die Preview- und Staging-Umgebung?
</summary>
<br>
Die URL der Vergabeplattform dient rein der Zuordnung dr Accounts/ Mandanten, diese hat nichts mit der Verlinkung auf die Vergabeunterlagen zu tun. 

Manche Vergabeplattformen nutzen z.B. Dropbox oder google drive oder Ähnliches für das Hosten der Vergabeunterlagen, weshalb sich daraus nicht eindeutig die dahinterliegende Plattform identifizieren lässt. Aus diesem Grund ist diese Information zusätzlich notwendig. Die Verlinkung zu den Vergabeunterlagen bleibt weiterhin im XML Dokument und diese wird primär in der BKMS Oberfläche angezeigt. Der bei der Accounterstellung mitgegebene Link wird nur rechts unten, unter der Bekanntmachung selbst, als Disclaimer/ Quelle angezeigt. 
</details>
<br>

<details>
<summary>
Worin besteht der Unterschied zwischen der bei der Accounterstellung angefragten URL der Vergabeplattform und der Verlinkung zu den Vergabeunterlagen im eForms-Dokument?
</summary>
<br>
Senden Sie uns gern eine Liste von benötigten Accounts an support@datenservice-oeffentlicher-einkauf.de Inklusive aller benötigter Informationen pro Account. Wir empfehlen, auf Staging exakt so viele Accounts zu verwenden, wie sie für Produktion planen, zu nutzen. Zusätzlich sind natürlich beliebig viele Testaccounts auf Preview und Staging möglich.  
</details>

<br>

<details>
<summary>
Wird auf Staging oder Preview der Veröffentlichungszyklus und die Validierung auf die selbe Art wie in Produktion durchgeführt oder werden die Statuswechsel beschleunigt? Mit welchen Verzägerungen zwischen Annahme und Veröffentlichung ist zu rechnen? 
</summary>
<br>
In allen Umgebungen wird die gleiche Validierung und die gleiche Verzögerung in der Veröffentlichung durchgeführt wie in der Produktionsumgebung. Die Zeitverzögerungen liegen in diesem Fall bei TED (Veröffentlichung werktags frühestens am nächsten Werktag bei Annahme bis 16 Uhr) bzw der rechtlich notwendigen Logik der nationalen Veröffentlichung (Weiterleitung an den BKMS) nach frühestens 48h. Der BKMS veröffentlicht sofort, wenn eine Bekanntmachung entgegengenommen wurde, es sei den das Bevorzugte Veröffentlichungsdatum liegt in der Zukunft. In diesem Fall würde die Veröffentlichung sowohl in TED als auch in BKMS erst am gewünschten Tag stattfinden unter den bei TED geltenden Einschränkungen (z.B. keine Veröffentlichung am Wochenende).
</details>
<br>

<details>
<summary>
Zur Anforderung von Zugängen soll die URL der Vergabeplattform angegeben werden. Wozu dient diese Angabe?
</summary>
<br>
Die Angabe der URL dient dazu, die genannten Systeme voneinander unterscheiden zu können, Ihnen den korrekten Zugang zu ermöglichen und Duplikate zu vermeiden. Vergabeplattformen sind die Systeme, in denen Bekanntmachungen veröffentlicht werden, die URL der Vergabeplattform kann so z.B. alpha.oeffentlichevergabe.de (Test-Umgebung BKMS) sein. Diese URL dient dazu, zu identifizieren, auf welcher Plattform Sie Ihre Bekanntmachungen derzeit veröffentlichen. Zu diesem Thema ist uns bewusst, dass es hier unterschiedliche Vorgehensweisen je nach Struktur des Systems der jeweiligen FVH geben kann. Prinzipiell gilt, dass sie einen Account pro System benötigen, dass zukünftig in den Vermittlungsdient einliefern soll. Wenn Sie unsicher sind, welche Systeme/ Plattformen für Sie an den DÖE anzuschließen sind, unterstützen wir Sie gern bei dieser Entscheidung. Senden Sie uns dazu gern eine Anfrage an support@datenservice-oeffentlicher-einkauf.de 
</details>
<br>

<details>
<summary>
Welche Systemumgebung ist die Umgebung, an die unsere Testsysteme Bekanntmachungen versenden können? Worin besteht der Unterschied zwischen der Preview und Staging Umgebung?
</summary>
<br>
Die Preview-Umgebung dient nur zum Testen. Hier werden häufig Updates eingespielt und dies ist auch unsere Testumgebung für zukünftige Releases. Die Staging-Umgebung ist eine 100% Kopie der Produktionsumgebung und sollte nur für produktionsnahe Tests genutzt werden. Beide Umgebungen liefern in die Staging-Umgebung des BKMS und TED Preview ein. Auf Staging sollten Ihre Tests genauso durchgeführt werden, wie sie es in Produktion planen, zu tun. Prinzipiell sind aber beide Umgebungen zum Test geeignet.
</details>
<br>

### Roadmap

<details>
<summary>
Gibt es eine Roadmap zur Weiterentwicklung der Komponenten des Datenservice Öffentlicher Einkauf?
</summary>
<br>
Ja. Die Informationen finden Sie hier: https://portal.ozg-vermittlungsdienst.de/roadmap
</details>
<br>

### Kommunikationskanäle

<details>
<summary> 
Wie kann das Team des Datenservice Öffentlicher Einkauf erreicht werden?
</summary>
Bitte nutzen Sie unsere Kontaktformulare:
<br>
Fragen/Anmerkungen zum Vermittlungsdienst/Self-Service Portal auf https://portal.ozg-vermittlungsdienst.de/contact
<br>
Fragen/Anmerkungen zum Redaktionssystem auf https://resy.datenservice-oeffentlicher-einkauf.de/kontakt
<br>
Fragen/Anmerkungen zum Bekanntmachungsservice auf https://oeffentlichevergabe.de/ui/de/contact
<br>
Wir sind offen für Ihre Vorschläge!
</details>
<br>

<details>
<summary>
Wie kann sichergestellt werden, dass Plattformanbieter regelmäßig über Neuigkeiten bzgl. des Datenservice informiert bleiben, insbesondere bzgl. neuer Versionen der Komponenten (Vermittlungsdienst, eSenderHub, REST-API, usw.), neuer Features, einer Aktualisierung der Roadmap etc.?
</summary>
<br>
Eine Kommunikation erfolgt durch Regelmäßige Informationstermine für die Fachverfahrenshersteller, Ankündigungen per E-Mail, aktuelle Roadmap, Versionshinweise und FAQ sind in dem veröffentlichten Dokumentationsrepository: https://github.com/EFA-FHB/ozg-vermittlungsdienst-doku . Ebenfalls gibt es das SDK-eForms-DE Repository: https://gitlab.opencode.de/OC000008125155/SDK-eforms-de.
</details>

<br>
<details>
<summary>
Wie kann sichergestellt werden, dass Plattformanbieter regelmäßig über Neuigkeiten bzgl. des eForms-DE Standard/ SDK-eForms-DE informiert bleiben.
</summary>
<br>

Die offiziellen Publikation zum Standard eForms-DE erfolgt auf https://xeinkauf.de/eforms-de/ 

Die Publikation des zugehörigen SDK erfolgt auf https://gitlab.opencode.de/OC000008125155/SDK-eforms-de 

Publikationen zum organisatorischen Rahmen siehe:

https://www.finanzen.bremen.de/digitalisierung/digitalisierung-von-verwaltungsleistungen-fuer-unternehmen/digitale-beschaffung-103422

Fragen zum DE-SDK sind über Issues im Repository zu eröffnen.
</details>
<br>

### Dokumentation

<details>
<summary>
Gibt es durch die Dokumentation zum Vermittlungsdienst (https://github.com/EFA-FHB/ozg-vermittlungsdienst-doku) bereits weiterführende Informationen zum Konstrukt des Datenservice. Inwieweit ist geplant, diese auf dem neusten Stand zu halten und ggf. durch Informationen in Form von FAQs ö. Ä. zu ergänzen? Handelt es sich bei dieser GitHub-Dokumentation um die offizielle Bereitstellung von Informationen zu diesem Thema?
</summary>
<br>

Die Github-Dokumentation wird weitergepflegt und ist bis auf weiteres die offizielle Dokumentation. Die kann auch im [Self-Service Portal](https://portal.ozg-vermittlungsdienst.de/) des DÖEs gelesen werden. 
</details>
<br>

<details>
<summary>
Wie kann für ein Release ermittelt werden, welche Versionen der Teilkomponenten unterstützt werden?  
</summary>
<br>
Unter https://portal.ozg-vermittlungsdienst.de/documentation/eForms_support ist dokumentiert, welche eForms-Versionen die Teilkomponenten unterstützen. 
Für jedes Release veröffentlichen wir Release Notes, um zu beschreiben, welche Komponente welche Version unterstützt.
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
Wie können Plattformbetreiber die Informationen des CVS-Reports der EU zu einer Bekanntmachung erhalten?</summary>
<br>
Alle Fehler und Warnungen aus dem CVS Report werden in den Statusinformationen übergeben. Dabei übergeben wir die ID, den Pfad, den Inhalt und den Text jeder angeschlagenen Regel. Es ist nicht vorgesehen, den CVS Report als Datei zurückzugeben.
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
Kann auch ein API-Key zur Authentifizierung genutz werden oder nur die Authentifizierung über Token?
</summary>
<br>
Die Authentifikation via API-Keys wird bald abgeschaltet, auch auf Preview. Langfristig können Sie sich nur über die Tokens mit Refresh alle 24h authentifizieren. In Einzelfällen werden API-Keys noch zu Test- und Debuggingzwecken genutzt. 
</details>
<br>

<details>
<summary>
In der REST-API wird von Mandanten gesprochen. Bedeutet 1 Mandant = 1 API-Key = 1 Vergabeplattform?
</summary>
<br>
Diese Annahme ist korrekt.
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
Vergabeplattformen möchten zeitnah Statusänderungen erkennen (derzeit erfolgt eine Statusabfrage pro relevanter Datenlieferung etwa alle 10 Minuten). Ist für "GET /v1/notices" geplant, die Liste auf solche Datenlieferungen einschränken oder filtern zu können, bei denen ein TED- oder DÖE-Statuswechsel seit einem übergebenen Zeitpunkt stattfand, um die Abfragelast auf dem System zu senken?
</summary>
<br>
Vielen Dank für diesen Vorschlag; wir werden eine Umsetzung prüfen.
</details>
<br>

<details>
<summary>
Wie können Plattformbetreiber die Informationen des CVS-Reports der EU zu einer Bekanntmachung erhalten, wenn diese weder in der Antwort bei Veröffentlichung (POST → /v2/notices), noch in den Statusinformationen (GET → /v1/notices/{trackingCode}) enthalten sind?
</summary>
<br>
Alle Fehler und Warnungen aus dem CVS Report werden zukünftig in den Statusinformationen übergeben. Dabei übergeben wir die ID, den Pfad, den Inhalt und den Text jeder angeschlagenen Regel. Derzeit ist es nicht vorgesehen, den CVS Report als Datei zurückzugeben.
</details>
<br>

<details>
<summary>
Ist es möglich, die online Validator API produktiv zu nutzen?
</summary>
<br>
Ja, die produktive Nutzung des Online Validators wird unterstützt. In der Produktivumgebung und in der Stagingumgebung wird die eforms-de-schematron Bugfix-Version immer die gleiche sein, wie auch im Vermittlungsdienst selbst. Auch die Nutzung des Offline-Validators (https://projekte.kosit.org/eforms/validator-edition-eforms-de) ist empfohlen. 
</details>
<br>

### Akzeptierte SDK-Versionen

<details>
<summary>
 Welche Versionen des Standards eForms-DE werden aktuell unterstützt?
</summary>
<br>
Ausführliche Informationen zur Unterstützung der eForms-Versionen finden Sie hier: https://portal.ozg-vermittlungsdienst.de/documentation/eForms_support
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
  Es gibt zwar keine Aussage zur Wahl der Sprache von Ausschreibungen in der Vergabeordnung, jedoch ist nach § 23 Abs. 1 Verwaltungsverfahrensgesetz (VwVfG) die Amtssprache deutsch. Dementsprechend ist zu erwarten, dass deutsche Behörden ihre Unterlagen immer mindestens in deutscher Sprache ausfertigen müssen. Mehrsprachigkeit ist natürlich möglich und erlaubt. 
  Für Veröffentlichende Entitäten die nicht als Behörde klassifiziert werden ist die Veröffentlichung auch ohne deutsche Sprache in Ordnung. Ab dem 31.01.2024 ist die Regel CR-DE-26 zum BT-300 temporär für die Validierung im Vermittlungsdienst deaktiviert, im Online Validator (validator.ozg-vermittlungsdienst.de) wird der Fehler jedoch weiterhin zurückgegeben. 
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
Der Standard XVergabe wird dauerhaft durch eForms-DE ersetzt und nicht weiterentwickelt. Der Abdeckungsgrad der enthaltenen Informationen ist sehr unterschiedlich. Seitens Datenservice Öffentlicher Einkauf wird kein Mapping von XVergabe auf eForms zur Verfügung gestellt.
</details>
<br>

---
[Zum Anfang](#häufig-gestellte-fragen)


