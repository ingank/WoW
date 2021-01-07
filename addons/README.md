# Addons

Entwicklung von World of Warcraft Classic Addons.

## Entwicklungsumgebung

* Windows 10
* Aktueller Wow Classic Client von Blizzard Entertaintment
* Visual Studio Code [[Link]](https://code.visualstudio.com/)
* Visual Studio Code Extensions:
  * trixnz.vscode-lua
  * septh.wow-bundle

## HelloWoW Addon erstellen

Ermittlung des Programmordners:

* Entweder `C:\Program Files`
* Oder `C:\Program Files (X86)`

Addon erstellen:

* Wechsle in den Unterordner `_classic_/Interface/Addons`
* Erstelle den Addonordner `HelloWoW`
* Wechsle in den Unterordner `HelloWoW`
* Erstelle die Datei `HelloWoW.toc`
* Erstelle die Datei `HelloWoW.lua`

Interface ermitteln:

* Im Blizzard Client wird die Version des WoW Classic Clients angezeigt
* Beispiel: `Version: 1.13.6.36935`
* Das entsprechende Interface lautet: `11306`

Inhalt der Datei `HelloWoW.toc`:
```
## Interface: 11306
## Title: HelloWoW
## Notes: Hello World WoW Addon
## Author: Foo Bar
## Version: 0.01
HelloWoW.lua
```

Inhalt der Datei `HelloWoW.lua`:
```
print("Hello World!")
```

Starte WoW Classic! Sobald der WoW Classic Client gestartet wurde,
wird in den Chatlog der Text *Hello World!* gepostet.

**Beachte:**
Im laufenden Spiel kann das Addon (und alle anderen Addons) mit dem Konsolenkommando `/reload` neu geladen werden.
Das ist sinnvoll, wenn das Addon gleichzeitig entwickelt und getestet wird.
Werden während der Testphase neue *.lua* oder *.xml* Dateien erzeugt,
so muss der Client neu gestartet werden,
damit diese Änderungen im Spiel aktualsiert werden.

## Quellen

* https://wow.gamepedia.com/Create_a_WoW_AddOn_in_under_15_Minutes
* https://wow.gamepedia.com/Getting_started_with_writing_addons
* https://www.jimhribar.com/developing-wow-addons/