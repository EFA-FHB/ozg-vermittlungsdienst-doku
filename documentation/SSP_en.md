
### Data service public procurement
[Table of contents](/documentation/documentation.md)
<br>

# Self-service portal of the DÖE

The self-service portal of the Public Purchasing Data Service for the production environment is available at the URL https://self-service.datenservice-oeffentlicher-einkauf.de/.
There is also the portal for the staging environment https://self-service.staging.datenservice-oeffentlicher-einkauf.de/ and the portal for the preview environment https://self-service.preview.datenservice-oeffentlicher-einkauf.de/.
<br><br>
The Self-Service Portal (SSP) offers user-friendly access to all [documents](https://self-service.datenservice-oeffentlicher-einkauf.de/documentation) of the Data Service Public Procurement (DÖE).

The portal will be an operational and support platform for users. It will help you with the transition and allow you to get away from emails. In future, it will offer more options for managing users and access yourself.

## Roles in the SSP

To log in to the portal, you must create a user. To do this, simply click on "Register" in the portal and create a new account. If you already have an SSP portal account, you can use it. You can now verify this user via a new process. In the verification process, you can also upload a PDF with a declaration of commitment. However, there is no fixed template for this. The document only serves to assure us that you are authorized to manage accounts for your company as a specialist procedure manufacturer.

> **WARNING**
> For the SSP admin account, please use the e-mail address of a mailbox, not a personal one, so that other people from your organization can also manage the VD accounts and dashboard accounts.
> The SSP admin account is protected by 2FA via email, which is why access to the mailbox is absolutely necessary for authorized persons.

After creating your account, please send us a list of all your technical VD accounts (existing accounts of submitting systems) that are to be managed by this new SSP admin account as soon as possible. The list should contain the respective VD account email and the associated platform URL and be sent to Support so that we can link your account to the VD system accounts accordingly.
<br><br>After verifying your SSP admin account, you can use this account to create so-called dashboard users with their own email and password. For each dashboard user, you can explicitly select the submitting systems (VD accounts) from which this user should be able to view the notifications.

> **TIP**
> Only dashboard users can see the announcement table, NOT SSP admin users or VD accounts. You may therefore have to set up an additional dashboard user with a separate e-mail address as an SSP admin if you want to see the announcement overview yourself.

### Role overview

> **IMPORTANT**
> All accounts need a unique e-mail address. We recommend NOT to use personal e-mail addresses for the SSP admin account!

From 11.12.23 the following roles will exist in the Self-Service Portal:
| Role in SSP | Description | Actions available in SSP |
|---------------------|--|--|
| SSP admin | Responsible for all FVH user accounts; admin for the FVH <br> Must be verified by Support in order to activate all user administration rights <br><br> <b>Important: To enable all user administration functions, you must tell us which VD account should be linked to your SSP admin account</b> | <ul><li>Creating new VD accounts (connections to the Vermittlungsdienst)</li> <li>Creating new dashboard users</li><li> User administration for your own organization</li><li>View documentation</li></ul>|
| Dashboard user | Service employee/customer support account with overview of all announcements of the linked VD accounts | <ul><li>Overview of all announcements of the linked VD accounts</li> <li>One user can be linked to several VD accounts</li><li>View documentation</li></ul>| |
| VD account | Only for the technical connection to the Vermittlungsdienst | <ul><li>May not log in to SSP</li><li>View documentation</li></ul> |


## Available services

The portal offers the following main functions:
* View documentation
  * There are long-term plans to transfer the documentation that is currently in Github to the portal. The SSP will then later become the central communication channel for the DÖE*
* Own creation of admin accounts in the SSP for specialist procedure manufacturers (SSP admin accounts)
* After successful verification: Create VD accounts and dashboard users with SSP admin account (replaces account creation by e-mail)
* With dashboard user account: View overview of announcements
* SSP admin account can manage users and assign rights (e.g. create users who can view announcements) <br>

## User information
### Create account
To create an account in the SSP, please click on the user icon at the top right and select "Register". You then have the option of creating an account with an e-mail address and password. A confirmation e-mail will be sent shortly to the e-mail address you entered. Please confirm your account by clicking on the link provided. You can then log in with your access data and have access to the registration form for verification as an SSP admin. The form will be sent to Support for checking and, if necessary, approval.

### Create a new technical VD account
Once an admin account has been created in the SSP and verified by Support (see above) and the user is logged in, they can fill out the form to create a technical VD account. You will find the option to do this on the start page and in the menu at the top left under "VD account registration". An e-mail will be sent to the e-mail address entered with the account details.

### Create a new dashboard user
It is also possible to create new dashboard users. To do this, the SSP admin user must navigate to "Dashboard user registration" and complete the form. One or more VD accounts can be selected under "Linked VD account". An email is sent to the email address entered with the account details and the dashboard user can log in and view all notifications sent by the linked account and their current status.

### View sent notifications (notice table)
With a dashboard user account (see above), you can log in to the portal and view all notifications sent by the linked account or accounts as well as their current status and (if available) error messages. The user can also download the XML file from the table of submitted notices and stop notices in the notice table with a configurable right.

