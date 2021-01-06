# Bedingungen

Anwendung:

```
/foo [target=unitid,mod1,mod2,...][...]... foo_options
```

* `/foo`
  * Kommando, das bedingt ausgeführt werden soll 
* `[target=unitid,attr_1,attr_2,...][...]...`
  * Bedingung(en)
* `foo_options`
  * Optionen und Argumente des Kommandos `\foo`

Es gilt:

* `target=unitid`
  * (1) Eine durch den Spieler erreichbare Einheit
  * (2) Eine durch die Aneinanderreihung von Einheiten adressierte Einheit
* `attr_x`
  * Zusätzliche Attribute die erfüllt sein müssen, um die Bedingung zu erfüllen
  * Alle Attribute einer Bedingung sind durch *AND (UND)* verknüpft
* `[...]`
  * Weitere mögliche Bedingungen nach dem Schema `[target=unitid,mod1,mod2,...]`
  * verknüpft durch *OR (ODER)* mit den anderen Bedingungen
* `...`
  * Fortsetzung der Reihe an Bedingungen

## Ziele (target=unitid)

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

## Zielattribute (attr_x)

Gegen das Ziel evaluiert:

* `exists`
  * Die Einheit existiert
* `help`
  * Die Einheit existiert UND ihr kann mit einem Spruch geholfen werden
* `harm`
  * Die Einheit existiert UND sie kann mit einem Spruch geheilt werden
* `dead`
  * Die Einheit existiert UND ist tot
* `party`
  * Die Einheit existiert UND ist in der aktuellen Gruppe
* `raid`
  * Die Einheit existiert UND ist in der aktuellen Raidgruppe
* `unithasvehicleui`
  * Die Einheit existiert UND befindet sich in einem Fahrzeug

Gegen den eigenen Charakter evaluiert:

* canexitvehicle
  * In a vehicle and able to exit
* channeling, channeling:spellName
  * Channeling any spell, or a certain spell
* combat
  * In combat
* equipped:type, worn:type
  * Refer to itemType for possible types (ie, weapon) and subtypes (ie, sword)
* flyable
  * Unreliable in Wintergrasp
* flying
  * Mounted or flight form, and in the air
* form:n, stance:n
  * Refer to GetShapeshiftForm for possible values* 
* group, group:party, group:raid* IsInGroup() and IsInRaid()* Self-explanatory* 
* indoors, outdoors* IsIndoors() and IsOutdoors()* Self-explanatory* 
* mounted* IsMounted()* Self-explanatory* 
* pet:name, pet:family* UnitCreatureFamily("pet")* Using a hunter pet by name or family* 
* petbattle* C_PetBattles.IsInBattle()* In a pet battle* 
* resting* IsResting()* In a rested zone* 
* spec:n, spec:n1/n2* GetActiveSpecGroup(false)* Activated the n'th (or any of n1, n2) spec* 
* stealth* IsStealthed()* Self-explanatory* 
* swimming* IsSubmerged()* Self-explanatory* 
* talent:row/col* * The given row/col talent is active* 
