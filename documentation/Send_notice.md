### EfA-Umsetzungsprojekt "Zugang zur öffentlichen Vergabe"
## Dokumentation Vermittlungsdienst
[Inhaltsverzeichnis](/documentation/Documentation.md)
<br>

# Eine Bekanntmachung senden

Um eine Bekanntmachung an den Vermittlungsdienst zu senden, muss die zur Verfügung gestellt REST-API verwendet werden, für die Zugangsdaten benötigt werden. Wie Sie die Zugangsdaten beantragen und wie Sie sich bei der API authentifizeren können entnehmen Sie dem Bereich [Anbindung an den Vermittlungsdienst](/documentation/Connection_to_mediator.md).
<br>
 
Für die Übersendung einer Bekanntmachung wird der Endpoint POST /v2/notices verwendet. Die Beschreibung des Endpoints finden Sie unter https://ozg-vermittlungsdienst.de/q/swagger-ui/#/Lieferungen/createDeliveryWithMetadata. Der Endpoint erwartet folgende Parameter im Request Body:
```
`notice`: Das XML eForms Dokument

`authorEmail`: Die E-Mail-Adresse des Verfassers einer Bekanntmachung. Diese wird bei europaweiter Veröffentlichung an TED weitergegeben.

`buyerPartyIdentification`, `buyerElectronicAddress`, `procedureIdentifier`: Optionale Parameter, welche es ermöglichen, die eingelieferte Bekanntmachung im Bekanntmachungsservice über das Peppol Netzwerk zu finden. 
``` 
Bei erfolgreicher Einlieferung bedeutet der Response Code `202`, dass die Bekanntmachung entgegengenommen wurde und nun weiter vearbeitet wird. 

Zur Nachverfolgung der Bekanntmachung erhalten Sie in der Response nach der Einlieferung einen Trackingcode und folgende Informationen:
```
<delivery status="AWAITING_TRANSFER" created="2023-06-25T23:47:46.470Z" lastUpdated="2023-06-25T23:47:46.470Z">
	<tracking-code>3446e1ee-5917-4d31-b623-81ddfb038d82</tracking-code>
	<notice-id>3fa85f64-5717-4562-b3fc-2c963f66afa6</notice-id>
	<notice-type>string</notice-type>
	<vergabeId>string</vergabeId>
	<vergabenummer>V0505/2021</vergabenummer>
	<description>string</description>
	<error>content too large</error>
</delivery>
```

Mit dem Trackingcode kann der Status der jeweiligen Bekanntmachung, über den Endpunkt `GET /v1/notices/{trackingcode}`, abgefragt werden. 

Alternativ kann entweder der Status aller eingelieferten Bekanntmachungen abgefragt werden über `GET /v1/notices` oder alle Statusänderungen basierend auf ihrem Zeitpunkt in einer anzugebenden Zeitspanne abgefragt werden über `GET /v1/notices/status`. Beide Endpunkte sind paginiert. 
>**Hinweis** <br>
>Der `GET /v1/notices/status` wird empfohlen, da so die aktuellen Statusinformationen am effizientesten abgefragt werden können.

Die Bedeutung der weiteren Response Codes entnehmen Sie https://ozg-vermittlungsdienst.de/q/swagger-ui/#/Lieferungen/createDeliveryWithMetadata.

