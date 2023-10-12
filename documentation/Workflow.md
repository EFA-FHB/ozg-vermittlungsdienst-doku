### EfA-Umsetzungsprojekt "Zugang zur öffentlichen Vergabe"
## Dokumentation Vermittlungsdienst
[Inhaltsverzeichnis](/documentation/documentation.md)
<br>

# Workflow einer Bekanntmachung im Datenservice öffentlicher Einkauf

Im folgenden Diagramm ist der generelle Workflow einer Bekanntmachung beschrieben.
<br><br>
Der zentrale Punkt zum Einliefern von Bekanntmachungen und Abfragen von Statusinformationen für Fachverfahrenshersteller (FVH) ist der Vermittlungsdienst. Bevor in den Vermittlungsdienst eingeliefert werden kann, muss sich jede Vergabeplattform einen Account in Keycloak erstellen lassen und sich im Vermittlungsdienst ein Token generieren. Das Account kann im Self-Service Portal beantragt sein (siehe [Connection to Mediator](documentation/Connection_to_mediator.md)). Mit diesem Token erfolgt die Authentifikation zum Einsenden in den Vermittlungsdienst.
<br><br>
Bevor eine Bekanntmachung an das Vermittlungssystem gesendet wird, ist es empfehlenswert diese Bekanntmachung an den eForms-DE Validierungsservice zu schicken (Externer Validator). So kann bereits vor Einlieferung geprüft werden, dass das eForms-DE Dokument valide ist. Beim Einsenden wird der Vermittlungsdienst das eForms entsprechend seiner Version ebenfalls validieren (eForms-EU 0.1.1, 1.0, 1.5 & eForms-DE 1.0.0, 1.0.1) und diese annehmen oder ablehnen. 
<br><br>
Bei erfolgreicher Einlieferung wird die Bekanntmachung weiter prozessiert. Abhängig davon, ob es sich um ein unterschwellig oder oberschwelliges eForms-Dokument handelt, werden Bekanntmachungen entweder direkt an den BKMS (unterschwellig) oder an den eSender-Hub (oberschwellig) weitergeleitet - siehe [Ober- oder Unterschwellenvergabe](/documentation/Ober-oder_unterschwellenvergabe.md). Im eSender-Hub erfolgt bei Einlieferung von eForms-DE eine Transformation in eForms-EU. Welche eForms Versionen die einzelnen Komponenten unterstützen können Sie [eForms Support](/documentation/eForms_support.md) nachlesen.
<br><br>
Nach erfolgreicher Transformation in die zur DE-Version passende EU-Version des eForms wird die Bekanntmachung an TED weitergeleitet. Die Rückmeldung von TED (Erfolgreiche Einlieferung oder Ablehnung) wird gespeichert und triggert einen entsprechenden Statuswechsel. Auch der Zeitpunkt dieses Statuswechsels wird gespeichert, sodass der Zeitpunkt der Einlieferung persistiert ist. Im Anschluss wird von TED der zugehörige Validierungsreport abgerufen gespeichert und eventuelle Fehler oder Warnungen (zum Beispiel Lawfulness warnings) extrahiert. 
<br><br>
Bei erfolgreicher Einlieferung wird der exakte Zeitpunkt der Einlieferung erfasst, um die 48h-Frist für eine nationale Veröffentlichung zu berechnen. Wenn keine Warnungen existieren wird spätestens nach Ablauf der 48h die Bekanntmachung an den BKMS weitergeleitet. Sollten Lawfulness warnings existieren, wird die Bekanntmachung spätestens nach 5 Tagen an den BKMS weitergeleitet, um die manuelle Prüfung von TED abzuwarten. Sollte eine Bekanntmachung vorher bei TED veröffentlicht werden, erfolgt sofort eine Weiterleitung an den BKMS. Der veröffentlichungszeitpunkt wird ebenfalls gespeichert.
<br><br>
Während des gesamten Prozesses werden Statusänderungen z.B. ausgelöst durch eine Rückmeldung von TED sowie aufgetretene Fehler oder Warnungen intern gespeichert. Relevante Statusinformationen können jederzeit durch die FVH über den Vermittlungsdienst abgefragt werden. Details zu Statusmeldungen und Fehlern finden sie unter [Statusinformationen](documentation\Status_information.md).
<br><br>

![Workflow Diagramm](/documentation/images/workflow_2.png)


