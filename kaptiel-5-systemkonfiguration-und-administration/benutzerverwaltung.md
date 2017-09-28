### Benutzerverwaltung

* Unter Linux werden die Arbeitsverzeichnisse der angelegten Benutzer unter **/home/&lt;benutzername&gt;** angelegt, der Systemadministrator root erhält sein Arbeitsverzeichnis direkt unter **/root**

* Bei einigen Distributionen wie Ubuntu und Konsorten ist der root-User geschützt und kann dessen Administrationsgewalt nur über einen Standarduser mit den entsprechenden Berechtigungen erhalten; dies erfolgt nach dem Login des Standardusers über den Befehl 'sudo', der geschützten Kommandos voran gestellt wird, z.B.** 'sudo apt update'**

* Die Dateien in denen Benutzer, Gruppen und Passwörter hinterlegt werden lauten **/etc/passwd**, **/etc/group**, **/etc/shadow** und **/etc/gshadow**

* Es wird unterschieden zwischen System- und normalen Usern. Bei der Zuordnung von User-ID's \(UID\) erhalten Systemuser ID's im Bereich 0-999, wobei für den Benutzer root die 0 reserviert ist. Normale User sind dann ab der UID 1000 zu finden.

* Ein User ist einer **Hauptgruppe \(GID\)**, die den gleichen Namen trägt wie sein Username und ggfls. weiteren Gruppen zugeordnet. Über den Befehl **'id &lt;benutzername&gt;'** wird angezeigt, welcher UID, Hauptgruppe und welchen weiteren Gruppen ein Benutzer zugeordnet ist.

* Über den Befehl **adduser** können Benutzer angelegt werden. Dabei können etliche Usermerkmale wie Gruppenzugehörigkeit, UID, verschlüsseltes Arbeitsverzeichnis usw. dediziert festgelegt werden. Anzuwendende Usermerkmale können auch in der Datei **/etc/adduser.conf** hinterlegt werden.

* Über den Befehl **getent** können Einträge verschiedener Datenbanken angezeigt werden wie z.B. Gruppenzugehörigkeiten, Benutzer, Dienste etc.

* Die initialen Inhalte des Arbeitsverzeichnisses eines Benutzers können in dem Verzeichnis **/etc/skel** hinterlegt werden, woraus sie dann in das beim Anlegen des Benutzers erstellte Arbeitsverzeichnis /home/&lt;benutzername&gt; kopiert werden.

* Über die Pakete winbind, samba, libpam-winbind und libnss-winbind \(unter ubuntu\) kann ein Linux-Client in eine ActiveDirectory-Infrastruktur eingebunden werden



