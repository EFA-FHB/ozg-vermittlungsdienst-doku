- Notes for specialist procedure manufacturers](#hinweise-für-fachverfahrenshersteller)
- Upcoming maintenance windows](#upcoming-maintenance-windows)
- Known bugs and errors](#known-bugs-and-errors)
- Notes](#notes)
- Past-maintenance-windows-or-failures](#past-maintenance-windows-or-failures)

## Notes for specialist procedure manufacturers
- The doe_status INTERNAL_ERROR is NOT a final status, regardless of which ted_status it is combined with. This means that our support team takes a closer look at the notification and then, depending on the error message (e.g. 502 gateway timeout from TED or a Schematron error in terms of content), sets it either to doe_status REJECTED (finally rejected) or to doe_status ACCEPTED. This process is partially automated so that the announcement is automatically resubmitted in the event of connection errors with TED.
- If your system no longer automatically updates the announcement status after the doe_status INTERNAL_ERROR (which is NOT final), you can also check the status via the Notices table in the Self-Service Portal (portal.ozg-vermittlungsdienst.de) using the login data of your system at the Vermittlungsdienst. Notices will not remain in INTERNAL_ERROR status. Please do not open support tickets for this, but contact your specialist procedure manufacturer. Only the doe_status REJECTED (also known as TED = Manually rejected on the Self-Service Portal) is final, in which case you must submit the notice with a new notice ID or version.

Further important information on creating eForms can be found in the FAQ provided by [KoSIT](https://xeinkauf.de/eforms-de/faq/)

## Upcoming maintenance windows

| Environment | System | Date | Time | Comment |
|-------------|----------------------------------|------------|-------------------|---------------------|
| Production and staging | DÖE incl. BKMS | October 25/26, 2025 | 07:00-12:00 | Quarterly maintenance (incl. time changeover) |

## Known bugs and malfunctions of the last months

| system | available since | expected fix | error | status |
|--------------|----------------|----------------------------|--------|--------|
|--------------|----------------|----------------------------|--------|--------|

## Notes

The preview environment is only available between 06:00 and 20:00. The staging environment should also be used for testing purposes; it is available around the clock.

## Past maintenance windows or disruptions in the last few months

| Environment | System | Date | Time | Comment |
|--------------------------|---------------------|------------|-------------------|---------------------|
| Production and staging | SSP portal | October 22-23, 2025 | -- |The STOP function via the SSP portal is currently not functional. It is recommended to use the direct call of the Vermittlungsdienst https://ozg-vermittlungsdienst.de/q/swagger-ui/#/Lieferungen/stopPublication - Fixed on October 23, 2025 |
| Staging | SSP portal | October 06-17, 2025| -- | Authentication error - Fixed on October 17, 2025 |
| Staging | DÖE except BKMS | September 05-11, 2025 | -- | Authentication error - Fixed on September 11, 2025 |
| Production | All TED apps and their APIs | August 28, 2025 | 07:00-09:00 | Maintenance work: All TED applications in production environments and their APIs may be affected by disruptions |
| Production and staging | DÖE | July 31, 2025 | from 16:00 | End of support period for eForms v1.2: From this point on, announcements in v1.2 format will no longer be accepted. All notices accepted and valid until then will continue to be sent to TED and the announcement service and published there. |
| Production and staging | DÖE incl. BKMS | July 26/27, 2025 | 07:00-12:00 | Quarterly maintenance |
