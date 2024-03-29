
### Data service public procurement
[Table of contents](/documentation/documentation.md)
<br>

# Self-service portal of the DöE

The self-service portal of the Public Purchasing Data Service for the production environment is available at the URL https://portal.ozg-vermittlungsdienst.de/.
There is also the portal for the staging environment https://portal.staging-ozg-vermittlungsdienst.de/ and the portal for the preview environment https://portal.preview-ozg-vermittlungsdienst.de/.
<br><br>
The Self-Service Portal (SSP) offers user-friendly access to all [documents](https://portal.ozg-vermittlungsdienst.de/documentation) of the Data Service Public Procurement (DöE).

The portal will be an operational and support platform for users. It will help you with the transition and allow you to get away from emails. It will offer more possibilities to manage users and access yourself.

## From 11.12.23: Roles in SSP
### Important information about the release on 11.12.


On 11.12. there will be a new release of the SSP. From this date, your technical VD account will no longer work for logging into the SSP, but will only be used for the technical connection to the Vermittlungsdienst, Validator and Viewer.
<br> <br>To log in to the portal, you must create a user. To do this, simply click on "Register" in the portal and create a new account. If you already have an SSP Portal account, you can use it. You can now verify this user via a new process. In the verification process, you can also upload a PDF with a declaration of commitment. However, there is no fixed template for this. The document only serves to assure us that you are authorized to manage accounts for your company as a specialist procedure manufacturer.

> **WARNING**
> For the SSP admin account, please use the e-mail address of a mailbox, not a personal one, so that other people from your organization can also manage the VD accounts and dashboard accounts.
> The SSP admin account is protected by 2FA via e-mail, which is why access to the mailbox is absolutely necessary for authorized persons.

After creating your account, please send us a list of all your technical VD accounts (existing accounts of submitting systems) that are to be managed by this new SSP Admin account as soon as possible. The list should contain the respective VD account email and the associated platform URL and be sent to Support so that we can link your account to the VD system accounts accordingly.
<br><br>After verifying your SSP Admin account, you can use this account to create so-called dashboard users with their own email and password. For each dashboard user, you can explicitly select the submitting systems (VD accounts) from which this user should be able to view the notifications.

> **TIP**
> Only dashboard users can see the announcement table, NOT SSP admin users or VD accounts. You may therefore have to set up an additional dashboard user with a separate e-mail address as an SSP Admin if you want to see the announcement overview yourself.

### Role overview

> **IMPORTANT**
> All accounts need a unique e-mail address. We recommend NOT to use personal e-mail addresses for the SSP-Admin account!

From 11.12.23 the following roles will exist in the Self-Service Portal:
| Role in SSP | Description | Actions available in SSP |
|---------------------|--|--|
| SSP (-Admin)-User | Responsible for all user accounts of the FVH; Admin for the FVH <br> Must be verified by Support to unlock all user administration rights <br><br> <b>Important: To enable all user management functions, you must tell us which VD account should be linked to your SSP admin account</b> | <ul><li>Creating new VD accounts (connections to the Vermittlungsdienst)</li> <li>Creating new dashboard users</li><li> User management for your own organization</li><li>View documentation</li></ul>|
| Dashboard user | Service employee/customer support account with overview of all announcements of the linked VD accounts | <ul><li>Overview of all announcements of the linked VD accounts</li> <li>One user can be linked to several VD accounts</li><li>View documentation</li></ul>| |
| VD account | Only for the technical connection to the Vermittlungsdienst | <ul><li>May not log in to SSP</li><li>View documentation</li></ul> |


## Available services

The portal offers the following main functions:
* View documentation
  * There are long-term plans to transfer the documentation that is currently in Github to the portal. The SSP will then later become the central communication channel for the DöE*
* Own creation of admin account in SSP for specialist procedure manufacturers (SSP admin accounts)
* After successful verification: Create VD accounts and dashboard users with SSP admin account (replaces account creation by email)
* With dashboard user account: View overview of announcements
* SSP admin account can perform user management and rights assignment (e.g. create users who can view announcements) <br>

## User information
### Create account
To create an account in SSP, please click on the user icon at the top right and select "Register". You then have the option of creating an account with an e-mail address and password. A confirmation e-mail will be sent shortly to the e-mail address you entered. Please confirm your account using the link provided. You can then log in with your access data and have access to the registration form for verification as an SSP admin. The form will be sent to Support for checking and, if necessary, approval.

### Create a new technical VD account
Once an admin account has been created in SSP and verified by Support (see above) and the user is logged in, they can fill out the form to create a technical VD account. You will find the option to do this on the start page and in the menu at the top left under "VD account registration". An email will be sent to the email address entered with the account details.

### Create new dashboard user
It is also possible to create new dashboard users. To do this, the SSP admin user must navigate to "Dashboard user registration" and complete the form. One or more VD accounts can be selected under "Linked VD account". An email is sent to the email address entered with the account details and the dashboard user can log in and view all notifications sent by the linked account and their current status.

### View sent notifications (notice table)
With a dashboard user account (see above), you can log in to the portal and view all notifications sent by the linked account or accounts as well as their current status and (if available) error messages.

## Future planned features
The following features are on the roadmap for the SSP:
* **Download notice xml**: The dashboard user can download the XML file from the submitted notice table
**Improved display of error messages**: The dashboard user will be shown errors/warnings for the selected notice in a more readable format (if any exist)
**Display of the sender of the announcement**: The user is shown the email address of the sender of the notice. This e-mail address can be searched for
**Enable stopping of notices in the notice table** (configurable right)
**Display of change notices in the notice table**: This means that the dashboard user can now also see the Change Noticess in addition to PIN/CN/CAN. It can be filtered accordingly.
