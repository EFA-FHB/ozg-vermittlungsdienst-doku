### Data service public procurement
[Table of contents](/documentation/documentation.md)
<br>

# Status and transfer information

The REST API of the switching service can be used to query all status and error information of an announcement. The status and error information of the BKMS and TED are regularly queried and saved by the switching service or eSender Hub, so the status and further information on an announcement is always available for further retrieval.
<br>

## Contents
- Endpoints for querying status and transfer information](#endpoints)
- Structure of the status information](#info-struktur)
    - [Status table: Transmission of a notice](#statustabelle-uebermittlung)
    - [Status table: Upper threshold award](#statustabelle-oberschwellen)
    - [Status table: Sub-threshold award](#statustabelle-unterschwelle)
- Structure of the transfer information](#transfer-info)
- Lawfullness Warnings](#lawfullness)


<br><br>

## Endpoints for querying status and transfer information<span id="endpoints">
To query the status and transfer information, the switching service provides the endpoints `GET /v1/notices` for a list of data deliveries, `GET /v1/notices/status` for a list of data deliveries in a specific time period and `GET /v1/notices/{trackingcode}` for a single data delivery.

The switching service carries out status queries to BKMS and TED every three minutes. It therefore makes sense to query the status information of the notices to the switching service every 5 minutes at most.

The corresponding OpenAPI specification can be found at https://ozg-vermittlungsdienst.de/ and is available for download in JSON format at https://ozg-vermittlungsdienst.de/Vermittlungsdienst_REST-API.json.
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
			<description>Result report of the validation of the data delivery by the switching service</description>
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

The status information contains the status of the Public Purchasing data service `doeStatus`, the last change date of the DoE status `doeStatusUpdate` and a description of the currently set status `statusDescription` for both subthreshold and above-threshold notifications.

For above-threshold announcements, the TED status `tedStatus` with the last change date `tedStatusUpdate` is also transmitted. The TED status values are based on the EU status values.
<br><br>


### Status table: Transmission of a notification<span id="statustabelle-uebermittlung">

| DöE status | final status?| status description |
| ----------------- | -|--------------------------------------------------------------------------------------------------------- |
| AWAITING_TRANSFER | no | The notice has been accepted and approved by the mediator. The further dispatch is being prepared. |

Once the transmission of a contract notice has been successfully completed, the status of the contract notice is set to AWAITING_TRANSFER and the mediation service begins with further steps in the processing of the sub- or above-threshold award. The following status tables list the possible statuses for the processing of the subthreshold and superthreshold award.
<br><br>

### Status table: Upper threshold award<span id="status-table-upper-threshold">

The following status combinations can be transmitted when requesting the status of an above-threshold award.

| TED status | DöE status |final status? |Status description | Publish on award platform? |
| ----------------- | -------------- | ---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | - |
| PENDING | PENDING | no | The announcement has been accepted by the eSender for further processing. Transmission of the announcement to TED and the announcement service is still pending. | still waiting |
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
| MANUALLY_REJECTED | NOT_SEND | yes | The announcement was either manually rejected by TED due to a legal check or by the switching service due to an error and is neither published by TED nor by the announcement service. This can be distinguished by the error message.     | no
| MANUALLY_REJECTED | PENDING | no | The announcement has been manually rejected by TED due to a legal check and will also be stopped in the announcement service shortly.                        | no |
| MANUALLY_REJECTED | ACCEPTED | no | The announcement was manually rejected by TED due to a legal check and will also be stopped in the announcement service shortly.                        | no |
| MANUALLY_REJECTED | PUBLISHED | no | The announcement was manually rejected by TED due to a legal check and will also be stopped in the announcement service shortly.                        | no |
| MANUALLY_REJECTED | STOPPED | yes | The announcement was manually rejected by TED due to a legal check and has also been stopped in the announcement service.                                | no
| REJECTED | INTERNAL_ERROR | no | An internal error has occurred. The support team will take a closer look at the announcement, the status will then change.                                 | still waiting |
| NOT_SEND | INTERNAL_ERROR | no | An internal error has occurred. The support team will take a closer look at the notification and the status will then change.


<br>

### Status table: Sub-threshold award<span id="statustabelle-unterschwelle">

The following status combinations can be transmitted when requesting the status of a subthreshold award.

| DöE status | final status | status description |
| ---------- | ----| --------------------------------------------------------------- |
| ACCEPTED | no | The announcement has been accepted by the announcement service. |
| REJECTED | yes | The announcement has been rejected by BKMS.                    |
| PROCESSING | no | The announcement is being processed by BKMS.                   |
| PUBLISHED | yes | The announcement has been published in the BKMS.                |
| STOPPED | yes | The announcement has been stopped in the announcement service.   |



<br>

## Structure of the transfer information<span id="transfer-info">
The transfer information is also contained in the delivery schema for each announcement. This information includes warnings and error messages from the switching service, the announcement service and TED.
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

A single warning and a single error message have the same structure. `source` indicates the system in which the warning or error occurred. The following values are possible in `source`:

| source | description |
| -------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| TED | Errors and warnings coming from TED, this includes both the http codes (5\*\*, 4\*\*) which are returned in the event of an unsuccessful transmission, as well as errors and warnings from the TED validation report. |
| BKMS | Errors that come from BKMS when BKMS returns an http code that represents an unsuccessful transmission (5\*\*, 4\*\*).                                                                                                |
| PRE_VALIDATION | Errors and warnings from the internal validation service.                                                                                                                                                                    |

The `description` contains the description of the warning or error message. The `path` indicates the position at which the error or warning occurred. The `rule` tag contains the name of the rule applied and `ruleContent` contains the rule actually applied.

Warnings and error messages from the announcement service and from TED are passed through unchanged.
<br><br>

## Lawfullness Warnings<span id="lawfullness">
In addition to errors, there are also warnings. These come exclusively from the EU rules and, unlike errors, do not prevent the notice from being accepted. TED has currently only defined one type of warning, so-called "lawfullness warnings". These will most likely be almost irrelevant for German notices, but are technically possible.

A lawfulness warning means that a manual check of a notice at TED is necessary. TED then checks the content of the announcement and decides whether it will be published or rejected and not published. TED has up to 5 days to make this decision. For this reason, notices with a Lawfullness Warning are only forwarded to the BKMS upon publication or 5 days after successful submission to TED.


