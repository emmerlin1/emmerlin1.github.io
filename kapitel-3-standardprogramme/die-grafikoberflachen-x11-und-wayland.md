### Die Grafikoberflächen X11 und Wayland

* Das **X Window System X11**, dessen Grundlage das X-Protokoll ist  arbeitet nach dem **Client-/Server-Modell** und ermöglicht die Übertragung grafischer Grundoperationen über ein Netzverbindung.

* Es wurde von 1985-1987 am MIT \(Massachusetts Institute of Technology\) entwickelt.

* Unter Linux ist es unter der Implementierung mit Namen X.org bekannt.

* Der Austausch von Nachrichten erfolgt über **Unix-Domain-Sockets**

* X11 hat keine 3D-Grafikprimitive, somit stellt X11 für viele Clients nurmehr ein Stück Speicher auf der Grafikkarte zur Verfügung, in das der Client über direkte 3D-Operationen \(z.B. per OpenGL\) seine Grafikausgabe zeichnet.  
  Ein spezieller X11-Client kümmert sich dann um die richtige Reihenfolge der Ausgabe \(Compositor\)

* Der Nachfolger **Wayland** kümmert sich im wesentlichen nur noch um genau dieses Compositing und das Fenstermanagement, das Rendering \(3D-Operationen\) hingegen wird den Clients überlassen. Wayland ist somit sehr schlank und leicht erweiterbar.

* Ein sog. 'Displaymanager' wird häufig mit der grafischen Oberfläche zusammen gestartet und organisiert die verschiedenen 'Windowmanager' und die zugehörige Authentifizierung



