### EfA-Umsetzungsprojekt "Zugang zur öffentlichen Vergabe"
## Dokumentation Vermittlungsdienst
[Startseite](/documentation/documentation.md)
<br><br>

# Verfügbare Systemumgebungen
Aktuell steht eine **Test-, Referenz- und eine Produktionsumgebung** des Vermittlungsdiensts zur Verfügung. Jedes System sendet innerhalb der Umgebung die Daten an
das entsprechende Bekanntmachungsservice-System. Mit Anbindung des eSenders, der für die Übermittlung der Bekanntmachungen an TED zuständig ist, ist jedes Vermittlungsdienst-System in der Lage, Bekanntmachungen auch an das entsprechende TED-System zu übermitteln.
<br><br>

**Hinweis:** Mit dem eSender Preview Release am 31.3.2023 wird der eSender für die Preview-Umgebung angebunden und testbar sein.
<br><br>

<table class="wrapped">
  <colgroup>
    <col/>
    <col/>
    <col/>
    <col/>
  </colgroup>
  <thead>
    <tr>
      <th style="text-align: left;">
        <br/>
      </th>
      <th style="text-align: left;">
        <p>Preview Umgebung (inkl. eSender preview)</p>
      </th>
      <th style="text-align: left;">
        <p>Staging Umgebung </p>
      </th>
      <th style="text-align: left;">
        <p>Production Umgebung </p>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align: left;">URL</td>
      <td style="text-align: left;">
        <a class="external-link" href="https://bkms-mediator-app-preview.efa-fhb.apps-int.nortal.com/" rel="nofollow">https://bkms-mediator-app-preview.efa-fhb.apps-int.nortal.com</a>
      </td>
      <td style="text-align: left;">
        <a class="external-link" href="https://evergabe-staging.hb-interim.gisa.de/" rel="nofollow">https://evergabe-staging.hb-interim.gisa.de</a>
      </td>
      <td style="text-align: left;">
        <a class="external-link" href="https://ozg-vermittlungsdienst.de/" rel="nofollow">https://ozg-vermittlungsd</a>
        <a class="external-link" href="https://ozg-vermittlungsdienst.de/" rel="nofollow">ienst.de/</a>
      </td>
    </tr>
    <tr>
      <td style="text-align: left;">IP Address(es)</td>
      <td style="text-align: left;">20.50.223.245</td>
      <td style="text-align: left;">185.158.224.40</td>
      <td style="text-align: left;">185.158.224.47 + 185.158.224.58</td>
    </tr>
    <tr>
      <td style="text-align: left;">eForms Validator</td>
      <td style="text-align: left;">
        <a href="https://validator.ozg-vermittlungsdienst.de/q/swagger-ui/">https://validator.ozg-vermittlungsdienst.de/q/swagger-ui/</a>
      </td>
      <td style="text-align: left;">
        <a href="https://validator.ozg-vermittlungsdienst.de/q/swagger-ui/">https://validator.ozg-vermittlungsdienst.de/q/swagger-ui/</a>
      </td>
      <td style="text-align: left;">
        <a href="https://validator.ozg-vermittlungsdienst.de/q/swagger-ui/">https://validator.ozg-vermittlungsdienst.de/q/swagger-ui/</a>
      </td>
    </tr>
    <tr>
      <td style="text-align: left;">BKMS</td>
      <td style="text-align: left;">
        <a href="https://alpha.oeffentlichevergabe.de/" rel="nofollow">https://alpha.oeffentlichevergabe.de/</a>
      </td>
      <td style="text-align: left;">
        <a class="external-link" href="https://alpha.oeffentlichevergabe.de/" rel="nofollow">https://alpha.oeffentlichevergabe.de/</a>
      </td>
      <td style="text-align: left;">
        <a class="external-link" href="https://www.oeffentlichevergabe.de/" rel="nofollow">https://www.oeffentlichevergabe.de/</a>
      </td>
    </tr>
    <tr>
      <td style="text-align: left;">
        <p>Keycloak</p>
      </td>
      <td style="text-align: left;">
        <a href="https://keycloak-preview.efa-fhb.apps-int.nortal.com/realms/ozg-vermittlungsdienst/account/#/" rel="nofollow">https://keycloak-preview.efa-fhb.apps-int.nortal.com/realms/ozg-vermittlungsdienst/account/#/</a>
        <span style="color: rgb(23,43,77);">
          <span> </span>
        </span>
      </td>
      <td style="text-align: left;">
        <a href="https://auth-evergabe-staging.hb-interim.gisa.de/" rel="nofollow" style="text-decoration: inherit;text-align: left;">https://auth-evergabe-staging.hb-interim.gisa.de/</a>
      </td>
      <td style="text-align: left;">
        <p>-</p>
      </td>
    </tr>
    <tr>
      <td style="text-align: left;">
        <p>TED</p>
        <p>
          <br/>
        </p>
      </td>
      <td style="text-align: left;">
        <a class="external-link" href="https://enotices2.preview.ted.europa.eu/esenders/webjars/swagger-ui/index.html#/" rel="nofollow">https://enotices2.preview.ted.europa.eu/</a>
        <br/>(Wird verwendet in eSender Preview Release am 31.3.2023)</td>
      <td style="text-align: left;">
        <p>
          <a class="external-link" href="https://enotices2.preview.ted.europa.eu/esenders/webjars/swagger-ui/index.html#/" rel="nofollow">https://enotices2.preview.ted.europa.eu/</a>
        </p>
        <p>(Nicht im eSender Preview Release am 31.3.2023 enthalten)</p>
      </td>
      <td style="text-align: left;">
        <p>
          <a class="external-link" href="https://enotices2.preview.ted.europa.eu/esenders/webjars/swagger-ui/index.html#/" rel="nofollow">https://enotices2.ted.europa.eu/</a>
        </p>
        <p>(Nicht im eSender Preview Release am 31.3.2023 enthalten)</p>
      </td>
    </tr>
  </tbody>
</table>