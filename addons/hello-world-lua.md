# Hello World Addon mit Lua

## Vorbereitung

Das Addon sollte, wie [hier](new-addon.md) beschrieben angelegt werden.

## Implementierung

Inhalt der Datei `Foo.toc`:
```
## Interface: 11306
## Title: Foo
## Notes: Hello World mit Lua
Foo.lua
```

Inhalt der Datei `Foo.lua`:
```
print("Hello World!")
```

Starte WoW Classic! Sobald der WoW Classic Client gestartet wurde,
wird in den Chatlog der Text *Hello World!* gepostet.

## Testing/Debugging

Informationen zum Testen und Debuggen von WoW Classic Addons finden sich [hier](test-addon.md).
