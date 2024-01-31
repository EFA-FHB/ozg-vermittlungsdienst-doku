### Public procurement data service

## Important notes on creating eForms
To ensure a smooth submission, please always observe the following aspects:

- The **BT-05 Notice Dispatch date** **(IssueDate)** field must be between yesterday and tomorrow at the time of dispatch to the switching service, otherwise TED will reject the notice. This is currently NOT checked in the switching service as it is a new dynamic rule from TED
- The role **ted-esen** must NOT be used in announcements, neither as org-role nor as org-sub-role. This leads to problems in the transformation, as the procurement office is always automatically set as ted-esen

- The field **Preferred Publication Date BT-738 (RequestedPublicationDate)** can be set to the same date as the Notice Dispatch date or up to 2 days after the Notice Dispatch date according to the German standard. Please make sure to specify the same time zone for both values, as otherwise TED may reject the request in individual cases
- The filling of the field **BT-165 Winner Size (Winner Size)** is currently not checked by the German rules. Please make sure that this field is filled correctly for the following notice types: '25', '26', '27', '28', '29', '30', '31', '32', 'E4', '33', '34', '35', '36' & '37'
- Currently there is a bug in TED that based on restrictive rules on CPV codes **grant recipients** can only tender for works, but <u>not for supplies and services</u>. TED is still working on fixing this.
The CPV codes are interpreted as follows:
    - Supply services: Main CPV code from divisions 0 to 44 or 48
    - Services: Main CPV code from divisions 49 to 98
    - Construction work: Main CPV code from division 45
    - If you are affected by this (notification fails due to rule **BR-BT-00262-0211**), please contact our support support-oeffentlichevergabe@bdr.de immediately for specific assistance
- To fill in the **BT-501 identification number (of the organization)**, please refer to the information on the routing ID in our FAQ: https://github.com/EFA-FHB/ozg-vermittlungsdienst-doku/blob/main/faq.md#identifikationsnummer-organisation-bt-501
- If your system no longer updates the announcement status automatically after the doe_status INTERNAL_ERROR (which is NOT final), you can also check the status via the Notices table in the Self-Service Portal (portal.ozg-vermittlungsdienst.de) with the login data of your system at the mediation service. Notices will not remain in INTERNAL_ERROR status. Please do not open any tickets with the BDR for this, but contact your specialist procedure manufacturer. Only the doe_status REJECTED is final, in which case you must submit the notice with a new notice ID or version.


## Notes for specialist procedure manufacturers
- The doe_status INTERNAL_ERROR is NOT a final status, regardless of which ted_status it is combined with. This means that our support will take a closer look at the announcement and then, depending on the error message (e.g. 502 Gateway Timeout from TED or a content error as mentioned above, e.g. IssueDate incorrect), will either set it to doe_status REJECTED (finally rejected) or to doe_status ACCEPTED.  This process will be further optimized and automated in the future, but please do not stop querying the status for the announcement in the event of a doe_status INTERNAL_ERROR.
- We are currently seeing an increasing number of rejections when submitting based on incorrect email syntax for the "authorEmail" specification. Please ensure that a valid email with the correct syntax is supplied in this field when submitting to the placement service for each announcement. If the email is not correct, the following error message will appear: "NOTICE_METADATA_INVALID - Required data is missing or the data entered does not match the schema". We validate emails using the following regex expression provided by TED: \b[A-Za-z0-9._%+-]+@[A-Za-z0-9.-]+(?:_[A-Za-z0-9.-])*\.[A-Za-z]{2,5}\b <br>
If you have domains that do not correspond to this, please open a support ticket with TED.

## Upcoming maintenance windows or known issues

