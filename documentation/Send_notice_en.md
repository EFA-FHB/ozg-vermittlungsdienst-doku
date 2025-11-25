### Data service public procurement
[Table of contents](/documentation/documentation.md)
<br>

# Submitting an announcement

To send an announcement to the Vermittlungsdienst, the REST API provided must be used, for which access data is required. How to request the access data and how to authenticate with the API is described here [Connection to the Vermittlungsdienst](/documentation/Connection_to_mediator.md).
<br>
 
The POST /v2/notices endpoint is used to send an announcement. The description of the endpoint can be found here https://ozg-vermittlungsdienst.de/q/swagger-ui/#/Lieferungen/createDeliveryWithMetadata. The endpoint expects the following parameters in the request body:
```
`notice`: The XML eForms document

`authorEmail`: The e-mail address of the author of a notice. This is forwarded to TED in the case of Europe-wide publication.

`buyerPartyIdentification`, `buyerElectronicAddress`, `procedureIdentifier`: Optional parameters which enable the submitted announcement to be found in the announcement service via the Peppol network.

`publishToTed`: Optional parameter. Specifies whether the notice should be sent to TED. Only applies to forms E1 to E4. If the parameter for 1-40 is set to false, this is ignored. If this parameter is not filled, E1 is sent to TED by default, E2-E4 are not. This parameter does not affect the transmission to the announcement service. If E1-E4 forms are sent to TED, transmission to the announcement service takes place immediately.
```
In the event of successful submission, the response code `202` means that the notice has been received and is now being processed further.

To track the notice, a tracking code with the following information is provided in the response after posting:
```
<delivery status="AWAITING_TRANSFER" created="2023-06-25T23:47:46.470Z" lastUpdated="2023-06-25T23:47:46.470Z">
	<tracking-code>3446e1ee-5917-4d31-b623-81ddfb038d82</tracking-code>
	<notice-id>3fa85f64-5717-4562-b3fc-2c963f66afa6</notice-id>
	<notice-type>string</notice-type>
	<awardId>string</awardId>
	<award number>V0505/2021</award number>
	<description>string</description>
	<error>content too large</error>
</delivery>
```

The tracking code can be used to query the status of the respective notice via the endpoint `GET /v1/notices/{trackingcode}`.

Alternatively, either the status of all notices submitted can be queried via `GET /v1/notices` or all status changes can be queried based on their time in a specified period of time via `GET /v1/notices/status`. Both endpoints are paginated.
>**Note** <br>
>The `GET /v1/notices/status` is recommended, as this is the most efficient way to query the current status information.

The meaning of the other response codes is documented here: https://ozg-vermittlungsdienst.de/q/swagger-ui/#/Lieferungen/createDeliveryWithMetadata.


