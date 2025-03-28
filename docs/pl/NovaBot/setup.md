---
title: Konfiguracja bota
description: Przewodnik konfiguracji NovaBot
icon: fontawesome/solid/gear
---

# :fontawesome-solid-gear: Konfiguracja bota Discord

## **Wymagania wstępne**
* Serwer Discord Bot
* [NodeJS v22 LTS](https://nodejs.org/en "Long Term Support") lub nowszy
* Licencja [może być uzyskana na naszym Discordzie po zakupie](https://bbb.crafttale.eu)

## **Kroki konfiguracji NovaBot**

### Krok 1: Utwórz aplikację Discord
1. Przejdź do [Discord Developer Portal](https://discord.com/developers/applications).
2. Kliknij przycisk "New Application".
3. Nadaj swojej aplikacji nazwę i kliknij "Create".

### Krok 2: Utwórz użytkownika bota
1. W swojej nowej aplikacji przejdź do zakładki "Bot" po lewej stronie.
2. Możesz dostosować profil swojego bota, ustawiając awatar i nazwę.
3. Wyłącz ustawienie "Public Bot".

!!! tip 
    W sekcji "General Information" możesz ustawić nazwę wyświetlaną dla swojego bota oraz opis (bio).

### Krok 3: Pobierz dane uwierzytelniające bota (Token/Application ID)
1. W zakładce "Bot", w sekcji "TOKEN", kliknij "Copy", aby uzyskać token swojego bota. **Trzymaj ten token w tajemnicy**.
2. ApplicationID można znaleźć w sekcji "General Information".
3. Umieść obie te wartości w pliku konfiguracyjnym bota w głównym folderze bota.
4. Włącz wszystkie intencje: "Presence Intent", "Server Members Intent" i "Message Content Intent", aby zapewnić pełną funkcjonalność bota.

### Krok 4: Zaproś swojego bota na serwer
1. Przejdź do zakładki "Installation" po lewej stronie.
2. W sekcji "Installation Contexts" wybierz "Guild Install".
3. W sekcji "Install Link" wybierz "Discord Provided Link".
4. W sekcji "Default Install Settings" wybierz "application.commands" i "bot".
5. Zapisz zmiany, skopiuj wygenerowany URL z **kroku 3** i otwórz go w przeglądarce.
6. Wybierz serwer, na który chcesz zaprosić swojego bota, i kliknij "Authorize".

## **Kroki konfiguracji klastra MongoDB**

### Krok 1: Zarejestruj konto MongoDB Atlas
1. Odwiedź [stronę rejestracji MongoDB Atlas](https://www.mongodb.com/cloud/atlas/register).
2. Wypełnij wymagane informacje, takie jak imię, e-mail i hasło.
3. Kliknij przycisk "Get started free".
4. Zweryfikuj swój adres e-mail, klikając link weryfikacyjny wysłany na Twój e-mail.

### Krok 2: Zaloguj się i utwórz klaster
1. Zaloguj się na swoje konto MongoDB Atlas, używając zarejestrowanego e-maila i hasła.
2. Po zalogowaniu zostaniesz przekierowany na pulpit Atlas. Kliknij "New Project", aby utworzyć nowy projekt.
3. Wprowadź nazwę projektu i kliknij "Next".
4. Kliknij "Build a Cluster", aby utworzyć nowy klaster.
5. Wybierz preferowanego dostawcę chmury i region.
6. Wybierz poziom klastra (dla darmowego poziomu wybierz M0 Sandbox).
7. Kliknij "Create Cluster".

### Dalsze kroki
1. Skonfiguruj adres IP swojego bota, aby zabezpieczyć połączenie z klastrem MongoDB i zapewnić odpowiednią kontrolę dostępu oraz bezpieczeństwo danych.
2. Łańcuch połączenia można uzyskać, klikając w klastrze przycisk "Connect" z wybranym sterownikiem **Mongoose** (najnowsza wersja). Otrzymasz coś w stylu `mongodb+srv://<name>:<db_password>@novabotdatacluster.something.mongodb.net/?retryWrites=true&w=majority&appName=myAppName`.
3. Zmień `<name>` i `<db_password>` na swoje utworzone dane uwierzytelniające i skopiuj cały łańcuch do konfiguracji bota.

### Ostatecznie: Uruchom swojego bota
W terminalu uruchom `node index.js`.

!!! success
    Gotowe! Pomyślnie skonfigurowałeś NovaBot.