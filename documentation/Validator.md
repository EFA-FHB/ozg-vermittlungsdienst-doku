
[Inhaltsverzeichnis](/documentation/documentation.md)
<br>

# eForms-Validierungsservice

Unter der URL https://validator.ozg-vermittlungsdienst.de/ ist der eForms-Validierungsservice verfügbar.<br>
Mit Hilfe des Validierungsservices können eForms-DE-Dokumente in den aktuell unterstützten Versionen vorab validiert werden, um Validierungsfehler bei der Übertragung von Bekanntmachungen an den Vermittlungsdienst zu vermeiden.
<br><br>
Der Validierungsservice kann auch offline entweder als Java-Dependency oder als selbst gehosteten Webservice genutzt werden. Der Code ist Open Source und zu finden unter https://projekte.kosit.org/eforms/validator-edition-eforms-de. 
<br><br>
Es wird eine Kombination aus einer XML-Schema-Validierung und einer Schematron-Validierung der Dokumente durchgeführt. Als Ergebnis wird ein Validierungsreport, der dem Aufbau des Validierungsreports aus dem Vermittlungsdienst entspricht, im JSON-Format zurückgegeben.
<br><br>
Die zugehörige OpenAPI-Spezifikation zum Validierungsservice ist hier https://validator.ozg-vermittlungsdienst.de/ zu finden und steht im JSON-Format zum Download unter https://validator.ozg-vermittlungsdienst.de/eForm-DE_validation_service_REST-API.json bereit.
<br><br>
Die Nutzung des Services ist ohne vorherige Registrierung oder Anmeldung möglich.
Übermittelte Dokumente und die Validierungsreports werden weder im System gespeichert noch weitergleitet.
Es ist zu beachten, dass der Service ausschließlich für Entwicklungsarbeiten gedacht ist und auch nur zu diesem Zweck genutzt werden sollte. Es wird keine Gewähr für Verfügbarkeit und Reaktionszeit übernommen.

