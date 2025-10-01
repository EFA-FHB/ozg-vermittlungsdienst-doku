### Datenservice Öffentlicher Einkauf
[Inhaltsverzeichnis](/documentation/documentation.md)
<br>

# Hinweise zum Erstellen von eForms-DE-Dokumenten

Bei der eForms-Dokumentenerstellung gilt es, einige Regeln zu bestimmten Feldern zu beachten.

## eSender-Informationen
>**eForms-DE-spezifisch**

Feld: *ganzer Abschnitt ```<efac:Organization>```*

Der Datenservice Öffentlicher Einkauf übernimmt die Rolle des eSenders für alle an TED zu übermittelnden oberschwelligen Bekanntmachungen. Für die Organisationen darf deshalb der Typ „ted-esen“ NICHT in den Bekanntmachungen verwendet werden, da diese Angabe automatisch vom eSender-Hub eingefügt wird.
Wenn eine Bekanntmachung erstellt und eine Organisation angegeben wird, muss für jede Organisation definiert werden, welche Rolle diese im Rahmen der Bekanntmachung spielt. Die Rollen sind definiert in der EU-Codeliste: https://github.com/OP-TED/eForms-SDK
Ein Wert in der EU-Codeliste ist „ted-esen“. Dieser Wert darf in Deutschland nicht verwendet werden. 
<br>

## Zusammenhang zwischen Dispatch Date (BT-05) und Preferred Publication Date (BT-738)

### Erläuterung der Felder:

BT-05 (Dispatch Date)  <cbc:IssueDate>: Dieses Feld stellt den Versendungszeitpunkt der Bekanntmachung dar. Es wird empfohlen, dieses Datum automatisch bei Versendung durch das System setzen zu lassen. Bei Testdateien wird empfohlen, den Wert immer auf das aktuelle Datum zu setzen. Das Datum sollte nicht künstlich in die Vergangenheit gesetzt werden. 

BT-738 (Preferred Publication Date) <cbc:RequestedPublicationDate>: Dieses Feld dient zur expliziten Angabe, wann eine Bekanntmachung veröffentlicht werden soll.


### Ausgangslage Regeln in EU und DE:

_eForms-EU 1.5_

- BT-05 (Dispatch Date) ist verpflichtend und BT-738 (Preferred Publication Date) ist optional (Regel BR-BT-00005-0150)
- Das BT-738 (Preferred Publication Date) darf maximal 92 Tage in der Zukunft liegen und muss nach dem BT-05 (Dispatch Date) liegen (Regel BR-BT-00738-0053)
- Wenn das BT-738 (Preferred Publication Date) nicht befüllt ist, wird eine Veröffentlichung „as soon as possible“ durchgeführt

Quellen:
https://github.com/OP-TED/eForms-SDK/blob/1.5.1/schematrons/static/validation-stage-5.sch

_eForms-EU 1.7_

- BT-05 (Dispatch Date) ist verpflichtend und BT-738 (Preferred Publication Date) ist optional (Regel BR-BT-00005-0150)
- Das BT-738 (Preferred Publication Date) darf maximal 60 Tage in der Zukunft liegen und muss mindestens 2 Tage nach dem BT-05 (Dispatch Date) liegen (Regel BR-BT-00738-0053)
- Wenn das BT-738 (Preferred Publication Date) nicht befüllt ist, wird eine Veröffentlichung „as soon as possible“ durchgeführt
- BT-05 (Dispatch Date) muss zwischen gestern und morgen liegen (Dynamische Regel)

Quellen:
https://github.com/OP-TED/eForms-SDK/blob/1.7.0/schematrons/static/validation-stage-5.sch
https://github.com/OP-TED/eForms-SDK/blob/1.7.0/schematrons/dynamic/validation-stage-6b.sch

_eForms-DE (1.0.1 & 1.1.0)_

- Alle statischen EU Regeln der jeweiligen Version greifen
- Das BT-738 (Preferred Publication Date) ist verpflichtend

Quellen: https://xeinkauf.de/app/uploads/2023/03/specification-eforms-de-v1.0.1.pdf
https://xeinkauf.de/app/uploads/2023/08/specification-eforms-de-v1.1.0.pdf
