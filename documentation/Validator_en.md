
[Table of contents](/documentation/documentation.md)
<br>

### eForms validation service

The eForms validation service is available at the URL https://validator.ozg-vermittlungsdienst.de/.<br>
The validation service can be used to validate eForms-DE documents in the currently supported versions in advance in order to avoid validation errors when transmitting notices to the Vermittlungsdienst.
<br><br>
The validation service can also be used offline either as a Java dependency or as a self-hosted web service. The code is open source and can be found at https://projekte.kosit.org/eforms/validator-edition-eforms-de.
<br><br>
A combination of XML schema validation and Schematron validation of the documents is performed. As a result, a validation report is returned in JSON format, which corresponds to the structure of the validation report from the Vermittlungsdienst.
<br><br>
The corresponding OpenAPI specification for the validation service can be found here https://validator.ozg-vermittlungsdienst.de/ and is available for download in JSON format at https://validator.ozg-vermittlungsdienst.de/eForm-DE_validation_service_REST-API.json.
<br><br>
The service can be used without prior registration or login.
Transmitted documents and the validation reports are neither stored in the system nor forwarded.
Please note that the service is intended exclusively for development work and should only be used for this purpose. No guarantee is given for availability and response time.

