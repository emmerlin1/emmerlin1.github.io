### Der vi\(m\)

Der Editor vim \("vi" steht für "visual", improved vi\) ist ein bildschirmorientierter Editor, d. h. der Text ist in seiner aktuellen Version auf dem Bildschirm zu sehen.

![](/images/vi.png)

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

#### Arbeiten im Visual Mode \(Copy/Cut/Delete\)

| Zeichen | Bedeutung |
| :--- | :--- |
| v | Beginne, mittels Pfeil-/Bewegungstasten Zeichen zu markieren |
| V | Beginne, mittels Pfeil-/Bewegungstasten Zeilen zu markieren, Ende durch Drücken von y \(copy\), d \(cut/delete\) |



