---
title: 'PsyMessagement'
description: 'Introduction to PsyMessagement'
hide:
    - footer
icon: material/package
---

# :material-package: PsyMessagement
## O pluginu
Aktuálně je plugin postaven na 1.20 Paper API, je tu možnost fungování pro nižší verze, netestováno, není primární.

Plugin pro vlastní zprávy v chatu a při připojení/odpojení.
Nejlepší volba pro Almost-Vanilla (skoro čisté až na pár pluginů) servery.

✅Podpora ItemsAdder :image: ve zprávách.
✅Závislost na Vault a nějakém Chat+Permissions pluginu (LuckPerms)

Příkazy:

* /psy - Ukáže informace o pluginu
* /psy reload - Znovu načítá konfiguraci pluginu (výluka permisí)

Permise:
Prefix permise `psymessagement` + suffix permise

* psymessagement.admin - /reload příkaz
* psymessagement.colors - permise pro používání MiniMessage komponentu ve zprávách.

## Konfigurace

```yml
Messages:
  join-message: '%PREFIX%%PLAYER% <gold>joined the <bold>server</bold>!</gold>'
  leave-message: '%PREFIX%%PLAYER% <red>left the <bold>server</bold>!</red>'
  format: '%PREFIX%%PLAYER%%SUFFIX% %CUSTOM% %MESSAGE%'
  custom: '>>'

Colors:
  chatcolor-permission-suffix: colors


debug: false
Version: 1.0.8
```

Aktuálně podporované placeholdery jsou:

* %PREFIX% - Prefix hráče přístupný přes Vault
* %PLAYER% - Jméno hráče - nezměněné
* %DISPLAY_NAME% - Zobrazované jméno hráče (s prefixem a sufixem, pokud je uvedeno)
* %SUFFIX% - Sufix hráče přístupný přes Vault

Jenom pro `format`:

* %CUSTOM% - Vlastní oddělovač hráče a zprávy poskytovaný přes pole `custom`
* %MESSAGE% - Zástupce zprávy - musí být vždy přítomen!

!!! warning
    Podporován je pouze MiniMessage, např. <gold><bold>TEXT</gold></bold> <#FFAA00>SAMPLE</#FFAA00>. Po změně permisí je nutné restartovat server.

## Kde získat
PsyMessagement může být stažen [zde](https://modrinth.com/plugin/psymessagement)