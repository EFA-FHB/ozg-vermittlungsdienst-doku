
# Datenservice Öffentlicher Einkauf

<details>
<summary>
Was ist der Datenservice Öffentlicher Einkauf und aus welchen Komponenten besteht er?
</summary>

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
Wie viele Vergabeplattformen sind an den Datenservice Öffentlicher Einkauf angebunden?
</summary>
Derzeit sind rund 92 (Stand 2025) Vergabeplattformen an den Datenservice Öffentlicher Einkauf angebunden.
</details>
<br>

<details>
<summary>
Was sind die Service- und Betriebszeiten des Datenservice Öffentlicher Einkauf?
</summary>
Die Produktiv- und Staging- (Test-)Umgebungen des Datenservice Öffentlicher Einkauf sind rund um die Uhr (24/7) verfügbar. Die Preview-Umgebung steht ebenfalls zu Testzwecken zur Verfügung, ist jedoch nur täglich von 6:00 bis 20:00 Uhr erreichbar.
</details>
<br>

<details>
<summary>
In welchem Zyklus werden Bekanntmachungen bei TED und im Bekanntmachungsservice veröffentlicht?
</summary>
Grundsätzlich werden alle übermittelten Bekanntmachungen ohne Verzögerung an TED bzw. den Bekanntmachungsservice zugestellt. EU-weite Bekanntmachungen müssen zunächst auf TED veröffentlicht werden. Erst nachdem TED die Veröffentlichung abgeschlossen und den Status „PUBLISHED“ zurückgemeldet hat, erfolgt die Weiterleitung dieser Bekanntmachungen an den Bekanntmachungsservice. Der Datenservice Öffentlicher Einkauf wartet dabei bis zu 48 Stunden auf die Veröffentlichung bei TED. Erfolgt innerhalb dieses Zeitraums keine Rückmeldung über die Publizierung, wird die Bekanntmachung dennoch an den Bekanntmachungsservice weitergeleitet. TED selbst unterliegt internen Veröffentlichungsregeln: Bekanntmachungen, die an einem Tag zugestellt und akzeptiert werden, erscheinen frühestens am folgenden Tag auf der Plattform. Eine Ausnahme bilden Wochenenden, da an Samstagen und Sonntagen üblicherweise keine Publizierungen erfolgen. In diesen Fällen werden die Bekanntmachungen am darauffolgenden Montag veröffentlicht. Eine weitere Ausnahme bilden sogenannte [„lawfulness warnings“](https://info.preview.datenservice-oeffentlicher-einkauf.de/documentation/Status_information#lawfulness). In diesen Fällen behält sich TED vor, eine Bekanntmachung manuell zu prüfen, bevor sie veröffentlicht wird. Diese Prüfung kann bis zu fünf Tage in Anspruch nehmen.
</details>
<br>

<details>
<summary>
Wie kann das Team des Datenservice Öffentlicher Einkauf erreicht werden?
</summary>

Das Team ist über das folgende [Kontaktformular](https://self-service.datenservice-oeffentlicher-einkauf.de/contact) zu erreichen.
</details>
<br>
