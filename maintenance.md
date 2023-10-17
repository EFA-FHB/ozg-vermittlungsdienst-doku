# Bekannte Wartungsfenster



## Anstehende Wartungsfenster

| Umgebung    | System              | Datum      | Zeit              | Kommentar           |
|-------------|---------------------|------------|-------------------|---------------------|
| DöE Produktion + Staging | alle Services außer BKMS | 19.10.2023 | 09:00 - 12:00 CEST | Rechenzentrumswartung | 
| TED Preview | TED Apps for eForms | 10.10.2023 | 07:00 - 10:00 CEST | Angekündigt von TED | 
| TED Production | TED Apps for eForms | 11.10.2023 | 07:00 - 10:00 CEST | Angekündigt von TED | 

## Vergangene Wartungsfenster

| Umgebung    | System              | Datum      | Zeit              | Kommentar           |
|-------------|---------------------|------------|-------------------|---------------------|
| TED Produktion + Preview | TED Developer Portal, TED Apps for eForms | 02.10.2023 | 07:00 - 09:00 CEST | Angekündigt von TED | 
| TED Produktion | TED Apps for eForms | 27.09.2023 | 07:00 - 09:00 CEST | Angekündigt von TED |
| DÖE Produktion  | Vermittlungsdienst| 14.09.2023| 08:00 - 09:30 Uhr | vorrübergehend nicht erreichbar | 
| TED Produktion| TED Apps for eForms | 30.08.2023 | 18:00-22:00 CEST | Angekündigt von TED | 
| TED Produktion| TED Apps for eForms | 30.08.2023 | 18:00-22:00 CEST | Angekündigt von TED |
| TED Preview | TED Apps for eForms | 28.08.2023 | 07:00-11:00 CEST  | Angekündigt von TED |
| TED Preview | TED Apps for eForms | 24.08.2023 | 07:00-08:00 CEST  | Angekündigt von TED |
| TED Produktion| TED Apps for eForms | 23.08.2023 | 07:00-08:00 CEST | Angekündigt von TED | 

# Bekannte Bugs 

| System       | vorhanden seit      | voraussichtliche Behebung   | Fehler           |
|--------------|--------------------------|-----------------------------|---------------------|
| SSP Staging + Production | 04.10.2023 |  | Bilder in Dokumentation können nicht dargestellt werden, bitte vorübergehend https://portal.preview-ozg-vermittlungsdienst.de nutzen |
| TED Preview  | 09.08.2023               | 25.08.2023                   | Bekanntmachungen ab dem 09.08.2023 werden durch TED nicht mehr in den Status 'PUBLISHED' gesetzt, sie bleiben in 'ACCEPTED' hängen auf Grund eines Fehlers seitens TED |


# Hinweise

Am 27.09.2023 wurde der API-Key für die Einlieferung bei TED angepasst. Aus diesem Grund werden Statusinformationen für Bekanntmachungen, die vor diesem Datum in Staging oder Preview eingeliefert wurden, nicht mehr bei TED abgefragt. Dies ist eine einmalige Anpassung und wird in Zukunft nicht wieder vorkommen. 
