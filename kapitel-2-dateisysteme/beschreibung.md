## Beschreibung der Verzeichnisstruktur unter Linux

### bin

**/bin** enthält elementare Linux-Kommandos zur Systemverwaltung, die von allen Benutzern ausgeführt werden können. Weitere Programme befinden sich in **/usr/bin**.   
**/bin** kann auch einfach ein Link auf **/usr/bin** sein, womit die Trennung zwischen** /bin** und **/usr/bin** aufgehoben ist.

### boot

enthält Dateien, die zum Booten des Systems verwendet werden. Zu finden ist hier **initrd** \(initial ramdisk\), ein temporäres Dateisystem, das die zum Start des Systems benötigten Dateien beinhaltet. Desweiteren enthält es die notwendigen Dateien des Bootloaders grub, den komprimierten Linux-Kernel \(**vmlinuz**\) und die Lookup-System-Tabelle \(**System.map**\). 

### dev

enthält alle Device-Dateien. Auf fast alle Hardware-Komponenten –

etwa die serielle Schnittstelle oder eine Festplattenpartition – wird

über sogenannte Device-Dateien zugegriffen. Diese werden dynamisch

durch das udev-System eingerichtet \(siehe Abschnitt 13.10, »Device-

Dateien«\). Bei den meisten Distributionen befindet sich das /dev-Ver-

zeichnis in einer RAM-Disk, d. h., der Inhalt des Verzeichnisses bleibt bei

einem Neustart des Rechners nicht erhalten.





