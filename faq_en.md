### Public procurement data service
# Frequently asked questions

- [Data service for public procurement](#datenservice-öffentlicher-einkauf)
- [Standard eForms-DE and SDK-DE](#standard-eForms-DE-and-SDK-DE)
- [General](#general)

## Data service public purchasing

### Connection

<details>
<summary>
Which systems are available and where do I need an account?
</summary>

<br><br>
**[Editorial system](https://resy.datenservice-oeffentlicher-einkauf.de/)**: Web interface for creating announcements and publishing them on TED and in the announcement service. <br>
Does your public procurement office not have software from a specialist procedure manufacturer for creating notices, does it not support all the forms you need or have you previously used TED's eNotices2? Then the editorial system is right for you!
<br><br>
**[Vermittlungsdienst](https://ozg-vermittlungsdienst.de/)**: Purely technical interface for accepting, validating and forwarding notices to TED and the notice service. <br>
Does NOT provide an interface for creating announcements! Only machine-to-machine communication is possible, e.g. from an awarding authority software. This connection is usually implemented by the specialist procedure manufacturer.
<br><br>
**[Self-Service Portal](https://github.com/EFA-FHB/ozg-vermittlungsdienst-doku/blob/main/documentation/SSP.md)**: Web interface for the account management of Vermittlungsdienst accounts.
<br> Mainly used by specialist procedure manufacturers. Dashboard accounts are possible for viewing the status information of submitted notices, please contact your specialist procedure manufacturer!
<br>
</details>
<br>

<details>
<summary>
What information is required to apply for an account? (updated on 11.10.23)
</summary>
<br>


Since 04.10, accounts should be requested in the [Self-Service Portal](https://portal.ozg-vermittlungsdienst.de). All required information is requested in the registration form for a VD account. These are:

<br>

- System environment for which access data is requested (preview, staging, production). Registration in the portal takes place for the corresponding environment, i.e. if an account is required for the staging environment, this should be requested in the staging portal.

- E-mail address to be used as the user name (this must be unique for each environment, no duplicates allowed)
  
- URL of the awarding platform on which the notices are published
  
- First name, surname and email address of the representative of the FVH (specialist procedure manufacturer)
  
- Name of the FVH
</details>
<br>


<details>
<summary>
One e-mail address must be entered as the user name for each registration. Is it possible to enter the same e-mail address for several systems?
</summary>
<br>
We generally request two emails per account (sometimes also referred to as a client): An account email to activate the account and a contact email. An individual email per account is required for activation in order to set the password for the account and to enable unique authentication with the combination of email and password. However, the account email can also be a functional mailbox and is only required to manage the account. The contact email address is only used if questions arise during operation regarding a notification sent from this account. The contact email and account email may be identical if necessary and the same contact email (e.g. a central contact person) may be used for several accounts. However, you can reuse your account email once between the system environments, for example the same account email address for preview, staging and production. We generally recommend one account per awarding platform.
</details>
<br>

<details>
<summary>
When creating an account, a contact email address of an FVH must be specified. What is this used for?
</summary>
<br>
This email is used when we want to proactively contact you. This may be the case, for example, if there are anomalies with your account or the notices submitted or if we send general information to all account managers.
</details>

<br>

<details>
<summary>
Can multiple accounts be requested at the same time? How many accounts are recommended for the preview and staging environment?
</summary>
<br>
The URL of the awarding platform is used purely to assign the accounts/clients; it has nothing to do with the link to the award documents.

Some awarding platforms use e.g. Dropbox or google drive or similar for hosting the award documents, which is why the platform behind it cannot be clearly identified. For this reason, this information is also necessary. The link to the tender documents remains in the XML document and this is primarily displayed in the BKMS interface. The link provided when the account is created is only displayed at the bottom right, below the notice itself, as a disclaimer/source.
</details>
<br>

<details>
<summary>
What is the difference between the URL of the procurement platform requested when creating the account and the link to the procurement documents in the eForms document?
</summary>
<br>
Please send us a list of required accounts to support-oeffentlichevergabe@bdr.de including all required information per account. We recommend using exactly as many accounts for staging as you plan to use for production. In addition, any number of test accounts are of course possible on Preview and Staging.  
</details>

<br>

<details>
<summary>
On staging or preview, is the release cycle and validation performed in the same way as in production or are the status changes accelerated? What delays can be expected between acceptance and release?
</summary>
<br>
In all environments, the same validation and the same delay in publishing is performed as in the production environment. In this case, the time delays are with TED (publication on working days at the earliest on the next working day if accepted by 4 pm) or the legally required logic of national publication (forwarding to the BKMS) after 48 hours at the earliest. The BKMS publishes immediately once an announcement has been received, unless the preferred publication date is in the future. In this case, publication in both TED and BKMS would only take place on the requested date, subject to the restrictions applicable to TED (e.g. no publication at weekends).
</details>
<br>

<details>
<summary>
The URL of the awarding platform should be specified to request access. What is the purpose of this information?
</summary>
<br>
The purpose of specifying the URL is to be able to distinguish between the systems mentioned, to enable you to access them correctly and to avoid duplicates. Procurement platforms are the systems in which notices are published; the URL of the procurement platform can be alpha.oeffentlichevergabe.de (test environment BKMS), for example. This URL is used to identify the platform on which you are currently publishing your notices. We are aware that there may be different procedures depending on the structure of the system of the respective FVH. In principle, you will need one account for each system that is to be used for future deliveries to the brokerage service. If you are unsure which systems/platforms should be connected to the DöE for you, we will be happy to support you in this decision. Please send us an inquiry to support-oeffentlichevergabe@bdr.de.
</details>
<br>

<details>
<summary>
Which system environment is the environment to which our test systems can send notifications? What is the difference between the preview and staging environment?
</summary>
<br>
The preview environment is only used for testing. Updates are often installed here and this is also our test environment for future releases. The staging environment is a 100% copy of the production environment and should only be used for production-related tests. Both environments deliver into the Alpha environment of BKMS and TED Preview. On staging, your tests should be performed exactly as you plan to do in production. In principle, however, both environments are suitable for testing.
</details>
<br>

<details>
<summary>
Where can I find examples of eForms-DE? What different types are there? ?
</summary>
<br>
Sample documents for eForms-DE can be found in the KoSIT schematron repository: https://projekte.kosit.org/eforms/eforms-de-schematron/-/tree/main/src/test/eforms-de-base-samples
The different versions of the documents can be accessed via the respective tags and releases.

The abbreviations are to be understood as follows:

PIN
Eng: Prior Information Notice
Deu: Prior information
Subtype 1-14, E2
PINs are announcements that are published before the start of the "call for competition".

CN
Eng: Contract Notice
Deu: Open procedure / public invitation to tender
Subtype 15-24, E3
CNs are notices that initiate the "call for competition".

CAN
Eng: Contract Award Notice
Deu: Notice (awarded contract)
Subtype 25-40, E4
CANs are used to create contract award notices, which are published shortly after the contract is signed. They refer to the contract notice and contain information about the award procedure, such as the contract award, the winner, etc.

The naming of the reference documents involves the following:

eforms = standard document type
PIN/CN/CAN = see above; indicates the type of notice
Number 1-40 or E1-E4 = subtype of notice, where E is for subliminal notices
DE = standard is eForms-DE
(in)/valid = whether the file is valid or invalid according to the eForms-de specification
There is not yet an example file for all types of notices. If you need an example for a specific type that does not exist in the above link, we will be happy to forward a request. Unfortunately, the EU does not provide examples for all types of notices either, which means that providing examples is sometimes quite time-consuming.
</details>
<br>

### Roadmap

<details>
<summary>
Is there a roadmap regarding the further development of the Vermittlungsdienst, eSenderHub, etc. components after the deadline of 25.10.2023, in particular with regard to feature and API enhancements, milestones and the respective go-live dates?
</summary>
<br>
As things currently stand, two more releases are planned for the data service after 25.10.2023. The content of the releases primarily relates to convenience functions and evaluation options. API changes and extensions are not planned according to the current planning status.
</details>
<br>


<details>
<summary>
Will there be a roadmap for the further development of the SDK? This is particularly interesting for platform operators in view of the adaptation times for new SDK-EU versions, as the SDK-DE and SDK-EU currently still differ in their versioning.
</summary>
<br>

The version designations of the SDK for the respective national eForms-DE standard are based on the version designations of the eForms-DE standard. For each eForms-DE SDK, the European SDK version on which it is based is indicated. (see also explanation at https://gitlab.opencode.de/OC000008125155/SDK-eforms-de)

It is not planned that a new eForms-DE version will be published for every minor version of eForms-EU. Therefore, the versioning of eForms-EU and eForms-DE will not be directly identical in the future. However, there will always be exactly one corresponding eForms-EU version for each eForms-DE version.
</details>
<br>

<details>
<summary>
In what time frame will a DE update be made available after an EU update has been released?
</summary>
<br>

Please note that a DE update is not automatically required for every EU update.
<br>
The GDK is not the responsibility of KoSIT. However, the eForms-DE specification. As was jointly determined at the 1st technical working meeting, we are currently unable to provide a simple answer with clear dates in view of the uncertainties that still exist regarding the entry into force and lifespan of the versions of the EU-SDK. What is certain is that a specific version of eForms-DE will declare itself compatible with a specific version of eForms-SDK and that this should happen as soon as possible. As currently eForms-DE 1.0.1 is compatible with eForms-SDK 1.5.1 (SDK 1.5.1 was released on January 20, 2023 and eForms-DE on February 5). This implicitly means that there will not be an eForms-DE version for every eForms-SDK version. The current eForms-DE version 1.1.0 is compatible with SDK 1.7.
</details>
<br>


### Go-Live

<details>
<summary>
What are the submission deadlines? (added on 12.10.23)
</summary>
<br>
To ensure that the announcement is published on TED on the same day, we recommend that the announcement is submitted to the Vermittlungsdienst by 23:00 on the same day.

Example for the FVH:
 To ensure that the notice is sent to the Vermittlungsdienst on the same day, we recommend that the notice be submitted to the specialized procedure manufacturer by 22:00 on the same day.
</details>
<br>

<details>
<summary>
 When will the public procurement data service start? (added on 25.09.23)
</summary>
<br>
The productive start of the Public Procurement Data Service is regulated by §83a of the current Public Procurement Ordinance (VgV). This is expected to be 25.10.2023.
</details>
<br>

<details>
<summary>
Are all 40 EU notice types supported at go-live?
</summary>
<br>
All document types from eForms-DE are accepted (40 for the upper threshold and 3 for the lower threshold). Where necessary, these are generically converted into the eForms-EU format. This corresponds to the contents of the current eForms-DE standard.
</details>
<br>

<details>
<summary>
Is it possible to continue submitting notices via eNotices2 from 25.10.2023?
</summary>
<br>
From 25.10.2023, all above-threshold notices must legally be submitted in eForms-DE format via the public procurement data service. Direct submission via eNotices2 is not standard-compliant, as the adaptations to the eForms-DE standard would not be taken into account and is no longer legally permissible.
</details>

<br>

<details>
<summary>
Does the introduction of eForms apply to both upper (EU) and lower thresholds (national) or only to the EU level?
</summary>
<br>
From 25.10.23, EU-wide notices in eForms-DE format must be transmitted via the interface. If the interface is also to be used for national notices, this must also be done via the eForms format so that the data service can process them. You can find out which formats are currently supported and processed in our preview at https://github.com/EFA-FHB/ozg-vermittlungsdienst-doku/blob/development/documentation/eForms_support.md.
</details>
<br>

<details>
<summary>
How is a change of eSender for an announcement handled if it is to be corrected? How is a change of eSender handled within a procedure with multiple notices? How can corrections or references for subsequent notices be made in relation to notices submitted in the old format?
</summary>
<br>

It will not be possible to query the status of an old announcement via the data service or to stop an old announcement that was not submitted via the data service, as the data service cannot send queries about announcements sent in the old format. However, the change of eSender has no influence on the possibility of referencing old notices.
How references and corrections to old notices are possible is described in detail here: https://github.com/EFA-FHB/ozg-vermittlungsdienst-doku/blob/main/documentation/eForms_creation.md
</details>
<br>

### Communication channels

<details>
<summary>
Accessibility:
</summary>
*Questions and suggestions for improvement* regarding the Vermittlungsdienst and the eSender Hub can be directed to oeffentliche-vergabe@nortal.com. Alternatively, Github issues can be created in the documentation repository and the SDK-eForms-DE repository.

For *support requests regarding the operation* of the Vermittlungsdienst and the eSender Hub, please contact: support-oeffentlichevergabe@bdr.de.

*Questions about the announcement service* can be directed to support-oeffentlichevergabe@bdr.de.

We are open to your suggestions!
</details>
<br>


<details>
<summary>
How can it be ensured that platform providers are regularly informed about news regarding the data service, in particular regarding new versions of the components (Vermittlungsdienst, eSenderHub, REST API, etc.), new features, an update of the roadmap, etc.?
</summary>
<br>
Communication takes place through regular information dates for the specialist procedure manufacturers, announcements by e-mail, current roadmap, release notes and FAQs are available in the published documentation repository: https://github.com/EFA-FHB/ozg-vermittlungsdienst-doku. There is also the SDK-eForms-DE repository: https://gitlab.opencode.de/OC000008125155/SDK-eforms-de.
</details>

<br>
<details>
<summary>
How to ensure that platform providers are regularly informed about news regarding the eForms-DE standard / SDK-eForms-DE.
</summary>
<br>

The official publication of the eForms-DE standard is available at https://xeinkauf.de/eforms-de/ .

The associated SDK is published at https://gitlab.opencode.de/OC000008125155/SDK-eforms-de .

For publications on the organizational framework, see

https://www.finanzen.bremen.de/digitalisierung/digitalisierung-von-verwaltungsleistungen-fuer-unternehmen/digitale-beschaffung-103422

Questions about the DE-SDK can be opened via issues in the repository.
</details>
<br>




### Documentation

<details>
<summary>
Does the documentation for the Vermittlungsdienst (https://github.com/EFA-FHB/ozg-vermittlungsdienst-doku) already provide further information on the data service construct. To what extent is it planned to keep this up to date and, if necessary, to supplement it with information in the form of FAQs or similar? Is this GitHub documentation the official provision of information on this topic?
</summary>
<br>

The Github documentation will continue to be maintained and is the official documentation until further notice. It can also be read in the [Self-Service Portal](https://portal.ozg-vermittlungsdienst.de/) of the DöE.
</details>
<br>

<details>
<summary>
How can I determine which versions of the subcomponents are supported for a release?  
</summary>
<br>

Under [eForms Support](/documentation/eForms_support.md) it is documented which eForms versions the subcomponents support.
<br>
For each release, we publish releasenotes to describe which component supports which version. The versions eForms-DE 1.0.1 and 1.1.0 will be supported in all components of the public procurement data service from September 13.
</details>
<br>

<details>
<summary>
Is the documentation for the Vermittlungsdienst (https://github.com/EFA-FHB/ozg-vermittlungsdienst-doku) the official documentation?
</summary>
<br>

Yes, the Github documentation is updated regularly and is the official documentation until further notice. The documentation is also published in the [Self-Service Portal](https://portal.ozg-vermittlungsdienst.de/).
</details>
<br>


### Status model

<details>
<summary>
Stop, change or cancel announcement? (added on 09/27/2013)
</summary>
<br>
-"Publishing" visible in eNotices2 Web and API next month
- Buyer/API can stop the publication of a notice in "Submitted" status
- Once the status "Published" (i.e. on TED) is reached, the notice can be changed or the procedure can be continued
- Lot or procedure can be canceled via award notice without winner
- Change notice with the reason "cancel" = the announcement is null and void - this is possible, but not recommended!
</details>
<br>

<details>
<summary>
How can the start of the 48-hour standstill period be tracked when the announcement is received by TED?
</summary>
<br>
There are two ways to read the time of successful submission to TED from the status information in the Vermittlungsdienst. Either via the technical timestamp when the eSender received confirmation of the submission from the TED API (<tedStatus>ACCEPTED</tedStatus> tedStatusUpdate>2023-07-31T08:02:02.442Z</tedStatusUpdate>) or via the submittedAt value transmitted by TED, which is included in the status query (<ted_accepted_timestamp>). Both values are only slightly different, as there can be a minimal delay between the time when TED accepts the notification and when a success message is returned to the eSender as a response.
</details>
<br>

<details>
<summary>
With the EU's status change notifications, platform providers have also received further metadata on the respective status, e.g. the submission ID, the specific time of publication on TED, the OJ number, etc. With the OJ number, customers previously had the option of no longer having to enter these numbers manually for subsequent notices relating to this contract ("previous notice of the same contract"), as they could be pre-filled. Is it still possible to obtain the above-mentioned information for publication in order to offer customers this range of functionalities?
</summary>
<br>
TED no longer provides the same metadata per disclosure as before, we return all relevant info we receive.
The following data is provided by TED for an announcement.

![Data of an announcement from TED](images/faq/Announcement_Data_of_TED.png)

We process the status, the time of submission and, if applicable, the time of publication. The OJ number is no longer used in eNotices2. If you require further data from this query, please send us an email with your requirements to: support-oeffentlichevergabe@bdr.de. We will be happy to organize a bilateral exchange.
</details>
<br>

<details>
<summary>
How are rejected announcements in error states such as 'REJECTED' status of TED or an 'INTERNAL ERROR' status of BKMS further processed?
</summary>
<br>
There will be an internal monitoring to react to error states (status InternalError) or bugs. Currently, Nortal is the first point of contact at the e-mail address support-oeffentlichevergabe@bdr.de if you have problems with your submissions and your notifications run into an error status. Generally, such error statuses indicate bugs in the DöE, in TED or in the announcement sent. Whenever errors occur in the system (e.g. rejection by TED), they are logged so that a support ticket can be created and a technical analysis carried out if necessary. An individual decision is then made as to which measures are appropriate to rectify the error. In the event of technical errors, the notification can either be resent as a new version after rectification or processed again manually internally. However, this depends on the individual case. If TED rejects the notice, it is possible that an error exists in the notice, e.g. the notice-id is already in use. In this case, the error message returned by TED on rejection is saved so that it can react accordingly.

If your system no longer automatically updates the notice status after the doe_status INTERNAL_ERROR (which is NOT final), you can also check the status via the notices table in the Self-Service Portal (portal.ozg-vermittlungsdienst.de) using your system's login data for the Vermittlungsdienst. Notices will not remain in INTERNAL_ERROR status. Please do not open any tickets with the BDR for this, but contact your specialist procedure manufacturer. Only the doe_status REJECTED is final, in which case you must submit the notice with a new notice ID or version.
</details>
<br>

<details>
<summary>
Is it possible for an above-threshold announcement to change to NOT_PUBLISHED after the deadline if it has already been published in the BKMS? Because then we would have TED:NOT_PUBLISHED / DSE:PUBLISHED, a status that I could not find in the flowchart.
</summary>
<br>
The NOT_PUBLISHED status is only relevant for announcements with lawfulness warnings. If an announcement has no lawfulness warnings, no manual check is performed by TED, so the status NOT_PUBLISHED based on a manual rejection cannot occur.

In the case of lawfulness warnings, an announcement is only forwarded to the BKMS 5 days after SUBMITTED in TED in order to await the manual check. However, if a situation arises in which an announcement has already been published in BKMS and then changes to NOT_PUBLISHED in TED, our system automatically stops this announcement in BKMS so that the status changes to DöE:Stopped. In this way, we ensure that no announcements rejected by TED remain published in the BKMS. However, this scenario is very unlikely.
</details>
<br>

### API mediation service


<details>
<summary>
How can platform operators obtain the information of the EU CVS report on a notice?
<br>
All errors and warnings from the CVS report are passed in the status information. Here we pass the ID, the path, the content and the text of each rule that has been struck. It is not intended to return the CVS report as a file.
</details>
<br>

<details>
<summary>
The REST API description refers to "current data deliveries". What exactly does this mean?
</summary>
<br>
The v1/notices endpoint returns status information on all notices that have been successfully delivered by the currently authenticated client.
</details>
<br>

<details>
<summary>
Can an API key also be used for authentication or only authentication via tokens?
</summary>
<br>
Authentication via API keys will soon be switched off, even on Preview. In the long term, you will only be able to authenticate via tokens with refresh every 24 hours. In individual cases, API keys are still used for testing and debugging purposes.
</details>
<br>

<details>
<summary>
The REST API refers to clients. Does 1 client = 1 API key = 1 issuing platform?
</summary>
<br>
This assumption is correct.
</details>
<br>

<details>
<summary>
The REST API description refers to "current data deliveries". What exactly does this mean?
</summary>
<br>
The v1/notices endpoint returns status information on all notices that have been successfully delivered by the currently authenticated client.
</details>
<br>

<details>
<summary>
Allocation platforms would like to recognize status changes promptly (currently a status query is made approximately every 10 minutes for each relevant data delivery). Are there plans for "GET /v1/notices" to be able to restrict or filter the list to those data deliveries for which a TED or DOE status change has taken place since a submitted time in order to reduce the query load on the system?
</summary>
<br>
Thank you for this suggestion; we will look into implementing it.
</details>
<br>

<details>
<summary>
How can platform operators obtain the information from the EU CVS report on a notice if it is not included in the response on publication (POST → /v2/notices) or in the status information (GET → /v1/notices/{trackingCode})?
</summary>
<br>
All errors and warnings from the CVS report will be transferred to the status information in future. We will pass the ID, the path, the content and the text of each rule that has been struck. It is currently not planned to return the CVS report as a file.
</details>
<br>

<details>
<summary>
Is it possible to use the online Validator API productively?
</summary>
<br>
Yes, productive use of the Online Validator is supported. In the production environment and in the staging environment, the eforms-de-schematron bugfix version will always be the same as in the Vermittlungsdienst itself. The use of the offline validator (https://github.com/EFA-FHB/eforms-validator-core) is also recommended.
</details>
<br>

### Ongoing allocation procedures and changeover to the new data service

<details>
<summary>
 How was the link to or reference to previous announcements made? (added on 27.09.23)

 </summary>

- The notices are linked to the procedure ID.

  Special features:

   --> Planning/PINs are not part of procedures: Use BT-125

   --> Surcharges within a framework agreement: Use OPT-100

   --> Change notice: Use BT-758

   --> Contract amendment: Use BT-1501

   --> Notices before eForms (and all other cases): Use OPP-090

- Use TED publication number ([1-8 digits]-[year]) or eForms UUID

- You can also find this information in the [Developer Docs FAQ](https://docs.ted.europa.eu/home/eforms/FAQ/index.html#_forms_and_procedures)

  - For further details on linking the announcements, see
https://github.com/EFA-FHB/ozg-vermittlungsdienst-doku/blob/main/documentation/eForms_creation.md

- Details on the use of the references can be found here: https://docs.ted.europa.eu/eforms/latest/schema/procedure-lot-part-information.html#previousNoticeSection

 The components of the data service can only accept the new eForms structures. The award platforms currently communicate with the EU using the TED schema structures. For ongoing award procedures, it will be the case that, for example, a contract award notice is published after a contract notice or, for example, a contract modification is published for a contract award notice. Can notices for ongoing procurement procedures continue to be sent to the data service in TED 2.0.9 XML format until the cut-off date of 25.10.2023 or should they be sent directly to TED as before until the cut-off date?

Until eForms-DE becomes mandatory, the old format can be submitted directly to TED. For future submissions to the Public Procurement Data Service, only the new format of the eForms-DE standard can be used.
</details>
<br>

<details>
<summary>
Will it be possible to send corrections to the data service, which will submit them to TED as a separate, new eSender Hub, even if the notices were previously submitted to TED by the platform operator as a former eSender Hub? <br>
More precisely:

- How is a change of eSender for an announcement handled if it is to be corrected?
- How is a change of eSender handled within a procedure with multiple notices?
</summary>
<br>
It will not be possible to use the data service to query the status of an old announcement or to stop an old announcement that was not submitted via the data service, as the data service cannot perform queries on announcements from other eSenders. This is a restriction imposed by TED on submitting eSenders.

In principle, it is possible to correct an announcement by sending a new version of an announcement in eForms format to the data service before publication. This update is then sent to TED and TED publishes the latest version of the announcement. If the original announcement has already been published, a "change notice" must be sent.

It is currently being clarified with TED how a previous announcement in the old format can be referenced in order to link them together and to what extent the change of the submitting eSender has an influence on changes.
</details>
<br>



<details>
<summary>
Is OPP-090-Procedure used exclusively for the case of old notices (old TED scheme) with further processing in eForms?
 </summary>

Both change notices and therefore the "Change Notice Version Identifier" (BT-758) as well as the "Framework Notice Identifier" (OPT-100) and "Previous Notice" (OPP-090) are TED-specific solutions that can be used directly.

</details>
<br>

### Accepted SDK versions

<details>
<summary>
As far as we know, the eForms-DE format is no longer compatible with the eForms-EU format, as it is no longer a pure subset of it. This means that no API functions of the EU can be called with the eForms DE format, be it the new eForms API or the APIs of the viewer services (PDF/HTML rendering). Is it correct that the new data service does not offer a render method and that the EU render methods can no longer be used due to incompatibility? How can functions such as PDF/HTML rendering still be used?
</summary>
<br>

Question 2 under [Roadmap](#roadmap) - The need for a rendering method has already been recorded and is currently being analyzed.

The eSender Hub will ensure that this announcement is transformed into a valid eForms-EU document in accordance with the eForms-DE version submitted in order to be able to use the TED functions.
</details>
<br>

<details>
<summary>
 Which versions of the eForms-DE standard are currently supported? (added on (29.09.23)
</summary>
<br>
In October 2023, the Public Procurement Data Service will support versions 1.0 and 1.1 of the eForms-DE standard, technically this corresponds to a CustomizationID (see field OPT-002-notice) with the values "eforms-de-1.1" or "eforms-de-1.0". To support the implementation, the SDK-DE versions SDK-DE-1.1.0_1.7.1 and SDK-DE-1.0.1_1.5.3:20230727 are currently available at https://gitlab.opencode.de/OC000008125155/SDK-eforms-de.
</details>
<br>

<details>
<summary>
Currently, Mediator also seems to accept eForm-EU up to SDK version 1.5. How long will this still be available? The background to this is that contracting authorities often require a longer period of time (often weeks) between the creation of the contract notice (or start of the procedure) and its publication. Therefore, a longer period is necessary between the start of production of eForms-DE and the shutdown of eForms-EU.
</summary>
<br>
It is currently planned to switch off support for eForms-EU 1.5 with the release in July, as it is also not supported in the announcement service. If it is necessary to support this or other EU versions for longer, this can be discussed.
</details>
<br>

### Special cases

<details>
<summary>
Will there be corresponding procedure models for any rare, but conceivable, special cases that can be invoked if the cases occur?
 </summary>
 Here are two examples:
Example 1:<br>
The Vermittlungsdienst accepts a notice which is valid according to the Vermittlungsdienst/eSenderHub. The EU later rejects acceptance ("rejected" status), for example because the SDK version is no longer supported. The platform operator receives the status "internalError" according to the status mapping. What would the next steps be in this case?<br>
Example 2:<br>
According to the EU, a business rule will soon be introduced that no longer allows the "dispatch date" in a notice (date of dispatch of the notice), which is set by the platform operators and the time of transmission of the data service to the EU, to deviate by a maximum of 24 hours, otherwise acceptance by the EU will be blocked. Any technical problems in the data service must therefore always be resolved within 24 hours.

<br>
There will be a support structure to respond to error states (InternalError status) or bugs. It is currently being clarified what this support structure will look like and when it will be operational. From June onwards, Nortal will be the first point of contact at the e-mail address support-oeffentlichevergabe@bdr.de. Whenever errors occur in the system (e.g. rejection by TED), these will be logged so that a support ticket can be created and a technical analysis carried out if necessary.
</details>
<br>



# Standard eForms-DE and SDK-DE

[Back to top](#frequently-asked-questions)<br>

**Please note that we answer all questions regarding the eForms-DE standard according to our current state of knowledge. The information is subject to change at any time**.

**For further questions about the <u>eForms-DE</u> standard, please contact the Coordination Office for IT Standards (KoSIT) as the operator by e-mail: eforms@finanzen.bremen.de**

**If you have any further questions about the <u>SDK-DE</u>, please contact Bundesdruckerei's support team by e-mail at [support-oeffentlichevergabe@bdr.de](mailto:support-oeffentlichevergabe@bdr.de)**, stating explicitly which version of the SDK-DE you have questions about.

## General questions

<details>
  <summary>
    Are there any requirements for the language of the announcement or multilingualism?
  </summary>
  <br>
  Although there is no statement on the choice of language for invitations to tender in the procurement regulations, Section 23 (1) of the Administrative Procedure Act (VwVfG) stipulates that the official language is German. Accordingly, it is to be expected that German authorities must always prepare their documents at least in German. Multilingualism is of course possible and permitted.
  For publishing entities that are not classified as public authorities, publication without German is fine. As of 31.01.2024, the rule CR-DE-26 for BT-300 is temporarily deactivated for validation in the Vermittlungsdienst, but the error is still returned in the online validator (validator.ozg-vermittlungsdienst.de).
</details>

## Questions about the SDK-DE

<details>
<summary>
Where can I find the latest version of the SDK-DE, which is supported by Datenservice Öffentlicher Einkauf (DÖE) and conforms to the German eForms-DE standard? (updated on 16.11.2023)</summary>
<br>


The SDK-DE can be found at https://gitlab.opencode.de/OC000008125155/SDK-eforms-de.<br>The latest version of the SDK-DE belonging to the standard eForms-DE version 1.1.0 published on [xeinkauf.de](https://xeinkauf.de/eforms-de/) is **1.1.0_1.7.2**:

https://gitlab.opencode.de/OC000008125155/SDK-eforms-de/-/releases/SDK-DE_1.1.0_1.7.2<br>

</details>

<br>

## Questions about Business Terms and Groups (BT/BG)

Sorted by BT/BG number.

### Procurer legal nature (BT-11) and CPV
<details>
<summary>
CPV code Main subject and cross-dependencies to the legal form of the bidder. Restrictive rule BR-BT-00262-0211 of the EU. (updated on 27.09.23)</summary>
<br>

According to this rule, recipients of grants under VgV can only tender for construction services, but not services. Even in award procedures under SektVO, KonzVgV or VSVgV, there are restrictions on the selection of forms applicable in an award procedure for grant recipients issuing tenders compared to other awarding bodies, which is incomprehensible.

**This is a BUG in TED. This has now been fixed and is built into both the DÖE and the SDK from version 1.1.0_1.7.2;
https://gitlab.opencode.de/OC000008125155/SDK-eforms-de/-/blob/SDK-DE_1.1.0_1.7.2/sdk/examples/de/notices/ContractAwardNotice_CVD3.xml?ref_type=tags**
</details>
<br>

### BT-743 (electronic invoicing) must be set to "required"
<details>
<summary>
BT-743 (Electronic invoicing) must be set to "required" by an EU rule as soon as the legal basis BT-01 is not set to "Other" </summary
<br>

TED will unfortunately only fix this error of an overly strict rule regarding BT-743 (electronic invoicing) in version 1.10 of the TEd-SDK and higher, but not for previous versions. Platforms that send notices to the Datenservice Öffentlicher Einkauf Vermittlungsdienst in Germany will unfortunately have to deal with the error until the expected introduction of SDK-DE 1.2.0_1.10.0 in February 2024 and the subsequent implementation in the awarding platforms or editorial system.

As a transitional solution until then, contracting authorities can enter "required" in BT-743 (Electronic invoicing), but then note in BT-77 (Provisions - Financing) that although "required" is entered in BT-743, this is NOT "required" according to this regulation, but that electronic invoicing is "permitted" and desired instead.

**This is a BUG at TED. This will be fixed in 1.10 and therefore in eForms 1.2. The above workaround must be used for older versions **.
</details>
<br>

### Announcement of results (BG-7), Offer (BG-320 Offer)
<details>
<summary>
In the element "Announcement of results" (BG-7) > "Tender" (BG-320), should only awarded tenders/lots or all tenders/lots received be listed?
</summary>
<br>

In this question, the provisions of the respective directives and regulations under which the award procedure falls continue to apply.
</details>
<br>

### No immediate publication (BG-8; BT-195/BT196/BT197/BT-198)
<details>
<summary>
Why is it mandatory to specify the time limit for fields that are not to be published for mandatory fields?
</summary>
<br>

The specification follows the EU Implementation Handbook on this point. It is a target formulation that does not require a business rule.
Details: https://op.europa.eu/en/publication-detail/-/publication/73a78487-cc8b-11ea-adf7-01aa75ed71a1
</details>
</summary>
<br>

### Award criteria (BG-707, BG-38, BT-53 et al.)
<details>
<summary>
Are award criteria with a weighting not to be specified or optional?
</summary>
<br>

For award criteria >=10%, the information is mandatory for eForms-en; for award criteria <10%, the cardinalities of the information provided by TED currently remain unchanged.

It is strongly recommended to also enter the information for the award criteria whose weighting is below 10% in order to comply with the 100% rule of TED.
</details>
</summary>
<br>

### National exclusion grounds (BT-67 exclusion grounds)

<details>
<summary>
Why have the codes for national exclusion grounds of the code list "Criterion Exclusion Grounds" been changed in the eForms-DE v1.1.0 version?
</summary>
<br>

Only the codes "ex-os" (exclusion grounds upper threshold) and "ex-us" (exclusion grounds lower threshold) have been removed, as the existing EU code "nati-ground" (purely national exclusion grounds) can be used instead.

We have updated the changelog for you: https://projekte.kosit.org/eforms/eforms-de-codelist/-/blob/main/CHANGELOG.md.
  </details>

<details>
<summary>
Which exclusion reason can be preset if all reasons apply equally?
</summary>
In the event that all exclusion grounds apply equally, "nati-ground" (purely national exclusion grounds) is the most comprehensive code.
</details>
<br>

<details>
<summary>
Why does the ARC require mandatory grounds for exclusion to be selected or stated in a contract notice at all?
</summary>
 The motivation is that tenders not only refer to national laws, but also explicitly list exclusion grounds, in particular for the sake of transparency, even for bidders from abroad.
 </details>
<br>

<details>
<summary>
What should an awarding authority enter in the "Description" field (BT-67(b) procedure) for each selectable exclusion reason?
</summary>
The presentation was chosen uniformly for EU-wide and national procurement procedures.
In BT-67, an explanation of the reasons for exclusion can be entered.
</details>
<br>

### Earlier planning (BT-125)
<details>
<summary>
How are the fields OPP-090-Procedure, BT-125-Lot and BT-1251-Lot to be filled technically (permitted characters) and professionally?
</summary>
<br>

The BT-125(i) & OPP-090 are specified with the UUID (publication number) of the EU prior information notice or with the Official Journal number in order to also refer to older prior information notices.

For BT-1251, only a length restriction of 30 characters is specified in the SDK.
</details>
<br>
<details>
<summary>
For which case is BT-125-Lot and BT-1251-Lot used?
</summary>
<br>

An awarding authority has published a prior information notice in which it announces that an invitation to tender for subject X is to take place soon. This prior information notice is now given an announcement number. Some time later, the contracting authority invites tenders for subject X in a contract notice (CN). The publication number of the prior information notice is now entered in BT-125(i) in order to refer to the prior information notice that was published some time ago.
BT-1251 is a specification of where information on subject X was provided. This is done in the prior information notice in Parts. So BT-1251 is the information in which part of the prior information was provided.
</details>
</summary>
<br>


### Display of the winner in an award notice (supplemented 27.10.23)
(BT-142, BT-13713, , OPT-320, BT-13714, , OPT-310, OPT-300, BT-721, BT-145, BT-1451, BT-768, BT-3202)
 <details>
<summary>Abbreviated version
 </summary>

<br>

Please note that in eForms, contractors and clients are stored in different places in the eForms structure for awarded tenders (contracts).

The client is stored in the Contract structure.
An offer is assigned to a contract and bidders are assigned to the offer. These bidders represent the contractors of the contract.

The following long version describes exactly what needs to be done to enable this backward linking and to ensure correct display in the contract notice service.
</details>
<br>
 <details>
  <summary>Long version
  </summary>

<br>
The following illustration is intended to help you complete the eForms form for the notification of results (CAN) so that the associated awarded contracts can be displayed correctly in the notification service (www.oeffentlichevergabe.de).
These completion instructions are aimed at specialist procedure manufacturers for the technical implementation of the following fields in the specialist procedure. If necessary, this can be used as a guide for users. For this reason, the technical field identifiers and their German interface designations (used in accordance with the eforms-DE standard, if available, otherwise those from the SDK-DE) are specified:
<br>

1. description of the results of the tender
    The results of an alert are stored in the XML in the <efac:NoticeResult> section. In the following sections, only the sub-sections that are required here to output the expected results in the announcement service are described.

2. description of the results of a lot
   
    The BT-142 (winner determined, <cbc:TenderResultCode listName="winner-selection-status">) is located in the form module "Lot result" (<efac:LotResult>). Behind this is a code list with the following values:

       a. A competition winner has not yet been determined, the competition is not yet closed.

       b. No competition winner has been determined and the competition is closed.

       c. At least one winner has been determined (code: selec-w).

    Only in the event that "c" was selected can a result be reported for this lot and at least the winning bid for this lot must be indicated. If several bids have been awarded, all winning bids must be listed below. In the section "Lot result" (<efac:LotResult>), the relationship between the lot <efac:TenderLot> , BT-13713-LotResult, (procedural result lot identifier) and the tender (<efac:LotTender>, OPT-320-LotResult) is established.

3. description of the tender
   
    The description of the tenders takes place in the form module "Tenders" (<efac:LotTender>)
    Here it is important to set an internal form reference number to the offer, as this should already be used in the previous section, for example - in the reference to the offer (see <efac:LotTender>, OPT-320-LotResult in section 2). Here, too, the LOS to which the tender refers must be referenced again (in the Tender Lot ID field): <efac:TenderLot>, BT-13714-Tender>. In addition, a further reference must now be inserted at this point to the section
    <efac:TenderingParty> in the OPT-310-Tender field (identifier - bidder). This reference refers to the "Bidder" form module, which is described below.

4. description of the bidder(s) for a tender

    In the form module "Bidder" <efac:TenderingParty>, the details of the bidder(s) of a tender(s) must be stored. The main purpose here is to indicate whether the tender was submitted by an individual bidder or by a bidding party or by a bidder who will employ subcontractors. Only references to the bidder organizations are therefore required here. If it is a bidder in this tender, then the reference to the bidder organization must be entered in the <efac:Tenderer> OPT-300-Tenderer (ID - Bidder ) field.
    The field efac:Tenderer/efbc:GroupLeadIndicator OPT-170-Tenderer (head of the tenderer) must also be completed for each specified tenderer. At least one of the specified bidder organizations must be qualified as "leader of the tender". Bidding parties that have joined forces in subcontracts can also be specified here (however, the corresponding description of these fields is omitted here).

5. description of the contract
    
    Once the above requirements 2-5 have been fulfilled, the relationships that represent the technically interesting part of the contract notice service, namely the contracts that have been concluded for a lot, can be mapped. This is done in the form module "Orders" ("Contracts") <efac:SettledContract>.
    The following information should be entered in this section
  
      BT-721-Contract - Name of the contract

      BT-145-Contract - Date of conclusion of the contract

      BT-1451-Contract - Date of decision on the winner

      BT-768-Contract - Order as part of a framework agreement.


The following field is the most important for determining the winner:

BT-3202-Contract - Order Bid ID, as this field is used to determine the underlying bid in a backward chaining process and the bidder or head of a bidding consortium who signed the contract for the bidders

In order to also be able to map which organization on the client side signed the contract, the following field should also contain ID - contract signatory <cac:SignatoryParty> (OPT-300-Contract-Signatory) with a reference to the organization on the client side that signed the contract.

Setting up these references in this way according to the pattern described also fulfills another purpose: only if all references exist correctly can the requirements of BT-165 (Company size) must be filled in and BT-706 (Nationality of the beneficial owner of the winner) must be filled in, of the eForms-DE standard be fulfilled.

 </details>

 </summary>

<br>

### Identification number (organization) (BT-501) Route ID
<details>
<summary>
What identifier must be entered for BT-501? (updated on 25.10.2023)
</summary>
<br>
 In principle, the choice of a unique identifier lies with the respective organization itself. Requirements for this identifier are

* It must be unique, i.e. there must be no other organization with the same identifier
* This should be used sustainably across all announcements

The use of the routing ID is recommended for public administration (as this is already frequently used for electronic invoicing). This has the following form:

0204:Routing ID

Example (fictitious):

0204:991-1234512345-06

The format specification of the routing ID (version 2.0.2) can be viewed and downloaded via the following link:

https://leitweg-id.de/wp-content/uploads/2021/08/Leitweg-ID-Formatspezifikation-v2-0-2.pdf


As long as or to the extent that this is not available, another unique identification number must be specified temporarily. If there is no other unique identification number, a telephone number of the organization can also be entered as a unique identification number. This should then have the following form:

`t:03023125000`

This should be entered with a prefix (t:), area code, without special characters and without spaces, as in the fictitious example.

**Notes for awarding chambers:**

We recommend using the identifiers in the table below for the awarding chambers. These are taken from the following page, among others:

https://www.bundeskartellamt.de/DE/UeberUns/LinksundAdressen/Vergabekammern_der_L%C3%A4nder/Vergabekammern_artikel.html


| Federal/Federal State | Authority | Identifier |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------|-------------------|
|Bund|Federal Procurement Chambers|t:022894990|
| Baden-Württemberg |Vergabekammer Baden-Württemberg | 0204:08-A9866-40 |
| Bavaria | Northern Bavaria Chamber of Public Procurement at the Government of Middle Franconia | t:0981531277 |
| Bavaria|Government of Upper Bavaria Procurement Chamber of Southern Bavaria |t:08921762411 |
| Berlin| Public Procurement Chamber of the State of Berlin | 0204:11-1300000V00-74 |
| Brandenburg| Public Procurement Chamber of the State of Brandenburg at the Ministry for Economic Affairs and Energy | t:03318661719 |
| Bremen | Public Procurement Chamber Bremen Senator for Construction, Mobility and Urban Development | t:042136159796 |
| Hamburg| Public Procurement Chamber at the Finance Authority | t:040428231690 |
| Hamburg|Awarding Chamber at the Authority for Urban Development and Housing |t:040428403230 |
| Hesse| Procurement Chamber of the State of Hesse at the Darmstadt Regional Council | t:06151126603 |
| Mecklenburg-Western Pomerania| Public Procurement Chambers at the Ministry of Economics, Labor and Health | t:03855885160 |
| Lower Saxony| Public Procurement Chamber of Lower Saxony at the Ministry of Economic Affairs, Labour and Digitalization of Lower Saxony | t:04131153308 |
| North Rhine-Westphalia| Rhineland Public Procurement Chamber via Cologne District Government | t:02211473055 |
| North Rhine-Westphalia|Westphalia Chamber of Public Procurement | t:02514111691 |
| Rhineland-Palatinate| Rhineland-Palatinate Public Procurement Chamber at the Ministry of Economic Affairs, Transport, Agriculture and Viticulture | t:06131162234 |
| Saarland| Public Procurement Chamber of the Saarland | t:0681501994 |
| Saxony| Public Procurement Chamber of the Free State of Saxony at the State Directorate of Saxony | t:03419773800 |
| Saxony-Anhalt| 1st and 2nd Public Procurement Chamber of the State of Saxony-Anhalt | t:03455141529 |
| Schleswig-Holstein| Schleswig-Holstein Public Procurement Chamber at the Ministry of Economic Affairs, Transport, Labor, Technology and Tourism of the State of Schleswig-Holstein | t:04319884640 |
| Thuringia| Public Procurement Chamber of the Free State of Thuringia at the Thuringian State Office of Administration | t:0361573321276 |
|<br>||||
|</details>||||
|<br>||||
</details>

### New edition of the procedure (BT-634)

<details>
<summary>
What is the benefit of BT-634-Lot in the CN if it is not yet possible to assess whether the procedure/lot needs to be re-tendered at the time the contract notice is drawn up?
</summary>
<br>

The name for BT-634 (new edition of the procedure) is less confusing in English: "Relaunch". The BT-634 should therefore not be used for an indication in the future, but as an indicator of whether a procedure or lot for the advertised item already existed and was canceled in the past. The BT-634 can then be used at procedure or lot level to indicate whether this notice is the "restart" for the annulment of a previous notice.
  </details>
<br>


### Vehicle class (BT-723)
<details>
<summary>
 Help for selecting the values of the code list for BT-723 vehicle class
</summary>
<br>

Assistance can be found in Annex II of the framework directive https://eur-lex.europa.eu/legal-content/DE/TXT/HTML/?uri=CELEX:32007L0046:
|Code|Meaning|
|---|---|
|M1|Light commercial vehicle of vehicle category M1 or passenger car (motor vehicles for the carriage of passengers with no more than eight seats in addition to the driver's seat).
|M2|Light commercial vehicle of vehicle category M2 (motor vehicles for the carriage of passengers with more than eight seats in addition to the driver's seat and a maximum permissible mass of up to 5 tons).
|N1|Light commercial vehicle of vehicle category N1 (motor vehicles for the carriage of goods with a maximum authorized mass of up to 3.5 tons).
|N2|Heavy commercial vehicle of vehicle category N2 (motor vehicles for the carriage of goods with a maximum permissible mass of more than 3.5 tons and up to 12 tons.)|
|N3|Heavy commercial vehicle of vehicle category N3 (motor vehicles for the carriage of goods with a maximum permissible mass of more than 12 tons.)|
|M3|Bus of vehicle category M3 (motor vehicles for the carriage of passengers with more than eight seats in addition to the driver's seat and a maximum permissible mass of more than 5 tons).

</details>
<br>

### (Particularly) suitable for SMEs (BT-726)

<details>
<summary>
Blurring due to the relationship between "Particularly suitable for SMEs" (BT-726) and the collection of structured data in the unstructured data field "Additional information" (BT-300)
</summary>
<br>

The parties involved are aware of the imprecision resulting from the collection of structured data in unstructured fields, but are currently considered acceptable. The approach is seen as an interim solution and work is continuing on a "clean" solution.
This is being done in consideration of the fact that the BKMS will be able to evaluate any data immediately from October 25th
  </details>
<br>

<details>
<summary>
Does the data service remove this information, or is it also sent to the EU?
</summary>
<br>

The eSender Hub does not remove this data, the entries from this field are also forwarded 1:1 to the EU. As this is a text field, there is no technical problem here. Only one value can be inserted at the beginning of the text field: #Specially suitable for:{freelance OR self OR startup}#'. After this value, however, further explanations can be inserted as free text.
  </details>

<br>
<details>
<summary>
Do the values in brackets also have to be sent? e.g. freelance (particularly suitable for freelancers)
</summary>
<br>

No, these values are essential for a better understanding of the codes
  </details>

<br>
<details>
<summary>
What about localization if, for example, the language of the announcement is English and then the free text field BT-300 contains German terms (also with regard to the umlaut in Selbstständige)?
</summary>
<br>

In principle, there is no automatic translation of field contents, i.e. German terms in the fields remain German. The EU has not yet decided on a uniform approach to localization.
  </details>

<br>
<details>
<summary>
Can further information be written to the field, e.g. by the user or automatically by the application?
</summary>
<br>

It is possible to add free text after the code as long as the total character limit is observed. The following note has been added to BT-300 for clarification:
"To the extent that it is necessary to specify one of the codes (freelance, self, startup) because of rule BR-DE-26, the code must be specified on the first line and separated from other additional information by two blank lines. The format of the first line is defined as follows: #Specially suitable for:{freelance|self|startup}."
  </details>
<br>

### Preferred publication date (Requested Publication Date BT-738)

<details>
<summary>
New features and details (added on 27.09.23)
</summary>
<br>

- Date of publication of eForms notices on TED: no longer 5 fixed calendar days

- Possibility to set a preferred publication date (BT-738)

- If no date is specified, TED will publish "As soon as possible", i.e. in the next available OJS issue

   --> Announcement can appear in TED at 9:00 a.m. the next morning; maximum 2 working days

   --> less time to stop the publication

- If a date is specified, TED will publish on the preferred date or in the next available OJS issue after that date
  
   --> see TED publication calendar for working days

   --> preferred publication date can be up to 60 days in the future

- The working day before the expected publication date:
  
   --> daily export on working days between noon and midday - notification is included in OJS output
  
   --> overnight to "publication" status (or over the weekend or on public holidays)
  </details>
  <br>

### BT-1501(n) Linking of old SIMAP/non-eForms notices
<details>
<summary>
What ID do I need to use to link to old notices prior to the eForms commitment?
<br>
Please use the Notice Publication ID or document number, which is uniquely assigned by TED for each notice. This can be seen both in the search results of the notices on the TED website in the column 'Document number' and in the direct link from TED to the notice as well as in the detail page of the notice in the heading. It consists of a series of numbers, a hyphen and the year of publication of the announcement. e.g. 1234576-2022. The number of numbers before the hyphen may vary.
  </details>

### BT-1501(s)-Contract
<details>
<summary>
What value do I need to use for BT-1501(s)-Contract?</summary>
<br>
Please create a contract and then link its ID in this field. This can have the value CON-0001, for example.
</details>


### Lots
<details>
<summary>
How are the LOT entries to be used for "none", one or more lots?
</summary>
<br>

According to TED, if there is 'no' lot, there must only be one technical lot entry with the value LOT-0000.
If there are two lots, there are two lots with the values LOT-0001 and LOT-0002. For 5 lots, for example, LOT-0001, LOT-0002, LOT-0003, LOT-0004, LOT-0005. The structure of LOT-0000 is completely identical to that of any other LOT, including LOT-0001. Only the ID is different.

Documentation can be found here: https://docs.ted.europa.eu/eforms/1.5/schema/procedure-lot-part-information.html
</details>
<br>

<details>
<summary>
While reviewing the documents of the national tailoring, some inconsistencies regarding lot groups have been discovered. According to eForms-DE standard v1.0.0 and v1.0.1, the optional fields of the group "Award - groups of lots" or "Framework agreement, lot group, maximum value" are marked with number "0" and should therefore not be able to be used. In SDK-eForms-DE v1.5.1, which is based on the eForms-DE standard v1.0.0, however, the fields appear in fields.json. How should lot groups generally be handled in future?
</summary>
<br>

For the sake of simplicity and to avoid inconsistencies with Schematron rules supplied by the EU, the SDK for the national eForms-DE standard contains fields at a technical level that are not used in accordance with the eForms-DE standard.

Lot groups are not provided for in eForms-DE.
</details>
<br>

### NUTS codes

<details>
<summary>
Is there a code list with country codes where it is not possible to specify the NUTS code?
</summary>
<br>

Country-specific NUTS code lists are available in the TED SDK (https://github.com/OP-TED/eForms-SDK/blob/1.7.0/codelists/country.gc )
  </details>
<br>

<details>
<summary>
Conversely, if you can specify NUTS codes, do you never have to specify the country?
</summary>
<br>

As the country is part of the NUTS code, it is not necessary to specify it separately.
  </details>
<br>

<details>
<summary>
Is it still mandatory to specify the NUTS lvl3 codes?
</summary>
<br>
Yes, if NUTS codes are available, they must be provided
</details>
<br>

# General
[Go to top](#frequently-asked-questions)

### eNotices portal of the EU

 <details>
<summary>
Information from TED as of 27.09.23

 </summary>

<br>

- For API submissions, NoticeAuthorEmail should be the buyer's email - eSenders must specify the true email address of the originator in the metadata

- Notice author email receives notifications of status changes:
       --> Submission, Validation Failed, Stopped, Not Published, Published
  
- The eSender receives a copy to the e-mail address used by EU Login for the API key.

- Ongoing improvements to the content and translation of these email notifications
  
- New feature coming soon: Buyers will receive an email notification when an announcement with the same buyer name has been published

- Note for API testing (risk of receiving many emails): use a unique "main buyer name" for recurring buyers and a random name for multiple buyers
  
- Vermittlungsdienst API parameter: authorEmail
               Please enter the email of your end customers accordingly**
           </details>
           <br>

<details>
<summary>
According to the EU (see https://simap.ted.europa.eu/de_DE/web/simap/statistical-production-files - Statistics 2023 by format and transmission channel), many contracting authorities have so far used the EU portal eNotices to create and publish the contract notice. eNotices2, the new portal with integrated eForms, does not recognize or take into account national tailoring. May contracting authorities continue to use eNotices2 even though it does not take national tailoring into account?
</summary>
<br>
eNotices2 may no longer be used for above-threshold submissions from 25.10., as the adjustments to the eForms standard would not be taken into account, so that direct submission via eNotices2 to TED is no longer legally permissible.
</details>
<br>

<details>
<summary>
Will there be a new portal for interested companies to replace the current service.bund.de site?
</summary>
<br>
There are no plans for another portal to replace sevice.bund.de. The project wish is for all notices (upper and lower threshold) to be available in the Public Procurement Data Service.
</details>
<br>

<details>
<summary>
Is there a mapping from XVergabe to eForms?
</summary>
<br>
The XVergabe standard will be permanently replaced by eForms-DE and will not be further developed. The degree of coverage of the information contained varies greatly. No mapping from XVergabe to eForms is provided by Datenservice Öffentlicher Einkauf.
</details>
<br>

---
[Back to top](#frequently-asked-questions)
