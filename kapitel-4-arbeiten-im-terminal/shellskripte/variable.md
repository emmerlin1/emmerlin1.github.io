# Variable und arithmetische Ausdrücke

* `farbe=blau` Variablendeklaration
* `echo Wert der Variablen \$farbe: $farbe` Verwendung/Ausgabe einer Variablen \(das escape-Zeichen '\' verhindert die Variablenersetzung\)
* ``echo "$farbe"; echo `date``` Bei der Verwendung von **doppelten Anführungsstrichen** werden Variablen und bei Verwendung von **Backticks** Befehle ausgewertet!
* `echo "Arbeitsverzeichnis des Users: $HOME"` Verwendung von Umgebungsvariablen
* ``mydir= `pwd``` Zuweisung von Kommandoauswertungen zu Variablen
* `myarray=(null eins zwei drei vier fuenf)` Array von Werten zuweisen
* `echo ${myarray[0]}` Ausgabe eines Array-Elements
* `echo ${myarray[*]} #oder echo ${array[@]}` Ausgabe aller Array-Elemente
* `echo ${#myarray[*]}` **Anzahl** der belegten Elemente anzeigen
* `unset myarray; unset myarray[2]` **Löschung** des gesamten Arrays oder einzelner Elemente
* `a=123; echo $((3+4*a))` Arithmetischer Ausdruck: Variable a kann in einem arithmetischen Ausdruck ohne '$' verwendet werden!
* Spezielle Shellvariable:

| Variable | Bedeutung |
| :--- | :--- |
| $? | Rückgabewert des letzten Kommandos |
| $$ | Prozessnummer \(PID\) der aktuellen Shell |
| $! | PID des zuletzt gestarteten Hintergrundprozesses |
| $0 | Name des aktuell ausgeführten Skripts |
| $\# | Anzahl der beim Aufruf des Skripts übergebenen Parameter |
| $\* oder $@ | Gesamtheit der beim Aufruf des Skripts übergebenen Parameter in Form eines leerzeichengetrennten Strings |
| ${n} | Zugriff auf n-ten Parameter des Skripts, Klammern können entfallen, wenn n&lt;10 |

