### Dateien und Inhalte suchen

* **find** -iname "filename"  
  Finde Datei mit Namen filename, Groß-/Kleinschreibung wird nicht beachtet.

* **find** / -iname "filename"  
  Finde Datei ausgehend vom Wurzelverzeichnis.

* **find** /home/user -iname "\*.conf"  
  Finde alle Dateien mit Endung .conf im Homeverzeichnis von user.

* find /home/pat -iname "\*.conf"** \| less**  
  Füttere das Kommando less mit dem Ergebnis der Dateisuche. Dadurch kann das Suchergebnis selbst durchgescrollt und durchsucht werden.

* find /** -type f** -iname "filename"  
  Durchsuche nur bestimmte Dateiarten 

  * f=regular files, 

  * d=directories,

  * l=symb. links,

  *  c=char. devices, 

  * b=block devices



