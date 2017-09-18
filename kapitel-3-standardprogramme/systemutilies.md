### Systemutilities

| Befehl | Bedeutung | Beispiel |
| :--- | :--- | :--- |
| **alias** | Aliasname für ein Kommando vergeben |  |
| **awk** | Utility für Bearbeitung/Auswertung von Textdateien |  |
| **bg** | Verlagere einen per CTRL-Z gestoppten Prozess in den Hintergrund, der dort dann weiter läuft |  |
| **cat** | Füge mehrere Dateien zusammen, auch kann der Befehl für die Anzeige von Dateiinhalten genutzt werden |  |
| **chroot** | Mit chroot kann ein programm sein Wurzelverzeichnis wechseln |  |
| **crontab** | Steuerung von zeitlich geplanten Vorgängen \(Skripte, Programme, Backups etc.\) |  |
| **cut** | Extrahiert spaltenweise Ausschnitte aus Textzeilen mittels angegebenem Trennzeichen/Zeichenposition |  |
| **date** | Ausgabe von Datum/Zeit |  |
| **dd** | dd dient zum bit-genauen Kopieren von Festplatten, Partitionen oder Dateien |  |
| **df** | diskfree, zeige den freien Festplattenplatz von eingehängten Partitionen an |  |
| **diff** | Vergleich der Inhalte zweier Dateien/Ordner |  |
| **echo** | Zeilenweise Anzeige von Zeichenketten/Variablen auf dem Standardausgabegerät |  |
| **env** | Steuerung/Anzeige der Umgebungsvariablen |  |
| **fg** | Holen eines Prozesses in den Vordergrund |  |
| **grep** | Durchsuchen von Dateien nach Textstücken |  |
| **jobs** | Zeigt die Hintergrundprozesse an |  |
| **join** | Verbinde Inhalte zweier Dateien zeilenweise |  |
| **kill/killall** | Beende Prozesse |  |
| **locale** | Informationen über Gebietsschema |  |
| **logger** | Vollführt Einträge im System-Log-Mechanismus |  |
| **logname** | Anzeige des aktuellen Loginnamens |  |
| **lp** | Druckbefehl in Warteschlange einreihen |  |
| **make** | Tool zum Übersetzen von C-Quellcode |  |
| **man** | Manual-Seiten für Linux-Befehle und C-Funktionen |  |
| mesg | Erlaube Anzeige von Nachrichten anderer User | mesg y |
| **mkfifo** | Erzeugung einer FIFO-Pipe |  |
| **mknod** | Erzeugung von Block- und Zeichengeräten |  |
| **nano** | Angenehmer Terminal-Editor |  |
| **nice** | Veränderung der Priorität eines laufenden Prozesses |  |
| **nl** | Ausgabe von Dateien mit Zeilennummerierung |  |
| **nohup** | Starten eines Kommandos mit unterdrücktem HUP-Signal, Prozess läuft nach Ausloggen/Beendigung der Konsole weiter | nohup gedit & |
| **ps** | Ausgabe der aktuellen Prozessliste |  |
| **read** | Lesen von Standard Input | rea first middle last |
| **renice** | Änderung der Priorität eines laufenden Prozesses, Höherstufung nur als root | sudo renice -10 \`pidof nano\` |
| **sed** | Nicht-interaktiver Texteditor für Konsole oder Shell-Skripte | sed -e '/debug/d'  log |
| **sleep** | Pausieren eines Prozesses | sleep 10 |
| **sort** | Zeilenweise Sortierung von Standardausgaben/Textdateien | ls -s &#124; sort -n |
| **split** | Aufteilung von großen Dateien auf mehrere kleinere | split -b 700M archiv.tar split-archiv.tar. |
| **sync** | Explizites Schreiben von im Speicher gehaltenen Daten auf die Platte | sync |
| **tee** | Verdopplung der Ausgabe - in Textdatei und auf Standardausgabe | ls -la &#124; tee alle\_dateien.txt |
| **top** | Dynamische Anzeige der aktuell auf dem System laufenden Prozesse \(Alternative htop\) und des Ressourcenverbrauchs | top |
| **truncate** | Die Größe einer Datei auf die angegebene Größe verkleinern/-größern; abgeschnittene Daten gehen verloren; nicht existierende Dateien werden erstellt | truncate -s 100g /tmp/SWAPDATEI |
| **umask** | Anzeige/Änderung der aktuellen Maskierung der Zugriffsrechte einer neuen Datei | touch 0022 |
| **unalias** | Aliasnamen löschen | unalias ll |
| **uname** | Ausgabe bestimmter Systeminfos wie Kernelversion/-Variante, Hostname, Prozessortyp, Betriebssystem | uname -a |
| **uptime** | Ausgabe der aktuellen Laufzeit des Systems | uptime -s |
| **users** | Anzeige der aktuell am System angemeldeten Benutzer | users |
| **vim** | Konsolentexteditor | vim |
| **wc** | Anzeige der Wort-/Zeilen-/Byteanzahl, einer Datei | wc -w textdatei.txt |
| **whereis** | Lokalisiere die Binärdatei, Quelldateien und Manpages für das Dateiargument | whereis ls |
| **which** | Zeige den Pfad des Kommandos | which ls |
| **who** | Zeige die angemeldeten Benutzer und weitere Informationen | who -b |
| **whoami** | Wer bin ich? | whoami |
| **write** | Schreibe Nachricht an am System eingeloggten Benutzer \(mesg y muss bei diesem aktiviert sein\) | write username  |
| **zcat** | Gib den Inhalt gzip-komprimierter Dateien aus | zcat gezippt.gz |

Ver

