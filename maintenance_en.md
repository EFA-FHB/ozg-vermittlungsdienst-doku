- Important notes for creating eForms](#important-notes-for-creating-eForms)
- Notes for specialist procedure manufacturers](#hinweise-für-fachverfahrenshersteller)
- Upcoming maintenance windows](#upcoming-maintenance-window)
- Known bugs and errors](#known-bugs-and-errors)
- Notes](#notes)
- Past-maintenance-windows-or-failures](#past-maintenance-windows-or-failures)

## Important notes on the creation of eForms
To ensure smooth submission, please always observe the following aspects:

- The **BT-05 Notice Dispatch date** **(IssueDate)** field must be between yesterday and tomorrow at the time of dispatch to the Vermittlungsdienst, otherwise TED will reject the notice.
- The role **ted-esen** must NOT be used in notices, neither as org-role nor as org-sub-role.

- The field **Preferred Publication Date BT-738 (RequestedPublicationDate)** can be set to the same date as the Notice Dispatch date or up to 2 days after the Notice Dispatch date according to the German standard. Please make sure to specify the same time zone for both values, as otherwise TED may reject the request in individual cases
- The filling of the field **BT-165 Winner Size (Winner Size)** is currently not checked by the German rules. Please make sure that this field is filled correctly for the following notice types: '25', '26', '27', '28', '29', '30', '31', '32', 'E4', '33', '34', '35', '36' & '37'
- To fill in the **BT-501 identification number (of the organization)**, please refer to the notes on the routing ID in our FAQ: https://github.com/EFA-FHB/ozg-vermittlungsdienst-doku/blob/main/faq.md#identifikationsnummer-organisation-bt-501
- If your system no longer automatically updates the announcement status after the doe_status INTERNAL_ERROR (which is NOT final), you can also check the status via the Notices table in the Self-Service Portal (portal.ozg-vermittlungsdienst.de) with the login data of your system at the Vermittlungsdienst. Notices will not remain in INTERNAL_ERROR status. Please do not open any tickets with the BDR for this, but contact your specialist procedure manufacturer. Only the doe_status REJECTED is final, in which case you must submit the notice with a new notice ID or version.


## Notes for specialist procedure manufacturers
- The doe_status INTERNAL_ERROR is NOT a final status, regardless of which ted_status it is combined with. This means that our support team takes a closer look at the notification and then, depending on the error message (e.g. 502 Gateway Timeout from TED or an error in content as mentioned above, e.g. IssueDate incorrect), sets it either to doe_status REJECTED (finally rejected) or to doe_status ACCEPTED.  This process will be further optimized and automated in the future, but please do not stop querying the status for the announcement in case of a doe_status INTERNAL_ERROR.

## Upcoming maintenance windows

| Environment | System | Date | Time | Comment |
|-------------|----------------------------------|------------|-------------------|---------------------|
| Production and staging | DÖE incl. BKMS | March 13 and 14, 2025 | 07:00-17:00 | Maintenance work: There may be delays in forwarding to the BKMS and status updates during the specified period. All accepted announcements will be forwarded afterwards.
| Production | TED Apps for eForms, including API interfaces | March 13, 2025 | 07:00-09:00 | Maintenance work: all TED apps in production environments and their APIs may experience disruptions |

## Known bugs and malfunctions

| system | available since | expected fix | bug | status |
|--------------|--------------------------|-----------------------------|---------------------|----|
| DÖE Staging | 18.02.2025 | 19.02.2025 | The delivery of test announcements is currently not possible due to a faulty API integration | __Fixed__ |
| Public service preview and staging | 21.01.2025 | 23.01.2025 | Delivery to the test environments is currently not possible due to a faulty API integration | __Fixed__ |
| Vermittlungsdienst Preview | 08.01.2025 | 17.01.2025 | Preview environment is not available | __Fixed__ |
| All services except BKMS and TED | 07.01.2025 | 09.01.2025 | There may currently be sporadic app failures | __Fixed__ |
| Vermittlungsdienst Preview | 06.01.2025 | 07.01.2025 | Preview environment is not available | __Fixed__ |
| Vermittlungsdienst Preview | 26.11.2024 | 27.11.2024 | Preview environment is not available | __Fixed__ |
| TED Apps for eForms | 31.10.2024 | 05.11.2024 | Validation error: Forms 16, 17 and 29 in eForms-SDK-1.7 version are not recognized correctly during validation. This leads to rejections during transmission. The notices can be resubmitted by increasing the version number under <cbc:VersionID> accordingly.__ | __Fixed by TED__ |
| Announcement service | 19.09.2024 | 20.09.2024 | Authorization error at BKMS: the delivery process is disrupted, but all transmitted announcements will be forwarded immediately as soon as BKMS accepts them again. | __Fixed__ |
| TED Apps for eForms | 06.09.2024 | 09.09.2024 | Technical error in the assignment of publicationIds from TED: Initially incorrect publicationIds were assigned, which were subsequently replaced by the correct ones. __A corresponding update in the DÖE is currently not possible for technical reasons.__| __Fixed by TED__ |
| All validators | 28.05.2024 | 10/2024 | __BR-DE-23__: Validation process aborts if an announcement under _<cac:SubordinateAwardingCriterion>_ contains the tag _<efac:AwardCriterionParameter>_ twice. A __500 Internal Sever Error__ error is returned | __Fixed__ |



## Hints

The preview environment is only available between 06:00 and 20:00. Please also use the staging environment for testing purposes, which is available around the clock.

On 27.09.2023 the API key for submission to TED was adjusted. For this reason, status information for announcements that were submitted to staging or preview before this date will no longer be requested from TED. This is a one-time adjustment and will not occur again in the future.

## Past maintenance windows or disruptions

| Environment | System | Date | Time | Comment |
|--------------------------|---------------------|------------|-------------------|---------------------|
| Staging, preview and alpha | DÖE incl. BKMS | March 06, 2025 | 07:00-17:00 | Maintenance work: During the specified period, there may be delays in forwarding to the BKMS and status updates. All accepted announcements will be forwarded afterwards.
| Production and staging | All TED apps for eForms, including API interfaces | February 12, 2025 | 07:00-09:00 | Quarterly maintenance: The services are not available during the specified period |
| Staging | All DÖE apps except BKMS and TED | January 16, 2025 | 08:00-12:00 | Quarterly maintenance: The services are not available during the specified period |
| Production | TED Apps for eForms, including API interfaces | October 31, 2024 | 07:00-09:00 | Announced by TED: The application and its API may not be available during the specified period |
| Production | All services of the DÖE except BKMS | October 26-27, 2024 | Quarterly maintenance (incl. time changeover) |
| Production | TED Apps for eForms | September 03, 2024 | 07:00-09:00 | Announced by TED |
| Production | TED Apps for eForms | September 05, 2024 | 07:00-10:30 |Announced by TED |
| Production | TED Apps for eForms | August 20, 2024 | 07:00-09:00 CET | Announced by TED |
| Production | All services of the DÖE except BKMS (Staging) | 01.08.2024 | | Technical disruption due to certificate renewal |
| Production | All services of the DÖE except BKMS | July 27-28, 2024 | | Quarterly maintenance |
| Production | Announcement service | 30 July 2024 | | Integration disruption between Vermittlungsdienst and eSender due to deployment of the new version of the announcement service |
| Preview | Vermittlungsdienst | 26.06.2024 | | Preview environment is not accessible |
| Production + Staging | All services of the DÖE except BKMS (Production + Staging) | 14.06.2024 | | Currently the production and staging environment is not available due to problems in the data center. We expect a prompt resolution |
| Preview | All services of the DÖE except BKMS | 22.05.2024 | | Preview environment is not available |
| Preview | All services of the DÖE except BKMS | 30.04.2024 | | Preview environment is not available |
| Preview | All services of the DÖE except BKMS | 22.04.2024 | | Preview environment is not available |
| Production | Validator in the Vermittlungsdienst | 02.04.2024 | | In the case of very large announcements with a large number of rules, there are occasional timeouts during delivery |
| Production | Viewer | 02.04.2024 | | In some cases, eFormsDE 1.2 announcements with certain indicator values cannot be rendered |
| Production | Integration with BKMS | 14.03.2024 | | Authentication problem with BKMS leads to disruptions during the delivery process |
| Production | Vermittlungsdienst | 29.02.2024 | | Disruptions in the processing of individual announcements due to heavy load |
| All environments | Vermittlungsdienst | 31.05.2024 | from 14:00 CEST | Infrastructure maintenance: removal of static IP addresses |
| Production | TED Production | 16.05.2024 | 07:00 - 09:00 CEST | TED Infrastructure Maintenance |
| Staging and Preview | TED Preview | 15.05.2024 | 07:00 - 09:00 CEST | TED Infrastructure Maintenance |
| Staging | All services of the DÖE except BKMS | 22.05.2024 | 09:00 - 12:00 CEST | Infrastructure maintenance |
| Production | All services of the DÖE except BKMS | 29.05.2024 | 16:00 - 17:00 CEST | Infrastructure maintenance |
| Production | All services of the DÖE except BKMS | 27-28.07.2024 | 20:00 - 20:00 CEST | Infrastructure maintenance |
| Production | All services of the DÖE except BKMS | 26-27.10.2024 | 20:00 - 20:00 CEST | Infrastructure maintenance |
| Staging | All services of the DÖE except BKMS | 18.04.2024 | 09:00 - 12:00 CEST | Infrastructure maintenance |
| Production | All services of the DÖE except BKMS | 21.03.2024 | 16:00 - 17:00 CEST | Maintenance work: Authorization token to be recreated |
| Production | All services of the DÖE except BKMS | 27-28.01.2024 | 20:00 - 20:00 CEST | Infrastructure maintenance |
| Staging | All services of the DÖE except BKMS | 17.01.2024 | 19:00 - 20:00 CEST | Infrastructure maintenance |
| Production and staging | All services of the DÖE except BKMS | 09.01.2024 | 20:00 - 22:00 CEST | Infrastructure maintenance |
| Preview | All services of the DÖE except BKMS | 27.12.2023 - 02.01.2024 | | Temporary unavailability, please use the respective services in the staging environment for tests in the meantime! |
| Production | All services of the Vermittlungsdienst incl. eSender (not BKMS) | 21.11.2023 | 06:00 - 07:00 CEST | Infrastructure maintenance |
| Production | All services of the Vermittlungsdienst incl. eSender (not BKMS) | 11.12.2023 | 06:00 - 07:00 CEST | Infrastructure maintenance |
| BKMS Production | BKMS | 27.10 | 27.10. 13:10 - 14:35 CEST | Online search function was not available |
| DÖE Produktion + Staging | all services except BKMS | 25.10.2023 | 15:31 - 16:03 CEST | Unavailability of the data center |
| DÖE Production + Staging | all services except BKMS |23.10.2023 - 24.10.2023 | 17:00 - 09:00 CEST | Unavailable due to infrastructure problems |
| DÖE Production + Staging | all services except BKMS | 20.10.2023 | 10:00 - 13:00 CEST | Deployment for performance improvements |
| Production + Staging | all services except BKMS | 10.10.2023 | 09:00 - 12:00 CEST | Data Center Maintenance |
| TED Preview | TED Apps for eForms | 10/10/2023 | 07:00 - 10:00 CEST | Announced by TED |
| TED Production | TED Apps for eForms | 11.10.2023 | 07:00 - 10:00 CEST | Announced by TED |
| TED Production + Preview | TED Developer Portal, TED Apps for eForms | 02.10.2023 | 07:00 - 09:00 CEST | Announced by TED |
| TED Production | TED Apps for eForms | 27.09.2023 | 07:00 - 09:00 CEST | Announced by TED |
| TED Production | Vermittlungsdienst | 14.09.2023 | 08:00 - 09:30 CEST | temporarily unavailable |
| TED Production | TED Apps for eForms | 30.08.2023 | 18:00-22:00 CEST | Announced by TED |
| TED Production | TED Apps for eForms | 30.08.2023 | 18:00-22:00 CEST | Announced by TED |
| TED Preview | TED Apps for eForms | 28.08.2023 | 07:00-11:00 CEST | Announced by TED |
| TED Preview | TED Apps for eForms | 24.08.2023 | 07:00-08:00 CEST | Announced by TED |
| TED Production | TED Apps for eForms | 23.08.2023 | 07:00-08:00 CEST | Announced by TED |
