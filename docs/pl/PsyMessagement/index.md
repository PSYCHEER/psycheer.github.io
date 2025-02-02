---
title: 'PsyMessagement'
description: 'Introduction to PsyMessagement'
hide:
    - footer
icon: 
---

# :package: PsyMessagement

Currently is plugin built against 1.20 Paper API, possibility of working for lower versions, not tested, not primary.

Plugin for custom Chat and Join/Leave messages.
Best choice for Almost-Vanilla servers.

✅ItemsAdder :image: in messages supported.
✅Vault dependency and some Chat+Permissions plugin (LuckPerms)

Commands:

* /psy - Show information about plugin
* /psy reload - Reloads plugin configuration (except permissions)

Permissions:
Permission prefix `psymessagement` + permission suffix

* psymessagement.admin - reload command
* psymessagement.colors - permission for MiniMessage parsing, can be changed in configuration

## Configuration

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

Currently supported placeholders are:

* %PREFIX% - Prefix of Player accessed via Vault
* %PLAYER% - Name of the player - unchanged
* %DISPLAY_NAME% - Display name of the player (with prefix and suffix if stated)
* %SUFFIX% - Suffix of player accessed via Vault

Only for `format`:

* %CUSTOM% - Custom player and message divider provided via `custom` field
* %MESSAGE% - Message placeholder - have to be always present!

!!! warning
    Only MiniMessage is supported ex. <gold><bold>TEXT</gold></bold> <#FFAA00>SAMPLE</#FFAA00>. After permission change is needed to restart the server.

### Where to get PsyMessagement
PsyMessagement can be found for download [here](https://modrinth.com/plugin/psymessagement)