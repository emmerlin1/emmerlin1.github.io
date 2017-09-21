### grep, sed, awk, sort, cut und regular expressions

Mittels grep, sed, awk, sort, cut und regulären Ausdrücken können Textausgaben gefiltert, durchsucht und ausgewertet werden. Im Folgenden werden einige Beispiele aufgeführt:

#### regular expressions

Eine kurze Zusammenfassung regulärer Ausdrücke ist beispielsweise [hier↑](https://www.cheatography.com/davechild/cheat-sheets/regular-expressions/pdf_bw/) zu finden. Eine vollständige Referenz ist ebenfalls [verfügbar↑](https://www.princeton.edu/~mlovett/reference/Regular-Expressions.pdf).

Im Folgenden sind wichtige Ausdrücke ausgeführt:

| Ausdruck | Bedeutung | Beispiel |
| :--- | :--- | :--- |
| ^ | Zeile/Zeichenfolge muss mit folgendem Zeichen beginnen | '^P' ist zutreffend für "Phil" aber nicht für "Chill" |
| $ | Zeile/Zeichenfolge muss mit vorhergehendem Zeichen enden | 'L$' ist zutreffend für "PhiL" aber nicht für "Chili" |
| . | Punkt kann mit **einem** beliebigem Zeichen belegt sein | 'S.m.s.e.' ist zutreffend für "Semester" |
| {n,m} | Zeichen/Ausdruck davor ist n bis m mal vorhanden | 'C{2,4}' ist zutreffend für "CCabc" und C"CCCabc", aber nicht für "Cabc" |
| {,m} | Zeichen/Ausdruck davor ist m oder weniger mal vorhanden | 'C{,4}' ist zutreffend für "CCabc" und C"CCCabc", und auch für "Cabc" oder "abc" |
|  |  |  |

#### grep

#### sed

* cat text.txt \| sed '=' \| sed 'N;s/\n/. /'  
  Gib die Datei text.txt zeilenweise aus \(cat text.txt\), füge für jede Zeile die Zeilennummer mit Zeilenumbruch hinzu \( sed '='\)

* sed -e '/$/N; s/\n//;' text.txt  
  Teste Zeilenbedingung /$/ \(hier Backslash am Ende der Zeile\), wenn ja, dann lies die nächste Zeile ein \(N;\) und ersetze Backslash und Zeilenumbruch mit nichts \(s/\n//;\)

* Weitere Beispiele zu häufig auftretenden Anwendungsfällen sind unter [sourceforge](http://sed.sourceforge.net/sedfaq.html) zu finden.

#### awk

* ls -l \| awk 'BEGIN {sum=0} {sum=sum+$5} END {print sum}'
  summiere die 5. Spalte der ausgegebenen Zeilen des Befehls 'ls -l' auf und gebe die Summe am Ende aus



