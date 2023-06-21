### EfA-Umsetzungsprojekt "Zugang zur öffentlichen Vergabe"
## Dokumentation Vermittlungsdienst
[Inhaltsverzeichnis](/documentation/documentation.md)
<br><br>

# eForms Dokumentenerstellung

Bei der eForms Dokumentenerstellung gilt es einige Regeln zu bestimmten Felden zu beachten.

## eSender-Informationen:

Feld: BT - 

XML: <...>

Der DöE übernimmt die Rolle des eSenders für alle an TED zu übermittelnden Bekanntmachungen. Für die Organisationen sollte deshalb der Typ "ted-esen" nichts in den Bekanntmachung verwendet werden, da diese Angabe automatisch vom eSender eingefügt wird. 

Zu beachten: dieses Feld wurde in vorherigen (v1.0) Beispielen vorhanden, nicht aber in den neuen Beispielen.
<br>

## Datumsangaben

BT-05: ``` <cbc:IssueDate> ```

BT-738:``` <cbc:RequestedPublicationDate>```

- Dispatch Date (BT-05, Tag der Absendung der Bekanntmachungen) muss mindestens zwei Tage bevor und maximal ein Tag nach der heutigen Tag sein. Wenn heute zum Beispiel der 05.06.2023 ist, könnte dieses Datum entweder 03.06.2023, 04.06.2023, 05.06.2023 oder 06.06.2023 sein. Das heißt, das Datum weist genau aus, wenn das Formular geschickt wurde.
- Bevorzugtes Veröffentlichungsdatum (Requested Publication Date, BT-738) muss mindestens zwei Tage nach dem Dispatch Date liegen. Der Vorteil am verpflichtenden Abstand nach dem Tag der Absendung liegt dabei, es gibt immer mindestens zwei Tage Zeitraum, bei Bedarf die Bekanntmachung noch vor Veröffentlichung zu stoppen und zu korrigieren (siehe Stop Funktion).
- Bevorzugtes Veröffentlichungsdatum muss maximal 60 Tage nach dem Dispatch Date liegen. Das heißt, ein potenzielles Problem mit Bekanntmachungen, die Monate im Voraus geschickt werden und deswegen nicht mehr aktuell sein, wird vermeidet.

#### Beispiele von validen Kombinationen von Daten:

- Heute: 05.06.2023 <br>
Dispatch Date: 04.06.2023<br>
Requested Publication Date: 10.06.2023<br>
- Heute: 05.06.2023<br>
Dispatch Date: 06.06.2023<br>
Requested Publication Date: 04.08.2023
<br><br>

## Erstellung von eForms in Verbindung mit im alten Vergabeformat bei TED eingereichten Bekanntmachungen

Es besteht die Möglichkeit, dass ein Vergabeprozess vor dem 25.10.2023 noch im alten Format TED-XML begonnen wird. Wenn beispielsweise eine PIN oder eine CN im alten Format begonnen wurde, kann es notwendig werden, diese Bekanntmachung in einer Folgebekanntmachung (zum Beispiel in einer CN/CAN) zu referenzieren. Außerdem kann es notwendig sein, dass eine über das alte Format veröffentlichte Bekanntmachung zu korrigieren oder anzupassen, sodass eine Change Notice mit Referenz auf diese Bekanntmachung notwendig ist. 

TED hat für diese Referenzen im neuen eForms Format mehrere Felder vorgesehen, in denen eine solche Referenz verwendet werden kann. Für die Referenz wird aus dem alten Format die Notice Publication ID verwendet. Diese hat immer eine Struktur nnnnnnnn-yyyy, wobei die letzten vier Stellen eine Jahreszahl darstellen. Es gibt in eForms folgende spezifische Felder für bestimmte Referenzen: 

- Change Notice Version Identifier (BT-758)
- Modification Previous Notice Section Identifier (BT-1501)
- Previous Planning Identifier (BT-125)
- Framework Notice Identifier (OPT-100)

Wenn eines dieser Felder im eForms verwendet werden kann, sollten diese Referenzfelder mit der Notice Publication ID befüllt werden. Wenn keines dieser Felder in der speziellen Bekanntmachung verwendet werden kann, besteht zusätzlich die Möglichkeit folgendes Feld zu nutzen:
- Previous Notice (OPP-090)

Generell liegt es in der Verantwortung der versendenden Stelle, sicherzustellen, dass das korrekte Feld und die korrekte ID für die Referenz verwendet wird. Derzeit führt TED noch keine umfangreichen Prüfungen hierzu durch, will dies aber in der Zukunft einbauen. Der Datenservice öffentlicher Einkauf behandelt Bekanntmachungen mit Referenzen auf alte Bekanntmachungen wie jede andere Art von Bekanntmachungen. 

TED hat im Zusammenhang mit dieser Diskussion bestätigt, dass ein Wechsel des eSenders von einem FVH auf den DöE keine Auswirkungen haben wird. Es wird möglich sein, auf eine im alten Format eingereichte Bekanntmachung zu referenzieren, auch wenn diese von einem anderen eSender eingeliefert wurde. 

Weitere Details zur Verwendung der Referenzen können hier nachgelesen werden: https://docs.ted.europa.eu/eforms/latest/schema/procedure-lot-part-information.html#previousNoticeSection

Generell handelt es sich hierbei um eine Darstellung der derzeit uns bekannten Spezifikation durch TED. Diese kann sich jederzeit ändern. Daher empfehlen wir dringend, die Kommunikationskanäle von TED zu dieser Thematik zu verfolgen. 