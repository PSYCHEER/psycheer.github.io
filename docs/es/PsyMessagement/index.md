---
title: 'PsyMessagement'
description: 'Introducción al plugin PsyMessagement'
hide:
    - footer
icon: material/package
---

# :material-package: PsyMessagement
## Acerca del plugin
El plugin actualmente está creado para funcionar con la versión 1.20 de la API de Paper, es posible que funcione en versiones inferiores aunque no está testeado al no ser la versión principal.

Plugin para enviar mensajes custom al entrar/salir del servidor.
La mejor opción para servidores semi-vanilla.

✅ItemsAdder: :image: en los mensajes soportado.
✅Vault: Dependencias además de los plugins de permisos (LuckPerms)

Comandos:

* /psy - Muestra información del plugin
* /psy reload - Recarga la configuración del plugin (excepto permisos)

Permisos:
Prefijo de permiso `psymessagement` + permiso de sufijo

* psymessagement.admin - comando de recarga
* psymessagement.colors - permiso para el parseo usando el formado de MiniMessage, puede ser cambiado en la configuración

## Configuración

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

Los Placeholders soportados de momento son:

* %PREFIX% - Prefijo del jugador al cuál accedemos vía Vault
* %PLAYER% - Nombre del jugador sin cambios
* %DISPLAY_NAME% - Nombre del jugador con y sin prefijos si están definidos
* %SUFFIX% - Sufijo del jugador al cuál accedemos vía Vault

Solo para la sección `format`:

* %CUSTOM% - Divisor para el mensaje y el jugador custom que se obtiene del valor `custom`
* %MESSAGE% - Placeholder del mensaje - ¡Siempre debe estar presente!

!!! warning
    Solo soporta MiniMessages ej. <gold><bold>TEXTO</gold></bold> <#FFAA00>PRUEBA</#FFAA00>. Después de cambiar un permiso, debes reiniciar el servidor.

## Dónde obtener PsyMessagement
PsyMessagement puede descargarse [aquí](https://modrinth.com/plugin/psymessagement)