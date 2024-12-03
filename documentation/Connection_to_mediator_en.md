
### Data service public procurement
[Table of contents](/documentation/documentation.md)
<br>

>**Note** <br>
>Please note: If subliminal notices continue to be sent to service.bund.de, these must NOT also be sent to the Vermittlungsdienst!

# Connection to the Vermittlungsdienst
Notices can be transmitted to the Vermittlungsdienst via the [REST-API](#anbindung-per-rest-api) of the Vermittlungsdienst or via the [eDelivery-Network PEPPOL](#anbindung-per-peppol).
<br>

## Connection via REST API
The REST API and the associated documentation for the existing endpoints are available at https://ozg-vermittlungsdienst.de.
To use the API, access data must be requested once. Authorization takes place via OAuth 2.0.
<br>

### Applying for an account to deliver announcements

>**Note** <br>
>After the production release in June 2023, a new user must be requested for the production and staging environment, even if a user already exists in Preview.

From October 4, 2023, a new account will be set up via the self-service portal (production environment: https://portal.ozg-vermittlungsdienst.de). An account can be created in the portal by specifying an e-mail address and a password. After confirming the e-mail address, the user can log in and fill out the application form for a new VD account. A separate user is required for each awarding platform. <br>

Once the user has been created, an authentication email containing a link for authentication and password creation is sent to the specified user email address for verification. If you apply for 10 accounts on one environment, you will also need 10 individual e-mail addresses. The e-mail address is used to retrieve the tokens that you need for unique authentication with the account. It must therefore be unique.
<br><br>
The link is valid for 10 days.<br>
Click on the link and follow the instructions to create a password.
<br><br>
With the access data created, an access token and a refresh token can be generated using the API.
<br><br>
Please note that you must apply for one access per development environment (preview, staging, production). The access data is not synchronized. [Preview](https://portal.preview-ozg-vermittlungsdienst.de/) and [Staging](https://portal.staging-ozg-vermittlungsdienst.de/) accounts can be requested in the corresponding self-service portal environment.
<br>

### Authentication and authorization (access token, refresh token)
The endpoint `POST /api/token` is used with the parameters `username` and `password` to be passed in order to obtain an `access_token` and `refresh_token`. The username is the e-mail address you have specified.

The `access_token` is valid for 24 hours and can be used for authorization for all subsequent requests in the header as follows: `Authorization: Bearer <<access_token>>`. After 24 hours, a new authentication is required. To avoid regular authentication with `username` and `password`, a new `access_token` can be generated using the `refresh_token` and the endpoint `POST /api/token/refresh` without having to perform a new full authentication.

Requesting a new token does not invalidate the previous token.

Example response of the endpoints `POST /api/token` and `POST /api/token/refresh`:

```
{
  "access_token": "eyJhbGciOikpXVCJ9.eyJzMDIyfQ.SflKxwRJSM",
  "expires_in": 36000,
  "refresh_expires_in": 36000,
  "refresh_token": "eyJhbGciOikpXVCJ9.eyJzMDIyfQ.SflKxwRJSM",
  "token_type": "Bearer",
  "not-before-policy": 0,
  "session_state": "e65f24ae-4e90-4635-8ae7-4fb89fe471bf",
  "scope": "profile email"
}
```
<br>

Further information on the concept of the refresh token and instructions for implementation are available at https://auth0.com/blog/refresh-tokens-what-are-they-and-when-to-use-them/
<br>


## Connection via PEPPOL

Public procurement platforms can also submit notices to the **Public Procurement Data Service** via the **Peppol infrastructure** for secure data exchange.

### Use of the Peppol infrastructure
Systems registered in the Peppol infrastructure can send notices to the addressee with the **Peppol ID "0204:994-DOEVD-83" (production)** using the **Peppol profile "P008 - Publish Notices "**.

- Further information on the Peppol profile can be found here: [Peppol Documentation - Publish Notices](https://peppol.org/documentation/technical-documentation/pre-award-documentation)

### Communication
Communication takes place via the use of a **pre-award-capable AccessPoint**, which are either:
- are provided by commercial providers, or
- can be implemented independently in a Peppol-compliant manner (possibly based on open source).

**Important:** Full pre-award capability of the AccessPoint includes support for **"REM Evidence "**, as described in the following documentation:
[Peppol BIS eDelivery Guide for Pre-Award v1.3](https://docs.peppol.eu/pracc/files/BIS-eDelivery-guide-for-pre-award-v1.3.pdf)

### Registration
Questions regarding registration must be clarified via a **Peppol-Authority**:
[List of Peppol Authorities](https://peppol.org/members/peppol-authorities)

### Further information
- Official Peppol website: [peppol.org](https://peppol.org)
- For additional technical information, please refer to the following explanations.

### Connecting procurement platforms to the Vermittlungsdienst via PEPPOL

The primary interface for the transmission of notices is the PEPPOL network. Notices can be transmitted as follows:

### PEPPOL address of the Vermittlungsdienst (Participant ID).
- Productive environment**: `0204:994-doevd-83`.
- Staging**: `0204:994-doevdtest-85`

#### Transmission via the business process with the ID:
- `urn:fdc:peppol.eu:prac:bis:p008:1.2`
  - Send**: The sender transmits a *Publish Notice Request* (Transaction ID: `urn:fdc:peppol.eu:prac:trns:t015:1.2`).
  - **Receive**: The Vermittlungsdienst sends a *Notice Publication Response* (Transaction ID: `urn:fdc:peppol.eu:prac:trns:t016:1.2`).

### SMP Inbox Document Owner:
- **Productive environment**: `oeffentliche-vergabe-peppol`
- Staging**: `oeffentlich-vergabe-peppol-test`.

#### URL:
- **Productive environment**: [https://ws.b2brouter.com/transactions](https://ws.b2brouter.com/transactions)
- **Staging**: [https://ws-staging.b2brouter.com/transactions](https://ws-staging.b2brouter.com/transactions)

---

### Structure of a PEPPOL message

PEPPOL messages consist of several layers that are defined by different standards. Each layer encloses the data of the next layer and extends it with specific aspects that are required. The layers from the outside in:

#### **1. Standard Business Document Header (SBDH):**
- Used to route messages in the PEPPOL network;
- Contains the PEPPOL sender and recipient addresses;
- Access points only require the data of this layer for routing;
- SBDH is an XML format. The next layer is contained in a Base64-encoded XML tag.

#### **2. Associated Signature Containers (ASiC):**
- A ZIP archive of any data that is cryptographically signed;
- Contains the file `META-INF/ASiCManifest.xml`, which lists all contained files with checksums;
- Exactly one file is marked with `RootFile=true` in `META-INF/ASiCManifest.xml`. This file is the business or process document that is to be processed;
- The business or process document can reference other files in the ASiC container.

#### **3. Business document:**
- Contains the technical transaction to be executed by the sender;
- The Vermittlungsdienst can receive *Publish Notice Requests* (Transaction ID: `urn:fdc:peppol.eu:prac:trns:t015:1.2`) to publish notices;
- In response, the Vermittlungsdienst sends a *Notice Publication Response* (Transaction ID: `urn:fdc:peppol.eu:prac:trns:t016:1.1`);
- In the case of a *Publish Notice Request*, the business document contains relative paths to BKMS files that are to be published. These paths refer to other files in the ASiC container.

---

#### **Notice documents (for Publish Notice Request):**
- Notice in XML eForms format;
- The *Peppol BIS Profile P008 Publish Notice* of the pre-award version 1.2 is used. Earlier versions do not yet support the eForms DE standard;
- The profile includes the transactions:
  - **T015 Publish Notice**: For the transmission of notices;
  - **T016 Notice Publication Response**: For status information that the Vermittlungsdienst sends back to the sender.

---

### The PEPPOL access point
The PEPPOL access point for the Vermittlungsdienst and the BKMS is operated by the Procurement Office of the Federal Ministry of the Interior (BeschA) itself.

---

### Web resources
- **Peppol homepage:** [https://peppol.eu/](https://peppol.eu/)
- **SBDH/UBL identifiers/processes/profiles for Peppol:** [https://docs.peppol.eu/pracc/files/BIS-eDelivery-guide-for-pre-award-v1.2.pdf](https://docs.peppol.eu/pracc/files/BIS-eDelivery-guide-for-pre-award-v1.2.pdf)
- **PEPPOL pre-award standard documentation:** [https://docs.peppol.eu/pracc/](https://docs.peppol.eu/pracc/)
- Peppol BIS Profile P008:** [https://docs.peppol.eu/pracc/profiles/p008/index.html](https://docs.peppol.eu/pracc/profiles/p008/index.html)
- **PEPPOL T015 - Publish Notice 1.2:** [https://docs.peppol.eu/pracc/transactions/T015/index.html](https://docs.peppol.eu/pracc/transactions/T015/index.html)
- **PEPPOL T016 - Notice Publication Response 1.2:** [https://docs.peppol.eu/pracc/transactions/T016/index.html](https://docs.peppol.eu/pracc/transactions/T016/index.html)

<br>



## How to reset a user password in Keycloak?

>**Note** <br>
> The user's password is also the password used for logging in to the switching service interface! <br>
> If you change the password, make sure that it is also changed in the software for posting to the Vermittlungsdienst!

1. call up the self-service portal of the desired environment (can be found under [System environments](/documentation/Development_environments.md) in the _Self Service Portal_ column).

2. click on 'Forgot password?
![Forgot password](images/kc_login.png)
<br>

3. enter your e-mail address and click on 'Send'.<br>
![Enter e-mail](images/kc_passwort_vergessen.png)
<br>

4. the message 'You should receive an e-mail with further instructions shortly' is displayed.<br>
![message](images/kc_nachricht_best%C3%A4tigungsemail.png)
<br>

5. check the emails: A link to reset the login information is included in the email.<br>
![Confirmation email](images/e-mail_password_reset.png)
<br>

6. click on 'Link to reset credentials'.
<br>

7. the user will be redirected to the 'Update password' page<br>.
![Update password](images/kc_password_update.png)
<br>

8. enter and confirm the new password and click on 'Submit'.<br>
The password must consist of at least 8 characters, contain 1 capital letter and 1 number.
<br>

9. the password must be stored in the FVH software to ensure that the connection with the Vermittlungsdienst works.
<br>

## Delete access
To delete your access, please send an e-mail to Bundesdruckerei support [support-oeffentlichevergabe@bdr.de ](mailto:support-oeffentlichevergabe@bdr.de ).<br>
The e-mail must contain the following information

- System environment in which the access data is to be deleted
- E-mail address to be used as the user name
- URL of the awarding platform
- First name, surname and email address of the FVH representative
- Name of the FVH

After checking the data provided in the e-mail, we will delete the access and send you a confirmation by e-mail.
