### Prozessverwaltung

* Prozesse können die Prozesszustände 'runnable', operating und sleeping besitzen.
* Wird ein **'Kindprozess'** beendet und wurde dessen Endestatus noch nicht vom **'Vaterprozess'** abgefragt, so wird er als sog. **Zombieprozess** vom Betriebssystem verwaltet
* Ausführliche Prozessinformationen können über den Befehl '**ps aux'** erfragt werden. Eine hierarchische Anzeige zeigt **'pstree'**, das ggfls. installiert werden muss.
* Über das Kommando **'pgrep'** kann man gezielt nach Prozess-ID's spezifizierbarer Prozessnamen suchen, z.B. '**pgrep -u &lt;username&gt; bash'**, mit 'pkill' kann man den gefundenen auch gleich beenden
* Prozesse mit dem gleichen Namen können über **'killall &lt;processname&gt;'** beendet werden. Die Option --signal &lt;SIGNAL&gt; spezifiziert das Signal, mit dem der Prozess beendet werden soll
* Über **'kill -&lt;signal&gt; &lt;PID&gt;'** kann ein bestimmter Prozess mit einem spezifizierbaren Signal beendet werden
* **'kill -l'** gibt die Liste verfügbarer Signale aus
* **'htop'** und **'top'** zeigen die Ressourcenbelegung \(CPU, RAM\) der Prozesse in einer wählbaren Sortierung an \(Refresh alle 2 Sekunden\)



