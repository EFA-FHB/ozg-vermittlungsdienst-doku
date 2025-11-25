### Data service public procurement
[Table of contents](/documentation/documentation.md)
<br>

# Distinguishing between awards below and above the EU thresholds

When processing a contract notice in the Vermittlungsdienst, certain criteria are used to check whether a contract notice was submitted above or below the EU thresholds.
<br><br>
If it is a notice below the EU thresholds, it is forwarded directly to the notice service after validation. The contract notice will not be sent to TED.
<br><br>
A notice above the EU thresholds is forwarded by the Vermittlungsdienst to the eSender Hub. There, the submitted eForms-DE format is converted into the eForms-EU format required by TED. After successful validation, the notice is transmitted to TED and then sent to the notice service in compliance with legal requirements (e.g. 48-hour deadline).
<br>

## Criteria for differentiation
The system decides between notices above and below the EU thresholds based on the following criteria
1. subtype of the notice
2. eForms version

Only if both criteria are met for notices above the EU thresholds will this be carried out.
<br>

### Subtype of the notice
This information is read from the XML field `SubTypeCode`. If the subtype of the notice begins with "E" (e.g. E3), it is a notice below the EU thresholds. Notices above the EU thresholds have a number from 1 to 40 as a subtype.
<br>

### eForms version
This information is read from the XML field `CustomizationID`. TED only accepts certain eForms EU versions and only certain eForms versions can be processed by the eSender Hub. Further details on version support are documented here: [eForms Version Support](/documentation/eForms_support.md).