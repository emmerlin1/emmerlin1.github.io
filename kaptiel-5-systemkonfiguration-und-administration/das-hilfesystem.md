### Das Hilfesystem

#### Der help-Befehl, die --help-Option

* Der **help-Befehl** ist ein in die Bash integriertes Kommando durch dessen Anwendung man eine Beschreibung von den verschiedenen Builtin-Funktionen der Bash bekommen kann, z.B. help exit oder help while
* Die Handbuchseiten \(**man-pages** \) bieten eine umfangreiche Hilfe zur Beschreibung von System- und anderen Programmen und auch von Bibliotheksfunktionen der glibc-API \(Standard-C-Bibliothek\).
  * Die man-pages befinden sich unter dem Verzeichnis **/usr/share/man**, man-pages für eigene Programme können in **/usr/local/share/**man platziert werden
  * Gliederung der Handbuchseiten:
    | Abschnitt | Inhalt |
    | :--- | :--- |
    | NAME | Kommandoname mit knapper Funktionsbeschreibung |
    | SYNOPSIS | Befehlssyntax |
    | DESCRIPTION | Ausführliche Beschreibung der Funktionsweise |
    | OPTIONS | Aufrufoptionen mit Beschreibung |
    | ARGUMENTS | Aufrufparameter |
    | FILES | Dateien mit Bezug zum Kommando |
    | EXAMPLES | Beispielung für die Anwendung des Kommandos |
    | SEE ALSO | Verweis auf verwandte man-pages |
    | DIAGNOSTICS | auftretende Fehlermeldungen |
    | COPYRIGHT | Autoren |
    | BUGS | Bekannte auftretende Fehler |
  * Die man-pages sind in unterschiedliche Sektionen eingeteilt:
    | Sektions-Nr. | Themenbereich |
    | :--- | :--- |
    | 1 | Benutzerkommandos |
    | 2 | Systemaufrufe |
    | 3 | Funktionen der Programmiersprache C |
    | 4 | Gerätedateien und Treiber |
    | 5 | Konfigurationsdateien und Dateiformate |
    | 6 | Spiele |
    | 7 | Diverses \(z.B. signal, ASCII-Tabelle\) |
    | 8 | Kommandos zur Systemadministration |
    | 9 | Kernel-Funktionen |
    | n | Benutzerdefinierte Kommandos |
  * Über den Befehl 'man -k &lt;Begriff&gt;' oder **'apropos &lt;Begriff&gt;' **erfährt man, in welchen Sektionen etwas zu dem jeweiligen Begriff zu finden ist \(z.B. **man -k printf**\)
  * Aufruf einer man-page mittels 'man &lt;Begriff&gt;', Beendigung mit der Taste 'q'



