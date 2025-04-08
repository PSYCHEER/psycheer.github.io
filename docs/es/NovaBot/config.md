---
title: "Configuración de tu NovaBot"
description: "Configura tu NovaBot"
icon: material/file-document
---

# :material-file-document: Configuración

## Configuración por defecto
```yaml title="config.yml" hl_lines="2"
bot:
  version: "1.0.0"
  licensekey: ""
  mongoURI: ""
  name: "NovaBot👑"
  token: ""
  app_id: ""
  guild: ""
  activity: "Waiting for orders"
  activity_type: "Cyclical"
  cycle:
  - text: "{botName}"
    duration: 5 # In seconds
  - text: "Looking for tickets {ticketCount}"
    duration: 10
  status: "idle"
  showStatistics: true
  reloadCommandRoles: [""]
```

!!! warning "No cambies la versión"
    El valor de `version` es para que el bot revise en qué versión se encuentra y pueda actualizarse, ¡no lo toques!

### licensekey
Tu licencia, puede obtenerse en nuestro [Discord de NovaBot](https://bbb.crafttale.eu/).
Es necesario para que el bot empiece a funcionar.

### mongoURI
URI de tu MongoDB.
Si no tienes una cuenta de MongoDB, puedes crear una [aquí](https://mongodb.com).
Si necesitas ayuda configurando un Mongo Cluster para el bot (una base de datos), siéntete libre de abrir un ticket en nuestro servidor de Discord.

### name
El nombre del bot. Puede eser cualquiera, pero hacerlo cambiará el nombre de la configuración (el valor "General Informations") en el [Portal de Desarrolladores de Discord](https://discord.com/developers/applications).

### token
El Token puede obtenerse [aquí](./setup.md).

### app_id
La ApplicationID puede obtenerse [aquí](./setup.md).

### guild
La GuildID puede obtenerse en discord.
Haz click derecho en el icono de tu Hermandad (o Guild) en la lista de servidores de discord y selecciona la opción "Copiar la ID del servidor".
Necesitas tener el "Modo desarrollador" activado en tu configuración de Discord (en la sección de Avanzado).

### activity
Texto custom que prefieras.

### activity_type
`Playing|Streaming|Listening|Watching|Competing|Bubble|Cyclical`

`Bubble` mostrará un texto custom (definido en Activity) en la foto de perfil de tu bot.

`Cyclical` mostrará múltiples mensajes en un ciclo con una duración definida en el valor **duration** establecido en **cycle settings**.
!!! danger
    ¡Un valor muy bajo del valor `duration` puede ocasionar que tu bot reciba una expulsión temporal debido a los límites de velocidad entre cambios de Discord!

### status
En el estado, solo pueden haber tres opciones siendo éstas "online|idle|dnd", que elige el estado del bot.
Online - Círculo verde (o disponible),
Idle - Círculo amarillo (o ausente),
Dnd - Círculo rojo con un símbolo de menos (o no molestar)

### showStatistics
Establécelo en true|false para (no) mostrar estadísticas en la consola del bot (inicios y contador de mensajes).

### reloadCommandRoles
Un Array (o lista) de roles que pueden usar el comando de /reload para recargar la configuración del bot.