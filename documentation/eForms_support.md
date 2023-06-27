### EfA-Umsetzungsprojekt "Zugang zur öffentlichen Vergabe"
## Dokumentation Vermittlungsdienst
[Inhaltsverzeichnis](/documentation/documentation.md)
<br>

# eForms Unterstützung - Preview Umgebung
Aktuell werden unterschiedliche eForms-Versionen unterstützt und entsprechend dem folgenden Beispeil verarbeitet. In Zukunft werden vom Vermittlungsdienst, sowohl unterschwellige als auch oberschwellige Bekanntmachungen, ausschließlich im eForms-DE Format angenommen.

<br>

*bis 25.10.2023*

| Version  | Mediator | External validator | Internal validator | eSender   | BKMS  | TED  |
| ------- | -------- | ------------------ | ------------------ | --------- | ----- | ---- |
| eForms-EU 0.1.1 | ja, aber nur für Unterschwellenvergabe | \-  | ja | \-  | ja, aber nur für Unterschwellenvergabe | nein    |
| eForms-EU 1.0   | ja, aber nur für Unterschwellenvergabe | \-  | ja | \-  | ja, aber nur für Unterschwellenvergabe | nein    |
| eforms-EU 1.5   | nein  | ja | ja | ja | \-  | nur akzeptiert  1.3 und folgenden Versionen bis Januar 2024  |
| eForms-DE 1.0.1 (schematron 0.5.0) | ja | ja | ja | ja | ja | ja, nach Umstellung in eForms-EU 1.5.1  |
| eForms-DE 1.1  | geplante Unterstützung bis Oktober 2023 | geplante Unterstützung bis Oktober 2023 | geplante Unterstützung bis Oktober 2023 | geplante Unterstützung bis Oktober 2023 | geplante Unterstützung bis Oktober 2023 | ja, nach Umstellung in eForms-EU 1.7.0<br><br>geplante Unterstützung bis Oktober 2023 |

<br>

*ab 25.10.2023 (Production Environment)*

| Version                               | Mediator                        | External validator | Internal validator | eSender    | BKMS      | TED       |
| ------------------------------------- | ------------------------------- | ------------------ | ------------------ | ---------- | --------- | ------------ |
| eForms-EU 0.1.1                       | ja, aber nur für Unterschwellenvergabe | \-                 | ja                | \-         | ja, aber nur für Unterschwellenvergabe | nein    |
| eForms-EU 1.0                         | ja, aber nur für Unterschwellenvergabe | \-                 | ja                | \-         | ja, aber nur für Unterschwellenvergabe | nein    |
| eforms-EU 1.5                         | nein                          | ja                | ja                | ja        | \-        | ja          |
| eForms-DE 1.0.1 (schematron 0.5.0)    | ja                            | ja                | ja                | ja        | ja       | ja, nach Umstellung in eForms-EU 1.5.1 |
| eforms-EU 1.7 (future implementation) | nein                          | ja                | ja                | geplante Unterstützung | \-   | ja  |
| eForms-DE 1.1 (recommended version)   | ja                            | ja                | ja                | ja                     | ja  | ja, nach Umstellung in eForms-EU 1.7.0 |


## eForms Validierung
Alle Bekanntmachungen werden bei der Übermittlung an den Vermittlungsdienst, bevor Sie vom System angenommen werden, validiert. Die Validierung erfolgt anhand einer Kombination aus einer XML-Schema-Validierung und einer Schematron-Validierung. Als Ergebnis wird ein Validierungsreport im JSON-Format zurückgegeben.

### Validierungs Blacklist

Regeln die bei der Validierung mit Schematron EU und DE Regeln ignoriert werden sollen:

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




