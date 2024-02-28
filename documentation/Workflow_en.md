### Data service public procurement
[Table of contents](/documentation/documentation.md)
<br>

# Workflow of an announcement in the public procurement data service

The following diagram describes the general workflow of an announcement.
<br><br>
The central point for submitting notices and querying status information for specialized procedure manufacturers (FVH) is the Vermittlungsdienst. Before being able to submit to the Vermittlungsdienst, each awarding platform must have an account created in Keycloak and generate a token in the Vermittlungsdienst. The account can be requested in the Self-Service Portal (see [Connection to Mediator](/documentation/Connection_to_mediator.md)). This token is used for authentication for submission to the Vermittlungsdienst.
<br><br>
Before a notification is sent to the mediation system, it is advisable to send this notification to the eForms-DE validation service (external validator). This allows you to check that the eForms-DE document is valid before it is submitted. Upon submission, the Vermittlungsdienst will also validate the eForms according to its version (eForms-EU 0.1.1, 1.0, 1.5 & eForms-DE 1.0.0, 1.0.1) and accept or reject it.
<br><br>
If the submission is successful, the announcement is processed further. Depending on whether it is a below-threshold or above-threshold eForms document, notices are either forwarded directly to the BKMS (below-threshold) or to the eSender Hub (above-threshold) - see [above- or below-threshold award](/documentation/Upper-or_lower-threshold-award.md). In the eSender Hub, a transformation to eForms-EU takes place when eForms-DE is submitted. You can find out which eForms versions the individual components support in [eForms Support](/documentation/eForms_support.md).
<br><br>
After successful transformation into the EU version of eForms that matches the DE version, the notification is forwarded to TED. The response from TED (successful submission or rejection) is saved and triggers a corresponding status change. The time of this status change is also saved so that the time of the submission is persisted. TED then retrieves the associated validation report, saves it and extracts any errors or warnings (e.g. lawfulness warnings).
<br><br>
If the submission is successful, the exact time of submission is recorded in order to calculate the 48-hour deadline for national publication. If no warnings exist, the announcement is forwarded to the BKMS at the latest after the 48-hour period has expired. If lawfulness warnings exist, the announcement is forwarded to the BKMS after 5 days at the latest to await the manual check by TED. If an announcement is published on TED before this, it is forwarded to the BKMS immediately. The time of publication is also saved.
<br><br>
During the entire process, status changes, e.g. triggered by feedback from TED, as well as errors or warnings that have occurred are saved internally. Relevant status information can be queried at any time by FVH via the Vermittlungsdienst. Details on status messages and errors can be found under [Status information](documentation\Status_information.md).
<br><br>

![Workflow diagram](/documentation/images/workflow_2.png)


