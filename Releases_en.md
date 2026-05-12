# Releases

<a id=juengste-release-updates></a>
### Latest Release Updates
Status: 12.05.2026

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
      <th rowspan="2">Application / Services</th>
      <th rowspan="2">Latest Update<br>[Release ID]</th>
      <th colspan="3">Environment</th>
      <th rowspan="2", class="notes", style="min-width:300px;text-align:left;">Release Notes</th>
    </tr>
    <tr>
      <th style="color:#00488b;">Preview<br>Deployment</th>
      <th style="color:#DAA520;">Staging<br>Deployment</th>
      <th style="color:#07702D;">Production<br>Deployment</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><a href="https://self-service.datenservice-oeffentlicher-einkauf.de/" rel="nofollow">Self-Service-Portal</a></td>
      <td data-field="release-id">26-4</td>
      <td style="color:#00488b;">31.03.2026</td>
      <td style="color:#DAA520;">14.04.2026</td>
      <td style="color:#07702D;">19.05.2026 (planned)</td>
      <td>The SSP was restructured and the majority of the documentation is now accessible only after logging in.</td>
    </tr>
    <tr>
      <td><a class="external-link" href="https://ozg-vermittlungsdienst.de" rel="nofollow">Vermittlungsdienst</a></td>
      <td data-field="release-id">26-4</td>
      <td style="color:#00488b;">31.03.2026</td>
      <td style="color:#DAA520;">14.04.2026</td>
      <td style="color:#07702D;">19.05.2026 (planned)</td>
      <td>A new status for forwarding to the Federal Statistical Office has been introduced. <br>
The "tedPublishedTimestamp" field has been renamed to "tedPublishedDate" in GET and POST responses, as TED only provides a date.</td>
    </tr>
    <tr>
      <td>eSender-Hub</td>
      <td data-field="release-id">26-4</td>
      <td style="color:#00488b;">30.03.2026</td>
      <td style="color:#DAA520;">14.04.2026</td>
      <td style="color:#07702D;">19.05.2026 (planned)</td>
      <td>Various bug fixes have been implemented.</td>
    </tr>
    <tr>
      <td><a href="https://viewer.ozg-vermittlungsdienst.de">Notice-Viewer</a></td>
      <td data-field="release-id">26-2</td>
      <td style="color:#00488b;">26.02.2026</td>
      <td style="color:#DAA520;">10.03.2026</td>
      <td style="color:#07702D;">19.03.2026</td>
      <td>The generation of the notice now depends on the ProfileID.</td>
    </tr>
    <tr>
      <td><a href="https://validator.ozg-vermittlungsdienst.de">Online-Validator / <br> Offline-Validator</a></td>
      <td data-field="release-id">26-2</td>
      <td style="color:#00488b;">26.02.2026</td>
      <td style="color:#DAA520;">10.03.2026</td>
      <td style="color:#07702D;">19.03.2026</td>
      <td>- The validation of the notice is now dependent on the ProfileID.<br>- A new optional parameter has been added for the ProfileID.<br>- Obsolete versions of eForms have been removed from the list of supported versions.</td>
    </tr>
    <tr>
      <td><a href="https://info.datenservice-oeffentlicher-einkauf.de/">Info-Seite</td>
      <td>26-4</td>
      <td style="color:#00488b;">31.03.2026</td>
      <td style="color:#DAA520;">14.04.2026</td>
      <td style="color:#07702D;">19.05.2026 (planned)</td>
      <td>A new information page for the publicly available DÖE documentation can now be found on the info-page.</td>
    </tr>
    <tr class="divider">
      <td><a class="external-link" href="https://gitlab.opencode.de/OC000008125155/SDK-eforms-de" rel="nofollow">SDK zu eForms-DE</td>
      <td data-field="release-id">SDK-DE 1.14.2</td>
      <td style="color:#00488b;">26.02.2026</td>
      <td style="color:#DAA520;">10.03.2026</td>
      <td style="color:#07702D;">19.03.2026</td>
      <td>see https://gitlab.opencode.de/OC000008125155/SDK-eforms-de</td>
    </tr>
    <tr>
      <td><a class="external-link" href="https://www.oeffentlichevergabe.de" rel="nofollow">Bekanntmachungsservice</a></td>
      <td data-field="release-id">26-4</td>
      <td style="color:#00488b;"></td>
      <td style="color:#DAA520;">14.04.2026</td>
      <td style="color:#07702D;">19.05.2026 (planned)</td>
      <td>Additional technical details for submission to the Federal Statistical Office have been added to the details page of the notice.</td>
    </tr>
  </tbody>
