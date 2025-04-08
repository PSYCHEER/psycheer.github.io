---
title: Creación de un Addon
description: Guía del sistema de Addons de NovaBot
icon: material/format-paint
---

# :material-format-paint: **Creación de Addons**

Crear un Addon para NovaBot es sencillo.

??? tip
    Debido al idioma original (en inglés), los códigos ejemplificados se mantendrán en ese mismo idioma durante esta guía, aunque se pueden modificar esos textos sin ningún problema.

## Estructura de las carpetas

```yml title="Estructura de las carpetas" hl_lines="4"
novabot:
  - index.js
  - addons:
    - yourAddon:
      - index.js
      - events:
        - event.js
      - commands:
        - command.js
```

Para verificar que NovaBot leerá todos los archivos en orden, se debe seguir estrictamente la estructura de las carpetas.
NovaBot automáticamente registrará todos los comandos dentro de la carpeta `commands` y registrará todos los eventos dentro de la carpeta `events`.

## index.js

```js title="index.js simple" linenums="1"
async function myFunction(){
    console.log("Hello World!");
}

module.exports = {
  name: "YourAddon",
  version: "1.0.0",
  author: "YourName",
  description: "My awesome add-on!",
  myFunction
```

Esto es un simple `index.js`.
Como puedes ver, `module.exports` exporta los campos `name`, `version`, `author` y `description`.
Estas variables son importantes para NovaBot, ya que los mostrará en el /reload y en la consola cuando inicie.

## command.js

```js title="command.js simple" linenums="1"
const { SlashCommandBuilder, MessageFlags } = require("discord.js");

const { myFunction } = require("../index.js");

module.exports = {
    data: new SlashCommandBuilder()
    .setName("command")
    .setDescription("Simple command"),

    async execute(interaction){
        await myFunction();
        await interaction.reply({
            content: "myFunction works!",
            flags: MessageFlags.Ephemeral
            //ephemeral: true is deprecated and obsolete
        })
    }
}
```
Esto creará un simple comando (/command) para nuestro bot que llamarà a la función `myFunction` la cuál dirá "Hello world!" en la consola.

## event.js
```js title="Evento simple" linenums="1"

module.exports = {
    name: "messageCreate",
    async execute(message){
        console.log(`${message.author.id} wrote ${message}`);
    }
}

```
Esto enviará el mensaje "000000000000000000 wrote MyMessageContent" en la consola cada vez que alguien envíe un mensaje.

!!! success
    ¡Ya estamos! ¡Esperamos que esto ayude a liberar tu creatividad!