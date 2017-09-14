## Archivierung und Komprimierung

| Befehl | Bedeutung |
| :--- | :--- |
| gzip myfile.txt | Datei wird gz-komprimiert und durch komprimierte Datei ersetzt |
| gzip -l myfile.txt.gz | zeigt Kompressionsverhältnis der komprimierten Datei an |
| gzip myfile.txt.gz | Wiederherstellung der Originaldatei |
|  |  |
| bzip2 und xz | Alternativen zu gzip |
|  |  |
| tar czf myarchive.tgz verzeichnisname | Erstellung eines gzip-gezippten Tar-Archivs einer Verzeichnisstruktur |
| tar xzf myarchive.tgz | Entpacken eines gzip-gezippten Tar-Archivs |
| tar tzf myarchive.tgz | Anzeigen des Inhalts eines gzip-gezippten Tar-Archivs |
|  |  |
| find . -name "\*.txt" \| cpio -ov &gt;archive.cpio | Archiviere gefundene .txt-Dateien mit cpio in archive.cpio |
| cpio -iv &lt;archive.cpio | Entpacke cpio-Archiv |