| environment | system | date | time | comment |
|-------------|---------------------|------------|-------------------|---------------------|
| Production and staging | All services of the DöE except BKMS | 09.01.2024 | 20:00 - 22:00 CEST | Infrastructure maintenance |
| Staging | All services of the DöE except BKMS | 17.01.2024 | 19:00 - 20:00 CEST | Infrastructure maintenance |
| Production | All services of the DöE except BKMS | 27-28.01.2024 | 20:00 - 20:00 CEST | Infrastructure maintenance |
| Production | All services of the DöE except BKMS | 27-28.04.2024 | 20:00 - 20:00 CEST | Infrastructure maintenance |
| Production | All services of the DöE except BKMS | 27-28.07.2024 | 20:00 - 20:00 CEST | Infrastructure maintenance |
| Production | All services of the DöE except BKMS | 26-27.10.2024 | 20:00 - 20:00 CEST | Infrastructure maintenance |



## Known bugs

| system | available since | expected fix | bug |
|--------------|--------------------------|-----------------------------|---------------------|
| DöE VD + Validator + Viewer | 11.12.2023 | fixed | For 'Authorization error. The user does not have sufficient permissions to access this resource', please request a new access_token and authenticate with it, then the problem no longer exists.  |


## Notes

The preview environment is only available between 06:00 and 20:00. Please also use the staging environment for testing purposes, which is available around the clock.

On 27.09.2023 the API key for submission to TED was adjusted. For this reason, status information for announcements that were submitted to staging or preview before this date will no longer be requested from TED. This is a one-time adjustment and will not occur again in the future.

## Past maintenance windows or disruptions

| Environment | System | Date | Time | Comment |
|-------------|---------------------|------------|-------------------|---------------------|
| Preview | All services of the DöE except BKMS | 27.12.2023 - 02.01.2024 | | Temporary unavailability, please use the respective services in the staging environment for tests in the meantime! |
| Production | All services of the switching service incl. eSender (not BKMS) | 21.11.2023 | 06:00 - 07:00 CEST | Infrastructure maintenance |
| Production | All services of the switching service incl. eSender (not BKMS) | 11.12.2023 | 06:00 - 07:00 CEST | Infrastructure maintenance |
| BKMS Production | BKMS | 27.10 | 27.10. 13:10 - 14:35 CEST | Online search function was not available |
| DÖE Produktion + Staging | all services except BKMS | 25.10.2023 | 15:31 - 16:03 CEST | Unavailability of the data center |
| DöE Production + Staging | all services except BKMS |23.10.2023 - 24.10.2023 | 17:00 - 09:00 CEST | Unavailable due to infrastructure problems |
| DöE Production + Staging | all services except BKMS | 20.10.2023 | 10:00 - 13:00 CEST | Deployment for performance improvements |
| DöE Production + Staging | all services except BKMS | 10.10.2023 | 09:00 - 12:00 CEST | Data center maintenance |
| TED Preview | TED Apps for eForms | 10/10/2023 | 07:00 - 10:00 CEST | Announced by TED |
| TED Production | TED Apps for eForms | 11.10.2023 | 07:00 - 10:00 CEST | Announced by TED |
| TED Production + Preview | TED Developer Portal, TED Apps for eForms | 02.10.2023 | 07:00 - 09:00 CEST | Announced by TED |
| TED Production | TED Apps for eForms | 27.09.2023 | 07:00 - 09:00 CEST | Announced by TED |
| TED Production | Switching Service | 14.09.2023 | 08:00 - 09:30 CEST | temporarily unavailable |
| TED Production| TED Apps for eForms | 30.08.2023 | 18:00-22:00 CEST | Announced by TED |
| TED Production| TED Apps for eForms | 30.08.2023 | 18:00-22:00 CEST | Announced by TED |
| TED Preview | TED Apps for eForms | 28.08.2023 | 07:00-11:00 CEST | Announced by TED |
| TED Preview | TED Apps for eForms | 24.08.2023 | 07:00-08:00 CEST | Announced by TED |
| TED Production | TED Apps for eForms | 23.08.2023 | 07:00-08:00 CEST | Announced by TED |
