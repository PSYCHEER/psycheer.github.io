---
title: 'ZynoBot - DontPing Addon'
description: 'ZynoBot - DontPing'
hide:
    - footer
icon: material/message-reply-text
---

# :material-message-reply-text: ZynoBot DontPing Addon

Zmęczony wszystkimi pingami od swojej społeczności?  
Pobierz dodatek DontPing dla ZynoBot!  
Wyłącz pingowanie w dowolnym kanale dla każdego, kto nie ma roli moderacyjnej!  
Wybierz, czy usunąć wiadomość z pingiem, czy ją zachować!  
Ustaw własną wiadomość, aby wymusić na społeczności niepingowanie!  

Automatycznie we wszystkich zgłoszeniach, a także możesz skonfigurować, na których kanałach powinno to być ograniczone!

## Konfiguracja

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