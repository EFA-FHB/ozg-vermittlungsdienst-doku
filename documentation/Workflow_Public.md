### Datenservice Öffentlicher Einkauf
<br>

# Workflow einer Bekanntmachung im Datenservice Öffentlicher Einkauf

Im folgenden Diagramm ist der generelle Workflow einer Bekanntmachung beschrieben.
<br><br>
Der zentrale Punkt zum Einliefern von Bekanntmachungen und Abfragen von Statusinformationen für Fachverfahrenshersteller ist der Vermittlungsdienst. Bevor in den Vermittlungsdienst eingeliefert werden kann, muss sich jede Vergabeplattform einen Account in Keycloak erstellen lassen und sich im Vermittlungsdienst einen Token generieren. Der Account kann im Self-Service-Portal beantragt werden. Mit diesem Token erfolgt die Authentifikation zum Einsenden in den Vermittlungsdienst.
<br><br>
Vor dem Versand einer Bekanntmachung an den Vermittlungsdienst kann diese optional an den eForms-DE-Validierungsservice (externen Validator) gesendet werden. So kann bereits vor Einlieferung geprüft werden, ob das eForms-DE-Dokument valide ist. Beim Einsenden wird der Vermittlungsdienst das eForms-Dokument entsprechend seiner Version ebenfalls validieren und dieses annehmen oder ablehnen. 
<br><br>
Bei erfolgreicher Einlieferung wird die Bekanntmachung weiter prozessiert. Abhängig davon, ob es sich um ein eForms-Dokument zu einer Bekanntmachung oberhalb oder unterhalb der EU-Schwellenwerte handelt, werden Bekanntmachungen entweder direkt an den Bekanntmachungsservice (unterhalb der EU-Schwellenwertes) oder an den eSender-Hub (oberhalb der EU-Schwellenwerte) weitergeleitet. Im eSender-Hub erfolgt bei Einlieferung von Bekanntmachungen im Format eForms-DE eine Transformation in das Format eForms-EU.
<br><br>
Nach erfolgreicher Transformation in die zur DE-Version passende EU-Version des eForms wird die Bekanntmachung an TED weitergeleitet. Die Rückmeldung von TED (erfolgreiche Einlieferung oder Ablehnung) wird gespeichert und triggert einen entsprechenden Statuswechsel. Auch der Zeitpunkt dieses Statuswechsels wird gespeichert, sodass der Zeitpunkt der Einlieferung persistiert. Im Anschluss wird von TED der zugehörige Validierungsreport abgerufen und gespeichert. Eventuelle Fehler oder Warnungen (zum Beispiel Lawfulness Warnings) werden extrahiert.
<br><br>
Bei erfolgreicher Einlieferung wird der exakte Zeitpunkt der Einlieferung erfasst, um die 48-Stunden-Frist für eine nationale Veröffentlichung zu berechnen. Ausgenommen sind die Formulare E1 bis E4 – diese werden ohne die übliche Verzögerung von 48 Stunden unmittelbar an den Bekanntmachungsservice übermittelt. Wenn keine Warnungen existieren wird spätestens nach Ablauf der 48 Stunden die Bekanntmachung an den Bekanntmachungsservice weitergeleitet. Sollten Lawfulness Warnings existieren, wird die Bekanntmachung spätestens nach fünf Tagen an den Bekanntmachungsservice weitergeleitet, um die Ergebnisse der manuellen Prüfung von TED abzuwarten. Sollte eine Bekanntmachung vor Ablauf dieser fünf Tage bei TED veröffentlicht werden, erfolgt sofort eine Weiterleitung an den Bekanntmachungsservice. Der Veröffentlichungszeitpunkt wird ebenfalls gespeichert.
<br><br>
Während des gesamten Prozesses werden Statusänderungen z. B. ausgelöst durch eine Rückmeldung von TED sowie aufgetretene Fehler oder Warnungen intern gespeichert. Relevante Statusinformationen können jederzeit durch die FVH über den Vermittlungsdienst abgefragt werden.
<br><br>

![Workflow Diagramm](/documentation/images/workflow_2.png)





