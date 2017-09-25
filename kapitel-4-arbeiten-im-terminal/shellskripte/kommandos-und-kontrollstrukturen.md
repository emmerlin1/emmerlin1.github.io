### Kommandos und Kontrollstrukturen

* Verzweigungen und Schleifen verwenden als 'Weichenstellung' für den weiteren Ablauf \(Steuerungsgröße\) grundsätzlich nicht den Wert 'true' oder 'false' sondern den Rückgabewert von Programmen, z.B.
  `test -d "$HOME/.config" && echo "existiert"`
  
* Dabei gilt der Rückgabewert 0 für "Erfolg" und 1-255 als Misserfolg:

| Wert | Bedeutung |
| :--- | :--- |
| **0** | Erfolg |
| **1** | allgemeiner Fehler |
| **2** |  |
| **3-126** | frei wählbar durch den User \(z.B. exit 25\) |
| **127** | aufgerufener Befehl/Programm wurde nicht gefunden |
| **128** | Ungültiges Argument für exit verwendet \(z.B. exit 2.5 |
| **129-192** | Programmabbruch durch Signal 'Wert'-128, Signalübersicht durch Befehl **kill -l** |



