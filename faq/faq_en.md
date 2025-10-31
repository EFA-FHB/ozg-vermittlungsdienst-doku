### Public procurement data service
# Frequently asked questions

- [Data service for public procurement](#datenservice-öffentlicher-einkauf)
- [Standard eForms-DE and SDK-DE](#standard-eForms-DE-and-SDK-DE)
- [General](#general)

# Data service public purchasing

### Connection

<details>
<summary>
What are the components of the Public Procurement Data Service and where do I need an account?
</summary>

**[Editorial system](https://resy.datenservice-oeffentlicher-einkauf.de/)**: Web interface for creating notices and publishing them on TED and in the notice service.
Does your contracting authority not have software from a specialist procedure manufacturer for creating notices, does it not support all the forms you need or have you previously used TED's eNotices2? Then the editorial system is right for you!
<br>
**[Vermittlungsdienst](https://ozg-vermittlungsdienst.de/)**: Purely technical interface for accepting, validating and forwarding notices to TED and the notice service.
Does NOT provide an interface for creating announcements! Only machine-to-machine communication is possible, e.g. from an awarding authority software. This connection is usually carried out by the specialist procedure manufacturer.
<br>
**[Self-Service Portal](https://github.com/EFA-FHB/ozg-vermittlungsdienst-doku/blob/main/documentation/SSP.md)**: Web interface for the account management of Vermittlungsdienst accounts.
Mainly used by specialist procedure manufacturers. Dashboard accounts are possible for viewing the status information of submitted notices, please contact your specialist procedure manufacturer!
<br>
**[Announcement service](https://oeffentlichevergabe.de/)**: All notices sent via the public procurement data service are published in the notice service. The announcement service offers a wide range of search options so that bidders can find announcements in line with their range of services. When using the ELSTER company account, further convenient functions such as saving search functions and notification services are also available. Furthermore, the data of the announcement service can be reused via an open data interface in the formats eForms-DE, CSV and OCDS.
<br>
</details>
<br>

<details>
<summary>
What information is required to apply for an account? (updated on 11.10.23)
</summary>
<br>

Since 04.10.2023, accounts should be applied for in the [Self-Service Portal](https://portal.ozg-vermittlungsdienst.de). All required information is requested in the registration form for a VD account. These are:

<br>

- System environment for which access data is requested (preview, staging, production). Registration in the portal takes place for the corresponding environment, i.e. if an account is required for the staging environment, this should be requested in the staging portal.

- E-mail address to be used as the user name (this must be unique for each environment, no duplicates allowed)
  
- URL of the awarding platform on which the notices are published
  
- First name, surname and e-mail address of the representative of the FVH (specialist procedure manufacturer)
  
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
Please send us a list of required accounts to support@datenservice-oeffentlicher-einkauf.de including all required information per account. We recommend using exactly as many accounts for staging as you plan to use for production. In addition, any number of test accounts are of course possible on Preview and Staging.  
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
The purpose of specifying the URL is to be able to distinguish between the systems mentioned, to enable you to access them correctly and to avoid duplicates. Public procurement platforms are the systems in which notices are published; the URL of the public procurement platform can be alpha.oeffentlichevergabe.de (test environment BKMS), for example. This URL is used to identify the platform on which you are currently publishing your notices. We are aware that there may be different procedures depending on the structure of the system of the respective FVH. In principle, you will need one account for each system that is to be used for future deliveries to the brokerage service. If you are unsure which systems/platforms should be connected to the DÖE for you, we will be happy to support you in this decision. Please send us an inquiry to support@datenservice-oeffentlicher-einkauf.de
</details>
<br>

<details>
<summary>
Which system environment is the environment to which our test systems can send notifications? What is the difference between the preview and staging environment?
</summary>
<br>
The preview environment is only used for testing. Updates are often installed here and this is also our test environment for future releases. The staging environment is a 100% copy of the production environment and should only be used for production-related tests. Both environments feed into the staging environment of BKMS and TED Preview. On staging, your tests should be performed exactly as you plan to do in production. In principle, however, both environments are suitable for testing.
</details>
<br>

### Roadmap

<details>
<summary>
Is there a roadmap for the further development of the components of the Public Procurement Data Service?
</summary>
<br>
Yes, you can find the information here: https://portal.ozg-vermittlungsdienst.de/roadmap
</details>
<br>

### Communication channels

<details>
<summary>
How can the Public Procurement Data Service team be contacted?
</summary>
Please use our contact forms:
<br>
Questions/comments about the Vermittlungsdienst/self-service portal at https://portal.ozg-vermittlungsdienst.de/contact
<br>
Questions/comments about the editorial system at https://resy.datenservice-oeffentlicher-einkauf.de/kontakt
<br>
Questions/comments about the announcement service at https://oeffentlichevergabe.de/ui/de/contact
<br>
We are open to your suggestions!
</details>
<br>

<details>
<summary>
How can it be ensured that platform providers are regularly informed about news regarding the data service, in particular regarding new versions of the components (Vermittlungsdienst, eSenderHub, REST API, etc.), new features, an update of the roadmap, etc.?
</summary>
<br>
Communication takes place through regular information dates for the specialist procedure manufacturers, announcements by email, current roadmap, release notes and FAQs are available in the published documentation repository: https://github.com/EFA-FHB/ozg-vermittlungsdienst-doku . There is also the SDK-eForms-DE repository: https://gitlab.opencode.de/OC000008125155/SDK-eforms-de.
</details>

<br>
<details>
<summary>
How to ensure that platform providers are regularly informed about news regarding the eForms-DE standard / SDK-eForms-DE.
</summary>
<br>

The official publication of the eForms-DE standard is available at https://xeinkauf.de/eforms-de/

The associated SDK is published at https://gitlab.opencode.de/OC000008125155/SDK-eforms-de

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

The Github documentation will continue to be maintained and is the official documentation until further notice. It can also be read in the [Self-Service Portal](https://portal.ozg-vermittlungsdienst.de/) of the DÖE.
</details>
<br>

<details>
<summary>
How can I determine which versions of the subcomponents are supported for a release?  
</summary>
<br>
The eForms versions supported by the subcomponents are documented at https://portal.ozg-vermittlungsdienst.de/documentation/eForms_support.
For each release, we publish release notes to describe which component supports which version.
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

### API brokering service

<details>
<summary>
How can platform operators obtain the information of the EU CVS report on a notice?
</summary>
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
Allocation platforms would like to recognize status changes promptly (currently a status query is made approximately every 10 minutes for each relevant data delivery). Is it planned for "GET /v1/notices" to be able to restrict or filter the list to those data deliveries for which a TED or DOE status change has taken place since a submitted time in order to reduce the query load on the system?
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
All errors and warnings from the CVS report will be transferred to the status information in future. We will pass the ID, the path, the content and the text of each rule that has been struck. It is not currently planned to return the CVS report as a file.
</details>
<br>

<details>
<summary>
Is it possible to use the online Validator API productively?
</summary>
<br>
Yes, productive use of the Online Validator is supported. In the production environment and in the staging environment, the eforms-de-schematron bugfix version will always be the same as in the Vermittlungsdienst itself. The use of the offline validator (https://projekte.kosit.org/eforms/validator-edition-eforms-de) is also recommended.
</details>
<br>

### Accepted SDK versions

<details>
<summary>
 Which versions of the eForms-DE standard are currently supported?
</summary>
<br>
You can find detailed information on the support of the eForms versions here: https://portal.ozg-vermittlungsdienst.de/documentation/eForms_support
</details>
<br>

# Standard eForms-DE and SDK-DE

[Back to top](#frequently-asked-questions)<br>

**Please note that we answer all questions regarding the eForms-DE standard according to our current state of knowledge. The information is subject to change at any time**.

**For further questions about the <u>eForms-DE</u> standard, please contact the Coordination Office for IT Standards (KoSIT) as the operator by e-mail: eforms@finanzen.bremen.de**

## General questions

<details>
  <summary>
    Are there any requirements for the language of the announcement or multilingualism?
  </summary>
  <br>
  Although there is no statement on the choice of language for invitations to tender in the procurement regulations, Section 23 (1) of the Administrative Procedure Act (VwVfG) stipulates that the official language is German. Accordingly, it is to be expected that German authorities must always prepare their documents at least in German. Multilingualism is of course possible and permitted.
  For publishing entities that are not classified as public authorities, publication without German is fine. As of 31.01.2024, the rule CR-DE-26 for BT-300 is temporarily deactivated for validation in the Vermittlungsdienst, but the error is still returned in the online validator (validator.ozg-vermittlungsdienst.de).
</details>

<details>
  <summary>
    Are there forms that are not taken into account in eForms-DE?
  </summary>
  <br>
    The following forms are not included in the eForms-DE standard:
  
| Form | Type | Description | Reason for non-implementation in eForms-DE |
|-------------|----------------------------------|------------|---------------------|
| 1 | Planning | Announcement of the publication of prior information in a buyer profile - general guideline | Information is contained in the buyer profile |
| 2 | Planning | Publication of a periodic indicative notice in a buyer profile - __sectoral directive__ | Information is included in the buyer profile |
| 3 | Planning | Notice of publication of a prior information notice on a buyer profile - Defense Procurement Directive | Information is included in the buyer profile |
| T01 | Planning | Prior information notice on public passenger transport services | This is based on Regulation (EC) No. 1370/2007, which continues to apply with updates. Currently, the data collection for T1 takes place in the "eNotices" application directly at TED. The eForms Regulation ((EU) 2019/1780) is the central basis for the VgV valid since 25.10.2023. Regulation (EC) No. 1370/2007 is not part of the eForms Regulation. |
| T02 | Result | Notice on contracts awarded for public passenger transport services | The basis is Regulation (EC) No. 1370/2007, which continues to apply with updates. Currently, data collection for T2 is carried out directly at TED in the "eNotices" application. The eForms Regulation ((EU) 2019/1780) is the central basis for the VgV valid since 25.10.2023. Regulation (EC) No. 1370/2007 is not part of the eForms Regulation. |
</details>
<br>

## Questions about the SDK-DE

<details>
<summary>
Where can I find the latest version of the SDK-DE, which is supported by Datenservice Öffentlicher Einkauf (DÖE) and conforms to the German eForms-DE standard?
</summary>
<br>
The SDK-DE is published on https://gitlab.opencode.de/OC000008125155/SDK-eforms-de
</details>
<br>

# General
[Back to top](#frequently-asked-questions)

### eNotices portal of the EU

 <details>
<summary>
How to communicate with TED?

 </summary>

<br>

- For API submissions, the NoticeAuthorEmail must be the email of the procurer (end user)
- The email author of the notice receives notifications about status changes:
--> Submission, Stopped, Not Published, Published
- The eSender receives a copy to the email address used by EU-Login for the API key
</details>
<br>

<details>
<summary>
Is it still possible to submit notices via eNotices2?
</summary>
<br>
Since 25.10.2023, all above-threshold notices must legally be submitted in eForms-DE format via the public procurement data service. Direct submission via eNotices2 is not legally permissible, as the adaptations to the eForms-DE standard are not taken into account there. (See also VgV § 10a)
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

