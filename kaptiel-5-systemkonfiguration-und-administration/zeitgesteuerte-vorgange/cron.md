### cron

Der cron-Dienst dient der Ausführung von wiederkehrenden Aufgaben. Die Bearbeitung der Konfiguration erfolgt user-bezogen über den Befehl **crontab -e**, wobei das Ergebnis im Verzeichnis **/var/spool/cron/crontabs/&lt;username&gt;** gespeichert wird.

Die Crontab-Einträge werden in der Form Minute, Stunde, Tag, Monat, Wochentag, auszuführender Befehl eingefügt und anschließend gespeichert und der verwendete Editor geschlossen



```
*     *     *     *     *  auszuführender Befehl
-     -     -     -     -
|     |     |     |     |
|     |     |     |     +--- Wochentag (0 - 7) (Sonntag ist 0 und 7; oder Sun, Mon, Tue, Wed, Thu, Fri, Sat)
|     |     |     +--------- Monat (1 - 12)
|     |     +--------------- Tag (1 - 31)
|     +--------------------- Stunde (0 - 23)
+--------------------------- Minute (0 - 59; */5 entspricht alle 5 Minuten)
```



