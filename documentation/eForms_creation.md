### Datenservice Öffentlicher Einkauf
[Inhaltsverzeichnis](/documentation/documentation.md)
<br>

# Hinweise zum Erstellen von eForms-DE-Dokumenten

Bei der eForms-Dokumentenerstellung gilt es, einige Regeln zu bestimmten Feldern zu beachten.

## eSender-Informationen
>**eForms-DE-spezifisch**

Feld: *ganzer Abschnitt ```<efac:Organization>```*

Der Datenservice Öffentlicher Einkauf übernimmt die Rolle des eSenders für alle an TED zu übermittelnden oberschwelligen Bekanntmachungen. Für die Organisationen darf deshalb der Typ „ted-esen“ NICHT in den Bekanntmachungen verwendet werden, da diese Angabe automatisch vom eSender-Hub eingefügt wird.
Wenn eine Bekanntmachung erstellt und eine Organisation angegeben wird, muss für jede Organisation definiert werden, welche Rolle diese im Rahmen der Bekanntmachung spielt. Die Rollen sind definiert in der EU-Codeliste: https://github.com/OP-TED/eForms-SDK<br>
Ein Wert in der EU-Codeliste ist „ted-esen“. Dieser Wert darf in Deutschland nicht verwendet werden. 
