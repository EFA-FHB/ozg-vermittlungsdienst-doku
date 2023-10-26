### EfA Implementation Project "Access to Public Procurement".
## Documentation mediation service
[table of contents](/documentation/documentation.md)
<br>

## Status - and transfer information

Using the REST API of the switching service, all status and error information of an announcement can be queried. The status and error information of the BKMS and TED are regularly queried and stored by the switching service and eSender Hub, respectively, so the status and other information about an announcement is available for further retrieval at any time.
<br>

## Content
- Endpoints to query status and transfer information](#endpoints).
- Structure of status information](#info-structure)
    - [Status table: transfer of a notice](#status-table-transfer)
    - Status table: Upper threshold award](#status-table-upper-threshold).
    - Status table: Sub-threshold award](#status-table-sub-threshold)
- Structure of Transfer Information](#transfer-info)
- [Lawfullness Warnings](#lawfullness)


<br><br>

## Endpoints for querying status and transfer information<span id="endpoints">.
To query status and transfer information, the switch service provides `GET /v1/notices` endpoints for a list of data deliveries, `GET /v1/notices/status` endpoints for a list of data deliveries in a given time period, and `GET /v1/notices/{trackingcode}` endpoints for a single data delivery.

The switching service performs the status queries to BKMS and TED every three minutes. Therefore, querying the status information of the notices to the switching service at most every 5 minutes is reasonable.

The associated OpenAPI specification can be found at https://ozg-vermittlungsdienst.de/ and is available for download in JSON format at https://ozg-vermittlungsdienst.de/Vermittlungsdienst_REST-API.json.
<br><br>

## Status information structure<span id="info-structure">.
The endpoints to query the status information, return the status information for each announcement within the delivery schema as follows.

```
<?xml version="1.0" encoding="UTF-8"?>
<delivery>
	...
	<tedStatus>PENDING</tedStatus>.
	<tedStatusUpdate>2023-04-26T14:32:52.625Z</tedStatusUpdate>
	<doeStatus>AWAITING_TRANSFER</doeStatus>.
	<doeStatusUpdate>2023-04-26T14:32:52.625Z</doeStatusUpdate>
	<statusDescription>string</statusDescription>
	...
</delivery>
```

For both subthreshold and superthreshold notices, the status information includes the status of the Public Purchasing data service `doeStatus`, the last modification date of the DöE status `doeStatusUpdate`, and a description of the currently set status `statusDescription`.

For high-threshold notices, the TED status `tedStatus` with the last modification date `tedStatusUpdate` is also transmitted. The TED status values are based on the EU status values.
<br><br>


### Status table: Transmission of a notice<span id="statustabelle-uebermittlung">.

| status table | status description |
| ----------------- | --------------------------------------------------------------------------------------------------------- |
| AWAITING_TRANSFER | The notice has been accepted and acknowledged by the mediator. Further dispatch is being prepared. |

After the transmission of a notice has been successfully completed, the status of the notice is set to AWAITING_TRANSFER and the mediation service starts with further steps of processing the lower or upper threshold award. The following status tables list the possible statuses for processing the lower and upper threshold award.
<br><br>

### Status table: Upper threshold award<span id="status-table-upper-threshold">.

The following status combinations, can be transmitted when requesting the status of an Upper Threshold award.

| TED status | DöE status | status description |
| ----------------- | -------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| PENDING | The announcement has been accepted by the eSender for further processing. Transmission of the announcement to TED and to the announcement service is still pending. |
| NOT_SEND | INTERNAL_ERROR | An internal error has occurred. An appropriate support ticket will be created if necessary.                                                                               |
| PENDING | The announcement has been accepted by the eSender for further processing. Transmission of the announcement to TED and to the announcement service is still pending. |
| NO_RESPONSE | PENDING | Transmission to TED is attempted again. Transmission of the announcement to the announcement service is still pending.                                          |
| ACCEPTED | PENDING | The announcement has been accepted by TED, the transmission to the announcement service is still pending.                                                              |
| ACCEPTED | ACCEPTED | The announcement has been accepted by TED and the announcement service, but not yet published.                                                              |
| ACCEPTED | PUBLISHED | The notice has been accepted by TED but not yet published. The announcement has already been published in the announcement service.      |
| PUBLISHING | PENDING | The announcement is published in TED, the transmission to the announcement service is still pending.                                                            |
| PUBLISHING | ACCEPTED | The announcement is published in TED, the announcement has been accepted by the announcement service.                                                           |
| PUBLISHING | PUBLISHED | The announcement is published in TED, the announcement has been accepted by the announcement service.                                                        |
| STOPPED | NOT_SEND | The announcement was stopped in TED and will not be sent to the announcement service.                                                                             |
| STOPPED | PENDING | The announcement was stopped in TED and will not be sent to the announcement service.                                                                             |
| STOPPED | ACCEPTED | The announcement has been stopped in TED and will be stopped in the announcement service soon.                                                               |
| STOPPED | PUBLISHED | The announcement has been stopped in TED and will be stopped in the announcement service shortly.                                                               |
| STOPPED | STOPPED | The announcement has been stopped in TED as well as in the announcement service.                                                                                      |
| PUBLISHED | PENDING | The announcement has been published in TED, the transmission to the announcement service is still pending.                                                           |
| PUBLISHED | ACCEPTED | The announcement has been published in TED and accepted by the announcement service, but not yet published.                                                |
| PUBLISHED | PUBLISHED | The announcement has been published in TED and in the announcement service.                                                                                            |
| MANUALLY_REJECTED | NOT_SEND | The announcement was manually rejected by TED due to a legal review and was not sent to the announcement service.                              |
| MANUALLY_REJECTED | PENDING | The announcement has been manually rejected by TED due to a legal check and will be stopped in the announcement service shortly.                        |
| MANUALLY_REJECTED | ACCEPTED | The announcement has been manually rejected by TED due to a legal review and will be stopped in the announcement service shortly.                        |
| MANUALLY_REJECTED | PUBLISHED | The announcement has been manually rejected by TED due to a legal review and will be stopped in the announcement service shortly.                        |
| MANUALLY_REJECTED | STOPPED | The announcement has been manually rejected by TED due to a legal review and has also been stopped in the announcement service.                                |
| REJECTED | INTERNAL_ERROR | An internal error has occurred. An appropriate support ticket will be created if necessary.                                                                               |

<br>

### Status table: Sub-threshold award<span id="statustabelle-unterschwelle">

The following status combinations, can be transmitted when requesting the status of a sub-threshold award.

| DöE status | status description |
| ---------- | --------------------------------------------------------------- |
| ACCEPTED | The announcement has been accepted by the announcement service. |
| REJECTED | The announcement was rejected by BKMS.                    |
| PROCESSING | The announcement is processed by BKMS.                   |
| PUBLISHED | The announcement has been published in BKMS.                |
| STOPPED | The announcement has been stopped in the announcement service.   |



<br>

## Structure of transfer information<span id="transfer-info">.
The transfer information is also included for each announcement in the delivery schema. This information includes warnings and error messages from the switching service, the announcement service, and TED.
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

Within the transfer information `transferResponse` warnings `warnings` are listed separately from error messages `errors`. It is possible to receive multiple warnings and error messages as a response per announcement.

A single warning and a single error message have the same structure. Source indicates in which system the warning or error originated. The following values are possible in `source`:

| source | description |
| -------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| TED | Errors and warnings coming from TED, this includes both the http codes (5\*\*, 4\*\*) returned on unsuccessful submission and errors and warnings from the TED validation report. |
| BKMS | Errors coming from BKMS when BKMS returns an http code representing an unsuccessful submission (5\*\*, 4\*\*).                                                                                                |
| PRE_VALIDATION | errors and warnings from the internal validation service.                                                                                                                                                                    |

The `description` contains the description of the warning or error message. The `path` contains the position where the error or warning occurred. The `rule` tag contains the name of the rule applied and `ruleContent` the rule actually applied to it.

Warnings and error messages from the announcement service and TED are passed through unchanged.
<br><br>

## Lawfullness Warnings<span id="lawfullness">.
In addition to errors there are warnings. These come exclusively from the EU rules and, unlike errors, do not prevent the announcement from being accepted. TED has currently defined only one type of warnings, so called "Lawfullness Warnings". These will most likely be almost irrelevant for German announcements, but are technically possible.

A Lawfullness Warning means that a manual check of a notice at TED is necessary. TED then checks the content of the announcement and decides whether it will be published or rejected and not published. TED has up to 5 days to make this decision. For this reason, notices with a Lawfullness Warning will not be forwarded to BKMS until they are published or 5 days after they have been successfully submitted to TED.


