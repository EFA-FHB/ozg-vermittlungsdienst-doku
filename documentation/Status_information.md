### Datenservice Öffentlicher Einkauf
[Inhaltsverzeichnis](/documentation/documentation.md)
<br>

# Status - und Transferinformationen

Mit Hilfe der REST-API des Vermittlungsdienstes können alle Status- und Fehlerinformationen einer Bekanntmachung abgefragt werden. Die Status- und Fehlerinformationen des BKMS und von TED werden regelmäßig vom Vermittlungsdienst bzw. eSender-Hub abgefragt und gespeichert, so liegen jederzeit der Status und weitere Informationen zu einer Bekanntmachung zum weiteren Abruf bereit.
<br>

## Inhalte
- [Endpunkte zur Abfrage der Status- und Transferinformationen](#endpunkte)
- [Struktur der Statusinformationen](#info-struktur)
    - [Statustabelle: Übermittlung einer Bekanntmachung](#statustabelle-uebermittlung)
    - [Statustabelle: Oberschwellenvergabe](#statustabelle-oberschwelle)
    - [Statustabelle: Unterschwellenvergabe](#statustabelle-unterschwelle)
- [Struktur der Transferinformationen](#transfer-info)
- [Lawfulness Warnings](#lawfulness)


<br><br>

## Endpunkte zur Abfrage der Status- und Transferinformationen<span id="endpunkte">
Zur Abfrage der Status- und Transferinformationen stellt der Vermittlungsdienst die Endpunkte `GET /v1/notices` für eine Liste von Datenlieferungen, `GET /v1/notices/status` für eine Liste von Datenlieferungen in einem bestimmten Zeitraum und `GET /v1/notices/{trackingcode}` sowie `GET /v1/notices/by-notice/{noticeId}/{version}` für eine einzelne Datenlieferung zur Verfügung.

Der Vermittlungsdienst führt die Statusabfragen an den Bekanntmachungsservice und an TED alle drei Minuten durch. Daher ist eine Abfrage der Statusinformationen der Bekanntmachungen an den Vermittlungsdienst maximal alle fünf Minuten sinnvoll.

Die zugehörige OpenAPI-Spezifikation ist hier https://ozg-vermittlungsdienst.de/  zu finden und steht im JSON-Format zum Download unter https://ozg-vermittlungsdienst.de/Vermittlungsdienst_REST-API.json bereit.
<br><br>

## Struktur der Statusinformationen<span id="info-struktur">
Die Endpunkte zur Abfrage der Statusinformationen geben die Statusinformationen für jede Bekanntmachung innerhalb des Delivery-Schemas wie folgt zurück.

```
<?xml version="1.0" encoding="UTF-8"?>
<deliveries start="0" max="100" total="1234">
	<delivery>
		<noticeId>3fa85f64-5717-4562-b3fc-2c963f66afa6</noticeId>
		<noticeType>CN</noticeType>
		<trackingCode>3446e1ee-5917-4d31-b623-81ddfb038d82</trackingCode>
		<vergabeId>string</vergabeId>
		<vergabenummer>V0505/2021</vergabenummer>
		<description>string</description>
		<tedPublicationLink>https://preview.ted.europa.eu/udl?uri=TED:NOTICE:{publicationId}:HTML:DE:HTML</tedPublicationLink>
    		<bkmsPublicationLink>https://alpha.oeffentlichevergabe.de/ui/de/search/details?{noticeId}</bkmsPublicationLink>
		<tedStatus>PENDING</tedStatus>
		<tedStatusUpdate>2023-11-03T15:01:38.373Z</tedStatusUpdate>
		<tedAcceptedTimestamp>2023-11-03T15:01:38.373Z</tedAcceptedTimestamp>
		<tedPublishedTimestamp>2023-11-03T15:01:38.373Z</tedPublishedTimestamp>
		<tedPublicationId>string</tedPublicationId>
		<doeStatus>AWAITING_TRANSFER</doeStatus>
		<doeStatusUpdate>2023-11-03T15:01:38.373Z</doeStatusUpdate>
		<statusDescription>string</statusDescription>
		<transferResponse>
			<warnings>
				<warning>
					<source>TED</source>
					<description>The value of BT-701-notice must match the &apos;ProcedureOrNoticeID&apos; pattern</description>
					<path>/can:ContractAwardNotice/cbc:ID</path>
					<rule>BR-BT-00701-0052</rule>
					<ruleContent>matches(normalize-space(.),&apos;^[a-f0-9]{8}-[a-f0-9]{4}-4[a-f0-9]{3}-[89ab][a-f0-9]{3}-[a-f0-9]{12}$&apos;)</ruleContent>
				</warning>
			</warnings>
			<errors>
				<error>
					<source>TED</source>
					<description>The value of BT-701-notice must match the &apos;ProcedureOrNoticeID&apos; pattern</description>
					<path>/can:ContractAwardNotice/cbc:ID</path>
					<rule>BR-BT-00701-0052</rule>
					<ruleContent>matches(normalize-space(.),&apos;^[a-f0-9]{8}-[a-f0-9]{4}-4[a-f0-9]{3}-[89ab][a-f0-9]{3}-[a-f0-9]{12}$&apos;)</ruleContent>
				</error>
			</errors>
		</transferResponse>
		<validation>
			<validatedEformsVersion>eforms-sdk-1.0.0</validatedEformsVersion>
			<description>Ergebnisreport der Validierung der Datenlieferung durch den Vermittlungsdienst</description>
			<warnings>
				<warning>
					<rule>rule|text|BR-BT-00506-0052</rule>
					<ruleContent>matches(normalize-space(.),&apos;^[a-zA-Z0-9][a-zA-Z0-9._%+-]*@(?:[a-zA-Z0-9-]+\.)+[a-zA-Z]{2,63}$&apos;)</ruleContent>
					<description>The value of BT-506-Organization-Company must match the &apos;Email&apos; pattern</description>
					<path>/ContractNotice/ext:UBLExtensions/ext:UBLExtension/ext:ExtensionContent/efext:EformsExtension/efac:Organizations/efac:Organization[1]/efac:Company</path>
					<type>SCHEMATRON</type>
				</warning>
			</warnings>
			<errors>
				<error>
					<rule>rule|text|BR-BT-00506-0052</rule>
					<ruleContent>matches(normalize-space(.),&apos;^[a-zA-Z0-9][a-zA-Z0-9._%+-]*@(?:[a-zA-Z0-9-]+\.)+[a-zA-Z]{2,63}$&apos;)</ruleContent>
					<description>The value of BT-506-Organization-Company must match the &apos;Email&apos; pattern</description>
					<path>/ContractNotice/ext:UBLExtensions/ext:UBLExtension/ext:ExtensionContent/efext:EformsExtension/efac:Organizations/efac:Organization[1]/efac:Company</path>
					<type>SCHEMATRON</type>
				</error>
			</errors>
			<schematronValidated>true</schematronValidated>
		</validation>
		<created>2023-11-03T15:01:38.373Z</created>
		<lastUpdated>2023-11-03T15:01:38.373Z</lastUpdated>
	</delivery>
</deliveries>
```

Die Statusinformationen enthalten sowohl bei unterschwelligen als auch bei oberschwelligen Bekanntmachungen den Status des Datenservice Öffentlicher Einkauf `doeStatus`, das letzte Änderungsdatum des DÖE-Status `doeStatusUpdate` sowie eine Beschreibung des aktuell gesetzten Status `statusDescription`.

Bei oberschwelligen Bekanntmachungen wird zusätzlich der TED-Staus `tedStatus` mit dem letzten Änderungsdatum `tedStatusUpdate` übermittelt. Die TED-Statuswerte orientieren sich an den Statuswerten der EU. 
<br><br>


### Statustabelle: Übermittlung einer Bekanntmachung<span id="statustabelle-uebermittlung">

| DÖE-Status        | Finaler Status?|Statusbeschreibung                                                                                       |
| ----------------- | -|--------------------------------------------------------------------------------------------------------- |
| AWAITING_TRANSFER | nein |Die Bekanntmachung wurde vom Mediator angenommen und akzeptiert. Die weitere Versendung wird vorbereitet. |

Nachdem die Übermittlung einer Bekanntmachung erfolgreich abgeschlossen ist, wird der Status der Bekanntmachung auf AWAITING_TRANSFER gesetzt und der Vermittlungsdienst beginnt mit weiteren Schritten der Verarbeitung der Unter- oder Oberschwellenvergabe. In den folgenden Statustabellen werden die möglichen Status für die Verarbeitung der Unter- und Oberschwellenvergabe aufgelistet.
<br><br>

### Statustabelle: Oberschwellenvergabe<span id="statustabelle-oberschwelle">

Die folgenden Statuskombinationen können bei der Statusabfrage einer Oberschwellenvergabe übermittelt werden.

| TED-Status        | DÖE-Status     |Finaler Status? |Statusbeschreibung                                                                                                  						  |  Auf Vergabeplattform publizieren? | 
| ----------------- | -------------- | ---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | - | 
| PENDING           | PENDING        |nein      |Die Bekanntmachung wurde vom eSender zur weiteren Verarbeitung angenommen. Die Übermittlung der Bekanntmachung an TED und an den Bekanntmachungsservice steht noch aus. | noch abwarten  | 
| NO_RESPONSE       | PENDING        | nein     |Die Übermittlung an TED wird erneut versucht. Die Übermittlung der Bekanntmachung an den Bekanntmachungsservice steht noch aus.                                          |  noch abwarten | 
| ACCEPTED          | PENDING        | nein     |Die Bekanntmachung wurde von TED akzeptiert, die Übermittlung an den Bekanntmachungsservice steht noch aus.                                                              |  48h nach tedAcceptedTimestamp | 
| ACCEPTED          | ACCEPTED       | nein     |Die Bekanntmachung wurde von TED und dem Bekanntmachungsservice akzeptiert, aber noch nicht veröffentlicht.                                                              |  48h nach tedAcceptedTimestamp  | 
| ACCEPTED          | PUBLISHED      | nein     |Die Bekanntmachung wurde von TED akzeptiert, aber noch nicht veröffentlicht. Die Bekanntmachung wurde bereits im Bekanntmachungsservice veröffentlicht.     		  |  48h nach tedAcceptedTimestamp  | 
| PUBLISHING        | PENDING        | nein     |Die Bekanntmachung wird in TED veröffentlicht, die Übermittlung an den Bekanntmachungsservice steht noch aus.                                                            |  48h nach tedAcceptedTimestamp  | 
| PUBLISHING        | ACCEPTED       | nein     |Die Bekanntmachung wird in TED veröffentlicht, die Bekanntmachung wurde vom Bekanntmachungsservice akzeptiert.                                                           |  48h nach tedAcceptedTimestamp  | 
| PUBLISHING        | PUBLISHED      | nein     |Die Bekanntmachung wird in TED veröffentlicht, die Bekanntmachung wurde im Bekanntmachungsservice veröffentlicht.                                                        |  48h nach tedAcceptedTimestamp  | 
| STOPPED           | NOT_SEND       | ja       |Die Bekanntmachung wurde in TED gestoppt und wird nicht zum Bekanntmachungsservice gesendet.                                                                             |  nein | 
| STOPPED           | PENDING        | nein     |Die Bekanntmachung wurde in TED gestoppt und wird in Kürze auch im Bekanntmachungsservice gestoppt werden.                                                               |  nein | 
| STOPPED           | ACCEPTED       | nein     |Die Bekanntmachung wurde in TED gestoppt und wird in Kürze auch im Bekanntmachungsservice gestoppt werden.                                                               |  nein | 
| STOPPED           | PUBLISHED      | nein     |Die Bekanntmachung wurde in TED gestoppt und wird in Kürze auch im Bekanntmachungsservice gestoppt werden.                                                               |  nein | 
| STOPPED           | STOPPED        | ja       |Die Bekanntmachung wurde sowohl in TED als auch im Bekanntmachungsservice gestoppt.                                                                                      |  nein | 
| PUBLISHED         | PENDING        | nein     |Die Bekanntmachung wurde in TED veröffentlicht, die Übermittlung an den Bekanntmachungsservice steht noch aus.                                                           |  ja | 
| PUBLISHED         | ACCEPTED       | nein     |Die Bekanntmachung wurde in TED veröffentlicht und vom Bekanntmachungsservice akzeptiert, aber noch nicht veröffentlicht.                                                |  ja | 
| PUBLISHED         | PUBLISHED      | ja       |Die Bekanntmachung wurde in TED und im Bekanntmachungsservice veröffentlicht.                                                                                            |  ja | 
| MANUALLY_REJECTED | NOT_SEND       | ja       |Die Bekanntmachung wurde entweder von TED auf Grund einer rechtlichen Prüfung oder vom Vermittlungsdienst auf Grund eines Fehlers manuell abgelehnt und wird weder von TED noch vom Bekanntmachungsservice veröffentlicht. Dies lässt sich anhand der Fehlermeldung unterscheiden.     |  nein | 
| MANUALLY_REJECTED | PENDING        | nein     |Die Bekanntmachung wurde von TED auf Grund einer rechtlichen Prüfung manuell abgelehnt und wird in Kürze auch im Bekanntmachungsservice gestoppt.                        |  nein | 
| MANUALLY_REJECTED | ACCEPTED       | nein     |Die Bekanntmachung wurde von TED auf Grund einer rechtlichen Prüfung manuell abgelehnt und wird in Kürze auch im Bekanntmachungsservice gestoppt.                        |  nein | 
| MANUALLY_REJECTED | PUBLISHED      | nein     |Die Bekanntmachung wurde von TED auf Grund einer rechtlichen Prüfung manuell abgelehnt und wird in Kürze auch im Bekanntmachungsservice gestoppt.                        |  nein | 
| MANUALLY_REJECTED | STOPPED        | ja       |Die Bekanntmachung wurde von TED auf Grund einer rechtlichen Prüfung manuell abgelehnt und wurde auch im Bekanntmachungsservice gestoppt.                                |  nein | 
| REJECTED          | INTERNAL_ERROR | nein     |Ein interner Fehler ist aufgetreten. Das Support-Team wird sich die Bekanntmachung genauer ansehen, der Status ändert sich anschließend.                                 |  noch abwarten | 
| NOT_SEND          | INTERNAL_ERROR | nein     |Ein interner Fehler ist aufgetreten. Das Support-Team wird sich die Bekanntmachung genauer ansehen, der Status ändert sich anschließend.                       	  |  noch abwarten | 


<br>

### Statustabelle: Unterschwellenvergabe<span id="statustabelle-unterschwelle">

Die folgenden Statuskombinationen können bei der Statusabfrage einer Unterschwellenvergabe übermittelt werden.

| DÖE-Status | Finaler Status?| Statusbeschreibung                                             |
|------------| ----| --------------------------------------------------------------- |
| ACCEPTED   | nein | Die Bekanntmachung wurde vom Bekanntmachungsservice akzeptiert. |
| REJECTED   | ja   | Die Bekanntmachung wurde vom BKMS abgelehnt.                    |
| PROCESSING | nein | Die Bekanntmachung wird vom BKMS verarbeitet.                   |
| PUBLISHED  | ja   | Die Bekanntmachung wurde im BKMS veröffentlicht.                |
| STOPPED    | ja   | Die Bekanntmachung wurde  im Bekanntmachungsservice gestoppt.   |



<br>

## Struktur der Transferinformationen<span id="transfer-info">
Die Transferinformationen sind ebenfalls für jede Bekanntmachung im Delivery-Schema enthalten. Diese Informationen beinhalten Warnungen und Fehlermeldungen vom Vermittlungsdienst, dem Bekanntmachungsservice und von TED.
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

Innerhalb der Transferinformationen `transferResponse` werden Warnungen `warnings` von Fehlermeldungen `errors` getrennt aufgelistet. Pro Bekanntmachung ist es möglich, mehrere Warnungen und Fehlermeldungen als Rückantwort zu erhalten. 

Eine einzelne Warnung und eine einzelne Fehlermeldung haben denselben Aufbau. `source` gibt an, in welchem System die Warnung oder der Fehler entstand. Folgende Werte sind in `source` möglich:

| Werte in Source  | Beschreibung                   |
| -------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| TED            | Fehler und Warnungen, die von TED kommen. Dies beinhaltet sowohl die http-Codes (5\*\*, 4\*\*), welche bei einer erfolglosen Übermittlung zurückgegeben werden, als auch Fehler und Warnungen aus dem TED-Validierungsreport. |
| BKMS           | Fehler, die vom BKMS kommen, wenn BKMS einen http-Code zurückgibt, der eine erfolglose Übermittlung darstellt (5\*\*, 4\*\*).                                                                                                |
| PRE_VALIDATION | Fehler und Warnungen aus dem internen Validierungsdienst.                                                                                                                                                                    |

Die `description` enthält die Beschreibung der Warnung oder der Fehlermeldung. Im `path` wird die Position angegeben, an der der Fehler oder die Warnung auftrat. Der Tag `rule` enthält die Bezeichnung der angewandten Regel und `ruleContent` die dazu tatsächlich angewandte Regel.

Warnungen und Fehlermeldungen vom Bekanntmachungsservice und von TED werden unverändert durchgereicht.
<br><br>

## Lawfulness Warnings<span id="lawfulness">
Zusätzlich zu Fehlern gibt es Warnungen. Diese kommen ausschließlich aus den EU-Regeln und verhindern anders als Fehler nicht die Annahme der Bekanntmachung. TED hat derzeit nur eine Art von Warnungen definiert, sogenannte "Lawfulness Warnings". Diese werden höchstwahrscheinlich für deutsche Bekanntmachungen nahezu irrelevant sein, sind aber technisch möglich. 

Eine Lawfulness Warning bedeutet, dass eine manuelle Überprüfung einer Bekanntmachung bei TED notwendig ist. Dort wird dann der Inhalt der Bekanntmachung geprüft und entschieden, ob diese veröffentlicht wird oder abgelehnt und nicht veröffentlicht wird. Eine Entscheidung muss nach maximal fünf Tagen getroffen sein. Aus diesem Grund werden Bekanntmachungen mit einer Lawfulness Warning erst bei Veröffentlichung oder spätestens fünf Tage nach erfolgreicher Einlieferung bei TED an den Bekanntmachungsservice weitergeleitet.


