### EfA Implementation Project "Access to Public Procurement".
## Documentation Mediation Service
[table of contents](/documentation/documentation.md)
<br>

# Notes for the creation of eForms-DE documents.

When creating eForms documents, there are some rules to follow regarding certain fields.

## eSender information
>**eForms-DE specific**

Field: *entire section ``<efac:Organization>``*

The DöE assumes the role of eSender for all upper-threshold notices to be submitted to TED. Therefore, for the organizations, the type "ted-esen" should not be used in the notices, as this information is automatically inserted by the eSender hub.

To note here: In the sample files for eForms-DE 1.0 currently available in the Kosit repository, this role is still partially present. With the release of version eForms-DE 1.1, the sample files will also be adapted accordingly, so that the role ted-esen is no longer used.
<br>

## Relationship between Dispatch Date (BT-05) Preferred Publication Date (BT-738)

### Explanation of fields:

BT-05 (Dispatch Date): <cbc:IssueDate> : This field represents the dispatch date of the announcement. It is recommended to have this date set automatically by the system when it is dispatched. For test files, it is recommended to always set the value to the current date. The date should not be set artificially in the past.

BT-738 (Preferred Publication Date): <cbc:RequestedPublicationDate> : This field is used to explicitly specify when an announcement should be published.


### Initial position rules in EU and DE:

_eForms-EU 1.5_.

- BT-05 (Dispatch Date) is mandatory and BT-738 (Preferred Publication Date) is optional (Rule BR-BT-00005-0150)
- BT-738 (Preferred Publication Date) must be no more than 92 days in the future and must be after BT-05 (Dispatch Date) (Rule BR-BT-00738-0053)
- If the BT-738 (Preferred Publication Date) is not filled, a publication will be made "as soon as possible".

Sources:
https://github.com/OP-TED/eForms-SDK/blob/1.5.1/schematrons/static/validation-stage-5.sch

_eForms-EU 1.7_

- BT-05 (Dispatch Date) is mandatory and BT-738 (Preferred Publication Date) is optional (Rule BR-BT-00005-0150).
- BT-738 (Preferred Publication Date) must be no more than 60 days in the future and must be at least 2 days after BT-05 (Dispatch Date) (Rule BR-BT-00738-0053)
- If BT-738 (Preferred Publication Date) is not filled, a publication will be made "as soon as possible"
- BT-05 (Dispatch Date) must be between yesterday and tomorrow (Dynamic Rule)

Sources:
https://github.com/OP-TED/eForms-SDK/blob/1.7.0/schematrons/static/validation-stage-5.sch
https://github.com/OP-TED/eForms-SDK/blob/1.7.0/schematrons/dynamic/validation-stage-6b.sch

_eForms-DE (1.0.1 & 1.1.0)_

- All static EU rules of the respective version apply
- The BT-738 (Preferred Publication Date) is obligated

Sources: https://xeinkauf.de/app/uploads/2023/03/specification-eforms-de-v1.0.1.pdf
https://xeinkauf.de/app/uploads/2023/08/specification-eforms-de-v1.1.0.pdf

### Current problem BEFORE Schematron Release 0.5.3 or 0.6.1

Due to the requirement to specify the BT-738 (Preferred Publication Date), in combination with the current EU rules, it is not possible to have a publication done at TED "as soon as possible", as this only happens if the field is left blank. With the valid restrictions it is only allowed that BT-738 (Preferred Publication Date) must be at least one day (eforms-DE 1.0.1) or at least two days (eforms-DE 1.1.0) after BT-05 (Dispatch Date). Thus, a publication at TED "as soon as possible" is not possible.


### Solution with Schematron Release 0.5.3 resp. 0.6.1

The existing EU rules BR-BT-00005-0150 & BR-BT-00738-0053 restricting BT-738 (Preferred Publication Date) are suspended and replaced by new DE rules (SR-BT-738-1 and SR-BT-738-P60D). This will allow the following submissions:

_eForms-DE 1.0.1_.
- The BT-738 (Preferred Publication Date) may be on the same day as the BT-05 (Dispatch Date).
- The BT-738 (Preferred Publication Date) may be one day after the BT-05 (Dispatch Date).
- The BT-738 (Preferred Publication Date) may be 2-92 days after the BT-05 (Dispatch Date).

_eForms-DE 1.1.0_

- The BT-738 (Preferred Publication Date) may be on the same day as the BT-05 (Dispatch Date).
- The BT-738 (Preferred Publication Date) may be one day after the BT-05 (Dispatch Date).
- The BT-738 (Preferred Publication Date) may be 2-60 days after the BT-05 (Dispatch Date).

IMPORTANT: If the BT-738 (Preferred Publication Date) is less than 2 days after the BT-05 (Dispatch Date), then the BT-738 (Preferred Publication Date) field in the eSender Hub will be removed before sending to TED. This allows TED to perform a publication "as soon as possible". This ensures compatibility with EU rules.

### Implementation of the solution

_Schematron rules_

The new rules to replace the EU rules have already been published by KoSIT:

Schematron release for eForms-DE 1.0.1:
https://projekte.kosit.org/eforms/eforms-de-schematron/-/releases/v0.5.3

Schematron release for eForms-DE 1.1.0
https://projekte.kosit.org/eforms/eforms-de-schematron/-/releases/v0.6.1


_Data service public purchase_

DöE is currently building in both the new Schematron rules and the transformation in the eSender Hub. These changes will be released in production with the next release in week 41 and will be testable (more detailed info about the release can be found [here](https://github.com/EFA-FHB/ozg-vermittlungsdienst-doku/blob/main/Releases.md).

_SDK_EN_

The new rules have already been implemented in SDK-DE 1.0.1 and 1.1.0.

## Creation of eForms in conjunction with notices submitted to TED in the old award format.
>**not eForms-DE specific**.

For a transition period, it may be necessary to create links between notices submitted to TED in the old award format and notices submitted to TED in the eForms format. Possible scenarios necessitating linking include:
- A procurement process was started before 10/25/2023 old format TED-XML and will continue in eForms-DE format. Documents created in the old format must be referenced in subsequent notices.
- A notice published in the old format must be corrected or adapted so that a change notice with reference to this notice is necessary.

TED has provided several fields for these references in the new eForms format where such a reference can be used. For the reference, the Notice Publication ID is used from the old format. This always has a structure nnnnnn-yyyy, where the last four digits represent a year. There are the following specific fields for certain references in eForms:

- Change Notice Version Identifier (BT-758).
- Modification Previous Notice Section Identifier (BT-1501)
- Previous Planning Identifier (BT-125)
- Framework Notice Identifier (OPT-100)

If any of these fields can be used in the eForms, these reference fields should be populated with the Notice Publication ID. If none of these fields can be used in the specific notice, there is an additional option to use the following field:
- Previous Notice (OPP-090)

In general, it is the responsibility of the sending agency to ensure that the correct field and ID is used for the reference. Currently, TED does not perform extensive checks on this, but plans to incorporate this in the future. The Public Purchasing Data Service treats notices with references to old notices as any other type of notice.

TED has confirmed in connection with this discussion that changing the eSender from an FVH to the DöE will have no impact. It will be possible to reference a notice submitted in the old format, even if it was submitted by a different eSender hub.

Further details on the use of references can be found here: https://docs.ted.europa.eu/eforms/latest/schema/procedure-lot-part-information.html#previousNoticeSection

In general, this is a representation of the specification currently known to us by TED. This is subject to change at any time. Therefore, we strongly recommend following TED's communication channels on this topic.
