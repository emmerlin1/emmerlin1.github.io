## Beschreibung der Verzeichnisstruktur unter Linux
<!--sec data-title="/bin" data-id="section0" data-collapse=true data-show=true show="Read" hide="Hide" ces-->
**/bin** enthält elementare Linux-Kommandos zur Systemverwaltung, die von allen Benutzern ausgeführt werden können. Weitere Programme befinden sich in **/usr/bin**.  
**/bin** kann auch einfach ein Link auf **/usr/bin** sein, womit die Trennung zwischen** /bin** und **/usr/bin** aufgehoben ist.
<!--endsec-->

<!--sec data-title="/boot" data-id="section1" data-collapse=true data-show=true ces-->
**/boot** enthält Dateien, die zum Booten des Systems verwendet werden. Zu finden ist hier **initrd** \(initial ramdisk\), ein temporäres Dateisystem, das die zum Start des Systems benötigten Dateien beinhaltet. Desweiteren enthält es die notwendigen Dateien des Bootloaders **grub**, den komprimierten Linux-Kernel \(**vmlinuz**\) und die Lookup-System-Tabelle \(**System.map**\).
<!--endsec-->

<!--sec data-title="/dev" data-id="section2" data-collapse=true data-show=true ces-->
**/dev** enthält alle Geräte-Dateien. Auf fast alle Hardware-Komponenten - etwa die serielle Schnittstelle oder eine Festplattenpartition – wird über sogenannte Device-Dateien zugegriffen. Dies spiegelt die Treiber-Philosophie von Linux wider:


> Everything is a File \(-Descriptor\)

Die Geräte werden dynamisch durch das **udev**-System eingerichtet. Das /dev-Verzeichnis befindet sich bei den meisten Distributionen in einer RAM-Disk, d. h., der Inhalt des Verzeichnisses wird bei jedem Neustart des Rechners neu generiert.

Das NULL-Device \(/dev/null\) wirkt als 'Mülleimer', in dem dort abgelegte Daten entsorgt werden können, wie z.B. Standard- und Fehlerausgaben \(2=stderr,1=stdout\):  

{% asciinema_local %}../asciinema/findredirect.json{% endasciinema_local %}
<!--endsec-->

<!--sec data-title="/etc" data-id="section3" data-collapse=true data-show=true ces-->
**/etc** enthält Konfigurationsdateien der über den Paketmanager der jeweiligen Distribution installierten Programmpakete. Innerhalb von /etc gibt es eine Menge an Unterverzeichnissen, über die die Konfigurationsdateien in einzelne Gruppen unterteilt werden - z.B. /etc/systemd für den Startup-Dienst systemd.

<!--endsec-->

<!--sec data-title="/home" data-id="section4" data-collapse=true data-show=true ces-->
Unter **/home** wird vom System das jeweilige Arbeitsverzeichnis eines Users angelegt. Das Heimatverzeichnis ist jenes Verzeichnis, in dem sich der Anwender nach dem Einloggen automatisch befindet und auf dessen Dateien er uneingeschränkte Zugriffsrechte hat. Ausgenommen ist der User 'root', dessen Heimatverzeichnis **/root** lautet.
Der Inhalt eines neu angelegten Arbeitsverzeichnisses kann durch den Inhalt des Template-Verzeichnisses **/etc/skel** automatisiert erweitert/ergänzt werden.


<!--endsec-->


