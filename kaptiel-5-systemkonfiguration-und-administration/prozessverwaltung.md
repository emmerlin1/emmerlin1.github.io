### Prozessverwaltung

* Prozesse können die Prozesszustände 'runnable', operating und sleeping besitzen.
* Wird ein **'Kindprozess'** beendet und wurde dessen Endestatus noch nicht vom **'Vaterprozess'** abgefragt, so wird er als sog. **Zombieprozess** vom Betriebssystem verwaltet
* Ausführliche Prozessinformationen können über den Befehl '**ps aux'** erfragt werden. Eine hierarchische Anzeige zeigt **'pstree'**, das ggfls. installiert werden muss.
* Prozesse mit dem gleichen Namen können über **'killall &lt;processname&gt;'** beendet werden. Die Option --signal &lt;SIGNAL&gt; spezifiziert das Signal, mit dem der Prozess beendet werden soll
* Über **'kill -&lt;signal&gt; &lt;PID&gt;'** kann ein bestimmter Prozess mit einem spezifizierbaren Signal beendet werden
* **'kill -l'** gibt die Liste verfügbarer Signale aus



