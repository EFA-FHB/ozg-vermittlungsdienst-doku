### EfA Implementation Project "Access to Public Procurement".
## Documentation mediation service
[table of contents](/documentation/documentation.md)
<br>

## Change notices/ stop-and-update functionality.

## content
- Adjust the content of a notice](#stop-or-change)
    - [Update to a notice](#update)
	- [Change notices](#change-notice)
- STOP publication functionality](#stop-func)

## Customize the content of a notice<span id='stop-or-change'>.
There are two ways to change the content of a notice: By *stop + update* before publication or by a change notice (*change notice*) after publication.
<br><br>

### Update to a notice<span id='update'>.
An update or resubmission (also referred to as an update) to a notice is a simple editing process when the notice has not yet been published in TED and/or BKMS. If an announcement needs to be corrected, the previous version must first be stopped or in rejected status. Otherwise, an update is not possible to ensure that only one valid version of a document exists in the Mediation Service at any given time. To create an update, the same noticeID should be used as in the previous document to be corrected, only the versionID must be increased (gaps are possible). An update is NOT the same as a change notice. An update does not contain the UBL extension of a change notice and can only be submitted before the notice is published.
<br>

#### **Examples**

Scenario A: Correction of a rejected notice through an update.

Notice A with noticeID ABC *Version 01* is submitted and rejected, e.g. because it was filled in incorrectly. Since it was rejected, it is not published.
2. the FVH would like to correct this notice.
3. the FVH submits an update with noticeID ABC *Version 02*.
4. the update is accepted because the previous version of the document has the status REJECTED.

Scenario B: Using an update to edit a submitted notice.

1. notice A with noticeID ABC *Version 01* is submitted and accepted. It is not yet published, e.g. because the desired publication date is in the future.
2. the FVH wants to edit something in this notice, e.g. because some information has changed and needs to be adjusted.
3. the FVH stops the previously submitted noticeID ABC *version 01* using the stop endpoint (This is mandatory before sending an update. TED has announced that this will likely be so restricted in TED in the future).
4. the switching service stops the announcement in TED and BKMS (depending on where it has already been sent)
5. the FVH submits an update with noticeID ABC *version 02*.
6. the update is accepted because the previous version of the notice is in STOPPED status.
<br><br>

### Change Notice<span id='change-notice'>.
A change notice (also referred to as a change notice) is an amendment that changes a previously published notice. When a change notice is submitted, that notice has its own noticeID and versionID. A change notice always contains a UBL extension that must specify which specific notice is to be changed. This is specified in the BT-738 Change Notice Identifier field. Here the noticeID-versionID or the Notice Publication Number (if the referenced notice was submitted in the old TED-XML format) must be specified in the xml.

Example of a reference reference with noticeID-versionID:

`<efbc:ChangedNoticeIdentifier>c4c415ee-ac08-4465-8fa6-57568cf69462-01</efbc:ChangedNoticeIdentifier>`

Example of a reference using the Notice Publication ID:

`<efbc:ChangedNoticeIdentifier>01234567-2022</efbc:ChangedNoticeIdentifier>`

The process for submitting a Change Notice is the same as for any other notice. The process for submitting to TED and BKMS is also the same for Change Notices as for any other notice.
<br><br>

## STOP Publication functionality<span id='stop-func'>.
The Stop Publication functionality is used to stop publication of notices on TED/BKMS (upper-threshold award) or BKMS only (lower-threshold award). Stopping a notice is only possible if a notice has been fully processed internally but not yet published.

The publication of a notice can be stopped for the following reasons:
1. manually by an external user (FVH):
The user can request stopping of an announcement using the TrackingCode via the API V1/notices/stop/{trackingCode} in the mediation service. In this case, it is stored in the switching service that it was a manual stop operation.
Automatic: If TED manually rejects a submitted notice due to [Lawfullness Warnings](Status_information.md/#lawfullness), this notice will not be published in TED. If this announcement has already been sent to BKMS, it will now be automatically stopped in BKMS as well. In this case, it is stored in the switching service that this was an automatic stop process.

There are some differences in the way that surface and subliminal notices can be stopped.
 <br> <br>

**Subthreshold Announcement** <br>
The publication can only be manually stopped before the preferred publication date (BT-738) specified in the notice, so the notice is not yet published on BKMS.

![nat-flow-stop](images/nat-flow-stop.png)
 <br> <br><br>

**Overthreshold award: manual stop** <br>
The publication can only be stopped manually before the announcement is published on TED. Whether the announcement has already been published in BKMS is not relevant here. A manual stop is only possible if no previous versions intended for publication exist (see examples above).

![eu-manual-stop](images/eu-manual-stop.png)
 <br> <br>

**Overthreshold allocation: automatic stop** <br>
In case of manual rejection by TED, the publication is automatically stopped in BKMS, even if it should have been published in BKMS before.

![eu-auto-stop](images/eu-auto-stop.png)

 <br>

**Stop responses** <br>
You can see what responses you get when sending stop requests from the API at https://ozg-vermittlungsdienst.de/q/swagger-ui/#/Lieferungen/stopPublication.