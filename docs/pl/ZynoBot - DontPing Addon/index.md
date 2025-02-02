---
title: 'ZynoBot - DontPing Addon'
description: 'ZynoBot - DontPing'
hide:
    - footer
icon: material/message-reply-text
---

# :material-message-reply-text: ZynoBot DontPing Addon

Tired of all the pings from your community?
Feel free to download the DontPing addon for ZynoBot!
Disable pinging in any channel for anyone who doesn't have a moderation role!
Choose whether to delete the ping message or keep it!
Set your own message to force the community not to ping!

Automatically in all tickets and you can configure in which channels it should be restricted!

## Configuration

```json
{
    "channels": 
    [
        "0000000000000000000",
        "0000000000000000000"
    ],
    "deleteping": "true",
    "warnmessage": "{MENTION} do not ping the staff!"
}
```