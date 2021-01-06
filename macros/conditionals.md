# Bedingungen

Anwendung:

```
/foo [target=unitid,mod1,mod2,...][...] foo_options
```

Dabei gilt:

* `/foo`
  * Kommando, das bedingt ausgeführt werden soll 
* `[target=unitid,mod1,mod2,...][...]`
  * Bedingung(en)
* `foo_options`
  * Optionen und Argumente des Kommandos `\foo`

Bedingungen:

* `target=unitid`
  * (1) Eine durch den Spieler erreichbare Einheit
  * (2) Eine durch die Aneinanderreihung von Einheiten adressierte Einheit
* `modx` = welche Attribute muss das `target` zusätzlich aufweisen, damit die Bedingung erfüllt ist?
