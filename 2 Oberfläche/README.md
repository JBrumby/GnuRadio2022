In diesem Flussplan geht es darum, 
die Oberfläche des Programms aufzuräumen
indem die Gui-Elemente angeordnet werden.

das passiert über die Variable "gui-hint"

The format ist:
(row, column, row span, column span)

wobei:
- row, colum >= 0
- row span, column span >= 1

siehe: https://wiki.gnuradio.org/index.php/GUI_Hint

Das Konzept erscheint mir so einfach, dass es kaum Erklärung bedarf.

- Die erste Zahl gibt an in welcher Reihe das Element stehen soll.
- Die zweite Zahl gibt an in welcher Spalte das Element stehn soll.
- die dritte gibt an, über wieviele Spalten sich ein Element erstrecken soll, 
- die vierte Zahl gibt an, wieviel Reihen übereinander eingenommen werden soll.

Das ganze entsteht dynamisch es muss nichts vorab konfiguriert werden

Man kann mehrere Elemente in einem "QT-Gui-Tab-Widget"-Block zusammen fassen.
mit dem Gui Hint kann ebenfalls adressiert werden, in welchem Tab von welcher Box sich das Element befindetn soll.
Außer diesen beiden Gestaltungsmöglichkeiten: 
- Raster und 
- Zusammenfassung eines Rasters von Elementen in Tabs 
gibt es keine grafischen Gestaltungsmöaglichkeiten.

Eine Box ist ein QT-gui-tabbed Widget mit nur einem Tab. Na ja. Wenig,  genügt aber.

Das wäre damit auch geklärt

Viele Grüße
