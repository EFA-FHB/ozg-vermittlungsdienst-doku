**EfA Implementation Project "Access to Public Procurement "**.
### Documentation mediation service
[Table of contents](/documentation/Documentation.md)
<br>

# eForms Validator

The eForms validation service is available at the URL https://validator.ozg-vermittlungsdienst.de/.<br>
The validation service allows you to pre-validate your eForms-DE version 1.0 and 1.1 documents to avoid validation errors when sending notices to the switching service.
<br><br>
Should you wish to use the validator offline yourself (either as a Java dependency or as a self-hosted web service) the code is open source and can be found at https://github.com/EFA-FHB/eforms-validator-core.
<br><br>
A combination of XML schema validation and Schematron validation of the documents is performed. As a result, a validation report corresponding to the structure of the validation report from the mediation service is returned in JSON format.
<br><br>
The associated OpenAPI specification for the validator can be found at https://validator.ozg-vermittlungsdienst.de/ and is available for download in JSON format at https://validator.ozg-vermittlungsdienst.de/eForm-DE_validation_service_REST-API.json.
<br><br>
The service can be used without prior registration or login.
Submitted documents and the validation reports are neither stored in the system nor forwarded.
Please note that the service is intended for development work only and should be used for this purpose only. No guarantee is given for availability and response time.
