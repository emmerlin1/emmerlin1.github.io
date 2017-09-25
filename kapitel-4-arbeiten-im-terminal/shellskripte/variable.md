### Shellvariable

* `farbe=blau`  
  Variablendeklaration

* `echo Wert der Variablen \$farbe: $farbe`  
  Verwendung/Ausgabe einer Variablen \(das escape-Zeichen '\' verhindert die Variablenersetzung\)

* ``echo "$farbe"; echo `date```  
  Bei der Verwendung von **doppelten Anführungsstrichen** werden Variablen und bei Verwendung von **Backticks** Befehle ausgewertet!

* `echo "Arbeitsverzeichnis des Users: $HOME"`  
  Verwendung von Umgebungsvariablen



