# USB-Joyadapter_SMD  ![License: CC BY-SA 4.0](https://img.shields.io/badge/License-CC%20BY--SA%204.0-lightgrey.svg)
ATtiny basierter USB adapter für classic DB9 joysticks.

Die Ursprungsidee kommt aus dem forum64.de.  
https://www.forum64.de/index.php?thread/43055-usb-joystickadapter-neue-firmware-weiterentwicklung/

Die Software ist frei verfügbar und wird u.a. in dem [Thread](https://www.forum64.de/index.php?thread/43055-usb-joystickadapter-neue-firmware-weiterentwicklung/&postID=1390222#post1390222) zum Download angeboten, alle anderen Quellen, zumindest die, die ich gefunden habe, laufen ins Leere.
Daher stelle ich die Daten, der Vollständigkeit halber in dem Ordner [USB-Joystickadapter_THT](https://github.com/der-pw/USB-Joyadapter_SMD/tree/main/USB-Joystickadapter_THT) mit zur Verfügung. Darin enthalten sind sowohl die Software, zwei kompillierte Versionen, einmal für ATtiny2313 und ATtiny4313 und zusätzlich auch die Boarddaten der "alten" THT-Version.  
Ich bin aber nicht der Author!

Ich wollte eine SMD Version, möglichst kompakt aber noch gut zum Handlöten, haben.
Das Platinenlayout liegt als [KiCad-Projekt](https://github.com/der-pw/USB-Joyadapter_SMD/tree/main/kicad) vor. Exportierte Gerberdaten für Fertiger (bspw. [JLCPCB](https://jlcpcb.com/)) kann man ebenfalls [hier herunterladen](https://github.com/der-pw/USB-Joyadapter_SMD/raw/main/Joyadapter_SMD_gerber.zip).

![Draufsicht](https://github.com/der-pw/USB-Joyadapter_SMD/raw/main/images/Platine.jpeg)


### Programmierung
Ich habe das Hexfile mittels [AVRDUDESS](https://github.com/zkemble/AVRDUDESS) und einem ISP-Programmer auf den ATtiny geschrieben.
Die ISP-Schnittstelle wurde aus Platzgründen als SMD-Pads ausgeführt.
Eine Möglichkeit, man lötet Verbindungskabel zum Programmer an, ober man baut mit einer Buchsenleiste 6x1 RM2,54, 6 Pogo-Pins (P50-B1) und dem [Adapter](https://github.com/der-pw/USB-Joyadapter_SMD/blob/main/3D%20print/Pogo-Adapter.stl) eine Programmierklemme.
Da man das Teil prinzipiell nur einmal flashed und die Software ist m.E. ausentwickelt, kann man wohl eher kurz ein paar Kabel anlöten.

![Draufsicht](https://github.com/der-pw/USB-Joyadapter_SMD/raw/main/images/PogoAdapter.jpeg)

Die Fuses habe ich folgendermaßen gesetzt.  
**Low:** *0xCF*  
**High:** *0xDB*  
**Ext:** *0xFF*  
Fusecalc: https://www.engbedded.com/fusecalc/

### Gehäuse
Es gibt auch ein Gehäuse in der Variante mit den hochstehenden DB9-Buchsen.  
Zum Festschrauben beider Gehäusehälften wurden 2x12mm Linsenkopfschrauben verwendet.

![Gehäuse](https://github.com/der-pw/USB-Joyadapter_SMD/raw/main/images/Gehaeuse.jpeg)

Alternativ könnte man auch 90° gewinkelte DB9-Buchsen verwenden. Dann gucken die Kabel rechts und links aus dem Gehäuse heraus.
Ich wollte es erst einmal recht kompakt haben.
Vielleicht ergibt sich nochmal die Gelegenheit für ein Gehäuse mit 90° Buchsen.

### Teileliste:
https://www.reichelt.de/my/1803950  
Einige Teile sind (Stand 06.21) schwer zu bekommen.  

  
Ein großer **Dank** geht an das [forum64.de](https://www.forum64.de/) und seine hilfsbereiten Mitglieder. :thumbsup:
