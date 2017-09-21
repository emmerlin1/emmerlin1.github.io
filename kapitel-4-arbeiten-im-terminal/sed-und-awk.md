### grep, sed, awk, sort, cut und regular expressions

Mittels grep, sed, awk, sort, cut und regulären Ausdrücken können Textausgaben gefiltert, durchsucht und ausgewertet werden. Im Folgenden werden einige Beispiele aufgeführt:

#### regular expressions

Eine kurze Zusammenfassung regulärer Ausdrücke ist beispielsweise [hier↑](https://www.cheatography.com/davechild/cheat-sheets/regular-expressions/pdf_bw/) zu finden. Eine vollständige Referenz ist ebenfalls [verfügbar↑](https://www.princeton.edu/~mlovett/reference/Regular-Expressions.pdf).

Im Folgenden sind wichtige Ausdrücke ausgeführt:

| Übereinstimmung | Bedeutung | Beispiel |
| :--- | :--- | :--- |
| ^ | Zeile/Zeichenfolge muss mit folgendem Zeichen beginnen | '^P' ist zutreffend für "Phil" aber nicht für "Chill" |
| $ | Zeile/Zeichenfolge muss mit vorhergehendem Zeichen enden | 'L$' ist zutreffend für "PhiL" aber nicht für "Chili" |
| . | Punkt kann mit **einem** beliebigem Zeichen belegt sein | 'S.m.s.e.' ist zutreffend für "Semester" |
| **Anzahl** | **Bedeutung** | **Beispiel** |
| \* | stimmt mit beliebiger Anzahl überein \(0..n\) | 'R\*i\*c\*h\*$' ist zutreffend für "qqRRRiihh" |
| + | Zeichen/Ausdruck davor ist mindestens einmal vorhanden \(1..n\) | '^K\*e\*s\*d\*e\*n+' ist zutreffend für "nP" |
| {n,m} | Zeichen/Ausdruck davor ist n bis m mal vorhanden | 'C{2,4}' ist zutreffend für "CCabc" und C"CCCabc", aber nicht für "Cabc" |
| {,m} | Zeichen/Ausdruck davor ist m oder weniger mal vorhanden | 'C{,4}' ist zutreffend für "CCabc" und C"CCCabc", und auch für "Cabc" oder "abc" |
| {m} | Zeichen muss exakt m mal vorhanden sein | 'a\[0,9\]{5}b' ist zutreffend für "a12349b", aber nicht für "a123456b" |
| C? | Zeichen/Ausdruck davor ist optional \(0,1\) |  |
| **Gruppierung** | **Bedeutung** | **Beispiel** |
| \[\] | eines der beinhalteten Zeichen ist vorhanden | '\[abc\]\[a-c\]\[stu\]' ist zutreffend für "cat" |
| \(\) | Gruppierung von Zeichen ist vorhanden | 'Das Wetter ist \(toll\|richtig schlecht\)' ist zutreffend für "Das Wetter ist toll" |

#### grep

#### sed

* cat text.txt \| sed '=' \| sed 'N;s/\n/. /'  
  Gib die Datei text.txt zeilenweise aus \(cat text.txt\), füge für jede Zeile die Zeilennummer mit Zeilenumbruch hinzu \( sed '='\), lies die nächste Zeile \(N;\) und

* sed -e '/$/N; s/\\\n//;' text.txt  
{% math %}\int_{-\infty}^\infty g(x) dx{% endblock %}
  Teste Zeilenbedingung /$/ \(hier Backslash am Ende der Zeile\), wenn ja, dann lies die nächste Zeile ein \(N;\) und ersetze Backslash und Zeilenumbruch mit nichts \(s/\n//;\)

* Weitere Beispiele zu häufig auftretenden Anwendungsfällen sind unter [sourceforge](http://sed.sourceforge.net/sedfaq.html) zu finden.

#### awk

* ls -l \| awk 'BEGIN {sum=0} {sum=sum+$5} END {print sum}'
  summiere die 5. Spalte der ausgegebenen Zeilen des Befehls 'ls -l' auf und gebe die Summe am Ende aus



