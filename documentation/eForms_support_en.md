### Data service public procurement
[Table of contents](/documentation/documentation.md)
<br>

# eForms support
Different eForms versions are currently supported and processed according to the following example. In future, both subthreshold and above-threshold notices will be accepted by the Vermittlungsdienst exclusively in eForms-DE format.

<br>

*Overview of existing eForms-DE versions and the associated technical artifacts and tools:*
| eForms-DE Standard | KoSIT Schematron | KoSIT Codelists | SDK-DE | eForms-DE Offline Validator | will be accepted until |
|--------------------|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|------------|
| [eForms-DE 1.0.1](https://xeinkauf.de/app/uploads/2023/03/specification-eforms-de-v1.0.1.pdf) | [0.5.3](https://projekte.kosit.org/eforms/eforms-de-schematron/-/releases/v0.5.3) | [2023-05-17](https://projekte.kosit.org/eforms/eforms-de-codelist/-/releases/v2023-05-17) | [1.0.1_1.5.3_20230727](https://gitlab.opencode.de/OC000008125155/SDK-eforms-de/-/tree/SDK-DE_1.0.1_1.5.3_20230727?ref_type=tags) | [1.0.6](https://github.com/EFA-FHB/eforms-validator-core/releases/tag/1.0.6) supports eForms-DE 1.0.1 & 1.1.0 | Preview: 15.01.2024, Staging: 22.1.2024, Prod: 31.01.2024 |
| [eForms-DE 1.1](https://xeinkauf.de/app/uploads/2023/08/specification-eforms-de-v1.1.0.pdf) | [0.6.2](https://projekte.kosit.org/eforms/eforms-de-schematron/-/releases/v0.6.2) | [2023-07-07](https://projekte.kosit.org/eforms/eforms-de-codelist/-/releases/v2023-07-07) | [1.1.0_1.7.0](https://gitlab.opencode.de/OC000008125155/SDK-eforms-de/-/tags/SDK-DE_1.1.0_1.7.0) | [1.0.6](https://github.com/EFA-FHB/eforms-validator-core/releases/tag/1.0.6) supports eForms-DE 1.0.1 & 1.1.0 | Preview: CW 16-17, Staging: CW 17-18, Prod: approx. end of CW 19 |
| [eForms-DE 1.1](https://xeinkauf.de/app/uploads/2023/08/specification-eforms-de-v1.1.0.pdf) | [0.7.0](https://projekte.kosit.org/eforms/eforms-de-schematron/-/releases/v0.7.0) | [2023-07-07](https://projekte.kosit.org/eforms/eforms-de-codelist/-/releases/v2023-07-07) | [1.1.0_1.7.2](https://gitlab.opencode.de/OC000008125155/SDK-eforms-de/-/tags/SDK-DE_1.1.0_1.7.2) | [1.0.11](https://github.com/EFA-FHB/eforms-validator-core/releases/tag/1.0.11) supports eForms-DE 1.0.1 & 1.1.0 | Preview: CW 16-17, Staging: CW 17-18, Prod: approx. end of CW 19 |
| eForms-DE 1.2 <br>*(expected to be available from February 2024)* | | | | | Prod: 01.12.2024|


<br>

*The following versions can be submitted in the Prod Environment in the Vermittlungsdienst from 25.10.2023:*

| Version | Vermittlungsdienst | External validator | eSender-Hub | BKMS | TED |
| ------------------------------------- | ------------------------------- | ------------------ | ---------- | --------- | ------------ |
| eForms-EU 0.1.1 | yes, but only for sub-threshold awards | no | yes | yes, but only for sub-threshold awards | no |
| eForms-EU 1.0 | yes, but only for sub-threshold awards | no | yes | yes, but only for sub-threshold awards | no |
| eForms-EU 1.5 | no | yes | yes | no | yes, until 31.01.2024 |
| eForms-DE 1.0.1 (schematron 0.5.2) | yes, until 31.01.2024 | yes | yes | yes | yes, after conversion in the eSender Hub to eForms-EU 1.5.2, until 31.01.2024 |
| eForms-DE 1.1 (recommended version) | yes, until 11.05.2024 | yes | yes | yes | yes, after conversion in the eSender Hub to eForms-EU 1.7.0, until 11.05.2024 |

Please note: After 25.10.2023, only eForms-DE versions will be supported in the production system. We recommend using the eForms-DE 1.1 version.

## eForms validation
All notices are validated when they are transmitted to the Vermittlungsdienst before they are accepted by the system. Validation is carried out using a combination of XML schema validation and Schematron validation. As a result, a validation report is returned in JSON format.

The open source validator https://github.com/EFA-FHB/eforms-validator-core offers an option for offline validation in the same way as the Vermittlungsdienst.

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




