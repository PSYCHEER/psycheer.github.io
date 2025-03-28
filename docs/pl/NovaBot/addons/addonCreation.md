---
title: Tworzenie dodatku
description: Przewodnik po systemie dodatków NovaBot
icon: material/format-paint
---

# :material-format-paint: **Tworzenie dodatku**

Tworzenie dodatku dla NovaBot jest proste

## Folder Structure

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

Aby NovaBot poprawnie odczytał wszystkie pliki, musimy ściśle przestrzegać struktury folderów. NovaBot automatycznie rejestruje wszystkie komendy w folderze `commands` oraz wszystkie zdarzenia w folderze `events`.

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

To jest prosty `index.js`. Jak widać, `module.exports` eksportuje `name`, `version`, `author` i `description`. Te zmienne są ważne dla NovaBot, aby mogły być wyświetlane w /reload oraz w konsoli podczas uruchamiania.

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
To stworzy prostą komendę slash (/) dla naszego bota, która wywołuje funkcję `myFunction`, wypisującą "Hello World!" w konsoli.

## event.js
```js title="Simple event" linenums="1"

module.exports = {
    name: "messageCreate",
    async execute(message){
        console.log(`${message.author.id} wrote ${message}`);
    }
}

```
To wyśle do konsoli komunikat w formacie "000000000000000000 napisał MojaTreśćWiadomości" za każdym razem, gdy użytkownik wyśle wiadomość.

!!! success
    Gotowe! Mamy nadzieję, że uwolnisz swoją kreatywność!