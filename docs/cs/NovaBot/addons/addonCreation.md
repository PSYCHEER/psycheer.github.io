---
title: Vytvoření Doplňku
description: Průvodce systémem doplňků NovaBot
icon: material/format-paint
---

# :material-format-paint: **Vytvoření Doplňku**

Vytvoření doplňku pro NovaBot je jednoduché

## Struktura Složek

```yml title="Folder Structure" hl_lines="4"
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

Aby NovaBot mohl číst všechny soubory ve správném pořadí, musíme přísně dodržovat strukturu složek.
NovaBot automaticky registruje všechny příkazy uvnitř složky `commands` a registruje všechny události ve složce `events`.

## index.js

```js title="Simple index.js" linenums="1"
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

Toto je jednoduchý `index.js`.
Jak můžete vidět, `module.exports` exportuje `name`, `version`, `author` a `description`.
Tyto proměnné jsou důležité pro NovaBot, aby je měl, takže je může zobrazit v /reload a v konzoli při startu.

## command.js

```js title="Simple command.js" linenums="1"
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
Toto vytvoří jednoduchý příkaz lomítka (/) pro náš bot, který volá funkci `myFunction`, která řekne "Hello World!" do konzole.

## event.js
```js title="Simple event" linenums="1"

module.exports = {
    name: "messageCreate",
    async execute(message){
        console.log(`${message.author.id} wrote ${message}`);
    }
}

```
Toto pošle "000000000000000000 napsal MyMessageContent" do konzole pokaždé, když uživatel pošle zprávu.

!!! success
    Hotovo! Doufám, že uvolníte svou kreativitu!