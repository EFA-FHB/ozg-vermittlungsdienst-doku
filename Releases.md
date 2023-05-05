### EfA-Umsetzungsprojekt "Zugang zur öffentlichen Vergabe"**
# Releases Vermittlungsdienst
[Übersicht](/Readme.md)
<br><br>

## Preview Release Mai (Release Datum 04.05.2023)
Status: veröffentlicht<br>
System: Preview (https://bkms-mediator-app-preview.efa-fhb.apps-int.nortal.com)
<details>
<summary>Release notes</summary>

### Vermittlungsdienst
- Erweiterung der API Autorisierung um Refresh Token (Details unter [Anbindung an den Vermittlungsdienst](/documentation/Connection_to_mediator.md))
- Erweiterung der Statusinformationen um Warnungen und Fehlermeldungen (Details unter [Status- und Transferinformationen](/documentation/Status_information.md))
- Erweiterung der Fehlermeldungen
- Versionsprüfung einer unterschwelligen Bekanntmachung im Bekanntmachungsservice
- Statusabfrage (veröffentlicht) einer unterschwelligen Bekanntmachung im Bekanntmachungsservice 
- Erweiterung des Validierungs-Reports um die assert id
- Optimierungen und Fehlerbehebungen

### Validator
- Erweiterung des Ergebnis-Reports um `rule` und `ruleContent` 
- Optimierungen und Fehlerbehebungen
</details>
<br><br>

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

