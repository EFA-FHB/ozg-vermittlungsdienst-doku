### EfA-Umsetzungsprojekt "Zugang zur öffentlichen Vergabe"
## Dokumentation Vermittlungsdienst
[Inhaltsverzeichnis](/documentation/documentation.md)
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
        <a class="external-link" href="https://preview.ozg-vermittlungsdienst.de" rel="nofollow">https://preview.ozg-vermittlungsdienst.de</a>
      </td>
      <td style="text-align: left;">
        <a class="external-link" href="https://staging.ozg-vermittlungsdienst.de" rel="nofollow">https://staging.ozg-vermittlungsdienst.de</a>
      </td>
      <td style="text-align: left;">
        <a class="external-link" href="https://ozg-vermittlungsdienst.de" rel="nofollow">https://ozg-vermittlungsdienst.de</a>
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
        <a href="https://preview-validator.ozg-vermittlungsdienst.de">https://preview-validator.ozg-vermittlungsdienst.de</a>
      </td>
      <td style="text-align: left;">
        <a href="https://staging-validator.ozg-vermittlungsdienst.de">https://staging-validator.ozg-vermittlungsdienst.de</a>
      </td>
      <td style="text-align: left;">
        <a href="https://validator.ozg-vermittlungsdienst.de">https://validator.ozg-vermittlungsdienst.de</a>
      </td>
    </tr>
    <tr>
      <td style="text-align: left;">BKMS</td>
      <td style="text-align: left;">
        <a href="https://alpha.oeffentlichevergabe.de" rel="nofollow">https://alpha.oeffentlichevergabe.de</a>
      </td>
      <td style="text-align: left;">
        <a class="external-link" href="https://alpha.oeffentlichevergabe.de" rel="nofollow">https://alpha.oeffentlichevergabe.de</a>
      </td>
      <td style="text-align: left;">
        <a class="external-link" href="https://www.oeffentlichevergabe.de" rel="nofollow">https://www.oeffentlichevergabe.de</a>
      </td>
    </tr>
    <tr>
      <td style="text-align: left;">
        <p>Keycloak</p>
      </td>
      <td style="text-align: left;">
        <a href="https://preview-auth.ozg-vermittlungsdienst.de" rel="nofollow">https://preview-auth.ozg-vermittlungsdienst.de</a>
        <span style="color: rgb(23,43,77);">
          <span> </span>
        </span>
      </td>
      <td style="text-align: left;">
        <a href="https://staging-auth.ozg-vermittlungsdienst.de" rel="nofollow" style="text-decoration: inherit;text-align: left;">https://staging-auth.ozg-vermittlungsdienst.de</a>
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
        <a class="external-link" href="https://enotices2.preview.ted.europa.eu/esenders/webjars/swagger-ui/index.html#/" rel="nofollow">https://enotices2.preview.ted.europa.eu</a>
        <br/>(Wird verwendet in eSender Preview Release am 31.3.2023)</td>
      <td style="text-align: left;">
        <p>
          <a class="external-link" href="https://enotices2.preview.ted.europa.eu/esenders/webjars/swagger-ui/index.html#/" rel="nofollow">https://enotices2.preview.ted.europa.eu</a>
        </p>
        <p>(Nicht im eSender Preview Release am 31.3.2023 enthalten)</p>
      </td>
      <td style="text-align: left;">
        <p>
          <a class="external-link" href="https://enotices2.preview.ted.europa.eu/esenders/webjars/swagger-ui/index.html#/" rel="nofollow">https://enotices2.ted.europa.eu</a>
        </p>
        <p>(Nicht im eSender Preview Release am 31.3.2023 enthalten)</p>
      </td>
    </tr>
  </tbody>
</table>