# Go-live ticker

Here you will find current information in preparation for 10/25/2023 and continuous updates between 10/25-27/2023.

## Known issues
If any issues arise during the go-live, you will find updated information in this section.

Unfortunately, due to a supra-regional network disruption, there were technical issues with the accessibility of our data center between 3:31pm and 4:03pm on 10/25/2023. Unfortunately, this also affected the posting of announcements and the retrieval of information.  
Please check your postings as the services are now available again.


## ! Important notes for the creation of eForms !
To ensure a smooth posting process, please always keep the following aspects in mind:

- The **BT-05 Notice Dispatch date** **(IssueDate)** field must be between yesterday and tomorrow at the time of dispatch to the switching service, otherwise TED will reject the notice. This is NOT currently checked in the switching service as it is a new dynamic rule from TED
- The **ted-esen** role MUST NOT be used in announcements, either as org-role or org-sub-role. This leads to problems in the transformation, because always automatically the procurement office is set as ted-esen

- The field **Preferred Publication Date BT-738 (RequestedPublicationDate)** can be set to the same time as the Notice Dispatch date or up to 2 days after the Notice Dispatch date according to the German standard. Please make sure to specify the same time zone for both values, otherwise TED may reject the request in some cases.
- The filling of the field **BT-165 Winner Size (Winner Size)** is currently not checked by the German rules. Please make sure that this field is filled correctly for the following Notice Types: '25', '26', '27', '28', '29', '30', '31', '32', 'E4', '33', '34', '35', '36' & '37'.
- Currently there is a bug with TED that based on restrictive rules on CPV codes **grant recipients** can only bid construction services, but <u>no supplies or services</u>. TED is still working to address this.
CPV codes are interpreted as follows:
    - Supply Services: Main CPV code from divisions 0 through 44 or 48.
    - Services: Main CPV code from divisions 49 through 98.
    - Construction work: Main CPV code from division 45
    
If you are affected by this (notice fails due to rule **BR-BT-00262-0211**), please immediately contact our support support-oeffentlichevergabe@bdr.de for specific assistance
- For the filling of the **BT-501 identification number (of the organization)**, please refer to the notes on, among other things, the routing ID in our FAQ: https://github.com/EFA-FHB/ozg-vermittlungsdienst-doku/blob/main/faq.md#identifikationsnummer-organisation-bt-501


### Notes for manufacturers of specialized procedures
- We are currently seeing an increasing number of rejections during submission based on incorrect syntax of the email for the "authorEmail" specification. Please ensure that a valid email with correct syntax is supplied in this field when submitting to the switching service for each announcement. If the email is not correct, the following error message will appear: "NOTICE_METADATA_INVALID - Required data is missing or the data entered does not match the schema". We validate emails using the following regex expression: \b[A-Za-z0-9._%+-]+@[A-Za-z0-9.-]+(?:_[A-Za-z0-9.-])*\.[A-Za-z]{2,5}\b

## Upcoming maintenance windows

| environment | system | date | time | comment |
|-------------|---------------------|------------|-------------------|---------------------|
| - | - | - | - | - |

## Known bugs

| system | present since | expected fix | bug |
|--------------|--------------------------|-----------------------------|---------------------|
| - | - | - | - |


## Notes

On 27/09/2023, the API key for submission to TED was adjusted. Because of this, status information for announcements submitted to staging or preview before this date will no longer be requested from TED. This is a one-time adjustment and will not occur again in the future.


## Past maintenance windows or disruptions

| Environment | System | Date | Time | Comment |
|-------------|---------------------|------------|-------------------|---------------------|
|BKMS Production | BKMS | 27.10 | 27.10. 13:10 - 14:35 CEST | Online search function was not available |
| DÖE Production + Staging | all services except BKMS | 10/25/2023 | 15:31 - 16:03 CEST | Data center unavailable |
| DöE Production + Staging | all services except BKMS |23.10.2023 - 24.10.2023 | 17:00 - 09:00 CEST | Unavailable due to infrastructure problems |
| DöE Production + Staging | all Services except BKMS | 20.10.2023 | 10:00 - 13:00 CEST | Deployment for performance improvements |
| DöE Production + Staging | all services except BKMS | 10.10.2023 | 09:00 - 12:00 CEST | Data Center Maintenance |
| TED Preview | TED Apps for eForms | 10.10.2023 | 07:00 - 10:00 CEST | Announced by TED |
| TED Production | TED Apps for eForms | 11.10.2023 | 07:00 - 10:00 CEST | Announced by TED |
| TED Production + Preview | TED Developer Portal, TED Apps for eForms | 02.10.2023 | 07:00 - 09:00 CEST | Announced by TED |
| TED Production | TED Apps for eForms | 27.09.2023 | 07:00 - 09:00 CEST | Announced by TED |
| TED Production | Operator Service | 14.09.2023| 08:00 - 09:30 CEST | temporarily unavailable |
| TED Production| TED Apps for eForms | 30.08.2023 | 18:00-22:00 CEST | Announced by TED |
| TED Production| TED Apps for eForms | 30.08.2023 | 18:00-22:00 CEST | Announced by TED |
| TED Preview | TED Apps for eForms | 28.08.2023 | 07:00-11:00 CEST | Announced by TED |
| TED Preview | TED Apps for eForms | 24.08.2023 | 07:00-08:00 CEST | Announced by TED |
| TED Production | TED Apps for eForms | 23.08.2023 | 07:00-08:00 CEST | Announced by TED |
