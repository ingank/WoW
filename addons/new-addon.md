# Neues Addon erstellen

Mögliche Pfade zum Addon-Ordner von WoW Classic unter Windows:

```
C:\Program Files\World of Warcraft\_classic_\Interface\Addons\
C:\Program Files (X86)\World of Warcraft\_classic_\Interface\Addons\
```

Pfad zum Addon-Ordner von WoW Classic unter MacOS:
```
/Applications/World of Warcraft/_classic_/Interface/Addons/
```

Dort wird ein Ordner mit dem Namen des Addons erstellt. Beispiel:
```
C:\Program Files (X86)\World of Warcraft\_classic_\Interface\Addons\Foo
```

Erstelle in diesem Ordner folgende Dateien:
* Foo.toc
* Foo.lua
* Foo.xml

Die Version des Interfaces muss ermittelt werden:

* Im Blizzard Client wird die Version des WoW Classic Clients angezeigt
* Beispiel: `Version: 1.13.6.36935`
* Das entsprechende Interface lautet: `11306`

Die Datei `Foo.toc` sollte mindestens folgenden Code enthalten:
```
## Interface: 11306
## Title: Foo
## Notes: Ein richtiges Foo-Addon
Foo.xml
Foo.lua
```

Die Datei `Foo.xml` sollte mindestens folgenden Code enthalten:
```
<Ui xsi:schemaLocation="http://www.blizzard.com/wow/ui/ ..\FrameXML\UI.xsd">
</Ui>
```

Die Datei `Foo.lua` kann vorerst leer bleiben.

*Hinweis:*
Auch wenn dies vorerst ein leeres Addon ist,
kann es doch durch Starten des WoW Classic Client testweise geladen werden.
So ist sicher gestellt,
dass bis hierher alles richtig konfiguriert wurde.
Außerdem kann das Addon von der ersten Codezeile an live im Spiel getestet werden.