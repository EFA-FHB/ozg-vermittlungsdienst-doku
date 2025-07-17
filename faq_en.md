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
The purpose of specifying the URL is to be able to distinguish between the systems mentioned, to enable you to access them correctly and to avoid duplicates. Public procurement platforms are the systems in which notices are published; the URL of the public procurement platform can be alpha.oeffentlichevergabe.de (test environment BKMS), for example. This URL is used to identify the platform on which you are currently publishing your notices. We are aware that there may be different procedures depending on the structure of the system of the respective FVH. In principle, you will need one account per system that is to be used for future deliveries to the brokerage service. If you are unsure which systems/platforms should be connected to the DÖE for you, we will be happy to support you in this decision. Please send us an inquiry to support@datenservice-oeffentlicher-einkauf.de
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
All errors and warnings from the CVS report will be transferred to the status information in future. We will pass the ID, the path, the content and the text of each rule that has been struck. It is not currently planned to return the CVS report as a file.
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
<br>
The SDK-DE is published on https://gitlab.opencode.de/OC000008125155/SDK-eforms-de
</details>

<br>

## Questions about business terms and groups (BT/BG)

Sorted by BT/BG number.

### Announcement of results (BG-7), Offer (BG-320 Offer)
<details>
<summary>
Should the element "Announcement of results" (BG-7) > "Tender" (BG-320) only list awarded tenders/lots or all tenders/lots received?
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

### Options (BT-53 Options)
<details>
<summary>
Why is BT-53 (Options) part of the eForms-DE specification, but BT is not an element in TED representations and the EU XML?
</summary>
<br>

eForms-DE is the implementation of the "Commission Implementing Regulation (EU) 2022/2303 of November 24, 2022 amending Implementing Regulation (EU) 2019/1780 establishing standard forms for the publication of notices for public contracts". BT-53 (Options) is explicitly specified in this directive and is an indicator that indicates whether the buyer reserves the right to "reorder" from the same buyer.
In technical terms, a possible entry would be "Yes" or "No".
BT-53 is not required if BT-54 (Options - Description) is filled. In other words, if there is a text that describes the options that the buyer reserves. In this case, BT-53 can automatically be set to "Yes". If BT-54 is not present, then BT-53 is automatically set to "No".
This technically means that there is no need to explicitly implement BT-53, as this follows "automatically" from BT-54.

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

It is strongly recommended that you also enter the information for the award criteria whose weighting is below 10% in order to comply with the 100% rule of TED.
</details>
</summary>
<br>

### National exclusion grounds (BT-67 exclusion grounds)

<details>
<summary>
Why have the codes for national exclusion grounds of the code list "Criterion Exclusion Grounds" been changed in version eForms-DE v1.1.0?
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
BT-1251 is a specification of the point at which information on subject X was provided. This is done in the prior information notice in Parts. So BT-1251 is the information in which part of the prior information was provided.
</details>
</summary>
<br>

### Display of the winner in an award notice (supplemented 27.10.23)
(BT-142, BT-13713, , OPT-320, BT-13714, , OPT-310, OPT-300, BT-721, BT-145, BT-1451, BT-768, BT-3202)
 <details>
<summary>Abbreviated version
 </summary>

<br>

It should be noted that in eForms, contractors and clients are stored in different places in the eForms structure for awarded tenders (contracts).

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

BT-3202-Contract - Order bid identifier, as this field is used to determine the underlying bid as part of a backward chain and the bidder or head of a bidding consortium who has signed the contract for the bidders

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
|N1|Light commercial vehicle of vehicle category N1 (motor vehicles for the carriage of goods with a maximum permissible mass of up to 3.5 tons).
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
Does the data service remove this information or is it also transmitted to the EU?
</summary>
<br>

The eSender Hub does not remove this data, the entries from this field are also forwarded 1:1 to the EU.
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
Can additional information be written to the field, e.g. by the user or automatically by the application?
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
<br>

### BT-1501(s)-Contract
<details>
<summary>
What value do I need to use for BT-1501(s)-Contract?</summary>
<br>
Please create a contract and then link its ID in this field. This can have the value CON-0001, for example.
</details>
<br>

### Lots
<details>
<summary>
How are the LOT entries to be used for "none", one or more lots?
</summary>
<br>

According to TED, if there is 'no' lot, there must only be one technical lot entry with the value LOT-0000. If there are two lots, there are two lots with the values LOT-0001 and LOT-0002. For 5 lots, for example, LOT-0001, LOT-0002, LOT-0003, LOT-0004, LOT-0005. The structure of LOT-0000 is completely identical to that of any other LOT, including LOT-0001. Only the ID is different.
See also: https://docs.ted.europa.eu/eforms-common/FAQ/index.html#_schema_and_field_definitions
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

# General
[Go to top](#frequently-asked-questions)

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
