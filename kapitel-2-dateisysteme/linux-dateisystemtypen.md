## Dateisystemtypen

* **EXT3    
  **Nachfolger von EXT2 mit Journaling-Funktion \(nur die letzten Transaktionen vor einem Absturz müssen rückgängig gemacht werden\); ist abwärtskompatibel zu ext2

* **EXT4    
  **seit Kernelversion 2.6.28 als stabil eingestuft;  
    im Vergleich zu EXT3:

  * Verbesserte Performance 
  * Verbesserte Datensicherheit
  * Zeitstempel im Nanosekunden-Bereich statt nur im Sekundenbereich
  * Unlimitierte Anzahl an Unterverzeichnissen
  * Integrierte Verschlüsselung ab Kernel 4.1...

* **Btrfs**

  * Speicherung von Metadaten und Datenblöcken in zwei Baumstrukturen
  * integrierte RAID-Funktion
  * Copy on Write
  * Snapshots
  * Checksummen zur Absicherung

* **XFS  
  **ausgereift und stabil, im Desktop-Bereich nicht sehr verbreitet; Rechteverwaltung, Journaling

* **JFS  
  **von IBM; Journaling File System; Defragmentierung unter Linux wird nicht unterstützt

* **ReiserFS, Reiser4  
  **erstes Journaling-Dateisystem, das standardmäßig im Linux-Kernel enthalten war \(2.4.1\), Reiser4 ist Nachfolger von ReiserFS Version 3

* **ZFS  
  **128-Bit-Dateisystem; Ähnlichkeiten zu Btrfs, Einsatz im Server-Bereich und in Rechenzentren; 4GB freier Arbeitsspeicher empfohlen; 



