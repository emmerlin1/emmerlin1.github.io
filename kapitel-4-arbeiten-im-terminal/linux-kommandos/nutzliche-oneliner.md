### Nützliche Oneliner

* `find\bin \usr\bin -type f -exec file {} \; |grep"shell" |wc-l`  
  Durchsuche \(find\) die Verzeichnisse /bin und /usr/bin nach allen Dateien und füttere mit jeder gefundenen Datei den Befehl file;  
  dessen Ausgabe wird nach dem Wort "shell" durchsucht \(grep\), wird es gefunden, dann summiert der Befehl wc diese Zeile auf;  
  d.h. wir erhalten die **Gesamtanzahl** von Shellskripten in den beiden durchsuchten Verzeichnissen

* cut -d ':' -f 1,3 /etc/passwd \| sort -t ':' -k2n - \| tr ':' '\t'  
  extrahiere den Usernamen und die UID der in /etc/passwd vorhandenen User

* tr -c a-zA-Z '\n' &lt; Readme1.txt  \| sed '/^$/d' \| sort \| uniq -i -c  
  Zähle in einer Textdatei, wie oft die einzelnen Worte dort vorkommen

* sort m1.txt \| join - m2.txt  
  Füge eine Datei einer anderen sortierten Datei an

* ps aux \| awk '{if \($5 != 0 \) print $2,$5,$6,$11}' \| sort -k2n  
  Anzeige der Prozesse und deren Speicheranforderungen

* du -sk /var/log/\* \| sort -r -n \| head -10  
  Anzeige der Größe von Dateien und Verzeichnisinhalten, sortiert und beschränkt auf die größten 10 Werte

* cat ~/.bash\_history \| tr "\\|\;" "\n" \| sed -e "s/^ //g" \| cut -d " "  
  Dursuchen der Command-History-Datei und Zählung, wie oft eine Befehl aufgerufen wurde

* find -not -empty -type f -printf "%s\n" \| sort -rn \| uniq -d \| xargs -I{} -n1 find -type f -size {}c -print0 \| xargs -0 md5sum \| sort \| uniq -w32 --all-repeated=separate  
  Finde und beseitige Dateiduplikate in einem Verzeichnisbaum



