# Beschreibung

**/bin** enthält elementare Linux-Kommandos zur Systemverwaltung, die von allen Benutzern ausgeführt werden können. Weitere Programme befinden sich in **/usr/bin**.  
**/bin** kann auch einfach ein Link auf **/usr/bin** sein, womit die Trennung zwischen **/bin** und **/usr/bin** aufgehoben ist. 

**/boot** enthält Dateien, die zum Booten des Systems verwendet werden. Zu finden ist hier **initrd** \(initial ramdisk\), ein temporäres Dateisystem, das die zum Start des Systems benötigten Dateien beinhaltet. Desweiteren enthält es die notwendigen Dateien des Bootloaders **grub**, den komprimierten Linux-Kernel \(**vmlinuz**\) und die Lookup-System-Tabelle \(**System.map**\). 

**/dev** enthält alle Geräte-Dateien. Auf fast alle Hardware-Komponenten - etwa die serielle Schnittstelle oder eine Festplattenpartition – wird über sogenannte Device-Dateien zugegriffen. Dies spiegelt die Treiber-Philosophie von Linux wider:

> Everything is a File \(-Descriptor\)

Die Geräte werden dynamisch durch das **udev**-Subsystem eingerichtet. Der Inhalt des /dev-Verzeichnisses wird in der Regel bei jedem Neustart des Rechners neu generiert.

Das NULL-Device \(/dev/null\) wirkt als 'Mülleimer', in dem dort abgelegte Daten entsorgt werden können, wie z.B. Standard- und Fehlerausgaben \(2=stderr,1=stdout\):  


**/etc** enthält Konfigurationsdateien der über den Paketmanager der jeweiligen Distribution installierten Programmpakete. Innerhalb von /etc gibt es eine Menge an Unterverzeichnissen, über die die Konfigurationsdateien in einzelne Gruppen unterteilt werden - z.B. /etc/systemd für den Startup-Dienst systemd. 

Unter **/home** wird vom System das jeweilige Arbeitsverzeichnis eines neu erstellten Users angelegt. Das Heimatverzeichnis ist das Verzeichnis, in dem sich der Anwender nach dem Einloggen automatisch befindet und auf dessen Dateien er uneingeschränkten Zugriff hat. Ausgenommen ist der User 'root', dessen Heimatverzeichnis **/root** lautet.

Der Inhalt eines neu angelegten Arbeitsverzeichnisses kann durch den Inhalt des Template-Verzeichnisses **/etc/skel** automatisiert erweitert/ergänzt werden. Im Arbeitsverzeichnis eines Users werden auch userbezogene Ordner und Dateien angelegt, denen ein Punkt vorangestellt ist \(z.B. .config, .cache oder .local\). Hierdurch können insbesondere userbezogene Konfigurationseinstellungen gespeichert werden. 

**/lib** enthält Kernel-Bibliotheken und diejenigen Shared Libraries, die für das Booten des Systems und die Ausführung der in /bin und /sbin liegenden Programme notwendig sind. Die Endung von Bibliotheken lautet auf .so. Kernelmodule befinden sich im Unterverzeichnis /lib/modules/'kernel-version'. 

Unter **/media** werden externe Medien wie USB-Sticks/-Festplatten, SD-Karten etc. eingebunden, deren Gerätezuordnung und Partitionierung über 'cat /proc/partitions' und nach der Einbindung der Partition über 'df' einsehbar ist. 

Das Verzeichnis **/mnt** sollte mittlerweile nur noch für die vorübergehende Einbindung von Dateisystemen durch den User 'root' verwendet werden. \('sudo mount /dev/sdc3 /mnt'\) 

**/opt** ist für Zusatzpakete vorgesehen, wird allerdings selten von Programmpaketen der installierten Distribution verwendet. Öfter kommt es vor, dass über Installationsskripte installierte Software in diesem Verzeichnis seinen Platz findet \(wie z.B. eagle, android-studio, arduino, skypeforlinux etc.\) 

**/proc** ist ein Pseudo Prozess-Informations-Dateisystem und enthält Laufzeit-Informationen des Systems \(Prozesse, RAM-Verteilung, Hardwarekonfiguration etc.\). Es dient somit als Kontroll- und Informationszentrum bezogen auf den Kernel.

Viele Systemaufrufe \(z.B. lsmod\) rufen einfach nur Dateiinhalte dieses Verzeichnisses ab. Auch Kernelparameter können über hier vorhandene Dateien abgerufen/verändert werden. Ein wesentliches Merkmal der hier vorhandenen Dateien ist, dass sie \(abgesehen von kcore und weniger anderer\) die Größe 0 aufweisen. Sie fungieren sozusagen als Zeiger auf aktuelle Kernelinformationen.

Jeder Prozessordner wird durch seine Prozess-ID abgebildet und enthält Informationen über die vom Prozess verwendeten Systemressourcen. 

Das root-Userverzeichnis wird getrennt von allen anderen Userverzeichnissen direkt unter der Wurzel des Dateisystems verwaltet 

**/run** ist ein temporäres Dateisystem, dessen Inhalt beim Neustart verloren geht und flüchtige Prozesslaufzeitinformationen enthält, die frühzeitig im Booprozess verfügbar sind. 

Dieses Verzeichnis enthält wichtige Systemkommandos, die dem superuser 'root' vorbehalten sind. 

Das Verzeichnis **/srv** enthält Daten für Serveranwendungen wie beispielsweise Web- und FTP-Server. 

enthält ab Kernel 2.6 das sysfs-Dateisystem. Es liefert ähnlich wie das proc-Dateisystem Laufzeit-Informationen, deren Inhalt jedoch auf Informationen von Kernelstrukturen und deren Transport in den Userspace fokussiert ist.

Dabei werden so gut wie alle verfügbaren Ressourcen abgedeckt. 

**/tmp** enthält temporäre Dateien. Oft werden temporäre Dateien aber auch in /var/tmp gespeichert. 

In **/usr** \(unix system ressources\) findet man alle Anwendungsprogramme, Bibliotheken, das X-System, installierten Quellcode etc..

Der Inhalt verändert sich in der Regel nur bei Paket-\(De\)installationen und Updates.

| Verzeichnis | Inhalt |
| :--- | :--- |
| /usr/bin | ausführbare Programme |
| /usr/include | C-Include-Dateien |
| /usr/lib\[64\] | diverse Libraries, außerdem zahllose Unterverzeichnisse für C-Compiler, diverse andere Programmiersprachen, große Programmpakete wie emacs oder LATEX etc. |
| /usr/local | Anwendungen und Dateien, die nicht unmittelbar zur Linux-Distribution- gehören oder später installiert wurden |
| /usr/sbin | nur von 'root' ausführbare Programme |
| /usr/share | architekturunabhängige Daten, Dokumentation |
| /usr/src | Quellcode zum Linux-Kernel und anderen Programmen |

Sich systembedingt verändernde Anwendungsdaten befinden sich im Verzeichnis **/var**.

Wichtige Unterverzeichnisse sind **adm** _\(distributionsabhängige Administrationsdateien\)_, **lock** _\(Locking-Dateien zum Zugriffsschutz auf Devices\)_, **log** _\(Logging-Dateien\), mail \(E-Mail-Dateien\)_, **run** _\(Laufzeit-Dateien mit Prozess-IDs von manchen Systemdiensten\)_ und **spool** _\(zwischengespeicherte Druckdateien, News-Dateien etc.\)_.

## Beispiel zu /dev/null:

