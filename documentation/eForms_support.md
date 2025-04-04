### Datenservice Öffentlicher Einkauf
[Inhaltsverzeichnis](/documentation/documentation.md)
<br>

# eForms-Unterstützung
Aktuell werden unterschiedliche eForms-Versionen unterstützt und entsprechend dem folgenden Beispiel verarbeitet. In Zukunft werden vom Vermittlungsdienst sowohl unterschwellige als auch oberschwellige Bekanntmachungen ausschließlich im eForms-DE-Format angenommen.

<br>

*Übersicht an bestehenden eForms-DE-Versionen und den dazugehörigen technischen Artefakten und Hilfsmitteln:*

|eForms-DE-Standard|KoSIT-Schematron|KoSIT-Codelisten|SDK-DE|eForms-DE-Offline-Validator|Akzeptiert ab|Akzeptiert bis|
|--|--|--|--|--|--|--|
|[eForms-DE 2.1](https://projekte.kosit.org/api/v4/projects/356/packages/maven/de/xeinkauf/eforms-de/2.1.0/eforms-de-2.1.0.zip)|[1.0.2](https://projekte.kosit.org/eforms/eforms-de-schematron/-/releases/v1.0.2) [Blacklist](https://projekte.kosit.org/eforms/eforms-de-schematron/-/blob/v1.0.1/src/main/ted-excluded-rules.txt?ref_type=tags)|[2024-12-20](https://projekte.kosit.org/eforms/eforms-de-codelist/-/releases/v2024-12-20)|[1.13.0](https://gitlab.opencode.de/OC000008125155/SDK-eforms-de/-/releases/1.13.0)|[1.3.1](https://projekte.kosit.org/eforms/validator-edition-eforms-de/-/releases/1.3.1) unterstützt eForms-DE 1.1.0, 1.2.0, 2.0.0, 2.1.0| Preview und Stagingumgebungen: ab 17.03.2025 <br> Produktionsumgebung: ab 28.04.2025 |28.11.2025 (ohne Support bis 31.03.2027)|
|[eForms-DE 2.0](https://projekte.kosit.org/api/v4/projects/356/packages/maven/de/xeinkauf/eforms-de/2.0.0/eforms-de-2.0.0.zip)|[0.9.4](https://projekte.kosit.org/eforms/eforms-de-schematron/-/releases/v0.9.4) [Blacklist](https://projekte.kosit.org/eforms/eforms-de-schematron/-/blob/v0.9.4/src/main/ted-excluded-rules.txt?ref_type=tags)|[2024-09-02](https://projekte.kosit.org/eforms/eforms-de-codelist/-/releases/v2024-09-02)|[1.12.4](https://gitlab.opencode.de/OC000008125155/SDK-eforms-de/-/releases/1.12.4)|[1.3.0](https://projekte.kosit.org/eforms/validator-edition-eforms-de/-/releases/1.3.0) unterstützt eForms-DE 1.1.0, 1.2.0, 2.0.0|07.03.2025|18.07.2025 (ohne Support bis 30.06.2026)|
|[eForms-DE 2.0](https://projekte.kosit.org/api/v4/projects/356/packages/maven/de/xeinkauf/eforms-de/2.0.0/eforms-de-2.0.0.zip)|[0.9.3](https://projekte.kosit.org/eforms/eforms-de-schematron/-/releases/v0.9.3) [Blacklist](https://projekte.kosit.org/eforms/eforms-de-schematron/-/blob/v0.9.3/src/main/ted-excluded-rules.txt?ref_type=tags)|[2024-09-02](https://projekte.kosit.org/eforms/eforms-de-codelist/-/releases/v2024-09-02)|[1.12.3](https://gitlab.opencode.de/OC000008125155/SDK-eforms-de/-/releases/1.12.3)|[1.2.9](https://projekte.kosit.org/eforms/validator-edition-eforms-de/-/releases/1.2.9) unterstützt eForms-DE 1.1.0, 1.2.0, 2.0.0|18.02.2025|18.07.2025 (ohne Support bis 30.06.2026)|
|[eForms-DE 2.0](https://projekte.kosit.org/api/v4/projects/356/packages/maven/de/xeinkauf/eforms-de/2.0.0/eforms-de-2.0.0.zip)|[0.9.2](https://projekte.kosit.org/eforms/eforms-de-schematron/-/releases/v0.9.2) [Blacklist](https://projekte.kosit.org/eforms/eforms-de-schematron/-/blob/v0.9.2/src/main/ted-excluded-rules.txt?ref_type=tags)|[2024-09-02](https://projekte.kosit.org/eforms/eforms-de-codelist/-/releases/v2024-09-02)|[1.12.2](https://gitlab.opencode.de/OC000008125155/SDK-eforms-de/-/releases/1.12.2)|[1.2.7](https://projekte.kosit.org/eforms/validator-edition-eforms-de/-/releases/1.2.7) unterstützt eForms-DE 1.1.0, 1.2.0, 2.0.0|12.12.2024|18.07.2025 (ohne Support bis 30.06.2026)|
|[eForms-DE 2.0](https://projekte.kosit.org/api/v4/projects/356/packages/maven/de/xeinkauf/eforms-de/2.0.0/eforms-de-2.0.0.zip)|[0.9.1](https://projekte.kosit.org/eforms/eforms-de-schematron/-/releases/v0.9.1) [Blacklist](https://projekte.kosit.org/eforms/eforms-de-schematron/-/blob/v0.9.1/src/main/ted-excluded-rules.txt?ref_type=tags)|[2024-09-02](https://projekte.kosit.org/eforms/eforms-de-codelist/-/releases/v2024-09-02)|[1.12.1](https://gitlab.opencode.de/OC000008125155/SDK-eforms-de/-/releases/1.12.1)|[1.2.6](https://projekte.kosit.org/eforms/validator-edition-eforms-de/-/releases/1.2.6) unterstützt eForms-DE 1.1.0, 1.2.0, 2.0.0|01.11.2024|18.07.2025 (ohne Support bis 30.06.2026)|
|[eForms-DE 1.2](https://xeinkauf.de/app/uploads/2024/02/specification-eforms-de-v1.2.0.pdf)|[0.8.4](https://projekte.kosit.org/eforms/eforms-de-schematron/-/releases/v0.8.4) [Blacklist](https://projekte.kosit.org/eforms/eforms-de-schematron/-/blob/v0.8.4/src/main/ted-excluded-rules.txt?ref_type=tags) |[2024-02-06](https://projekte.kosit.org/eforms/eforms-de-codelist/-/releases/v2024-02-06)|[1.2.0_1.10.3](https://gitlab.opencode.de/OC000008125155/SDK-eforms-de/-/tags/SDK-DE_1.2.0_1.10.3_0)|[1.0.15](https://github.com/EFA-FHB/eforms-validator-core/releases/tag/1.0.15) unterstützt eForms-DE 1.1.0 & 1.2.0|08.07.2024|31.07.2025
|[eForms-DE 1.2](https://xeinkauf.de/app/uploads/2024/02/specification-eforms-de-v1.2.0.pdf)|[0.8.3](https://projekte.kosit.org/eforms/eforms-de-schematron/-/releases/v0.8.3) [Blacklist](https://projekte.kosit.org/eforms/eforms-de-schematron/-/blob/v0.8.3/src/main/ted-excluded-rules.txt?ref_type=tags) |[2024-02-06](https://projekte.kosit.org/eforms/eforms-de-codelist/-/releases/v2024-02-06)|[1.2.0_1.10.2](https://gitlab.opencode.de/OC000008125155/SDK-eforms-de/-/releases/SDK-DE_1.2.0_1.10.2_0)|[1.0.14](https://github.com/EFA-FHB/eforms-validator-core/releases/tag/1.0.14) unterstützt eForms-EU 1.10 (nur T01+T02), eForms-DE 1.1.0 und eForms-DE 1.2.0|27.03.2024|31.07.2025|
|[eForms-DE 1.1](https://xeinkauf.de/app/uploads/2023/08/specification-eforms-de-v1.1.0.pdf)|[0.7.2](https://projekte.kosit.org/eforms/eforms-de-schematron/-/releases/v0.7.2) [Blacklist](https://projekte.kosit.org/eforms/eforms-de-schematron/-/blob/v0.7.2/src/main/ted-excluded-rules.txt?ref_type=tags) |[2023-07-07](https://projekte.kosit.org/eforms/eforms-de-codelist/-/releases/v2023-07-07)|[1.1.0_1.7.3_1](https://gitlab.opencode.de/OC000008125155/SDK-eforms-de/-/tags/1.1.0_1.7.3_1)|[1.0.12](https://github.com/EFA-FHB/eforms-validator-core/releases/tag/1.0.12) unterstützt eForms-DE 1.0.1 & 1.1.0|13.09.2023|30.04.2025

Außerhalb der eForms-Durchführungsverordnung, auf der der Standard eForms-DE basiert, wurden zur Umsetzung der __Verordnung (EG) Nr. 1370/2007 vom Amt für Veröffentlichungen der EU__ die Formulare __T01__ (_"Vorinformation zu öffentlichen Personenverkehrsdiensten"_) und __T02__ (_"Bekanntmachung über vergebene Aufträge für öffentliche Personenverkehrsdienste"_) definiert, die von der europäischen Veröffentlichungsplattform TED akzeptiert werden. 

Die Formulare T01 und T02 werden auch vom Datenservice Öffentlicher Einkauf unterstützt, so dass diese (zur Weiterleitung an TED und den Bekanntmachungsservice) hier maschinell von Vergabeplattformen auf Basis des SDK-EU oder manuell über das kostenfrei nutzbare [Redaktionssystem](https://resy.datenservice-oeffentlicher-einkauf.de/) eingeliefert werden können.

SDK-EU|Akzeptiert ab|Akzeptiert bis|
|--|--|--|
[1.13.0](https://github.com/OP-TED/eForms-SDK/tree/1.13.0)|Previewumgebung: ab 17.02.2025 <br> Produktionsumgebung: ab 28.04.2025|voraussichtlich <br> bis 31.03.2027|
[1.12.0](https://github.com/OP-TED/eForms-SDK/tree/1.12.0)|01.11.2024|30.06.2026|
[1.10.3](https://github.com/OP-TED/eForms-SDK/tree/1.10.3)|08.07.2024|31.07.2025|





## eForms-Validierung
Alle Bekanntmachungen werden bei der Übermittlung an den Vermittlungsdienst, bevor sie vom System angenommen werden, validiert. Die Validierung erfolgt anhand einer Kombination aus einer XML-Schema-Validierung und einer Schematron-Validierung. Als Ergebnis wird ein Validierungsreport im JSON-Format zurückgegeben.

Eine Möglichkeit zur Offline-Validierung, so wie sie auch der Vermittlungsdienst durchführt, bietet der Open-Source-Validator: https://projekte.kosit.org/eforms/validator-edition-eforms-de

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



