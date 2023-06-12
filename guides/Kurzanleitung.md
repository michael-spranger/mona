# MoNA - Installation, Einrichtung und Inbetriebnahme
---------------------------------------------------
Letzte Anpassung dieser Anleitung: 01.06.2021, gültig für MoNA-Release ab 3.0.0

## Installation
------------
1. Herunterladen der aktuellen Version von MoNA (aus Moodle).
2. Entpacken des heruntergeladenen Archivs.
3. Verschieben des Installationsverzeichnisses auf ein Laufwerk ohne rechtliche Einschränkungen.
4. Für Windows-Nutzer: Hinzufügen des MoNA-Installationsverzeichnisses zu den Ausnahmen im Windows Defender (siehe unterer Abschnitt "Anpassen des Windows Defender").
5. Kopieren der Lizenzdatei in das Unterverzeichnis "./configurations".
6. Start mit Doppelklick auf "mona.exe".

Auf dem Startbildschirm wird Ihnen die Gültigkeit Ihrer Lizenz angezeigt.
Bitte melden Sie sich rechtzeitig vor deren Ablauf unter spranger@hs-mittweida.de, um eine Verlängerung zu beantragen!

## Konfiguration: mona.ini
-----------------------
Um größere Datenmengen verarbeiten zu können, kann bzw. muss die Datei "mona.ini" im MoNA-Installationsverzeichnisses angepasst werden.
In dieser Konfigurationsdatei kann der maximal von MoNA verwendbare Arbeitsspeicher von standardmäßig 8GB auf einen höheren Wert eingestellt werden, abhängig davon, wieviel Arbeitsspeicher auf dem Gerät verfügbar ist, auf dem MoNA betrieben wird.

Die entsprechende Zeile in der Konfigurationsdatei lautet in der Ursprungsform:
-Xmx8g

Dieser Wert kann beispielsweise für 16GB folgendermaßen geändert werden:
-Xmx16g

Als Empfehlung sollte hier nicht der gesamte Arbeitsspeicher eines Gerätes angegeben werden, je nach den zusätzlich zu MoNA verwendeten Programmen sollte 1/4 des Arbeitsspeichers für andere Programme übrig bleiben.
Die in der Konfigurationsdatei angegebene Menge an Arbeitsspeicher für MoNA wird zudem dynamisch und erst bei Bedarf auch tatsächlich in Anspruch genommen.

## Konfiguration: Anpassen des Windows Defender
--------------------------------------------
Um ein ggf. stark verlangsamtes Einlesen von Falldaten unter Microsoft Windows zu verhindern, muss das MoNA-Installationsverzeichnis als Ausnahme zum Windows Defender hinzugefügt werden.

1. Öffnen der Einstellungsseite "Viren - und Bedrohungsschutz" in den Systemeinstellungen (Start -> Einstellungen -> Update und Sicherheit -> Windows Sicherheit -> Viren - und Bedrohungsschutz).
2. Öffnen der Einstellungen für Viren- & Bedrohungsschutz über "Einstellungen verwalten".
3. Im Unterpunkt "Ausschlüsse" den Eintrag "Ausschlüsse hinzufügen oder entfernen" auswählen.
4. Hier über den Punkt "+ Ausschluss hinzufügen" das MoNA-Installationsverzeichnis auswählen und damit als Ausnahme hinzufügen.
