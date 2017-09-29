### anacron

* anacron läuft im Gegensatz zu cron nicht als Dienst sondern wird   
  1. von cron wie in /etc/cron.d/anacron spezifiziert,   
  2. beim Systemstart,   
  3. nach dem Aufwachen aus dem Power-Down-Mode,  
  4. und nach Änderung des Power-Management-Status \(Batterie/Netzbetrieb\) ausgeführt

* wann anacron zuletzt ausgeführt wurde kann von den Dateien /var/spool/anacron/cron.\[daily, weekly, monthly\] erfragt werden.

* 


