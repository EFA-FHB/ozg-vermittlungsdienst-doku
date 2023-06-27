### EfA-Umsetzungsprojekt "Zugang zur öffentlichen Vergabe"**
# Häufig gestellte Fragen
[Übersicht](/Readme.md)
<br>

- [Datenservice Öffentlicher Einkauf](#datenservice-öffentlicher-einkauf)
- [GDK (eForms-DE Standard/SDK-eForms-DE)](#gdk-eforms-de-standardsdk-eforms-de)
- [Allgemein](#allgemein)
<br>

## Datenservice Öffentlicher Einkauf

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
Alle Versionen außer eForms-DE 1.0.1 werden nur noch vorübergehend unterstützt!
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

### API-Vermittlungsservice

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
Wird es möglich sein, Berichtigungen zum Datenservice zu senden, welcher diese als eigenständiger, neuer eSender an TED übermittelt, auch wenn die Bekanntmachungen zuvor durch den Plattformbetreiber als ehemaliger eSender an TED übermittelt wurde? Genauer gesagt: • Wie wird mit einem Wechsel des eSenders für eine Bekanntmachung umgegangen, wenn diese berichtigt werden soll? • Wie wird mit einem Wechsel des eSenders innerhalb eines Verfahrens mit mehreren Bekanntmachungen umgegangen?
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

## GDK (eForms-DE Standard/SDK-eForms-DE)
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

---
[Zum Anfang](#häufig-gestellte-fragen)
