### Data service public procurement
[Table of contents](/documentation/documentation.md)
<br>

### Notes on creating eForms-DE documents

When creating eForms documents, it is important to observe a few rules for certain fields.

## eSender information
>**eForms-DE-specific**

Field: *entire section ```<efac:Organization>````*

The DÖE assumes the role of the eSender for all above-threshold notices to be transmitted to TED. For the organizations, the type "ted-esen" must therefore NOT be used in the announcements, as this information is automatically inserted by the eSender Hub.
When you create a notice and specify an organization, you must define for each organization what role it plays in the notice. The roles are defined in the EU code list: https://github.com/OP-TED/eForms-SDK/blob/1.7.0/codelists/organisation-role.gc.
One value in the EU code list is "ted-esen". This value may not be used in Germany.

## Relationship between Dispatch Date (BT-05) and Preferred Publication Date (BT-738)

### Explanation of the fields:

BT-05 (Dispatch Date) – cbc:IssueDate: This field represents the dispatch time of the notice. It is recommended that this date be set automatically by the system at the moment of dispatch. For test files, it is recommended to always set the value to the current date.
The date should not be artificially set to a past value.

BT-738 (Preferred Publication Date) – cbc:RequestedPublicationDate: This field is used to explicitly specify the desired publication date of the notice.
