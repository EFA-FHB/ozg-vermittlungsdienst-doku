### EfA-Umsetzungsprojekt "Zugang zur öffentlichen Vergabe"
## Dokumentation Vermittlungsdienst
[Inhaltsverzeichnis](/documentation/documentation.md)
<br>

# Status - und Transferinformationen

Mit Hilfe der REST API des Vermittlungsdienstes können alle Status- und Fehlerinformationen einer Bekanntmachung abgefragt werden. Die Status- und Fehlerinformationen des BKMS und von TED werden regelmäßig vom Vermittlungsdienst bzw. eSender-Hub abgefragt und gespeichert, so liegt jederzeit der Status und weitere Informationen zu einer Bekanntmachung zum weiteren Abruf bereit.
<br>

## Inhalte
- [Endpunkte zur Abfrage der Status- und Transferinformationen](#endpunkte)
- [Struktur der Statusinformationen](#info-struktur)
    - [Statustabelle: Übermittlung einer Bekanntmachung](#statustabelle-uebermittlung)
    - [Statustabelle: Oberschwellenvergabe](#statustabelle-oberschwelle)
    - [Statustabelle: Unterschwellenvergabe](#statustabelle-unterschwelle)
- [Struktur der Transferinformationen](#transfer-info)
- [Lawfullness Warnings](#lawfullness)


<br><br>

## Endpunkte zur Abfrage der Status- und Transferinformationen<span id="endpunkte">
Zur Abfrage der Status- und Transferinformationen stellt der Vermittlungsdienst die Endpunkte `GET /v1/notices` für eine Liste von Datenlieferungen, `GET /v1/notices/status` für eine Liste von Datenlieferungen in einem bestimmten Zeitraum und `GET /v1/notices/{trackingcode}` für eine einzelne Datenlieferung zur Verfügung.

Der Vermittlungsdienst führt die Statusabfragen an BKMS und TED alle drei Minuten durch. Daher ist eine Abfrage der Statusinformationen der Bekanntmachungen an den Vermittlungsdienst maximal alle 5 Minuten sinnvoll.

Die zugehörige OpenAPI-Spezifikation finden Sie unter https://ozg-vermittlungsdienst.de/ und steht Ihnen im JSON-Format zum Download unter https://ozg-vermittlungsdienst.de/Vermittlungsdienst_REST-API.json bereit.
<br><br>

## Struktur der Statusinformationen<span id="info-struktur">
Die Endpunkte zur Abfrage der Statusinformationen, geben die Statusinformationen für jede Bekanntmachung innerhalb des Delivery Schemas wie folgt zurück.

```
<?xml version="1.0" encoding="UTF-8"?>
<delivery>
	...
	<tedStatus>PENDING</tedStatus>
	<tedStatusUpdate>2023-04-26T14:32:52.625Z</tedStatusUpdate>
	<doeStatus>AWAITING_TRANSFER</doeStatus>
	<doeStatusUpdate>2023-04-26T14:32:52.625Z</doeStatusUpdate>
	<statusDescription>string</statusDescription>
	...
</delivery>
```

Die Statusinformationen enthalten sowohl bei unterschwelligen als auch bei oberschwelligen Bekanntmachungen den Status des Datenservice Öffentlicher Einkauf `doeStatus`, das letzte Änderungsdatum des DöE-Status `doeStatusUpdate` sowie eine Beschreibung des aktuell gesetzten Status `statusDescription`.

Bei oberschwelligen Bekanntmachungen wird zusätzlich der TED-Staus `tedStatus` mit dem letzten Änderungsdatum `tedStatusUpdate` übermittelt. Die TED-Statuswerte orientieren sich an den Statuswerten der EU. 
<br><br>


### Statustabelle: Übermittlung einer Bekanntmachung<span id="statustabelle-uebermittlung">

| DöE-Status        | Statusbeschreibung                                                                                       |
| ----------------- | --------------------------------------------------------------------------------------------------------- |
| AWAITING_TRANSFER | Die Bekanntmachung wurde vom Mediator angenommen und akzeptiert. Die weitere Versendung wird vorbereitet. |

Nachdem die Übermittlung einer Bekanntmachung erfolgriech abgeschlossen ist, wird der Status der Bekanntmachung auf AWAITING_TRANSFER gesetzt und der Vermittlungsdienst beginnt mit weiteren Schritten der Verarbeitung der Unter- oder Oberschwellenvergabe. In den folgenden Statustabellen werden die möglichen Status für die Verarbeitung der Unter- und Oberschwellenvergabe aufgelistet.
<br><br>

### Statustabelle: Oberschwellenvergabe<span id="statustabelle-oberschwelle">

Die folgenden Statuskombinationen, können bei der Statusabfrage eine Oberschwellenvergabe übermittelt werden.

| TED-Status        | DöE-Status     | Statusbeschreibung                                                                                                    |
| ----------------- | -------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| PENDING           | PENDING        | Die Bekanntmachung wurde vom eSender zur weiteren Verarbeitung angenommen. Die Übermittlung der Bekanntmachung an TED und an den Bekanntmachungsservice stehen noch aus. |
| NOT_SEND          | INTERNAL_ERROR | Ein interner Fehler ist aufgetreten. Ein entsprechendes Support-Ticket wird ggf. erstellt.                                                                               |
| PENDING           | PENDING        | Die Bekanntmachung wurde vom eSender zur weiteren Verarbeitung angenommen. Die Übermittlung der Bekanntmachung an TED und an den Bekanntmachungsservice stehen noch aus. |
| NO_RESPONSE       | PENDING        | Die Übermittlung an TED wird erneut versucht. Die Übermittlung der Bekanntmachung an den Bekanntmachungsservice steht noch aus.                                          |
| ACCEPTED          | PENDING        | Die Bekanntmachung wurde von TED akzeptiert, die Übermittlung an den Bekanntmachungsservice steht noch aus.                                                              |
| ACCEPTED          | ACCEPTED       | Die Bekanntmachung wurde von TED und dem Bekanntmachungsservice akzeptiert, aber noch nicht veröffentlicht.                                                              |
| ACCEPTED          | PUBLISHED      | Die Bekanntmachung wurde von TED akzeptiertt akzeptiert, aber noch nicht veröffentlicht. Die Bekanntmachung wurde bereits im Bekanntmachungsservice veröffentlicht.      |
| PUBLISHING        | PENDING        | Die Bekanntmachung wird in TED veröffentlicht, die Übermittlung an den Bekanntmachungsservice steht noch aus.                                                            |
| PUBLISHING        | ACCEPTED       | Die Bekanntmachung wird in TED veröffentlicht, die Bekanntmachung wurde vom Bekanntmachungsservice akzeptiert.                                                           |
| PUBLISHING        | PUBLISHED      | Die Bekanntmachung wird in TED veröffentlicht, die Bekanntmachung wurde im Bekanntmachungsservice veröffentlicht.                                                        |
| STOPPED           | NOT_SEND       | Die Bekanntmachung wurde in TED gestoppt und wird nicht zum Bekanntmachungsservice gesendet.                                                                             |
| STOPPED           | PENDING        | Die Bekanntmachung wurde in TED gestoppt und wird nicht zum Bekanntmachungsservice gesendet.                                                                             |
| STOPPED           | ACCEPTED       | Die Bekanntmachung wurde in TED gestoppt und wird in Kürze auch im Bekanntmachungsservice gestoppt werden.                                                               |
| STOPPED           | PUBLISHED      | Die Bekanntmachung wurde in TED gestoppt und wird in Kürze auch im Bekanntmachungsservice gestoppt werden.                                                               |
| STOPPED           | STOPPED        | Die Bekanntmachung wurde sowohl in TED als auch im Bekanntmachungsservice gestoppt.                                                                                      |
| PUBLISHED         | PENDING        | Die Bekanntmachung wurde in TED veröffentlicht, die Übermittlung an den Bekanntmachungsservice steht noch aus.                                                           |
| PUBLISHED         | ACCEPTED       | Die Bekanntmachung wurde in TED veröffentlicht und vom Bekanntmachungsservice akzeptiert, aber noch nicht veröffentlicht.                                                |
| PUBLISHED         | PUBLISHED      | Die Bekanntmachung wurde in TED und im Bekanntmachungsservice veröffentlicht.                                                                                            |
| MANUALLY_REJECTED | NOT_SEND       | Die Bekanntmachung wurde von TED auf Grund einer rechtlichen Prüfung manuell abgelehnt und wurde nicht zum Bekanntmachungsservice gesendet.                              |
| MANUALLY_REJECTED | PENDING        | Die Bekanntmachung wurde von TED auf Grund einer rechtlichen Prüfung manuell abgelehnt und wird in Kürze auch im Bekanntmachungsservice gestoppt.                        |
| MANUALLY_REJECTED | ACCEPTED       | Die Bekanntmachung wurde von TED auf Grund einer rechtlichen Prüfung manuell abgelehnt und wird in Kürze auch im Bekanntmachungsservice gestoppt.                        |
| MANUALLY_REJECTED | PUBLISHED      | Die Bekanntmachung wurde von TED auf Grund einer rechtlichen Prüfung manuell abgelehnt und wird in Kürze auch im Bekanntmachungsservice gestoppt.                        |
| MANUALLY_REJECTED | STOPPED        | Die Bekanntmachung wurde von TED auf Grund einer rechtlichen Prüfung manuell abgelehnt und wurde auch im Bekanntmachungsservice gestoppt.                                |
| REJECTED          | INTERNAL_ERROR | Ein interner Fehler ist aufgetreten. Ein entsprechendes Support-Ticket wird ggf. erstellt.                                                                               |

<br>

### Statustabelle: Unterschwellenvergabe<span id="statustabelle-unterschwelle">

Die folgenden Statuskombinationen, können bei der Statusabfrage eine Unterschwellenvergabe übermittelt werden.

| DöE status | Statusbeschreibung                                             |
| ---------- | --------------------------------------------------------------- |
| ACCEPTED   | Die Bekanntmachung wurde vom Bekanntmachungsservice akzeptiert. |
| REJECTED   | Die Bekanntmachung wurde von BKMS abgelehnt.                    |
| PROCESSING | Die Bekanntmachung wird vom BKMS verarbeitet.                   |
| PUBLISHED  | Die Bekanntmachung wurde im BKMS veröffentlicht.                |
| STOPPED    | Die Bekanntmachung wurde  im Bekanntmachungsservice gestoppt.   |



<br>

## Struktur der Transferinformationen<span id="transfer-info">
Die Transferinformationen sind ebenfalls für jede Bekanntmachung im Delivery Schema enthalten. Diese Informationen beinhalten Warnungen und Fehlermeldungen vom Vermittlungsdienst, dem Bekanntmachungsservice und TED.
```
<?xml version="1.0" encoding="UTF-8"?>
<delivery>
	...
	<transferResponse>
		<warnings>
			<warning>
				<source>BKMS</source>
				<description>string</description>
				<path>string</path>
				<rule>string</rule>
				<ruleContent>string</ruleContent>
			</warning>
		</warnings>
		<errors>
			<error>
				<source>BKMS</source>
				<description>string</description>
				<path>string</path>
				<rule>string</rule>
				<ruleContent>string</ruleContent>
			</error>
		</errors>
	</transferResponse>
	...
</delivery>
```

Innerhalb der Transferinformationen `transferResponse` werden Warnungen `warnings` von Fehlermeldungen `errors` getrennt aufgelistet. Pro Bekanntmachung ist es möglich mehrere Warnungen und Fehlermeldungen als Rückantwort zu erhalten. 

Eine einzelne Warnung und eine einzelne Fehlermeldung haben den selben Aufbau. `source` gibt an in welchem System die Warnung oder der Fehler entstand. Folgende Werte sind in `source` möglich:

| source         | Beschreibung                                                                                                                                                                                                                 |
| -------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| TED            | Fehler und Warnungen die von TED kommen, dies beinhaltet sowohl die http-Codes (5\*\*, 4\*\*) welche bei einer erfolglosen Übermittlung zurückgegeben werden, als auch Fehler und Warnungen aus dem TED-Validierungs Report. |
| BKMS           | Fehler, die von BKMS kommen, wenn BKMS einen http-Code zurückgibt, der eine erfolglose Übermittlung darstellt (5\*\*, 4\*\*).                                                                                                |
| PRE_VALIDATION | Fehler und Warnungen aus dem internen Validierungsdienst.                                                                                                                                                                    |

Die `description` enthält die Beschreibung der Warnung oder der Fehlermeldung. Im `path` wird die Position angegeben an der der Fehler oder die Warnung auftrat. Der Tag `rule` enthält die Bezeichnung der angewandten Regel und `ruleContent` die dazu tatsächlich angewandte Regel.

Warnungen und Fehlermeldungen vom Bekanntmachungsservice und von TED werden unverändert durchgereicht.
<br><br>

## Lawfullness Warnings<span id="lawfullness">
Zusätzlich zu Fehlern gibt es Warnungen. Diese kommen ausschießlich aus den EU Regeln und verhindern anders als Fehler nicht die Annahme der Bekanntmachung. TED hat derzeit nur eine Art von Warnungen definiert, sogenannte "Lawfullness Warnings". Diese werden höchstwahrscheinlich für deutsche Bekanntmachungen nahezu irrelevant sein, sind aber technisch möglich. 

Eine Lawfullness Warning bedeutet, dass eine manuelle Überprüfung einer Bekanntmachung bei TED notwendig ist. TED prüft dann den Inhalt der Bekanntmachung und entscheidet, ob diese veröffentlicht wird oder abgelehnt und nicht veröffentlicht wird. Für diese Entscheidung hat TED bis zu 5 Tage Zeit. Aus diesem Grund werden Bekanntmachungen mit einer Lawfullness Warning erst bei Veröffentlichung oder 5 Tage nach erfolgreicher Einlieferung bei TED an den BKMS weitergeleitet. 


