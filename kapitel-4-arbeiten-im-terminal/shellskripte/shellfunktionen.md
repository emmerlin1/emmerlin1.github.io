### Shellfunktionen

* Häufig benutzte Programmsequenzen lassen sich als separate Shellskripte abspeichern und dann entsprechend aufrufen; eine Alternative hierzu sind Shellfunktionen
{%ace edit=true, lang='sh'%}
#!/bin/bash  
function sortfkt () {  
   sort -n -r  
}  
ls -l | sort-num-rev
{%endace%}


* Shellfunktionen verhalten sich aus Sicht der aufrufenden Stelle wie Standardkommandos; sie besitzen eine Standard-Ein- und Ausgabe, können mit Aufrufparameter umgehen etc.

* Innerhalb einer Shellfunktion entsprechen die Positionsparameter ($1,$2...,$*) den Argumenten der Shellfunktion und nicht denen des aufrufenden Shellprozesses.

* Innerhalb einer Shellfunktion kann der Funktionsname über die Variable FUNCNAME ermittelt werden.

* Über das return-Kommando kann ein Rückgabewert zurück gegeben werden. Ist keines vorhanden, wird der Rückgabewert des letzten Kommandos der Shellfunktion zurück gegeben.






