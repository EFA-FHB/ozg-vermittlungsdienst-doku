### EfA-Umsetzungsprojekt "Zugang zur öffentlichen Vergabe"
## Dokumentation Vermittlungsdienst
[Inhaltsverzeichnis](/documentation/documentation.md)
<br>

# eForms Dokumentenerstellung

Bei der eForms Dokumentenerstellung gilt es einige Regeln zu bestimmten Felden zu beachten.

### eSender-Informationen:

Feld: *ganzer Abschnitt ``` <efac:Organization>```*

Der DöE übernimmt die Rolle des eSenders für alle an TED zu übermittelnden oberschwelligen Bekanntmachungen. Für die Organisationen sollte deshalb der Typ "ted-esen" nicht in den Bekanntmachungen verwendet werden, da diese Angabe automatisch vom eSender eingefügt wird. 

Hierbei zu beachten: In den derzeit im Kosit Repository vorhandenen Beispieldateien zu eForms-DE 1.0 ist diese Rolle teilweise noch vorhanden. Mit Veröffentlichung der Version eForms-DE 1.1 werden auch die Beispieldateien entsprechend angepasst, sodass die Rolle ted-esen nicht mehr verwendet wird. 
<br>

### Datumsangaben

Betroffene Felder: *BT-05: ``` <cbc:IssueDate> ```* , *BT-738: ``` <cbc:RequestedPublicationDate>```*

- Der *Tag der Absendung der Bekanntmachungen* (Dispatch Date - BT-05) muss mindestens zwei Tage bevor und maximal einen Tag nach dem heutigen Tag liegen. Wenn heute zum Beispiel der 05.06.2023 ist, muss das Dispatch Date entweder 03.06.2023, 04.06.2023, 05.06.2023 oder 06.06.2023 sein. 
- Das *Bevorzugte Veröffentlichungsdatum* (Requested Publication Date - BT-738) muss mindestens zwei Tage nach dem Tag der Absendung der Bekanntmachung liegen. Dadurch wird ermöglicht, dass eine Bekanntmachung innerhalb der ersten 48h nach Versenden noch zurückgezogen und korrigiert werden kann, bevor die Veröffentlichung erfolgt. Hierfür wurde eine neue Stop-Funktion im Vermittlungsdienst geschaffen. Weitere Details dazu finden Sie hier:  [Change Notices/Updates & STOP Publication-Funktionalität](/documentation/STOP%20update%20%26%20change%20notices.md). 
Das Bevorzugte Veröffentlichungsdatum darf maximal 60 Tage nach dem Dispatch Date liegen. Damit wird die Aktualität einer Bekanntmachung zum Zeitpunkt der Veröffentlichung Gewährleistet.

#### Beispiele von validen Kombinationen von Datumsangaben:

- Heute: 05.06.2023 <br>
Dispatch Date: 04.06.2023<br>
Requested Publication Date: 07.06.2023<br>
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
