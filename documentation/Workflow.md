### EfA-Umsetzungsprojekt "Zugang zur öffentlichen Vergabe"
## Dokumentation Vermittlungsdienst
[Startseite](/documentation/documentation.md)
<br><br>

# Workflow einer Bekanntmachung im Vermittlungsdienst

Im folgenden Diagramm ist der generelle Workflow einer Bekanntmachung beschrieben.
<br><br>
Der zentrale Punkt zum Einliefern von Bekanntmachungen und Abfragen von Statusinformationen für Fachverfahrenshersteller (FVH) ist der Mediator. Bevor in den Mediator eingeliefert werden kann, muss ein Account in Keycloak erstellt und dort ein Token generiert werden. Mit diesem Token erfolgt die Authentifikation zum Einsenden in den Mediator.
<br><br>
Bevor eine Bekanntmachung an das Vermittlungssystem gesendet wird, ist es empfehlenswert diese Bekanntmachung an den eForms-DE Validierungsservice zu schicken. So kann bereits vor Einlieferung geprüft werden, dass das eForms-DE valide ist. Beim Einsenden wird der Mediator das eForms entsprechend seiner Version ebenfalls validieren (eForms-EU 0.1.1, 1.0, 1.5 & eForms-DE 1.0.0, 1.0.1) und diese annehmen oder ablehnen. 
<br><br>
Bei erfolgreicher Einlieferung wir die Bekanntmachung weiter prozessiert. Abhängig davon, ob es sich um ein unterschwellig oder oberschwelliges eForms-Dokument handelt, werden Bekanntmachungen entweder direkt an den BKMS (unterschwellig) oder an den eSender (oberschwellig) weitergeleitet. Der BKMS akzeptiert derzeit (auf der Umgebung Alpha im Rahmen des eSender Preview Release 31.3.23) die Versionen eForms-EU 0.1.1 und 1.0. Im eSender erfolgt bei Einlieferung von eForms-DE 1.0.0 eine Transformation in eForms-EU 1.5. Hierbei ist zu beachten, dass im eSender derzeit (Stand eSender Preview Release 31.3.23) nur eForms-DE 1.0.0 unterstützt wird, nicht eForms-DE 1.0.1, da das codetable mapping noch nicht final ist.
<br><br>
Nach erfolgreicher Transformation in eForms-EU 1.5 wird die Bekanntmachung an TED (Umgebung Preview) weitergeleitet. Die Rückmeldung von TED (Erfolgreiche Einlieferung oder Ablehnung) wird gespeichert und triggert einen entsprechenden Statuswechsel. Im Anschluss wird von TED der zugehörige Validierungsreport abgefragt, gespeichert und eventuelle Fehler oder Warnungen (zum Beispiel Lawfulness warnings) extrahiert. 
<br><br>
Bei erfolgreicher Einlieferung wird der exakte Zeitpunkt der Einlieferung erfasst, um die 48h-Frist für eine nationale Veröffentlichung zu berechnen. Wenn keine Warnungen existieren wird nach Ablauf der 48h die Bekanntmachung an den BKMS weitergeleitet. Sollten Lawfulness Warnungen existieren, wird die Bekanntmachung erst nach 5 Tagen an den BKMS weitergeleitet, um die manuelle Prüfung von TED abzuwarten. 
<br><br>
Aktuell unterstützt der BKMS Bekanntmachungen mit Version eForms-DE 1.0.0 und eForms-EU 1.5 nicht, sodass der DöE Status für oberschwellige Bekanntmachungen immer "Pending" sein wird (Stand eSender Preview Release 31.3.23). Hierzu wird vom BKMS intern eine spezielle HTTP 400 Fehlermeldung ausgegeben (z.B. Unsupported eForms version: "eforms-de-1.0"), um zu verdeutlichen, dass die Ablehnung nur durch die (noch) nicht unterstützte Version verursacht wird. 
<br><br>
Während des gesamten Prozesses werden Statusänderungen z.B. ausgelöst durch eine Rückmeldung von TED sowie aufgetretene Fehler oder Warnungen intern gespeichert. Relevante Statusinformationen können jederzeit durch die FVH vom Mediator abgefragt werden (Siehe Statusliste und Diagramme).
<br><br>

![Workflow Diagramm](/documentation/images/workflow_diagramm.png)


