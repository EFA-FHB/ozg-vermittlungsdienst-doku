### Data service public procurement
[Table of contents](/documentation/documentation.md)
<br>

# Distinction between lower and upper threshold awards

When processing a notice in the switching service, certain criteria are used to check whether a sub-threshold or above-threshold notice has been transmitted.
<br><br>
If it is a subthreshold notice, it is forwarded directly to the BKMS after validation. The announcement is not sent to TED.
<br><br>
An above-threshold announcement is forwarded by the switching service to the eSender Hub. There, the supplied format is converted into an eForms-EU format of the notice required by TED. After successful validation, the notice is transmitted to TED and then sent to the BKMS in compliance with legal requirements (e.g. 48h deadline).
<br>

## Criteria for the decision
The system decides between sub-threshold and above-threshold award based on the following criteria
1. subtype of the contract notice
2. eForms version

Only if both criteria for the above-threshold award are met will this be carried out.
<br>

### Subtype of the notice
This information is read from the XML field `SubTypeCode`. If the subtype of the notice begins with "E" (e.g. E3), it is a subthreshold notice. Above-threshold notices have a number 1-40 as subtype.
<br>

### eForms version
This information is read from the XML field `CustomizationID`. TED only accepts certain eForms-EU versions and only certain eForms versions can be processed by the eSender Hub.
Further details on version support can be found here: [eForms Version Support](/documentation/eForms_support.md)