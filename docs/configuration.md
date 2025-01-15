---
title: "NovaBot Configuration"
description: "Setting up the NovaBot"
---

# Configuration

### Default configuration
```yaml title="config.yml" hl_lines="2"
bot:
  version: "1.0.0" # Do not change this
  licensekey: "" # Obtained on our Discord server after verification
  mongoURI: "" # MongoDB connection URI
  name: "NovaBot👑"
  token: "" # Bot token
  app_id: "" # Application ID
  guild: "" # Guild ID
  activity: "Waiting for orders"
  # Bubble to show custom message as custom status message over bot's profile photo
  # Cyclical to show multiple messages in a cycle
  activity_type: "Cyclical" # Playing|Streaming|Listening|Watching|Competing|Bubble|Cyclical
  cycle:
  - text: "{botName}"
    duration: 5 # In seconds
  - text: "Looking for tickets {ticketCount}"
    duration: 10
  status: "idle" # online|idle|dnd
  showStatistics: true
  reloadCommandRoles: ["1322505726391881748"] # Array of roles which can do /reload command for addon configurations reload
```

!!! warning "Do not change version"
    It's for bot to check which version is on and update config!

### licensekey
Your unique license key can be obtained on our Discord for NovaBot.
Is needed for bot to start up.

### mongoURI