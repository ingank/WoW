# Bedingungen

Anwendung:

```
/foo [target=unitid,mod1,mod2,...][...]... foo_options
```

Dabei gilt:

* `/foo`
  * Kommando, das bedingt ausgeführt werden soll 
* `[target=unitid,mod1,mod2,...][...]...`
  * Bedingung(en)
* `foo_options`
  * Optionen und Argumente des Kommandos `\foo`

Bedingung(en):

* `target=unitid`
  * (1) Eine durch den Spieler erreichbare Einheit
  * (2) Eine durch die Aneinanderreihung von Einheiten adressierte Einheit
* `modx`
  * Zusätzliche Attribute des `target=unitid` um die Bedingung zu erfüllen
* `[...]`
  * Weitere mögliche Bedingungen nach dem Schema `[target=unitid,mod1,mod2,...]`
  * verknüpft durch *OR (ODER)* mit den anderen Bedingungen
* `...`
  * Fortsetzung der Reihe an Bedingungen
