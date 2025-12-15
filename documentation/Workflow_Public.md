

# Workflow einer Bekanntmachung im Datenservice Öffentlicher Einkauf

Im folgenden Diagramm ist der generelle Workflow einer Bekanntmachung beschrieben.
<br><br>
Der zentrale Punkt zum Einliefern von Bekanntmachungen und Abfragen von Statusinformationen für Fachverfahrenshersteller ist der Vermittlungsdienst. Bevor in den Vermittlungsdienst eingeliefert werden kann, muss sich jede Vergabeplattform einen Account in Keycloak erstellen lassen und sich im Vermittlungsdienst einen Token generieren. Der Account kann im Self-Service-Portal beantragt werden. Mit diesem Token erfolgt die Authentifikation zum Einsenden in den Vermittlungsdienst.
<br><br>
Vor dem Versand einer Bekanntmachung an den Vermittlungsdienst kann diese optional an den eForms-DE-Validierungsservice (externen Validator) gesendet werden. So kann bereits vor Einlieferung geprüft werden, ob das eForms-DE-Dokument valide ist. Beim Einsenden wird der Vermittlungsdienst das eForms-Dokument entsprechend seiner Version ebenfalls validieren und dieses annehmen oder ablehnen. 
<br><br>
Bei erfolgreicher Einlieferung wird die Bekanntmachung weiter prozessiert. Abhängig davon, ob es sich um ein eForms-Dokument zu einer Bekanntmachung oberhalb oder unterhalb der EU-Schwellenwerte handelt, werden Bekanntmachungen entweder direkt an den Bekanntmachungsservice (unterhalb der EU-Schwellenwertes) oder an den eSender-Hub (oberhalb der EU-Schwellenwerte) weitergeleitet. Einlieferungen im Format des Standards eForms-DE werden im eSender-HUB in das europäische Format eForms-EU transformiert.
<br><br>
Nach erfolgreicher Transformation in die zur DE-Version passende EU-Version des eForms wird die Bekanntmachung an TED weitergeleitet. Die Rückmeldung von TED (erfolgreiche Einlieferung oder Ablehnung) wird gespeichert und triggert einen entsprechenden Statuswechsel. Auch der Zeitpunkt dieses Statuswechsels wird gespeichert, sodass der Zeitpunkt der Einlieferung persistiert. Im Anschluss wird von TED der zugehörige Validierungsreport abgerufen und gespeichert. Eventuelle Fehler oder Warnungen (zum Beispiel Lawfulness Warnings) werden extrahiert.
<br><br>
Bei erfolgreicher Einlieferung wird der exakte Zeitpunkt der Einlieferung erfasst, um die 48-Stunden-Frist gemäß §40 VgV für eine nationale Veröffentlichung zu berechnen. Ausgenommen sind die Formulare E1 bis E4, die ohne Verzögerung an den Bekanntmachungsservice übermittelt werden. Die Weiterleitung erfolgt, wenn TED die dortige Publikation bestätigt hat, spätestens jedoch nach 48 Stunden, wenn zwischenzeitlich weder eine Ablehnung noch eine „Lawfulness Warning“ (Infragestellung der Rechtmäßigkeit) zurückgemeldet wird. Meldet TED eine „Lawfulness Warning“ zurück, erhöht sich die maximale Wartefrist von 48 Stunden auf 5 Tage, um die Ergebnisse der manuellen Prüfung im Amt für Veröffentlichungen der EU abzuwarten. Der Veröffentlichungszeitpunkt wird ebenfalls gespeichert.
<br><br>
Während des gesamten Prozesses werden Statusänderungen z. B. ausgelöst durch eine Rückmeldung von TED sowie aufgetretene Fehler oder Warnungen intern gespeichert. Relevante Statusinformationen können jederzeit durch die Fachverfahrenshersteller über den Vermittlungsdienst abgefragt werden.
<br><br>

![Workflow Diagramm](/documentation/images/workflow_2.png)





