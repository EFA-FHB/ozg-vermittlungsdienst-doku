### EfA-Umsetzungsprojekt "Zugang zur öffentlichen Vergabe"**
# Releases
[Übersicht](/Readme.md)
<br>

## Production Release Juni 
Status: Veröffentlicht 28.06.2023<br>
<details>
<summary>Release notes</summary>

### Vermittlungsdienst
>**Umgebungen** <br>
>Preview Umgebung https://preview.ozg-vermittlungsdienst.de<br>
>Staging Umgebung https://staging.ozg-vermittlungsdienst.de<br>
>Production Umgebung https://ozg-vermittlungsdienst.de<br>

>**Info** <br>
>Nach dem Produktionsrelease im Juni muss für die Produktions- und Stagingumgebung erneut ein User angefragt werden, auch wenn in Preview bereits ein User besteht. 

- Stop-Endpoint zum stoppen von nationalen Bekanntmachungen im BKMS hinzugefügt
- Prüfung dass Aktualisierungen von Bekanntmachungen nicht möglich sind, wenn die vorherige Version nicht gestoppt wurde oder wenn sie bereits veröffentlicht ist
- Open-Api-Beschreibung angepasst
- Verbesserte Fehlermeldungen bei der Rückgabe von Informationen an FVH
- Metriken hinzugefügt, um die letzten erfolgreichen und erfolglosen Endpunktaufrufe zusammen mit den geplanten Jobläufen zu messen
- Mehrere Optimierungen und Fehlerbehebungen
- Einführung von Paging für geplante Jobs
- Prüfung von auftretenden Aktualisierungen von eSender verbessert
- Die Integration des internen Validator wurde verbessert, die Fehlertypen sind nun klarer klassifiziert.
- Die Antwort auf das Datum der letzten Aktualisierung der PSPs wurde aktualisiert und ist nun genauer.
- Geänderte Namen für Fehlergründe:
Anstelle von DELIVERY_NOT_FOUND steht NOTICE_NOT_FOUND
Anstelle von DELIVERY_ALREADY_PROCESSED steht NOTICE_ALREADY_PROCESSED
Anstelle von DELIVERY_METADATA_INVALID steht NOTICE_METADATA_INVALID
- Neuer Endpunkt /v1/notices/status erstellt - Gibt die Statusinformationen für Bekanntmachungen innerhalb eines bestimmten Zeitraums zurück.

### eSender-Hub
- Manueller Stopp in BKMS implementiert, wenn PSP die Benachrichtigung stoppt
- Automatische Stopp in BKMS aufgrund von TED NOT_PUBLISHED implementiert
- Aktualisierte Übersetzungen für Fehlermeldungen
- Transformationen umgesetzt: Versionsumwandlung von eform-de-1.0 nach eform-sdk-1.5 und Umwandlung von DE-Codelisten in EU-Codelisten
- Implementiert: Abrufen und Speichern des BKMS-Status PUBLISHED
- Jobs PROCESS_NOTICES und ALIGN_TED_STATUS verbessert
- Einführung einer Anwendung zur Kontoverwaltung
- Verbesserte Antwort für Mediator im Falle von Duplikaten
- API-Schlüssel für Produktions- und Staging-Benutzer wurden aktualisiert
- Performance Verbesserungen
- Mehrere Optimierungen und Fehlerbehebungen
</details>
<br>

## Preview Release Mai 
Status: Veröffentlicht 04.05.2023<br>
<details>
<summary>Release notes</summary>
<br>

### Vermittlungsdienst
Preview Umgebung https://bkms-mediator-app-preview.efa-fhb.apps-int.nortal.com
- Erweiterung der API Autorisierung um Refresh Token<br>
Details unter [Anbindung an den Vermittlungsdienst](/documentation/Connection_to_mediator.md)

- Erweiterung der Statusinformationen um Transferinformationen (Warnungen und Fehlermeldungen).<br> 
Details unter [Status- und Transferinformationen](/documentation/Status_information.md)
- Detailliertere Fehlermeldungen 
- Versionsprüfung erfolgt nun zusätzlich anhand der Daten des Bekanntmachungsservice<br>
Bei Übermittlung einer Änderungsmitteilung einer unterschwelligen Bekanntmachung erfolgen folgende Prüfungen:<br>
-Ist die zu ändernde Bekanntmachung im BKMS vorhanden?<br>
-Sind bereits mehrere Bekanntmachungen im BKMS vorhanden, deren verkettete noticeId und noticeVersion mit dem Change Notice Version Identifier übereinstimmen?<br>
-Ist eine Änderungsmitteilung im BKMS vorhanden, welche die zu ändernde Version bereits aktualisiert hat?<br>
Das heißt es wird nur die neueste Version in einer Kette von Bekanntmachungen aktualisiert.
- Im Bekanntmachungsservice veröffentlichte unterschwellige Bekanntmachungen erhalten den Status PUBLISHED.<br>
Der Status wird bei einer Statusabfrage entsprechend zurückgegeben.
- Mehrere Optimierungen und Fehlerbehebungen
<br><br>

