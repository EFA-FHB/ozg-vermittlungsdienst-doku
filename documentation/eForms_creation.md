### EfA-Umsetzungsprojekt "Zugang zur öffentlichen Vergabe"
## Dokumentation Vermittlungsdienst
[Inhaltsverzeichnis](/documentation/Documentation.md)
<br>

# Hinweise zum Erstellen von eForms-DE Dokumenten

Bei der eForms Dokumentenerstellung gilt es einige Regeln zu bestimmten Felden zu beachten.

## eSender-Informationen
>**eForms-DE spezifisch**

Feld: *ganzer Abschnitt ```<efac:Organization>```*

Der DöE übernimmt die Rolle des eSenders für alle an TED zu übermittelnden oberschwelligen Bekanntmachungen. Für die Organisationen darf deshalb der Typ "ted-esen" NICHT in den Bekanntmachungen verwendet werden, da diese Angabe automatisch vom eSender-Hub eingefügt wird.
Wenn Sie eine Bekanntmachung erstellen und eine Organisation angeben, müssen Sie für jede Organisation definieren, welche Rolle diese im Rahmen der Bekanntmachung spielt. Die Rollen sind definiert in der EU Codeliste: https://github.com/OP-TED/eForms-SDK/blob/1.7.0/codelists/organisation-role.gc
Ein Wert in der EU Codeliste ist "ted-esen". Dieser Wert darf in Deutschland nicht verwendet werden. 

Hierbei zu beachten: In den derzeit im Kosit Repository vorhandenen Beispieldateien zu eForms-DE 1.0 ist diese Rolle teilweise noch vorhanden. Mit Veröffentlichung der Version eForms-DE 1.1 werden auch die Beispieldateien entsprechend angepasst, sodass die Rolle ted-esen nicht mehr verwendet wird. 
<br>

## Zusammenhang zwischen Dispatch Date (BT-05) Preferred Publication Date (BT-738)

### Erläuterung der Felder:

BT-05 (Dispatch Date): <cbc:IssueDate> : Dieses Feld stellt den Versendungszeitpunkt der Bekanntmachung dar. Es wird empfohlen, dieses Datum automatisch bei Versendung durch das System setzen zu lassen. Bei Testdateien wir empfohlen, den Wert immer auf das aktuelle Datum zu setzen. Das Datum sollte nicht künstlich in die Vergangenheit gesetzt werden. 

BT-738 (Preferred Publication Date): <cbc:RequestedPublicationDate> : Dieses Feld dient zur expliziten Angabe, wann eine Bekanntmachung veröffentlicht werden soll


### Ausgangslage Regeln in EU und DE:

_eForms-EU 1.5_

- BT-05 (Dispatch Date) ist verpflichtend und BT-738 (Preferred Publication Date) ist optional (Regel BR-BT-00005-0150)
- Das BT-738 (Preferred Publication Date) darf maximal 92 Tage in der Zukunft liegen und muss nach dem BT-05 (Dispatch Date) liegen (Regel BR-BT-00738-0053)
- Wenn das BT-738 (Preferred Publication Date) nicht befüllt ist, wird eine Veröffentlichung "as soon as possible" durchgeführt

Quellen:
https://github.com/OP-TED/eForms-SDK/blob/1.5.1/schematrons/static/validation-stage-5.sch

_eForms-EU 1.7_

- BT-05 (Dispatch Date) ist verpflichtend und BT-738 (Preferred Publication Date) ist optional (Regel BR-BT-00005-0150)
- Das BT-738 (Preferred Publication Date) darf maximal 60 Tage in der Zukunft liegen und muss mindestens 2 Tage nach dem BT-05 (Dispatch Date) liegen (Regel BR-BT-00738-0053)
- Wenn das BT-738 (Preferred Publication Date) nicht befüllt ist, wird eine Veröffentlichung "as soon as possible" durchgeführt
- BT-05 (Dispatch Date) muss zwischen gestern und morgen liegen (Dynamische Regel)

Quellen:
https://github.com/OP-TED/eForms-SDK/blob/1.7.0/schematrons/static/validation-stage-5.sch
https://github.com/OP-TED/eForms-SDK/blob/1.7.0/schematrons/dynamic/validation-stage-6b.sch

_eForms-DE (1.0.1 & 1.1.0)_

- Alle statischen EU Regeln der jeweiligen Version greifen
- Das BT-738 (Preferred Publication Date) ist verpflichted

Quellen: https://xeinkauf.de/app/uploads/2023/03/specification-eforms-de-v1.0.1.pdf
https://xeinkauf.de/app/uploads/2023/08/specification-eforms-de-v1.1.0.pdf

### Derzeitige Problematik VOR Schematron Release 0.5.3 bzw. 0.6.1

Durch die Verpflichtung der Angabe des BT-738 (Preferred Publication Date) ist es in Kombination mit den geltenden EU-Regeln nicht möglich, eine Veröffentlichung bei TED "as soon as possible" durchführen zu lassen, da dies nur geschieht, wenn das Feld leer gelassen wird. Mit den geltenden Einschränkungen ist es nur zulässig, das BT-738 (Preferred Publication Date) mindestens einen Tag (eforms-DE 1.0.1) bzw. mindestens zwei Tage (eforms-DE 1.1.0) nach dem BT-05 (Dispatch Date) liegen muss. Somit ist eine Veröffentlichung bei TED "as soon as possible" nicht möglich.


### Lösung mit Schematron Release 0.5.3 bzw. 0.6.1

Die bestehenden EU Regel BR-BT-00005-0150 & BR-BT-00738-0053 zur Einschränkung des BT-738 (Preferred Publication Date) werden ausgesetzt und durch neue DE-Regeln ersetzt (SR-BT-738-1 and SR-BT-738-P60D). Dadurch werden folgende Eingaben zulässig:

