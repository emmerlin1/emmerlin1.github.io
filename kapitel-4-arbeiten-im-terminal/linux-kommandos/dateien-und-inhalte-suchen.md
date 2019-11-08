# Dateien und Inhalte suchen

## find

* `find -iname "filename"` Finde Datei mit Namen filename, Groß-/Kleinschreibung wird nicht beachtet.
* `find / -iname "filename"` Finde Datei ausgehend vom Wurzelverzeichnis.
* `find /home/user -iname "*.conf"` Finde alle Dateien mit Endung .conf im Homeverzeichnis von user.
* ```find /home/pat -iname "*.conf" | ``less`````  Füttere das Kommando less mit dem Ergebnis der Dateisuche. Dadurch kann das Suchergebnis selbst durchgescrollt und durchsucht werden.
* find / **-type f** -iname "filename" Durchsuche nur bestimmte Dateiarten
  * f=regular files,
  * d=directories,
  * l=symb. links,
  * c=char. devices,
  * b=block devices
* find / **-size +50M** -iname "filename" Suche Dateien größer als 50MByte
* find /travelphotos -type f -size +200k **-not** -iname "\*2015\*" Suche Dateien größer als 200kB, deren Name den Substring 2015 nicht enthalten
* find / **-user** username / **-group** users **-perm** 777 -iname "\*" Suche Dateien, die dem Benutzer username, der Gruppe users angehören und die Zugriffsrechte rwx aufweisen.
* find . -type f -perm 777 **-exec** chmod 755 **{} \**; Suche reguläre Dateien mit den Zugriffsrechten rwxrwxrwx und ändere deren Rechte über 'chmod 755' zu r-xr-xr-x

## locate

* sudo apt install mlocate; sudo updatedb;
* **locate** -i "\*.jpg"

## grep

* **grep -r -i** "search query" /path/to/directory/ Suche rekursiv nach dem Inhalt 'search query' im Pfad '/path/to/directory/'
* grep -r -i "search query" /path/to/directory/ **\| cut -d: -f1** Zeige nur den ersten Teil der jeweiligen Ergebniszeile \(Trennzeichen ist hier der Doppelpunkt\)
* grep -r -i "search query" /path/to/directory/ **2&gt;/dev/null** Zugriffs-Fehler werden in den Mülleimer umgeleitet

