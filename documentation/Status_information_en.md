---
title: Status Information
---

[Table of contents](/documentation/documentation.md)
<br>

# Status and transfer information

All status and error information related to a notice can be queried using the REST API of the Vermittlungsdienst. The status and error information from the BKMS and TED is regularly queried and stored by the Vermittlungsdienst or eSender Hub, so that the status and further information regarding a notice is available for further retrieval at any time.
<br>

## Contents
- [Endpoints for querying status and transfer information](#endpoints)
- [Structure of the status information](#info-struktur)
    - [Status table: Transmission of a notification](#statustabelle-uebermittlung)
    - [Status table: Notices above the EU thresholds](#statustabelle-oberschwelle)
    - [Status table: Notices below the EU thresholds](#statustabelle-unterschwelle)
    - [Status table: Notices relevant for the Service Vergabestatistik](#statustabelle-svs)
- [Structure of the transfer information](#transfer-info)
- [Lawfulness Warnings](#lawfulness)


<br><br>

## Endpoints for querying status and transfer information<span id="endpoints">
To query the status and transfer information, the Vermittlungsdienst provides the endpoints `GET /v1/notices` for a list of data deliveries, `GET /v1/notices/status` for a list of data deliveries in a specific period and `GET /v1/notices/{trackingcode}` and `GET /v1/notices/by-notice/{noticeId}/{version}` for a single data delivery.

The Vermittlungsdienst performs status queries to the Publication Service and TED every three minutes. It therefore makes sense to query the status information of the notices to the Vermittlungsdienst at most every five minutes.

The corresponding OpenAPI specification can be found here https://ozg-vermittlungsdienst.de/ and is available for download in JSON format at https://ozg-vermittlungsdienst.de/Vermittlungsdienst_REST-API.json.
<br><br>

## Structure of the status information<span id="info-struktur">
The endpoints for querying the status information return the status information for each notice within the delivery schema as follows:

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
			<description>Result report of the validation of the data delivery by the Vermittlungsdienst</description>
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

For notices above and below the EU thresholds, the status information contains the status of the Publications Office `doeStatus`, the last change date of the doe status `doeStatusUpdate` and a description of the currently set status `statusDescription`.

For notices above the EU thresholds, the TED status `tedStatus` with the latest change date `tedStatusUpdate` is also provided. The TED status values are based on the EU status values.

For Contract Award Notices that are relevant for the Service Vergabestatistik (SVS), the following status information is also transmitted: `svsStatus`, the last change date of the SVS status `svsStatusUpdate`, a code `svsStatusDetail.code` and a description that explains the status in more detail `svsStatusDetail.descriptionDe` / `svsStatusDetail.descriptionEn`. The URL for the SVS is transmitted under `svsReportLink`.
<br><br>


### Status table: Transmission of a notification<span id="statustabelle-uebermittlung">

| DÖE-Status | Final Status?|Status Description |
| ----------------- | -|--------------------------------------------------------------------------------------------------------- |
| AWAITING_TRANSFER | no | The notice has been accepted by the Vermittlungsdienst. Further dispatch is being prepared. |

Once the transmission of a notice has been successfully completed, the status of the notice is set to AWAITING_TRANSFER and the Vermittlungsdienst begins the next steps in processing the notices above and below the EU thresholds. The possible statuses for processing notices above and below the EU thresholds are listed in the following status tables.
<br><br>

### Status table: Notices above the EU thresholds<span id="statustabelle-oberschwelle">

The following status combinations can be transmitted when requesting the status of a notice above the EU thresholds

| TED status | DoE status | Final status? | Status description | Publish on procurement platform? |
| ----------------- | -------------- | ---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | - |
| PENDING | PENDING | no | The notice has been accepted by the eSender for further processing. The notice has not yet been sent to TED and the Publication Service. | still waiting |
| NO_RESPONSE | PENDING | no | Transmission to TED will be attempted again. The transmission of the notice to the Publication Service is still pending. | still waiting |
| ACCEPTED | PENDING | no | The notice has been accepted by TED, transmission to the Publication Service is still pending. | 48h after tedAcceptedTimestamp |
| ACCEPTED | ACCEPTED | no | The notice has been accepted by TED and the Publication Service, but has not yet been published. | 48h after tedAcceptedTimestamp |
| ACCEPTED | PUBLISHED | no | The notice has been accepted by TED but not yet published. The notice has already been published in the Publication Service | 48h after tedAcceptedTimestamp |
| PUBLISHING | PENDING | no | The notice is published in TED, the transmission to the Publication Service is still pending. | 48h after tedAcceptedTimestamp |
| PUBLISHING | ACCEPTED | no | The notice is published in TED, the notice has been accepted by the Publication Service. | 48h after tedAcceptedTimestamp |
| PUBLISHING | PUBLISHED | no | The notice is published in TED, the notice has been published in the Publication Service. | 48h after tedAcceptedTimestamp |
| STOPPED | NOT_SEND | yes | The notice has been stopped in TED and will not be sent to the Publication Service. | no |
| STOPPED | PENDING | no | The notice has been stopped in TED and will soon be stopped in the Publication Service. | no |
| STOPPED | ACCEPTED | no | The notice has been stopped in TED and will also be stopped in the Publication Service shortly. | no |
| STOPPED | PUBLISHED | no | The notice has been stopped in TED and will also be stopped in the Publication Service shortly. | no |
| STOPPED | STOPPED | yes | The notice has been stopped in TED as well as in the Publication Service. | no |
| PUBLISHED | PENDING | no | The notice has been published in TED, the transmission to the Publication Service is still pending. | yes |
| PUBLISHED | ACCEPTED | no | The notice has been published in TED and accepted by the Publication Service, but not yet published. | yes |
| PUBLISHED | PUBLISHED | yes | The notice has been published in TED and in the Publication Service. | yes |
| MANUALLY_REJECTED | NOT_SEND | yes | The notice was either manually rejected by TED due to a legal check or by the Vermittlungsdienst due to an error and will not be published by TED or the Publication Service. This can be distinguished by the error message. | no |
| MANUALLY_REJECTED | PENDING | no | The notice was manually rejected by TED due to a legal check and will also be stopped in the Publication Service shortly. | no |
| MANUALLY_REJECTED | ACCEPTED | no | The notice was manually rejected by TED due to a legal check and will also be stopped in the Publication Service shortly. | no |
| MANUALLY_REJECTED | PUBLISHED | no | The notice was manually rejected by TED due to a legal check and will also be stopped in the Publication Service shortly. | no |
| MANUALLY_REJECTED | STOPPED | yes | The notice was manually rejected by TED due to a legal check and has also been stopped in the Publication Service. | no |
| REJECTED | INTERNAL_ERROR | no | An internal error has occurred. The support team will take a closer look at the notice, the status will then change. | still waiting |
| NOT_SEND | INTERNAL_ERROR | no | An internal error has occurred. The support team will take a closer look at the notification, the status will then change. | still waiting |


<br>

### Status table: Notices below the EU thresholds<span id="statustabelle-unterschwelle">

The following status combinations can be transmitted when querying the status of a notice below the EU thresholds

| DÖE status | Final status | Status description |
|------------| ----| --------------------------------------------------------------- |
| ACCEPTED | no | The contract notice has been accepted by the Publication Service. |
| REJECTED | yes | The notice has been rejected by the Publication Service. |
| PROCESSING | no | The notice is being processed by the Publication Service. |
| PUBLISHED | yes | The notice has been published in the Publication Service. |
| STOPPED | yes | The notice has been stopped in the Publication Service. |

<br>

### Status table: Notices relevant for the Service Vergabestatistik<span id="statustabelle-svs">

The following status combinations can be transmitted by the Vermittlungsdienst when querying the status of a procurement notice relevant for the Service Vergabestatistik.

| SVS status <br> `svsStatus` | StatusDetailCode <br> `svsStatusDetail.code` | Final status? | Status description / Display text in BKMS <br> `svsStatusDetail.descriptionEn` |
|---|---|---|---|
| NOT_QUALIFIED | 1000 | Yes | No automatic statistical report was generated for this contract award notice as no reporting unit ID was provided. |
| NOT_QUALIFIED | 1010 | Yes | No automatic statistical report was generated for this contract award notice as the submitted report ID is invalid. |
| NOT_QUALIFIED | 1020 | Yes | No automatic statistical report was generated for this contract award notice as the procedure has not yet been completed for all lots. |
| NOT_QUALIFIED | 1030 | Yes | No automatic statistical report was generated for this contract award notice as contract values of up to 1.000 EUR are not included in the public procurement statistics. |
| NOT_QUALIFIED | 1040 | Yes | No automatic statistical report was generated for this contract award notice as the reporting deadline has been exceeded. |
| NOT_QUALIFIED | 1050 | Yes | No automatic statistical report was generated for this contract award notice as an automatic statistical report had already been sent and the reporting deadline has since expired. |
| NOT_QUALIFIED | 1060 | Yes | No automatic statistical report was generated for this contract award notice as no contract was assigned. |
| NOT_QUALIFIED | 1070 | Yes | No automatic statistical report was generated for this contract award notice as individual orders from a framework agreement are not included in the public procurement statistics. |
| PENDING | 2000 | No | A statistical report will be generated automatically for this contract award notice and submitted to the Federal Statistical Office at the end of the reporting period. |
| SUSPENDED | 3000 | Yes | The automatically generated statistical report was withdrawn before it was submitted to the Federal Statistical Office. |
| SUSPENDED | 3500 | Yes | The statistical report was withdrawn before it was submitted to the Federal Statistical Office. An updated version will be generated automatically and submitted to the Federal Statistical Office at the end of the reporting period. |
| PROCESSED | 4000 | No | A statistical report was automatically generated for this contract award notice; it will now be submitted to the Federal Statistical Office. |
| PROCESSED | 4010 | Yes | An error occurred while generating the statistical report from the contract award notice. |
| DELIVERED | 5000 | Yes | The automatically generated statistical report has been successfully submitted to the Federal Statistical Office. The reporting requirement is considered fulfilled. |
| DELIVERED | 5010 | No | The transmission of the automatically generated statistical report to the Federal Statistical Office failed; further attempts to send it will be made. |
| DELIVERED | 5020 | Yes | The transmission of the automatically generated statistical report to the Federal Statistical Office failed. |
| UNKNOWN | 7000 | | Due to a technical error, it is currently not possible to determine the status of the automatic statistics report. |

<br>

## Structure of the transfer information<span id="transfer-info">
The transfer information is also contained in the delivery schema for each notice. This information includes warnings and error messages from the Vermittlungsdienst, the Publication Service and TED.
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

Within the transfer information `transferResponse`, warnings `warnings` are listed separately from error messages `errors`. It is possible to receive several warnings and error messages as a response for each notification.

A single warning and a single error message have the same structure. `source` specifies the system in which the warning or error originated. The following values are possible in `source`:

| values in source | description |
| -------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| TED | Errors and warnings that come from TED. This includes both the http codes (5\*\*, 4\*\*), which are returned in the event of an unsuccessful transmission, as well as errors and warnings from the TED validation report. |
| Publication Service | Errors coming from the Publication Service when the Publication Service returns an http code representing an unsuccessful submission (5\*\*, 4\*\*). |
| PRE_VALIDATION | Errors and warnings from the internal validation service. |

The `description` contains the description of the warning or error message. The `path` indicates the position where the error or warning occurred. The `rule` tag contains the name of the rule applied and `ruleContent` contains the rule actually applied.

Warnings and error messages from the Publication Service and from TED are passed through unchanged.
<br><br>

## Special case lawfulness warnings<span id="lawfulness">
A lawfulness warning means that a manual check of a notice at TED is necessary. The content of the notice is then checked and a decision is made as to whether it will be published or rejected and not published. A decision must be made after a maximum of five days. For this reason, notices with a lawfulness warning are only forwarded to the Publication Service upon publication or at the latest five days after successful submission to TED.](image.png)