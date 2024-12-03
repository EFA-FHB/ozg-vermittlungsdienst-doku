### Data service public procurement
[Table of contents](/documentation/documentation.md)
<br>

# eForms support
Different eForms versions are currently supported and processed according to the following example. In future, both subthreshold and above-threshold notices will be accepted by the Vermittlungsdienst exclusively in eForms DE format.

<br>

*Overview of existing eForms-DE versions and the associated technical artifacts and tools:*
| eForms-DE-Standard | KoSIT-Schematron | KoSIT-Codelists | SDK-DE | eForms-DE-Offline-Validator | Accepted from | Accepted until |
|--------------------|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|------------|------------|
| [eForms-DE 2.0](https://xeinkauf.de/app/uploads/2024/02/specification-eforms-de-v1.2.0.pdf) | [0.9.1](https://projekte.kosit.org/eforms/eforms-de-schematron/-/releases/v0.9.1) | [2024-09-02](https://projekte.kosit.org/eforms/eforms-de-codelist/-/releases/v2024-09-02) | [1.12.1](https://gitlab.opencode.de/OC000008125155/SDK-eforms-de/-/tags/1.12.1) | [1.2.6](https://projekte.kosit.org/eforms/validator-edition-eforms-de/-/releases/1.2.6) supports eForms-DE 1.1.0, 1.2.0, 2.0.0 | 01.11.2024 | 18.07.2025 |
| eForms-DE 1.2](https://xeinkauf.de/app/uploads/2024/02/specification-eforms-de-v1.2.0.pdf) | [0.8.4](https://projekte.kosit.org/eforms/eforms-de-schematron/-/releases/v0.8.4) | [2024-02-06](https://projekte.kosit.org/eforms/eforms-de-codelist/-/releases/v2024-02-06) | [1.2.0_1.10.3](https://gitlab.opencode.de/OC000008125155/SDK-eforms-de/-/tags/SDK-DE_1.2.0_1.10.3_0) | [1.0.15](https://github.com/EFA-FHB/eforms-validator-core/releases/tag/1.0.15) supports eForms-DE 1.1.0 & 1.2.0 | 08.07.2024 | 30.04.2025 |
| eForms-DE 1.1](https://xeinkauf.de/app/uploads/2023/08/specification-eforms-de-v1.1.0.pdf) | [0.7.2](https://projekte.kosit.org/eforms/eforms-de-schematron/-/releases/v0.7.2) | [2023-07-07](https://projekte.kosit.org/eforms/eforms-de-codelist/-/releases/v2023-07-07) | [1.1.0_1.7.3_1](https://gitlab.opencode.de/OC000008125155/SDK-eforms-de/-/tags/1.1.0_1.7.3_1) | [1.0.12](https://github.com/EFA-FHB/eforms-validator-core/releases/tag/1.0.12) supports eForms-DE 1.0.1 & 1.1.0 | 13.09.2023 | 30.04.2025 |

## eForms validation
All notices are validated when they are sent to the Vermittlungsdienst before they are accepted by the system. Validation is carried out using a combination of XML schema validation and Schematron validation. As a result, a validation report is returned in JSON format.

One option for offline validation, as performed by the Vermittlungsdienst, is the open source validator: https://projekte.kosit.org/eforms/validator-edition-eforms-de

### Validation blacklist

National tailoring results in differences between values permitted in the EU and nationally, for example in code lists and the customizationID: certain EU rules must therefore be skipped in order to validate valid documents according to German tailoring.

The following rules should be ignored:

| Content | BT Field | Rule to be ignored |
| ----------------------------- | -------- | ------------------ |
| CustomizationID | BR-OPT-00002-0052 |
| buyer-contracting-type.gc | BT-740 | BR-BT-00740-0052 |
| buyer-legal-type.gc | BT-11 | BR-BT-00011-0052 |
| criterion-exclusion-ground.gc | BT-67 | BR-BT-00067-0104 |
| gpp-criteria.gc | BT-165 | BR-BT-00165-0052 |
| missing-info-submission.gc | BT-771 | BR-BT-00001-0155 |
| procurement-procedure-type.gc | BT-105 | BR-BT-00105-0052 |
| received-submission-type.gc | BT-760 | BR-BT-00760-0052 |
| social-objective.gc | BT-775 | BR-BT-00775-0051 |



