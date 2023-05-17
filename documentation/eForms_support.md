### EfA-Umsetzungsprojekt "Zugang zur öffentlichen Vergabe"
## Dokumentation Vermittlungsdienst
[Inhaltsverzeichnis](/documentation/documentation.md)
<br><br>

# eForms Unterstützung - Preview Umgebung
Aktuell werden unterschiedliche eForms-Versionen unterstützt und entsprechend dem folgenden Beispeil verarbeitet. In Zukunft werden vom Vermittlungsdienst, sowohl unterschwellige als auch oberschwellige Bekanntmachungen, ausschließlich im eForms-DE Format angenommen.

![eForms Version flow](images/eforms_version_flow.png)

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




