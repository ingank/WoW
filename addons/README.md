# Addons

World of Warcraft Classic Addon Developement.

## Entwicklungsumgebung

* Windows 10
* Aktueller Wow Classic Client von Blizzard Entertaintment
* Visual Studio Code [[Link]](https://code.visualstudio.com/)
* Visual Studio Code Extensions:
  * trixnz.vscode-lua
  * septh.wow-bundle

## Hello World (HelloWoW Addon)

Ermittlung des Programmordners:

* Entweder `C:\Program Files`
* Oder `C:\Program Files (X86)`

Addon erstellen:

* Wechsle in den Unterordner `_classic_/Interface/Addons`
* Erstelle den Addonordner `HelloWoW`
* Erstelle die Datei `HelloWoW.toc`
* Erstelle die Datei `HolloWoW.lua`

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
HelloWoW = { }

function Sandbox:HelloWorld()
    message("Hello World!")
end

HelloWoW:HelloWorld()
```
