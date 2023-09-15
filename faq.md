### EfA-Umsetzungsprojekt "Zugang zur öffentlichen Vergabe"**
# Häufig gestellte Fragen
[Übersicht](/Readme.md)
<br>

- [Datenservice Öffentlicher Einkauf](#datenservice-öffentlicher-einkauf)
- [Standard eForms-DE und SDK-DE](#standard-eForms-DE-und-SDK-DE)
- [Allgemein](#allgemein)
<br>

## Datenservice Öffentlicher Einkauf

### Anbindung

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
Bei der Accounterstellung muss eine Kontaktemail eines FVH angegeben werden. Wozu wird diese verwendet?
</summary>
<br>
Diese Email wird verwendet, wenn wir proaktiv auf Sie zugehen wollen. Dies kann der Fall sein, wenn es beispielsweise Auffälligkeiten mit ihrem Account oder den eingelieferten Bekanntmachungen gibt oder wir generelle Informationen an alle Accountverantwortlichen versenden. 
</details>
<br>

<details>
<summary>
Können mehrere Accounts gleichzeitig beantragt werden? Wie viele Accounts empfehlen sich jeweils für Preview und Staging?
</summary>
<br>
Senden Sie uns gern eine Liste von benötigten Accounts an oeffentliche-vergabe-support@nortal.com Inklusive aller benötigter Informationen pro Account. Wir empfehlen, auf Staging exakt so viele Accounts zu verwenden, wie sie für Produktion planen, zu nutzen. Zusätzlich sind natürlich beliebig viele Testaccounts auf Preview und Staging möglich.  
</details>
<br>

<details>
<summary>
Kann Zugriff auf die BKMS Alpha-Umgebung gewährt werden?
</summary>
<br>
Wenn nötig kann ein Zugriff auf die BKMS Alpha-Umgebung beantragt werden. Senden Sie hierfür bitte eine Anfrage an oeffentliche-vergabe-support@nortal.com. Beachten Sie aber, dass dies einige Zeit in Anspruch nehmen kann, da eine manuelle Prüfung durchgeführt wird. 
</details>
<br>

<details>
<summary>
Zur Anforderung von Zugängen soll die URL der Vergabeplattform angegeben werden. Wozu dient diese Angabe?
</summary>
<br>
Die Angabe der URL dient dazu, die genannten Systeme voneinander unterscheiden zu können, Ihnen den korrekten Zugang zu ermöglichen und Duplikate zu vermeiden. Vergabeplattformen sind die Systeme, in denen Bekanntmachungen veröffentlicht werden, die URL der Vergabeplattform kann so z.B. alpha.oeffentlichevergabe.de (Test-Umgebung BKMS) sein. Diese URL dient dazu, zu identifizieren, auf welcher Plattform Sie Ihre Bekanntmachungen derzeit veröffentlichen. Zu diesem Thema ist uns bewusst, dass es hier unterschiedliche Vorgehensweisen je nach Struktur des Systems der jeweiligen FVH geben kann. Prinzipiell gilt, dass sie einen Account pro System benötigen, dass zukünftig in den Vermittlungsdient einliefern soll. Wenn Sie unsicher sind, welche Systeme/ Plattformen für Sie an den DöE anzuschließen sind, unterstützen wir Sie gern bei dieser Entscheidung. Senden Sie uns dazu gern eine Anfrage an oeffentliche-vergabe-support@nortal.com. 
</details>
<br>

<details>
<summary>
Welche Systemumgebung ist die Umgebung, an die unsere Testsysteme Bekanntmachungen versenden können? Worin besteht der Unterschied zwischen der Preview und Staging Umgebung?
</summary>
<br>
Die Preview-Umgebung dient nur zum Testen. Hier werden häufig Updates eingespielt und dies ist auch unsere Testumgebung für zukünftige Releases. Die Staging-Umgebung ist eine 100% Kopie der Produktionsumgebung und sollte nur für produktionsnahe Tests genutzt werden. Beide Umgebungen liefern in die Alpha Umgebung des BKMS und TED Preview ein. Auf Staging sollten Ihre Tests genauso durchgeführt werden, wie sie es in Produktion planen, zu tun. Prinzipiell sind aber beide Umgebungen zum Test geeignet.
</details>
<br>

<details>
<summary>
Wird der Datenservice eine Render-Methode analog der Render-Methoden der EU anbieten? 
</summary>
<br>
Ein Notice-Viewer für das Rendering von eForms-DE Dokumenten in HTML ist bereits in Arbeit und wird vorraussichtlich Mitte/ Ende September veröffentlicht. Der Endpunkt wurde bereits im Vermittlungsdienst auf der Previewumgebung veröffentlicht, damit der Endpunkt bereits eingebunden werden kann. Dieser liefert eine gerenderte Beispieldatei zurück. Feedback und Anregungen nehmen wir gern unter oeffentliche-vergabe-support@nortal.com entgegen.
</details>
<br>

### Roadmap

<details>
<summary>
Gibt es eine Roadmap bezüglich der Weiterentwicklung auch nach Stichtag 25.10.2023 der Komponenten Vermittlungsdienst, eSenderHub, usw., insbesondere im Hinblick auf Feature- und API-Erweiterungen, Meilensteine und die jeweiligen Go-live-Zeitpunkte?
</summary>
<br>
Zum derzeitigen Stand sind nach dem 25.10.2023 noch zwei Releases für den Datenservice geplant. Der Inhalt der Releases bezieht sich primär auf Komfortfunktionen und Auswertungsmöglichkeiten. API-Änderungen und Erweiterungen sind nach aktuellem Planungsstand nicht vorgesehen.
</details>
<br>

<details>
<summary>
Welche Features (abgesehen vom Umfang des Production Release) befinden sich noch in Planung? Diese Frage zielt insbesondere auf die weiteren Dienste des EU-Portals "eNotices2" ab, wie Generierung von PDF-Darstellungen, Einsicht und Eingriff in Prozesse über eine Weboberfläche, Eingeben von Bekanntmachungen über Weboberflächen, etc., die aufgrund des zentralen eSender-Dienstes nicht mehr nutzbar sind.
</summary>
<br>
Generierung der PDF/HTML Darstellung: Aktuell in Klärung, der Bedarf wurde durch das Projekt anerkannt.

Einsicht in Prozess über Weboberfläche (Dashboard):
Aktuell in Umsetzung: Geplant ist die Einsicht in Statusinformationen für einen Mandanten und evtl. das Nutzen des Stop-Endpunkts über die gleiche Oberfläche.
</details>
<br>

### Go-Live

<details>
<summary>
Ist der Zeitpunkt für den produktiven Go-live (d.h. vollständige Bereitstellung der kompletten Produktivumgebung) bereits bekannt? Ist der Zeitpunkt für die Bereitstellung des Production Release bereits bekannt?**
</summary>
<br>
Zum aktuellen Standpunkt ist eine technische Pilotphase des Datenservice Öffentlicher Einkauf inklusive eSender-Hub Ende Juni 2023 geplant. Der Start der Pilotphase für eine Anbindung per PEPPOL ist für Ende Juli 2023 geplant. Hier bestehen allerdings Abhängigkeiten zu Zulieferungen der EU und des Expertengremiums eForms. Das Inkrafttreten der rechtlichen Verpflichtung erfolgt zum 25.10.2023; eine entsprechende Freigabe des Bundesrats wird bis Sommer 2023 erwartet.
</details>
<br>

<details>
<summary>
Werden zum Go-live alle 40 EU-Bekanntmachungstypen unterstützt? Wann steht der genaue Umfang des Production Release fest? Aktuell wird eine Umsetzung einiger Features mit "voraussichtlich ja" für den Production Release angekündigt. Wann wird bekannt sein, ob eine tatsächliche Umsetzung im Production Release erfolgen wird (https://github.com/EFA-FHB/ozg-vermittlungsdienst-dokuoku/blob/development/Releases.md)?
</summary>
<br>
Es werden alle Dokumententypen aus eForms-DE angenommen (40 für die Oberschwelle und 3 für die Unterschwelle). Wo notwendig werden diese generisch in das eForms-EU Format konvertiert. Dies entspricht den Inhalten des aktuellen eForms-DE Standards.
</details>
<br>

<details>
<summary>
Ist es möglich ab dem 25.10.2023 weiterhin Bekanntmachungen über eNotices2 einzuliefern? 
</summary>
<br>
Ab dem 25.10.2023 müssen rechtlich alle oberschwelligen Bekanntmachungen im eForms-DE Format über den Datenservice Offentlicher Einkauf eingeliefert werden. Eine direkte Einlieferung über eNotices2 ist nicht standardkonform, da die Anpassungen des eForms-DE Standards nicht berücksichtigt würden und ist rechtlich nicht mehr zulässig. 
</details>
<br>

<details>
<summary>
Wird der Datenservice Öffentlicher Einkauf auch den TED-2.0.9-XML-Format bis zum Stichtag (25.10.2023) unterstützen? Soll bis zum Stichtag weiter über das alte Format bei TED eingeliefert werden? 
</summary>
<br>
Bis eForms-DE verpflichtend wird, kann noch im alten Format direkt bei TED eingeliefert werden, der Datenservice Öffentlicher Einkauf unterstützt dieses Format allerdings nicht. Der Datenservice kann ausschließlich mit eForms genutzt werden. Ab 25.10. muss zwingend über den Datenservice öffentlicher Einkauf mit dem Format eForms-DE 1.0.1 oder 1.1.0 eingeliefert werden. 
</details>
<br>

<details>
<summary>
Wird es am 25. Oktober eine Einführung von eForms sowohl für Ober- (EU) als auch Unterschwellenwerte (National) geben oder nur für die EU-Ebene?
</summary>
<br>
Die beiden Standards eForms-EU und eForms-DE sind bereits eingeführt und können genutzt werden. Ab dem 25. Oktober müssen sowohl nationale als auch EU-weite Mitteilungen im Format eForms-DE an die Schlichtungsstelle übermittelt werden. Welche Formate derzeit unterstützt und verarbeitet werden, erfahren Sie in unserer Vorschau unter https://github.com/EFA-FHB/ozg-vermittlungsdienst-doku/blob/development/documentation/eForms_support.md.
</details>
<br>


### Kommunikationskanäle

<details>
<summary>
Wie kann sichergestellt werden, dass Plattformanbieter regelmäßig über Neuigkeiten bzgl. des Datenservice informiert bleiben, insbesondere bzgl. neuer Versionen der Komponenten (Vermittlungsdienst, eSenderHub, REST-API, usw.), neuer Features, einer Aktualisierung der Roadmap etc.?
</summary>
<br>
Eine Kommunikation erfolgt durch Regelmäßige Informationstermine für die Fachverfahrenshersteller, Ankündigungen per E-Mail, aktuelle Roadmap, Versionshinweise und FAQ sind in dem veröffentlichten Dokumentationsrepository: https://github.com/EFA-FHB/ozg-vermittlungsdienst-doku. Ebenfalls gibt es das SDK-eForms-DE Repository: https://gitlab.opencode.de/OC000008125155/SDK-eforms-de.

<u>Erreichbarkeiten:</u>

*Fragen und Verbesserungsvorschläge* gegenüber dem Vermittlungsdienst und dem eSender-Hub können an oeffentliche-vergabe@nortal.com gerichtet werden. Alternativ können Github Issues im Dokumentationsrepository und dem SDK-eForms-DE Repository erstellt werden.

Bei *Supportanfragen zum Betrieb* des Vermittlungsdienst und des eSender-Hubs wenden Sie sich bitte an: oeffentliche-vergabe-support@nortal.com.

*Fragen zum Bekanntmachungsservice* können an support-oeffentlichevergabe@bdr.de gerichtet werden.

Wir sind offen für Ihre Vorschläge!
</details>
<br>

### Dokumentation

<details>
<summary>
Gibt es durch die Dokumentation zum Vermittlungsdienst (https://github.com/EFA-FHB/ozg-vermittlungsdienst-doku) bereits weiterführende Informationen zum Konstrukt des Datenservice. Inwieweit ist geplant, diese auf dem neusten Stand zu halten und ggf. durch Informationen in Form von FAQs ö. Ä. zu ergänzen? Handelt es sich bei dieser GitHub-Dokumentation um die offizielle Bereitstellung von Informationen zu diesem Thema?
</summary>
<br>
Die Github-Dokumentation wird weitergepflegt und ist bis auf weiteres die offizielle Dokumentation, der finale Ort der Doku steht aber noch nicht fest. 
</details>
<br>

<details>
<summary>
Wie kann für ein Release ermittelt werden, welche Versionen der Teilkomponenten unterstützt werden. 
</summary>
<br>
Unter [eForms Unterstützung](/documentation/eForms_support.md) ist dokumentiert welche eForms-Versionen die Teilkomponenten unterstützen.
<br>
Für jedes Release verffentlichen wir releasenotes, um zu beschreiben, welche Komponente welche Version unterstützt. Die Versionen eForms-DE 1.0.1 und 1.1.0 werden ab 13. September in allen Komponenten des Datenservice öffentlicher Einkauf unterstützt. 
</details>
<br>

<details>
<summary>
Ist die Dokumentation zum Vermittlungsdienst (https://github.com/EFA-FHB/ozg-vermittlungsdienst-doku) die offizielle Dokumentation?
</summary>
<br>
Ja, die Github-Dokumentation wird regelmäßig aktualisiert und ist bis auf weiteres die offizielle Dokumentation. Langfristig wird die Dokumentation ggf. in ein Portal umgezogen. Hierüber informieren wir Sie rechtzeitig. 
</details>
<br>


### Statusmodell
<details>
<summary>
Mit den Statusänderungsmeldungen der EU haben Plattformanbieter auch weitergehende Metadaten zum jeweiligen Status erhalten, bspw. die Submission-ID, den konkreten Zeitpunkt der Veröffentlichung auf TED, die ABl.-Nummer etc. Mit der ABl.-Nummer hatten Kunden bisher die Möglichkeit, bei Folgebekanntmachungen zu diesem Auftrag (Angabe "frühere Bekanntmachung desselben Auftrags") diese Nummern nicht mehr manuell eintragen zu müssen, da diese vorbefüllt werden konnten. Besteht auch weiterhin die Möglichkeit, o. g. Informationen zur Veröffentlichung zu erhalten, um den Kunden diese Reihe an Funktionalitäten zu bieten?
</summary>
<br>
TED stellt nicht mehr dieselben Metadaten pro Bekanntmachung zur Verfügung wie früher, wir geben alle relevanten Infos zurück, die wir bekommen.
Die folgenden Daten werden von TED zu einer Bekanntmachung zur Verfügung gestellt.

![Daten einer Bekanntmachung von TED](/images/faq/Bekanntmachung_Daten_von_TED.png) 

Wir prozessieren dabei den Status, den Zeitpunkt der Einlieferung und wenn gegeben den Zeitpunkt der Veröffentlichung. Die ABl.-Nummer wird in eNotices2 nicht mehr verwendet. Wenn Sie weitere Daten aus dieser Abfrage benötigen, schreiben Sie uns bitte eine Mail mit Ihren Anforderungen an: oeffentliche-vergabe-support@nortal.com. Gerne organisieren wir einen bilateralen Austausch.
</details>
<br>

<details>
<summary>
Wie werden abgelehnte Bekanntmachungen in Fehlerzuständen wie 'REJECTED' Status von TED oder einem 'INTERNAL ERROR' Status von BKMS weiter prozessiert? 
</summary>
<br>
Es wird ein internes Monitoring geben, um auf Fehlerzustände (Status InternalError) oder Bugs zu reagieren. Aktuell ist Nortal unter der E-Mail Adresse oeffentliche-vergabe-support@nortal.com der erste Ansprechpartner, wenn Sie Probleme mit Ihren Einlieferungen haben udn Ihre Bekanntmachungen in einen Fehlerstatus laufen. Generell deuten solche Fehlerzustände auf Bugs im DöE, in TED oder in der versendeten Bekanntmachung hin. Wann immer Fehler im System passieren (Beispielsweise bei Ablehnung durch TED), werden diese geloggt, sodass bei Bedarf ein Support Ticket erstellt und eine technische Analyse durchgeführt werden kann. Es wird dann individuell entschieden, welche Maßnahmen zur behebung des Fehlers zielführend sind. Bei technischen Fehlern kann die Bekanntmachung entweder nach Behebung erneut als neue Version versendet oder intern manuell erneut prozessiert werden. Dies ist jedoch vom Einzelfall abhängig. Sollte TED ablehnen besteht die Möglichkeit, dass ein Fehler in der Bekanntmachung existiert, beispilesweise die notice-id bereits genutzt wird. In diesem Fall wird gespeichert, welche Fehlermeldung TED bei der Ablehnung zurückgeliefert hat, sodass entsprechend reagiert werden kann. 
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
Wird es möglich sein, die online Validator API produktiv zu nutzen?
</summary>
<br>
Derzeit kann keine Verfügbarkeit des Online Validators garantiert werden. Wir prüfen aber gerade, ob ides in Zukunft möglich gemacht werden kann
</details>
<br>

### Laufende Vergabeverfahren und Umstellung auf den neuen Datenservice

<details>
<summary>
Die Komponenten des Datenservice können nur die neuen eForms-Strukturen entgegennehmen. In den Vergabeplattformen wird aktuell zur EU mit den TED-Schema-Strukturen kommuniziert. Für laufende Vergabeverfahren wird es so sein, dass bspw. nach einer Auftragsbekanntmachung eine Bekanntmachung vergebener Aufträge veröffentlicht wird oder bspw. für eine Bekanntmachung vergebener Aufträge eine Auftragsänderung. Können Bekanntmachungen bis zum Stichtag 25.10.2023 für laufende Vergabeverfahren weiterhin im TED-2.0.9-XML-Format an den Datenservice gesendet werden oder sollen diese bis zum Stichtag wie bisher direkt an TED übermittelt werden?
</summary>
<br>
Bis eForms-DE verpflichtend wird, kann noch im alten Format direkt bei TED eingeliefert werden, der Datenservice Öffentlicher Einkauf unterstützt dieses Format allerdings nicht. Der Datenservice kann ausschließlich mit eForms genutzt werden. Wir empfehlen allerdings, bereits ab Start der Pilotphase Einlieferungen im eForms-DE Standard über den Datenservice durchzuführen.

Die Antwortfindung ggü. TED ist weiterhin im Gange.
</details>
<br>

<details>
<summary>
Wird es möglich sein, Berichtigungen zum Datenservice zu senden, welcher diese als eigenständiger, neuer eSender-Hub an TED übermittelt, auch wenn die Bekanntmachungen zuvor durch den Plattformbetreiber als ehemaliger eSender-Hub an TED übermittelt wurde? Genauer gesagt: • Wie wird mit einem Wechsel des eSenders für eine Bekanntmachung umgegangen, wenn diese berichtigt werden soll? • Wie wird mit einem Wechsel des eSenders innerhalb eines Verfahrens mit mehreren Bekanntmachungen umgegangen?
</summary>
<br>
Es wird nicht möglich sein, über den Datenservice den Status einer alten Bekanntmachung abzufragen oder eine alte Bekanntmachung zu stoppen, die nicht über den Datenservice eingeliefert wurde, da der Datenservice keine Anfragen zu Bekanntmachungen von anderen eSendern durchführen kann. Dies ist eine Restriktion von TED zu einliefernden eSendern.

Die Berichtigung einer Bekanntmachung ist prinzipiell möglich, indem vor Veröffentlichung einer Bekanntmachung eine neue Version einer Bekanntmachung im eForms Format an den Datenservice verschickt wird. Dieses Update wird dann zu TED versendet und TED veröffentlicht die aktuellste Version der Bekanntmachung. Wenn die ursprüngliche Bekanntmachung bereits veröffentlicht ist, muss eine „Change Notice“ versendet werden.

Es ist derzeit in Klärung mit TED, wie auf eine vorherige Bekanntmachung im alten Format referenziert werden kann, um diese miteinander zu verknüpfen und inwiefern der Wechsel des einliefernden eSenders Einfluss auf Änderungen hat.
</details>
<br>

### Akzeptierte SDK-Versionen

<details>
<summary>
Laut unseres Kenntnisstands ist das eForms-DE-Format nicht mehr kompatibel zum eForms-EU-Format, da es kein reines Subset mehr davon ist. Somit können mit dem eForms-DE-Format keinerlei API-Funktionen der EU aufgerufen werden, sei es die neue eForms-API oder die APIs der Viewer-Services (PDF-/HTML-Rendering). Ist es korrekt, dass der neue Datenservice keine Render-Methode anbietet und auch die Render-Methoden der EU aufgrund der Inkompatibilität nicht mehr verwendet werden können? Wie können Funktionen wie PDF-/HTML-Rendering dennoch genutzt werden?
</summary>
<br>

Frage 2 unter [Roadmap](#roadmap) - Der Bedarf für eine Rendering Methode wurde bereits aufgenommen und wird derzeit analysiert.

Der eSender-Hub trägt Sorge dafür, entsprechend der eingelieferten eForms-DE Version diese Bekanntmachung in ein valides eForms-EU Dokument zu transformieren, um damit die TED-Funktionen nutzen zu können.
</details>
<br>

<details>
<summary>
In den eForms ist eine Angabe "CustomizationID", z. B. `<cbc:CustomizationID>eforms-sdk-1.7</cbc:CustomizationID>`, notwendig. • Ist unsere Annahme korrekt, dass der eSender-Hub eine hier angegebene SDK-eForms-DE-Version auf die entsprechende EU-Version mappt? • Welche SDK-Versionen (DE bzw. EU) können hier durch den Plattformbetreiber eingetragen werden?
</summary>
<br>
Für die ab vorrausichtlich Juni unterstützte Version des nationalen Standards eForms-DE lautet der Versionsbezeichner des zugehörigen SDK "eforms-de-1.0", siehe Datei eforms-de.validation.sch im Verzeichnis schematrons/schematron-de. (https://gitlab.opencode.de/OC000008125155/SDK-eforms-de/-/tree/main/sdk/schematrons/schematron_de)
</details>
<br>

<details>
<summary>
Derzeit scheint der Mediator auch eForm-EU bis SDK-Version 1.5 zu akzeptieren. Wie lange wird dies noch zur Verfügung stehen? Hintergrund ist, dass Vergabestellen häufig längere Zeit (oft Wochen) zwischen Anlage der Bekanntmachung (bzw. Verfahrensstart) und deren Veröffentlichung benötigen. Daher ist ein längerer Zeitraum zwischen Beginn der Produktivstellung der eForms-DE und Abschaltung der eForms-EU notwendig.
</summary>
<br>
Aktuell ist geplant die Unterstützung für eforms-EU 1.5 mit dem Release im Juli abzuschalten, da sie auch im Bekanntmachungsservice nicht unterstützt wird. Falls es notwendig ist, diese oder andere EU Versionen länger zu unterstützen, kann darüber diskutiert werden.
</details>
<br>

### Sonderfälle

<details>
<summary>
Wird es für etwaige seltene, jedoch denkbare, Sonderfälle entsprechende Vorgehensmodelle geben, auf die sich bei Eintreten der Fälle berufen werden kann? Hierzu sollen zwei Beispiele dienen:<br>
Beispiel 1:<br>
Der Vermittlungsdienst nimmt eine Bekanntmachung entgegen, welche laut Vermittlungsdienst/eSenderHub valide ist. Die EU lehnt später die Entgegennahme ab (Status "rejected"), etwa weil die SDK-Version nicht mehr unterstützt wird. Der Plattformbetreiber erhält gemäß Statusmapping den Status "internalError". Wie würde das weitere Vorgehen in dem Falle aussehen?<br>
Beispiel 2:<br>
Laut der EU wird demnächst eine Business-Rule eingeführt, die es nicht mehr erlaubt, dass das "dispatch date" in einer Bekanntmachung (Tag der Absendung der Bekanntmachung), welches von den Plattformbetreibern gesetzt wird und der Zeitpunkt der Übermittlung des Datenservice an die EU, max. um 24 Stunden abweichen darf, sonst wird die Annahme durch die EU blockiert. Etwaige technische Probleme im Datenservice müssten somit immer innerhalb von 24 Stunden gelöst werden.
</summary>
<br>
Es wird eine Supportstruktur geben, um auf Fehlerzustände (Status InternalError) oder Bugs zu reagieren. Es ist derzeit in Klärung, wie diese Supportstruktur zu welchem Zeitpunkt des Betriebs aussehen wird. Zu Beginn ab Juni ist Nortal unter der E-Mail Adresse oeffentliche-vergabe-support@nortal.com der erste Ansprechpartner. Wann immer Fehler im System passieren (Beispielsweise bei Ablehnung durch TED), werden diese geloggt, sodass bei Bedarf ein Support Ticket erstellt und eine technische Analyse durchgeführt werden kann.
</details>
<br>

## Standard eForms-DE und SDK-DE
[Zum Anfang](#häufig-gestellte-fragen)<br>

**Bitte beachten Sie, dass wir alle Fragen bezüglich eForms gemäß unserem aktuellen Wissensstand beantworten. Änderungen der Informationen sind jederzeit durch die KoSIT möglich. Bei weiteren Fragen zum Thema eForms wenden Sie sich gerne per E-Mail an eforms@finanzen.bremen.de** 

### Roadmap

<details>
<summary>
Wird es eine Roadmap bezüglich der Weiterentwicklung des SDK geben? Dies ist für Plattformbetreiber insbesondere vor dem Hintergrund der Anpassungszeitpunkte an neue SDK-EU-Versionen interessant, da das SDK-DE und SDK-EU aktuell in ihrer Versionierung noch auseinandergehen.
</summary>
<br>

Die Versionsbezeichnungen der SDK zum jeweiligen nationalen Standard eForms-DE orientieren sich an den Versionsbezeichnungen des Standards eForms-DE. Zu jedem eForms-DE-SDK ist angegeben, auf welcher europäischen SDK-Version diese beruht. (siehe auch Erläuterung auf https://gitlab.opencode.de/OC000008125155/SDK-eforms-de)

Es ist nicht geplant, dass zu jeder minor Version des eForms-EU auch eine neue Version eForms-DE veröffentlicht wird. Deshalb wird die Versionierung von eForms-EU und eForms-DE auch in Zukunft nicht direkt übereinstimmen. Es wird aber immer für jede eForms-DE Version exakt eine korrespondierende eForms-EU Version geben.
</details>
<br>

<details>
<summary>
In welchem Zeitrahmen wird ein DE-Update zur Verfügung gestellt, nachdem ein EU-Update veröffentlicht wurde?
</summary>
<br>

Es ist hierbei zu beachten, dass nicht für jedes EU-Update automatisch ein DE-Update notwendig ist.
<br>
Das GDK liegt nicht in der Verantwortung der KoSIT. Jedoch die Spezifikation eForms-DE. Wie beim 1. technischen Arbeitstreffen gemeinsam festgestellt wurde, können wir angesichts noch vorliegenden Unklarheiten über in Kraft treten und Lebensdauer der Versionen des EU-SDK, derzeit noch keine einfache Antwort mit klaren Daten geben. Was feststeht ist, dass eine bestimmte Version eForms-DE sich kompatibel zu einer bestimmten Version eForms-SDK erklärt und dies möglichst zeitnah geschehen soll. Wie derzeit eForms-DE 1.0.1 kompatibel zu eForms-SDK 1.5.1 ist (SDK 1.5.1 wurde am 20. Januar 2023 veröffentlicht und eForms-DE am 5. Februar). D.h. implizit, dass es nicht zu jeder Version eForms-SDK eine Version eForms-DE geben wird.
</details>
<br>

### Go-Live

<details>
<summary>
Mit welcher SDK-Version soll der produktive Go-live erfolgen?
</summary>
<br>

Unterstützt wird die aktuelle Version 1.0.1 und eine weitere Version voraussichtlich ab September 2023.
</details>
<br>

### Kommunikationskanal

<details>
<summary>
Wie kann sichergestellt werden, dass Plattformanbieter regelmäßig über Neuigkeiten bzgl. des eForms-DE Standard/ SDK-eForms-DE informiert bleiben.
</summary>
<br>

Die offiziellen Publikation zum Standard eForms-DE erfolgt auf https://xeinkauf.de/eforms-de/ .

Die Publikation des zugehörigen SDK erfolgt auf https://gitlab.opencode.de/OC000008125155/SDK-eforms-de .

Publikationen zum organisatorischen Rahmen siehe:

https://www.finanzen.bremen.de/digitalisierung/digitalisierung-von-verwaltungsleistungen-fuer-unternehmen/digitale-beschaffung-103422

Fragen zum DE-SDK sind über Issues im Repository zu eröffnen.
</details>
<br>

### Abweichungen

<details>
<summary>
Bei der Durchsicht der Dokumente des nationalen Tailorings sind einige Unstimmigkeiten bzgl. Losgruppen entdeckt worden. Gemäß eForms-DE Standard v1.0.0 und v1.0.1 werden die optionalen Felder der Gruppe "Vergabe — Gruppen von Losen" oder "Rahmenvereinbarung, Losgruppe, Höchstwert" mit Anzahl "0" markiert und sollen daher nicht verwendet werden können. Im SDK-eForms-DE v1.5.1, welches auf dem eForms-DE-Standard v1.0.0 basiert, tauchen die Felder hingegen in der fields.json auf. Wie soll zukünftig im Allgemeinen mit Losgruppen umgegangen werden?
</summary>
<br>

Der Einfachheit halber und zur Vermeidung von Inkonsistenzen mit von EU gelieferten Schematron-Regeln enthält das SDK zum nationalen Standard eForms-DE auf technischer Ebene Felder, die dennoch gemäß des Standards eForms-DE nicht genutzt werden.

Losgruppen sind in eForms-DE nicht vorgesehen.
</details>
<br>

### Verlinkung 

<details>
<summary>
Wie erfolgte die Verlinkung bzw. der Verweis auf vorherige Bekanntmachungen?
 </summary> 
  
 Details zur Verlinkung der Bekanntmachungen siehe
https://github.com/EFA-FHB/ozg-vermittlungsdienst-doku/blob/main/documentation/eForms_Erstellung.md

Weitere Details zur Verwendung der Referenzen können hier nachgelesen werden: https://docs.ted.europa.eu/eforms/latest/schema/procedure-lot-part-information.html#previousNoticeSection 

</details>
<br>


## Fragen zu BG/BT

### Nationale Ausschlussgründe (BT-67 exclusion grounds)

<details>
<summary>
Weshalb wurden die Codes zu nationalen Ausschlussgründen der Codeliste "Criterion Exclusion Grounds" in der Version eForms-DE v1.1.0 verändert?
</summary>

<br>

Entfernt wurden lediglich die Codes "ex-os" (Ausschlusshinweise Oberschwelle) und "ex-us" (Ausschlusshinweise Unterschwelle), da stattdessen der in der EU bestehende Code "nati-ground" (rein nationale Ausschlussgründe) verwendet werden kann.

Wir haben das Changelog für sie aktualisiert: https://projekte.kosit.org/eforms/eforms-de-codelist/-/blob/main/CHANGELOG.md.
  </details>
<details>
<summary>
Welcher Auschlussgrund kann vorbelegt werden, sollten alle Gründe gleichermaßen zutreffen?
</summary>
Für den Fall, dass alle Ausschlussgründe gleichermaßen zutreffen, ist "nati-ground" (rein nationale Ausschlussgründe) der umfassendste Code.
</details>
<br>

### Bekanntmachung der Ergebnisse (BG-7), Angebot (BG-320 Angebot)
<details>
<summary>
Sollen im Element „Bekanntmachung über die Ergebnisse“ (BG-7) > „Angebot“ (BG-320) nur bezuschlagte oder alle eingegangenen Angebote/Lose gelistet werden?
</summary>
<br>

In dieser Frage gelten unverändert die Bestimmungen der jeweiligen Richtlinien und Verordnungen unter welche das Vergabeverfahren fällt. 
</details>
<br>

### Keine sofortige Veröffentlichung (BG-8; BT-195/BT196/BT197/BT-198) 
<details>
<summary>
Warum sind Angabe der Befristung der nicht zu veröffentlichenden Felder bei Pflichtfeldern obligatorisch?
</summary>
<br>

Die Spezifikation folgt in diesem Punkt dem Implementation Handbook der EU. Es handelt sich um eine Soll-Formulierung, die keine Geschäftsregel erfordert. 
Details: https://op.europa.eu/en/publication-detail/-/publication/73a78487-cc8b-11ea-adf7-01aa75ed71a1 
</details>
<br>

### Fahrzeugklasse (BT-723)
<details>
<summary>
 Hilfestellungen zur Auswahl der Werte der Codeliste für BT-723 Fahrzeugklasse
</summary>
<br>

In der finalen Version von eForms-DE-v1.0.1 ist die Codelist für die Fahrzeugklassen angepasst. Es sind nur noch die "Einzelwerte" sind diese zu verwenden.

Eine Hilfestellung ist Anhang II der Rahmenrichtlinie https://eur-lex.europa.eu/legal-content/DE/TXT/HTML/?uri=CELEX:32007L0046 zu entnehmen.:
|Code|Bedeutung|
|---|---|
|M1|Leichtes Nutzfahrzeug der Fahrzeugklasse M1 bzw. Pkw (Kraftfahrzeuge für die Personenbeförderung mit höchstens acht Sitzplätzen außer dem Fahrersitz.)|
|M2|Leichtes Nutzfahrzeug der Fahrzeugklasse M2 	(Kraftfahrzeuge für die Personenbeförderung mit mehr als acht Sitzplätzen außer dem Fahrersitz und einer zulässigen Gesamtmasse bis zu 5 Tonnen.)|
|N1|Leichtes Nutzfahrzeug der Fahrzeugklasse N1 	(Kraftfahrzeuge für die Güterbeförderung mit einer zulässigen Gesamtmasse bis zu 3,5 Tonnen.)
|N2|Schweres Nutzfahrzeug der Fahrzeugklasse N2 (Kraftfahrzeuge für die Güterbeförderung mit einer zulässigen Gesamtmasse von mehr als 3,5 Tonnen bis zu 12 Tonnen.)|
|N3|Schweres Nutzfahrzeug der Fahrzeugklasse N3	(Kraftfahrzeuge für die Güterbeförderung mit einer zulässigen Gesamtmasse von mehr als 12 Tonnen.)|
|M3|Bus der Fahrzeugklasse M3	(Kraftfahrzeuge für die Personenbeförderung mit mehr als acht Sitzplätzen außer dem Fahrersitz und einer zulässigen Gesamtmasse von mehr als 5 Tonnen.)

</details>
<br>

### Lose
<details>
<summary>
Wie sind die LOT-Einträge bei "keinem", einen oder mehreren Losen zu verwenden?
</summary>
<br>

Laut TED muss, bei 'keinem' Los nur ein technischer Lot eintrag vorhanden sein mit dem Wert LOT-0000. 
Wenn es zwei Lose gibt, gibt es zwei Lots mit den Werten LOT-0001 und LOT-0002. Bei 5 Losen z.B. LOT-0001, LOT-0002, LOT-0003, LOT-0004, LOT-0005. Die Struktur von LOT-0000 ist komplett identisch wie von jedem anderen LOT, also auch LOT-0001. Lediglich die ID ist anders.

Doku ist hier zu finden: https://docs.ted.europa.eu/eforms/1.5/schema/procedure-lot-part-information.html
</details>
<br>



### NUTS-Codes

*Weitere Informationen zum Umgang mit NUTS-Codes werden hier nachgereicht.*



# Allgemein
[Zum Anfang](#häufig-gestellte-fragen)

### eNotices Portal der EU

<details>
<summary>
Nach Angabe der EU (siehe https://simap.ted.europa.eu/de_DE/web/simap/statistical-production-files - Statistik 2023 nach Format und Übermittlungskanal) haben bisher noch viele Auftraggeber das EU-Portal eNotices zur Erstellung und Veröffentlichung der Bekanntmachung genutzt. eNotices2, das neue Portal mit den integrierten eForms, kennt und berücksichtigt nicht das nationale Tailoring. Dürften Vergabestellen weiterhin eNotices2 verwenden, obwohl dort das nationale Tailoring nicht berücksichtigt ist?
</summary>
<br>
Die Beantwortung dieser rechtlichen Fragestellung ist angestoßen und wird nach erfolgter Klärung beantwortet.
</details>
<br>

<details>
<summary>
Wird es ein neues Portal für interessierte Unternehmen geben, das die jetzige service.bund.de-Seite ersetzt? 
</summary>
<br>
Es ist kein weiteres Portal zum Ersatz von sevice.bund.de geplant. Projektwunsch ist es, dass alle Bekanntmachungen (Ober- und Unterschwelle) im Datenservice Öffentlicher Einkauf vorhanden sind. 
</details>
<br>

<details>
<summary>
Existiert ein Mapping von XVergabe auf eForms?
</summary>
<br>
Wir als DöE können leider kein Mapping zur XVergabe zur Verfügung stellen. Außerdem ist die Xvergabe bereits veraltet und somit nicht mehr auf dem selben Stand wie eForms
</details>
<br>

---
[Zum Anfang](#häufig-gestellte-fragen)
