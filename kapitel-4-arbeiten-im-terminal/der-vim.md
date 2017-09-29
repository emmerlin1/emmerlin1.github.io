### Der vi\(m\)

Der Editor vim \("vi" steht für "visual", improved vi\) ist ein bildschirmorientierter Editor, d. h. der Text ist in seiner aktuellen Version auf dem Bildschirm zu sehen. Für eine ausführliche Auflistung der VIM-Befehle stehen zahlreiche [CheatSheets↑](https://gettextbook.download/CS 35L/Final Review/04_VIM.pdf) zur Verfügung, auch ein [graphischer Überblick](http://www.viemu.com/vi-vim-cheat-sheet.gif).

![](/images/vi.png)

VIM kann unter Einbeziehung verschiedener Plugins auch als IDE genutzt werden:
[VIM preconfigured as IDE](https://github.com/xmementoit/vim-ide)
#### ex-Befehle

| Befehl | Bedeutung |
| :--- | :--- |
| :w | Schreibe aktuellen Buffer in aktuelle Datei \(Speichern\) |
| :w! | Schreibe aktuellen Buffer in akt. Datei, ignoriere Schreibschutz |
| :wq | Schreibe aktuellen Buffer in aktuelle Datei und beende vim |
| :w filename | Schreibe aktuellen Buffer in Datei filename |
| w &gt;&gt; filename | Hänge aktuellen Buffer an Inhalt der Datei filename |
| :q | Beende Buffer, ohne zu speichern, Warnung bei vorhandenen Änderungen |
| :q! | Beende Buffer zwingend, ohne zu speichern, ignoriere Änderungen |
| :r filename | Text aus der angegebenen Datei nach der momentanen Zeile einfügen. |
| :e filename | Lade Datei filename als Buffer, leerer Buffer falls Datei nicht vorhanden |
| :buffers | Zeige offene Buffer an \(nummerierte Liste\) |
| :bn | Zeige nächsten offenen Buffer an |
| :vs | Halbiere Fenster vertikal |
| :10,100 s/^/\#/ | Füge am Anfang der Zeilen 10-100 eine Raute \# ein \(substitute mit regular expression\) |

#### Umschalten in den  Eingabemodus

| Zeichen | Bedeutung |
| :--- | :--- |
| a | Eingabe rechts vom Cursor \(append\) |
| A | Eingabe am Zeilenende |
| i | Engabe links vom Cursor \(insert\) |
| I | Eingaben am Zeilenanfang |
| o | Eingabe in der folgenden Zeile, Spalte 1 |
| O | Eingabe in der vorhergehenden Zeile, Spalte 1 |
| r | Ersetzung eines Zeichens |
| 5r | Ersetzung von 5 Zeichen mit dem einzugebenden Zeichen |
| R | Ersetzungseingabemodus |
| x | Lösche Zeichen unter dem Cursor |
| 5X | Lösche 5 Zeichen vor dem Cursor |
| /Wort | Suche Wort im aktuellen Buffer |
| n | Suche nächstes Wort im aktuellen Buffer |
| p | Füge Text der 'Zwischenablage' nach dem Cursor \(der Zeile\) ein |
| P | Füge Text der 'Zwischenablage' vor dem Cursor \(der Zeile\) ein |
| y | Kopiere aktuelle Zeile in 'Zwischenablage' |

#### Navigation

| Zeichen | Bedeutung |
| :--- | :--- |
| k | eine Zeile aufwärts navigieren |
| j | eine Zeile abwärts navigieren |
| l | ein Zeichen nach rechts |
| h | ein Zeichen nach links |
| w | ein Wort nach rechts |
| b | ein Wort nach links |
| Ctrl+f | eine Bildschirmseite nach unten |
| Ctrl+b | eine Bildschirmseite nach oben |
| gg | an den Anfang des Dokuments |
| GG | an das Ende des Dokuments |

#### Arbeiten im Visual Mode \(Copy/Cut/Delete\)

| Zeichen | Bedeutung |
| :--- | :--- |
| v | Beginne, mittels Pfeil-/Bewegungstasten Zeichen zu markieren, Ende durch Drücken von y \(copy\), d \(cut/delete\) |
| V | Beginne, mittels Pfeil-/Bewegungstasten Zeilen zu markieren, Ende durch Drücken von y \(copy\), d \(cut/delete\) |



