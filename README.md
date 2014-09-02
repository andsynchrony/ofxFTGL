# ofxFTGL -- fast typography library with Unicode support

Originally by Rick Companje. 

example and binary builds by obviousjim

ofxFTGLSimpleLayout and example added by Stefan Wagner (andsynchrony)




1. lege Ordnerstruktur innerhalb des src-directorys an
src > ofxFTGL > ...

2. Laufzeitbibliothek (Eigenschaften > Konfigurationseigenschaften > C/C++ > Codegenerierung):
2.1 in der Debug-Konfiguration:
/MDd
2.2 in der Release-Konfiguration:
/MD

3. zusätzliche includes (sowohl in Debug- als auch in Release-Konfiguration):
src\ofxFTGL;src\ofxFTGL\libs;src\ofxFTGL\libs\FTGL;src\ofxFTGL\libs\FTGL\lib;src\ofxFTGL\libs\FTGL\include;src\ofxFTGL\libs\FTGL\include\FTGL;src\ofxFTGL\src;

4. zusätzliche Bibliotheksverzeichnisse (sowohl in Debug- als auch in Release-Konfiguration):
src/ofxFTGL/libs/FTGL/lib/vs2012;

5. lege Projekt-Ordnerstruktur passend an ABER:
// um das Projekt in der Debug-Konfiguration starten zu können:
ziehe NUR ftgl_static_D.lib in src/ofxFTGL/libs/FTGL/lib/vs2012;

// um das Projekt in der Release-Konfiguration starten zu können:
ziehe NUR ftgl_static.lib in src/ofxFTGL/libs/FTGL/lib/vs2012;

6. Projekt in der jeweiligen Konfiguration starten

7. Es sollte laufen

// um zwischen den jeweiligen Konfigurationen umzuschalten muss immer in der 
Projekt-Ordnerstruktur die .lib-Datei passend ausgetauscht werden


------------------------------------------------------
------------------------------------------------------
------------------------------------------------------
sollten nun anstatt der UTF-8-Zeichen Ersatzsymbole angezeigt werden bitte folgende Schritte testen:

- unter Datei > Erweiterte Speicheroptionen... auf UTF-8 umstellen
- sämtliche src-Dateien mit utf8-encoding speichern (am besten nicht im Projekt selbst, sondern z.B. über Sublime Text)
- im Programm die Projektmappe umbenennen
- im Programm den Projektnamen ändern
- im Programm den Stammnamespace ändern
