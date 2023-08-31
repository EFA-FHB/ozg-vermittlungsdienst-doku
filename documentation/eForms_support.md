### EfA-Umsetzungsprojekt "Zugang zur öffentlichen Vergabe"
## Dokumentation Vermittlungsdienst
[Inhaltsverzeichnis](/documentation/documentation.md)
<br>

# eForms Unterstützung
Aktuell werden unterschiedliche eForms-Versionen unterstützt und entsprechend dem folgenden Beispiel verarbeitet. In Zukunft werden vom Vermittlungsdienst sowohl unterschwellige als auch oberschwellige Bekanntmachungen ausschließlich im eForms-DE Format angenommen.

<br>

*Übersicht an bestehenden eForms-DE-Versionen und den dazugehörigen technischen Artefakten und Hilfsmitteln:*
| eForms-DE Standard | KoSIT Schematron                                                                  | KoSIT Codelisten                                                                          | SDK-DE                                                                                                                                             | eForms-DE Offline Validator                                                                                                | wird angenommen bis |
|--------------------|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|------------|
| [eForms-DE 1.0.1](https://xeinkauf.de/app/uploads/2023/03/specification-eforms-de-v1.0.1.pdf)    | [0.5.2](https://projekte.kosit.org/eforms/eforms-de-schematron/-/releases/v0.5.2) | [2023-05-17](https://projekte.kosit.org/eforms/eforms-de-codelist/-/releases/v2023-05-17) | [1.0.1_1.5.3_20230727](https://gitlab.opencode.de/OC000008125155/SDK-eforms-de/-/tree/SDK-DE_1.0.1_1.5.3_20230727?ref_type=tags)                   | [1.0.3](https://github.com/EFA-FHB/eforms-validator-core/releases/tag/1.0.3) unterstützt eForms-DE 1.0.1 & 1.1.0 |    31.01.2024        |
| [eForms-DE 1.1](https://xeinkauf.de/app/uploads/2023/08/specification-eforms-de-v1.1.0.pdf)      | [0.6.0](https://projekte.kosit.org/eforms/eforms-de-schematron/-/releases/v0.6.0) | [2023-07-07](https://projekte.kosit.org/eforms/eforms-de-codelist/-/releases/v2023-07-07) | [1.1.0_1.7.0](https://gitlab.opencode.de/OC000008125155/SDK-eforms-de/-/tags/SDK-DE_1.1.0_1.7.0) | [1.0.3](https://github.com/EFA-FHB/eforms-validator-core/releases) unterstützt eForms-DE 1.0.1 & 1.1.0           |   11.05.2024         |


<br>

*Folgende Versionen können bis 25.10.2023 im Vermittlungsdienst eingeliefert werden:*

| Version  | Vermittlungsdienst | External validator |  eSender-Hub   | BKMS  | TED  |
| ------- | -------- |  ------------------ | --------- | ----- | ---- |
| eForms-EU 0.1.1 | ja, aber nur für Unterschwellenvergabe | nein  |  nein  | ja, aber nur für Unterschwellenvergabe | nein    |
| eForms-EU 1.0   | ja, aber nur für Unterschwellenvergabe | nein | nein  | ja, aber nur für Unterschwellenvergabe | nein    |
| eforms-EU 1.5   | nur in der Preview-Umgebung, NICHT in Prod  | ja |  ja | nein  | ja, bis 31.01.2024  |
| eForms-DE 1.0.1 (schematron 0.5.2) | ja | ja | ja |  ja | ja, nach Umwandlung im eSender-Hub in eForms-EU 1.5.1, bis 31.01.2024  |
| eForms-DE 1.1  | geplante Unterstützung in KW37 2023 |  geplante Unterstützung in KW37 2023 | ja | geplante Unterstützung in KW37 2023 | ja, nach Umwandlung im eSender-Hub in eForms-EU 1.7.0<br><br>geplante Unterstützung in KW37 2023, bis 11.05.2024 |

<br>

*Folgende Versionen können ab 25.10.2023 im Prod Environment im Vermittlungsdienst eingeliefert werden:*

| Version                               | Vermittlungsdienst                       | External validator |  eSender-Hub    | BKMS      | TED       |
| ------------------------------------- | ------------------------------- | ------------------ | ---------- | --------- | ------------ |
| eForms-EU 0.1.1                       | ja, aber nur für Unterschwellenvergabe | nein                | ja                |  ja, aber nur für Unterschwellenvergabe | nein    |
| eForms-EU 1.0                         | ja, aber nur für Unterschwellenvergabe | nein                 | ja                |  ja, aber nur für Unterschwellenvergabe | nein    |
| eforms-EU 1.5                         | nein                          | ja                | ja                |  nein        | ja, bis 31.01.2024         |
| eForms-DE 1.0.1 (schematron 0.5.2)    | ja                            | ja                | ja                |  ja       | ja, nach Umwandlung im eSender-Hub in eForms-EU 1.5.2, bis 31.01.2024 |
| eForms-DE 1.1 (Empfohlene Version)   | ja                            | ja                | ja                | ja                     | ja, nach Umwandlung im eSender-Hub in eForms-EU 1.7.0, bis 11.05.2024 |

Bitte beachten Sie: Nach dem 25.10.2023 werden im Produktivsystem ausschließlich eForms-DE Versionen unterstützt. Wir empfehlen die Version eForms-DE 1.1 zu verwendet. 

## eForms Validierung
Alle Bekanntmachungen werden bei der Übermittlung an den Vermittlungsdienst, bevor Sie vom System angenommen werden, validiert. Die Validierung erfolgt anhand einer Kombination aus einer XML-Schema-Validierung und einer Schematron-Validierung. Als Ergebnis wird ein Validierungsreport im JSON-Format zurückgegeben.

Eine Möglichkeit zur Offline Validierung, so wie sie auch der Vermittlungsdienst durchführt, bietet der Open Source Validator https://github.com/EFA-FHB/eforms-validator-core

### Validierungs Blacklist

Durch das Nationale Tailoring entstehen Unterschiede zwischen in der EU und national zugelassenen Werten, beispilesweise bei Codellisten und der customizationID: Deshalb müssen bestimmte EU Regeln aübersprungen werden, ob nach deutschem Tailoring valide Dokumente zu validieren. 

Die folgenden Regeln sollten ignoriert werden:

| Content                       | BT Field | Rule to be ignored |
| ----------------------------- | -------- | ------------------ |
| CustomizationID               |          | BR-OPT-00002-0052  |
| buyer-contracting-type.gc     | BT-740   | BR-BT-00740-0052   |
| buyer-legal-type.gc           | BT-11    | BR-BT-00011-0052   |
| criterion-exclusion-ground.gc | BT-67    | BR-BT-00067-0104   |
| gpp-criteria.gc               | BT-165   | BR-BT-00165-0052   |
| missing-info-submission.gc    | BT-771   | BR-BT-00001-0155   |
| procurement-procedure-type.gc | BT-105   | BR-BT-00105-0052   |
| received-submission-type.gc   | BT-760   | BR-BT-00760-0052   |
| social-objective.gc           | BT-775   | BR-BT-00775-0051   |