### Validator
Preview Umgebung https://eforms-validator-preview.efa-fhb.apps-int.nortal.com 
- Erweiterung des Ergebnis-Reports um die Regelbezeichnung `rule` und die angewandte Regel `ruleContent` 

- Mehrere Optimierungen und Fehlerbehebungen
</details>
<br>

## Vergleich geplanter Features in Preview Release und Production Release 
<details>
<summary>Vergleich anzeigen</summary>
<table class="wrapped">
  <colgroup>
    <col/>
    <col/>
    <col/>
    <col/>
    <col/>
  </colgroup>
  <tbody>
    <tr>
      <th scope="col">Feature</th>
      <th scope="col">Komponente</th>
      <th scope="col">Preview Release 31.3.2023</th>
      <th scope="col">Production Release</th>
      <th scope="col">Kommentar</th>
    </tr>
    <tr>
      <td>Registrierung und Anlegen eines<strong> Users in</strong> <strong>Keycloak</strong>
      </td>
      <td>Keycloak</td>
      <td>
        <p>
          ✅
        </p>
        <p>Ja (Keycloak Preview)</p>
      </td>
      <td>
        <p>
          ✅
        </p>
        <p>Ja (Keycloak Preview) und (Keycloak Production)</p>
      </td>
      <td>Es ist zu beachten, dass separate User für Preview und Production gepflegt werden müssen. Weitere Informationen finden Sie unter [Anbindung an den Vermittlungsdienst](Connection_to_mediator.md)
      </td>
    </tr>
    <tr>
      <td>Generierung eines <strong>API-Keys in Keycloak</strong> zum Einsenden in den Mediator </td>
      <td>Keycloak</td>
      <td>
        <p>
          ✅
        </p>
        <p>Ja (Keycloak Preview)</p>
      </td>
      <td>
        <p>
          ✅
        </p>
        <p>Ja (Keycloak Preview) und (Keycloak Production)</p>
      </td>
      <td>Es ist zu beachten, dass separate User für Preview und Production gepflegt werden müssen. Ein API-Key ist 24h gültig und muss danach erneuert werden</td>
    </tr>
    <tr>
      <td>Validieren von eForms-DE 1.0 über den externen<strong> eForms Validator Service</strong>
      </td>
      <td>eForms Validator</td>
      <td>
        <p>
          ✅
        </p>
        <p>Ja</p>
      </td>
      <td>
        <p>
          ✅
        </p>
        <p>Ja</p>
      </td>
      <td>
        <br/>
      </td>
    </tr>
    <tr>
      <td>Einliefern, akzeptieren und validieren von <strong>eForms-EU 0.1.1, 1.0 und 1.5 </strong>
      </td>
      <td>Mediator</td>
      <td>
        <p>
          ✅
        </p>
        <p>Ja</p>
      </td>
      <td>
        <p>✅</p>
        <p>vorraussichtlich ja</p>
      </td>
      <td>Ab Produktion sollte ein neuerer, deutscher Standard verwendet werden, vorzugsweise eForms-DE 1.0.0 oder aktueller. Alte Standards können ggf. noch für eine Übergangszeit unterstützt werden</td>
    </tr>
    <tr>
      <td>Einliefern, akzeptieren und validieren von <strong>eForms-DE 1.0.0</strong>
      </td>
      <td>Mediator</td>
      <td>
        <p>
          ✅
        </p>
        <p>Ja</p>
      </td>
      <td>
        <p>
          ✅
        </p>
        <p>Ja</p>
      </td>
      <td>
        <br/>
      </td>
    </tr>
    <tr>
      <td>Einliefern, akzeptieren und validieren von <strong>eForms-DE 1.0.1 </strong>
      </td>
      <td>Mediator</td>
      <td>
        <p>
          ✅
        </p>
        <p>Ja</p>
      </td>
      <td>
        <p>
          ✅
        </p>
        <p>Ja</p>
      </td>
      <td>Derzeit kann Version eForms-DE 1.0.1 testweise im Mediator eingeliefert werden, diese kann aber (noch) nicht vom eSender in eForms-EU 1.5 verarbeitet werden, da das Codetable mapping noch nicht final ist</td>
    </tr>
    <tr>
      <td>Weiterleiten und annehmen von <strong>nationalen</strong> eForms in Version eForms-EU 0.1.1 und 1.0 im <strong>BKMS</strong>
      </td>
      <td>Mediator, BKMS</td>
      <td>
        <p>
          ✅
        </p>
        <p>Ja </p>
      </td>
      <td>
        <p>✅</p>
        <p>vorraussichtlich ja</p>
      </td>
      <td>Ab Produktion sollte ein neuerer, deutscher Standard verwendet werden, vorzugsweise eForms-DE 1.0.0 oder aktueller. Alte Standards können ggf. noch für eine Übergangszeit unterstützt werden</td>
    </tr>
    <tr>
      <td>Weiterleiten und annehmen von <strong>nationalen</strong> eForms in Version eForms-EU 1.5 an <strong>BKMS</strong>
      </td>
      <td>Mediator, BKMS</td>
      <td>
        <p>
          ❌ 
        </p>
        <p>Nein </p>
      </td>
      <td>
        <p>
          ❌ 
        </p>
        <p>Nein</p>
      </td>
      <td>Die Bekanntmachung wird zwar an den BKMS weitergeleitet, aber vom BKMS abgelehnt, da eForms-EU 1.5 nicht unterstützt wird</td>
    </tr>
    <tr>
      <td>Weiterleiten und annehmen von <strong>nationalen</strong> eForms in Version eForms-DE 1.0.0 im <strong>BKMS</strong>
      </td>
      <td>Mediator, BKMS</td>
      <td>
        <p>
          ❌ 
        </p>
        <p>Nein</p>
      </td>
      <td>
        <p>✅</p>
        <p>vorraussichtlich ja</p>
      </td>
      <td>
        <br/>
      </td>
    </tr>
    <tr>
      <td>Weiterleiten und annehmen von <strong>nationalen</strong> eForms in Version eForms-DE 1.0.1 im <strong>BKMS</strong>
      </td>
      <td>Mediator, BKMS</td>
      <td>
        <p>
          ❌ 
        </p>
        <p>Nein</p>
      </td>
      <td>
        <p>✅</p>
        <p>vorraussichtlich ja</p>
      </td>
      <td>
        <br/>
      </td>
    </tr>
    <tr>
      <td>Weiterleiten von <strong>eu-weiten</strong> eForms in Version eForms-EU 0.1.1 und 1.0 an <strong>eSender</strong>
      </td>
      <td>Mediator, eSender</td>
      <td>
        <p>
          ❌ 
        </p>
        <p>Nein</p>
      </td>
      <td>
        <p>
          ❌ 
        </p>
        <p>Nein</p>
      </td>
      <td>Ab Produktion sollte ein neuerer, deutscher Standard verwendet werden, vorzugsweise eForms-DE 1.0.0 oder aktueller. Bekanntmachungen mit älteren Versionen werden nicht vom eSender verarbeitet</td>
    </tr>
    <tr>
      <td>Weiterleiten von <strong>eu-weiten</strong> eForms in Version eForms-EU 1.5 an <strong>eSender</strong>
      </td>
      <td>Mediator, eSender</td>
      <td>
        <p>
          ✅
        </p>
        <p>Ja</p>
      </td>
      <td>
        <p>✅</p>
        <p>vorraussichtlich ja</p>
      </td>
      <td>Ab Produktion sollte ein neuerer, deutscher Standard verwendet werden, vorzugsweise eForms-DE 1.0.0 oder aktueller. Alte Standards können ggf. noch für eine Übergangszeit unterstützt werden</td>
    </tr>
    <tr>
      <td>Weiterleiten von <strong>eu-weiten</strong> eForms in Version eForms-DE 1.0.0 an <strong>eSender </strong>und anschließende Transformation</td>
      <td>Mediator, eSender</td>
      <td>
        <p>
          ✅
        </p>
        <p>Ja</p>
      </td>
      <td>
        <p>
          ✅
        </p>
        <p>Ja</p>
      </td>
      <td>
        <br/>
      </td>
    </tr>
    <tr>
      <td>Weiterleiten von <strong>eu-weiten</strong> eForms in Version eForms-DE 1.0.1 an <strong>eSender </strong>und anschließende Transformation</td>
      <td>Mediator, eSender</td>
      <td>
        <p>
          ❌ 
        </p>
        <p>Nein</p>
      </td>
      <td>
        <p>
          ✅
        </p>
        <p>Ja</p>
      </td>
      <td>
        <br/>
      </td>
    </tr>
    <tr>
      <td>Weiterleiten und Prozessieren von über die Preview-Umgebung eingelieferten, eu-weite eForms an <strong>TED Preview</strong>
      </td>
      <td>eSender, TED</td>
      <td>
        <p>
          ✅
        </p>
        <p>Ja</p>
      </td>
      <td>
        <p>
          ✅
        </p>
        <p>Ja</p>
      </td>
      <td>
        <br/>
      </td>
    </tr>
    <tr>
      <td>Weiterleiten und Prozessieren von über die Production-Umgebung eingelieferten, eu-weite eForms an <strong>TED Production</strong>
      </td>
      <td>eSender, TED</td>
      <td>
        <p>
          ❌ 
        </p>
        <p>Nein</p>
      </td>
      <td>
        <p>
          ✅
        </p>
        <p>Ja</p>
      </td>
      <td>
        <br/>
      </td>
    </tr>
    <tr>
      <td>Abfragen des TED <strong>validation Reports</strong> und Extrahieren von Fehlern und Warnungen</td>
      <td>eSender, TED</td>
      <td>
        <p>
          ✅
        </p>
        <p>Ja</p>
      </td>
      <td>
        <p>
          ✅
        </p>
        <p>Ja</p>
      </td>
      <td>
        <br/>
      </td>
    </tr>
    <tr>
      <td>Weiterleiten und Annehmen von <strong>eu-weiten</strong> eForms in Version eForms-EU 1.5 im <strong>BKMS</strong>
      </td>
      <td>eSender, BKMS</td>
      <td>
        <p>
          ❌ 
        </p>
        <p>Nein</p>
      </td>
      <td>
        <p>
          ❌ 
        </p>
        <p>Nein</p>
      </td>
      <td>Die Bekanntmachung wird zwar an den BKMS weitergeleitet, aber vom BKMS abgelehnt, da eForms-EU 1.5 nicht unterstützt wird</td>
    </tr>
    <tr>
      <td>Weiterleiten und Annehmen von <strong>eu-weiten</strong> eForms in Version eForms-DE 1.0.0 im <strong>BKMS</strong>
      </td>
      <td>eSender, BKMS</td>
      <td>
        <p>
          ❌ 
        </p>
        <p>Nein</p>
      </td>
      <td>
        <p>✅</p>
        <p>vorraussichtlich ja</p>
      </td>
      <td>
        <br/>
      </td>
    </tr>
    <tr>
      <td>Weiterleiten und Annehmen von <strong>eu-weiten</strong> eForms in Version eForms-DE 1.0.0 im <strong>BKMS</strong>
      </td>
      <td>eSender, BKMS</td>
      <td>
        <p>
          ❌ 
        </p>
        <p>Nein</p>
      </td>
      <td>
        <p>✅</p>
        <p>vorraussichtlich ja</p>
      </td>
      <td>
        <br/>
      </td>
    </tr>
    <tr>
      <td>
        <strong>Stoppen </strong>eines in TED nicht veröffentlichten eForms in <strong>TED</strong>
      </td>
      <td>Mediator, eSender, TED</td>
      <td>
        <p>
          ✅
        </p>
        <p>Ja</p>
      </td>
      <td>
        <p>
          ✅
        </p>
        <p>Ja</p>
      </td>
      <td>
        <br/>
      </td>
    </tr>
    <tr>
      <td>
        <strong>Stoppen </strong>eines in TED nicht veröffentlichten eForms in <strong>BKMS</strong>
      </td>
      <td>Mediator, eSender, BKMS</td>
      <td>
        <p>
          ❌ 
        </p>
        <p>Nein</p>
      </td>
      <td>
        <p>❌ </p>
        <p>vorraussichtlich Nein</p>
      </td>
      <td>
        <br/>
      </td>
    </tr>
    <tr>
      <td>Zur Verfügung stellen von <strong>Statusinformationen</strong>
      </td>
      <td>Mediator, eSender</td>
      <td>
        <p>✅</p>
        <p>Ja (teilweise)</p>
      </td>
      <td>
        <p>
          ✅
        </p>
        <p>Ja</p>
      </td>
      <td>Einige Statuskombinationen können aufgrund anderer noch nicht verfügbarer Features (z.B. Keine Unterstützung von eForms-DE 1.0.0 durch BKMS) im Preview Release nicht getestet werden.</td>
    </tr>
    <tr>
      <td>Zur Verfügung stellen von beim Prozessieren des eForms aufgetretenen <strong>relevanten Fehlern und Warnungen</strong>
      </td>
      <td>Mediator, eSender</td>
      <td>
        <p>✅</p>
        <p>Ja (teilweise)</p>
      </td>
      <td>
        <p>
          ✅
        </p>
        <p>Ja</p>
      </td>
      <td>Derzeit werden noch nicht alle Fehler und Warnungen weitergegeben</td>
    </tr>
  </tbody>
</table>
</details>

