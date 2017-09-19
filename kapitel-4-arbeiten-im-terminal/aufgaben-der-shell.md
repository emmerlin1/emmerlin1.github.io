

### Aufgaben der Shell   

* Annahme der Kommandozeile vom Terminal, Entschlüsselung des Kommandos und Aufteilung in seine Einzelkomponenten \(Kommandoname, Optionen, Parameter\) 
* Suchen und Starten des angegebenen Programms. Der Suchweg wird durch die Shellvariable PATH vorgegeben.
* Steuerung der Ein- und Ausgabe des Terminals. UNIX ist als Dialogsystem konzipiert und war ursprünglich für den Betrieb mit Fernschreibern \(Teletype\) und Datensichtgerät konzipiert. Diese sogenannten "Terminals" findet man heute noch in den logischen Terminals, z. B.:

        den Konsolen, die dem Bildschirm und der Tastatur des PCs zugeordnet sind,

        den Pseudo-Terminals, die einer Telnet-Verbindung zugeordnet werden oder

        den X-Terminal-Fenstern auf der grafischen Benutzeroberfläche. 

    Daher gibt es drei Standarddateien, die dem aktuellen Terminal zugeordnet sind:

        Standardeingabe \(Tastatur, stdin\)

        Standardausgabe \(Bildschirm, stdout\)

        Standard-Fehlerausgabe \(Bildschirm, stderr\) 

    Die Shell kann angewiesen werden, die Ein- und Ausgaben umzuleiten.

    Ersetzung von Sonderzeichen und Befehlssubstitution. Kommandoeingaben können durch Sonderzeichen erweitert und der Kommandostring kann selbst durch die Shell expandiert werden.

    Ablaufsteuerung. Die Shell beherrscht viele Strukturen, wie man sie von Programmiersprachen her kennt \(Test, bedingte Anweisung, Schleifen, Variablen, Rechenanweisungen\).

    Erzeugen von Kind- und Hintergrundprozessen. 

