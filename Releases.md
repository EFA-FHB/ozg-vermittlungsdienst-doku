# Releases

<a id=juengste-release-updates></a>
### Jüngste-Release-Updates
Stand: 06.05.2026

<style>
table {
  border-collapse: collapse;
  border: 1px solid #000;
  line-height: 1.1;
  width: 100%;
}

th, td {
  padding: 1;
  margin: 0;
  vertical-align: middle;
  word-wrap: break-word;
  line-height: 1.2;
  border-left: 1px solid #000;
  border-right: 1px solid #000; 
}

th {
  text-align: center;
}

tr.divider td {
  border-top: 1.5px solid #000;
}

</style>

<table>
  <thead>
    <tr>
      <th rowspan="2">Anwendung / Services</th>
      <th rowspan="2">jüngstes Update<br>[Release ID]</th>
      <th colspan="3">Umgebung</th>
      <th rowspan="2", class="notes", style="min-width:300px;text-align:left;">Release Notes</th>
    </tr>
    <tr>
      <th style="color:#00488b;">Preview<br>Inbetriebnahme</th>
      <th style="color:#DAA520;">Staging<br>Inbetriebnahme</th>
      <th style="color:#07702D;">Produktion<br>Inbetriebnahme</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><a href="https://self-service.datenservice-oeffentlicher-einkauf.de/" rel="nofollow">Self-Service-Portal</a></td>
      <td data-field="release-id">26-4</td>
      <td style="color:#00488b;">31.03.2026</td>
      <td style="color:#DAA520;">14.04.2026</td>
      <td style="color:#07702D;">19.05.2026 (geplant)</td>
      <td>Das SSP wurde umgebaut und die Dokumentation befindet sich hauptsächlich nur hinter der Anmeldung.</td>
    </tr>
    <tr>
      <td><a class="external-link" href="https://ozg-vermittlungsdienst.de" rel="nofollow">Vermittlungsdienst</a></td>
      <td data-field="release-id">26-4</td>
      <td style="color:#00488b;">31.03.2026</td>
      <td style="color:#DAA520;">14.04.2026</td>
      <td style="color:#07702D;">19.05.2026 (geplant)</td>
      <td>Ein neuer Status zur Weiterleitung an das Statistische Bundesamt wurde eingeführt. <br>
