---
layout: page
published: true
---
## Was unterscheidet funktionale von objektorientierter Programmierung?

Bei der funktionalen Programmierung steht die Funktion und die Datenmengen auf denen sie definiert ist im Mittelpunkt. Es gibt keine Prozeduren, keine Objekte und dementsprechend keine Methoden.
  
Eine Funktion ist eine Abbildung von einem Eingabewert auf einen Ausgabewert.
EIN Eingabewert, EIN Ausgabewert. 
  
Folgendes - mit Prozeduren und Methoden problemlos machbares - geht mit Funktionen NICHT:
- keinen Eingabewert übergeben
- mehrere Eingabewerte übergeben
- Eingabewerte verändern (es sind Werte und keine 'Speicherblöcke')
- auf andere Daten, z.B. globaler Natur, zuzugreifen
- keinen Ausgabewert zurückliefern
- mehrere Ausgabewerte zurückliefern
- Exceptions werfen
- andere Seiteneffekte auslösen (die Welt außerhalb der Funktion verändern)
  
Funktionen sind also echte, pure Abbildungen. Ein Wert geht rein und ein Wert kommt raus. Das ist alles.
  
Das hat eine ganze Menge Vorteile:
- Funktionen sind einfach zu testen
- Funktionen sind einfach zu verstehen
- Funktionen sind einfach zu ändern
- Funktionen lassen sich einfach verketten. 
- Es passiert nichts unerwartetes.
    
Der vielleicht stärkste Vorteil gegenüber klassischer imperativer Programmierung ist:
- Ein Programm besteht aus einer Reihe verketter Funktionen
  - Daten gehen an dem einen Ende rein, kommen am anderen Ende raus
  - Keine weiteren Daten spielen eine Rolle, keine Daten werden verändert
      
==> **Kontrollfluss und Datenfluss sind identisch !!!**
      
Wieso ist das ein so großer Vorteil?
  
Schauen wir uns doch einmal eine Methode eines objektorientierten Programms an. Die Methode hat vollen Zugriff auf:
- mehrere Parameter
- Attribute ihres Objekts, inkl. Vererbungshierarchie
- statischen Attribute ihrer Klasse
- öffentliche statische Attribute aller öffentlichen Klassen (global)
    
All diese Werte kann eine Methode heranziehen und verändern. D.h. neben der etwaigen Berechnung eines Rückgabewerts, kann eine Methode große Teile des Datenraums eines Programms verändern. D.h. der Datenfluss und der Kontrollfluss haben nur wenig miteinander zu tun. Was bei kleinen Programmen noch halbwegs intellektuell handhabbar ist, bereitet bei großen Programmen zunehmend Probleme. Diese versuchen wir durch clevere Abstraktionen, Einschränkung der Sichtbarkeiten, Modularisierung, etc. irgendwie zu bändigen. In der Regel gelingt dies aber nur unter hohem Aufwand und mit zweifelhaftem Ergebnis. Schnell passiert es, dass der angesehenste Programmierer im Team nicht der ist, der den besten Code schreibt, sondern der sich am besten in dem vorhandenen auskennt und damit zu leben weiß.
  
  
## Aber kann man denn mit so wenig effektiv arbeiten?
  
Überraschenderweise ja. Man muss nur genauer hinsehen.

[[TOP]](/haskell/Preface) [[NEXT]](/haskell/Funktionen)
