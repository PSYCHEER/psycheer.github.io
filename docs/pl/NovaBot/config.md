---
title: "Konfiguracja NovaBot"
description: "Konfigurowanie NovaBot"
icon: material/file-document
---

# :material-file-document: Konfiguracja

## Podstawowa konfiguracja
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

!!! warning "Nie zmieniaj wersji"
    Jest to dla bota, żeby sprawdzał, na której wersji jest, aby zaktualizował konfig!

### licensekey
Twój unikatowy klucz licencyjny może zostać uzyskany na [Discordzie NovaBot](https://bbb.crafttale.eu/).
Klucz jest potrzebny do aktywacji bota.

### mongoURI
URI połączenia MongoDB.
Jeśli nie masz konta MongoDB, możesz je założyć [tutaj](https://mongodb.com).
Jeśli będziesz potrzebował pomocy z konfiguracją Mongo Cluster dla bota (baza danych), nie wahaj się otworzyć ticketu na naszym serwerze Discord.

### name
Nazwa bota. Może być ustawiona dowolnie, ale zmieni ustawienie nazwy w sekcji "Informacje ogólne" w Discord Developer Portal.

### token
Token może zostać uzyskany [tutaj](https://psycheer.github.io/novabot/setup)

### app_id
ApplicationID może zostać uzyskane [tutaj](https://psycheer.github.io/novabot/setup).

### guild
GuildID może zostać uzyskane z Discorda.
Kliknij prawym przyciskiem na ikonę swojej gildii w liście serwerów Discord i wybierz "Skopiuj ID serwera".
Musisz włączyć „Tryb developera” w Ustawieniach Discorda.

### activity
niestandardowy tekst

### activity_type
`Playing|Streaming|Listening|Watching|Competing|Bubble|Cyclical`

`Bubble` aby wyświetlić niestandardową wiadomość jako status z niestandardową wiadomością nad zdjęciem profilowym bota.

`Cyclical` aby wyświetlić wiele wiadomości w cyklu w **duration** zakresu czasu w  **cycle settings**.
!!! danger
    Bardzo niskie wartości `duration` mogą prowadzić do tymczasowego zablokowania bota z powodu ograniczeń szybkości Discorda!

### status
W statusie mogą znajdować się te trzy opcje "online|idle|dnd", który wybiera status bota.
Online - Zielone kółko,
Idle - Żółty Księżyc,
Dnd - Czerwone kółko z ikoną minus

### showStatistics
Przełącz true|false, aby (nie) pokazywać statystyk w konsoli bota (liczenie uruchomień i wiadomości).

### reloadCommandRoles
Role, które mogą używać polecenia /reload do ponownego załadowania konfiguracji dodatku.

### reloadSettings
Różne ustawienia osadzania, brak komunikatu o pozwoleniu, brak komunikatu o dodatkach lub placeholderach w menu wyboru.