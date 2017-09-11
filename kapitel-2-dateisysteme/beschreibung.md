## Beschreibung der Verzeichnisstruktur unter Linux

### bin

**/bin** enthält elementare Linux-Kommandos zur Systemverwaltung, die von allen Benutzern ausgeführt werden können. Weitere Programme befinden sich in **/usr/bin**.  
**/bin** kann auch einfach ein Link auf **/usr/bin** sein, womit die Trennung zwischen** /bin** und **/usr/bin** aufgehoben ist.

### /boot

enthält Dateien, die zum Booten des Systems verwendet werden. Zu finden ist hier **initrd** \(initial ramdisk\), ein temporäres Dateisystem, das die zum Start des Systems benötigten Dateien beinhaltet. Desweiteren enthält es die notwendigen Dateien des Bootloaders **grub**, den komprimierten Linux-Kernel \(**vmlinuz**\) und die Lookup-System-Tabelle \(**System.map**\).

### /dev

enthält alle Geräte-Dateien. Auf fast alle Hardware-Komponenten - etwa die serielle Schnittstelle oder eine Festplattenpartition – wird über sogenannte Device-Dateien zugegriffen. Dies spiegelt die Treiber-Philosophie von Linux wider:

> Everything is a File \(-Descriptor\)

Die Geräte werden dynamisch durch das **udev**-System eingerichtet. Das /dev-Verzeichnis befindet sich bei den meisten Distributionen in einer RAM-Disk, d. h., der Inhalt des Verzeichnisses wird bei jedem Neustart des Rechners neu generiert.

Das NULL-Device \(/dev/null\) wirkt als 'Mülleimer', in dem dort abgelegte Daten entsorgt werden können, wie z.B. Standard- und Fehlerausgaben \(2=stderr,1=stdout\):  
`script.sh > /dev/null 2>&1`

