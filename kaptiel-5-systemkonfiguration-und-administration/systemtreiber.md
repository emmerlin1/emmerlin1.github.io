# Systemtreiber

* Liste der geladenen Treiber über `lsmod`
* Zuordnung der Treiber über `lshw -c <class>`, z.B. `lshw -c display`
* Analyse des sys-Filesystems über das Paket 'sysfsutils': `systool` \(Gesamtübersicht\), `systool -v -m qxl` \(Anzeige aller Attribute des Moduls qxl\)
* Nutzung der [libudev](https://www.freedesktop.org/software/systemd/man/libudev.html)-Bibiliothek in C-Programmen, um auf sysfs-Elemente zugreifen zu können



