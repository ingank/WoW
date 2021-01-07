# Makros in World of Warcraft Classic

```
#meta
#meta meta_args
/foo
/foo foo_args
/foo [con1] foo_args
/foo [con2,con3] foo_args
/foo [con3][con4] foo_args
/foo [con5] foo_args1; [con6] foo_args2
```

Es gilt:

* `#meta, #meta meta_args`
  * Metakommando
  * Erste Zeile des Makros
* `/foo`
  * Auszuführendes Kommando
* `foo_args`
  * Optionen und Argumente des Kommandos `/foo`
* `[con1-6]`
  * Conditionals = Bedingungen (`IF ... THEN ...`)
* `IF [con1] THEN DO /foo foo_args`
* `IF [con2] AND [con3] THEN DO /foo foo_args`
* `IF [con3] OR [con4] THEN DO /foo foo_args`
* `IF [con5] THEN DO /foo foo_args1 ELSIF [con6] THEN DO /foo foo_ars2`