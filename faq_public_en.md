
- [Data service for public procurement](#datenservice-öffentlicher-einkauf)
- [Standard eForms-DE and SDK-DE](#standard-eForms-DE-and-SDK-DE)
- [General](#general)

# Data service public purchasing

### Connection

<details>
<summary>
What are the components of Datenservice Öffentlicher Einkauf and where do I need an account?
</summary>

**[Redaktionssystem](https://resy.datenservice-oeffentlicher-einkauf.de/)**: Redaktionssystem is designed for contracting authorities and, for example, service providers of public contracting authorities or grant recipients who do not use an electronic procurement system.
The editorial system allows notices for Europe-wide procurement procedures to be entered, edited, corrected, and sent to TED via the Vermittlungsdienst.
<br>
**[Vermittlungsdienst](https://ozg-vermittlungsdienst.de/)**: Purely technical interface for accepting, validating and forwarding notices to TED and to Bekanntmachungsservice. Does NOT provide an interface for creating notices! Only machine-to-machine communication is possible, e.g. from an awarding authority software.
This connection is usually carried out by the specialist procedure manufacturer.
<br>
**[Self-Service Portal](https://github.com/EFA-FHB/ozg-vermittlungsdienst-doku/blob/main/documentation/SSP.md)**: The Self-Service Portal (SSP) is a web interface for managing the agency's accounts.
It is primarily used by process developers to view the status information of submitted notices in a dashboard.
<br>
**[Bekanntmachungsservice](https://oeffentlichevergabe.de/)**: All notices sent via Datenservice Öffentlicher Einkauf are published in Bekanntmachungsservice. It offers a wide range of search options so that bidders can find notices in line with their range of services. When using the ELSTER company account, further convenient functions such as saving search functions and notification services are also available.
Furthermore, the data of Bekanntmachungsservice  can be reused via an open data interface in the formats eForms-DE, CSV and OCDS.
</details>
<br>

<details>
<summary>
Which procurement platforms are connected to Datenservice Öffentlicher Einkauf?
</summary>
Currently, around 87 procurement platforms across Germany are connected to Datenservice Öffentlicher Einkauf (DÖE). Through these connections, the notices from the various regional and national procurement platforms are centrally compiled and made available.
</details>
<br>

<details>
<summary>
What are the service and operating hours (of the components) of Datenservice Öffentlicher Einkauf?
</summary>
The production and staging (test) environments of Datenservice Öffentlicher Einkauf (DÖE) are available around the clock (24/7). The preview environment is also available for testing purposes, but is only accessible daily from 6:00 a.m. to 8:00 p.m.
</details>
<br>

<details>
<summary>
In what cycle are notices published on TED and in Bekanntmachungsservice?
</summary>
In principle, all submitted notices are delivered to TED or Bekanntmachungsservice without delay.

EU-wide notices must first be published on TED. These notices are only forwarded to Bekanntmachungsservice after TED has completed the publication and returned the "PUBLISHED" status. Datenservice Öffentlicher Einkauf (DÖE) waits up to 48 hours for publication on TED. If no response regarding publication is received within this period, the notice will still be forwarded to Bekanntmachungsservice. TED itself is subject to internal publication rules: Notices delivered and accepted on one day will appear on the platform the following day at the earliest. Weekends are an exception, as no publications are usually made on Saturdays and Sundays. In these cases, the notices are published on the following Monday. Another exception is so-called "lawfulness warnings." In these cases, TED reserves the right to manually review an notice before publishing it. This review may take up to five days.
</details>
<br>

### Communication channels

<details>
<summary>
How can the Datenservice Öffentlicher Einkauf team be contacted?
</summary>
The team can be reached via the following contact form.  
<br>
https://portal.ozg-vermittlungsdienst.de/contact
</details>
<br>

# Standard eForms-DE and SDK-DE
### General questions -> Multilingualism
<details>
<summary>
Are there any requirements for the language of the notice or multilingualism?
</summary>
Although there is no statement on the choice of language for invitations to tender in the procurement regulations, Section 23 (1) of the Administrative Procedure Act (VwVfG) stipulates that the official language is German. Accordingly, it is to be expected that German authorities must always prepare their documents at least in German. Multilingualism is of course possible and permitted. For publishing entities that are not classified as public authorities, publication without German is fine.
</details>
<br>

--@include test_en.md