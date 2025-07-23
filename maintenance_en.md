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
- If your system no longer updates the announcement status automatically after the doe_status INTERNAL_ERROR (which is NOT final), you can also check the status via the Notices table in the Self-Service Portal (portal.ozg-vermittlungsdienst.de) with the login data of your system at the Vermittlungsdienst. Notices will not remain in INTERNAL_ERROR status. Please do not open support tickets for this, but contact your specialist procedure manufacturer. Only the doe_status REJECTED (also known as TED = Manually rejected on the Self-Service Portal) is final, in which case you must submit the notice with a new notice ID or version.


## Notes for manufacturers of specialized procedures
- The doe_status INTERNAL_ERROR is NOT a final status, regardless of which ted_status it is combined with. This means that our support team takes a closer look at the notification and then, depending on the error message (e.g. 502 gateway timeout from TED or a Schematron error in terms of content), sets it either to doe_status REJECTED (finally rejected) or to doe_status ACCEPTED. This process is partially automated so that the announcement is automatically retransmitted in the event of connection errors with TED.

## Upcoming maintenance windows

| Environment | System | Date | Time | Comment |
|-------------|----------------------------------|------------|-------------------|---------------------|
| Production and Staging | DÖE | July 31, 2025 | from 16:00 | End of support period for eForms v1.2: From this point on, announcements in v1.2 format will no longer be accepted. All notices accepted and valid until then will continue to be sent to TED and the announcement service and published there. |
| Production and Staging | DÖE incl. BKMS | July 26/27, 2025 | 07:00-12:00 | Quarterly maintenance |
| Production and staging | DÖE incl. BKMS | October 25/26, 2025 | 07:00-12:00 | Quarterly maintenance (incl. time changeover) |

## Known bugs and malfunctions of the last months

| system | available since | expected fix | error | status |
|--------------|----------------|----------------------------|--------|--------|
| *No entries* | - | - | **Currently no bugs or malfunctions are documented** | - |

## Notes

The preview environment is only available between 06:00 and 20:00. Please also use the staging environment for testing purposes, this is available around the clock.

On 27.09.2023 the API key for submission to TED was adjusted. For this reason, status information for announcements that were submitted to staging or preview before this date will no longer be requested from TED. This is a one-time adjustment and will not occur again in the future.

## Past maintenance windows or disruptions in the last few months

| Environment | System | Date | Time | Comment |
|--------------------------|---------------------|------------|-------------------|---------------------|
| Production | DOE excl. BKMS | June 17, 2025 | 18:00-22:00 | Quarterly maintenance: Affected services are not available during the specified period |
| Staging | DÖE excl. BKMS | May 13, 2025 | 09:00-13:00 | Quarterly maintenance: Affected services are not available during the specified period |
