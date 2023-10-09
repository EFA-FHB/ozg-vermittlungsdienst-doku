### EfA Implementation Project "Access to Public Procurement".
## Documentation Mediation Service
[table of contents](/documentation/documentation.md)
<br>

## eForms support
Currently, different eForms versions are supported and processed according to the following example. In the future, both subthreshold and superthreshold notices will be accepted by the switching service in eForms-DE format only.

<br>

*Overview of existing eForms-DE versions and associated technical artifacts and utilities:*
| eForms-DE Standard | KoSIT Schematron | KoSIT Codelists | SDK-DE | eForms-DE Offline Validator | will be accepted until |
|--------------------|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|------------|
| [eForms-DE 1.0.1](https://xeinkauf.de/app/uploads/2023/03/specification-eforms-de-v1.0.1.pdf) | [0.5.3](https://projekte.kosit.org/eforms/eforms-de-schematron/-/releases/v0.5.3) | [2023-05-17](https://projekte.kosit.org/eforms/eforms-de-codelist/-/releases/v2023-05-17) | [1.0.1_1.5.3_20230727](https://gitlab.opencode.de/OC000008125155/SDK-eforms-de/-/tree/SDK-DE_1.0.1_1.5.3_20230727?ref_type=tags) | [1.0.6](https://github.com/EFA-FHB/eforms-validator-core/releases/tag/1.0.6) supports eForms-DE 1.0.1 & 1.1.0 | 31.01.2024 |
| [eForms-DE 1.1](https://xeinkauf.de/app/uploads/2023/08/specification-eforms-de-v1.1.0.pdf) | [0.6.2](https://projekte.kosit.org/eforms/eforms-de-schematron/-/releases/v0.6.2) | [2023-07-07](https://projekte.kosit.org/eforms/eforms-de-codelist/-/releases/v2023-07-07) | [1.1.0_1.7.0](https://gitlab.opencode.de/OC000008125155/SDK-eforms-de/-/tags/SDK-DE_1.1.0_1.7.0) | [1.0.6](https://github.com/EFA-FHB/eforms-validator-core/releases/tag/1.0.6) supports eForms-DE 1.0.1 & 1.1.0 | 11.05.2024 |


<br>

*Following versions can be submitted to the switching service until 10/25/2023:*.

| Version | Switching service | External validator | eSender hub | BKMS | TED |
| ------- | -------- | ------------------ | --------- | ----- | ---- |
| eForms-EU 0.1.1 | yes, but only for sub-threshold award | no | no | yes, but only for sub-threshold award | no |
| eForms-EU 1.0 | yes, but only for sub-threshold award | no | no | yes, but only for sub-threshold award | no |
| eForms-EU 1.5 | only in the preview environment, NOT in Prod | yes | yes | no | yes, until 31.01.2024 |
| eForms-DE 1.0.1 (schematron 0.5.2) | yes | yes | yes | yes, after conversion in eSender-Hub to eForms-EU 1.5.1, until 31.01.2024 |
| eForms-DE 1.1 | planned support in KW37 2023 | planned support in KW37 2023 | yes | planned support in KW37 2023 | yes, after conversion in eSender-Hub to eForms-EU 1.7.0, planned support in KW37 2023, until 11.05.2024 |

<br>

*Following versions can be submitted in the Prod Environment in the switching service from 25.10.2023:*.

| Version | Switching Service | External validator | eSender Hub | BKMS | TED |
| ------------------------------------- | ------------------------------- | ------------------ | ---------- | --------- | ------------ |
| eForms-EU 0.1.1 | yes, but only for sub-threshold award | no | yes | yes, but only for sub-threshold award | no |
| eForms-EU 1.0 | yes, but only for sub-threshold award | no | yes | yes, but only for sub-threshold award | no |
| eForms-EU 1.5 | no | yes | yes | no | yes, until 31.01.2024 |
| eForms-DE 1.0.1 (schematron 0.5.2) | yes | yes | yes | yes, after conversion in eSender-Hub to eForms-EU 1.5.2, until 31.01.2024 |
| eForms-DE 1.1 (Recommended version) | yes | yes | yes | yes, after conversion in eSender-Hub to eForms-EU 1.7.0, until 11.05.2024 |

Please note: After 10/25/2023, only eForms-DE versions will be supported in the production system. We recommend to use version eForms-DE 1.1.

## eForms validation
All notices are validated when they are submitted to the switching service before being accepted by the system. Validation is performed using a combination of XML schema validation and Schematron validation. As a result, a validation report is returned in JSON format.

An option for offline validation, as performed by the switching service, is provided by the open source validator https://github.com/EFA-FHB/eforms-validator-core.

### Validation Blacklist

Due to national tailoring, differences arise between values permitted in the EU and nationally, e.g. for code lists and the customizationID: Therefore, certain EU rules must be skipped if valid documents are to be validated according to German tailoring.

The following rules should be ignored:

| Content | BT Field | Rule to be ignored |
| ----------------------------- | -------- | ------------------ |
| CustomizationID | | BR-OPT-00002-0052 |
| buyer-contracting-type.gc | BT-740 | BR-BT-00740-0052 |
| buyer-legal-type.gc | BT-11 | BR-BT-00011-0052 |
| criterion-exclusion-ground.gc | BT-67 | BR-BT-00067-0104 |
| gpp-criteria.gc | BT-165 | BR-BT-00165-0052 |
| missing-info-submission.gc | BT-771 | BR-BT-00001-0155 |
| procurement-procedure-type.gc | BT-105 | BR-BT-00105-0052 |
| received-submission-type.gc | BT-760 | BR-BT-00760-0052 |
| social-objective.gc | BT-775 | BR-BT-00775-0051 |




