### Plattenbelegung und Systempartitionen

* **df -h** \| grep ^/dev/\[s,h,v\]d  
  Zeige den verfügbaren Plattenplatz der vorhandenen Festplatten und USB-Speicher an

* cat /proc/partitions  
  Zeige die dem System bekannten Partitionen. Die Spalten major/minor geben an, welcher Treiber für die jeweilige Partition zuständig ist.

* udevadm info --export-db  
  Anzeige aller GeräteInformationen des Dienstes udev \(user dev\)

* ls -l /dev/sda  
  Ausführliche Anzeige von Block-Device-Informationen zu sda \(u.a. Major 8, Minor 0 \)

* ls -l /sys/dev/block/8\:0/device/driver  
  Zeigt den Treiber an, der für das Management der major-/minor-Zuordnung verantwortlich ist

* sudo lshw -short   
  sudo lshw -html &gt; ~/System.html  
  zeigt Hardware-Informationen des Systems an



