## grep, sed, awk, sort, cut und regular expressions

Mittels grep, sed, awk, sort, cut und regulären Ausdrücken können Textausgaben gefiltert, durchsucht und ausgewertet werden. Im Folgenden werden einige Beispiele aufgeführt:

#### regular expressions

Eine kurze Zusammenfassung regulärer Ausdrücke ist beispielsweise [hier↑](https://www.cheatography.com/davechild/cheat-sheets/regular-expressions/pdf_bw/) zu finden. Eine vollständige Referenz ist ebenfalls [verfügbar↑](https://www.princeton.edu/~mlovett/reference/Regular-Expressions.pdf) und auch mindestens ein deutsches [Tutorial↑](https://www.danielfett.de/de/tutorials/tutorial-regulare-ausdrucke/). 

Im Folgenden sind wichtige Ausdrücke aufgeführt:

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
| C? | Zeichen/Ausdruck vor dem Fragezeichen ist optional \(0,1\) | |
| **Gruppierung** | **Bedeutung** | **Beispiel** |
| \[\] | eines der beinhalteten Zeichen ist vorhanden | '\[abc\]\[a-c\]\[stu\]' ist zutreffend für "cat" |
| \(\) | Gruppierung von Zeichen ist vorhanden | <code>'Das Wetter ist (toll&#124;richtig schlecht)'</code> ist zutreffend für "Das Wetter ist toll" |

#### grep

* [Beschreibung↑](https://www.gnu.org/software/grep/manual/grep.html) von grep (global regular expression print) in Form einer HTML-Seite

* grep liest eine Datei/Eingabe oder auch alle Dateien eines Verzeichnisbaums zeilenweise ein und gibt diejenigen Zeilen aus, die einer wählbaren Zeichen-Zusammensetzung entsprechen. Die Zeichenfolge kann auch reguläre Ausdrücke enthalten.

* `grep -n "boo" a_file`
  
  Gebe die Zeilen einer Datei a_file und deren Zeilenummer (-n) aus, die die Zeichenfolge "boo" enthalten
  
| Option | Bedeutung |
| :--- | :--- |
| -n | Gib die entsprechende Zeilennummer mit aus |
| -v | Gib inverses Ergebnis aus |
| -c | Gib nur die entsprechende Zeilennummer aus |
| -l | Gib nur die Dateinamen aus, in denen der Suchtext gefunden wurde |
| -i | ignoriere Groß-/Kleinschreibung |
| -x | exakte Übereinstimmung mit der gelesenen Zeile |
| -A2 | gibt die Zeile mit der Übereinstimmung und die 2 folgenden aus |


#### sed

* Ausführliche Beschreibungen und Beispiele zum stream editor sed sind [hier↑](http://www.grymoire.com/Unix/Sed.html) zu finden; sed wendet eine Folge von anzugebenden Kommandos auf Zeile für Zeile gelesene Daten einer Datei/Eingabe an.

* `cat text.txt | sed '=' | sed 'N;s/\n/. /'`

  Gib die Datei text.txt zeilenweise aus \(cat text.txt\), füge für jede Zeile die Zeilennummer mit Zeilenumbruch hinzu \( sed '='\), lies die nächste Zeile \(N;\) in die aktuelle Musterbehandlung (Pattern Space) ein und ersetze den Zeilenumbruch zu dieser angehängten Zeile mit '. '.

* `sed -e '/\\$/N; s/\\\n//;' text.txt`

  Teste Zeilenbedingung /\\\\$/ \(hier Backslash am Ende der Zeile\), wenn ja, dann lies die nächste Zeile ein \(N;\) und ersetze Backslash und Zeilenumbruch mit nichts \(s/\\\n//;\)

* Weitere Beispiele zu häufig auftretenden Anwendungsfällen sind unter [sourceforge↑](http://sed.sourceforge.net/sedfaq.html) und [tldp.org↑](http://tldp.org/LDP/Bash-Beginners-Guide/html/chap_05.html) zu finden.

#### awk

* awk ist ein Akronym der Nachnamen seiner drei Entwickler Aho, Weinberger, Kernighan; im Gegensatz zu sed stehen für awk Variablen, eingebaute Funktionen und eine Art Programmiersprache zur Verfügung. [Hier↑](https://www.gnu.org/s/gawk/manual/gawk.pdf) ist eine ausführliche Beschreibung von awk verfügbar.

* `ls -l | awk 'BEGIN {sum=0} {sum=sum+$5} END {print sum}'`

  summiere die 5. Spalte der ausgegebenen Zeilen des Befehls 'ls -l' auf und gebe die Summe am Ende aus


