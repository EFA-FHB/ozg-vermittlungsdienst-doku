### Data service public procurement
[Table of contents](/documentation/documentation.md)
<br>

# Status and transfer information

All status and error information of an announcement can be queried using the REST API of the Vermittlungsdienst. The status and error information of the BKMS and TED is regularly queried and stored by the Vermittlungsdienst or eSender Hub, so that the status and further information on an announcement is available for further retrieval at any time.
<br>

## Contents
- Endpoints for querying status and transfer information](#endpoints)
- Structure of the status information](#info-struktur)
    - [Status table: Transmission of a notification](#statustabelle-uebermittlung)
    - [Status table: Notices above the EU thresholds](#statustabelle-oberschwelle)
    - [Status table: Notices below the EU thresholds](#statustabelle-unterschwelle)
- [Structure of the transfer information](#transfer-info)
- Lawfulness Warnings](#lawfulness)


<br><br>

## Endpoints for querying status and transfer information<span id="endpoints">
To query the status and transfer information, the Vermittlungsdienst provides the endpoints `GET /v1/notices` for a list of data deliveries, `GET /v1/notices/status` for a list of data deliveries in a specific period and `GET /v1/notices/{trackingcode}` and `GET /v1/notices/by-notice/{noticeId}/{version}` for a single data delivery.

The Vermittlungsdienst performs status queries to the notification service and TED every three minutes. It therefore makes sense to query the status information of the notices to the Vermittlungsdienst every five minutes at most.

The corresponding OpenAPI specification can be found here https://ozg-vermittlungsdienst.de/ and is available for download in JSON format at https://ozg-vermittlungsdienst.de/Vermittlungsdienst_REST-API.json.
<br><br>

## Structure of the status information<span id="info-struktur">
The endpoints for querying the status information return the status information for each announcement within the delivery schema as follows

```
<?xml version="1.0" encoding="UTF-8"?>
<deliveries start="0" max="100" total="1234">
	<delivery>
		<noticeId>3fa85f64-5717-4562-b3fc-2c963f66afa6</noticeId>
		<noticeType>CN</noticeType>
		<trackingCode>3446e1ee-5917-4d31-b623-81ddfb038d82</trackingCode>
		<awardId>string</awardId>
		<award number>V0505/2021</award number>
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

For notices above and below the EU thresholds, the status information contains the status of the public procurement data service `doeStatus`, the last change date of the doe status `doeStatusUpdate` and a description of the currently set status `statusDescription`.

For notices above the EU thresholds, the TED status `tedStatus` with the last change date `tedStatusUpdate` is also transmitted. The TED status values are based on the EU status values.
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
| PENDING | PENDING | no | The announcement has been accepted by the eSender for further processing. The announcement has not yet been sent to TED and the announcement service. | still waiting |
| NO_RESPONSE | PENDING | no | Transmission to TED will be attempted again. The transmission of the announcement to the announcement service is still pending.                                          | still waiting |
| ACCEPTED | PENDING | no | The announcement has been accepted by TED, transmission to the announcement service is still pending.                                                              | 48h after tedAcceptedTimestamp |
| ACCEPTED | ACCEPTED | no | The announcement has been accepted by TED and the announcement service, but has not yet been published.                                                              | 48h after tedAcceptedTimestamp |
| ACCEPTED | PUBLISHED | no | The announcement has been accepted by TED but not yet published. The announcement has already been published in the announcement service | 48h after tedAcceptedTimestamp |
| PUBLISHING | PENDING | no | The announcement is published in TED, the transmission to the announcement service is still pending.                                                            | 48h after tedAcceptedTimestamp |
| PUBLISHING | ACCEPTED | no | The announcement is published in TED, the announcement has been accepted by the announcement service.                                                           | 48h after tedAcceptedTimestamp |
| PUBLISHING | PUBLISHED | no | The announcement is published in TED, the announcement has been published in the announcement service.                                                        | 48h after tedAcceptedTimestamp |
| STOPPED | NOT_SEND | yes | The announcement has been stopped in TED and will not be sent to the announcement service.                                                                             | no |
| STOPPED | PENDING | no | The announcement has been stopped in TED and will soon be stopped in the announcement service.                                                               | no |
| STOPPED | ACCEPTED | no | The announcement has been stopped in TED and will also be stopped in the announcement service shortly.                                                               no | |
| STOPPED | PUBLISHED | no | The announcement has been stopped in TED and will also be stopped in the announcement service shortly.                                                               | no |
| STOPPED | STOPPED | yes | The announcement has been stopped in TED as well as in the announcement service.                                                                                      | no |
| PUBLISHED | PENDING | no | The announcement has been published in TED, the transmission to the announcement service is still pending.                                                           yes | |
| PUBLISHED | ACCEPTED | no | The announcement has been published in TED and accepted by the announcement service, but not yet published.                                                | yes
| PUBLISHED | PUBLISHED | yes | The announcement has been published in TED and in the announcement service.                                                                                            | yes
| MANUALLY_REJECTED | NOT_SEND | yes | The announcement was either manually rejected by TED due to a legal check or by the Vermittlungsdienst due to an error and will not be published by TED or the announcement service. This can be distinguished by the error message.     | no
| MANUALLY_REJECTED | PENDING | no | The announcement was manually rejected by TED due to a legal check and will also be stopped in the announcement service shortly.                        | no |
| MANUALLY_REJECTED | ACCEPTED | no | The announcement was manually rejected by TED due to a legal check and will also be stopped in the announcement service shortly.                        | no |
| MANUALLY_REJECTED | PUBLISHED | no | The announcement was manually rejected by TED due to a legal check and will also be stopped in the announcement service shortly.                        | no |
| MANUALLY_REJECTED | STOPPED | yes | The announcement was manually rejected by TED due to a legal check and has also been stopped in the announcement service.                                | no
| REJECTED | INTERNAL_ERROR | no | An internal error has occurred. The support team will take a closer look at the announcement, the status will then change.                                 | still waiting |
| NOT_SEND | INTERNAL_ERROR | no | An internal error has occurred. The support team will take a closer look at the notification, the status will then change.


<br>

### Status table: Notices below the EU thresholds<span id="statustabelle-unterschwelle">

The following status combinations can be transmitted when querying the status of a notice below the EU thresholds

| DÖE status | Final status | Status description |
|------------| ----| --------------------------------------------------------------- |
| ACCEPTED | no | The contract notice has been accepted by the contract notice service. |
| REJECTED | yes | The announcement has been rejected by the announcement service.                    |
| PROCESSING | no | The announcement is being processed by the BKBekanntmachungsservice.                   |
| PUBLISHED | yes | The announcement has been published in the announcement service.                |
| STOPPED | yes | The announcement has been stopped in the announcement service.   |



<br>

## Structure of the transfer information<span id="transfer-info">
The transfer information is also contained in the delivery schema for each announcement. This information includes warnings and error messages from the Vermittlungsdienst, the announcement service and TED.
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
| Announcement service | Errors coming from the announcement service when announcement service returns an http code representing an unsuccessful submission (5\*\*, 4\*\*).                                                                                                |
| PRE_VALIDATION | Errors and warnings from the internal validation service.                                                                                                                                                                    |

The `description` contains the description of the warning or error message. The `path` indicates the position where the error or warning occurred. The `rule` tag contains the name of the rule applied and `ruleContent` contains the rule actually applied.

Warnings and error messages from the announcement service and from TED are passed through unchanged.
<br><br>

## Special case lawfulness warnings<span id="lawfulness">
A lawfulness warning means that a manual check of an announcement at TED is necessary. The content of the announcement is then checked and a decision is made as to whether it will be published or rejected and not published. A decision must be made after a maximum of five days. For this reason, announcements with a lawfulness warning are only forwarded to the announcement service upon publication or at the latest five days after successful submission to TED.



