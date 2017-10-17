### Systemutilities

| Befehl | Bedeutung | Beispiel |
| :--- | :--- | :--- |
| **alias** | Aliasname für ein Kommando vergeben | alias ll='ls -l' |
| **awk** | Utility für Bearbeitung/Auswertung von Textdateien | awk '$2 == "localhost" { print $1 }' /etc/hosts |
| **bg** | Verlagere einen per CTRL-Z gestoppten Prozess in den Hintergrund, der dort dann weiter läuft | bg %1 |
| **cat** | Füge mehrere Dateien zusammen, auch kann der Befehl für die Anzeige von Dateiinhalten genutzt werden | cat file1.txt file2.txt &gt;file3.txt |
| **chroot** | Mit chroot kann ein programm sein Wurzelverzeichnis wechseln | z.B. [Linux-Reparatur↑](https://wiki.ubuntuusers.de/chroot/Live-CD/) |
| **crontab** | Steuerung von zeitlich geplanten Vorgängen \(Skripte, Programme, Backups etc.\) | crontab -e |
| **cut** | Extrahiert spaltenweise Ausschnitte aus Textzeilen mittels angegebenem Trennzeichen/Zeichenposition | <code>grep -r -i "include" ./ &#124; cut -d: -f1</code> |
| **date** | Ausgabe von Datum/Zeit | date +%d.%m.%Y |
| **dd** | dd dient zum bit-genauen Kopieren von Festplatten, Partitionen oder Dateien | sudo dd if=2017-08-16-raspbian-stretch.img of=/dev/sdg status=progress bs=16M |
| **df** | diskfree, zeige den freien Festplattenplatz von eingehängten Partitionen an | df -h |
| **diff** | Vergleich der Inhalte zweier Dateien/Ordner | diff file1 file2 |
| **echo** | Zeilenweise Anzeige von Zeichenketten/Variablen auf dem Standardausgabegerät | echo 'Hello Linux World!' |
| **env** | Steuerung/Anzeige der Umgebungsvariablen; dauerhaft werden Variable in /etc/environment hinzugefügt | env VAR1="blahblah" command\_to\_run command\_options |
| **export** | Definiert und verwaltet Umgebungsvariable; zusätzliche persistente Umgebungsvariablen werden im Verzeichnis /etc/profile.d in Form von shell-Dateien hinterlegt | export var="myvalue" |
| **fdisk** | Plattenpartitionierungstool | fdisk /dev/sda |
| **fg** | Holen eines Prozesses in den Vordergrund (**Ctrl+z**, **jobs**) | fg %1 |
| **gcc** | Standard C-Compiler | gcc -o mybin mybin.c |
| **grep** | Durchsuchen von Dateien nach Textstücken | grep -r -i "include" ./ |
| **hash** | Zeigt und verwaltet verwendete Bash-Kommandos | hash |
| **jobs** | Zeigt die Hintergrundprozesse an | jobs |
| **join** | Verbinde Inhalte zweier Dateien zeilenweise | join -1 2 -2 1 &lt;\(sort -k 2 wine.txt\) &lt;\(sort reviews.txt\) |
| **kill/killall** | Beende Prozesse | kill -9 2345 |
| **locale** | Informationen über Gebietsschema | locale -a |
| **logger** | Vollführt Einträge im System-Log-Mechanismus \(/var/log/syslog\) | logger 'mymessage' |
| **logname** | Anzeige des aktuellen Loginnamens | logname |
| **lp** | Druckbefehl in Warteschlange einreihen | lp textfile.txt |
| **lsusb** | Zeige USB-Busse des Systems und die angschlossenen USB-Geräte | lsusb -t |
| **make** | Tool zum Übersetzen von C-Quellcode | make -f mymakefile |
| **man** | Manual-Seiten für Linux-Befehle und C-Funktionen | man -k printf |
| **mesg** | Erlaube Anzeige von Nachrichten anderer User | mesg y |
| **mkfifo** | Erzeugung einer FIFO-Pipe | mkfifo my\_pipe; gzip -9 -c &lt; my\_pipe &gt; out.gz &; cat file &gt; my\_pipe |
| **mknod** | Erzeugung von Block- und Zeichengeräten | sudo mknod /dev/myrandom c 1 8 |
| **mount** | Zeigt die eingehängten Dateisysteme wie Festplatten, USB-Sticks und SD-Karten aber auch temporäre an; es können auch Medien manuell eingehängt werden | sudo mount /dev/sda1 /mnt |
| **nano** | Angenehmer Terminal-Editor | nano |
| **nice** | Veränderung der Priorität eines zu startenden Prozesses \(negativ = höhere Priorität\) | sudo nice -11 gedit |
| **nl** | Ausgabe von Dateien mit Zeilennummerierung | nl textfile.txt |
| **nohup** | Starten eines Kommandos mit unterdrücktem HUP-Signal, Prozess läuft nach Ausloggen/Beendigung der Konsole weiter | nohup gedit & |
| **passwd** | Änderung des Passworts | passwd username |
| **ps** | Ausgabe der aktuellen Prozessliste |  |
| **read** | Lesen von Standard Input | read first middle last |
| **renice** | Änderung der Priorität eines laufenden Prozesses, Höherstufung nur als root | sudo renice -10 \`pidof nano\` |
| **sed** | Nicht-interaktiver Texteditor für Konsole oder Shell-Skripte | sed -e '/debug/d'  log |
| **sleep** | Pausieren eines Prozesses | sleep 10 |
| **sort** | Zeilenweise Sortierung von Standardausgaben/Textdateien | <code>ls -s &#124; sort -n</code> |
| **source** | Einbinden von in Dateien hinterlegter Funktionalität in die aktuelle Shell | `source myfunctions.sh` |
| **split** | Aufteilung von großen Dateien auf mehrere kleinere | split -b 700M archiv.tar split-archiv.tar. |
| **sync** | Explizites Schreiben von im Speicher gehaltener Daten auf die Platte | sync |
| **tail** | Ausgabe der letzten Zeilen einer Datei | tail -20 myfile |
| **tee** | Verdopplung der Ausgabe - in Textdatei und auf Standardausgabe | <code>ls -la &#124; tee alle\_dateien.txt</code> |
| **top** | Dynamische Anzeige der aktuell auf dem System laufenden Prozesse \(Alternative htop\) und des Ressourcenverbrauchs | top |
| **touch** | Erstellung einer leeren Datei | touch myfile.txt |
| **truncate** | Die Größe einer Datei auf die angegebene Größe verkleinern/-größern; abgeschnittene Daten gehen verloren; nicht existierende Dateien werden erstellt | truncate -s 100g /tmp/SWAPDATEI |
| **umask** | Anzeige/Änderung der aktuellen Maskierung der Zugriffsrechte einer neuen Datei | umask 0022 |
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
| **write** | Schreibe Nachricht an am System eingeloggten Benutzer \(mesg y muss bei diesem aktiviert sein\) | write username |
| **zcat** | Gib den Inhalt gzip-komprimierter Dateien aus | zcat gezippt.gz |

[Weiterer kleiner Kommando-Überblick](https://community.linuxmint.com/tutorial/view/244)

