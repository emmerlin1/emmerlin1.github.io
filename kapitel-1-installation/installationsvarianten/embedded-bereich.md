### Installation von Linux auf SD-Karte/eMMC:

* **unter Linux:**

  ```
  dd bs=4M if=2017-08-16-raspbian-stretch.img of=/dev/sdX conv=fsync
  ```

  * **/dev/sdX** ist dabei das Device über das der USB-Stick angesprochen wird, über den Befehl 'cat /proc/partitions' vor und nach dem Einstecken des Sticks kann der Device-Name ermittelt werden \(z.B. /dev/sdg\)

  * unter if \(input-file\) wird der Name des Installations-Images angegeben

* **unter Windows:  **
  [win32diskmanager](https://sourceforge.net/projects/win32diskimager/)



