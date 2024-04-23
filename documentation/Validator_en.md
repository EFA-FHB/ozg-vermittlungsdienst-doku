### Data service public procurement
[Table of contents](/documentation/documentation.md)
<br>

### eForms Validator

The eForms validation service is available at the URL https://validator.ozg-vermittlungsdienst.de/.<br>
You can use the validation service to validate your eForms-DE documents of version eForms-DE 1.1 and 1.2 in advance in order to avoid validation errors when transmitting notices to the Vermittlungsdienst.
<br><br>
If you want to use the validator offline yourself (either as a Java dependency or as a self-hosted web service), the code is open source and can be found at https://github.com/EFA-FHB/eforms-validator-core.
<br><br>
A combination of XML schema validation and Schematron validation of the documents is performed. As a result, a validation report is returned in JSON format, which corresponds to the structure of the validation report from the Vermittlungsdienst.
<br><br>
The corresponding OpenAPI specification for the validator can be found at https://validator.ozg-vermittlungsdienst.de/ and is available for download in JSON format at https://validator.ozg-vermittlungsdienst.de/eForm-DE_validation_service_REST-API.json.
<br><br>
The service can be used without prior registration or login.
Transmitted documents and validation reports are neither stored in the system nor forwarded.
Please note that the service is intended exclusively for development work and should only be used for this purpose. No guarantee is given for availability and response time.
