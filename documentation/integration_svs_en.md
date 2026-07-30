---
title: SVS Integration
---

[Inhaltsverzeichnis](/documentation/documentation.md)
<br>

# Service Vergabestatistik Integration

The Service Vergabestatistik (SVS) is a component of the Data Service for Public Procurement in Germany (DÖE). Using the SVS, statistical reports based on eForms contract award notices (CANs) can be automatically created and transmitted via the DÖE to the Federal Statistical Office (Statistisches Bundesamt).

![svs-integration](/documentation/images/svs_integration.png)

Use of the service is voluntary. As an alternative to the SVS, you can continue to use the existing reporting channels.

A prerequisite for using the service is that notices are submitted in accordance with the applicable ruleset for SDK 1.14 (or newer).

The service is used automatically when the contract award notice (CAN) submitted to the DÖE's Vermittlungsdienst (VD) contains a valid reporting unit ID in the `BT-001-DEX-NoticeResult` field. The SDK's ruleset then ensures that all business information required to fulfill the reporting obligation is contained in the notice.

After the notice has been successfully submitted to the Vermittlungsdienst, a Vergabestatistik report is automatically generated and transmitted to the Federal Statistical Office at the end of the reporting deadline.

## Information on Processing Status in the SVS

In the Self-Service Portal (SSP) of the Data Service for Public Procurement, registered users (typically support staff of procurement platform operators) can view not only the processing status for publication to TED and the Bekanntmachungsservice, but also the processing status regarding the statistical report.

In addition, the processing status can also be retrieved via the current version (1.3.8 or newer) of the Vermittlungsdienst endpoint: `/v1/notices/status`. For more information, see https://ozg-vermittlungsdienst.de/.

## Preview Function and Display of the Submitted Statistical Report

For a contract award notice (CAN) available in eForms format, a preview of the statistical report can be displayed via the `/preview` endpoint (without it being forwarded). For more information, see https://svs.datenservice-oeffentlicher-einkauf.de/api-docs/swagger-ui/index.html.
For a contract award notice (CAN) already transmitted to the Data Service for Public Procurement, the associated statistical report can be displayed. This is done via the ReportLink, which is returned in a status query to the Vermittlungsdienst (see "Information on Processing Status in the SVS"). This uses the `/notice/view/{token}` endpoint. For more information, see https://svs.datenservice-oeffentlicher-einkauf.de/api-docs/swagger-ui/index.html.