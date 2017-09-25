### Kommandos und Kontrollstrukturen

* Verzweigungen und Schleifen verwenden als 'Weichenstellung' für den weiteren Ablauf \(Steuerungsgröße\) grundsätzlich nicht den Wert 'true' oder 'false' sondern den Rückgabewert von Programmen, z.B.  
  `test -d "$HOME/.config" && echo "existiert"`

* Dabei gilt der Rückgabewert 0 für "Erfolg" und 1-255 als Misserfolg:

| Wert | Bedeutung |
| :--- | :--- |
| **0** | Erfolg |
| **1** | allgemeiner Fehler |
| **2** | Missbrauch einer Shellfunktion |
| **3-125** | frei wählbar durch den User \(z.B. exit 25\) |
| **126** | Kommando nicht ausführbar \(wegen Rechte/Dateityp\) |
| **127** | aufgerufener Befehl/Programm wurde nicht gefunden |
| **128** | Ungültiges Argument für exit verwendet \(z.B. exit 2.5 |
| **129-192** | Programmabbruch durch Signal 'Wert'-128, Signalübersicht durch Befehl **kill -l** |

* Der Befehl '**test**' dient zum Vergleich von Zeichenketten/Zahlen und der Überprüfung von Dateieigenschaften

  * **test "$x"**
    nur _ein_ Argument → das Argument \(hier $x\) wird auf 'nicht leer' geprüft
  * **test $x -lt 8**  
    die Operatoren -lt \(less\), -gt \(greater\), -ge \(greater/equal\), -le \(less/equal\), -eq \(equal\) oder -ne \(not equal\) wenden den entsprechenden Vergleich auf  das Zahl-Argument \($x\) an.

  * **test "$x" \&gt; 10**  
    Testet, ob das erste Argument \(Zeichenkette $x\) lexikographisch im Wörterbuch hinter der zweiten \(hier die 10\) steht

  * **test -r "$x"**  
    Prüft, ob die Datei $x existiert und lesbar ist

  * **test -d "$HOME/.config"**  
    Testet, ob das Verzeichnis \(-d\) .conf im Arbeitsverzeichnis des Benutzers existiert

  * **\[ "$x" \]**  
    Kurzform von 'test "$x"'

* **if-Verzweigung**  
  ```
if <condition>  
  then  
     ...  
  elif <condition>  
     ...  
  else  
     ...  
  fi
```



* **case-Mehrfachalternative **\(Beispiel sh. Verzeichnis init.d**\)**  
  ```
case <command> in  
     <pattern1>)  
        ...  
        ;;  
     <pattern2>)  
        ...  
        ;;  
     ...  
  esac;
```
* **for-Schleife**  
  ```
for <variable> in <Liste>  
  do  
     <command>  
  done
```



* **while/until**  
  ```
   while <condition>  
  do  
     <command>  
  done```

* **until/while**  
  ```
   until <condition>  
  do  
     <command>  
  done```






