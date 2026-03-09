# Releaseprüfung

## Milestone Release

Wir veröffentlichen Schild3 und den SVWS-Server Mit einer neuen Minior Versionsnummer
Beispiel im kommenden Release wird das sein.
SVWS-Server 1.3.1
Schild-NRW 3.4.0

Der SVWS-Server liefert über den Endpunkt getSchildMinVersion 3.4.0.
Vor dem Release wird in der Installation von Schild-NRW3 server.json 1.3.1 eingetragen.
Schild-NRW3 muss dann prüfen ob der Server mindestens 1.3.x ist und kann alle Kombitantionen aktzeptieren
Er muss außerdem prüfen ob er selbst mindestens 3.4.0 ist
Dann muss Schild-NRW3 starten.

Hier die beiden Endpunkte im Server:
https://nightly.svws-nrw.de/debug/index.html?urls.primaryName=server#/Server/getSchildMinVersion
https://nightly.svws-nrw.de/debug/index.html?urls.primaryName=server#/Server/getServerVersion

## Bugfix Release Schild-NRW3 oder SVWS-Server

Bugfix Server wäre dann 1.3.2 Schild3 startet weil 1.3.x ist erfüllt
Bugfix Schild3 wäre dann 3.4.1 Schild3 staret weil minVersion ist 3.4.0

## Notfall Release SVWS-Server

Es gibt einen Notfall und es muss Bugfix 1.3.2 herausgebracht werden mit einem DB Update was dazu führt, dass Schild-NRW3 nicht mehr läuft.
Dann wird der Endpunkt getSchildMinVersion auf 3.4.2 (Beispiel!) gesetzt. Wenn Schild-NRW3 dann merkt es ist zu alt, darf es nicht starten.
Es sollte ein Hinweis zum Update kommen. In diesem Fall würde ja auch imme reine lauffähige Version von Schild-NRW3 herausgebracht werden.

