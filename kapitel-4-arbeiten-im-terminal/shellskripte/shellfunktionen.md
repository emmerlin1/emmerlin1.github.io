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





