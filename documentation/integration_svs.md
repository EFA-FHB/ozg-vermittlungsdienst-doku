---
title: SVS Integration
---

[Inhaltsverzeichnis](/documentation/documentation.md)
<br>

# Service Vergabestatistik Integration

Der Service Vergabestatistik (SVS) ist eine Komponente des Datenservice Öffentlicher Einkauf (DÖE). Mittels des SVS können Statistikmeldungen basierend auf eForms-Vergabebekanntmachungen automatisch erstellt und über den DÖE an das Statistische Bundesamt übertragen werden.

![svs-integration](/documentation/images/svs_integration.png)

Die Nutzung des Services ist freiwillig. Alternativ zum SVS können Sie weiterhin die bisherigen Meldewege nutzen.

Voraussetzung für die Nutzung des Services ist die Einlieferung von Bekanntmachungen gemäß dem gültigen Regelwerk zu SDK 1.14 (oder neuer).

Der Service wird automatisch genutzt, wenn die an den Vermittlungsdienst des DÖE übermittelte Vergabebekanntmachung (CAN) im Feld `BT-001-DEX-NoticeResult` eine gültige Berichtseinheits-ID enthält. Das Regelwerk des SDKs stellt dann sicher, dass alle fachlichen Informationen zur Erfüllung der Meldepflicht in der Bekanntmachung enthalten sind. 

Nach der erfolgreichen Einlieferung der Bekanntmachung an den Vermittlungsdienst wird automatisch eine Vergabestatistikmeldung erzeugt und zum Ende der Meldefrist an das Statistische Bundesamt übermittelt.

### Informationen zum Bearbeitungsstatus im SVS

Im Self-Service-Portal des Datenservice Öffentlicher Einkauf kann für registrierte Nutzer (üblicherweise Support der Vergabeplattformbetreiber) neben des Bearbeitungsstatus zur Publikation auf TED und Bekanntmachungsservice auch der Bearbeitungsstatus bzgl. der Statistikmeldung eingesehen werden.

Darüber hinaus kann der Bearbeitungsstatus auch über die aktuelle Version (1.3.8 oder neuer) des Vermitlungsdienst-Endpunkts: `/v1/notices/status` abgerufen werden. Weitere Informationen finden Sie unter https://ozg-vermittlungsdienst.de/.

### Vorschaufunktion und Anzeige der übermittelten Statistikmeldung

Für eine im eForms-Format verfügbare Vergabebekanntmachung (CAN) kann über den Endpunkt `/preview` eine Vorschau zur Statistikmeldung angezeigt werden (ohne dass diese weitergeleitet wird). Weitere Informationen finden Sie unter https://svs.datenservice-oeffentlicher-einkauf.de/api-docs/swagger-ui/index.html. 
Zu einer bereits an den Datenservice Öffentlicher Einkauf übertragenen Vergabebekanntmachung (CAN) kann die zugehörige Statistikmeldung angezeigt werden. Dies erfolgt über den ReportLink, der in einer Statusabfrage an den Vermittlungsdienst (siehe “Informationen zum Bearbeitungsstatus im SVS) zurückgegeben wird. Dieser nutzt den Endpunkt `/notice/view/{token}`. Weitere Informationen finden Sie unter https://svs.datenservice-oeffentlicher-einkauf.de/api-docs/swagger-ui/index.html.