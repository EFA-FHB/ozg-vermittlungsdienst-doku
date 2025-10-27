
# Datenservice Öffentlicher Einkauf

### Anbindung

<details>
<summary>
Was ist der Datenservice Öffentlicher Einkauf und aus welchen Komponenten besteht er?
</summary>

**[Redaktionssystem](https://resy.datenservice-oeffentlicher-einkauf.de/)**: Das Redaktionssystem ist ein Angebot für Vergabestellen und beispielsweise Dienstleister von öffentlichen Auftraggebern oder Zuwendungsempfängern, die kein elektronisches Vergabesystem nutzen.
Mit dem Redaktionssystem können Bekanntmachungen zu europaweiten Vergabeverfahren erfasst, bearbeitet, korrigiert und über den Vermittlungsdienst an TED versendet werden.
<br>
**[Vermittlungsdienst](https://ozg-vermittlungsdienst.de/)**: Der Vermittlungsdienst ist eine reine technische Schnittstelle zur Annahme, Validierung und Weiterleitung von Bekanntmachungen an TED und den Bekanntmachungsservice. Er bietet KEINE Oberfläche zum Erstellen von Bekanntmachungen! Es ist ausschließlich eine Maschine-zu-Maschine Kommunikation möglich, wie z.B. mit einer Vergabestellensoftware.
Diese Anbindung wird durch den Fachverfahrenshersteller durchgeführt.
<br>
**[Self-Service Portal](https://github.com/EFA-FHB/ozg-vermittlungsdienst-doku/blob/main/documentation/SSP.md)**: Das Self-Service-Portal (SSP) ist eine Web-Oberfläche für das Accountmanagement von Accounts des Vermittlungsdienstes. Primär genutzt wird es durch Fachverfahrenshersteller zur Ansicht der Statusinformationen von eingelieferten Bekanntmachungen in einem Dashboard.
<br>
**[Bekanntmachungsservice](https://oeffentlichevergabe.de/)**: Im Bekanntmachungsservice werden alle über den eSender-HUB versendeten EU-weiten und nationalen Bekanntmachungen veröffentlicht. Der Bekanntmachungsservice bietet eine Vielzahl an Recherchemöglichkeiten, damit Bietende ihrem Leistungsspektrum entsprechend zielgenau Bekanntmachungen finden können. Mit Nutzung des ELSTER-Unternehmenskontos stehen zudem weitere Komfortfunktionen wie Speicherung von Suchfunktionen und Benachrichtigungsservices zur Verfügung.
Des Weiteren können die Daten des Bekanntmachungsservice über eine Open Data Schnittstelle in den Formaten eForms-DE, CSV und OCDS nachgenutzt werden.
</details>
<br>

<details>
<summary>
Welche Vergabeplattformen sind an den Datenservice Öffentlicher Einkauf angebunden?
</summary>
Derzeit sind rund 87 Vergabeplattformen aus dem gesamten Bundesgebiet an den Datenservice Öffentlicher Einkauf (DÖE) angebunden. Über diese Anbindungen werden die Bekanntmachungen aus den verschiedenen regionalen und bundesweiten Vergabeplattformen zentral zusammengeführt und bereitgestellt.
</details>
<br>

<details>
<summary>
Was sind die Service- und Betriebszeiten (der Komponenten) des Datenservice Öffentlicher Einkauf?
</summary>
Die Produktiv- und Staging- (Test-)Umgebungen des Datenservice Öffentlicher Einkauf (DÖE) sind rund um die Uhr (24/7) verfügbar. Die Preview-Umgebung steht ebenfalls zu Testzwecken zur Verfügung, ist jedoch nur täglich von 6:00 bis 20:00 Uhr erreichbar.
</details>
<br>

<details>
<summary>
In welchem Zyklus werden Bekanntmachungen bei TED und im Bekanntmachungsservice veröffentlicht?
</summary>
Grundsätzlich werden alle übermittelten Bekanntmachungen ohne Verzögerung an TED bzw. den Bekanntmachungsservice zugestellt. EU-weite Bekanntmachungen müssen zunächst auf TED veröffentlicht werden. Erst nachdem TED die Veröffentlichung abgeschlossen und den Status „PUBLISHED“ zurückgemeldet hat, erfolgt die Weiterleitung dieser Bekanntmachungen an den Bekanntmachungsservice. Der Datenservice Öffentlicher Einkauf (DÖE) wartet dabei bis zu 48 Stunden auf die Veröffentlichung bei TED. Erfolgt innerhalb dieses Zeitraums keine Rückmeldung über die Publizierung, wird die Bekanntmachung dennoch an den Bekanntmachungsservice weitergeleitet. TED selbst unterliegt internen Veröffentlichungsregeln: Bekanntmachungen, die an einem Tag zugestellt und akzeptiert werden, erscheinen frühestens am folgenden Tag auf der Plattform. Eine Ausnahme bilden Wochenenden, da an Samstagen und Sonntagen üblicherweise keine Publizierungen erfolgen. In diesen Fällen werden die Bekanntmachungen am darauffolgenden Montag veröffentlicht. Eine weitere Ausnahme bilden sogenannte „lawfulness warnings“. In diesen Fällen behält sich TED vor, eine Bekanntmachung manuell zu prüfen, bevor sie veröffentlicht wird. Diese Prüfung kann bis zu fünf Tage in Anspruch nehmen.
</details>
<br>

### Kommunikationskanäle

<details>
<summary>
Wie kann das Team des Datenservice Öffentlicher Einkauf erreicht werden?
</summary>
Das Team ist über das folgende Kontaktformular zu erreichen.
<br>
[portal.ozg-vermittlungsdienst.de](https://portal.ozg-vermittlungsdienst.de/contact)
</details>
<br>


# Standard eForms-DE und SDK-DE

### Allgemeine Fragen -> Mehrsprachigkeit
<details>
<summary>
Gibt es Vorgaben zur Sprache der Bekanntmachung oder zur Mehrsprachigkeit?
</summary>
Es gibt zwar keine Aussage zur Wahl der Sprache von Ausschreibungen in der Vergabeordnung, jedoch ist nach § 23 Abs. 1 Verwaltungsverfahrensgesetz (VwVfG) die Amtssprache deutsch. Dementsprechend ist zu erwarten, dass deutsche Behörden ihre Unterlagen immer mindestens in deutscher Sprache ausfertigen müssen. Mehrsprachigkeit ist natürlich möglich und erlaubt. Für Veröffentlichende Entitäten, die nicht als Behörde klassifiziert werden, ist die Veröffentlichung auch ohne deutsche Sprache in Ordnung.
</details>
<br>
