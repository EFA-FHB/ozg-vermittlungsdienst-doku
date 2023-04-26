### EfA-Umsetzungsprojekt "Zugang zur öffentlichen Vergabe"
## Dokumentation Vermittlungsdienst
[Startseite](/documentation/documentation.md)
<br><br>

# Statusinformationen

Der Status und weitere Informationen zu aufgetretenen Fehlern oder Warnungen zu einer Bekanntmachung können jederzeit über einen Request an den Mediator abgefragt werden. Da der Mediator regelmäßig sämtliche Statusänderungen zu oberschwelligen Bekanntmachungen vom eSender abfragt, liegt auch im Mediator immer der aktuelle Status einer Bekanntmachung vor, egal ob unterschwellig oder oberschwellig. Ebenso werden eventuelle Fehler von TED oder BKMS gespeichert und an den Mediator weitergegeben.
<br><br>
Bezüglich der Statusabfrage ist zu beachten, dass für eu-weite Bekanntmachungen immer zwei Statuswerte für jede Bekanntmachung existieren: Der Status der internen Prozessierung im Datenservice öffentlicher Einkauf (DöE-Status) und der Status in TED (TED-Status). Die TED Statuswerte orientieren sich an den Statuswerten der EU. 
<br><br>

## Status nationale Bekanntmachungen

Die folgenden Statuswerte existieren für unterschwellige Bekanntmachungen: 

**Anmerkung:** Die in kursiv formatierten Statuseinträge sind im eSender Release vom 31.3.2023 noch nicht testbar, da vom BKMS noch nicht zwischen ACCEPTED und PUBLISHED unterschieden wird.

| DöE Status        | Beschreibung                                                                                                   |
| ----------------- | -------------------------------------------------------------------------------------------------------------- |
| AWAITING_TRANSFER | Die Bekanntmachung wurde vom Mediator angenommen und akzeptiert. Nun wird die Versendung zum BKMS vorbereitet. |
| PROCESSING        | Die Bekanntmachung wird vom BKMS verarbeitet.                                                                  |
| ACCEPTED          | Die Bekanntmachung wurde vom Bekanntmachungsservice akzeptiert.                                                |
| REJECTED          | Die Bekanntmachung wurde von BKMS abgelehnt.                                                                   |
| ⚠️*PUBLISHED*   | *Die Bekanntmachung wurde im BKMS veröffentlicht.*                                                             |

**Anmerkung:** Die in rot markierten Statuskombinationen sind im eSender Preview Release am 31.3.2023 noch nicht testbar, da der BKMS noch nicht zwischen ACCEPTED und PUBLISHED unterscheidet. 

![national notices diagramm](images/natinal_notices_diagramm.png)
<br><br>

## Status oberschwellige Bekanntmachungen
Die folgenden Statuswerte existieren für oberschwellige Bekanntmachungen: 

**Anmerkung:** Die in kursiv formatierten Statuskombinationen sind im eSender Preview Release am 31.3.2023 noch nicht testbar, da Bekanntmachungen in eForms-DE 1.0.0 noch nicht vom BKMS angenommen werden.

