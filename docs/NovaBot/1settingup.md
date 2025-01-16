---
title: Setting up the bot
description: Guide for NovaBot set up
---

# Setting Up a Discord Bot

## Step 1: Create a Discord Application
1. Go to the [Discord Developer Portal](https://discord.com/developers/applications).
2. Click on the "New Application" button.
3. Give your application a name and click "Create".

## Step 2: Create a Bot User
1. In your new application, navigate to the "Bot" tab on the left.
2. You can customize your bot's profile by setting an avatar and name.
3. Turn "Public Bot" setting off.

## Step 3: Get Your Bot’s credentials (Token/Application ID)
1. In the "Bot" tab, under the "TOKEN" section, click "Copy" to get your bot's token. **Keep this token secret**.
2. ApplicationID can be found in "OAuth2" under name "ClientID".
3. Place both of these values into bot configuration file in root folder of the bot.
4. Turn on all intents "Presence Intent", "Server Members Intent" and "Message Content Intent" to ensure bot's full functionality.

## Step 4: Invite Your Bot to a Server
1. Go to the "Installation" tab on the left.
2. Under "Installation Contexts", select the "Guild Install".
3. Under "Install Link", select the "Discord Provided Link".
4. Under "Default Install Settings" choose "application.commands" and "bot".
5. Save changes and copy the generated URL from **step 3** and open it in your browser.
6. Select the server you want to invite your bot to and click "Authorize".

# Setting up the Mongo

## Step X: Run Your Bot
In your terminal, run `node index.js`.

That's it! You have successfully set up your NovaBot.