Das Feld 'tedPublishedTimestamp' wurde in GET- und POST-Responses in 'tedPublishedDate umbenannt', da TED nur ein Datum liefert.</td>
    </tr>
    <tr>
      <td>eSender-Hub</td>
      <td data-field="release-id">26-4</td>
      <td style="color:#00488b;">30.03.2026</td>
      <td style="color:#DAA520;">14.04.2026</td>
      <td style="color:#07702D;">19.05.2026 (geplant)</td>
      <td>Diverse Fehlerbehebungen wurden vorgenommen.</td>
    </tr>
    <tr>
      <td><a href="https://viewer.ozg-vermittlungsdienst.de">Notice-Viewer</a></td>
      <td data-field="release-id">26-2</td>
      <td style="color:#00488b;">26.02.2026</td>
      <td style="color:#DAA520;">10.03.2026</td>
      <td style="color:#07702D;">19.03.2026</td>
      <td>Die Generierung der Bekanntmachung erfolgt nun abhängig von der ProfileID.</td>
    </tr>
    <tr>
      <td><a href="https://validator.ozg-vermittlungsdienst.de">Online-Validator / <br> Offline-Validator</a></td>
      <td data-field="release-id">26-2</td>
      <td style="color:#00488b;">26.02.2026</td>
      <td style="color:#DAA520;">10.03.2026</td>
      <td style="color:#07702D;">19.03.2026</td>
      <td>- Die Validierung der Bekanntmachung erfolgt nun abhängig von der ProfileID<br>- Es wurde ein neuer optionaler Parameter für die ProfileID hinzugefügt<br>- Obsolete eForms-Versionen wurden aus der Liste der unterstützten Versionen entfernt</td>
    </tr>
    <tr>
      <td><i><a href="https://info.datenservice-oeffentlicher-einkauf.de/">Info-Seite</i></td>
      <td>26-4</td>
      <td style="color:#00488b;">31.03.2026</td>
      <td style="color:#DAA520;">14.04.2026</td>
      <td style="color:#07702D;">19.05.2026 (geplant)</td>
      <td>Eine neue Info-Seite für die öffentlich verfügbare Dokumentation befindet sich jetzt auf die Info-Seite.</td>
    </tr>
    <tr class="divider">
      <td><a class="external-link" href="https://gitlab.opencode.de/OC000008125155/SDK-eforms-de" rel="nofollow">SDK zu eForms-DE</td>
      <td data-field="release-id">SDK-DE 1.14.2</td>
      <td style="color:#00488b;">26.02.2026</td>
      <td style="color:#DAA520;">10.03.2026</td>
      <td style="color:#07702D;">19.03.2026</td>
      <td>siehe https://gitlab.opencode.de/OC000008125155/SDK-eforms-de</td>
    </tr>
    <tr>
      <td><a class="external-link" href="https://www.oeffentlichevergabe.de" rel="nofollow">Bekanntmachungsservice</a></td>
      <td data-field="release-id">26-4</td>
      <td style="color:#00488b;"></td>
      <td style="color:#DAA520;">14.04.2026</td>
      <td style="color:#07702D;">19.05.2026 (geplant)</td>
      <td>Ergänzung neuer technischer Details zur Weiterleitung an das Statistische Bundesamt auf der Detailseite der Bekanntmachung.</td>
    </tr>
  </tbody>
</table>

<br>

<a id=historie-der-releases></a>
### Historie der letzten Releases

<table>
  <thead>
    <tr>
      <th rowspan="2">Anwendung / Services</th>
      <th rowspan="2">Historie<br>[Release ID]</th>
      <th colspan="3">Umgebung</th>
      <th rowspan="2", class="notes", style="min-width:300px;text-align:left;">Release Notes</th>
    </tr>
    <tr>
      <th style="color:#00488b;">Preview<br>Inbetriebnahme</th>
      <th style="color:#DAA520;">Staging<br>Inbetriebnahme</th>
      <th style="color:#07702D;">Produktion<br>Inbetriebnahme</th>
    </tr>
  </thead>
  <tbody>
    <tr data-name="SSP release -1">
      <td rowspan="3"><a href="https://self-service.datenservice-oeffentlicher-einkauf.de/" rel="nofollow">Self-Service-Portal</a></td>
      <td></td>
      <td style="color:#00488b;">27.03.2025</td>
      <td style="color:#DAA520;">25.04.2025</td>
      <td style="color:#07702D;">28.04.2025</td>
      <td>- Kritische Schwachstellen wurden behoben<br>
- Diverse Bugs wurden gefixt</td>
    </tr>
    <tr data-name="SSP release -2">
      <td></td>
      <td style="color:#00488b;">11.12.2025</td>
      <td style="color:#DAA520;">11.12.2025</td>
      <td style="color:#07702D;">12.12.2025</td>
      <td>Healthcheckbug, dass der Bekanntmachungsservice offline ist wurde gefixt</td>
    </tr>
    <tr data-name="SSP release -3">
      <td></td>
      <td style="color:#00488b;">14.05.24</td>
      <td style="color:#DAA520;">22.05.24</td>
      <td style="color:#07702D;">28.05.24</td>
      <td>- Es wurden neue interne Rollen eingeführt, um den Status von Lieferungen verfolgen und überprüfen sowie die Benutzerverwaltung durchführen zu können<br>
