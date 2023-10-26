### EfA Implementation Project "Access to Public Procurement
# Releases

October 2023

- [Release for Notice-Viewer - PDF documents + synchronous calls](#Release-for-Notice-Viewer-PDF-documents-+-synchronous-calls)
- [Release for self-service portal-portal-account,-registration-form-for-a-separate-switchboard-account](#release-for-self-service-portal-portal-account,-registration-form-for-a-separate-switchboard-account)

September 2023

- [Release for RequestedPublicationDate Fix + Notice Viewer - Mediation Service, eSender Hub, Notice Viewer](#Release-for-RequestedPublicationDate-Fix-+-Notice-Viewer-Mediation-Service,-eSender-Hub,-Notice-Viewer)
- [Release for eForms-DE 1.1 - Mediation Service and eSender Hub](#Release-for-eForms-DE-1.1-Mediation-Service-and-eSender-Hub)

August 2023

- [Release Offline-Validator for eForms-DE 1.0.1 and 1.1.0](#Release-Offline-Validator-for-eForms-DE-1.0.1-and-1.1.0)

June 2023
  
- [Production Release June - Mediation Service & eSender Hub](#Production-Release-June-Mediation-Service-&-eSender-Hub)

May 2023

- [Preview Release May - Switching Service & Validator Web Service](#Preview-Release-May-Switching-Service-&-Validator-Webservice)

<a id=release-for-notice-viewer-PDF-documents-+-synchronous-calls></a>.
## release-for-notice-viewer-PDF-documents+-synchronous-calls.
| environment notification service | period | status |
|------------|-----------------------------|----------------|
| preview | 10/17/2023 | published |
| staging | 18.10.2023 | published |
| Production | 20.10.2023 | published |

> **Note** <br>
> When using this API endpoint, we would like to draw your attention to the fact that performance is currently still being optimized. Please take this into account with intensive request frequency and plan for appropriate tolerances in your workflows. We are actively working on improvements and thank you for your understanding.

Status: Published on 20.10.2023 <br>
<details>
<summary>Release Notes</summary>

### Notice Viewer
>**environments** <br>
> Preview https://viewer.preview-ozg-vermittlungsdienst.de <br>
> Staging https://viewer.staging-ozg-vermittlungsdienst.de<br>
> Production https://viewer.ozg-vermittlungsdienst.de<br>

- Backward compatibility with original `/view` endpoint.
- New endpoints for asynchronous HTML and PDF generation, same behavior as previous `view` endpoint, response is returned immediately, document is created in background.
  - `/view/async/html` and `/view/async/pdf`
- New endpoints for synchronous HTML and PDF generation, response with link is not returned until document is created.
  - `/view/sync/html` and `/view/sync/pdf`

</details>

<a id=release-for-self-service-portal-portal-account,-registration-form-for-a-separate-switching-service-account></a>
## release-for-self-service-portal-account,-registration-form-for-a-separate-intermediary-service-account.
| environment mediation service | period | status |
|------------|-----------------------------|----------------|
| Preview | Docu + registration form: **KW38** , status overview: **KW39** | published |
| staging | docu + registration form: **KW39** , status overview: **KW40** | published |
| production | docu + registration form: **KW40** , status overview **KW41** | published | |

Status: published on 10/4/2023 <br>
<details>
<summary>Release Notes</summary>

### Self-Service Portal
>**Environments** <br>
>NEW: Preview https://portal.preview-ozg-vermittlungsdienst.de <br>
>NEW: Staging https://portal.staging-ozg-vermittlungsdienst.de <br>
>NEW: Production https://portal.ozg-vermittlungsdienst.de<br>

### Show feature documentation + registration form
- Full documentation in portal incl. releases and maintenance pages
- Registration form for requesting new brokerage service accounts
  1. create a new portal account
  2. filling in the registration form for a separate mediation service account

### Feature status overview of announcements
- Status overview of all submitted announcements for mediation service accounts
  
</details>
<br>

<a id=Release-for-RequestedPublicationDate-Fix-+-Notice-Viewer-Switching-Service,-eSender-Hub,-Notice-Viewer></a>
## Release for RequestedPublicationDate Fix + Notice-Viewer - Mediation Service, eSender-Hub, Notice-Viewer.
| Environment Switching Service | Period | BKMS | Status |
|------------|-----------------------|---------------------------|--------|
| Preview | RequestedPublicationDate Fix only: **KW37**, Everything else: **KW39** | supported in alpha | published |
| staging | moved: **KW40** | supported in alpha | published |
| production | postponed: **KW41** | supported in production | published | |

Status: released 10/11/2023 <br>
<details>
<summary>Release notes</summary>

### Switching service
>**Environments** <br>
>NEW: Preview environment https://preview-ozg-vermittlungsdienst.de<br>
>NEW: Staging environment https://staging-ozg-vermittlungsdienst.de<br>
>Production environment https://ozg-vermittlungsdienst.de<br>

- Integration with new BKMS endpoint
- New naming of notification XML file in ASIC container: instead of 'notice.xml' now 'uuid.eforms.xml'
- Peppol integration with B2Brouter
- 'PublicationID' of TED is now processed and stored in the switching service

### Notice Viewer
>**Environments** <br>
>NEW: Preview environment https://viewer.preview-ozg-vermittlungsdienst.de<br>
>NEW: Staging environment https://viewer.staging-ozg-vermittlungsdienst.de<br>
>NEW: Production environment https://viewer.ozg-vermittlungsdienst.de<br>

- Authorization and integration with Mediator
- Support of eForms-DE 1.1.0 and -DE 1.0.1
- Latest DE SDK version added - 1.1.0 - 1.7.1
- Removal of files that are 24 hours older

Available as standalone web service with token authentication (same token as in mediator service can be used) for uploading XML files and as endpoint in mediator service for rendering already submitted announcements based on the

### eSender Hub
- New transformation from eForms-DE to eForms-EU regarding 'requestedPublicationDate', detailed explanation [here](/documentation/eForms_creation.md)

### Validator
>**Environments** <br>
>NEW: Preview environment https://validator.preview-ozg-vermittlungsdienst.de<br>
>NEW: Staging environment https://validator.staging-ozg-vermittlungsdienst.de<br>
>Production environment https://ozg-vermittlungsdienst.de<br>

- Schematron updates for eForms-DE 1.1 (https://projekte.kosit.org/eforms/eforms-de-schematron/-/releases/v0.6.2) and 1.0.1 (https://projekte.kosit.org/eforms/eforms-de-schematron/-/releases/v0.5.3)
- Token authorization for external validator
</details>
<br>

<a id=release-for-eForms-DE-1.1-switching-service-and-eSender-Hub></a>
## Release for eForms-DE 1.1 - Mediation Service and eSender Hub
| Environment Switching Service | Period | BKMS | Status |
|------------|-----------------------|---------------------------|----------------|
| Preview | **KW34** | supported in Alpha | published |
| Staging | **KW35** | supported in Alpha | published |
| production | **KW37** | supported in production | published |

Status: released on 09/13/2023 <br>
<details>
<summary>Release Notes</summary>

### Switching service
>**Environments** <br>
>Preview environment **until 09/15/2023**: https://preview.ozg-vermittlungsdienst.de, from 08/30/2023: https://preview-ozg-vermittlungsdienst.de <br>
>Staging environment **until 09/15/2023**: https://staging.ozg-vermittlungsdienst.de, from 08/30/2023: https://staging-ozg-vermittlungsdienst.de <br>
>Production environment https://ozg-vermittlungsdienst.de<br>

- Initial support for eForms-DE 1.1 (Schematron https://projekte.kosit.org/eforms/eforms-de-schematron/-/releases/v0.6.0)
- New DEMO endpoint for visualization of delivered eForms-DE documents /notice-viewer/{trackingCode} (currently returns only sample document)
- New job for re-sync of status information
- Various improvements for status change of notices and authentication

### eSender Hub
 - Initial eForms-DE 1.1 -> eForms-EU 1.7 transformation
</details>
<br>

<a id=Release-Offline-Validator-for-eForms-DE-1.0.1-and-1.1.0></a>
## Release Offline Validator for eForms-DE 1.0.1 and 1.1.0
Status: Published 08/14/2023<br>
https://github.com/EFA-FHB/eforms-validator-core/releases/tag/1.0.3
<br><br>

<a id=production-release-june-switching-service-&-eSender-Hub></a>
## Production Release June - Switching Service & eSender Hub.
Status: published 06/28/2023<br>
<details>
<summary>Release notes</summary>

### Switching service
>**environments<br>
>Preview environment https://preview.ozg-vermittlungsdienst.de<br>
>Staging environment https://staging.ozg-vermittlungsdienst.de<br>
>Production environment https://ozg-vermittlungsdienst.de<br>

>**Info** <br>
>After the production release in June, a user must be requested again for the production and staging environment, even if a user already exists in Preview.

- Added stop endpoint to stop national announcements in BKMS.
- Check that updates of announcements are not possible if the previous version has not been stopped or if it is already published
- Open Api description adapted
- Improved error messages when returning information to FVH.
- Added metrics to measure last successful and unsuccessful endpoint calls along with scheduled job runs
- Several optimizations and bug fixes
- Introduction of paging for scheduled jobs
- Improved auditing of eSender updates as they occur
- Internal validator integration improved, error types are now more clearly classified.
- Updated the response to the date of the last update of the PSPs and it is now more accurate.
- Changed names for error reasons:
Instead of DELIVERY_NOT_FOUND there is NOTICE_NOT_FOUND.
Instead of DELIVERY_ALREADY_PROCESSED it is NOTICE_ALREADY_PROCESSED
Instead of DELIVERY_METADATA_INVALID there is NOTICE_METADATA_INVALID
- New endpoint /v1/notices/status created - Returns status information for notices within a specified time period.

### eSender hub
- Implemented manual stop in BKMS when PSP stops notification.
- Implemented automatic stop in BKMS due to TED NOT_PUBLISHED
- Updated translations for error messages
- Transformations implemented: version conversion from eform-de-1.0 to eform-sdk-1.5 and conversion from DE code lists to EU code lists
- Implemented: Retrieval and storage of BKMS status PUBLISHED
- Jobs PROCESS_NOTICES and ALIGN_TED_STATUS improved
- Implemented account management application
- Improved response for mediation service in case of duplicates
- API keys for production and staging users updated
- Performance improvements
- Several optimizations and bug fixes
</details>
<br>

<a id=preview-release-may-intermediary-service-&-validator-webservice></a>
## Preview Release May - Mediation Service & Validator Web Service.
Status: published 05/04/2023<br>
<details>
<summary>Release notes</summary>
<br>

### Switching service
Preview environment https://bkms-mediator-app-preview.efa-fhb.apps-int.nortal.com
- Extension of API authorization to include refresh tokens<br>.
Details at [Connection to the mediator service](/documentation/Connection_to_mediator.md)

- Extension of status information to include transfer information (warnings and error messages).<br>
Details in [Status and transfer information](/documentation/Status_information.md).
- More detailed error messages
- Version check is now additionally performed using the data of the announcement service<br>.
When a change notice of a subthreshold notice is transferred, the following checks are made:<br>
-Is the announcement to be changed available in the BKMS?<br>
-Are there already several notices in the BKMS whose concatenated noticeId and noticeVersion match the Change Notice Version Identifier?<br>
-Is there a change notice in the BKMS that has already updated the version to be changed?<br>
This means only the latest version in a chain of notices will be updated.
- Subthreshold announcements published in the announcement service are given the status PUBLISHED.<br>
The status will be returned accordingly when a status query is made.
- Several optimizations and bug fixes
<br><br>

### Validator
Preview environment https://eforms-validator-preview.efa-fhb.apps-int.nortal.com
- Extension of the result report with the rule name `rule` and the applied rule `ruleContent`.

- Several optimizations and bug fixes
</details>
<br>
</details>
