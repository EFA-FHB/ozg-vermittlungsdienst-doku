### EfA Implementation Project "Access to Public Procurement".
# Frequently asked questions

- [Data service public procurement](#datenservice-öffentlicher-einkauf)
- [Standard eForms-DE and SDK-DE](#standard-eForms-DE-and-SDK-DE)
- [General](#general)

## data service public purchase

### Connection

<details>
<summary>
What information is needed to apply for an account? (updated 10/11-23)
</summary>
<br>

As of 04.10, accounts are to be applied for in the [Self-Service Portal](https://portal.ozg-vermittlungsdienst.de). All needed information is requested in the registration form for a VD account. These are:

<br>

- System environment for which access data is requested (preview, staging, production). Registration in the portal is for the corresponding environment, i.e. if an account is required for the staging environment, this should be requested in the staging portal.

- Email address to be used as username (this must be unique per environment, no duplicates allowed).
  
- URL of the staging platform on which the notices will be published.
  
- First and last name as well as the e-mail address of the representative of the FVH (specialist procedure manufacturer)
  
- Name of the FVH
</details>
<br>


<details>
<summary>
One email address must be specified as the username per registration. Is it possible to specify the same email address for multiple systems?
</summary>
<br>
Generally, we request two emails per account (sometimes referred to as a client): An account email to activate the account and a contact email. An individual email per account is required for activation, to set the password for the account and to enable unique authentication with the email and password combination. However, the account email can also be a functional mailbox and is only needed to manage the account. The contact email address will only be used if questions arise during operation regarding an announcement sent from this account. Contact email and account email may be identical if needed and the same contact email (e.g. a central contact person) may be used for multiple accounts. However, you may reuse your account email once each between system environments, for example the same account email address for Preview, Staging and Production. In general, we recommend one account per award platform.
</details>
<br>

<details>
<summary>
When creating an account, a contact email of a FVH must be specified. What is this used for?
</summary>
<br>
This email is used when we want to proactively reach out to you. This may be the case if, for example, there are anomalies with their account or the notices posted, or if we are sending general information to all account owners.
</details>
<br>

<details>
<summary>
Can multiple accounts be applied for at the same time? How many accounts are recommended for each of preview and staging?
</summary>
<br>
The URL of the awarding platform is purely for the assignment of accounts/clients, this has nothing to do with the link to the award documents.

Some awarding platforms use e.g. Dropbox or google drive or similar for hosting the award documents, which is why it is not possible to clearly identify the platform behind it. For this reason, this information is additionally necessary. The link to the tender documents remains in the XML document and is primarily displayed in the BKMS interface. The link provided during account creation is only displayed in the bottom right corner, below the announcement itself, as a disclaimer/source.
</details>
<br>

<details>
<summary>
What is the difference between the procurement platform URL requested during account creation and the link to the procurement documents in the eForms document?
</summary>
<br>
Feel free to send us a list of required accounts to support-oeffentlichevergabe@bdr.de Including all required information per account. We recommend using exactly as many accounts on staging as you plan to use for production. In addition, of course, any number of test accounts are possible on Preview and Staging.  
</details>
<br>

<details>
<summary>
On staging or preview, is the release cycle and validation done the same way as in production, or are the status changes accelerated? What delays should be expected between acceptance and release?
</summary>
<br>
In all environments, the same validation and delay in publishing is performed as in the production environment. In this case, the time delays are at TED (publication on weekdays at the earliest on the next working day if accepted by 4pm) or the legally required logic of national publication (forwarding to BKMS) after 48h at the earliest. The BKMS publishes immediately when an announcement has been received, unless the preferred publication date is in the future. In this case, the publication in both TED and BKMS would only take place on the requested day under the restrictions applicable at TED (e.g. no publication on weekends).
</details>
<br>

<details>
<summary>
To request access, the URL of the awarding platform should be specified. What is the purpose of this specification?
</summary>
<br>
The purpose of specifying the URL is to be able to distinguish between the systems mentioned, to provide you with correct access, and to avoid duplicates. Award platforms are the systems where notices are published, so the URL of the award platform can be e.g. alpha.oeffentlichevergabe.de (test environment BKMS). This URL is used to identify on which platform you are currently publishing your notices. On this topic, we are aware that there may be different procedures here depending on the structure of the system of the respective FVH. In principle, you will need one account per system that is to deliver to the switching service in the future. If you are unsure which systems/platforms are to be connected to the DöE for you, we will be happy to support you in this decision. Please feel free to send us an inquiry at support-oeffentlichevergabe@bdr.de.
</details>
<br>

<details>
<summary>
What is the system environment to which our test systems can send announcements? What is the difference between the preview and staging environment?
</summary>
<br>
The preview environment is for testing only. Updates are often pushed in here and this is also our testing environment for future releases. The staging environment is a 100% copy of the production environment and should only be used for production related testing. Both environments deliver into the alpha environment of BKMS and TED Preview. On staging, your tests should be run exactly as you plan to do in production. In principle, however, both environments are suitable for testing.
</details>
<br>

<details>
<summary>
Will the data service provide a render method analogous to the EU render methods?
</summary>
<br>
A notice viewer for rendering eForms-DE documents in HTML is already in the works and is expected to be released in mid/late September. The endpoint has already been published in the mediation service on the preview environment so the endpoint can already be included. This will return a rendered sample file. We welcome feedback and suggestions at support-oeffentlichevergabe@bdr.de.
</details>
<br>

<details>
<summary>
Where can examples of eForms-DE be found? What are the different types? ?
</summary>
<br>
Example documents for eForms-DE can be found in the schematron repository of KoSIT: https://projekte.kosit.org/eforms/eforms-de-schematron/-/tree/main/src/test/eforms-de-base-samples
Via the respective tags and releases the different versions of the documents can be retrieved.

The abbreviations are to be understood as follows:

PIN
Eng: Prior Information Notice
Deu: Prior Information
Subtype 1-14, E2
PINs are notices published before the start of the "call for competition".

CN
Eng: Contract Notice
Deu: Open Procedure / Public Invitation to Tender
Subtype 15-24, E3
CNs are notices that initiate the "call for competition".

CAN
Eng: Contract Award Notice
Deu: Contract Award Notice.
Subtype 25-40, E4
CANs are used to create Notices of Results that are published shortly after the contract is signed. They refer to the notice and contain information about the award process, such as the contract award, winner, etc.

The naming of the sample documents is about the following:

eforms = standard document type
PIN/CN/CAN = see above; designates the type of announcement
number 1-40 or E1-E4 = subtype of notice, where E is for subliminal notices
DE = standard is eForms-DE
(in)/valid = whether the file is valid or invalid according to the specification eForms-de
There is currently not an example file for all announcement types. If you need an example for a certain type that does not exist in the previously mentioned link, we will be happy to forward a request for it. Unfortunately, the EU does not provide examples for all announcement types either, so providing example is sometimes quite time consuming.
</details>
<br>

### Roadmap

<details>
<summary>
Is there a roadmap regarding the further development even after the cut-off date of 10/25/2023 of the components switching service, eSenderHub, etc., especially with regard to feature and API enhancements, milestones and the respective go-live dates?
</summary>
<br>
As of this writing, there are two releases planned for the data service after 10/25/2023. The content of the releases is primarily related to convenience features and reporting capabilities. API changes and enhancements are not planned according to the current planning status.
</details>
<br>

<details>
<summary>
What features (apart from the scope of the Production Release) are still in the planning stage? This question is especially aimed at the other services of the EU portal "eNotices2", such as generation of PDF representations, viewing and intervening in processes via a web interface, entering notices via web interfaces, etc., which are no longer usable due to the central eSender service.
</summary>
<br>
Generation of PDF/HTML representation: currently being clarified, the need has been acknowledged by the project.

Insight into process via web interface (dashboard):
Currently in implementation: planned is to view status information for a client and possibly use the stop endpoint via the same interface.
</details>
<br>

<details>
<summary>
Will there be a roadmap regarding the further development of the SDK? This is interesting for platform operators especially against the background of the adjustment times to new SDK-EU versions, since the SDK-DE and SDK-EU currently still diverge in their versioning.
</summary>
<br>

The version designations of the SDK to the respective national standard eForms-DE are based on the version designations of the standard eForms-DE. For each eForms-DE SDK it is indicated on which European SDK version it is based. (see also explanation on https://gitlab.opencode.de/OC000008125155/SDK-eforms-de)

It is not planned that for each minor version of eForms-EU also a new version eForms-DE will be published. Therefore the versioning of eForms-EU and eForms-DE will not match directly in the future. However, there will always be exactly one corresponding eForms-EU version for each eForms-DE version.
</details>
<br>

<details>
<summary>
In what time frame will a DE update be made available after an EU update is released?
</summary>
<br>

It should be noted here that not every EU update automatically requires a DE update.
<br>
The GDK is not the responsibility of KoSIT. However, the eForms-DE specification. As was jointly stated at the 1st technical working meeting, given still existing uncertainties about coming into force and lifetime of the versions of the EU-SDK, we cannot currently give a simple answer with clear data. What is certain is that a given version of eForms-DE will declare itself compatible with a given version of eForms-SDK and that this should happen as soon as possible. As currently eForms-DE 1.0.1 is compatible to eForms-SDK 1.5.1 (SDK 1.5.1 was released on January 20, 2023 and eForms-DE on February 5). I.e. implicitly that there will not be a version eForms-DE for every version eForms-SDK. The current eForms-DE version 1.1.0 is compatible with SDK 1.7.
</details>
<br>


### Go-Live

<details>
<summary>
What are the submission deadlines? (added 12/10/2013)
</summary>
<br>
To ensure that the notice is posted on TED on the same day, we recommend that the notice be submitted to the placement service by 11:00 PM on the same day.

Ex. for FVH:
 To ensure that the notice is sent to the switching service on the same day, we recommend that the notice be submitted to the subject process vendor by 10:00 p.m. of the same day.
</details>
<br>

<details>
<summary>
 When will the public purchasing data service start? (added 09/25-23)
</summary>
<br>
The productive start of the data service Public Purchasing is regulated by §83a of the current Procurement Regulation (VgV). This is expected to be 10/25/2023.
</details>
<br>

<details>
<summary>
Will all 40 EU notice types be supported at go-live?
</summary>
<br>
All document types from eForms-DE will be accepted (40 for the upper threshold and 3 for the lower threshold). Where necessary, these are generically converted to the eForms-EU format. This corresponds to the contents of the current eForms-DE standard.
</details>
<br>

<details>
<summary>
Is it possible to continue to submit notices via eNotices2 after 10/25/2023?
</summary>
<br>
As of 10/25/2023, all upper-threshold notices must legally be submitted in eForms-DE format via the Offentlicher Einkauf data service. Direct posting via eNotices2 is not standard compliant as it would not take into account the adaptations to the eForms-DE standard and is no longer legally permissible.
</details>
<br>

<details>
<summary>
Will the Public Purchasing data service also support the TED 2.0.9 XML format until the cut-off date (10/25/2023)? Should we continue to submit to TED using the old format until the deadline?
</summary>
<br>
Until eForms-DE becomes mandatory, it is still possible to submit directly to TED in the old format, but the Public Purchasing data service does not support this format. The data service can only be used with eForms. As of 25.10. it is mandatory to submit via the data service public purchasing with the format eForms-DE 1.0.1 or 1.1.0.
</details>
<br>

<details>
<summary>
Will there be a rollout of eForms on October 25 for both upper (EU) and lower (National) thresholds, or just for the EU level?
</summary>
<br>
Both eForms-EU and eForms-DE standards are already in place and can be used. As of October 25, EU-wide notices in eForms-DE format must be transmitted via the interface on a mandatory basis. If the interface is also to be used for national notices, this must also be done via the eForms format so that the data service can process them. To see which formats are currently supported and processed, see our preview at https://github.com/EFA-FHB/ozg-vermittlungsdienst-doku/blob/development/documentation/eForms_support.md.
</details>
<br>

<details>
<summary>
Which SDK version should be used for the productive go-live?
</summary>
<br>

The current versions eForms-DE 1.0.1 and 1.1 are supported. It is never recommended to session eForms-DE 1.1.0.
</details>
<br>

<details>
<summary>
How is a change of eSender for a notice handled when the notice is to be corrected? How is a change of eSender handled within a multiple notice process? How can corrections or references for subsequent notices be made with respect to notices submitted in the old format?
</summary>
<br>

It will not be possible to use the Data Service to query the status of an old notice or to stop an old notice that was not submitted through the Data Service, because the Data Service cannot send queries about notices sent in the old format. However, changing the eSender does not affect the ability to reference old notices.
How to reference and correct old notices is described in detail here: https://github.com/EFA-FHB/ozg-vermittlungsdienst-doku/blob/main/documentation/eForms_Erstellung.md
</details>
<br>

### Communication channels

<details>
<summary>
Accessibilities:
</summary>
*Questions and suggestions for improvement* towards the mediation service and the eSender hub can be directed to oeffentliche-vergabe@nortal.com. Alternatively, Github Issues can be created in the documentation repository and the SDK-eForms-DE repository.

For *support requests regarding the operation* of the Mediation Service and the eSender Hub, please contact: support-oeffentlichevergabe@bdr.de.

*Questions about the announcement service* can be directed to support-oeffentlichevergabe@bdr.de.

We are open to your suggestions!
</details>
<br>


<details>
<summary>
How to ensure that platform providers stay regularly informed about news regarding the data service, especially regarding new versions of the components (switching service, eSenderHub, REST API, etc.), new features, an update of the roadmap, etc.?
</summary>
<br>
A communication is done through regular informational meetings for the business process vendors, announcements via email, current roadmap, release notes and FAQ are in the published documentation repository: https://github.com/EFA-FHB/ozg-vermittlungsdienst-doku. Also available is the SDK-eForms-DE repository: https://gitlab.opencode.de/OC000008125155/SDK-eforms-de.
</details>

<br>
<details>
<summary>
How to ensure that platform providers stay regularly informed about news regarding the eForms-DE standard/ SDK-eForms-DE.
</summary>
<br>

The official publication for the eForms-DE standard is on https://xeinkauf.de/eforms-de/ .

The publication of the associated SDK takes place on https://gitlab.opencode.de/OC000008125155/SDK-eforms-de .

For publications on the organizational framework, see:

https://www.finanzen.bremen.de/digitalisierung/digitalisierung-von-verwaltungsleistungen-fuer-unternehmen/digitale-beschaffung-103422

Questions about the DE-SDK are to be opened via Issues in the repository.
</details>
<br>




### Documentation

<details>
<summary>
Does the documentation for the switching service (https://github.com/EFA-FHB/ozg-vermittlungsdienst-doku) already provide further information on the construct of the data service. To what extent is it planned to keep this up to date and, if necessary, to supplement it with information in the form of FAQs etc.? Is this GitHub documentation the official provision of information on this topic?
</summary>
<br>
The Github documentation will continue to be maintained and is the official documentation until further notice, but the final location of the doc has not yet been determined.
</details>
<br>

<details>
<summary>
For a release, how to determine which versions of the subcomponents are supported?  
</summary>
<br>

See [eForms support](/documentation/eForms_support.md) to document which eForms versions the subcomponents support.
<br>
For each release, we publish releasenotes to describe which component supports which version. As of September 13, eForms-DE 1.0.1 and 1.1.0 versions are supported in all public purchasing data service components.
</details>
<br>

<details>
<summary>
Is the documentation for the switching service (https://github.com/EFA-FHB/ozg-vermittlungsdienst-doku) the official documentation?
</summary>
<br>

Yes, the Github documentation is updated regularly and is the official documentation until further notice. The documentation will be published on the [Self-Service Portal](https://portal.ozg-vermittlungsdienst.de/) at the same time.
</details>
<br>


### Status model

<details>
<summary>
Pause, modify or cancel announcement? (added 9/27-23)
</summary>
<br>
- "Publishing" visible in eNotices2 web and API next month.
- Buyer/API can stop publishing an announcement in "Submitted" status.
- Once "Published" status is reached (i.e., on TED), the notice can be modified or the process can be continued
- Lot or procedure can be canceled via award notice without winner
- Change notice with reason "cancel" = the notice is null and void - this is possible but not recommended!
</details>
<br>

<details>
<summary>
How to track the start of the 48 hour standstill period when the notice was received by TED?
</summary>
<br>
There are two ways to read the time of successful submission to TED from the status information in the switching service. Either via the technical timestamp of when the eSender received an acknowledgement of the submission from the TED API (<tedStatus>ACCEPTED</tedStatus> tedStatusUpdate>2023-07-31T08:02:02.442Z</tedStatusUpdate>) or via the submittedAt value provided by TED when the status is requested (<ted_accepted_timestamp>). The two values are minimally apart, as there may be a minimal delay between when TED accepts the announcement and when a success message is returned to the eSender as a response.
</details>
<br>

<details>
<summary>
With the EU status change notifications, platform providers have also received further metadata on the respective status, e.g. the submission ID, the specific time of publication on TED, the OJ number, etc. With the OJ number, customers previously had the option of no longer having to manually enter these numbers for subsequent notices for this contract (indication "previous notice of the same contract"), as these could be pre-filled. Is there still the possibility to get above mentioned information for publication in order to provide this set of functionalities to customers?
</summary>
<br>
TED no longer provides the same metadata per announcement as before, we return all relevant info we receive.
The following data is provided by TED on an announcement.

![Data of an announcement from TED](images/faq/announcement_data_from_TED.png)

We process the status, the time of posting and if given the time of publication. The OJ number is no longer used in eNotices2. If you need more data from this query, please send us an email with your requirements to: support-oeffentlichevergabe@bdr.de. We will be happy to organize a bilateral exchange.
</details>
<br>

<details>
<summary>
How are rejected notices in error states such as 'REJECTED' status from TED or an 'INTERNAL ERROR' status from BKMS further processed?
</summary>
<br>
There will be internal monitoring to respond to error conditions (InternalError status) or bugs. Currently, Nortal at the email address support-oeffentlichevergabe@bdr.de is the first point of contact if you have problems with your submissions udn your announcements run into an error status. Generally such error states indicate bugs in the DöE, in TED or in the sent announcement. Whenever errors happen in the system (for example, when TED rejects), they are logged so that a support ticket can be created and a technical analysis performed if needed. An individual decision is then made as to what action is appropriate to correct the error. In the case of technical errors, the announcement can either be resent as a new version after it has been corrected or it can be reprocessed manually internally. However, this depends on the individual case. If TED refuses, it is possible that an error exists in the notice, e.g. the notice-id is already used. In this case, it is stored which error message TED returned when rejecting, so that it can be reacted accordingly.
</details>
<br>

<details>
<summary>
Can it happen that a superthreshold announcement changes to NOT_PUBLISHED after the deadline if it has already been published in BKMS? Because then we would have TED:NOT_PUBLISHED / DSE:PUBLISHED, a status I could not discover in the flowchart.
</summary>
<br>
The NOT_PUBLISHED status is only relevant for announcements with lawfulness warnings. If a notice has no lawfulness warnings, no manual review is performed by TED, so it cannot result in NOT_PUBLISHED status based on manual rejection.

In the case of lawfulness warnings, a notice will not be forwarded to BKMS until 5 days after SUBMITTED in TED to await manual review. However, if a situation arises where a notice is already published in BKMS, which then changes to NOT_PUBLISHED in TED, then that notice is automatically stopped by our system in BKMS so that the status would change to DöE:Stopped. In this way, we ensure that no announcements rejected by TED remain published in BKMS. However, this scenario is very very unlikely.
</details>
<br>

### API mediation service

<details>
<summary>
How does the API behave for the production environment before the cutoff date and after the cutoff date 10/25/2013?</summary> (added 10/11/2013)
<br>
From a purely technical perspective, the API will not change before and after the cutoff date.

On the cutoff date, ensured that all enabled accounts in the production environment are also enabled for submission to TED.

This is the case by default, but can be explicitly switched off if required, if certain accounts of the productive environment are to be explicitly used only for the submission of subliminal announcements.  

There is no technical "turning on" of the API or anything similar. The production environment is already technically as functional as the staging environment, even if legally no submission is allowed yet.
</details>
<br>


<details>
<summary>
How can platform operators obtain the EU CVS Report information on a notice?</summary>
<br>
All errors and warnings from the CVS report are passed in the status information. Here we pass the ID, path, content and text of each posted rule. There is no provision to return the CVS report as a file.
</details>
<br>

<details>
<summary>
The REST API description talks about "current data deliveries". What exactly is meant by this?
</summary>
<br>
The v1/notices endpoint returns status information about all notices that have been successfully delivered by the currently authenticated client.
</details>
<br>

<details>
<summary>
Can an API key also be used for authentication or only authentication via token?
</summary>
<br>
Authentication via API keys will be disabled soon, even on Preview. In the long run, you will only be able to authenticate via tokens with refresh every 24h. In single cases API keys are still used for testing and debugging purposes.
</details>
<br>

<details>
<summary>
In the REST API, we talk about clients. Does 1 client = 1 API key = 1 allocation platform?
</summary>
<br>
This assumption is correct.
</details>
<br>

<details>
<summary>
The REST API description talks about "current data deliveries". What exactly is meant by this?
</summary>
<br>
The v1/notices endpoint returns status information about all notices that have been successfully delivered by the currently authenticated client.
</details>
<br>

<details>
<summary>
Awarding platforms want to detect status changes in a timely manner (currently, one status request per relevant data delivery occurs approximately every 10 minutes). Is there a plan for "GET /v1/notices" to be able to limit or filter the list to those data deliveries where a TED or DOE status change has occurred since a committed time to reduce the query load on the system?
</summary>
<br>
Thank you for this suggestion; we will look into implementing it.
</details>
<br>

<details>
<summary>
How can platform operators obtain the EU CVS report information on a notice if it is not included in the response on publication (POST → /v2/notices), nor in the status information (GET → /v1/notices/{trackingCode})?
</summary>
<br>
All errors and warnings from the CVS report will be passed in the status information in the future. In doing so, we pass the ID, path, content, and text of each rule that was struck. Currently, there are no plans to return the CVS Report as a file.
</details>
<br>

<details>
<summary>
09/28/2013 Will it be possible to use the online validator API productively?
</summary>
<br>
Yes, productive use of the online validator is supported. In the production environment and in the staging environment, the eforms-de-schematron bugfix version will always be the same as in the mediation service itself. The use of the offline validator (https://github.com/EFA-FHB/eforms-validator-core) is also recommended.
</details>
<br>

### Ongoing procurement procedures and changeover to the new data service.

<details>
<summary>
 How was the linking to or referencing of previous announcements done? (added 9/27-23)

 </summary>

- The notices are linked to the procedure ID.

  Special Features:

   --> Planning/PINs are not part of procedures: Use BT-125

   --> Surcharges within a framework contract: use OPT-100

   --> change notification: use BT-758

   --> Contract amendment: use BT-1501

   --> Notices before eForms (and all other cases): Use OPP-090

- Use TED publication number ([1-8 digits]-[year]) or eForms UUID.

- In the [Developer Docs FAQ](https://docs.ted.europa.eu/home/eforms/FAQ/index.html#_forms_and_procedures) you can also find this information

  - For more details on how to link the announcements, see.
https://github.com/EFA-FHB/ozg-vermittlungsdienst-doku/blob/main/documentation/eForms_Erstellung.md

- Details on how to use the references can be found here: https://docs.ted.europa.eu/eforms/latest/schema/procedure-lot-part-information.html#previousNoticeSection

 The components of the data service can only accept the new eForms structures. In the awarding platforms, the TED schema structures are currently used for communication with the EU. For ongoing procurement procedures, it will be the case that, for example, a notice of awarded contracts will be published after a contract notice or, for example, a contract amendment will be published for a notice of awarded contracts. Can notices for ongoing procurement procedures continue to be sent to the data service in TED 2.0.9 XML format until the deadline of 25.10.2023 or should they be sent directly to TED until the deadline as before?

Until eForms-DE becomes mandatory, submissions can be made directly to TED in the old format. For future submission to the Public Purchasing data service, only the new format of the eForms-DE standard can be used.
</details>
<br>

<details>
<summary>
Will it be possible to send corrections to the data service that submits them to TED as a standalone, new eSender hub, even if the notices were previously submitted to TED by the platform operator as a former eSender hub? <br>
More specifically:

- How is a change of eSender for an announcement handled when it needs to be corrected?
- How is a change of eSender handled within a multiple notice process?
</summary>
<br>
It will not be possible to use the data service to query the status of an old notice or to stop an old notice that has not been submitted via the data service, as the data service cannot perform queries on notices from other eSenders. This is a restriction from TED to submitting eSenders.

Correction of a notice is in principle possible by sending a new version of a notice in eForms format to the data service before publication of a notice. This update is then sent to TED and TED publishes the latest version of the notice. If the original announcement has already been published, a "Change Notice" must be sent.

It is currently being clarified with TED how to reference a previous notice in the old format to link them together and to what extent the change of submitting eSender will affect changes.
</details>
<br>



<details>
<summary>
Is OPP-090-Procedure used exclusively for the case of old notices (old TED schema) with further processing in eForms?
 </summary>

Both Change Notices and thus the "Change Notice Version Identifier" (BT-758) and "Framework Notice Identifier" (OPT-100) and "Previous Notice" (OPP-090) are TED specific solutions that can be used directly.

</details>
<br>

### Accepted SDK versions

<details>
<summary>
As far as we know, the eForms-DE format is no longer compatible with the eForms-EU format, as it is no longer a pure subset of it. Thus, no EU API functions can be called with the eForms-DE format, be it the new eForms API or the Viewer Services APIs (PDF/HTML rendering). Is it correct that the new data service does not offer a render method and also the render methods of the EU can no longer be used due to incompatibility? How can features like PDF/HTML rendering still be used?
</summary>
<br>

Question 2 under [roadmap](#roadmap) - The need for a rendering method has already been recorded and is currently being analyzed.

The eSender Hub will take care, according to the delivered eForms-DE version, to transform this announcement into a valid eForms-EU document in order to be able to use the TED features.
</details>
<br>

<details>
<summary>
 Which versions of the eForms-DE standard are currently supported? (added on (09/29/2013)
</summary>
<br>
In October 2023, the Public Purchasing data service will support versions 1.0 and 1.1 of the eForms-DE standard, technically this corresponds to a CustomizationID (see field OPT-002-notice) with the values "eforms-de-1.1" and "eforms-de-1.0" respectively . To support the implementation, the SDK-DE with the versions SDK-DE-1.1.0_1.7.1 or SDK-DE-1.0.1_1.5.3:20230727 are currently available on https://gitlab.opencode.de/OC000008125155/SDK-eforms-de.
</details>
<br>

<details>
<summary>
Currently, Mediator also seems to accept eForm-EU up to SDK version 1.5. How long will this be available? The background is that contracting authorities often need a longer time (often weeks) between attachment of the notice (or start of procedure) and its publication. Therefore, a longer period is necessary between the start of the go-live of eForms-DE and the shutdown of eForms-EU.
</summary>
<br>
Currently, the plan is to turn off support for eforms-EU 1.5 with the July release, as it is also not supported in the announcement service. If there is a need to support this or other EU versions longer, it can be discussed.
</details>
<br>

### Special cases

<details>
<summary>
For any rare, but conceivable, special cases, will there be appropriate procedural models that can be invoked when the cases arise?<br>
 </summary>
 Two examples will serve this purpose:
Example 1:<br>
The switching service accepts an announcement, which is valid according to the switching service/eSenderHub. The EU later rejects the acceptance (status "rejected"), for example because the SDK version is no longer supported. The platform operator receives the status "internalError" according to the status mapping. What would be the further procedure in this case?<br>
Example 2:<br>
According to the EU, a business rule will soon be introduced which will no longer allow the "dispatch date" in a notice (the day the notice is sent), which is set by the platform operators and the time the data service is sent to the EU, to deviate by a maximum of 24 hours, otherwise acceptance by the EU will be blocked. Any technical problems in the data service would therefore always have to be solved within 24 hours.

<br>
There will be a support structure to respond to error conditions (status InternalError) or bugs. It is currently being clarified what this support structure will look like at what point in the operation. At the beginning from June, Nortal will be the first point of contact at the e-mail address support-oeffentlichevergabe@bdr.de. Whenever bugs happen in the system (for example, TED rejections), they will be logged so that a support ticket can be created and a technical analysis can be performed if needed.
</details>
<br>



# Standard eForms-DE and SDK-DE

[Back to top](#frequently-asked-questions)<br>

**Please note that we answer all questions regarding the standard eForms-DE according to our current knowledge. Information is subject to change at any time. If you have any further questions regarding the eForms-DE standard, please feel free to contact the Coordination Office for IT Standards (KoSIT) as operator by e-mail: eforms@finanzen.bremen.de**


## Questions about Business Terms and Groups (BT/BG)

Sorted by BT/BG number.

### Procurer Legal Nature (BT-11) and CPV.
<details>
<summary>
CPV code main subject matter and cross dependencies to the legal nature of the bidder. EU restrictive rule BR-BT-00262-0211. (updated 9/27-23)</summary>
<br>

According to this rule, grantees under VgV can only tender construction work, but not services. Even in award procedures under SektVO, KonzVgV, or VSVgV, there are restrictions on tendering grantees compared to other awarding bodies in the selection of forms applicable in an award procedure, which is incomprehensible.

**This is a BUG at TED. Verbal statement from TED at 6th workshop on 9/26/2023: Will be fixed for version 1.9.**
</details>
<br>

### Announcement of results (BG-7), bid (BG-320 bid).
<details>
<summary>
In the "Announcement of Results" (BG-7) > "Bid" (BG-320) element, should only awarded bids/lots be listed or all bids/lots received?
</summary>
<br>

In this matter, the provisions of the respective directives and regulations under which the procurement procedure falls apply unchanged.
</details>
<br>

### No immediate publication (BG-8; BT-195/BT196/BT197/BT-198).
<details>
<summary>
Why is indication of the time limit of fields not to be published mandatory for required fields?
</summary>
<br>

The specification follows the EU Implementation Handbook on this point. It is a shall formulation that does not require a business rule.
Details: https://op.europa.eu/en/publication-detail/-/publication/73a78487-cc8b-11ea-adf7-01aa75ed71a1
</details>
</summary>
<br>

### Award Criteria (BG-707, BG-38, BT-53 et al.)
<details>
<summary>
Are award criteria with a weighting not to be provided or optional?
</summary>
<br>

For award criteria >=10% the information is mandatory for eForms-de, for award criteria < 10% the cardinalities of the information provided by TED currently remain unchanged.

It is strongly recommended that the details are also recorded for the award criteria whose weighting is less than 10% in order to comply with TED's 100% rule.
</details>
</summary>
<br>

### National exclusion grounds (BT-67 exclusion grounds).

<details>
<summary>
Why have the codes for national exclusion grounds in the Criterion Exclusion Grounds code list been changed in eForms-DE v1.1.0?
</summary>
<br>

Only the codes "ex-os" (Criterion Exclusion Upper Threshold) and "ex-us" (Criterion Exclusion Lower Threshold) have been removed, since the code "nati-ground" (purely national exclusion grounds) existing in the EU can be used instead.

We have updated the changelog for them: https://projekte.kosit.org/eforms/eforms-de-codelist/-/blob/main/CHANGELOG.md.
  </details>

<details>
<summary>
Which exclusion reason can be pre-populated, should all reasons apply equally?
</summary>
In case all exclusion reasons apply equally, "nati-ground" (purely national exclusion reasons) is the most comprehensive code.
</details>
<br>

<details>
<summary>
According to the ARC, why do mandatory grounds for exclusion have to be selected or specified in a contract notice at all?
</summary>
 The motivation is that in tenders, reference is not only made to national laws, but that grounds for exclusion are explicitly listed, in particular for transparency, also vis-à-vis bidders from abroad.
 </details>
<br>

<details>
<summary>
What should an awarding agency enter in the "Description" field (BT-67(b)-Procedure) per selectable exclusion reason?
</summary>
The presentation has been chosen to be consistent for EU-wide and national procurement procedures.
In BT-67, an explanation can be deposited for the exclusion reasons shown.
</details>
<br>

### Previous planning (BT-125),
<details>
<summary>
How should the OPP-090-Procedure, BT-125-Lot, and BT-1251-Lot fields be populated technically (characters allowed) and technically?
</summary>
<br>

The BT-125(i) & OPP-090 are specified with the UUID (notice number) of the EU prior information or with the OJ number to refer also to older prior information.

For BT-1251, only a length limit of 30 characters is specified in the SDK.
</details>
<br>
<details>
<summary>
For which case is BT-125 lot and BT-1251 lot used?
</summary>
<br>

A contracting agency has published a prior information notice announcing that a solicitation on subject X will be issued in the near future. This prior information is now given a notice number. Some time later, the contracting agency advertises subject X in a contract notice (CN). In BT-125(i), the announcement number of the prior information notice is now entered to refer to the prior information notice that was published some time ago.
BT-1251 is a concretization of where information on Subject X was provided. This is done in the prior information in Parts. So BT-1251 is the specification in which Part of the prior information was informed.
</details>
</summary>
<br>


### Display of winner in a contract notice (added 10/27-23).
(BT-142, BT-13713, , OPT-320, BT-13714, , OPT-310, OPT-300, BT-721, BT-145, BT-1451, BT-768, BT-3202)
 <details>
<summary>short version
 </summary>
 
<br>

It should be noted that in eForms, contractors and clients for awarded bids (contracts) are stored in different locations in the eForms structure.

The contracting authority is stored in the Contract structure.
An offer is assigned to a contract, and bidders are assigned to the offer. These bidders represent the contractors of the contract.

What exactly has to be done to enable this backward chaining and lead to a correct display in the announcement service is described in the following long version .
</details>
<br>
 <details>
   <summary>Long version
      </summary>
 
<br>
The following outline is intended to assist in completing the Notice of Results (CAN) eForms form to the point where the associated awarded contracts can be correctly displayed in the Notice Service (www.oeffentlichevergabe.de).
These completion instructions are directed to specialist procedure manufacturers for the technical implementation of the following fields in the specialist procedure. If applicable, this can be used to guide users. For this reason, the technical field identifiers as well as their German interface designations (used according to the standard eforms-DE, if available, otherwise those from the SDK-DE) are given:
<br>

1. description of the results of the tender
    The results for a tender are stored in the XML in the <efac:NoticeResult> section. In the following sections, only the sub-sections are described that are required here to output the expected results in the announcement service.

2. description of the results of a lot
   
    In the form module "Result of lots" (<efac:LotResult>) is the BT-142 (winner determined, <cbc:TenderResultCode listName="winner-selection-status">). Behind it is a code list with the following values:

       a. A contest winner has not yet been determined, the contest is not yet closed.

       b. No contest winner has been determined and the contest is closed.

       c. At least one winner has been determined (code: selec-w).

    Only in the event that "c" has been selected, a result can be reported for that lot and at least the winning bid for that lot must be reported. In the event that multiple bids have been awarded, all winning bids shall be listed below. In the section "Result of Lots" (<efac:LotResult>), the relationship between the lot <efac:TenderLot> , BT-13713-LotResult, (procedure result lot identifier) and the bid (<efac:LotTender>, OPT-320-LotResult) is established.

3. description of the tender
   
    The description of the offers is done in the form module "Offers" (<efac:LotTender>).
    Here it is important to set a form internal reference number to the offer, as this should already be used e.g. in the previous section - in the reference to the offer (see <efac:LotTender>, OPT-320-LotResult in section 2). Again, the LOS to which the tender refers should then be referenced once more (in the Tender Lot Identifier field): <efac:TenderLot>, BT-13714-Tender>. In addition, a further reference should now be included at this point to the section
    <efac:TenderingParty> in the OPT-310-Tender field (identifier - bidder). This reference points to the form module "Bidder", which is described below.

4. description of the bidder(s) for a tender

    In the form module "Bidder" <efac:TenderingParty> the details of the bidder(s) of an offer(s) are to be stored. The main purpose here is to indicate whether the bid was submitted by an individual bidder or by a bidding consortium or by a bidder who will employ subcontractors. Therefore, only references to the bidding organizations are required here. If it is a bidder in this bid, then the reference to the bidder organization must be specified in the <efac:Tenderer> OPT-300-Tenderer (ID - Bidder ) field.
    For each bidder specified, additionally complete the efac:Tenderer/efbc:GroupLeadIndicator OPT-170-Tenderer (Head of Bidder) field. At least one of the specified bidder organizations must qualify as a "bidder's lead". Bidder parties that have joined together in subcontracts may also be indicated here (however, the appropriate description of these fields is omitted here).

5. description of the contract
      
    After the above requirements 2-5 have been fulfilled, the interrelationships can be mapped that represent the technically interesting part in the announcement service, namely the contracts that have been concluded for a lot. This is done in the form module "Orders" ("Contracts") <efac:SettledContract>.
    The following information should be provided in this section:
  
      BT-721-Contract - name of the contract

      BT-145-Contract - date of the contract conclusion

      BT-1451-Contract - date of the decision on the winner

      BT-768-Contract - order as part of a framework agreement.


To be able to determine the winner, the field named below is the most important:

BT-3202-Contract - Order Bid Identifier, because this field is used to determine the underlying bid as part of a backward chaining process, and this is used to determine the bidder, or head of a bidding consortium, who signed the contract on behalf of the bidders.

In order to also be able to map which organization on the client side signed the contract, the following field shall also contain ID - Contract Signatory <cac:SignatoryParty> (OPT-300-Contract-Signatory) with a reference to the contract signing organization on the client side.

Building these references according to the described pattern in this way also serves another purpose: only if all references exist cleanly, the requirements according to BT-165 (Company size) is mandatory to fill in and the BT-706 (Nationality of the beneficial owner of the winner) is mandatory to fill in, of the standard eForms-DE can be fulfilled.

 </details>

 </summary>
 
<br>

### Identification number (organization) (BT-501)
<details>
<summary>
What kind of identifier/identifier needs to be entered for BT-501? (updated 10/25/2023)
</summary>
<br>
 Generally, the choice of a unique identifier is up to the organization itself. Requirements for this identifier are:

* This must be unique, i.e. there must be no other organization with the same identifier.
* This should be used sustainably across all announcements

For public administration, the use of the routing ID is recommended (as this is already widely used for electronic invoicing). This takes the following form:

0204:Routing ID

Example (fictitious):

0204:991-1234512345-06

The routing ID format specification (version 2.0.2) can be viewed and downloaded from the following link:

https://leitweg-id.de/wp-content/uploads/2021/08/Leitweg-ID-Formatspezifikation-v2-0-2.pdf


Until or unless this is available, another unique identification number shall be temporarily designated. If there is no other unique identification number, a telephone number of the organization may also be entered as the unique identification number. This should then have the following form:

`t:03023125000`

This should be entered with prefix (t:), area code, without special characters and without spaces, as in the fictitious example.

**Notes for awarding chambers:**

For the awarding chambers, we recommend using the identifiers in the table below. These are taken from the following page, among others:

https://www.bundeskartellamt.de/DE/UeberUns/LinksundAdressen/Vergabekammern_der_L%C3%A4nder/Vergabekammern_artikel.html


| Federal/State | Authority | Identifier |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------|-------------------|
| Federal Government |Federal Chamber of Public Procurement |t:022894990|
| Baden-Württemberg |Chamber of Public Procurement Baden-Württemberg | t:07219268730 |
| Bavaria |Chamber of Public Procurement of Northern Bavaria at the Government of Middle Franconia | t:0981531277 |
| Bavaria|Government of Upper Bavaria Public Procurement Chamber of Southern Bavaria |t:08921762411 |
| Berlin| Procurement Chamber of the State of Berlin | 0204:11-1300000V00-74 |
| Brandenburg| Procurement Chamber of the State of Brandenburg at the Ministry of Economic Affairs and Energy | t:03318661719 |
| Bremen |Vergabekammer Bremen The Senator for the Environment, Construction and Transport | t:042136159796 |
| Hamburg| Procurement Chamber at the Ministry of Finance | t:040428231690 |
| Hamburg| Public Procurement Chamber at the Authority for Urban Development and Housing |t:040428403230 |
| Hesse| Procurement Chamber of the State of Hesse at the Darmstadt Regional Council | t:06151126603 |
| Mecklenburg-Western Pomerania| Public Procurement Chambers at the Ministry of Economics, Labor and Health | t:03855885160 |
| Lower Saxony| Public Procurement Chamber of Lower Saxony at the Lower Saxony Ministry of Economics, Labor and Digitalization | t:04131153308 |
| North Rhine-Westphalia| Rhineland Public Procurement Chamber via Cologne District Government | t:02211473055 |
| North Rhine-Westphalia| Procurement Chamber of Westphalia |t:02514111691 |
| Rhineland-Palatinate| Public Procurement Chamber Rhineland-Palatinate at the Ministry of Economy, Transport, Agriculture and Viniculture | t:06131162234 |
| Saarland| Public Procurement Chambers of Saarland | t:0681501994 |
| Saxony| Public Procurement Chamber of the Free State of Saxony at the Saxony State Directorate | t:03419773800 |
| Saxony-Anhalt| 1st and 2nd Procurement Chambers of the State of Saxony-Anhalt | t:03455141529 |
| Schleswig-Holstein| Public Procurement Chamber of Schleswig-Holstein at the Ministry of Economics, Transport, Labor, Technology and Tourism of the State of Schleswig-Holstein | t:04319884640 |
| Thuringia| Procurement Chamber of the Free State of Thuringia at the Thuringian State Administration Office | t:0361573321276 |
<br>
</details>
<br>

### New edition of the procedure (BT-634)

<details>
<summary>
What is the benefit of BT-634 lot in the CN if at the time the notice is written it is not yet possible to assess whether the procedure/lot needs to be re-tendered.
</summary>
<br>

The name for BT-634 (relaunch of the procedure) is less veriwrrend in English: "Relaunch", meaning "new start". Thus, the BT-634 is not to be used for an indication in the future, but rather as an indicator of whether a procedure or lot for the advertised item already existed and was cancelled in the past. Then, the BT-634 can be used to indicate at the procedure or lot level whether this notice is the "restart" for the cancellation of a previous notice.
  </details>
<br>


### Vehicle Class (BT-723)
<details>
<summary>
 Helps to select the values of the code list for BT-723 vehicle class.
</summary>
<br>

For assistance, refer to Annex II of the Framework Directive https://eur-lex.europa.eu/legal-content/DE/TXT/HTML/?uri=CELEX:32007L0046..:
|code|meaning|
|---|---|
|M1|Light commercial vehicle of vehicle category M1 or passenger car (motor vehicles for the carriage of passengers with not more than eight seats in addition to the driver's seat.)|
|M2|Light commercial vehicle of vehicle category M2 (motor vehicles for passenger transport with more than eight seats except the driver's seat and a maximum permissible mass of up to 5 tons.)|
|N1|Light commercial vehicle of vehicle class N1 (motor vehicles for the carriage of goods with a maximum permissible mass not exceeding 3.5 tons.)
|N2|Heavy commercial vehicle of vehicle category N2 (motor vehicles for the carriage of goods with a maximum permissible mass exceeding 3.5 tons but not exceeding 12 tons.)|
|N3|Heavy commercial vehicle of vehicle class N3 (motor vehicles for the carriage of goods with a maximum permissible mass exceeding 12 tons.)|
|M3|Bus of vehicle category M3 (motor vehicles for passenger transport with more than eight seats in addition to the driver's seat and a maximum permissible mass of more than 5 tons.)

</details>
<br>

### (Especially) suitable for SME (BT-726).

<details>
<summary>
Blurring due to the relationship between "Particularly suitable for SMEs" (BT-726) and the collection of structured data in the unstructured data field "Additional information" (BT-300)
</summary>
<br>

Stakeholders are aware of the vagueness that results from collecting structured data in unstructured fields, but it is currently considered acceptable. The approach is seen as an interim solution and further work is being done to find a "clean" solution.
This is being done with the consideration that BKMS can evaluate any data immediately as of October 25
  </details>
<br>

<details>
<summary>
Does the data service remove this information, or is it also transmitted to the EU?
</summary>
<br>

The eSender hub does not remove this data, the input from this field is also transmitted 1:1 to the EU. Since this is a text field, there is no technical problem here either. Only one value can be inserted for the beginning of the text field: #particularly suitable for:{freelance OR self OR startup}#'. However, after this specification, further explanations can be inserted as free text.
  </details>

<br>
<details>
<summary>
Do the values in parentheses also need to be sent? e.g. freelance (Particularly suitable for freelancers).
</summary>
<br>

No, these values are urgent for a better understanding of the codes
  </details>

<br>
<details>
<summary>
What about localization if, for example, the language of the announcement is English and then there are German terms in the BT-300 free text field (also with respect to the umlaut in self-employed)?
</summary>
<br>

In principle, there is no automatic translation of field contents, i.e. German terms in the fields remain German. The EU has not yet decided on a unilateral approach to localization.
  </details>

<br>
<details>
<summary>
Is any additional information allowed to be written to the field, e.g. by the user or automated by the application?
</summary>
<br>

It is possible to add free text after specifying the code, as long as the total character limit is respected. For clarification, the following note has been added to BT-300:
"To the extent that it is necessary to specify one of the codes (freelance, self, startup) because of rule BR-DE-26, the code must be specified on the first line and separated from other additional information by two blank lines. The format of the first line is defined as follows: #special for:{freelance|self|startup}."
  </details>
<br>

### Preferred Publication Date (Requested Publication Date BT-738).

<details>
<summary>
New features and details (added 09/27/2013).
</summary>
<br>

- Date of publication of eForms notices on TED: no longer 5 fixed calendar days.

- Ability to set a preferred publication date (BT-738).

- If no date is specified, then TED publishes "As soon as possible," i.e., in the next available OJS issue

   --> Notice may appear in TED at 9:00 a.m. the next morning; maximum of 2 business days.

   --> less time to stop publication.

- If a date is given, TED publishes on the preferred date or in the next available OJS issue after that date
  
   --> see TED publication calendar for working days.

   --> the preferred publication date can be up to 60 days in the future.

- On the business day prior to the expected publication date:
  
   --> daily export on working days between noon and noon - message goes into OJS output.
  
   --> overnight to publication status (or over the weekend or on holidays).
  </details>
  <br>

### Lots
<details>
<summary>
How to use LOT entries for "none", one or more lots?
</summary>
<br>

According to TED, if there is 'none' lot, there must be only one technical lot entry with the value LOT-0000.
If there are two lots, there are two lots with the values LOT-0001 and LOT-0002. For example, if there are 5 lots, there are LOT-0001, LOT-0002, LOT-0003, LOT-0004, LOT-0005. The structure of LOT-0000 is completely identical to any other LOT, including LOT-0001. Only the ID is different.

Doc can be found here: https://docs.ted.europa.eu/eforms/1.5/schema/procedure-lot-part-information.html
</details>
<br>

<details>
<summary>
While reviewing the national tailoring documents, some inconsistencies regarding lot groups have been discovered. According to eForms-DE standard v1.0.0 and v1.0.1, the optional fields of the group "Award - groups of lots" or "Framework agreement, lot group, maximum value" are marked with number "0" and therefore should not be able to be used. In the SDK-eForms-DE v1.5.1, which is based on the eForms-DE standard v1.0.0, however, the fields appear in the fields.json. How should lot groups be handled in general in the future?
</summary>
<br>

For simplicity and to avoid inconsistencies with EU supplied Schematron rules, the SDK to the eForms-DE national standard includes fields at the technical level that are nevertheless not used according to the eForms-DE standard.

Lot groups are not provided in eForms-DE.
</details>
<br>

### NUTS codes

<details>
<summary>
Is there a code list of country codes where it is not possible to specify the NUTS code?
</summary>
<br>

Country specific NUTS code lists are available in the TED SDK (https://github.com/OP-TED/eForms-SDK/blob/1.7.0/codelists/country.gc ).
  </details>
<br>

<details>
<summary>
Conversely, does the country never have to be specified if you can specify NUTS codes?
</summary>
<br>

Since the country is part of the NUTS code, an additional separate mention is not required.
  </details>
<br>

<details>
<summary>
Does the specification of NUTS-lvl3 codes remain mandatory?
</summary>
<br>
Yes, as far as NUTS codes are available, they have to be indicated
  </details>
<br>

# General
[Back to top](#frequently-asked-questions)

### eNotices portal of the EU

 <details>
<summary>
Information from TED as of 09/27/2013.

 </summary>

<br>

- For API submissions, NoticeAuthorEmail should be the buyer's email - eSenders must include the true email address of the ordering party in the metadata

- Notice author email will receive notifications of status changes:
       --> submission, validation failed, stopped, not published, published.
  
- The eSender will receive a copy to the email address used by EU Login for the API key.

- Ongoing improvements to the content and translation of these email notifications.
  
- New feature coming soon: Buyers will receive an email notification when an announcement with the same buyer name has been published

- Note for API testing (risk of receiving many emails): use a unique "main buyer name" for recurring buyers and a random name for multiple buyers
  
- **Agency service API parameter: authorEmail
               Please specify the email of your end buyers accordingly**.
           </details>
           <br>

<details>
<summary>
According to the EU (see https://simap.ted.europa.eu/de_DE/web/simap/statistical-production-files - Statistics 2023 by format and transmission channel), many contracting authorities still used the EU portal eNotices to create and publish the notice. eNotices2, the new portal with integrated eForms, knows and does not take into account national tailoring. Would contracting authorities be allowed to continue using eNotices2 even though national tailoring is not considered there?
</summary>
<br>
eNotices2 may no longer be used for above-threshold submissions as of 10/25, as the adjustments to the eForms standard would not be taken into account, making direct submission via eNotices2 to TED no longer legally permissible.
</details>
<br>

<details>
<summary>
Will there be a new portal for interested companies to replace the current service.bund.de site?
</summary>
<br>
There are no plans for another portal to replace sevice.bund.de. Project desire is to have all notices (upper and lower threshold) in the Public Purchasing data service.
</details>
<br>

<details>
<summary>
Does a mapping exist from XAward to eForms?
</summary>
<br>
The XVergabe standard will be permanently replaced by eForms-DE and will not be further developed. The degree of coverage of the contained information is very different. No mapping from XVergabe to eForms is provided by Datenservice Öffentlicher Einkauf.
</details>
<br>

---
[Back to top](#frequently-asked-questions)
