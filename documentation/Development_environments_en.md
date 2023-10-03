### EfA Implementation Project "Access to Public Procurement".
## Documentation Mediation Service
[table of contents](/documentation/documentation.md)
<br>

# Available system environments
Currently, a **test, reference, and a production** environment of the Mediation Service is available. Within the environment, each switching service instance sends the data to the corresponding announcement service. With connectivity to the eSender Hub, the Public Purchasing data service is also able to send notices to the appropriate TED environment.
<br><br>

**Note:** With the Production Release on 06/30/2023, the eSender Hub will be connected and testable in the production environment.
<br>

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
        <p>Preview environment</p>
      </th>
      <th style="text-align: left;">
        <p>Staging environment</p>
      </th>
      <th style="text-align: left;">
        <p>Production environment</p>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align: left;">URL</td>
      <td style="text-align: left;">
        Until 09/15/2023: <a class="external-link" href="https://preview.ozg-vermittlungsdienst.de" rel="nofollow">https://preview.ozg-vermittlungsdienst.de</a> <br>
        from 30.08.2023: <a class="external-link" href="https://preview-ozg-vermittlungsdienst.de" rel="nofollow">https://preview-ozg-vermittlungsdienst.de</a>
      </td>
      <td style="text-align: left;">
        Until 09/15/2023: <a class="external-link" href="https://staging.ozg-vermittlungsdienst.de" rel="nofollow">https://staging.ozg-vermittlungsdienst.de</a> <br>
        from 30.08.2023: <a class="external-link" href="https://staging-ozg-vermittlungsdienst.de" rel="nofollow">https://staging-ozg-vermittlungsdienst.de</a>
      </td>
      <td style="text-align: left;">
        <a class="external-link" href="https://ozg-vermittlungsdienst.de" rel="nofollow">https://ozg-vermittlungsdienst.de</a>
      </td>
    </tr>
    <tr>
      <td style="text-align: left;">IP Address(es)</td>
      <td style="text-align: left;">4.245.108.202</td>
      <td style="text-align: left;">185.158.224.47</td>
      <td style="text-align: left;">185.158.224.47 + 185.158.224.58</td>
    </tr>
    <tr>
      <td style="text-align: left;">eForms Validator</td>
      <td style="text-align: left;">
        <a class="external-link" href="https://validator.preview-ozg-vermittlungsdienst.de/" rel="nofollow">https://validator.preview-ozg-vermittlungsdienst.de/</a>
      </td>
      <td style="text-align: left;">
        <a href="https://validator.staging-ozg-vermittlungsdienst.de/">https://validator.staging-ozg-vermittlungsdienst.de/</a>
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
        <p>Account Management (Keycloak)</p>
      </td>
      <td style="text-align: left;">
        <a href="https://account-management.preview-ozg-vermittlungsdienst.de/" rel="nofollow">https://account-management.preview-ozg-vermittlungsdienst.de/</a>
        <span style="color: rgb(23,43,77);">
          <span> </span>
        </span>
      </td>
      <td style="text-align: left;">
        <a href="https://account-management.staging-ozg-vermittlungsdienst.de/" rel="nofollow" style="text-decoration: inherit;text-align: left;">https://account-management.staging-ozg-vermittlungsdienst.de//</a>
      </td>
      <td style="text-align: left;">
        <a href="https://account-management.ozg-vermittlungsdienst.de/" rel="nofollow" style="text-decoration: inherit;text-align: left;">https://account-management.ozg-vermittlungsdienst.de/</a>
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
        <br/></td>
      <td style="text-align: left;">
        <p>
          <a class="external-link" href="https://enotices2.preview.ted.europa.eu/esenders/webjars/swagger-ui/index.html#/" rel="nofollow">https://enotices2.preview.ted.europa.eu</a>
        </p>
        <p></p>
      </td>
      <td style="text-align: left;">
        <p>
          <a class="external-link" href="https://enotices2.preview.ted.europa.eu/esenders/webjars/swagger-ui/index.html#/" rel="nofollow">https://enotices2.ted.europa.eu</a>
        </p>
        <p></p>
      </td>
    </tr>
  </tbody>
</table>

1. call Account Management of the desired environment (found in [System Environments](/documentation/Development_environments.md) in the _Account Management (Keycloak)_ column).

2. click on 'Forgotten password?"_<br>
![On forgot password](images/kc_login.png)
<br>

3. enter email address and click on 'submit'<br>
![Enter email](images/kc_password_forgotten.png)
<br>

4. the message 'You should receive an email shortly with further instructions' will be displayed.<br>
![Message](images/kc_message_best%C3%A4tigungsemail.png)
<br>

5. check emails: a link to reset the credentials is received in the email.<br>
![Confirmation email](images/e-mail_password_reset.png)
<br>

6. click on 'link to reset credentials'.
<br>

7. user will be redirected to the 'Update Password' page.<br>
![Update PAssword](images/kc_password_update.png)
<br>

8. enter and confirm new password and click on 'Submit'.<br>
Password must be at least 8 characters, contain 1 capital letter and 1 number.
<br>

9.The password must be stored in the FVH software to ensure that the connection with the switching service works.
<br>
