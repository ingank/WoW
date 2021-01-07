# Bedingungen

Dieses Dokument bezieht sich auf den Aspekt der Bedingungen
(`[con]` = Conditionals = Bedingungen)
innerhalb des WoW Classic Makrosystems.

```
/foo [con] foo_args
```

Es gilt:

* `/foo`
  * Kommando, das bedingt ausgeführt werden soll
* `[con]`
  * Bedingung(en)
* `foo_args`
  * Optionen und Argumente des Kommandos `\foo`

## Bedingungsquellen

```
/foo [@unitid] foo_args
/foo [boolean] foo_args
/foo [boolean:spec] foo_args
```

Es gilt:

* `@unitid`
  * Ist entweder eine durch den Spieler direkt erreichbare Einheit
  * Oder eine durch die Aneinanderreihung von Zielen von Einheiten adressierbare Einheit (Beispiel: `@pettargettarget`)
  * kann durch das Präfix `no` negiert werden (Beispiel: `@noplayer` für alle Ziele, außer der eigene Charakter)
* `boolean`
  * Funktionen vom Typ Boolean, die von der WoW Client API zur Verfügung gestellt werden (Beispiel: `dead`)
* `boolean:spec`
  * Funtionen vom Typ Boolean, die zusätzlich einen speziellen Bezeichner benötigen (Beispiel: `mod:alt`) 


## Zielfunktion (@unitid)

Syntax
```
(1) target=unitid
(2) @unitid
```

mögliche Einheiten oder Einheitengruppen:

* `arenaX`
  * Das Arenamitglied mit der Nummer X (arena1 bis arena5)
* `mouseover` 
  * Die Einheit, die sich unter dem Mauszeiger befindet (oder sich bis vor kurzem befunden hat)
* `none`
  * Keine Einheit.
  * Wird beispielsweise verwendet, um Makros so zu modifizieren, dass sie nicht auf den eigenen Charakter wirken. Beispiel: `/cast [target=none] Healing Wave)`
* `partyX` 
  * Das X'te Mitglied der aktuellen Gruppe, ausgenommen des Spielers selber (party1 bis party4)
* `partypetX` 
  * Der Begleiter des X'ten Mitglieds der aktuellen Gruppe (partypet1 bis partypet4)
* `pet` 
  * Der eigene Begleiter
* `player`
  * Der eigene Charakter
* `raidX` 
  * Das X'te Mitglied der aktuellen Raidgruppe (raid1 bis raid40)
* `raidpetX` 
  * Der Begleiter des X'ten Mitglieds der aktuellen Raidgruppe (raidpet1 bis raidpett40)
* `target`
  * Das aktuell markierte Ziel.
* `vehicle` 
  * Das aktuell durch den eigenen Charakter genutzte Fahrzeug.

## Attributfunktionen (Boolean)

Gegen das Ziel evaluiert:

* `exists`
  * Die Einheit existiert
* `help`
  * Die Einheit existiert UND ihr kann beim Kampf geholfen werden
* `harm`
  * Die Einheit existiert UND sie kann durch den Spielercharakter verletzt werden
* `dead`
  * Die Einheit existiert UND ist tot
* `party`
  * Die Einheit existiert UND ist in der aktuellen Gruppe
* `raid`
  * Die Einheit existiert UND ist in der aktuellen Raidgruppe
* `unithasvehicleui`
  * Die Einheit existiert UND befindet sich in einem Fahrzeug

Gegen den eigenen Charakter evaluiert:

* `canexitvehicle`
  * Befindet sich in einem Fahrzeug UND kann dieses verlassen.
* `channeling`
  * Kanalisiert aktuell einen Spruch
* `channeling:foo_spell`
  * Kanalisiert aktuell den Spruch `foo_spell`
  * Siehe auch: "Bezeichner von Fertigkeiten und Sprüchen ermitteln"
* `combat`
  * Befindet sich im Kampf
* `equipped:foo_item`
  * Ist der Gegenstand `foo_item` angelegt?
  * Mögliche Bezeichner:
    * Typen, Untertypen und Ausrüstungsgegenstände
    * Siehe auch: [Typen und Untertypen](https://wow.gamepedia.com/ItemType)
    * Siehe auch: "Bezeichner von Ausrüstungsgegenständen ermitteln"
* `worn:type`
  * Alternative für `equipped:foo_item`
* `flying`
  * Fliegt
* `form:foo_id`
  * Alternative für `stance:foo_id`
* `stance:foo_id`
  * Hat eine bestimmte Gestalt oder Haltung angenommen
  * Siehe "Haltungen und Gestalten" 
* `group`
  * Befindet sich in einer Gruppe oder einer Raidgruppe
* `group:party`
  * Befindet sich in einer Gruppe (aber keiner Raidgruppe)
* `group:raid`
  * Befindet sich mindestens in einer Raidgruppe 
* `indoors`
  * Befindet sich in einem Gebäude
* `outdoors`
  * Befindet sich im Freien 
* `mounted`
  * Sitzt auf einem Gefährt
* `pet:name`
  * Jäger: Nutzt das Haustier mit dem Namen `name`
* `pet:family`
  * Jäger: Nutzt die Haustierklasse `family`
  * Siehe "Haustierklassen" 
* `petbattle`
  * Haustier befindet sich im Kampf 
* `resting`
  * Ist eingesperrt
* `stealth`
  * Ist unsichtbar
* `swimming`
  * Schwimmt
