### Datenservice Öffentlicher Einkauf
[Inhaltsverzeichnis](/documentation/documentation.md)
<br>

# Einsenden einer Bekanntmachung

Um eine Bekanntmachung an den Vermittlungsdienst zu senden, muss die zur Verfügung gestellte REST-API verwendet werden, für die Zugangsdaten benötigt werden. Wie die Zugangsdaten beantragt und wie bei der API Authentifizierung erfolgt, ist hier beschrieben [Anbindung an den Vermittlungsdienst](/documentation/Connection_to_mediator.md).
<br>
 
Für die Übersendung einer Bekanntmachung wird der Endpoint POST /v2/notices verwendet. Die Beschreibung des Endpoints steht hier https://ozg-vermittlungsdienst.de/q/swagger-ui/#/Lieferungen/createDeliveryWithMetadata. Der Endpoint erwartet folgende Parameter im Request-Body:
```
`notice`: Das XML eForms Dokument

`authorEmail`: Die E-Mail-Adresse des Verfassers einer Bekanntmachung. Diese wird bei europaweiter Veröffentlichung an TED weitergegeben.

`buyerPartyIdentification`, `buyerElectronicAddress`, `procedureIdentifier`: Optionale Parameter, welche es ermöglichen, die eingelieferte Bekanntmachung im Bekanntmachungsservice über das Peppol Netzwerk zu finden.

`publishToTed': Optionaler Parameter. Gibt an, ob die Bekanntmachung an TED übermittelt werden soll. Gilt nur für die Formulare E1 bis E4. Falls der Parameter für 1-40 auf false gesetzt wird, wird dies ignoriert. Wenn dieser Parameter nicht befüllt ist, wird E1 standardmäßig an TED versendet, E2-E4 nicht. Dieser Parameter beeinflusst die Übermittlung an den Bekanntmachungsservice nicht. Wenn E1-E4 Formulare an TED versendet werden, erfolgt eine Übermittlung an den Bekanntmachungsservice unmittelbar ohne 48h Verzögerung.
``` 
Bei erfolgreicher Einlieferung bedeutet der Response-Code `202`, dass die Bekanntmachung entgegengenommen wurde und nun weiter vearbeitet wird. 

Zur Nachverfolgung der Bekanntmachung wird in der Response nach der Einlieferung ein Trackingcode mit folgenden Informationen geliefert:
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

Mit dem Trackingcode kann der Status der jeweiligen Bekanntmachung über den Endpunkt `GET /v1/notices/{trackingcode}`, abgefragt werden. 

Alternativ kann entweder der Status aller eingelieferten Bekanntmachungen abgefragt werden über `GET /v1/notices` oder es können alle Statusänderungen basierend auf ihrem Zeitpunkt in einer anzugebenden Zeitspanne abgefragt werden über `GET /v1/notices/status`. Beide Endpunkte sind paginiert. 
>**Hinweis** <br>
>Der `GET /v1/notices/status` wird empfohlen, da so die aktuellen Statusinformationen am effizientesten abgefragt werden können.

Die Bedeutung der weiteren Response-Codes entnehmen Sie https://ozg-vermittlungsdienst.de/q/swagger-ui/#/Lieferungen/createDeliveryWithMetadata.


