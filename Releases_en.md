### EfA implementation project "Access to public procurement"
# Releases

<br />

- January 2024
  - Release for Self-Service Portal, Mediation Service, eSender, Notice Viewer and Validator](#Release-for-self-service-portal,-mediation-service,-eSender,-notice-viewer-and-validator)
- December 2023
  - Release for validation (eForms-DE 1.1 multilingualism)](#Release-for-validation)
  - [Release for self-service portal, switching service, eSender, notice viewer and validator](#Release-for-self-service-portal,-switching-service,-eSender,-notice-viewer-and-validator)
- November 2023
  - Hotfix release for switching service and eSender](#Release-for-switching-service-and-eSender)
  - Hotfix release for validator, mediation service and eSender](#Release-for-validator-mediator-and-eSender)
  - Hotfix release for notice viewer, validator and mediation service](#Release-for-notice-viewer-mediator-and-validator)
- October 2023
  - Release for Notice Viewer - PDF documents + synchronous calls](#Release-for-notice-viewer-PDF-documents+-synchronous-calls)
  - [Release for self-service portal, registration form for a separate mediation service account](#Release-for-self-service-portal,-registration-form-for-a-separate-mediation-service-account)
- September 2023
  - [Release for RequestedPublicationDate Fix + Notice Viewer - Mediation Service, eSender Hub, Notice Viewer](#Release-for-RequestedPublicationDate-Fix-+-Notice-Viewer-Mediation-Service,-eSender-Hub,-Notice-Viewer)
  - Release for eForms-DE 1.1 - switching service and eSender Hub](#Release-for-eForms-DE-1.1-switching-service-and-eSender-Hub)
- August 2023
  - Release Offline Validator for eForms-DE 1.0.1 and 1.1.0](#Release-Offline-Validator-for-eForms-DE-1.0.1-and-1.1.0)
- June 2023
  - Production Release June - Switching Service & eSender Hub](#Production-Release-June-Switching-Service-&-eSender-Hub)
- May 2023
  - Preview Release May - Switching Service & Validator Web Service](#Preview-Release-May-Switching-Service-&-Validator-Webservice)

<br />

<a id=release-for-self-service-portal,-mediation-service,-eSender,-notice-viewer-and-validator></a>
## Release for self-service portal, switching service, eSender, notice viewer and validator
| Environment Operator Service | Period | Status |
|------------|-----------------------------|----------------|
| Preview | 15.01.2024 | published |
| Staging | 22.12.2024 | will be published |
| Production | 31.12.2024 | will be published |

> **IMPORTANT** <br>
The following eForms versions are no longer supported by the switching service
- eForms DE-1.0.1
- eForms SDK-1.5.5

Status: In QA <br>
<details>
<summary>Release Notes</summary>

### Self-Service Portal
- ---

### Operator service
- ---

### eSender
- ---

### Validator (web service + open source)
- ---

### Notice Viewer
- ---

</details>

<a id=release-for-validation></a>
## Hotfix release for validation (eForms-DE 1.1 multilingualism)
| Environment Switching service | Period | Status |
|------------|-----------------------------|----------------|
| Preview | 18.11.2023 | published |
| Staging | 19.11.2023 | published |
| Production | 20.11.2023 | published |

Status: Published on 20.12.2023 <br>
<details>
<summary>Release notes</summary>

### Validator (web service + open source)
- Use of eForms-DE Schematron 0.7.2 for eForms-DE 1.1 (https://projekte.kosit.org/eforms/eforms-de-schematron/-/releases/v0.7.2)
- enables full support of multilingual eForms-DE documents

### Mediation service
- Use of eForms-DE Schematron 0.7.2 for eForms-DE 1.1 (https://projekte.kosit.org/eforms/eforms-de-schematron/-/releases/v0.7.2)
- enables full support of multilingual eForms-DE documents
- Verification of acceptance of change notices has been improved


</details>

<a id=release-for-self-service-portal,-mediation-service,-eSender,-notice-viewer-and-validator></a>
## Release for Self-Service Portal, Mediation Service, eSender, Notice Viewer and Validator
| Environment Operator Service | Period | Status |
|------------|-----------------------------|----------------|
| Preview | 28.11.2023 | published |
| Staging | 04.12.2023 | published |
| Production | 11.12.2023 | published |

Status: Published on 11.12.2023 <br>
<details>
<summary>Release notes</summary>

> **Note** <br>
It is no longer possible to log in to the self-service portal with an operator service user.

### Self-Service Portal
- After approval, an SSP user can now create their own attendant service and dashboard users themselves
- SSP users can link multiple attendant service users to one dashboard user
- All created switching service and dashboard users can be deleted, edited and deactivated
- All transmitted announcements are now available for the dashboard user

### Operator service
- The correct status is now set for repeated delivery to BKMS in the event of a duplicate
- Configurable status assignment table implemented
- The message has been added when the user has successfully stopped the notification
- Tenant deletion process has been changed
- Endpoint for tenant and dashboard user creation improved
- A new PATCH endpoint for updating eSender integration and Schematron validation has been introduced
- The endpoint for updating tenant users in Keycloak has been improved
- Change notice checks have been reintroduced
- Various status descriptions have been improved
- XSD error details about the failed rule are included in the response
- The validation model of 'business_document' has been introduced
- Mandatory lineDescription in PEPPOL message (T016) has been improved
- Endpoint for user creation/update has been improved
- Updated descriptions for Notice Viewer endpoints in Swagger
- Improved the error message when submitting a notice to indicate the error case
- Various performance improvements and bug fixes

### eSender
- Retry delivery is now implemented if BKMS does not respond
- BKMS integration has been improved
- Various performance improvements and bug fixes

### Validator (web service + open source)
- Bugfix for CR-DE-BT-165 and IssueDate applied
- Various performance improvements and bug fixes

### Notice Viewer
- Improved rendering of BT-801, BT-92, BT-93
- Caching for generated documents introduced
- Added placeholder.html for deleted files
- Updated description for Notice Viewer endpoint in Swagger (also applies to the switching service)
- Various performance improvements and bug fixes

</details>

<a id=release-for-switching-service-and-eSender></a>
## Hotfix release for switching service and eSender
| environment switching service | period | status |
|------------|-----------------------------|----------------|
| Preview | 20.11.2023 | published |
| Staging | 21.11.2023 | published |
| Production | 21.11.2023 | published |

Status: Published on 21.11.2023 <br>
<details>
<summary>Release notes</summary>

### eSender and switching service
- Improved technical configuration of the apps and renewal of certificates


</details>

<a id=release-for-validator-mediator-and-eSender></a>
## Hotfix release for validator, mediation service and eSender
| environment mediation service | period | status |
|------------|-----------------------------|----------------|
| Preview | 13.11.2023 | published |
| Staging | 15.11.2023 | published |
| Production | 16.11.2023 | published |

Status: Published on 16.11.2023 <br>
<details>
<summary>Release notes</summary>

### eSender
- Improved integration with TED: if TED is not available or a timeout takes too long
- Language issue (BT-500-Organization-Company): multiple languages are now supported
  
### Validator (web service + open source)
- eForms SDK 1.5.5 version has been implemented

### Switching service
- The number of allowed domain name characters in the 'authorEmail' parameter of the POST v2/notices endpoint has been increased and now supports from 2 to 18 characters.


</details>

<a id=release-for-notice-viewer-mediator-and-validator></a>
## Hotfix release for notice viewer, validator and mediation service
| environment mediation service | period | status |
|------------|-----------------------------|----------------|
| Preview | 08.11.2023 | published |
| Staging | 09.11.2023 | published |
| Production | 09.11.2023 | published |

Status: Published on 09.11.2023 <br>
<details>
<summary>Release notes</summary>

### Notice viewer
- Improvement for the visualization of monetary values, comma removed as separator for thousands of values
- Increase maximum file size to 2MB
  
### Validator (web service + open source)
- Use of eForms-EU SDK 1.7.2 for eForms-DE 1.1 (https://github.com/OP-TED/eForms-SDK/releases/tag/1.7.2)
- Increase maximum file size to 2MB

### Mediation service
- Increase maximum file size to 2MB


</details>

<a id=release-for-notice-viewer-pdf-documents+-synchronous-calls></a>
## Release for Notice Viewer - PDF documents + synchronous calls
| Environment Switching Service | Period | Status |
|------------|-----------------------------|----------------|
| Preview | 10/17/2023 | published |
| Staging | 18.10.2023 | published |
| Production | 20.10.2023 | published |

> **Note** <br>
> When using this API endpoint, we would like to point out that the performance is currently still being optimized. Please take this into account with intensive request frequency and plan appropriate tolerances in your processes. We are actively working on improvements and thank you for your understanding.

Status: Published on 20.10.2023 <br>
<details>
<summary>Release Notes</summary>

### Notice viewer
>**environments** <br>
> Preview https://viewer.preview-ozg-vermittlungsdienst.de <br>
> Staging https://viewer.staging-ozg-vermittlungsdienst.de <br>
> Production https://viewer.ozg-vermittlungsdienst.de<br>

- Backwards compatibility with original `/view` endpoint
- New endpoints for asynchronous HTML and PDF generation, same behavior as previous `view` endpoint, response is returned immediately, document is created in the background.
  - `/view/async/html` and `/view/async/pdf`
- New endpoints for synchronous HTML and PDF generation, response with link is only returned when document is created.
  - `/view/sync/html` and `/view/sync/pdf`

</details>

<a id=release-for-self-service-portal,-registration-form-for-a-separate-mediation-service-account></a>
## Release for self-service portal, registration form for a separate operator service account
| Environment Brokerage Service | Period | Status |
|------------|-----------------------------|----------------|
| Preview | Documentation + registration form: **KW38** , status overview: **KW39** | published |
| Staging | Documentation + registration form: **KW39** , Status overview: **KW40** | published |
| production | documentation + registration form: **KW40** , Status overview **KW41** | published |

Status: Published on 4.10.2023 <br>
<details>
<summary>Release notes</summary>

### Self-Service Portal
>**Environments** <br>
>NEW: Preview https://portal.preview-ozg-vermittlungsdienst.de <br>
>NEW: Staging https://portal.staging-ozg-vermittlungsdienst.de <br>
>NEW: Production https://portal.ozg-vermittlungsdienst.de<br>

### Show feature documentation + registration form
- Full documentation in the portal incl. releases and maintenance pages
- Registration form for requesting new brokerage service accounts
  1. create a new portal account
  2. filling in the registration form for a separate brokerage service account

### Feature Status overview of announcements
- Status overview of all notices submitted for mediation service accounts
  
</details>
<br>

<a id=Release-for-RequestedPublicationDate-Fix-+-Notice-Viewer-Mediation-Service,-eSender-Hub,-Notice-Viewer></a>
## Release for RequestedPublicationDate Fix + Notice-Viewer - Mediation Service, eSender-Hub, Notice-Viewer
| Environment Switching Service | Period | BKMS | Status |
|------------|-----------------------|---------------------------|--------|
| Preview | RequestedPublicationDate only Fix: **KW37**, Everything else: **KW39** | supported in Alpha | published |
| Staging | moved: **KW40** | supported in Alpha | published |
| production | postponed: **KW41** | supported in production | published |

Status: published on 11.10.2023 <br>
<details>
<summary>Release notes</summary>

### Operator service
>**Environments** <br>
>NEW: Preview environment https://preview-ozg-vermittlungsdienst.de<br>
>NEW: Staging environment https://staging-ozg-vermittlungsdienst.de<br>
>Production environment https://ozg-vermittlungsdienst.de<br>

- Integration with new BKMS endpoint
- New naming of the notification XML file in the ASIC container: instead of 'notice.xml' now 'uuid.eforms.xml'
- Peppol integration with B2Brouter
- 'PublicationID' from TED is now processed and saved in the switching service

### Notice Viewer
>**Environments** <br>
>NEW: Preview environment https://viewer.preview-ozg-vermittlungsdienst.de<br>
>NEW: Staging environment https://viewer.staging-ozg-vermittlungsdienst.de<br>
>NEW: Production environment https://viewer.ozg-vermittlungsdienst.de<br>

- Authorization and integration with the Mediator
- Support for eForms-DE 1.1.0 and -DE 1.0.1
- Latest DE-SDK version added - 1.1.0 - 1.7.1
- Removal of files that are 24 hours older

Available as a standalone web service with token authentication (same token as in the switching service can be used) for uploading XML files and as an endpoint in the switching service for rendering previously submitted notices using the

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

<a id=Release-for-eForms-DE-1.1-Mediation-service-and-eSender-Hub></a>
## Release for eForms-DE 1.1 - switching service and eSender Hub
| Environment Switching Service | Period | BKMS | Status |
|------------|-----------------------|---------------------------|----------------|
| Preview | **KW34** | supported in Alpha | published |
| Staging | **KW35** | supported in Alpha | published |
| Production | **KW37** | supported in production | published |

Status: published on 13.09.2023 <br>
<details>
<summary>Release notes</summary>

### Operator service
>**environments** <br>
>Preview environment **until 15.09.2023**: https://preview.ozg-vermittlungsdienst.de, from 30.08.2023: https://preview-ozg-vermittlungsdienst.de <br>
>Staging environment **until 15.09.2023**: https://staging.ozg-vermittlungsdienst.de, from 30.08.2023: https://staging-ozg-vermittlungsdienst.de <br>
>Production environment https://ozg-vermittlungsdienst.de<br>

- Initial support for eForms-DE 1.1 (Schematron https://projekte.kosit.org/eforms/eforms-de-schematron/-/releases/v0.6.0)
- New DEMO endpoint for visualization of submitted eForms-DE documents /notice-viewer/{trackingCode} (currently only returns sample document)
- New job for re-sync of status information
- Various improvements to the status change of notices and authentication

### eSender Hub
 - Initial eForms-DE 1.1 -> eForms-EU 1.7 transformation
</details>
<br>

<a id=Release-Offline-Validator-for-eForms-DE-1.0.1-and-1.1.0></a>
## Release offline validator for eForms-DE 1.0.1 and 1.1.0
Status: Published 14.08.2023<br>
https://github.com/EFA-FHB/eforms-validator-core/releases/tag/1.0.3
<br><br>

<a id=Production-Release-June-Mediation-Service-&-eSender-Hub></a>
## Production Release June - Switching Service & eSender Hub
Status: Published 28.06.2023<br>
<details>
<summary>Release notes</summary>

### Switching service
>**environments** <br>
>Preview environment https://preview.ozg-vermittlungsdienst.de<br>
>Staging environment https://staging.ozg-vermittlungsdienst.de<br>
>Production environment https://ozg-vermittlungsdienst.de<br>

>**Info** <br>
>After the production release in June, a new user must be requested for the production and staging environment, even if a user already exists in Preview.

- Stop endpoint added to stop national announcements in BKMS
- Check that updates of announcements are not possible if the previous version has not been stopped or if it has already been published
- Open Api description adapted
- Improved error messages when returning information to FVH
- Added metrics to measure the last successful and unsuccessful endpoint calls along with the scheduled job runs
- Several optimizations and bug fixes
- Introduction of paging for scheduled jobs
- Checking of occurring updates of eSender improved
- The integration of the internal validator has been improved, the error types are now more clearly classified
- The response to the date of the last update of the WBS has been updated and is now more accurate.
- Changed names for error reasons:
DELIVERY_NOT_FOUND has been replaced by NOTICE_NOT_FOUND
DELIVERY_ALREADY_PROCESSED has been replaced by NOTICE_ALREADY_PROCESSED
DELIVERY_METADATA_INVALID is replaced by NOTICE_METADATA_INVALID
- New endpoint /v1/notices/status created - Returns the status information for notices within a specified time period.

### eSender Hub
- Manual stop implemented in BKMS when PSP stops notification
- Implemented automatic stop in BKMS due to TED NOT_PUBLISHED
- Updated translations for error messages
- Transformations implemented: Version conversion from eform-de-1.0 to eform-sdk-1.5 and conversion from DE code lists to EU code lists
- Implemented: Retrieving and saving the BKMS status PUBLISHED
- Jobs PROCESS_NOTICES and ALIGN_TED_STATUS improved
- Introduction of an account management application
- Improved response for switching service in case of duplicates
- API keys for production and staging users have been updated
- Performance improvements
- Several optimizations and bug fixes
</details>
<br>

<a id=Preview-Release-May-Mediation-Service-&-Validator-Webservice></a>
## Preview Release May - Mediation Service & Validator Web Service
Status: Published 04.05.2023<br>
<details>
<summary>Release notes</summary>
<br>

### Operator service
Preview environment https://bkms-mediator-app-preview.efa-fhb.apps-int.nortal.com
- Extension of the API authorization with refresh tokens<br>
Details under [Connection to the mediation service](/documentation/Connection_to_mediator.md)

- Extension of the status information to include transfer information (warnings and error messages).<br>
Details under [Status and transfer information](/documentation/Status_information.md)
- More detailed error messages
- Version check is now also carried out using the data from the notification service<br>
The following checks are carried out when transmitting a change notification for a subthreshold notice:<br>
-Is the notice to be amended available in the BKMS<br>
-Are there already several notices in the BKMS whose concatenated noticeId and noticeVersion match the change notice version identifier?
-Is there a change notice in the BKMS that has already updated the version to be changed?<br>
This means that only the latest version in a chain of notices is updated.
- Subliminal announcements published in the announcement service receive the status PUBLISHED.<br>
The status is returned accordingly in a status query.
- Several optimizations and bug fixes
<br><br>

### Validator
Preview environment https://eforms-validator-preview.efa-fhb.apps-int.nortal.com
- Extension of the result report by the rule name `rule` and the applied rule `ruleContent`

- Several optimizations and bug fixes
</details>
<br>
</details>