| TED status (tedStatus)  | Datenservice Öffentlicher Einkauf Status (doeStatus) | Beschreibung                                                                                                                                                             |
| ----------------------- | ---------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| PENDING                 | AWAITING_TRANSFER                                     | Der Vermittlungsdienst hat die Bekanntmachung angenommen und verarbeitet sie in Kürze.                                                                                   |
| PENDING                 | PROCESSING                                           | Der Vermittlungsdienst verarbeitet die Bekanntmachung.                                                                                                                   |
| PENDING                 | PENDING                                              | Die Bekanntmachung wurde vom eSender zur weiteren Verarbeitung angenommen. Die Übermittlung der Bekanntmachung an TED und an den Bekanntmachungsservice stehen noch aus. |
| NO_RESPONSE             | PENDING                                              | Die Übermittlung an TED wird erneut versucht. Die Übermittlung der Bekanntmachung an den Bekanntmachungsservice steht noch aus.                                          |
| NOT_SEND                | INTERNAL_ERROR                                        | Ein interner Fehler ist aufgetreten. Ein entsprechendes Support-Ticket wird ggf. erstellt.                                                                               |
| REJECTED                | INTERNAL_ERROR                                        | Ein interner Fehler ist aufgetreten. Ein entsprechendes Support-Ticket wird ggf. erstellt.                                                                               |
| STOPPED                 | NOT_SEND                                             | Die Bekanntmachung wurde in TED gestoppt und wird nicht zum Bekanntmachungsservice gesendet.                                                                             |
| ⚠️*STOPPED*           | ⚠️*ACCEPTED/ PUBLISHED/ NO_RESPONSE*                | *Die Bekanntmachung wurde in TED gestoppt und wird in Kürze auch im Bekanntmachungsservice gestoppt werden.*                                                             |
| ⚠️*STOPPED*           | ⚠️*STOPPED*                                        | *Die Bekanntmachung wurde sowohl in TED als auch im Bekanntmachungsservice gestoppt.*                                                                                    |
| ACCEPTED                | PENDING                                              | Die Bekanntmachung wurde von TED akzeptiert, die Übermittlung an den Bekanntmachungsservice steht noch aus.                                                              |
| ACCEPTED                | NO_RESPONSE                                           | Die Bekanntmachung wurde von TED akzeptiert, aber noch nicht veröffentlicht. Die Übermittlung an den Bekanntmachungsservice wird erneut versucht.                        |
| ⚠️*ACCEPTED*          | ⚠️*ACCEPTED*                                       | *Die Bekanntmachung wurde von TED und dem Bekanntmachungsservice akzeptiert, aber noch nicht veröffentlicht.*                                                            |
| ⚠️*ACCEPTED*          | ⚠️*PUBLISHED*                                      | *Die Bekanntmachung wurde von TED akzeptiertt, aber noch nicht veröffentlicht. Die Bekanntmachung wurde bereits im Bekanntmachungsservice veröffentlicht.*               |
| PUBLISHED               | PENDING                                              | Die Bekanntmachung wurde in TED veröffentlicht, die Übermittlung an den Bekanntmachungsservice steht noch aus.                                                           |
| PUBLISHED               | NO_RESPONSE                                           | Die Bekanntmachung wurde in TED veröffentlicht, die Übermittlung an den Bekanntmachungsservice wird erneut versucht.                                                     |
| ⚠️*PUBLISHED*         | ⚠️*ACCEPTED*                                       | *Die Bekanntmachung wurde in TED veröffentlicht und vom Bekanntmachungsservice akzeptiert, aber noch nicht veröffentlicht.*                                              |
| ⚠️*PUBLISHED*         | ⚠️*PUBLISHED*                                      | *Die Bekanntmachung wurde in TED und im Bekanntmachungsservice veröffentlicht.*                                                                                          |
| MANUALLY_REJECTED       | NOT_SEND                                             | Die Bekanntmachung wurde von TED auf Grund einer rechtlichen Prüfung manuell abgelehnt und wurde nicht zum Bekanntmachungsservice gesendet.                              |
| ⚠️*MANUALLY_REJECTED* | ⚠️*ACCEPTED/ PUBLISHED/ NO_RESPONSE*                | *Die Bekanntmachung wurde von TED auf Grund einer rechtlichen Prüfung manuell abgelehnt und wird in Kürze auch im Bekanntmachungsservice gestoppt.*                      |
| ⚠️*MANUALLY_REJECTED* | ⚠️*STOPPED*                                        | Die Bekanntmachung wurde von TED auf Grund einer rechtlichen Prüfung manuell abgelehnt und wurde auch im Bekanntmachungsservice gestoppt.*                               |


**Anmerkung:** Die in rot markierten Statuskombinationen sind im eSender Preview Release am 31.3.2023 noch nicht testbar, da der BKMS eForms-DE 1.0.0 und das Stoppen von Bekannmachungen noch nicht unterstützt.

![eu-wide notices diagramm](images/eu-wide_notices_diagramm.png)

