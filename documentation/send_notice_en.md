### EfA Implementation Project "Access to Public Procurement".
## Documentation Mediation Service
[table of contents](/documentation/documentation.md)
<br>

## Send a notice

To send an announcement to the mediation service, you must use the provided REST API, for which credentials are required. For how to request credentials and how to authenticate to the API, see the [Connection to the mediation service](/documentation/Connection_to_mediator.md) section.
<br>
 
The POST /v2/notices endpoint is used to send an announcement. The description of the endpoint can be found at https://ozg-vermittlungsdienst.de/q/swagger-ui/#/Lieferungen/createDeliveryWithMetadata. The endpoint expects the following parameters in the request body:
```
`notice`: The XML eForms document

`authorEmail`: The email address of the author of a notice. This will be passed to TED in case of pan-European publication.

`buyerPartyIdentification`, `buyerElectronicAddress`, `procedureIdentifier`: Optional parameters which allow to find the submitted notice in the notice service via the Peppol network.
```
In case of successful delivery, the response code `202` means that the announcement has been received and is now being processed.

To track the notice, you will receive a tracking code and the following information in the response after posting:
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

The tracking code can be used to query the status of the particular notice, via the `GET /v1/notices/{trackingcode}` endpoint.

Alternatively, either the status of all notices submitted can be queried via `GET /v1/notices`, or all status changes based on their time in a time span to be specified can be queried via `GET /v1/notices/status`. Both endpoints are paginated.
>**Note** <br>
>The `GET /v1/notices/status` is recommended, as this is the most efficient way to retrieve the current status information.

For the meaning of the other response codes, see https://ozg-vermittlungsdienst.de/q/swagger-ui/#/Lieferungen/createDeliveryWithMetadata.

