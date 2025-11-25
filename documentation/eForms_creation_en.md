### Data service public procurement
[Table of contents](/documentation/documentation.md)
<br>

### Notes on creating eForms-DE documents

When creating eForms documents, it is important to observe a few rules for certain fields.

## eSender information
>**eForms-DE-specific**

Field: *entire section ```<efac:Organization>````*

The Public Procurement Data Service assumes the role of eSender for all notices above the EU thresholds to be transmitted to TED. For the organizations, the type "ted-esen" must therefore NOT be used in the notices, as this information is automatically inserted by the eSender Hub.
When a contract notice is created and an organization is specified, the role it plays in the contract notice must be defined for each organization. The roles are defined in the EU code list: https://github.com/OP-TED/eForms-SDK<br>
One value in the EU code list is "ted-esen". This value may not be used in Germany.

## Relationship between Dispatch Date (BT-05) and Preferred Publication Date (BT-738)

### Explanation of the fields:

BT-05 (Dispatch Date) <cbc:IssueDate>: This field represents the dispatch date of the announcement. It is recommended that this date is set automatically by the system when the notice is sent. For test files, it is recommended that the value is always set to the current date. The date should not be set artificially in the past.

BT-738 (Preferred Publication Date) <cbc:RequestedPublicationDate>: This field is used to explicitly specify when an announcement is to be published.
