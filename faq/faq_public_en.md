
# Data service Public procurement

### Connection

<details>
<summary>
What is the Public Procurement Data Service and what components does it consist of?
</summary>

**[Editorial system](https://resy.datenservice-oeffentlicher-einkauf.de/)**: The editorial system is an offer for contracting authorities and, for example, service providers of contracting authorities or grant recipients who do not use an electronic procurement system. The editing system can be used to record, edit and correct notices of award procedures and publish them on the notice service, which can also be sent to the TED platform of the Publications Office of the EU via the Vermittlungsdienst of the Public Procurement Data Service in compliance with public procurement law in the case of Europe-wide award procedures. It is also possible to withdraw procedures.
<br>

**[Vermittlungsdienst](https://ozg-vermittlungsdienst.de/)**: As a technical component, the Vermittlungsdienst accepts notices from procurement platforms in eForms-DE format. Notices for award procedures above the EU thresholds are validated and forwarded to the eSender Hub of the Public Procurement Data Service. Notices for award procedures below the EU thresholds are forwarded directly to the notice service after validation.
<br>

**[Self-Service Portal](https://github.com/EFA-FHB/ozg-vermittlungsdienst-doku/blob/main/documentation/SSP.md)**: The self-service portal offers operators of procurement platforms the opportunity to manage administrative processes themselves to relieve the burden on their own operations and to find out about the processing status of notices in the public procurement process at any time.
<br>

**[Publication service](https://oeffentlichevergabe.de/)**: The publicity service is the central place where EU-wide and national notices from the federal government, federal states and local authorities can be found. It offers a wide range of search options so that bidders can find notices on public procurement procedures from contracting authorities in line with their range of services. With the use of "My company account" (the company account based on ELSTER), further convenient functions such as storage of search functions and notification services are also available. Furthermore, the data of the notification service can be used via an open data interface in the formats eForms-DE, CSV and OCDS. In addition, other servers can retrieve current announcement data from the announcement service via the Peppol infrastructure using the Peppol profile "Search Notice".
<br>

**[eSender-HuB](https://oeffentlichevergabe.de/)**: The eSender Hub is an internal technical component that serves as the central point of communication with the EU Publications Office's pan-European Tenders Electronic Daily (TED). The eSender Hub converts the notices transmitted by the Vermittlungsdienst from the eForms-DE format into the required eForms-EU format and sends them to TED. In addition, the eSender Hub forwards the notices for procurement procedures above the EU thresholds to the Notice Service.
</details>
<br>

<details>
<summary>
How many procurement platforms are connected to the Public Procurement Data Service?
</summary>
Around 92 (as of 2025) procurement platforms are currently connected to the Public Procurement Data Service.
</details>
<br>

<details>
<summary>
What are the service and operating hours of the Public Procurement Data Service?
</summary>
The productive and staging (test) environments of the Public Procurement Data Service are available around the clock (24/7). The preview environment is also available for testing purposes, but can only be accessed daily from 6:00 to 20:00.
</details>
<br>

<details>
<summary>
In which cycle are announcements published on TED and in the announcement service?
</summary>
In principle, all submitted notices are sent to TED or the announcement service without delay. EU-wide notices must first be published on TED. Only after TED has completed the publication and reported back the status "PUBLISHED" are these announcements forwarded to the announcement service. The Public Procurement Data Service waits up to 48 hours for publication by TED. If no feedback on the publication is received within this period, the announcement is nevertheless forwarded to the announcement service. TED itself is subject to internal publication rules: Announcements that are delivered and accepted on one day will appear on the platform on the following day at the earliest. Weekends are an exception, as there are usually no publications on Saturdays and Sundays. In these cases, the notices are published on the following Monday. Another exception is so-called ["lawfulness warnings"](https://info.preview.datenservice-oeffentlicher-einkauf.de/documentation/Status_information#lawfulness). In these cases, TED reserves the right to check an announcement manually before it is published. This check can take up to five days.
</details>
<br>

### Communication channels

<details>
<summary>
How can the Public Procurement Data Service team be contacted?
</summary>

The team can be reached via the following [contact form](https://self-service.datenservice-oeffentlicher-einkauf.de/contact).
</details>
<br>


# Standard eForms-DE and SDK-DE

### Questions about multilingualism
<details>
<summary>
Are there specifications for the language of the notice or for multilingualism?
</summary>
Although there is no statement on the choice of language for invitations to tender in the Public Procurement Regulations, the official language is German in accordance with Section 23 (1) of the Administrative Procedure Act (VwVfG). Accordingly, it is to be expected that German authorities must always prepare their documents at least in German. Multilingualism is of course possible and permitted. For publishing entities that are not classified as public authorities, publication without German is fine.
</details>
<br>
