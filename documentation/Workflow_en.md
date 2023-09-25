### EfA Implementation Project "Access to Public Procurement".
## Documentation mediation service
[table of contents](/documentation/documentation.md)
<br>

## Workflow of an announcement in the data service of public procurement.

The following diagram describes the general workflow of an announcement.
<br><br>
The central point for submitting notices and requesting status information for specialized procedure manufacturers (FVH) is the mediation service. Before submitting to the mediation service, each contracting platform must have an account created in Keycloak and generate a token in the mediation service. This token is used for authentication to submit to the mediation service.
<br><br>
Before sending an announcement to the mediation system, it is recommended to send this announcement to the eForms-DE validation service (External validator). This way it can be checked that the eForms-DE document is valid before it is submitted. Upon submission, the intermediary service will also validate the eForms according to its version (eForms-EU 0.1.1, 1.0, 1.5 & eForms-DE 1.0.0, 1.0.1) and accept or reject them.
<br><br>
If successfully submitted, the notice will be further processed. Depending on whether it is a sub-threshold or a top-threshold eForms document, notices are forwarded either directly to the BKMS (sub-threshold) or to the eSender Hub (top-threshold) - see [Top or Bottom Threshold Award](/documentation/Ober-oder_unterschwellenvergabe.md). In the eSender Hub, a transformation to eForms-EU takes place when eForms-DE is submitted. Which eForms versions each component supports can be found [eForms Support](/documentation/eForms_support.md).
<br><br>
After successful transformation into the EU version of eForms matching the DE version, the announcement is forwarded to TED. The feedback from TED (successful submission or rejection) is stored and triggers a corresponding status change. The time of this status change is also stored so that the time of posting is persisted. Subsequently, TED retrieves the corresponding validation report and extracts any errors or warnings (for example, lawfulness warnings).
<br><br>
If the submission is successful, the exact time of submission is recorded to calculate the 48h deadline for national publication. If no warnings exist the announcement is forwarded to the BKMS at the latest after the 48h period. If lawfulness warnings exist, the announcement is forwarded to BKMS at the latest after 5 days to await manual review by TED. If an announcement is published at TED before, it is immediately forwarded to the BKMS. The publication time is also saved.
<br><br>
During the entire process, status changes, e.g. triggered by a feedback from TED, as well as errors or warnings that have occurred are stored internally. Relevant status information can be queried at any time by FVH via the switching service. Details on status messages and errors can be found in [status information](documentation\Status_information.md).
<br><br>

![Workflow diagram](/documentation/images/workflow_2.png)


