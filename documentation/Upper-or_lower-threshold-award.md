### Datenservice Öffentlicher Einkauf
[Inhaltsverzeichnis](/documentation/documentation.md)
<br>

# Unterscheidung von Vergaben unterhalb und oberhalb der EU-Schwellenwerte

Bei der Verarbeitung einer Bekanntmachung im Vermittlungsdienst wird anhand bestimmter Kriterien geprüft, ob eine Bekanntmachung oberhalb oder unterhalb der EU-Schwellenwerte übermittelt wurde.
<br><br>
Handelt es sich um eine Bekanntmachung unterhalb der EU-Schwellenwerte, wird diese nach der Validierung direkt an den Bekanntmachungsservice weitergeleitet. Eine Übermittlung der Bekanntmachung an TED wird nicht durchgeführt. 
<br><br>
Eine Bekanntmachung oberhalb der EU-Schwellenwerte wird vom Vermittlungsdienst an den eSender-Hub weitergeleitet. Dort wird das eingelieferte Format eForms-DE in das für TED benötigte eForms-EU-Format umgewandelt. Nach erfolgreicher Validierung wird die Bekanntmachung an TED übermittelt und anschließend unter Einhaltung rechtlicher Vorgaben (z. B. 48-Stunden-Frist) an den Bekanntmachungsservice gesendet.
<br>

## Kriterien für die Unterscheidung
Das System entscheidet zwischen Bekanntmachungen oberhalb und unterhalb der EU-Schwellenwerte basierend auf den folgenden Kriterien:
1. Subtype der Bekanntmachung
2. eForms-Version

Nur wenn beide Kriterien für Bekanntmachungen oberhalb der EU-Schwellenwerte erfüllt sind, wird diese durchgeführt.
<br>

### Subtype der Bekanntmachung
Diese Information wird aus dem XML-Feld `SubTypeCode` ausgelesen. Fängt der Subtype der Bekanntmachung mit „E" an (z. B. E3), handelt es sich um eine Bekanntmachung unterhalb der EU-Schwellenwerte. Bekanntmachungen oberhalb der EU-Schwellenwerte haben eine Nummer von 1 bis 40 als Subtype.
<br>

### eForms-Version
Diese Information wird aus dem XML-Feld `CustomizationID` ausgelesen. TED akzeptiert nur bestimmte eForms-EU-Versionen und nur bestimmte eForms-Versionen können vom eSender-Hub verarbeitet werden. Weitere Details zur Versionsunterstützung sind hier dokumentiert: [eForms Versionsunterstützung](/documentation/eForms_support.md).