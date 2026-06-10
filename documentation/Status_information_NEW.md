---
title: Status Information
---

[Inhaltsverzeichnis](/documentation/documentation.md)
<br>

# Status- und Transferinformationen

Mit Hilfe der REST-API des Vermittlungsdienstes können alle Status- und Fehlerinformationen einer Bekanntmachung abgefragt werden. Die Status- und Fehlerinformationen des BKMS und von TED werden regelmäßig vom Vermittlungsdienst bzw. eSender-Hub abgefragt und gespeichert, so dass jederzeit der Status und weitere Informationen zu einer Bekanntmachung zum weiteren Abruf bereit liegen.
<br>

## Inhalte
- [Endpunkte zur Abfrage der Status- und Transferinformationen](#endpunkte)
- [Struktur der Statusinformationen](#info-struktur)
    - [Statustabelle: Übermittlung einer Bekanntmachung](#statustabelle-uebermittlung)
    - [Statustabelle: Bekanntmachungen oberhalb der EU-Schwellenwerte](#statustabelle-oberschwelle)
    - [Statustabelle: Bekanntmachungen unterhalb der EU-Schwellenwerte](#statustabelle-unterschwelle)
	- [Statustabelle: Bekanntmachungen, die für den Service Vergabestatistik relevant sind](#statustabelle-svs)
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
		<tedStatusUpdate>2026-06-09T12:24:04.623Z</tedStatusUpdate>
		<tedAcceptedTimestamp>2026-06-09T12:24:04.624Z</tedAcceptedTimestamp>
		<tedPublishedDate>2026-06-09</tedPublishedDate>
		<tedPublicationId>string</tedPublicationId>
		<doeStatus>AWAITING_TRANSFER</doeStatus>
		<doeStatusUpdate>2026-06-09T12:24:04.624Z</doeStatusUpdate>
		<svsStatus>string</svsStatus>
		<svsStatusUpdate>2026-06-09T12:24:04.624Z</svsStatusUpdate>
		<svsStatusDetail>
			<code>1000</code>
			<descriptionEn>SVS processing in progress</descriptionEn>
			<descriptionDe>string</descriptionDe>
		</svsStatusDetail>
		<svsReportLink>string</svsReportLink>
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

Die Statusinformationen enthalten bei Bekanntmachungen oberhalb und unterhalb der EU-Schwellenwerte den Status des Datenservice Öffentlicher Einkauf `doeStatus`, das letzte Änderungsdatum des doe-Status `doeStatusUpdate` sowie eine Beschreibung des aktuell gesetzten Status `statusDescription`.

Bei Bekanntmachungen oberhalb der EU-Schwellenwerte wird zusätzlich der TED-Status `tedStatus` mit dem letzten Änderungsdatum `tedStatusUpdate` übermittelt. Die TED-Statuswerte orientieren sich an den Statuswerten der EU. 

Für CANs, die für den Service Vergabestatistik (SVS) relevant sind, werden zusätzlich folgende Statusinformationen übermittelt: `svsStatus`, das letzte Änderungsdatum des SVS-Status `svsStatusUpdate`, ein Code `code` sowie eine Beschreibung, die den Status genauer erklärt `descriptionDe` / `descriptionEn`. Unter `svsReportLink` wird die URL für das SVS übermittelt.
<br><br>


### Statustabelle: Übermittlung einer Bekanntmachung<span id="statustabelle-uebermittlung">

| DÖE-Status <br> `doeStatus` | Finaler Status?|Statusbeschreibung                                                                                       |
| ----------------- | -|--------------------------------------------------------------------------------------------------------- |
| AWAITING_TRANSFER | nein |Die Bekanntmachung wurde vom Vermittlungsdienst angenommen und akzeptiert. Die weitere Versendung wird vorbereitet. |

Nachdem die Übermittlung einer Bekanntmachung erfolgreich abgeschlossen ist, wird der Status der Bekanntmachung auf AWAITING_TRANSFER gesetzt und der Vermittlungsdienst beginnt mit weiteren Schritten der Verarbeitung der Bekanntmachungen oberhalb und unterhalb der EU-Schwellenwerte. In den folgenden Statustabellen werden die möglichen Status für die Verarbeitung der Bekanntmachungen oberhalb und unterhalb der EU-Schwellenwerte aufgelistet.
<br><br>

### Statustabelle: Bekanntmachungen oberhalb der EU-Schwellenwerte<span id="statustabelle-oberschwelle">

Die folgenden Statuskombinationen können bei der Statusabfrage einer Bekanntmachung oberhalb der EU-Schwellenwerte übermittelt werden.

| TED-Status <br> `tedStatus`  | DÖE-Status <br> `doeStatus`     |Finaler Status? |Statusbeschreibung                                                                                                  						  |  Auf Vergabeplattform publizieren? | 
| ----------------- | -------------- | ---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | - | 
| PENDING           | PENDING        |nein      |Die Bekanntmachung wurde vom eSender zur weiteren Verarbeitung angenommen. Die Übermittlung der Bekanntmachung an TED und an den Bekanntmachungsservice steht noch aus. | noch abwarten  | 
| NO_RESPONSE       | PENDING        | nein     |Die Übermittlung an TED wird erneut versucht. Die Übermittlung der Bekanntmachung an den Bekanntmachungsservice steht noch aus.                                          |  noch abwarten | 
| ACCEPTED          | PENDING        | nein     |Die Bekanntmachung wurde von TED akzeptiert, die Übermittlung an den Bekanntmachungsservice steht noch aus.                                                              |  48 Stunden nach Akzeptierung durch TED | 
| ACCEPTED          | ACCEPTED       | nein     |Die Bekanntmachung wurde von TED und dem Bekanntmachungsservice akzeptiert, aber noch nicht veröffentlicht.                                                              |  48 Stunden nach Akzeptierung durch TED  | 
| ACCEPTED          | PUBLISHED      | nein     |Die Bekanntmachung wurde von TED akzeptiert, aber noch nicht veröffentlicht. Die Bekanntmachung wurde bereits im Bekanntmachungsservice veröffentlicht.     		  |  48 Stunden nach Akzeptierung durch TED  | 
| PUBLISHING        | PENDING        | nein     |Die Bekanntmachung wird in TED veröffentlicht, die Übermittlung an den Bekanntmachungsservice steht noch aus.                                                            |  48 Stunden nach Akzeptierung durch TED  | 
| PUBLISHING        | ACCEPTED       | nein     |Die Bekanntmachung wird in TED veröffentlicht, die Bekanntmachung wurde vom Bekanntmachungsservice akzeptiert.                                                           |  48 Stunden nach Akzeptierung durch TED  | 
| PUBLISHING        | PUBLISHED      | nein     |Die Bekanntmachung wird in TED veröffentlicht, die Bekanntmachung wurde im Bekanntmachungsservice veröffentlicht.                                                        |  48 Stunden nach Akzeptierung durch TED  | 
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

### Statustabelle: Bekanntmachungen unterhalb der EU-Schwellenwerte<span id="statustabelle-unterschwelle">

Die folgenden Statuskombinationen können bei der Statusabfrage einer Bekanntmachung unterhalb der EU-Schwellenwerte übermittelt werden.

| DÖE-Status <br> `doeStatus` | Finaler Status?| Statusbeschreibung                                             |
|------------| ----| --------------------------------------------------------------- |
| ACCEPTED   | nein | Die Bekanntmachung wurde vom Bekanntmachungsservice akzeptiert. |
| REJECTED   | ja   | Die Bekanntmachung wurde vom Bekanntmachungsservice abgelehnt.                    |
| PROCESSING | nein | Die Bekanntmachung wird vom BKBekanntmachungsservice verarbeitet.                   |
| PUBLISHED  | ja   | Die Bekanntmachung wurde im Bekanntmachungsservice veröffentlicht.                |
| STOPPED    | ja   | Die Bekanntmachung wurde  im Bekanntmachungsservice gestoppt.   |

<br>

### Statustabelle: Bekanntmachungen, die für den Service Vergabestatistik relevant sind<span id="statustabelle-svs">

Die folgenden Statuskombinationen können bei der Statusabfrage einer Bekanntmachung vom Vermittlungsdienst an den Bekanntmachungsservice und das Self-Service-Portal übermittelt werden.

| SVS-Status <br> `doeStatus` | StatusDetailCode <br> `code` | Finaler Status? | Statusbeschreibung / Anzeigetext im BKMS |
|---|---|---|---|
| NOT_QUALIFIED | 1000 | Ja | Diese Vergabebekanntmachung wird im Service Vergabestatistik nicht verarbeitet, da keine BerichteinheitsID vermerkt wurde. |
| NOT_QUALIFIED | 1010 | Ja | Diese Vergabebekanntmachung wird im Service Vergabestatistik nicht verarbeitet, da die übermittelte BerichteinheitsID nicht gültig ist. |
| NOT_QUALIFIED | 1020 | Ja | Diese Vergabebekanntmachung wird im Service Vergabestatistik nicht verarbeitet, da das Verfahren noch nicht abgeschlossen ist. |
| NOT_QUALIFIED | 1030 | Ja | Diese Vergabebekanntmachung wird im Service Vergabestatistik nicht verarbeitet, da der Auftragswert des Verfahrens kleiner als 1000 € ist und daher in der Vergabestatistik nicht berücksichtigt wird. |
| NOT_QUALIFIED | 1040 | Ja | Diese Vergabebekanntmachung wird im Service Vergabestatistik nicht verarbeitet, da die Meldefrist abgelaufen ist. |
| NOT_QUALIFIED | 1050 | Ja | Diese Vergabebekanntmachung wird im Service Vergabestatistik nicht verarbeitet, da bereits eine Statistikmeldung versendet wurde und die Meldefrist abgelaufen ist. |
| NOT_QUALIFIED | 1060 | Ja | Das Verfahren wurde ohne Gewinner abgeschlossen. Eine Statistikmeldung erfolgt nicht. |
| NOT_QUALIFIED | 1070 | Ja | Das Verfahren ist Teil einer Rahmenvereinbarung, weswegen keine zusätzliche Statistikmeldung erfolgt. |
| NOT_QUALIFIED | 1080 | Ja | Diese Vergabebekanntmachung wird im Service Vergabestatistik nicht verarbeitet, da die Verfahrensarten „Sonstiges einstufiges Verfahren" und „Sonstiges zweistufiges Verfahren" in der Vergabestatistikverordnung in Vergabeverfahren oberhalb des EU-Schwellenwertes nicht vorgesehen sind. |
| PENDING | 2000 | Nein | Die Vergabebekanntmachung wird zum Ende der Meldefrist verarbeitet und versendet. |
| SUSPENDED | 3000 | Ja | Die Bekanntmachung wurde zurückgezogen. |
| PROCESSED | 4000 | Nein | Die Vergabebekanntmachung wurde erfolgreich verarbeitet, die Statistikmeldung wird nun versendet. |
| PROCESSED | 4010 | Nein | Beim Erstellen der Statistikmeldung aus der Vergabebekanntmachung ist ein Fehler aufgetreten. Bitte prüfen und versenden Sie die Vergabebekanntmachung erneut. |
| DELIVERED | 5000 | Ja | Der Versand wurde erfolgreich quittiert, die Meldepflicht gilt als erfüllt. |
| DELIVERED | 5010 | Nein | Der Versand ist fehlgeschlagen, es werden weitere Zustellversuche unternommen. |
| DELIVERED | 5020 | Ja | Der Versand ist trotz mehrmaliger Versuche fehlgeschlagen, bitte melden Sie die Statistik manuell mit der IDEV-Anwendung des StBa. |
| ACHIEVED | 6000 | Ja | Die Statistikmeldung wurde archiviert. |
| UNKNOWN | 7000 | ? | Es konnte kein Status ermittelt werden. |

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
| Bekanntmachungsservice           | Fehler, die vom Bekanntmachungsservice kommen, wenn Bekanntmachungsservice einen http-Code zurückgibt, der eine erfolglose Übermittlung darstellt (5\*\*, 4\*\*).                                                                                                |
| PRE_VALIDATION | Fehler und Warnungen aus dem internen Validierungsdienst.                                                                                                                                                                    |

Die `description` enthält die Beschreibung der Warnung oder der Fehlermeldung. Im `path` wird die Position angegeben, an der der Fehler oder die Warnung auftrat. Der Tag `rule` enthält die Bezeichnung der angewandten Regel und `ruleContent` die dazu tatsächlich angewandte Regel.

Warnungen und Fehlermeldungen vom Bekanntmachungsservice und von TED werden unverändert durchgereicht.
<br><br>

## Sonderfall Lawfulness Warnings<span id="lawfulness">
Eine Lawfulness Warning bedeutet, dass eine manuelle Überprüfung einer Bekanntmachung bei TED notwendig ist. Dort wird dann der Inhalt der Bekanntmachung geprüft und entschieden, ob diese veröffentlicht wird oder abgelehnt und nicht veröffentlicht wird. Eine Entscheidung muss nach maximal fünf Tagen getroffen sein. Aus diesem Grund werden Bekanntmachungen mit einer Lawfulness Warning erst bei Veröffentlichung oder spätestens fünf Tage nach erfolgreicher Einlieferung bei TED an den Bekanntmachungsservice weitergeleitet.



