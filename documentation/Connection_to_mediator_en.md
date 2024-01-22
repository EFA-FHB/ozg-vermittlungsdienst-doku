
### EfA implementation project "Access to public procurement"
## Documentation on the mediation service
[Table of contents](/documentation/Documentation.md)
<br>

>**Note** <br>
>Please note: If subliminal announcements are still sent to service.bund.de, these must NOT also be sent to the switching service!

# Connection to the switching service
Notices can be sent to the switching service via the [REST API](#connection-per-rest-api) of the switching service or via the [eDelivery Network PEPPOL](#connection-per-peppol).
<br>

## Connection via REST API
The REST API and the associated documentation for the existing endpoints are available at https://ozg-vermittlungsdienst.de.
To use the API, access data must be requested once. Authorization takes place via OAuth 2.0.
<br>

### Applying for an account to deliver announcements

>**Note** <br>
>After the production release in June, a new user must be requested for the production and staging environment, even if a user already exists in Preview.

From 04.10.2023, a new account will be set up via the self-service portal (production environment: https://portal.ozg-vermittlungsdienst.de). An account can be created in the portal by specifying an e-mail address and a password. After confirming the e-mail address, the user can log in and fill out the application form for a new VD account. A separate user is required for each awarding platform. <br>

Once the user has been created, an authentication e-mail containing a link for authentication and password creation is sent to the specified user e-mail address for verification. If you apply for 10 accounts on one environment, you will also need 10 individual email addresses. The email address is used to retrieve the tokens that you need for unique authentication with the account. It must therefore be unique.
<br><br>
The link is valid for 10 days.<br>
Click on the link and follow the instructions to create a password.
<br><br>
An access token and a refresh token can be generated using the API with the access data created.
<br><br>
Please note that you must apply for one access per development environment (preview, staging, production). The access data is not synchronized. [Preview](https://portal.preview-ozg-vermittlungsdienst.de/) and [Staging](https://portal.staging-ozg-vermittlungsdienst.de/) accounts can be requested in the corresponding self-service portal environment.
<br>

### Authentication and authorization (access token, refresh token)
The endpoint `POST /api/token` is used with the parameters `username` and `password` to be passed in order to obtain an `access_token` and `refresh_token`. The username is the e-mail address you have specified.

The `access_token` is valid for 24 hours and can be used for authorization for all subsequent requests in the header as follows: `Authorization: Bearer <<access_token>>`. After the 24 hours have expired, re-authentication is required. To avoid regular authentication with `username` and `password`, a new `access_token` can be generated using the `refresh_token` and the endpoint `POST /api/token/refresh` without having to perform a new complete authentication.

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
In future, it will also be possible to transmit notices to the exchange service via the PEPPOL eDelivery Network. Details and further information will follow.
<br>



## How to reset a user password in Keycloak?

>**Note** <br>
> The user's password is also the password that is used to log in to the switching service interface! <br>
> If you change the password, make sure that it is also changed in the software for posting to the switching service!

1. call up Account Management for the desired environment (can be found under [System environments](/documentation/Development_environments.md) in the _Account Management (Keycloak)_ column)

2. click on 'Forgot password?
![Forgot password](images/kc_login.png)
<br>

3. enter your e-mail address and click on 'Send'<br>
![Enter e-mail](images/kc_passwort_vergessen.png)
<br>

4. the message 'You should receive an e-mail with further instructions shortly' is displayed<br>
![message](images/kc_nachricht_best%C3%A4tigungsemail.png)
<br>

5. check the emails: A link to reset the login information is included in the email.<br>
![Confirmation email](images/e-mail_password_reset.png)
<br>

6. click on 'Link to reset credentials'.
<br>

7. the user is redirected to the 'Update password' page<br>.
![Update password](images/kc_password_update.png)
<br>

8. enter and confirm the new password and click on 'Submit'.<br>
The password must consist of at least 8 characters, contain 1 capital letter and 1 number.
<br>

9. the password must be stored in the FVH software to ensure that the connection with the switching service works.
<br>

## Delete access
To delete your access, please send an e-mail to Nortal AG support [oeffentliche-vergabe-support@nortal.com](mailto:oeffentliche-vergabe-support@nortal.com).<br>
The e-mail must contain the following information

- System environment in which the access data should be deleted
- E-mail address which is used as the user name
- URL of the awarding platform
- First and last name and e-mail address of the FVH representative
- Name of the FVH

After checking the data provided in the e-mail, we will delete the access and send you a confirmation by e-mail...
