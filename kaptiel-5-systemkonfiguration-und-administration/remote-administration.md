### Remote Administration

* Für die graphische Remote-Administration steht der tightvncserver bzw. der vnc4server unter Linux zur Verfügung. Das graphische System X11 erlaubt dabei über verschiedene Ports mehrere, voneinander unabhängige graphische Oberflächen zur Verfügung zu stellen. Der VNC-Server muss auf dem Remote-System mit den Inhalten einer Konfigurationsdatei \(/home/&lt;benutzername&gt;/.vnc/xstartup\) gestartet werden \( vnc4server :1\) und ist dann remote über den gewählten Port \(z.B. 5901\) erreichbar.

ssh -N -L 5903:localhost:5901 pi@10.8.9.129



puppet, ansible, chef

