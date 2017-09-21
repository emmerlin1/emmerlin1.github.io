### grep, sed, awk, sort, cut und regular expressions

Mittels grep, sed, awk, sort, cut und regulären Ausdrücken können Textausgaben gefiltert, durchsucht und ausgewertet werden. Im Folgenden werden einige Beispiele aufgeführt:

#### regular expressions

#### grep

#### sed

* cat text.txt \| sed '=' \| sed 'N;s/\n/\. /'
  Gib die Datei text.txt zeilenweise aus \(cat text.txt\), füge für jede Zeile die Zeilennummer mit Zeilenumbruch hinzu \( sed '='\)

* sed -e '/\\$/N; s/\\\n//;' text.txt  
  Teste Zeilenbedingung /\\$/ \(hier Backslash am Ende der Zeile\), wenn ja, dann lies die nächste Zeile ein \(N;\) und ersetze Backslash und Zeilenumbruch mit nichts \(s/\\\n//;\)

#### awk

* ls -l \| awk 'BEGIN {sum=0} {sum=sum+$5} END {print sum}'
  summiere die 5. Spalte der ausgegebenen Zeilen des Befehls 'ls -l' auf und gebe die Summe am Ende aus



