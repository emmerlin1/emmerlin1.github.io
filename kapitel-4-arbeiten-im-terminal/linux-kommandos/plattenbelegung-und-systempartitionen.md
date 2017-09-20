### Plattenbelegung und Systempartitionen

* df -h \| grep ^/dev/\[s,h,v\]d  
  Zeige den verfügbaren Plattenplatz der vorhandenen Festplatten und USB-Speicher an

* cat /proc/partitions  
  Zeige die dem System bekannten Partitionen. Die Spalten major/minor geben an, welcher Treiber für die jeweilige Partition zuständig ist.  
  udevadm info --export-db  
  ls -l /dev/sda --&gt; shows major, minor  
  ls -l /sys/dev/block/8\:0/device/driver --&gt; shows driver responsible for major, minor



