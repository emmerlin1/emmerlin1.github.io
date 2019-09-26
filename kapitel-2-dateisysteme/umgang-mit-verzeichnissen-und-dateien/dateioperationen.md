# Dateioperationen / Umleitung

## Dateioperationen

| Befehl | Bedeutung |
| :--- | :--- |
| **basename** Dateiname | Gibt einen Dateinamen ohne Pfadangaben aus |
| **cat** Datei1 Datei2 DateiN | Verbindet mehrere Dateien und gibt das Ergebnis auf Standardausgabe aus |
| **chgrp** groupname Dateiname | Gruppenzugehoerigkeit einer Datei ändern |
| **chown** username:groupname Dateiname | Eigentümer und Gruppenzugehoerigkeit einer Datei ändern |
| **cmp** Datei1 Datei2 | Vergleich zweier Dateien auf Übereinstimmung |
| **cp** Datei neue\_Datei | Kopieren einer Datei |
| **dirname** Dateiname | Gibt nur den Pfad zu einer Datei aus |
| **file** Datei | Zeigt die Dateiart einer Datei an \(Binär, Text, Executable, Architektur, 64bit, 32bit\) |
| **find** / -name "\*.txt" -print | Suche alle Dateien mit Endung txt im gesamten Dateibaum |
| **head** Textdatei | Erste Zeilen einer ASCII-Datei anzeigen |
| **less** Textdatei | seitenweise Anzeige einer ASCII-Datei, durchscrollbar mittels vi-Tastaturbefehlen |
| **ln** -s Quelle Ziel | Erstellen eines Softlinks zu einer Quelldatei |
| **more** Dateiname | Seitenweises Durchscrollen einer Textdatei nach unten |
| **mv** Datei neue\_Datei | Verschiebe Datei an Stelle neue\_Datei |
| **rm** Dateiname | Lösche Datei |
| **rename** alte\_Dateiendung neue\_Dateiendung Dateien | Umbenennung der Dateiendung von Dateien, z.B. rename .xml .xsd \*.xml |
| **tail** Textdatei | Ende einer Textdatei ausgeben |
| **touch** Datei | Ändert den Zeitstempel von Dateien. Wenn eine Datei nicht existiert, wird sie mit einer Groesse von 0 Byte angelegt |

## Umleitung

| Befehl | Bedeutung | Beispiel |
| :--- | :--- | :--- |
| &gt; | Umleitung der **Standardausgabe** z.B. in eine Datei | ls &gt; verzeichnis.txt |
| &gt;&gt; | Anhängen der Standardausgabe z.B. an den Inhalt einer Datei | ls &gt;&gt; verzeichnis.txt |
| 2&gt; | Umleitung der **Fehlerausgabe** z.B. in den 'Mülleimer' | ls 2&gt; /dev/null |
| &&gt; | Umleitung der Standardausgabe **und** Fehlerausgabe z.B. in eine Datei | ls &&gt; verzeichnis.txt |
| 2&gt;&1 | Umleitung der Fehlerausgabe dorthin wo auch die Standardausgabe hin ausgegeben wird z.B. in eine Datei | ls &gt; verzeichnis.txt 2&gt;&1 |
| exec 9&gt; filename | Umleitung aller nachfolgenden Ausgaben, z.B. über einen neuen Kanal in Datei schreiben | exec 9&gt; mylogfile; echo 'hello' &gt;&9 |
| exec 9&gt;&- | explizites Schließen eines Umleitungskanals |  |
| &lt; | Umleitung der **Standardeingabe** z.B. aus einer Datei lesen | grep &lt; /var/log/syslog |
| `|` | Verwendung der **Standardausgabe** eines Kommandos als Eingabe für das folgende Kommando | `cat /var/log/syslog | grep -v 'kernel'` |
| tee | Verdoppelung der Ausgabe → in eine Datei **und** auf stdout schreiben | `ls | tee verzeichnis.txt | grep '.png$'` |

