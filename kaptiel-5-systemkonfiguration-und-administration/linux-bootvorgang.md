### Linux Bootvorgang

* Systemd hat mittlerweile SysV-Init/Upstart als Systemstart-Mechanismus abgelöst

* Systemd ist der erste Prozess, der gestartet wird \(PID 1\)

* Systemd erzeugt im wesentlichen zuerst alle zu verwendenden Kommunikationskanäle und anschließend alle Dienste ohne Rücksicht auf Abhängigkeiten. Somit kann der Bootvorgang beschleunigt werden

* Dienste können auch ohne die bereits aktiven realen Kommunikationskanäle frühzeitig gestartet werden, indem Systemd notwendige Sockets temporär selbst zur Verfügung stellt und den jeweiligen Dienst zu gegebener Zeit dann neu startet.

* Konfiguration der Systemd-Dienste unter **/lib/systemd/system/**

* Systemd-Units:

|asdf|sd|
 

* `systemctl`
  Liste der laufenden Systemd-verwalteten Dienste

* `systemctl status cron.service`
  Status des cron-Dienstes

* `systemctl stop cron.service`
  Stoppen des cron-Dienstes

* `systemctl start cron.service`
  Starten des cron-Dienstes

* `systemd-cgls`
  Baumübersicht über die Prozessgruppen (cgroups) von gestarteten Diensten

