# Lokalisierung und Internationalisierung

* Umgebungsvariablen **LANGUAGE** und **LANG**
* Ausgabe der aktuellen Spracheinstellungen über den Befehl **locale**: LANG=de\_DE.UTF-8 LANGUAGE=de\_DE LC\_CTYPE="de\_DE.UTF-8" LC\_NUMERIC="de\_DE.UTF-8" LC\_TIME="de\_DE.UTF-8" LC\_COLLATE="de\_DE.UTF-8" LC\_MONETARY="de\_DE.UTF-8" LC\_MESSAGES="de\_DE.UTF-8" LC\_PAPER="de\_DE.UTF-8" LC\_NAME="de\_DE.UTF-8" LC\_ADDRESS="de\_DE.UTF-8" LC\_TELEPHONE="de\_DE.UTF-8" LC\_MEASUREMENT="de\_DE.UTF-8" LC\_IDENTIFICATION="de\_DE.UTF-8" LC\_ALL=
* Feineinstellungen können in der Datei **/etc/default/locale** vorgenommen werden \(Ubuntu\), z.B.: LANG=de\_DE.UTF-8 LC\_MESSAGES=POSIX
* /etc/timezone enthält die Zeitzone, die über den folgenden Befehl geändert werden kann \(Ubuntu\): `sudo dpkg-reconfigure tzdata   oder   sudo timedatectl set-timezone Europe/Berlin`
* verfügbare Zeitzonen sind in dem Verzeichnis **/usr/share/zoneinfo/** zu finden

