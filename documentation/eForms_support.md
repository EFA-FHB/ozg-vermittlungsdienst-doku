### Datenservice Öffentlicher Einkauf
[Inhaltsverzeichnis](/documentation/documentation.md)
<br>

# eForms-Unterstützung
Aktuell werden unterschiedliche eForms-Versionen unterstützt und entsprechend dem folgenden Beispiel verarbeitet. In Zukunft werden vom Vermittlungsdienst sowohl unterschwellige als auch oberschwellige Bekanntmachungen ausschließlich im eForms-DE-Format angenommen.

<br>

*Übersicht an bestehenden eForms-DE-Versionen und den dazugehörigen technischen Artefakten und Hilfsmitteln:*
| eForms-DE-Standard | KoSIT-Schematron  | KoSIT-Codelisten   | SDK-DE  | eForms-DE-Offline-Validator      | Akzeptiert ab | Akzeptiert bis |
|--------------------|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|------------|------------|
| [eForms-DE 1.2](https://xeinkauf.de/app/uploads/2024/02/specification-eforms-de-v1.2.0.pdf)      | [0.8.4](https://projekte.kosit.org/eforms/eforms-de-schematron/-/releases/v0.8.4) | [2024-02-06](https://projekte.kosit.org/eforms/eforms-de-codelist/-/releases/v2024-02-06) | [1.2.0_1.10.3](https://gitlab.opencode.de/OC000008125155/SDK-eforms-de/-/tags/SDK-DE_1.2.0_1.10.3_0) | [1.0.15](https://github.com/EFA-FHB/eforms-validator-core/releases/tag/1.0.15) unterstützt eForms-DE 1.1.0 & 1.2.0           | 08.07.2024 | 28.02.2025 |
| [eForms-DE 1.2](https://xeinkauf.de/app/uploads/2024/02/specification-eforms-de-v1.2.0.pdf) | [0.8.3](https://projekte.kosit.org/eforms/eforms-de-schematron/-/releases/v0.8.3) | [2024-02-06](https://projekte.kosit.org/eforms/eforms-de-codelist/-/releases/v2024-02-06) | [1.2.0_1.10.2](https://gitlab.opencode.de/OC000008125155/SDK-eforms-de/-/releases/SDK-DE_1.2.0_1.10.2_0) | [1.0.14](https://github.com/EFA-FHB/eforms-validator-core/releases/tag/1.0.14) unterstützt eForms-EU 1.10 (nur TO1+T02), eForms-DE 1.1.0 und eForms-DE 1.2.0 | 27.03.2024 | 28.02.2025 |
| [eForms-DE 1.1](https://xeinkauf.de/app/uploads/2023/08/specification-eforms-de-v1.1.0.pdf)      | [0.7.2](https://projekte.kosit.org/eforms/eforms-de-schematron/-/releases/v0.7.2) | [2023-07-07](https://projekte.kosit.org/eforms/eforms-de-codelist/-/releases/v2023-07-07) | [1.1.0_1.7.3_1](https://gitlab.opencode.de/OC000008125155/SDK-eforms-de/-/tags/1.1.0_1.7.3_1) | [1.0.12](https://github.com/EFA-FHB/eforms-validator-core/releases/tag/1.0.12) unterstützt eForms-DE 1.0.1 & 1.1.0           | 13.09.2023 | 28.02.2025 |

## eForms-Validierung
Alle Bekanntmachungen werden bei der Übermittlung an den Vermittlungsdienst, bevor sie vom System angenommen werden, validiert. Die Validierung erfolgt anhand einer Kombination aus einer XML-Schema-Validierung und einer Schematron-Validierung. Als Ergebnis wird ein Validierungsreport im JSON-Format zurückgegeben.

Eine Möglichkeit zur Offline-Validierung, so wie sie auch der Vermittlungsdienst durchführt, bietet der Open-Source-Validator: https://github.com/EFA-FHB/eforms-validator-core.

### Validierungs-Blacklist

Durch das nationale Tailoring entstehen Unterschiede zwischen in der EU und national zugelassenen Werten, beispielsweise bei Codelisten und der customizationID: Deshalb müssen bestimmte EU-Regeln übersprungen werden, um nach deutschem Tailoring valide Dokumente zu validieren. 

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



