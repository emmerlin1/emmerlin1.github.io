### anacron

* anacron läuft im Gegensatz zu cron nicht als Dienst sondern wird \(hier unter ubuntu\)  
  1. von cron wie in /etc/cron.d/anacron spezifiziert einmal pro Tag um 07:30 Uhr (wenn der Rechner da läuft),  
  2. nach dem Systemstart mit der in /etc/anacrontab angegebenen Verzögerung,  
  3. nach dem Aufwachen aus dem Power-Down-Mode mit der in /etc/anacrontab angegebenen Verzögerung,  
  4. und nach Änderung des Power-Management-Status \(Batterie/Netzbetrieb\)  mit der in /etc/anacrontab angegebenen Verzögerung ausgeführt

* wann anacron zuletzt ausgeführt wurde kann von den Dateien /var/spool/anacron/cron.\[daily, weekly, monthly\] erfragt werden. Die hier hinterlegten Timstamps verwendet anacron, um zu entscheiden, ob ein Befehl auszuführen ist

* 


