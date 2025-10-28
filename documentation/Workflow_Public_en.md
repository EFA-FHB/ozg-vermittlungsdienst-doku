### Data service public purchasing
<br>

# Workflow of an announcement in the public procurement data service

The following diagram describes the general workflow of an announcement.
<br><br>
The central point for submitting notices and querying status information for specialist procedure manufacturers is the Vermittlungsdienst. Before it can be submitted to the Vermittlungsdienst, each awarding platform must have an account created in Keycloak and generate a token in the Vermittlungsdienst. The account can be applied for in the self-service portal. This token is used for authentication for submission to the Vermittlungsdienst.
<br><br>
Before sending an announcement to the Vermittlungsdienst, it can optionally be sent to the eForms-DE validation service (external validator). This allows you to check whether the eForms-DE document is valid before submitting it. Upon submission, the Vermittlungsdienst will also validate the eForms document according to its version and accept or reject it.
<br><br>
If the submission is successful, the notification is processed further. Depending on whether it is a below-threshold or above-threshold eForms document, announcements are either forwarded directly to the announcement service (below-threshold) or to the eSender Hub (above-threshold). In the eSender Hub, a transformation to eForms-EU takes place when eForms-DE is submitted.
<br><br>
After successful transformation into the EU version of the eForms that matches the DE version, the notification is forwarded to TED. The feedback from TED (successful submission or rejection) is saved and triggers a corresponding status change. The time of this status change is also saved so that the time of the submission persists. TED then retrieves and saves the corresponding validation report. Any errors or warnings (e.g. lawfulness warnings) are extracted.
<br><br>
If the submission is successful, the exact time of submission is recorded in order to calculate the 48-hour deadline for national publication. Forms E1 to E4 are excluded - these are transmitted directly to the announcement service without the usual delay of 48 hours. If no warnings exist, the announcement will be forwarded to the announcement service after the 48-hour period at the latest. If lawfulness warnings exist, the announcement will be forwarded to the announcement service after five days at the latest to await the results of TED's manual check. If an announcement is published on TED before the end of these five days, it is immediately forwarded to the announcement service. The time of publication is also saved.
<br><br>
Throughout the entire process, status changes, e.g. triggered by feedback from TED, and any errors or warnings that occur are saved internally. Relevant status information can be queried at any time by FVH via the Vermittlungsdienst.
<br><br>

![Workflow diagram](/documentation/images/workflow_2.png)





