- [Notes for specialist procedure manufacturers](#hinweise-für-fachverfahrenshersteller)
- [Upcoming maintenance windows](#upcoming-maintenance-windows)
- [Known bugs and malfunctions in recent months](#known-bugs-and-malfunctions-in-recent-months)
- [Notes](#notes)
- [Past maintenance windows or disruptions in the last few months](#past-maintenance-windows-or-bugs-of-the-last-months)

## Notes for specialist procedure manufacturers
- The doe_status INTERNAL_ERROR is NOT a final status, regardless of which ted_status it is combined with. This means that our support team takes a closer look at the notification and then, depending on the error message (e.g. 502 gateway timeout from TED or a Schematron error in terms of content), sets it either to doe_status REJECTED (finally rejected) or to doe_status ACCEPTED. This process is partially automated so that the announcement is automatically resubmitted in the event of connection errors with TED.
- If your system no longer updates the announcement status automatically after the doe_status INTERNAL_ERROR (which is NOT final), you can also check the status via the Notices table in the Self-Service Portal (self-service.datenservice-oeffentlicher-einkauf.de) with the login data of your system at the Vermittlungsdienst. Notices will not remain in INTERNAL_ERROR status. Please do not open support tickets for this, but contact your specialist procedure manufacturer. Only the doe_status REJECTED (also known as TED = Manually rejected on the Self-Service Portal) is final, in which case you must submit the notice with a new notice ID or version.

Further important information on creating eForms can be found in the FAQ provided by [KoSIT](https://xeinkauf.de/eforms-de/faq/)

## Upcoming maintenance windows

| Environment | System | Date | Time | Comment |
|-------------|--------|------|------|---------|
| Production | TED API | 9 July 2026 | 07:00–08:00 | Maintenance work: All TED APIs in production environments will be temporarily unavailable |

## Known bugs and malfunctions of the last months

| System | Available since | Expected fix | Bug | Status |
|--------|----------------|--------------|-----|--------|
| Vermittlungsdienst, eSender-Hub and all Validators | 16th April 2026 | KW 19 2026 | At present, there may be instances where submissions to TED are rejected. The validation of rule BR-BT-00720-0048 (BT-720-Tender) currently differs from the TED validation. | Resolved on 7th May 2026 |

## Notes

The preview environment is only available between 06:00 and 20:00. The staging environment should also be used for testing purposes; it is available around the clock.

## Past maintenance windows or disruptions in the last few months

| Environment | System | Date | Time | Comment |
|-------------|--------|------|------|---------|
| Production | DÖE excl. Bekanntmachungsservice | 20 May 2026 | 16:00–20:00 | Maintenance work: All production applications and their APIs are temporarily unavailable |
| Production | TED API | 28 April 2026 | 07:00–09:00 | Maintenance work: All TED APIs in production environments will be temporarily unavailable |
| Production | TED API | 23 April 2026 | 07:00–09:00 | Maintenance work: All TED APIs in production environments may be affected by disruptions |
| Production | All TED apps and their APIs | 18 March 2026 | 13:50–16:00 | Submission of notices disrupted — resolved by TED |
| Production | All TED apps and their APIs | 23 February 2026 | 07:00–09:00 | Maintenance work: All TED apps in production environments and their APIs may be affected by disruptions |
| Production | All TED apps and their APIs | 19 February 2026 | 07:00–09:00 | Maintenance work: All TED apps in production environments and their APIs will be unavailable |
| Production | All TED apps and their APIs | 30 January 2026 | 06:45–09:00 | Maintenance work: All TED apps in production environments and their APIs will be unavailable |
| Production | All TED apps and their APIs | 7 January 2026 | 07:00–09:00 | Maintenance work: All TED apps in production environments and their APIs may be affected by disruptions |