</table>

<br>

<a id=historie-der-releases></a>
### Details of the latest releases

<table>
  <thead>
    <tr>
      <th rowspan="2">Application / Services</th>
      <th rowspan="2">History<br>[Release ID]</th>
      <th colspan="3">Environment</th>
      <th rowspan="2", class="notes", style="min-width:300px;text-align:left;">Release Notes</th>
    </tr>
    <tr>
      <th style="color:#00488b;">Preview<br>Deployment</th>
      <th style="color:#DAA520;">Staging<br>Deployment</th>
      <th style="color:#07702D;">Production<br>Deployment</th>
    </tr>
  </thead>
  <tbody>
    <tr data-name="SSP release -1">
      <td rowspan="3"><a href="https://self-service.datenservice-oeffentlicher-einkauf.de/" rel="nofollow">Self-Service-Portal</a></td>
      <td></td>
      <td style="color:#00488b;">27.03.2025</td>
      <td style="color:#DAA520;">25.04.2025</td>
      <td style="color:#07702D;">28.04.2025</td>
      <td>- Critical vulnerabilities have been fixed<br>
- Various bugs have been fixed</td>
    </tr>
    <tr data-name="SSP release -2">
      <td></td>
      <td style="color:#00488b;">11.12.2025</td>
      <td style="color:#DAA520;">11.12.2025</td>
      <td style="color:#07702D;">12.12.2025</td>
      <td>A health check bug which displayed the BKMS as being offline has been corrected.</td>
    </tr>
    <tr data-name="SSP release -3">
      <td></td>
      <td style="color:#00488b;">14.05.24</td>
      <td style="color:#DAA520;">22.05.24</td>
      <td style="color:#07702D;">28.05.24</td>
      <td>- New internal roles have been introduced to enable the tracking and verification of notice statuses, as well as user management<br>
- If a notice is rejected manually (MANUALLY_REJECTED), both the SSP admin's contact person and the 'authorEmail' address will be automatically notified by email with the reason for the rejection<br>
- Update to the accessibility statement<br>
- Various bugs have been fixed</td>
    </tr>
    <tr data-name="Vermittlungsdienst release -1">
      <td rowspan="3"><a class="external-link" href="https://ozg-vermittlungsdienst.de" rel="nofollow">Vermittlungsdienst</a></td>
      <td data-field="release-id">26-2</td>
      <td style="color:#00488b;">26.02.2026</td>
      <td style="color:#DAA520;">10.03.2026</td>
      <td style="color:#07702D;">19.03.2026</td>
      <td>The ability to accept and process notices with different ProfileIDs has been implemented.</td>
    </tr>
    <tr data-name="Vermittlungsdienst release -2">
      <td data-field="release-id">26-1</td>
      <td style="color:#00488b;">21.01.2026</td>
      <td style="color:#DAA520;">29.01.2026</td>
      <td style="color:#07702D;">05.02.2026</td>
      <td>Support for T01/02 forms has been implemented for SDK 1.14.</td>
    </tr>
    <tr data-name="Vermittlungsdienst release -3">
      <td></td>
      <td style="color:#00488b;">14.08.2025</td>
      <td style="color:#DAA520;">21.08.2025</td>
      <td style="color:#07702D;">28.08.2025</td>
      <td>The E1 form is now submitted to TED by default and published there.<br>
