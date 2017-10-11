### Linux Bootvorgang

* Im Verlauf des Bootvorgangs werden verschiedene '**runlevels**' durchlaufen

  * **0: **
    Shutdown-level
  * **S:** 
    Single-User-Runlevel \(niedrigster Level für Wartungsarbeiten\)
  * **1:** 
    Single-User Runlevel, oft identisch zu 'S'
  * **2:** 
    Lokaler Mehrnutzerbetrieb ohne Netzwerk mit lokalen Ressourcen, manchmal wird auch Netzwerk konfiguriert
  * **3:** 
    Netzwerkbetrieb, über das Netzwerk erreichbare Ressourcen sind verfügbar
  * **4:** 
    üblicherweise nicht verwendet, kann aber für Dienste genutzt werden
  * **5:** 
    zusätzliche Bereitstellung der grafischen Oberfläche
  * **6:** 
    Reboot, Netzverbindungen werden geschlossen, Dateipuffer geschrieben und Mounts ausgehängt

* Systemd hat mittlerweile SysV-Init/Upstart als Systemstart-Mechanismus abgelöst

* Systemd ist der erste Prozess, der gestartet wird \(PID 1\)

* Systemd erzeugt im wesentlichen zuerst alle zu verwendenden Kommunikationskanäle und anschließend alle Dienste ohne Rücksicht auf Abhängigkeiten. Somit kann der Bootvorgang beschleunigt werden

* Dienste können auch ohne die bereits aktiven realen Kommunikationskanäle frühzeitig gestartet werden, indem Systemd für den Start notwendige Sockets temporär selbst zur Verfügung stellt und den jeweiligen Dienst zu gegebener Zeit dann neu startet.

* Konfiguration der Systemd-Dienste unter **/lib/systemd/system/** oder bevorzugt behandelt und bei einem Update nicht überschrieben unter **/etc/systemd/system/**

* Konfiguration von sog. **Systemd-Units** \(über ini-ähnliches Dateiformat\):

  | Typ | Beschreibung |
  | :--- | :--- |
  | .device | Legt Gerätedateien an |
  | .mount | Ein- und Aushängen von Dateisystemen |
  | .path | Startet die Unit via inotify |
  | .network | Für die Konfiguration von Netzwerken via networkd |
  | .service | Für Dienste |
  | .socket | Stellt Verbindungen zwischen Prozessen her |
  | .target | Definiert eine Gruppe von Units |
  | .timer | Für wiederkehrende Aufgaben, ähnlich cron-Jobs |

* `systemctl`  
  Liste der laufenden Systemd-verwalteten Dienste

* `systemctl status cron.service`  
  Status des cron-Dienstes

* `systemctl stop cron.service`  
  Stoppen des cron-Dienstes

* `systemctl start cron.service`  
  Starten des cron-Dienstes

* `systemd-cgls`  
  Baumübersicht über die Prozessgruppen \(cgroups\) von gestarteten Diensten



