### EfA-Umsetzungsprojekt "Zugang zur öffentlichen Vergabe"
## Dokumentation Vermittlungsdienst
[Inhaltsverzeichnis](/documentation/documentation.md)
<br>

# Unterscheidung von Unter- und Oberschwellenvergabe

Bei der Verarbeitung einer Bekanntmachung im Vermittlungsdienst wird anhand bestimmter Kriterien geprüft, ob eine unterschwellige oder oberschwellige Bekanntmachung übermittelt wurde.
<br><br>
Handelt es sich um eine unterschwellige Bekanntmachung, wird diese nach der Validierung direkt an den BKMS weitergeleitet. Eine Übermittlung der Bekanntmachung an TED wird nicht durchgeführt. 
<br><br>
Eine oberschwellige Bekanntmachung wird vom Vermittlungsdienst an den eSender-Hub weitergeleitet. Dort wird das eigelieferte Format in ein für TED benötigtes eForms-EU Format der Bekanntmachung umgewandelt. Nach erfolgreicher Validierung wird die Bekanntmachung an TED übermittelt und anschließend unter Einhaltung rechtlicher Vorgaben (z.B. 48h-Frist) an den BKMS gesendet. 
<br>

## Kriterien zur Entscheidung
Das System entschiedet zwischen Unterschwellen- und Oberschwellenvergabe basierend auf den folgenden Kriterien:
1. Subtype der Bekanntmachung
2. eForms Version

Nur wenn beide Kriterien für die Oberschwellenvergabe erfüllt sind, wird diese durchgeführt.
<br>

### Subtype der Bekanntmachung
Diese Information wird aus dem XML Feld `SubTypeCode` ausgelesen. Fängt der Subtype der Bekanntmachung mit "E" an (z.B. E3), handelt es sich um eine unterschwellige Bekanntmachung. Oberschwellige Bekanntmachungen haben ein Nummer 1-40 als Subtype.
<br>

### eForms Version
Diese Information wird aus dem XML Feld `CustomizationID` ausgelesen. TED akzeptiert nur bestimmte eForms-EU Versionen und nur bestimmte eForms Versionen können vom eSender-Hub verarbeitet werden.
Weitere Details zur Versionsunterstützung finden Sie hier: [eForms Versionsunterstützung](/documentation/eForms_Unterstuetzte-Versionen.md)