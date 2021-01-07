# Hello World Addon mit XML/Lua

## Vorbereitung

Das Addon sollte, wie [hier](new-addon.md) beschrieben angelegt werden.

## Implementierung

Inhalt der Datei `Foo.toc`:
```
## Interface: 11306
## Title: Foo
## Notes: Hello World mit XML/Lua
Foo.xml
Foo.lua
```

Inhalt der Datei `Foo.lua`:
```
function Foo_OnLoad(self)
    print("Hello World!")
end
```

Inhalt der Datei `Foo.xml`:
```
<Ui xsi:schemaLocation="http://www.blizzard.com/wow/ui/ ..\FrameXML\UI.xsd">
    <Script file="Foo.lua" />
    <Frame name="Foo">
        <Scripts>
            <OnLoad function="Foo_OnLoad" />
        </Scripts>
    </Frame>
</Ui>
```

Starte WoW Classic! Sobald der WoW Classic Client gestartet wurde,
wird in den Chatlog der Text *Hello World!* gepostet.

## Testing/Debugging

Informationen zum Testen und Debuggen von WoW Classic Addons finden sich [hier](test-addon.md).
