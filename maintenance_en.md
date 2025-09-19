- [Notes for specialist procedure manufacturers](#hinweise-für-fachverfahrenshersteller)
- [Upcoming maintenance windows](#upcoming-maintenance-window)
- [Known bugs and errors](#known-bugs-and-errors)
- [Notes](#notes)
- [Past-maintenance-windows-or-failures](#past-maintenance-windows-or-failures)

## Notes for manufacturers of specialized procedures
- The doe_status INTERNAL_ERROR is NOT a final status, regardless of which ted_status it is combined with. This means that our support team takes a closer look at the notification and then, depending on the error message (e.g. 502 gateway timeout from TED or a Schematron error in terms of content), sets it either to doe_status REJECTED (finally rejected) or to doe_status ACCEPTED. This process is partially automated so that the announcement is automatically retransmitted in the event of connection errors with TED.
- If your system no longer updates the announcement status automatically after the doe_status INTERNAL_ERROR (which is NOT final), you can also check the status via the Notices table in the Self-Service Portal (portal.ozg-vermittlungsdienst.de) with the login data of your system at the Vermittlungsdienst. Notices will not remain in INTERNAL_ERROR status. Please do not open support tickets for this, but contact your specialist procedure manufacturer. Only the doe_status REJECTED (also known as TED = Manually rejected on the Self-Service Portal) is final, in which case you must submit the notice with a new notice ID or version.

Further important information on creating eForms can be found in the [FAQ provided by KoSIT](https://xeinkauf.de/eforms-de/faq/).


## Upcoming maintenance windows

| Environment | System | Date | Time | Comment |
|-------------|----------------------------------|------------|-------------------|---------------------|
| Production and staging | DÖE incl. BKMS | October 25/26, 2025 | 07:00-12:00 | Quarterly maintenance (incl. time changeover) |

## Known bugs and malfunctions of the last months

| system | available since | expected fix | error | status |
|--------------|----------------|----------------------------|--------|--------|
| DÖE staging except BKMS | September 05, 2025 | September 11, 2025 | Authentication error | Fixed on September 11, 2025 |

## Notes

The preview environment is only available between 06:00 and 20:00. Please also use the staging environment for testing purposes, this is available around the clock.

## Past maintenance windows or disruptions in recent months

| Environment | System | Date | Time | Comment |
|--------------------------|---------------------|------------|-------------------|---------------------|
| Production | All TED apps and their APIs | August 28, 2025 | 07:00-09:00 | Maintenance work: All TED apps in production environments and their APIs may be affected by disruptions |
| Production and staging | DÖE | July 31, 2025 | from 16:00 | End of support period for eForms v1.2: From this point on, announcements in v1.2 format will no longer be accepted. All notices accepted and valid until then will continue to be sent to TED and the announcement service and published there. |
| Production and staging | DÖE incl. BKMS | July 26/27, 2025 | 07:00-12:00 | Quarterly maintenance |
