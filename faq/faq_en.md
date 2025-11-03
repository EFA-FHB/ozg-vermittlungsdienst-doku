### Public procurement data service
# Frequently asked questions

- Data service for public procurement](#datenservice-öffentlicher-einkauf)
- Standard eForms-DE and SDK-DE](#standard-eForms-DE-and-SDK-DE)
- General](#general)

## Data service public purchasing

### Connection

<details>
<summary>
What are the components of the Public Procurement Data Service and where do I need an account?
</summary>
<br>
**[Editorial system](https://resy.datenservice-oeffentlicher-einkauf.de/)**: The editorial system is an offer for contracting authorities and, for example, service providers of contracting authorities or grant recipients who do not use an electronic procurement system.
The editing system can be used to record, edit and correct notices for Europe-wide award procedures and send them to TED via the Vermittlungsdienst.
<br>
**[Vermittlungsdienst](https://ozg-vermittlungsdienst.de/)**: The Vermittlungsdienst is a purely technical interface for accepting, validating and forwarding notices to TED and the Notice Service.
It does NOT provide an interface for creating announcements! Only machine-to-machine communication is possible, e.g. with awarding office software. This connection is implemented by the specialist procedure manufacturer.
<br>
**[Self-Service Portal](https://self-service.datenservice-oeffentlicher-einkauf.de/)**: The Self-Service Portal (SSP) is a web interface for the account management of Vermittlungsdienst accounts. It is primarily used by specialist procedure manufacturers to view the status information of submitted notices in a dashboard.
<br>
**Announcement service](https://oeffentlichevergabe.de/)**: All EU-wide and national notices sent via the eSender Hub are published in the notice service. The announcement service offers a wide range of search options so that bidders can find announcements in line with their range of services. When using the ELSTER company account, additional convenient functions such as saving search functions and notification services are also available. Furthermore, the data of the announcement service can be reused via an open data interface in the formats eForms-DE, CSV and OCDS.
<br>
</details>
<br>

<details>
<summary>
One e-mail address must be entered as the user name for each registration. Is it possible to enter the same e-mail address for several systems?
</summary>
<br>
In general, two e-mail addresses are requested per account (sometimes also referred to as a client): An e-mail address for activating the account and a contact e-mail address. An individual email address is required per account for activation in order to set the password for the account and to enable unique authentication with the combination of email and password. The account e-mail address can also be a functional mailbox and is only required to manage the account. The contact e-mail address is used if questions arise during operation regarding an announcement that was sent from this account. The contact e-mail address and account e-mail address may be identical and the same contact e-mail address (e.g. a central contact person) may be used for several accounts. However, the same account e-mail address can be used for the three system environments Preview, Staging and Production. We generally recommend one account per awarding platform.
</details>
<br>

<details>
<summary>
When creating an account, a contact email address of a specialist procedure manufacturer must be specified. What is this used for?
</summary>
<br>
This email address is used to proactively contact users of the self-service portal. This may be the case, for example, if there are anomalies with the account or the notifications submitted or if general information is to be sent to all account managers.
</details>
<br>

<details>
<summary>
Can multiple accounts be requested simultaneously for the individual systems? How many accounts are recommended for the preview and staging environment?
</summary>
<br>
We recommend using exactly as many accounts for staging as you plan to use for production. Of course, you can also use any number of test accounts on Preview and Staging.
</details>
<br>

<details>
<summary>
What is the difference between the URL of the procurement platform requested when creating the account and the link to the procurement documents in the eForms document?
</summary>
<br>
The URL of the awarding platform is used purely to assign the accounts/clients; it has nothing to do with the link to the award documents.
Some procurement platforms use Dropbox or Google Drive or similar to host the procurement documents, for example, which is why it is not possible to clearly identify the underlying platform. For this reason, the URL is also necessary. The link to the tender documents remains in the XML document. The link provided when the account is created is displayed as a disclaimer/source under the notice itself when it is published in the notice service.
</details>
<br>

<details>
<summary>
On staging or preview, are the release cycle and validation performed in the same way as in production or are the status changes accelerated? What delays can be expected between acceptance and release?
</summary>
<br>
Full validation and all status changes are performed in all environments. As new eForms versions are first rolled out to preview, then to staging and finally to production, different validation rules may be applied for a short time.
As the announcements are processed slightly faster on Preview and Staging with TED, publication on the staging environment of the announcement service is also slightly faster than in Production.
</details>
<br>

<details>
<summary>
The URL of the allocation platform should be specified to request accounts. What is the purpose of this information?
</summary>
<br>
The purpose of specifying the URL is to distinguish between the systems mentioned, to enable correct access and to avoid duplicates. Public procurement platforms are the systems in which notices are published; the URL of the public procurement platform can be alpha.oeffentlichevergabe.de (test environment of the public procurement service), for example. This URL identifies the platform on which notices are currently published. It is clear that there may be different procedures depending on the structure of the system of the respective FVH. In principle, you need one account for each system that is to be used in the future for delivery to the mediation service. If you are unsure which systems/platforms should be connected to the Vermittlungsdienst, you can clarify this by using the contact form https://self-service.datenservice-oeffentlicher-einkauf.de/contact.
</details>
<br>

<details>
<summary>
Which system environment is the environment to which the test systems of the specialist procedure manufacturers can send notifications? What is the difference between the preview and staging environment?
</summary>
<br>
The preview environment is only used for testing. Updates are often installed here and this is also the test environment for future releases. The staging environment is a 100% copy of the production environment and should only be used for production-related tests. Both environments feed into the staging environment of the announcement service and TED Preview. Tests should be carried out on staging in the same way as they are intended for production. In principle, however, both environments are suitable for testing.
</details>
<br>

### Roadmap

<details>
<summary>
Is there a roadmap for the further development of the components of the Public Procurement Data Service?
</summary>
<br>
Yes, the information is available here: https://self-service.datenservice-oeffentlicher-einkauf.de/roadmap
</details>
<br>

### Communication channels

<details>
<summary>
How can the Public Procurement Data Service team be contacted?
</summary>
The team can be reached via the following contact form:
<br>
Questions/comments about the Vermittlungsdienst/self-service portal at https://self-service.datenservice-oeffentlicher-einkauf.de/contact
<br>
Questions/comments about the editorial system at https://resy.datenservice-oeffentlicher-einkauf.de/kontakt
<br>
Questions/comments about the announcement service at https://oeffentlichevergabe.de/ui/de/contact
</details>
<br>

<details>
<summary>
How is it ensured that specialist procedure manufacturers are regularly informed about news regarding the Public Procurement Data Service, in particular with regard to new versions of the components (Vermittlungsdienst, eSender Hub, REST API, etc.), new features, an update of the roadmap, etc.?
</summary>
<br>
There are regular information events for the specialist procedure manufacturers, which are announced by e-mail.
</details>

<br>
<details>
<summary>
How can it be ensured that specialized procedure manufacturers are regularly informed about news regarding the eForms-DE standard/SDK-eForms-DE?
</summary>
<br>
The official publication of the eForms-DE standard is available at https://xeinkauf.de/eforms-de/
<br>
The associated SDK-DE is published at https://gitlab.opencode.de/OC000008125155/SDK-eforms-de
<br>
Questions about the SDK-DE can be opened via Issues in the repository.

</details>
<br>

### Documentation

<details>
<summary>
Where can I find the current documentation for the Public Procurement data service? To what extent is it planned to keep it up to date? Is this GitHub documentation the official provision of information on this topic?
</summary>
<br>

The Github documentation (https://github.com/EFA-FHB/ozg-vermittlungsdienst-doku) will continue to be maintained and is the official documentation. This can also be read in the self-service portal of the Public Procurement Data Service.
</details>
<br>

<details>
<summary>
How can I determine which eForms versions the subcomponents support for a release?   
</summary>
<br>
The eForms versions supported by the subcomponents are documented at https://self-service.datenservice-oeffentlicher-einkauf.de/documentation/eForms_support. Release notes are published for each release to describe which component supports which version.
</details>
<br>

<details>
<summary>
Is the documentation for the Vermittlungsdienst (https://github.com/EFA-FHB/ozg-vermittlungsdienst-doku) the official documentation?
</summary>
<br>

Yes, the Github documentation is updated regularly and is the official documentation until further notice. The documentation is also published in the [Self-Service Portal](https://self-service.datenservice-oeffentlicher-einkauf.de/).
</details>
<br>

### API brokering service

<details>
<summary>
How can manufacturers of specialized procedures obtain the information of the EU CVS report on a notice?
</summary>
<br>
All errors and warnings from the CVS report are transferred in the status information. The ID, path, content and text of each rule are passed. It is not intended to return the CVS report as a file.
</details>
<br>

<details>
<summary>
The REST API description refers to "current data deliveries". What exactly does this mean?
</summary>
<br>
The v1/notices endpoint returns status information on all notices that have been successfully delivered by the authenticated client.
</details>
<br>

<details>
<summary>
Can an API key also be used for authentication or only authentication via tokens?
</summary>
<br>
Authentication via API keys is no longer possible, even on Preview. In the long term, you can only authenticate via the tokens with refresh every 24 hours.
</details>
<br>

<details>
<summary>
The REST API refers to clients. Does 1 client = 1 awarding platform?
</summary>
<br>
Yes, that is correct.
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
How can manufacturers of specialized procedures obtain the information of the EU CVS report on a notice if it is neither included in the response on publication (POST → /v2/notices) nor in the status information (GET → /v1/notices/{trackingCode})?
</summary>
<br>
All errors and warnings from the CVS report are transferred in the status information. We pass the ID, the path, the content and the text of each rule that has been struck. It is currently not intended to return the CVS report as a file.
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
Detailed information on the support of the eForms versions can be found here: https://self-service.datenservice-oeffentlicher-einkauf.de/documentation/eForms_support
</details>
<br>

## Standard eForms-DE and SDK-DE

[Back to top](#frequently-asked-questions)<br>

**Please note that we answer all questions regarding the eForms-DE standard according to our current state of knowledge. The information is subject to change at any time**.

**For further questions about the <u>eForms-DE</u> standard, please contact the Coordination Office for IT Standards (KoSIT) as the operator by e-mail: eforms@finanzen.bremen.de. Additional information can be found in the [FAQ](https://xeinkauf.de/eforms-de/faq/) provided by KoSIT.**

### General questions

<details>
  <summary>
    Are there any requirements for the language of the announcement or multilingualism?
  </summary>
  <br>
  Although there is no statement on the choice of language for invitations to tender in the procurement regulations, Section 23 (1) of the Administrative Procedure Act (VwVfG) stipulates that the official language is German. Accordingly, it is to be expected that German authorities must always prepare their documents at least in German. Multilingualism is of course possible and permitted. For publishing entities that are not classified as public authorities, publication without German is fine.
</details>

<details>
  <summary>
    Are there forms that are not considered in eForms-DE?
  </summary>
  <br>
    The following forms are not included in the eForms-DE standard:
  
| Form | Type | Description | Reason for non-implementation in eForms-DE |
|-------------|------------------------------|------------|---------------------|
| 1 | Planning | Notice of publication of prior information in a procurer profile - general guideline | Information is included in the procurer profile |
| 2 | Planning | Publication of a periodic indicative notice in a buyer profile - __sector guideline__ | Information is included in the buyer profile |
| 3 | Planning | Publication of a prior information notice in a buyer profile - Defense Procurement Directive | Information is included in the buyer profile |
| T01 | Planning | Prior information notice on public passenger transport services | The basis is Regulation (EC) No. 1370/2007, which continues to apply with updates. Currently, data collection for T1 is carried out directly at TED in the "eNotices" application. The eForms Regulation ((EU) 2019/1780) is the central basis for the VgV valid since 25.10.2023. Regulation (EC) No. 1370/2007 is not part of the eForms Regulation. |
| T02 | Result | Notice on contracts awarded for public passenger transport services | The basis is Regulation (EC) No. 1370/2007, which continues to apply with updates. Currently, data collection for T2 is carried out directly at TED in the "eNotices" application. The eForms Regulation ((EU) 2019/1780) is the central basis for the VgV valid since 25.10.2023. Regulation (EC) No. 1370/2007 is not part of the eForms Regulation. |
</details>
<br>

### Questions about the SDK-DE

<details>
<summary>
Where can I find the latest version of the SDK-DE, which is supported by Datenservice Öffentlicher Einkauf (DÖE) and conforms to the German eForms-DE standard?
<br>
The SDK-DE is published on https://gitlab.opencode.de/OC000008125155/SDK-eforms-de
</details>
<br>

## General
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
No, no mapping from XVergabe to eForms is provided in the Public Procurement data service.
The XVergabe standard will be permanently replaced by eForms-DE and will not be developed further.
</details>
<br>

---
[Back to top](#frequently-asked-questions)





