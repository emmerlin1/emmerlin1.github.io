### at

* Das Kommando **at** dient dazu, beliebige Shell-Befehle zu einem **späteren** Zeitpunkt **einmalig** ausführen zu lassen.

* Das Warteschlangenkommando atq zeigt alle aktiven at-Prozesse an

```
**[terminal]
**[prompt emmerlin@mypc:]**[path ~$ ]**[command at 02:00]
warning: commands will be executed using /bin/sh
**[prompt at> ]**[command tar czf /mnt/backup.tgz $HOME]
**[prompt at> ]**[command echo "Backup fertig" | logger]
**[prompt at> ]**[command <Ctrl+d>]
```