- Falls eine Bekanntmachung manuell abgelehnt (MANUALLY_REJECTED) wird, es werden automatisch sowohl der SSP-Admins Ansprechpartner als auch 'authorEmail' via Email mit einer Begründung benachrichtigt<br>
- Aktualisierung der Erklärung zur Barrierefreiheit<br>
- Diverse Bugs wurden gefixt</td>
    </tr>
    <tr data-name="Vermittlungsdienst release -1">
      <td rowspan="3"><a class="external-link" href="https://ozg-vermittlungsdienst.de" rel="nofollow">Vermittlungsdienst</a></td>
      <td data-field="release-id">26-2</td>
      <td style="color:#00488b;">26.02.2026</td>
      <td style="color:#DAA520;">10.03.2026</td>
      <td style="color:#07702D;">19.03.2026</td>
      <td>Annahme und Verarbeitung von Bekanntmachungen mit unterschiedlichen ProfileIDs wurde implementiert.</td>
    </tr>
    <tr data-name="Vermittlungsdienst release -2">
      <td data-field="release-id">26-1</td>
      <td style="color:#00488b;">21.01.2026</td>
      <td style="color:#DAA520;">29.01.2026</td>
      <td style="color:#07702D;">05.02.2026</td>
      <td>Annahme und Verarbeitung der T01/02 Formulare im SDK 1.14 wurden implementiert.</td>
    </tr>
    <tr data-name="Vermittlungsdienst release -3">
      <td></td>
      <td style="color:#00488b;">14.08.2025</td>
      <td style="color:#DAA520;">21.08.2025</td>
      <td style="color:#07702D;">28.08.2025</td>
      <td>Das E1-Formular wird nun standardmäßig an TED übermittelt und dort veröffentlicht.<br>
Die optionale Veröffentlichung der Formulare E2, E3 und E4 auf TED ist nun ebenfalls möglich.</td>
    </tr>
    <tr data-name="eSender release -1">
      <td rowspan="3">eSender-Hub</td>
      <td>26-2</td>
      <td style="color:#00488b;">26.02.2026</td>
      <td style="color:#DAA520;">10.03.2026</td>
      <td style="color:#07702D;">19.03.2026</td>
      <td>Die Transformation der Bekanntmachung erfolgt nun abhängig von der ProfileID.</td>
    </tr>
    <tr data-name="eSender release -2">
      <td>26-1</td>
      <td style="color:#00488b;">21.01.2026</td>
      <td style="color:#DAA520;">29.01.2026</td>
      <td style="color:#07702D;">05.02.2026</td>
      <td>Unterstützung der T01/02 Formulare im SDK 1.14 wurde implementiert.</td>
    </tr>
    <tr data-name="eSender release -3">
      <td></td>
      <td style="color:#00488b;">14.08.2025</td>
      <td style="color:#DAA520;">21.08.2025</td>
      <td style="color:#07702D;">28.08.2025</td>
      <td>Die Verarbeitung von E-Formularen wurde implementiert.</td>
    </tr>
    <tr data-name="Viewer release -1">
      <td rowspan="3"><a href="https://viewer.ozg-vermittlungsdienst.de">Notice-Viewer</a></td>
      <td>26-1</td>
      <td style="color:#00488b;">21.01.2026</td>
      <td style="color:#DAA520;">29.01.2026</td>
      <td style="color:#07702D;">05.02.2026</td>
      <td>Generierung der T01/02 Formulare im SDK 1.14 wurde implementiert<br>
SwaggerUI Textanpassungen</td>
    </tr>
    <tr data-name="Viewer release -2">
      <td></td>
      <td style="color:#00488b;">14.08.2025</td>
      <td style="color:#DAA520;">21.08.2025</td>
      <td style="color:#07702D;">28.08.2025</td>
      <td>Der SDK-DE Patch 1.13.2 wurde integriert.<br>
