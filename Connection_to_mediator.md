**EfA-Umsetzungsprojekt "Zugang zur öffentlichen Vergabe"**
### Dokumentation Vermittlungsdienst
[Startseite](Readme.md)
<br><br>

# Anbindung an den Vermittlungsdienst
Es gibt zwei Möglichkeiten Bekanntmachungen an den Vermittlungsdienst zu übermitteln, per REST API oder per PEEPOL (in der Umsetzung).
<br><br>

## Anbindung per REST API
Der Vermittlungsdienst stellt eine REST API zur Verfügung, die von jeder Vergabeplattform genutzt werden kann, um Bekanntmachungen an den Vermittlungsdienst zu übermitteln.
<br><br>

## Anbindung per PEPPOL (in der Umsetzung)
Es ist zukünftig möglich Bekanntmachungen auch über das eDelivery Network PEPPOL an den Vermittlungsdienst zu übermitteln. Details und weitere Informationen folgen. 
<br><br>

## Beantragen eines Zugangs duch einen FVH
Ein Vertreter des FVH beantragt die Einrichtung eines neuen Benutzer bei dem zuständigen Organisationsadministrator per E-Mail oeffentliche-vergabe@nortal.com. Es muss pro Portal ein Benutzer angelegt werden.<br>
In der E-Mail müssen folgende Angaben enthalten sein:

- E-Mail-Adresse unter der der Benutzer angelegt werden soll
- URL der Vergabeplattform
- Vor- und Nachname sowie die E-Mail-Adresse des Vertreters des FVH
- Name des FVH

Nach der Erstellung des Benutzer wird zur Überprüfung an die angegebene Benutzer E-Mail-Adresse eine Bestätigungs-E-Mail versendet. Außerdem enthält die E-Mail einen Link zur Erstellung des Passworts.
<br><br>
Der Link ist 24 Stunden lang gültig.<br>
Das Passwort muss aus mindestens 8 Zeichen bestehen, 1 Großbuchstaben und 1 Zahl enthalten.<br>
Das Passwort muss in der FVH-Software hinterlegt werden um sicher zu gehen, dass die Verbindung mit dem Vermittlungsdienst funktioniert.
<br><br>

## Wie setzt man ein Benutzer Passwort zurück?
1. Anmeldeseite aufrufen<br>
Testumgebung. https://keycloak-preview.efa-fhb.apps-int.nortal.com/realms/ozg-vermittlungsdienst/account/#/ → Auf 'Anmelden' klicken<br>
![Anmeldeseite aufrufen](images/kc_anmeldeseite.png)
2. Auf 'Passwort vergessen?' klicken<br>
![Auf Passwort vergessen](images/kc_login.png)
3. E-Mail-Adresse eintragen und auf 'Absenden' klicken<br>
![E-Mail eintragen](images/kc_passwort_vergessen.png)
4. Die Meldung 'Sie sollten in Kürze eine E-Mail mit weiteren Instruktionen erhalten' wir angezeigt.<br>
![Meldung](images/kc_nachricht_best%C3%A4tigungsemail.png)
5. Überprüfen der E-Mails: Ein Link zum Zurücksetzen der Anmeldeinformationen ist in der E-Mail erhalten.<br>
![Bestätigungs-E-Mail](images/e-mail_passwort_zuruecksetzen.png)
6. Auf 'Link zum Zurücksetzen von Anmeldeinformationen' klicken.
7. Der Benutzer wird auf die Seite 'Passwort aktualisieren' umgeleitet.<br>
![PAsswort aktualisieren](images/kc_passwort_aktualisieren.png)
8. Neues Passwort eintragen und bestätigen und auf 'Absenden' klicken.<br>
Das Passwort muss aus mindestens 8 Zeichen bestehen, 1 Großbuchstaben und 1 Zahl enthalten.
9. Das Passwort muss in der FVH-Software hinterlegt werden um sicher zu gehen, dass die Verbindung mit dem Vermittlungsdienst funktioniert.