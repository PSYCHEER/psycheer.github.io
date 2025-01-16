---
title: "NovaBot Configuration"
description: "Setting up the NovaBot"
icon: material/file-document
---

# :material-file-document: Configuration

## Default configuration
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
  reloadCommandRoles: [""] # Array of roles which can do /reload command for addon configurations reload
```

!!! warning "Do not change version"
    It's for bot to check which version is on and update config!

### licensekey
Your unique license key can be obtained on our [Discord for NovaBot](https://bbb.crafttale.eu/).
Is needed for bot to start up.

### mongoURI
MongoDB connection URI.
If you have no MongoDB account, you can make one in [here](https://mongodb.com).
If you'll need a help with setting up a Mongo Cluster for bot (database), feel free to open a ticket on our Discord server.

### name
Bot's name. Can be set on whatever, but it will change name setting in "General Informations" in Discord Developer Portal

### token
Token can be obtained in [here](https://psycheer.github.io/novabot/setup)

### app_id
ApplicationID can be obtained in [here](https://psycheer.github.io/novabot/setup)

### guild
GuildID can be obtained from Discord.
Right click on your guild icon in Discord server list and choose "Copy Server ID".
Need to have enabled "Developer Mode" in Discord Settings.

### activity
Custom text

### activity_type
Playing|Streaming|Listening|Watching|Competing|Bubble|Cyclical
  Bubble to show custom message as custom status message over bot's profile photo
  Cyclical to show multiple messages in a cycle within **duration** time range in **cycle settings**.

### status
In status can be these three options "online|idle|dnd", which chooses a status of the bot.
Online - Green Circle,
Idle - Yellow Moon,
Dnd - Red Circle with minus icon

### showStatistics
Toggle true|false to (not) show statisctics in console of the bot (Starts and messages count).

### reloadCommandRoles
Array of roles, which may use /reload command to reload addon's configuration.