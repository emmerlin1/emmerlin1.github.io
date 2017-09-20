### Installation von Linux im Desktop-/Serverumfeld

* In der Regel gibt es getrennte Installations-Abbilder für den Desktop- und Servereinsatz
* Das Installationsabbild kann auf DVD/CD gebrannt werden, ressourcenschonender ist allerdings die Benutzung eines USB-Sticks \([Windows↑](http://www.linuxliveusb.com/)/[Linux↑](https://wiki.ubuntuusers.de/Live-USB/)\)
* Falls bei eingestecktem USB-Stick weiterhin das bereits installierte System bootet, kommt man gewöhnlich während des Bootvorgangs über F8 auf das BIOS-Bootmenu von dem dann der USB-Stick ausgewählt werden kann
* Im BIOS-Bootmenu aktueller Linux-Distributionen und Mainboards kann zwischen der Installation im UEFI- und BIOS-Modus gewählt werden
* Linux kann auch per netboot-Installation installiert werden. Hierzu ist das netboot-image und ein korrekt eingerichteter TFTP- und DHCP-Server erforderlich. Zudem muss im BIOS des zu installierenden Rechners 'vom Netz booten' \(PXE-Boot\) aktiviert werden. \([Beispiel Ubuntu↑](https://help.ubuntu.com/community/Installation/Netboot)\)

### Vorgehen bei installiertem Windows und gewünschtem Dual-Boot

1. Windows-Partition sichern
2. Installations-Medium im Live-Modus starten und über gparted die Windows- bzw. Daten-Partition verkleinern oder zweite Festplatte einbauen
3. Installationsvorgang normal starten, Windows wird in der Regel erkannt und Linux in der freien Partition installiert
4. Ist noch kein Betriebssystem auf dem Rechner installiert wird dringend empfohlen, zuerst Windows und anschließend Linux zu installieren

### Installation in einer virtualisierten Umgebung

* Dies ist die einfachste Möglichkeit, Linuxdistributionen und die darin enthaltenen Programme intensiv zu testen. 
  1. VirtualBox installieren
  2. Neue Virtuelle Machine mit neuer virtueller Platte anlegen
  3. Virtuelles Linux-Distributions-ISO-Fileimage als DVD-Drive auswählen
  4. Virtuelle Maschine starten und Linux über das ISO-Image installieren

## 



