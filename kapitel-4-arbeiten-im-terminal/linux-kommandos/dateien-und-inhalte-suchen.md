### Dateien und Inhalte suchen

#### find

* **find -iname "filename"**  
  Finde Datei mit Namen filename, Groß-/Kleinschreibung wird nicht beachtet.

* find** / **-iname "filename"  
  Finde Datei ausgehend vom Wurzelverzeichnis.

* find /home/user -iname "**\***.conf"  
  Finde alle Dateien mit Endung .conf im Homeverzeichnis von user.

* find /home/pat -iname "\*.conf"** \| less**  
  Füttere das Kommando less mit dem Ergebnis der Dateisuche. Dadurch kann das Suchergebnis selbst durchgescrollt und durchsucht werden.

* find /** -type f** -iname "filename"  
  Durchsuche nur bestimmte Dateiarten

  * f=regular files,

  * d=directories,

  * l=symb. links,

  * c=char. devices,

  * b=block devices

* find /** -size +50M** -iname "filename"

* find /travelphotos -type f -size +200k** -not** -iname "\*2015\*"

* find /** -user** username / **-group** users  **-perm** 777 -iname "\*"

* find . -type f -perm 777** -exec** chmod 755 **{} \**;



#### locate

* sudo apt install mlocate; sudo updatedb;
* **locate** -i "\*.jpg"
* 


