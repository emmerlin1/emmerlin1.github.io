# Shellskripte

[Variable↓](variable.md)

[Arithmetische Ausdrücke↓](https://github.com/emmerlin1/linux_einfuehrung/tree/72fda4173847371029c87102c18e1976781419d0/kapitel-4-arbeiten-im-terminal/shellskripte/arithmetische-ausdrucke.md)

[Kommandos und Kontrollstrukturen↓](kommandos-und-kontrollstrukturen.md)

[Shellfunktionen↓](shellfunktionen.md)

Shellskripte bieten die Möglichkeit, Befehlsketten nacheinander strukturiert über **einen** Aufruf ausführen und dabei weiterführende Funktionselemente wie Kontrollstrukturen und arithmetische Ausdrücke nutzen zu können. Da die Shell unter Linux eine tragende Rolle spielt, können somit hierüber auch komplexere Konfigurations- und Administrationsaufgaben automatisiert werden. Man sollte sich dabei jedoch immer der Durchschlagfähigkeit von möglichen Skriptfehlern bewusst sein.

Shellskripte können, nachdem sie mittels' chmod +x skriptname.sh' ausführbar gemacht wurden über '.**/skriptname.sh**' als eigener Kindprozess gestartet werden. Eine weitere Möglichkeit wäre, das Skript innerhalb des aktuellen Shellkontextes mittel '**source skriptname.sh**' auszuführen. Eine beliebte Anwendungsvariante ist die Skriptverwendung für geplante Aufgaben \(crontab\).

Shellskripte können komplexe Vorgänge beinhalten, die dann auch entsprechend über das Kommentarzeichen '\#' umfangreich dokumentiert werden sollten. Größere Skripte sollten mit einem Kommentarblock anfangen, der beschreibt, wie das Skript heißt, wie es aufgerufen werden muss, was es tun soll, Author usw.

Ein Bash-Guide für Anfänger ist u.a. [hier↑](https://wiki.ubuntuusers.de/Shell/Bash-Skripting-Guide_f%C3%BCr_Anf%C3%A4nger/) zu finden.

