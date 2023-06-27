### EfA-Umsetzungsprojekt "Zugang zur öffentlichen Vergabe"
## Dokumentation Vermittlungsdienst
[Inhaltsverzeichnis](/documentation/documentation.md)
<br>

# Eine Bekanntmachung senden

Um eine Bekanntmachung an den Vermittlungsdienst zu senden muss man die zur Verfügung gestellt API verwenden. Zur Verwendung der API benötigt man Zugansdaten. Wie Sie die Zugangsdaten beantragen und wie Sie sich bei der API authetifizeren können entnehmen Sie dem Bereich [Anbindung an den Vermittlungsdienst](/documentation/Connection_to_mediator.md).
<br><br>

Für die Übersendung einer Bekanntmachung wird der Endpoint POST /v2/notices verwendet. Die Beschreibung des Endpoints finden Sie unter https://ozg-vermittlungsdienst.de/q/swagger-ui/#/Lieferungen/createDeliveryWithMetadata. Der Endpoint erwartet folgende Parameter im Request Body:

*notice*<br>
Die Bekanntmachung im eForms-Format
<br><br>

*authorEmail*<br>
E-Mail-Adresse des Verfassers einer Bekanntmachung. Diese wird bei europaweiter Veröffentlichung an TED weitergegeben.
<br><br>

Die Parameter *buyerPartyIdentification*, *buyerElectronicAddress*, *procedureIdentifier* sind optional. Durch die Bereitstellung dieser Informationen an BKMS ermöglicht es den Beschaffungssystemen, über peppol nach Ausschreibungen zu suchen und sich darauf zu bewerben.
<br><br>
Der Response code 202 bedeutet die Bekanntmachung wurde entgegengenommen und wird nun weiter vearbeitet. Zur Nachverfolgung der Bekanntmachung erhalten Sie im Response eine Tracking-Nummer und folgende Informationen:<br>
`<delivery status="AWAITING_TRANSFER" created="2023-06-25T23:47:46.470Z" lastUpdated="2023-06-25T23:47:46.470Z">
	<tracking-code>3446e1ee-5917-4d31-b623-81ddfb038d82</tracking-code>
	<notice-id>3fa85f64-5717-4562-b3fc-2c963f66afa6</notice-id>
	<notice-type>string</notice-type>
	<vergabeId>string</vergabeId>
	<vergabenummer>V0505/2021</vergabenummer>
	<description>string</description>
	<error>content too large</error>
</delivery>`

Die Bedeutung der weiteren Response Codes entnehmen Sie https://ozg-vermittlungsdienst.de/q/swagger-ui/#/Lieferungen/createDeliveryWithMetadata.

