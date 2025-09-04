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
<br>

## Relationship between Dispatch Date (BT-05) and Preferred Publication Date (BT-738)

### Explanation of the fields:

BT-05 (Dispatch Date) <cbc:IssueDate>: This field represents the dispatch date of the announcement. It is recommended that this date is set automatically by the system when the notice is sent. For test files, it is recommended that the value is always set to the current date. The date should not be set artificially in the past.

BT-738 (Preferred Publication Date) <cbc:RequestedPublicationDate>: This field is used to explicitly specify when an announcement is to be published.


### Initial situation Rules in EU and DE:

_eForms-EU 1.5_

- BT-05 (Dispatch Date) is mandatory and BT-738 (Preferred Publication Date) is optional (rule BR-BT-00005-0150)
- The BT-738 (Preferred Publication Date) may be a maximum of 92 days in the future and must be after the BT-05 (Dispatch Date) (rule BR-BT-00738-0053)
- If the BT-738 (Preferred Publication Date) is not filled, publication is carried out "as soon as possible"

Sources:
https://github.com/OP-TED/eForms-SDK/blob/1.5.1/schematrons/static/validation-stage-5.sch

_eForms-EU 1.7_

- BT-05 (Dispatch Date) is mandatory and BT-738 (Preferred Publication Date) is optional (rule BR-BT-00005-0150)
- The BT-738 (Preferred Publication Date) may be a maximum of 60 days in the future and must be at least 2 days after the BT-05 (Dispatch Date) (rule BR-BT-00738-0053)
- If the BT-738 (Preferred Publication Date) is not filled, publication is carried out "as soon as possible"
- BT-05 (Dispatch Date) must be between yesterday and tomorrow (dynamic rule)

Sources:
https://github.com/OP-TED/eForms-SDK/blob/1.7.0/schematrons/static/validation-stage-5.sch
https://github.com/OP-TED/eForms-SDK/blob/1.7.0/schematrons/dynamic/validation-stage-6b.sch

_eForms-DE (1.0.1 & 1.1.0)_

- All static EU rules of the respective version apply
- The BT-738 (Preferred Publication Date) is mandatory

Sources: https://xeinkauf.de/app/uploads/2023/03/specification-eforms-de-v1.0.1.pdf
https://xeinkauf.de/app/uploads/2023/08/specification-eforms-de-v1.1.0.pdf

### Current problem BEFORE Schematron release 0.5.3 or 0.6.1

Due to the obligation to specify BT-738 (Preferred Publication Date), in combination with the applicable EU rules, it is not possible to have a publication carried out at TED "as soon as possible", as this only happens if the field is left blank. With the current restrictions, it is only permissible for BT-738 (Preferred Publication Date) to be at least one day (eforms-DE 1.0.1) or at least two days (eforms-DE 1.1.0) after BT-05 (Dispatch Date). This means that publication at TED "as soon as possible" is not possible.


### Solution with Schematron release 0.5.3 or 0.6.1

The existing EU rules BR-BT-00005-0150 and BR-BT-00738-0053 for restricting BT-738 (Preferred Publication Date) are suspended and replaced by new DE rules (SR-BT-738-1 and SR-BT-738-P60D). This will allow the following submissions:

_eForms-DE 1.0.1_
- The BT-738 (Preferred Publication Date) may be on the same day as the BT-05 (Dispatch Date)
- The BT-738 (Preferred Publication Date) may be one day after the BT-05 (Dispatch Date)
- The BT-738 (Preferred Publication Date) may be 2-92 days after the BT-05 (Dispatch Date)

_eForms-EN 1.1.0_

- The BT-738 (Preferred Publication Date) may be on the same day as the BT-05 (Dispatch Date)
- The BT-738 (Preferred Publication Date) may be one day after the BT-05 (Dispatch Date)
- The BT-738 (Preferred Publication Date) may be 2 - 60 days after the BT-05 (Dispatch Date)

IMPORTANT: If the BT-738 (Preferred Publication Date) is less than 2 days after the BT-05 (Dispatch Date), then the BT-738 (Preferred Publication Date) field in the eSender Hub will be removed before sending to TED. This enables TED to carry out publication "as soon as possible". This ensures compatibility with EU regulations.

### Implementation of the solution

Schematron rules

The new rules to replace the EU rules have already been published by KoSIT:

Schematron release for eForms-DE 1.0.1:
https://projekte.kosit.org/eforms/eforms-de-schematron/-/releases/v0.5.3

Schematron release for eForms-DE 1.1.0:
https://projekte.kosit.org/eforms/eforms-de-schematron/-/releases/v0.6.1


Data Service Public Purchasing

The DÖE is currently implementing both the new Schematron rules and the conversion in the eSender Hub. These changes will be published in production with the next release in week 41 and can then be tested (more detailed information on the release can be found [here](https://github.com/EFA-FHB/ozg-vermittlungsdienst-doku/blob/main/Releases.md)).

_SDK-EN_

The new rules have already been implemented in SDK-DE 1.0.1 and 1.1.0.

## Creation of eForms in connection with notices submitted to TED in the old award format
>**not eForms-DE-specific**

For a transitional period, it may be necessary to create links between notices submitted to TED in the old award format and notices submitted to TED in eForms format. Possible scenarios that make linking necessary are
- An award process was started before 25.10.2023 in the old TED-XML format and will be continued in the eForms-DE format. The documents created in the old format must be referenced in the subsequent notices.
- A notice published in the old format must be corrected or adapted so that a change notice with reference to this notice is required.

TED has provided several fields for these references in the new eForms format in which such a reference can be used. The Notice Publication ID from the old format is used for the reference. This always has the structure nnnnnnnn-yyyy, with the last four digits representing a year. There are the following specific fields for certain references in eForms:

- Change Notice Version Identifier (BT-758)
- Modification Previous Notice Section Identifier (BT-1501)
- Previous Planning Identifier (BT-125)
- Framework Notice Identifier (OPT-100)

If one of these fields can be used in eForms, these reference fields should be filled with the Notice Publication ID. If none of these fields can be used in the specific notice, it is also possible to use the following field:
- Previous Notice (OPP-090)

In general, it is the responsibility of the sending body to ensure that the correct field and ID is used for the reference. TED does not currently carry out extensive checks in this regard, but intends to do so in the future. The Public Procurement Data Service treats notices with references to old notices like any other type of notice.

In connection with this discussion, TED has confirmed that changing the eSender from an FVH to the DÖE will have no effect. It will be possible to reference an announcement submitted in the old format, even if it was submitted by a different eSender hub.

Further details on the use of references can be found here: https://docs.ted.europa.eu/eforms/latest/schema/procedure-lot-part-information.html#previousNoticeSection

In general, this is a representation of the specification currently known to us by TED. This may change at any time. We therefore strongly recommend that you follow TED's communication channels on this topic.

