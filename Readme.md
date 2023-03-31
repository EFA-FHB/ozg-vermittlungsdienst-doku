## EfA-Umsetzungsprojekt "Zugang zur öffentlichen Vergabe"
# Dokumentation Vermittlungsdienst
<br>

## Inhalte
- Einführung
- Aufgaben des Vermittlungsdienstes
- Datenservice Öffentlicher Einkauf Diagramm
- [Workflow](Workflow.md)
- [Verfügbare Systemumgebungen](Development_environments.md)
- [Anbindung an den Vermittlungsdienst](Connection_to_mediator.md)
- [Statusinformationen](Status_information.md)
- [eForms Unterstützung](eForms_support.md)
- [eForms Validator](Validator.md)
- [Releases](Releases.md)
<br><br>

## Einführung
Sie möchten Unternehmen und die öffentliche Verwaltung dabei unterstützen, bürokratische Hürden im Beschaffungsprozess abzubauen
und den Wettbewerb bei öffentlichen Aufträgen stärken? Dann binden Sie sich mit Ihrer Vergabeplattform gerne an den von der Freien
Hansestadt Bremen bereitgestellten Vermittlungsdienst an. Der Dienst ist Teil des Bremer EfA-Projektes „Zugang zur öffentlichen Vergabe“,
das im Projektkontext „Datenservice Öffentlicher Einkauf“ – einem Kooperationsprojekt des Bundes und Landes Bremen – umgesetzt wird.
Mit Hilfe des Vermittlungsdiensts können Vergabesysteme Bekanntmachungen an den Bekanntmachungsservice und TED übermitteln und so
bundesweite Ausschreiben für Unternehmen leicht zugänglich machen. Wie Sie sich anbinden können, erfahren Sie in dieser Dokumentation.
<br><br>

## Die Aufgaben des Vermittlungsdiensts auf einen Blick
- Validierung aller eingehenden Bekanntmachungen nach
Schema- sowie Schematron-Regeln und Prüfung, ob
Bekanntmachungen bereits im Bekanntmachungsservice
veröffentlicht wurden
- Übermittlung unterschwelliger Bekanntmachungen an
den Bekanntmachungsservice
- Übermittlung oberschwelliger Bekanntmachungen über
den eSender-Hub an TED und an den
Bekanntmachungsservice
<br><br>

## Datenservice Öffentlicher Einkauf Systemarchitektur
![Systemarchitektur](images/Infograf_eForms-Zusammenhaenge_2.jpg)