_eForms-DE 1.0.1_
- Das BT-738 (Preferred Publication Date) darf am selben Tag liegen wie das BT-05 (Dispatch Date)
- Das BT-738 (Preferred Publication Date) darf einen Tag nach dem BT-05 (Dispatch Date) liegen
- Das BT-738 (Preferred Publication Date) darf 2-92 Tage nach dem BT-05 (Dispatch Date) liegen

_eForms-DE 1.1.0_

- Das BT-738 (Preferred Publication Date) darf am selben Tag liegen wie das BT-05 (Dispatch Date)
- Das BT-738 (Preferred Publication Date) darf einen Tag nach dem BT-05 (Dispatch Date) liegen
- Das BT-738 (Preferred Publication Date) darf 2-60 Tage nach dem BT-05 (Dispatch Date) liegen

WICHTIG: Wenn das BT-738 (Preferred Publication Date) weniger als 2 Tage nach dem BT-05 (Dispatch Date) liegt, dann wird das Feld BT-738 (Preferred Publication Date) im eSender-Hub entfernt, bevor an TED versendet wird. Damit wird ermöglicht, dass TED eine Veröffentlichung "as soon as possible" durchführt. So wird eine Kompatibilität mit den EU-Regeln sichergestellt.

### Umsetzung der Lösung

_Schematron-Regeln_

Die neuen Regeln zum Ersetzen der EU Regeln wurden bereits durch die KoSIT veröffentlicht:

Schematron release für eForms-DE 1.0.1:
https://projekte.kosit.org/eforms/eforms-de-schematron/-/releases/v0.5.3

Schematron release für eForms-DE 1.1.0
https://projekte.kosit.org/eforms/eforms-de-schematron/-/releases/v0.6.1


_Datenservice öffentlicher Einkauf_

Der DöE baut sowohl die neuen Schematron Regeln als auch die Umwandlung im eSender-Hub derzeit ein. Diese Änderungen werden mit dem nächsten Release in KW 41 in Produktion veröffentlicht und sind dann testbar (genauere Infos zum Release finden Sie [hier](https://github.com/EFA-FHB/ozg-vermittlungsdienst-doku/blob/main/Releases.md). 

_SDK-DE_

Die neuen Regeln wurde im SDK-DE 1.0.1 und 1.1.0 bereits eingebaut. 

## Erstellung von eForms in Verbindung mit im alten Vergabeformat bei TED eingereichten Bekanntmachungen
>**nicht eForms-DE spezifisch**

Für einen Übergangszeitraum kann es notwendig werden, Verlinkungen zwischen den im alten Vergabeformat bei TED eingereichten Bekanntmachungen und Bekanntmachungen, die im eForms-Format bei TED eingereicht werden, herzustellen. Mögliche Szenarien, die eine Verlinkung notwendig machen, sind:
- Ein Vergabeprozess wurde vor dem 25.10.2023 alten Format TED-XML begonnen und wird im Format eForms-DE fortgesetzt. Auf die im alten Format erstellen Dokumente muss in den Folgebekanntmachungen referenziert werden.
- Eine im alten Format veröffentlichte Bekanntmachung ist zu korrigieren oder anzupassen, sodass eine Change Notice mit Referenz auf diese Bekanntmachung notwendig ist.

TED hat für diese Referenzen im neuen eForms Format mehrere Felder vorgesehen, in denen eine solche Referenz verwendet werden kann. Für die Referenz wird aus dem alten Format die Notice Publication ID verwendet. Diese hat immer eine Struktur nnnnnnnn-yyyy, wobei die letzten vier Stellen eine Jahreszahl darstellen. Es gibt in eForms folgende spezifische Felder für bestimmte Referenzen: 

- Change Notice Version Identifier (BT-758)
- Modification Previous Notice Section Identifier (BT-1501)
- Previous Planning Identifier (BT-125)
- Framework Notice Identifier (OPT-100)

Wenn eines dieser Felder im eForms verwendet werden kann, sollten diese Referenzfelder mit der Notice Publication ID befüllt werden. Wenn keines dieser Felder in der speziellen Bekanntmachung verwendet werden kann, besteht zusätzlich die Möglichkeit folgendes Feld zu nutzen:
- Previous Notice (OPP-090)

Generell liegt es in der Verantwortung der versendenden Stelle, sicherzustellen, dass das korrekte Feld und die korrekte ID für die Referenz verwendet wird. Derzeit führt TED noch keine umfangreichen Prüfungen hierzu durch, will dies aber in der Zukunft einbauen. Der Datenservice öffentlicher Einkauf behandelt Bekanntmachungen mit Referenzen auf alte Bekanntmachungen wie jede andere Art von Bekanntmachungen. 

TED hat im Zusammenhang mit dieser Diskussion bestätigt, dass ein Wechsel des eSenders von einem FVH auf den DöE keine Auswirkungen haben wird. Es wird möglich sein, auf eine im alten Format eingereichte Bekanntmachung zu referenzieren, auch wenn diese von einem anderen eSender-Hub eingeliefert wurde. 

Weitere Details zur Verwendung der Referenzen können hier nachgelesen werden: https://docs.ted.europa.eu/eforms/latest/schema/procedure-lot-part-information.html#previousNoticeSection

Generell handelt es sich hierbei um eine Darstellung der derzeit uns bekannten Spezifikation durch TED. Diese kann sich jederzeit ändern. Daher empfehlen wir dringend, die Kommunikationskanäle von TED zu dieser Thematik zu verfolgen. 
