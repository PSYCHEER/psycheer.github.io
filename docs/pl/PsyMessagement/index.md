---
title: 'PsyMessagement'
description: 'Wprowadzenie do PsyMessagement'
hide:
    - footer
icon: material/package
---

# :material-package: PsyMessagement
## O pluginie
Obecnie plugin jest zbudowany w oparciu o API Paper 1.20, możliwość działania na niższych wersjach nie została przetestowana i nie jest priorytetem.

Plugin do niestandardowych wiadomości na czacie oraz wiadomości dołączania/opuszczania serwera.
Najlepszy wybór dla serwerów typu Almost-Vanilla.

✅Obsługa ItemsAdder :image: w wiadomościach.  
✅Zależność Vault oraz jakiś plugin do czatu i uprawnień (LuckPerms).

Komendy:

* /psy - Wyświetla informacje o pluginie
* /psy reload - Przeładowuje konfigurację pluginu (z wyjątkiem uprawnień)

Uprawnienia:  
Prefiks uprawnień `psymessagement` + sufiks uprawnień

* psymessagement.admin - komenda reload
* psymessagement.colors - uprawnienie do parsowania MiniMessage, można zmienić w konfiguracji

## Konfiguracja

```yml
Messages:
  join-message: '%PREFIX%%PLAYER% <gold>dołączył do <bold>serwera</bold>!</gold>'
  leave-message: '%PREFIX%%PLAYER% <red>opuścił <bold>serwer</bold>!</red>'
  format: '%PREFIX%%PLAYER%%SUFFIX% %CUSTOM% %MESSAGE%'
  custom: '>>'

Colors:
  chatcolor-permission-suffix: colors


debug: false
Version: 1.0.8
```

Obecnie obsługiwane zastępniki to:

* **%PREFIX%** - Prefiks gracza uzyskany przez Vault  
* **%PLAYER%** - Nazwa gracza - niezmieniona  
* **%DISPLAY_NAME%** - Wyświetlana nazwa gracza (z prefiksem i sufiksem, jeśli ustawione)  
* **%SUFFIX%** - Sufiks gracza uzyskany przez Vault  

Tylko dla `format`:

* **%CUSTOM%** - Niestandardowy separator gracza i wiadomości określony w polu `custom`  
* **%MESSAGE%** - Zastępnik wiadomości - musi być zawsze obecny!  

!!! warning
    Obsługiwany jest tylko MiniMessage, np. `<gold><bold>TEKST</gold></bold>` `<#FFAA00>PRZYKŁAD</#FFAA00>`. Po zmianie uprawnień wymagane jest ponowne uruchomienie serwera.

## Skąd pobrać PsyMessagement
PsyMessagement można pobrać [tutaj](https://modrinth.com/plugin/psymessagement)