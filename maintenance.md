# Bekannte Wartungsfenster



## Anstehende Wartungsfenster

| Umgebung    | System              | Datum      | Zeit              | Kommentar           |
|-------------|---------------------|------------|-------------------|---------------------|
| TED Produktion | TED Apps for eForms | 27.09.2023 | 07:00 - 09:00 CEST | Angekündigt von TED |

## Vergangene Wartungsfenster

| Umgebung    | System              | Datum      | Zeit              | Kommentar           |
|-------------|---------------------|------------|-------------------|---------------------|
| DöE Produktion  | Vermittlungsdienst| 14.09.2023| 08:00 - 09:30 Uhr | vorrübergehend nicht erreichbar | 
| TED Produktion| TED Apps for eForms | 30.08.2023 | 18:00-22:00 CEST | Angekündigt von TED | 
| TED Preview | TED Apps for eForms | 28.08.2023 | 07:00-11:00 CEST  | Angekündigt von TED |
| TED Preview | TED Apps for eForms | 24.08.2023 | 07:00-08:00 CEST  | Angekündigt von TED |
| TED Produktion| TED Apps for eForms | 23.08.2023 | 07:00-08:00 CEST | Angekündigt von TED | 


# Bekannte Bugs 

| System       | vorhanden seit      | voraussichtliche Behebung   | Fehler           |
|--------------|--------------------------|-----------------------------|---------------------|
| Vermittlungsdienst (Preview) | 14.09.2023 | eforms-de-schematron 0.6.2 | eForms-DE erlaubt Unterschiede zwischen issueDate und requestedPublicationDate bis zu max. 92 Tagen (eforms-DE 1.0.1) und 60 Tagen (eForms-DE 1.1), während von TED maximal 91 und 59 Tage erlaubt sind | 
| Vermittlungsdienst Staging + Produktion | 07.09.2023  |  13.09.2023       | Bekanntmachungen können über den /v1/notices/stop/{trackingCode} aktuell nicht gestoppt werden | 
| TED Preview  | 09.08.2023               | 25.08.2023                   | Bekanntmachungen ab dem 09.08.2023 werden durch TED nicht mehr in den Status 'PUBLISHED' gesetzt, sie bleiben in 'ACCEPTED' hängen auf Grund eines Fehlers seitens TED |
