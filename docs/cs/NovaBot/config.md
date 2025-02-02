---
title: "Konfigurace NovaBot"
description: "Nastavení NovaBot"
icon: material/file-document
---

# :material-file-document: Konfigurace

## Výchozí konfigurace
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

  reloadSettings:
    ...
```

!!! warning "Neměňte verzi"
    Je to pro bota, aby zkontroloval, která verze je spuštěná a aktualizoval konfiguraci!

### licensekey
Váš unikátní licenční klíč lze získat na našem [Discordu pro NovaBot](https://bbb.crafttale.eu/).
Je potřeba pro spuštění bota.

### mongoURI
MongoDB připojovací URI.
Pokud nemáte účet MongoDB, můžete si ho vytvořit [zde](https://mongodb.com).
Pokud budete potřebovat pomoc s nastavením Mongo Clusteru pro bota (databáze), neváhejte otevřít tiket na našem Discord serveru.

### name
Jméno bota. Může být nastaveno na cokoliv, ale změní nastavení jména v "General Informations" v Discord Developer Portal.

### token
Token lze získat [zde](./setup.md).

### app_id
ApplicationID lze získat [zde](./setup.md).

### guild
GuildID lze získat z Discordu.
Klikněte pravým tlačítkem na ikonu vašeho serveru v seznamu serverů Discord a vyberte "Copy Server ID".
Musíte mít povolený "Developer Mode" v nastavení Discordu.

### activity
Vlastní text

### activity_type
`Playing|Streaming|Listening|Watching|Competing|Bubble|Cyclical`

`Bubble` pro zobrazení vlastního zprávy jako vlastní status nad profilovou fotkou bota.

`Cyclical` pro zobrazení více zpráv v cyklu v rámci **doby trvání** v **nastavení cyklu**.
!!! danger
    Velmi nízké hodnoty `duration` mohou vést k dočasnému banu bota kvůli limitům Discordu!

### status
Ve statusu mohou být tyto tři možnosti "online|idle|dnd", které vybírají status bota.
Online - Zelený kruh,
Idle - Žlutý měsíc,
Dnd - Červený kruh s mínus ikonou

### showStatistics
Přepněte true|false pro (ne)zobrazení statistik v konzoli bota (Počty startů a zpráv).

### reloadCommandRoles
Pole rolí, které mohou použít příkaz /reload pro znovunačtení konfigurace doplňku.

### reloadSettings
Různá nastavení pro vkládání, zprávu bez oprávnění, zprávu bez doplňků nebo zástupný symbol v menu výběru.