It is now also possible to publish the E2, E3 and E4 forms on TED on an optional basis.</td>
    </tr>
    <tr data-name="eSender release -1">
      <td rowspan="3">eSender-Hub</td>
      <td>26-2</td>
      <td style="color:#00488b;">26.02.2026</td>
      <td style="color:#DAA520;">10.03.2026</td>
      <td style="color:#07702D;">19.03.2026</td>
      <td>The transformation of the notice now depends on the ProfileID.</td>
    </tr>
    <tr data-name="eSender release -2">
      <td>26-1</td>
      <td style="color:#00488b;">21.01.2026</td>
      <td style="color:#DAA520;">29.01.2026</td>
      <td style="color:#07702D;">05.02.2026</td>
      <td>Support for T01/02 forms has been implemented for SDK 1.14.</td>
    </tr>
    <tr data-name="eSender release -3">
      <td></td>
      <td style="color:#00488b;">14.08.2025</td>
      <td style="color:#DAA520;">21.08.2025</td>
      <td style="color:#07702D;">28.08.2025</td>
      <td>The processing of E-forms has been implemented.</td>
    </tr>
    <tr data-name="Viewer release -1">
      <td rowspan="3"><a href="https://viewer.ozg-vermittlungsdienst.de">Notice-Viewer</a></td>
      <td>26-1</td>
      <td style="color:#00488b;">21.01.2026</td>
      <td style="color:#DAA520;">29.01.2026</td>
      <td style="color:#07702D;">05.02.2026</td>
      <td>Generation of T01/02 forms using SDK 1.14 has been implemented.<br>
SwaggerUI text updates.</td>
    </tr>
    <tr data-name="Viewer release -2">
      <td></td>
      <td style="color:#00488b;">14.08.2025</td>
      <td style="color:#DAA520;">21.08.2025</td>
      <td style="color:#07702D;">28.08.2025</td>
      <td>The SDK-DE Patch 1.13.2 has been integrated.<br>
Various bug fixes have been implemented.</td>
    </tr>
    <tr data-name="Viewer release -3">
      <td></td>
      <td style="color:#00488b;">07.07.2025</td>
      <td style="color:#DAA520;">14.07.2025</td>
      <td style="color:#07702D;">24.07.2025</td>
      <td>- Various bugs in HTML generation have been fixed.<br>
- The number format for total amounts has been corrected in the PDF generation.</td>
    </tr>
    <tr data-name="Validator release -1">
      <td rowspan="3"><a href="https://validator.ozg-vermittlungsdienst.de">Online-Validator / <br> Offline-Validator</a></td>
      <td></td>
      <td style="color:#00488b;">14.08.2025</td>
      <td style="color:#DAA520;">21.08.2025</td>
      <td style="color:#07702D;">28.08.2025</td>
      <td>The following SDK-DE patches have been applied:<br>
- SDK-DE 1.12.6<br>
- SDK-DE 1.13.2<br></td>
    </tr>
    <tr data-name="Validator release -2">
      <td></td>
      <td style="color:#00488b;">16.05.2025</td>
      <td style="color:#DAA520;">16.05.2025</td>
      <td style="color:#07702D;">19.05.2025</td>
      <td>The patches for SDK-DE 1.12.5 and SDK-DE 1.13.1 were implemented.</td>
    </tr>
    <tr data-name="Validator release -3">
      <td></td>
      <td style="color:#00488b;">27.03.2025</td>
      <td style="color:#DAA520;">25.04.2025</td>
      <td style="color:#07702D;">28.04.2025</td>
      <td>- Support for eForms-DE 2.1 was introduced.<br>
- SDK-DE 1.13.0 was introduced.</td>
    </tr>
    <tr>
      <td><a href="https://info.datenservice-oeffentlicher-einkauf.de/">Info-Seite</td>
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
      <td>see https://gitlab.opencode.de/OC000008125155/SDK-eforms-de</td>
    </tr>
    <tr data-name="BKMS release -1">
      <td rowspan="3"><a class="external-link" href="https://www.oeffentlichevergabe.de" rel="nofollow">Bekanntmachungsservice</a></td>
      <td>26-3</td>
      <td style="color:#00488b;"></td>
      <td style="color:#DAA520;">23.03.2026</td>
      <td style="color:#07702D;">29.04.2026</td>
      <td>Redesign of detail page for contract and results notices.</td>
    </tr>
    <tr data-name="BKMS release -2">
      <td>26-2</td>
      <td style="color:#00488b;"></td>
      <td style="color:#DAA520;">10.03.2026</td>
      <td style="color:#07702D;">19.03.2026</td>
      <td>Support for ProfileID has been implemented. The notice is now displayed depending on the ProfileID (SDK version).</td>
    </tr>
    <tr data-name="BKMS release -3">
      <td>26-1</td>
      <td style="color:#00488b;"></td>
      <td style="color:#DAA520;">29.01.2026</td>
      <td style="color:#07702D;">05.02.2026</td>
      <td>Support for T01/02 forms in SDK 1.14 has been implemented.</td>
    </tr>
  </tbody>
</table>
