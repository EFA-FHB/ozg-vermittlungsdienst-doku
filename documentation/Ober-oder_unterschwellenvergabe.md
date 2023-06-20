### EfA-Umsetzungsprojekt "Zugang zur öffentlichen Vergabe"
## Dokumentation Vermittlungsdienst
[Inhaltsverzeichnis](/documentation/documentation.md)
<br><br>

# Unterscheidung von Unter- und Oberschwellenvergabe

Bei der Verarbeitung einer Bekanntmachung im Vermittlungsdienst wird anhand bestimmter Kriterien geprüft, ob eine unterschwellige – oder eine oberschwellige Bekanntmachung übermittelt wurde.
<br><br>
Handelt es sich um eine unterschwellige Bekanntmachung, wird diese nach der Validierung direkt an den BKMS weitergeleitet. Eine Übermittlung der Bekanntmachung an TED wird nicht durchgeführt. Es erfolgt also eine Unterschwellenvergabe.
<br><br>
Eine oberschwellige Bekanntmachung wird innerhalb des Vermittlungsdienst an den eSender weitergeleitet. Dort wird anhand des eForms-DE Format ein für TED benötigtes eForms-EU Format der Bekanntmachung erzeugt. Nach erfolgreicher Validierung wird die Bekanntmachung an TED übermittelt und anschließend an das BKMS gesendet. Das heißt, die Bekanntmachung erfolgt über eine Oberschwellenvergabe.
<br><br>

## Kriterien zur Entscheidung
Das System entschiedet sich zwischen Unterschwellen- und Oberschwellenvergabe basierend auf den folgenden Kriterien:
1. Subtype der Bekanntmachung
2. eForms Version

Nur wenn beide Kriterien für die Oberschwellenvergabe erfüllt sind, wird dieser Prozess durchgeführt.
<br><br>

### Subtype der Bekanntmachung
Diese Information wird aus dem XML Feld SubTypeCode ausgelesen. Fängt der Subtype der Bekanntmachung mit "E" an (E1, E2, E3 & E4), handelt es sich um eine unterschwellige Bekanntmachung. Oberschwellige Bekanntmachungen haben ein Nummer 1-40 als Subtype.
<br><br>

### eForms Version
Diese Information wird aus dem XML Feld CustomizationID ausgelesen. TED akzeptiert nur bestimmte eForms-EU Versionen und der eSender des Vermittlungsdienst unterstützt ebenfalls nur bestimmte eForms-EU Versionen.
In der Produktionsumgebung muss ab 30.6. die eingelieferte Version eForms-DE 1.0 oder eine folgende eForms-DE Version sein. Eingereichte eForms-EU Versionen werden ab 30.6. nur noch für die Unterschwelle angenommen. Weitere Details zur Versionsunterstützung finden Sie hier: 


<br> 

*Unterstützte eForms Versionen **bis 25.10.2023**:*

| Version  | Mediator | External validator | Internal validator | eSender   | BKMS  | TED  |
| ------- | -------- | ------------------ | ------------------ | --------- | ----- | ---- |
| eForms-EU 0.1.1 | ja, aber nur für Unterschwellenvergabe | \-  | ja | \-  | ja, aber nur für Unterschwellenvergabe | nein    |
| eForms-EU 1.0   | ja, aber nur für Unterschwellenvergabe | \-  | ja | \-  | ja, aber nur für Unterschwellenvergabe | nein    |
| eforms-EU 1.5   | nein  | ja | ja | ja | \-  | nur akzeptiert  1.3 und folgenden Versionen bis Januar 2024  |
| eForms-DE 1.0.1 (schematron 0.5.0) | ja | ja | ja | ja | ja | ja, nach Umstellung in eForms-EU 1.5.1  |
| eForms-DE 1.1  | geplante Unterstützung bis Oktober 2023 | geplante Unterstützung bis Oktober 2023 | geplante Unterstützung bis Oktober 2023 | geplante Unterstützung bis Oktober 2023 | geplante Unterstützung bis Oktober 2023 | ja, nach Umstellung in eForms-EU 1.7.0<br><br>geplante Unterstützung bis Oktober 2023 |

<br>

*Unterstützte eForms Versionen **ab 25.10.2023** (Production Environment):*

| Version                               | Mediator                        | External validator | Internal validator | eSender    | BKMS      | TED       |
| ------------------------------------- | ------------------------------- | ------------------ | ------------------ | ---------- | --------- | ------------ |
| eForms-EU 0.1.1                       | ja, aber nur für Unterschwellenvergabe | \-                 | ja                | \-         | ja, aber nur für Unterschwellenvergabe | nein    |
| eForms-EU 1.0                         | ja, aber nur für Unterschwellenvergabe | \-                 | ja                | \-         | ja, aber nur für Unterschwellenvergabe | nein    |
| eforms-EU 1.5                         | nein                          | ja                | ja                | ja        | \-        | ja          |
| eForms-DE 1.0.1 (schematron 0.5.0)    | ja                            | ja                | ja                | ja        | ja       | ja, nach Umstellung in eForms-EU 1.5.1 |
| eforms-EU 1.7 (future implementation) | nein                          | ja                | ja                | geplante Unterstützung | \-   | ja  |
| eForms-DE 1.1 (recommended version)   | ja                            | ja                | ja                | ja                     | ja  | ja, nach Umstellung in eForms-EU 1.7.0 |


 Weitere Informationen zu Anbindung und Optionen zur Einlieferung finden Sie unter LINK ZU ANBINDUNGSLEITFADEN MIT OPTIONEN ZUM EINLIEFERN
