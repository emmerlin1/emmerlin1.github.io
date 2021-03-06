# Paketverwaltung

* Unter den verschiedenen Linux-Distributionen gibt es die verschiedensten Paketmanager:
  * **RPM** \(Red Hat Package Manager\) für RedHat, Mandriva und OpenSuSE
  * **dpkg** \(Debian PaketaManager\) und **apt** \(Advanced Package Tool\) bzw. **aptitude** für Debian/Ubuntu
  * **Portage** für Gentoo
  * **Portsystem** für BSD
* Verschiedene GUI-Oberflächen sollen die Benutzung der Paketmanager erleichtern.
* Bei den meisten Distributionen werden Abhängigkeiten unter den Paketen automatisch aufgelöst, somit läuft die Installation und das Upgrade von Paketen in der Regel vollautomatisch und ohne Konflikte ab.
* Verschiedene Repositories \(Softwarearchive\) stellen lizenzrechtlich klassifizierte bzw. von verschiedenen Seiten unterstützte Pakettypen bereit:
  * main:  offiziell unterstützte Pakete mit freier Lizenz
  * _**restricted**_: offiziell unterstützte Pakete, die nicht einer freien Lizenz unterliegen
  * _**universe**_: von der Linux-Community unterstützte Pakete unter freier Lizenz
  * _**multiverse**_: nicht-freie Software
  * ...
* Beispielhafte Abhandlung von updates mit apt:
  * `sudo apt update`
  * `sudo apt upgrade`
* Release-Upgrade unter Ubuntu: `sudo do-release-upgrade`
* nicht-offizielle Repositories einbinden \(personal package archive, keine Unterstützung durch die Distribution\):
  * `sudo add-apt-repository ppa:ubuntu-lxc/lxd-stable`
  * `sudo apt update`
  * `sudo apt install golang`
* Suche, zu welchem Paket eine Datei gehört: `dpkg -S <filename>`
* Inhalt eine Pakets anzeigen lassen: `dpkg-query -L <package-name>`
* Anzeige aller installierten Pakete: `apt list --installed`
* Auswahl unter verschiedenen Programm-Alternativen \(etc/alternatives\) über das utility update-alternatives: `update-alternatives --config editor`
* 
