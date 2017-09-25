### Shellvariable

* `farbe=blau`  
  Variablendeklaration

* `echo Wert der Variablen \$farbe: $farbe`  
  Verwendung/Ausgabe einer Variablen \(das escape-Zeichen '\' verhindert die Variablenersetzung\)

* <code>echo "$farbe"; echo &#96;date&#96;</code>  
  Bei der Verwendung von **doppelten Anführungsstrichen** werden Variablen und bei Verwendung von **Backticks** Befehle ausgewertet!

* `echo "Arbeitsverzeichnis des Users: $HOME"`  
  Verwendung von Umgebungsvariablen

* <code>mydir= &#96;pwd&#96;</code>  
  Zuweisung von Kommandoauswertungen zu Variablen
  
* `myarray=(null eins zwei drei vier fuenf)`  
  Array von Werten zuweisen

* `echo ${myarray[0]}`  
  Ausgabe eines Array-Elements

* `echo ${myarray[*]} #oder echo ${array[@]}`  
  Ausgabe aller Array-Elemente

* `echo ${#myarray[*]}`  
  **Anzahl** der belegten Elemente anzeigen
  
* `unset myarray; unset myarray[2]`  
  **Löschung** des gesamten Arrays oder einzelner Elemente
  
* Spezielle Shellvariable:

| Variable | Bedeutung | 
| :--- | :--- |
| $? | Rückgabewert des letzten Kommandos |
| $$ | Rückgabewert des letzten Kommandos |
| $! | Rückgabewert des letzten Kommandos |
| $0 | Rückgabewert des letzten Kommandos |
| $# | Rückgabewert des letzten Kommandos |
| $* | Rückgabewert des letzten Kommandos |
| $@ | Rückgabewert des letzten Kommandos |
| $n | Rückgabewert des letzten Kommandos |

































































