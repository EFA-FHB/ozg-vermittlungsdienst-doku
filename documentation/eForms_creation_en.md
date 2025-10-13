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
