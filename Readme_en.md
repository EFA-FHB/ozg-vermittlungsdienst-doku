### EfA implementation project "Access to public procurement"
# Mediation service

>**Go-Live 25.10.** <br>
> Important notes and known errors for productive submission can be found under [Maintenance](/maintenance.md)!

You want to support companies and public administration in reducing bureaucratic hurdles in the procurement process
and strengthen competition for public contracts? Then why not link your procurement platform to the procurement platform provided by the Free
Hanseatic City of Bremen. The service is part of the Bremen EfA project "Access to public procurement",
which is being implemented in the context of the "Public Procurement Data Service" project - a cooperation project between the federal government and the state of Bremen.
With the help of the mediation service, awarding systems can transmit notices to the notice service and TED and thus
make nationwide tenders easily accessible to companies. You can find out how to connect to the switching service in the [Documentation](/documentation/Documentation.md).
<br><br>
This repository contains the following documents to support a connection to the switching service:

- [Documentation switching service](/documentation/Documentation.md)
- FAQ](/faq.md)
- Release Notes](/Releases.md)
- Known maintenance windows](/maintenance.md)
- Events](/events.md)
<br>

## The tasks of the switching service
- Validation of all incoming announcements according to
Schema and Schematron rules and checking whether
announcements have already been published in the announcement service
have already been published
- Transmission of subliminal notices to
the announcement service
- Transmission of above-threshold notices via
the eSender Hub to TED and to the
announcement service
<br>

## Data service public procurement system architecture
![System architecture](/images/Datenservice_Oeffentlicher_Einkauf-Systemarchitektur.png)
