### Datenservice Öffentlicher Einkauf
[Inhaltsverzeichnis](/documentation/documentation.md)
<br>

# eForms-Validator

Unter der URL https://validator.ozg-vermittlungsdienst.de/ ist der eForms-Validierungsservice verfügbar.<br>
Mit Hilfe des Validierungsservices können Sie Ihre eForms-DE-Dokumente in den aktuell unterstützten Versionen vorab validieren, um Validierungsfehler bei der Übertragung von Bekanntmachungen an den Vermittlungsdienst zu vermeiden.
<br><br>
Sollten Sie den Validator selbst offline nutzen wollen (entweder als Java-Dependency oder als selbst gehosteten Webservice), ist der Code Open Source zu  finden unter https://projekte.kosit.org/eforms/validator-edition-eforms-de. 
<br><br>
Es wird eine Kombination aus einer XML-Schema-Validierung und einer Schematron-Validierung der Dokumente durchgeführt. Als Ergebnis wird ein Validierungsreport, der dem Aufbau des Validierungsreports aus dem Vermittlungsdienst entspricht, im JSON-Format zurückgegeben.
<br><br>
Die zugehörige OpenAPI-Spezifikation zum Validator finden Sie unter https://validator.ozg-vermittlungsdienst.de/ und steht Ihnen im JSON-Format zum Download unter https://validator.ozg-vermittlungsdienst.de/eForm-DE_validation_service_REST-API.json bereit.
<br><br>
Die Nutzung des Services ist ohne vorherige Registrierung oder Anmeldung möglich.
Übermittelte Dokumente und die Validierungsreports werden weder im System gespeichert noch weitergleitet.
Bitte beachten Sie, dass der Service ausschließlich für Entwicklungsarbeiten gedacht ist und auch nur zu diesem Zweck genutzt werden sollte. Es wird keine Garantie für Verfügbarkeit und Reaktionszeit übernommen.
