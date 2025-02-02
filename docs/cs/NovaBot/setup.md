---
title: Nastavení bota
description: Průvodce nastavením NovaBot
icon: fontawesome/solid/gear
---

# :fontawesome-solid-gear: Nastavení Discord Bota

## **Požadavky**
* Discord Bot Server
* [NodeJS v22 je LTS](https://nodejs.org/en "Long Term Support") nebo novější
* Minimálně 256MB RAM pro provoz bota.
* Licence [lze získat na našem Discordu po zakoupení](https://bbb.crafttale.eu)

## **Kroky k nastavení NovaBot**

### Krok 1: Vytvoření Discord Aplikace
1. Přejděte na [Discord Developer Portal](https://discord.com/developers/applications).
2. Klikněte na tlačítko "New Application".
3. Dejte své aplikaci jméno a klikněte na "Create".

### Krok 2: Vytvoření Bot Uživatele
1. Ve vaší nové aplikaci přejděte na záložku "Bot" vlevo.
2. Můžete přizpůsobit profil svého bota nastavením avatara a jména.
3. Vypněte nastavení "Public Bot".

!!! tip 
    V "General Information" můžete nastavit zobrazované jméno a popis (bio) vašeho bota.

### Krok 3: Získání přihlašovacích údajů bota (Token/Application ID)
1. V záložce "Bot", v sekci "TOKEN", klikněte na "Copy" pro získání tokenu vašeho bota. **Udržujte tento token v tajnosti**.
2. ApplicationID lze nalézt v "General Information".
3. Umístěte obě tyto hodnoty do konfiguračního souboru bota v kořenové složce bota.
4. Zapněte všechny záměry "Presence Intent", "Server Members Intent" a "Message Content Intent" pro zajištění plné funkčnosti bota.

### Krok 4: Pozvání Bota na Server
1. Přejděte na záložku "Installation" vlevo.
2. V sekci "Installation Contexts" vyberte "Guild Install".
3. V sekci "Install Link" vyberte "Discord Provided Link".
4. V sekci "Default Install Settings" vyberte "application.commands" a "bot".
5. Uložte změny a zkopírujte vygenerovanou URL z **kroku 3** a otevřete ji ve svém prohlížeči.
6. Vyberte server, na který chcete bota pozvat, a klikněte na "Authorize".

## **Kroky k nastavení MongoDB Clusteru**

### Krok 1: Registrace na MongoDB Atlas
1. Navštivte [registrační stránku MongoDB Atlas](https://www.mongodb.com/cloud/atlas/register).
2. Vyplňte požadované informace jako jméno, email a heslo.
3. Klikněte na tlačítko "Get started free".
4. Ověřte svou emailovou adresu kliknutím na ověřovací odkaz zaslaný na váš email.

### Krok 2: Přihlášení a Vytvoření Clusteru
1. Přihlaste se do svého MongoDB Atlas účtu pomocí registrovaného emailu a hesla.
2. Po přihlášení budete přesměrováni na dashboard Atlas. Klikněte na "New Project" pro vytvoření nového projektu.
3. Zadejte název projektu a klikněte na "Next".
4. Klikněte na "Build a Cluster" pro vytvoření nového clusteru.
5. Vyberte preferovaného poskytovatele cloudu a region.
6. Vyberte úroveň clusteru (pro bezplatnou úroveň vyberte M0 Sandbox).
7. Klikněte na "Create Cluster".

### Následné Kroky
1. Nastavte IP adresu vašeho bota pro zabezpečené připojení do MongoDB clusteru pro zajištění správné kontroly přístupu a bezpečnosti dat.
2. Připojovací řetězec lze získat kliknutím na tlačítko "Connect" v clusteru s vybraným ovladačem **Mongoose** (nejnovější verze) a získáte něco jako `mongodb+srv://<name>:<db_password>@novabotdatacluster.something.mongodb.net/?retryWrites=true&w=majority&appName=myAppName`
3. Změňte `<name>` a `<db_password>` na vaše vytvořené přihlašovací údaje a zkopírujte celý řetězec do konfiguračního souboru bota.

### Závěrečný Krok: Spuštění Vašeho Bota
Ve vašem terminálu spusťte `node index.js`.

 <!-- Nepřekládejte "Pterodactyl Panel", pouze pod ním -->
??? tip "Pterodactyl Panel"
    Pro Pterodactyl panel zadejte `index.js` do `Main file` v záložce `Startup`.

!!! success
    Hotovo! Úspěšně jste nastavili svého NovaBota.