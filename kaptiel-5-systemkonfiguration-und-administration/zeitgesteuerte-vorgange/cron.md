### cron

Der cron-Dienst dient der Ausführung von wiederkehrenden Aufgaben. Die Bearbeitung der Konfiguration erfolgt user-bezogen über den Befehl **crontab -e**, wobei das Ergebnis im Verzeichnis **/var/spool/cron/crontabs/&lt;username&gt;** gespeichert wird.

Die Crontab-Einträge werden in der Form Minute, Stunde, Tag, Monat, Wochentag, auszuführender Befehl eingefügt und anschließend gespeichert und der verwendete Editor geschlossen

```
*     *     *     *     *  Befehl der ausgeführt werden soll
-     -     -     -     -
|     |     |     |     |
|     |     |     |     +----- Wochentag (0 - 7) (Sonntag ist 0 und 7; oder Namen, siehe unten)
|     |     |     +------- Monat (1 - 12)
|     |     +--------- Tag (1 - 31)
|     +----------- Stunde (0 - 23)
+------------- Minute (0 - 59; oder Namen, siehe unten)
```





