### EfA Implementation Project "Access to Public Procurement".
# Mediation service

>**Go-Live 25.10.** <br>
> Important information about the Go-Live on 25.10. can be found under [Maintenance](/Maintenance.md)!

You want to support companies and public administration in reducing bureaucratic hurdles in the procurement process
and strengthen competition for public contracts? Then you are welcome to link your procurement platform to the mediation service provided by the Free
Hanseatic City of Bremen's mediation service. The service is part of the Bremen EfA project "Access to Public Procurement",
which is implemented in the project context "Data Service Public Procurement" - a cooperation project of the Federal Government and the State of Bremen.
With the help of the mediation service, procurement systems can transmit notices to the announcement service and TED, thus making it
make nationwide solicitations easily accessible to businesses. To learn how to connect to the switching service, see the [documentation](/documentation/Documentation.md).
<br><br>
The following documents are included in this repository to support a connection to the Mediation Service:

- [Documentation Switching Service](/documentation/Documentation.md)
- FAQ](/faq.md)
- [Release Notes](/releases.md)
- [Known maintenance windows](/maintenance.md)
- Events](/events.md)
<br>

## The tasks of the switchboard service
- Validation of all incoming announcements according to
Schema as well as Schematron rules and checking if any
announcements have already been published in the
have been published
- Transmission of subthreshold announcements to
the announcement service
- Transmission of upper-threshold announcements via the
the eSender hub to TED and to the
Announcement Service
<br>

## Data service public purchasing system architecture
![System Architecture](/images/data_service_public_purchasing_system_architecture.png)
