
# Data service Public procurement

### Connection

<details>
<summary>
What is the Public Procurement Data Service and what components does it consist of?
</summary>

**[Editorial system](https://resy.datenservice-oeffentlicher-einkauf.de/)**: The editorial system is an offer for contracting authorities and, for example, service providers of contracting authorities or grant recipients who do not use an electronic procurement system.
The editing system can be used to record, edit and correct notices for Europe-wide award procedures and send them to TED via the Vermittlungsdienst.
<br>
**[Vermittlungsdienst](https://ozg-vermittlungsdienst.de/)**: The Vermittlungsdienst is purely a technical interface for accepting, validating and forwarding notices to TED and the Notice Service. It does NOT provide an interface for creating announcements! Only machine-to-machine communication is possible, e.g. with awarding office software.
This connection is implemented by the specialist procedure manufacturer.
<br>
**[Self-Service Portal](https://github.com/EFA-FHB/ozg-vermittlungsdienst-doku/blob/main/documentation/SSP.md)**: The Self-Service Portal (SSP) is a web interface for the account management of Vermittlungsdienst accounts. It is primarily used by specialist procedure manufacturers to view the status information of submitted notices in a dashboard.
<br>
**Announcement service](https://oeffentlichevergabe.de/)**: All EU-wide and national notices sent via the eSender HUB are published in the notice service. The announcement service offers a wide range of search options so that bidders can find announcements in line with their range of services. When using the ELSTER company account, additional convenient functions such as saving search functions and notification services are also available.
Furthermore, the data of the announcement service can be reused via an open data interface in the formats eForms-DE, CSV and OCDS.
</details>
<br>

<details>
<summary>
Which procurement platforms are connected to the Public Procurement Data Service?
</summary>
Around 87 procurement platforms from all over Germany are currently connected to the Public Procurement Data Service (DÖE). The notices from the various regional and nationwide procurement platforms are brought together and made available centrally via these connections.
</details>
<br>

<details>
<summary>
What are the service and operating times (of the components) of the Public Procurement Data Service?
</summary>
The productive and staging (test) environments of the Data Service Public Procurement (DÖE) are available around the clock (24/7). The preview environment is also available for testing purposes, but can only be accessed daily from 6:00 to 20:00.
</details>
<br>

<details>
<summary>
In which cycle are announcements published on TED and in the announcement service?
</summary>
In principle, all submitted notices are sent to TED or the announcement service without delay. EU-wide notices must first be published on TED. Only after TED has completed the publication and reported back the status "PUBLISHED" will these notices be forwarded to the announcement service. The Public Procurement Data Service (DÖE) waits up to 48 hours for publication by TED. If no feedback on the publication is received within this period, the announcement is still forwarded to the announcement service. TED itself is subject to internal publication rules: Announcements that are delivered and accepted on one day will appear on the platform on the following day at the earliest. Weekends are an exception, as there are usually no publications on Saturdays and Sundays. In these cases, the notices are published on the following Monday. Another exception is so-called "lawfulness warnings". In these cases, TED reserves the right to check an announcement manually before it is published. This check can take up to five days.
</details>
<br>

### Communication channels

<details>
<summary>
How can the Public Procurement Data Service team be contacted?
</summary>

The team can be reached via the following [contact form](https://portal.ozg-vermittlungsdienst.de/contact).
</details>
<br>


# Standard eForms-DE and SDK-DE

### General questions -> Multilingualism
<details>
<summary>
Are there specifications for the language of the notice or for multilingualism?
</summary>
Although there is no statement on the choice of language for invitations to tender in the Public Procurement Regulations, the official language is German in accordance with Section 23 (1) of the Administrative Procedure Act (VwVfG). Accordingly, it is to be expected that German authorities must always prepare their documents at least in German. Multilingualism is of course possible and permitted. For publishing entities that are not classified as public authorities, publication without German is fine.
</details>
<br>
