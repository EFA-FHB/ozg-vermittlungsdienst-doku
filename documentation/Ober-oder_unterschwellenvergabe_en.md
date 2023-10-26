### EfA Implementation Project "Access to Public Procurement".
## Documentation mediation service
[table of contents](/documentation/documentation.md)
<br>

## Distinction between lower and higher threshold awarding

When processing a notice in the mediation service, certain criteria are used to determine whether a subthreshold or a superthreshold notice was transmitted.
<br><br>
If it is a subthreshold notice, it is forwarded directly to BKMS after validation. There will be no transmission of the notice to TED.
<br><br>
A suprathreshold announcement is forwarded by the switching service to the eSender hub. There, the delivered format is converted into an eForms-EU format of the announcement required for TED. After successful validation, the notice is submitted to TED and then sent to BKMS in compliance with legal requirements (e.g. 48h deadline).
<br>

## Criteria for decision
The system decides between sub-threshold and upper-threshold award based on the following criteria:
1. subtype of the notice
2. eForms version

Only if both criteria for the Upper Threshold award are met, the award will be made.
<br>

### Subtype of the announcement
This information is read from the XML field 'SubTypeCode'. If the subtype of the notice starts with "E" (e.g. E3), it is a subthreshold notice. Upper-threshold announcements have a number 1-40 as subtype.
<br>

### eForms Version
This information is read from the XML field `CustomizationID`. TED only accepts certain eForms-EU versions and only certain eForms versions can be processed by the eSender Hub.
More details about version support can be found here: [eForms version support](/documentation/eForms_support.md)