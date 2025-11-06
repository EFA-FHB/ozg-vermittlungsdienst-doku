
### Data service public procurement
[Table of contents](/documentation/documentation.md)
<br>

# Self-service portal of the public procurement data service

The self-service portal of the Public Purchasing Data Service for the production environment is available at the URL https://self-service.datenservice-oeffentlicher-einkauf.de/.
There is also the portal for the staging environment https://self-service.staging.datenservice-oeffentlicher-einkauf.de/ and the portal for the preview environment https://self-service.preview.datenservice-oeffentlicher-einkauf.de/.
<br><br>
As an operating and support platform, the Self-Service Portal (SSP) offers user-friendly access to all [documents](https://self-service.datenservice-oeffentlicher-einkauf.de/documentation) of the Data Service Public Procurement (DÖE).

## Roles in the SSP

To log in to the portal, a user must be created by clicking on 'Register' to create a new account. If an SSP portal account already exists, this can be used. This user can now verify via a new process. A PDF with a declaration of commitment can also be uploaded in the verification process. However, there is no fixed template for this. This document confirms that the person named there is authorized to manage accounts for their company as a specialist procedure manufacturer.

> **WARNING** <br>
> For the SSP admin account, please use the e-mail address of a mailbox, but not a personal one, so that other people from the organization can also manage the Vermittlungsdienst accounts and dashboard accounts.
> The SSP admin account is protected by 2FA via email, which is why access to the mailbox is absolutely necessary for authorized persons.

Once the SSP admin account has been verified, so-called dashboard users and Vermittlungsdienst users can be created with their own email and password using this account. For each dashboard user, you can explicitly select from which submitting systems (Vermittlungsdienst accounts) this user should be able to view the notices.

> **TIP** <br>
> Only dashboard users can see the announcement table, NOT SSP admin users or Vermittlungsdienst users. An additional dashboard user with a separate e-mail address must therefore be set up for an SSP admin if they want to see the announcement overview themselves.

### Role overview

> **IMPORTANT** <br>
> All accounts need a unique e-mail address. It is recommended NOT to use personal e-mail addresses for the SSP admin account!

The following roles are available in the Self-Service Portal:
| Role in SSP | Description | Actions available in SSP |
|---------------------|--|--|
| SSP admin | Responsible for all FVH user accounts; admin for the FVH <br> Must be verified by Support in order to activate all user administration rights <br><br> <b>Important: To enable all user administration functions, you must tell us which VD account should be linked to your SSP admin account</b> | <ul><li>Creating new VD accounts (connections to the Vermittlungsdienst)</li> <li>Creating new dashboard users</li><li> User administration for your own organization</li><li>View documentation</li></ul>|
| Dashboard user | Service employee/customer support account with overview of all announcements of the linked VD accounts | <ul><li>Overview of all announcements of the linked VD accounts</li> <li>One user can be linked to several VD accounts</li><li>View documentation</li></ul>| |
| VD account | Only for the technical connection to the Vermittlungsdienst | <ul><li>View documentation</li></ul> |

## Available services

The portal offers the following main functions:
* View documentation
* Create admin accounts in the SSP for specialist procedure manufacturers (SSP admin accounts)
* After successful verification: Create VD accounts and dashboard users with SSP admin account (replaces account creation by e-mail)
* With dashboard user account: View overview of announcements
* SSP admin account can perform user management and rights assignment (e.g. create users who can view announcements) <br>

## User information
### Create account
To create an account in the SSP, simply click on the user icon in the top right-hand corner and then select "Register". You then have the option of creating an account with an e-mail address and password. A confirmation e-mail will be sent shortly afterwards to the e-mail address entered. You can confirm the creation of the account via the link contained therein. It is then possible to log in with the access data and access the registration form for verification as an SSP admin. The form is sent to Support for verification.

### Create a new technical Vermittlungsdienst account
Once an admin account has been created in the SSP and verified by Support (see above) and the user is logged in, they can fill out the form to create a technical Vermittlungsdienst account. This is done on the start page and in the menu at the top left under "VD account registration". An e-mail with the account details will then be sent to the e-mail address entered.

### Create a new dashboard user
It is also possible to create new dashboard users. To do this, the SSP admin user must navigate to "Dashboard user registration" and complete the form. One or more VD accounts can be selected under "Linked VD account". An email is sent to the email address entered with the account details and the dashboard user can log in and view all notifications sent by the linked account and their current status.

### View sent notifications (notice table)
With a dashboard user account (see above), you can log in to the portal and view all notifications sent by the linked account(s) as well as their current status and (if available) error messages. The dashboard user can also download the XML file from the table of submitted notices and stop notices in the notice table with a configurable right.


