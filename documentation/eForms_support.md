---
title: eForms Unterstützung
---

[Inhaltsverzeichnis](/documentation/documentation.md)
<br>

# Unterstützte eForms-Versionen
Aktuell werden unterschiedliche eForms-Versionen unterstützt und entsprechend der folgenden Übersicht verarbeitet.

<br>

*Übersicht zu bestehenden eForms-DE-Versionen und den dazugehörigen technischen Artefakten und Hilfsmitteln:*

| eForms-DE-Standard | SDK-DE | gültiges Regelwerk | eForms-DE-Offline-Validator                                                                                | Akzeptiert ab                                       | Akzeptiert bis | Extended Lifecycle |
|--------------------|--------|--------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|----------------|----------------|
| [eForms-DE 2.1](https://projekte.kosit.org/api/v4/projects/356/packages/maven/de/xeinkauf/eforms-de/2.1.0/eforms-de-2.1.0.zip) | [1.14](https://gitlab.opencode.de/OC000008125155/SDK-eforms-de/-/tree/1.14.4?ref_type=tags) | [1.14.4](https://gitlab.opencode.de/OC000008125155/SDK-eforms-de/-/blob/1.14.4/sdk/docs/Regelwerk.md?ref_type=tags) | 1.4.8 unterstützt eForms-DE 2.0, 2.1 | Staging ab 23.07.2026 <br> Produktion ab 28.07.2028 | 02.12.2026 |ohne Support bis 31.12.2027 |
| [eForms-DE 2.1](https://projekte.kosit.org/api/v4/projects/356/packages/maven/de/xeinkauf/eforms-de/2.1.0/eforms-de-2.1.0.zip) | [1.13](https://gitlab.opencode.de/OC000008125155/SDK-eforms-de/-/tree/1.13.3?ref_type=tags) | [1.13.3](https://gitlab.opencode.de/OC000008125155/SDK-eforms-de/-/tree/1.13.3?ref_type=tags) | [1.4.7](https://projekte.kosit.org/eforms/validator-edition-eforms-de/-/releases/1.4.7) unterstützt eForms-DE 2.0, 2.1 | 28.04.2025                                          | 07.05.2026 |ohne Support bis 31.03.2027 |

Die Formulare __T01__ (_"Vorinformation zu öffentlichen Personenverkehrsdiensten"_) und __T02__ (_"Bekanntmachung über vergebene Aufträge für öffentliche Personenverkehrsdienste"_) dienen der Erfüllung der __Verordnung (EG) Nr. 1370/2007 des Europäischen Parlaments und des Rates__ sowie des __Personenbeförderungsgesetzes (PBefG)__ und werden ab **SDK DE 1.14** unterstützt. Die Nutzung des **SDK-EU** ist hierfür nicht mehr erforderlich. Eine Einlieferung der Formulare über das SDK-EU bleibt jedoch **bis zum Ablauf seiner Gültigkeit** weiterhin möglich. Anschließend werden diese Formulare ausschließlich über das **SDK DE** akzeptiert oder können auch über die Nutzung des [Redaktionssystems](https://resy.datenservice-oeffentlicher-einkauf.de/) eingeliefert werden.

SDK-EU|Akzeptiert ab| Akzeptiert bis                      |
|--|--|-------------------------------------|
[1.14.0](https://github.com/OP-TED/eForms-SDK/tree/1.14.0)|05.02.2026| voraussichtlich <br> bis 31.12.2027 |
[1.13.0](https://github.com/OP-TED/eForms-SDK/tree/1.13.0)|28.04.2025| voraussichtlich <br> bis 31.03.2027 |


## eForms-Validierung
Alle Bekanntmachungen werden bei der Übermittlung an den Vermittlungsdienst validiert, bevor sie vom System angenommen werden. Die Validierung erfolgt anhand einer Kombination aus einer XML-Schema-Validierung und einer Schematron-Validierung. Als Ergebnis wird ein Validierungsreport im JSON-Format zurückgegeben.

Eine Möglichkeit zur Offline-Validierung, wie sie auch der Vermittlungsdienst durchführt, bietet der von KoSIT bereitgestellte [Open-Source-Validator](https://projekte.kosit.org/eforms/validator-edition-eforms-de). <br>
Wir stellen Ihnen auch einen [Online-Validator](https://validator.ozg-vermittlungsdienst.de/q/swagger-ui/) zur Verfügung, mit dem Sie die Validierung Ihrer eForms überprüfen können.

### Validierungs-Blacklist

Durch das nationale Tailoring entstehen Unterschiede zwischen EU-weit und national gültigen Werten, wie dieses beispielsweise bei Codelisten und der customizationID der Fall ist. Deshalb müssen bestimmte EU-Regeln übersprungen werden, um nach deutschem Tailoring valide Dokumente zu überprüfen. Die aktuelle Liste der ignorierten Regeln befindet sich hier: [KoSIT-Repository für den deutschen eForms-Standard](https://projekte.kosit.org/eforms/eforms-de-schematron/-/blob/v0.9.4/src/main/ted-excluded-rules.txt)
