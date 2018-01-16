# Deutsche Gesetze und Verordnungen

Alle Gesetzestexte aus gesetze-im-internet.de als SQL-Dump und XML sowie Crawler Scripte zur aktualisierung.

Letzte Aktualisierung: Jan 2018 (insgesamt 6384)

Sprache: Python3

## Beschreibung der Scripte und Ordner

Der ganze Prozess wurde zur besseren Übersichtlichkeit in drei Schritte (Scripte) unterteilt:

links.py: Dieses Script muss zuerst ausgeführt werden und sammelt alle Infos zu verfügbaren Gesetzen und Verordnungen von https://www.gesetze-im-internet.de/aktuell.html, die u.a. für das Script files.py benötigt werden.

files.py: Dieses Script muss nach links.py ausgeführt werden und nutzt die json Dateien aus /data um alle Zip-Dateien herunterzuladen und in /laws zu entpacken.

todbase.py: Dieses Script muss zuletzt ausgeführt werden. Es importiert alle Gesetze und Verordnungen in eine SQL Datenbank. Struktur: Gesetz/Verordnung (Tabellen) - Paragraf/Artikel (Reihen)  - Absatz (Spalten).

laws/: Alle Gesetze und Verordnungen als XML Dateien.

data/: Informationen zu allen verfügbaren Gesetzen und Verordnungen die von files.py benötigt werden.

gesetze.sql: Alle Gesetze und Verordungen als SQL - Dump für mysql oder mariaDB Datenbanken.
