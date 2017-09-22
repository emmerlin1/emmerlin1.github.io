### Nützliche Oneliner

* **`find`**` \bin \usr\bin -type f -exec file {} \; | `**`grep`**` "shell" | `**`wc`**` -l`
  Durchsuche \(find\) die Verzeichnisse /bin und /usr/bin nach allen Dateien und füttere mit jeder gefundenen Datei den Befehl file;   
  dessen Ausgabe wird nach dem Wort "shell" durchsucht \(grep\), wird es gefunden, dann summiert der Befehl wc diese Zeile auf;  
  d.h. wir erhalten die **Gesamtanzahl** von Shellskripten in den beiden durchsuchten Verzeichnissen



