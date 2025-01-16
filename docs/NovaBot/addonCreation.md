# **Add-on Creation**

Doing addon for NovaBot is simple

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

To ensure NovaBot will read all files in order, we have to strictly follow folder structure.
NovaBot automatically register all commands inside of `commadns` folder and register all events in `events` folder.

## index.js

```js title="Simple index.js"
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

This is simple `index.js`.
As you can see, `module.exports` exports `name`, `version`, `author` and `description`.
These variables are important for NovaBot to have, so it can show in /reload and in console upon start.

## command.js

```js title="Simple command.js"
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
This will create a simple slash (/) command for our bot which calls `myFunction` function which will say "Hello World!" into console.

## event.js
```js title="Simple event"

module.exports = {
    name: "messageCreate",
    async execute(message){
        console.log(`${message.author.id} wrote ${message}`);
    }
}

```
This will send "000000000000000000 wrote MyMessageContent" into console every time a user send a message.

!!! success
    We are done! Hope you will unleash your creativity!