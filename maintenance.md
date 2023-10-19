# Go-live-Ticker


Hier finden Sie aktuelle Informationen in Vorbereitung auf den 25.10.2023 und kontinuierliche Updates zwischen 25.-27.10.2023.

## ! Wichtige Hinweise zur Erstellung von eForms !
Um eine reibungslose Einlieferung zu gewährleisten, beachten Sie bitte immer die folgenden Aspekte: 

- Die Rolle **ted-esen** darf in Bekanntmachungen NICHT verwendet werden, weder als org-role noch als org-sub-role. Dies führt zu Problemen in der Transformation, da immer automatisch das BeschA als ted-esen gesetzt wird

- Das Feld **BT-05 Notice Dispatch date** **(IssueDate)** muss zwischen gestern und morgen liegen, sonst lehnt TED die Bekanntmachung ab. Dies wird derzeit NICHT im Vermittlungsdienst geprüft, da es sich um eine neue dynamische Regel von TED handelt
- Die Befüllung des Feldes **BT-165 Winner Size (Winner Size)** wird derzeit nicht von den deutschen Regeln geprüft. Bitte stellen Sie selbstständig sicher, dass dieses Feld für die folgenden Notice Types korrekt befüllt wird: '25', '26', '27', '28', '29', '30', '31', '32', 'E4', '33', '34', '35', '36' & '37'
- Derzeit besteht ein Bug bei TED, dass **Zuwendungsempfänger** <u>keine Dienstleistungen</u> ausschreiben können. Sollten Sie hiervon betroffen sein (Bekanntmachung schlägt fehl wegen Regel **BR-BT-00262-0211**), melden Sie sich bitte umgehend bei unserem Support support-oeffentlichevergabe@bdr.de für spezifische Hilfestellungen
- Für die Befüllung der **BT-501 Identifikationsnummer (der Organisation)** beachten Sie bitte die Hinweise u. A. zur Leitweg-ID in unserer FAQ: https://github.com/EFA-FHB/ozg-vermittlungsdienst-doku/blob/main/faq.md#identifikationsnummer-organisation-bt-501


## Bekannte Probleme
Sollten während des Go-live Probleme auftreten, werden Sie in diesem Abschnitt aktuelle Informationen finden. 

**Derzeit keine bekannten Probleme. **

# Bekannte Wartungsfenster



## Anstehende Wartungsfenster

| Umgebung    | System              | Datum      | Zeit              | Kommentar           |
|-------------|---------------------|------------|-------------------|---------------------|
| DöE Produktion + Staging | alle Services außer BKMS | 20.10.2023 | 10:00 - 13:00 CEST | Deployment für Performanceverbesserungen | 


# Bekannte Bugs 

| System       | vorhanden seit      | voraussichtliche Behebung   | Fehler           |
|--------------|--------------------------|-----------------------------|---------------------|
| SSP Staging + Production | 04.10.2023 |  | Bilder in Dokumentation können nicht dargestellt werden, bitte vorübergehend https://portal.preview-ozg-vermittlungsdienst.de nutzen |
| TED Preview  | 09.08.2023               | 25.08.2023                   | Bekanntmachungen ab dem 09.08.2023 werden durch TED nicht mehr in den Status 'PUBLISHED' gesetzt, sie bleiben in 'ACCEPTED' hängen auf Grund eines Fehlers seitens TED |


# Hinweise

Am 27.09.2023 wurde der API-Key für die Einlieferung bei TED angepasst. Aus diesem Grund werden Statusinformationen für Bekanntmachungen, die vor diesem Datum in Staging oder Preview eingeliefert wurden, nicht mehr bei TED abgefragt. Dies ist eine einmalige Anpassung und wird in Zukunft nicht wieder vorkommen. 


## Vergangene Wartungsfenster

| Umgebung    | System              | Datum      | Zeit              | Kommentar           |
|-------------|---------------------|------------|-------------------|---------------------|
| DöE Produktion + Staging | alle Services außer BKMS | 10.10.2023 | 09:00 - 12:00 CEST | Rechenzentrumswartung | 
| TED Preview | TED Apps for eForms | 10.10.2023 | 07:00 - 10:00 CEST | Angekündigt von TED | 
| TED Production | TED Apps for eForms | 11.10.2023 | 07:00 - 10:00 CEST | Angekündigt von TED | 
| TED Produktion + Preview | TED Developer Portal, TED Apps for eForms | 02.10.2023 | 07:00 - 09:00 CEST | Angekündigt von TED | 
| TED Produktion | TED Apps for eForms | 27.09.2023 | 07:00 - 09:00 CEST | Angekündigt von TED |
| DÖE Produktion  | Vermittlungsdienst| 14.09.2023| 08:00 - 09:30 Uhr | vorrübergehend nicht erreichbar | 
| TED Produktion| TED Apps for eForms | 30.08.2023 | 18:00-22:00 CEST | Angekündigt von TED | 
| TED Produktion| TED Apps for eForms | 30.08.2023 | 18:00-22:00 CEST | Angekündigt von TED |
| TED Preview | TED Apps for eForms | 28.08.2023 | 07:00-11:00 CEST  | Angekündigt von TED |
| TED Preview | TED Apps for eForms | 24.08.2023 | 07:00-08:00 CEST  | Angekündigt von TED |
| TED Produktion| TED Apps for eForms | 23.08.2023 | 07:00-08:00 CEST | Angekündigt von TED | 
