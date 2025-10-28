### Data service public procurement
<br>

# Workflow of an announcement in the public procurement data service

The following diagram describes the general workflow of an announcement.
<br><br>
The central point for submitting notices and querying status information for specialized procedure manufacturers (FVH) is the Vermittlungsdienst. Before being able to submit to the Vermittlungsdienst, each awarding platform must have an account created in Keycloak and generate a token in the Vermittlungsdienst. The account can be requested in the self-service portal. This token is used for authentication for submission to the Vermittlungsdienst.
<br><br>
Before a notice is sent to the intermediary service, it is optional to send it beforehand to the eForms-DE Validation Service (external validator). This allows you to check that the eForms-DE document is valid before submitting it. Upon submission, the Vermittlungsdienst will also validate the eForms according to its version and accept or reject it.
<br><br>
If the submission is successful, the notification is processed further. Depending on whether it is a subthreshold or upper-threshold eForms document, notices are either forwarded directly to the BKMS (subthreshold) or to the eSender Hub (upper-threshold). In the eSender Hub, a transformation to eForms-EU takes place when eForms-DE is submitted.
<br><br>
After successful transformation into the EU version of the eForms that matches the DE version, the notification is forwarded to TED. The feedback from TED (successful submission or rejection) is saved and triggers a corresponding status change. The time of this status change is also saved so that the time of the submission persists. TED then retrieves and saves the associated validation report and extracts any errors or warnings (e.g. lawfulness warnings).
<br><br>
If the submission is successful, the exact time of submission is recorded in order to calculate the 48-hour deadline for national publication. Forms E1 to E4 are excluded - these are transmitted directly to the publication service without the usual delay of 48 hours. If no warnings exist, the announcement will be forwarded to the BKMS after the 48-hour period at the latest. If lawfulness warnings exist, the announcement will be forwarded to the BKMS after 5 days at the latest to await the manual check by TED. If an announcement is published on TED before this, it is forwarded to the BKMS immediately. The time of publication is also saved.
<br><br>
During the entire process, status changes, e.g. triggered by feedback from TED, as well as errors or warnings that have occurred are saved internally. Relevant status information can be queried at any time by FVH via the Vermittlungsdienst.
<br><br>

![Workflow diagram](/documentation/images/workflow_2.png)