Diverse Fehlerbehebungen wurden vorgenommen.</td>
    </tr>
    <tr data-name="Viewer release -3">
      <td></td>
      <td style="color:#00488b;">07.07.2025</td>
      <td style="color:#DAA520;">14.07.2025</td>
      <td style="color:#07702D;">24.07.2025</td>
      <td>- Es wurden diverse Bugs bei der HTML-Generierung gefixt.<br>
- Es wurde das Zahlenformat für Summenbeträge bei der PDF-Generierung korrigiert.</td>
    </tr>
    <tr data-name="Validator release -1">
      <td rowspan="3"><a href="https://validator.ozg-vermittlungsdienst.de">Online-Validator / <br> Offline-Validator</a></td>
      <td></td>
      <td style="color:#00488b;">14.08.2025</td>
      <td style="color:#DAA520;">21.08.2025</td>
      <td style="color:#07702D;">28.08.2025</td>
      <td>Folgende SDK-DE patchs wurden angewendet:<br>
- SDK-DE 1.12.6<br>
- SDK-DE 1.13.2<br></td>
    </tr>
    <tr data-name="Validator release -2">
      <td></td>
      <td style="color:#00488b;">16.05.2025</td>
      <td style="color:#DAA520;">16.05.2025</td>
      <td style="color:#07702D;">19.05.2025</td>
      <td>Das Patch des SDK-DE 1.12.5 sowie SDK-DE 1.13.1 wurden impelementiert</td>
    </tr>
    <tr data-name="Validator release -3">
      <td></td>
      <td style="color:#00488b;">27.03.2025</td>
      <td style="color:#DAA520;">25.04.2025</td>
      <td style="color:#07702D;">28.04.2025</td>
      <td>- Die Unterstützung von eForms-DE 2.1 wurde implementiert<br>
- SDK-DE 1.13.0 wurde impelementiert</td>
    </tr>
    <tr>
      <td><i><a href="https://info.datenservice-oeffentlicher-einkauf.de/">Info-Seite</i></td>
      <td></td>
      <td style="color:#00488b;"></td>
      <td style="color:#DAA520;"></td>
      <td style="color:#07702D;"></td>
      <td></td>
    </tr>
    <tr class="divider">
      <td><a class="external-link" href="https://gitlab.opencode.de/OC000008125155/SDK-eforms-de" rel="nofollow">SDK zu eForms-DE</td>
      <td>SDK-EU 1.14</td>
      <td style="color:#00488b;">21.01.2026</td>
      <td style="color:#DAA520;">29.01.2026</td>
      <td style="color:#07702D;">05.02.2026</td>
      <td>siehe https://gitlab.opencode.de/OC000008125155/SDK-eforms-de</td>
    </tr>
    <tr data-name="BKMS release -1">
      <td rowspan="3"><a class="external-link" href="https://www.oeffentlichevergabe.de" rel="nofollow">Bekanntmachungsservice</a></td>
      <td>26-3</td>
      <td style="color:#00488b;"></td>
      <td style="color:#DAA520;">23.03.2026</td>
      <td style="color:#07702D;">29.04.2026</td>
      <td>Überarbeitung Detailseite für Auftrags- und Ergebnisbekanntmachungen</td>
    </tr>
    <tr data-name="BKMS release -2">
      <td>26-2</td>
      <td style="color:#00488b;"></td>
      <td style="color:#DAA520;">10.03.2026</td>
      <td style="color:#07702D;">19.03.2026</td>
      <td>Unterstützung der ProfileID wurde implementiert. Die Bekanntmachung wird nun abhängig von der ProfileID (SDK-Version) dargestellt.</td>
    </tr>
    <tr data-name="BKMS release -3">
      <td>26-1</td>
      <td style="color:#00488b;"></td>
      <td style="color:#DAA520;">29.01.2026</td>
      <td style="color:#07702D;">05.02.2026</td>
      <td>Unterstützung der T01/02 Formulare im SDK 1.14 wurde implementiert.</td>
    </tr>
  </tbody>
</table>
