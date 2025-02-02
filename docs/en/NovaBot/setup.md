---
title: Setting up the bot
description: Guide for NovaBot set up
icon: fontawesome/solid/gear
---

# :fontawesome-solid-gear: Setting Up a Discord Bot

## **Prerequisites**
* Discord Bot Server
* [NodeJS v22 is LTS](https://nodejs.org/en "Long Term Support") or newer
* Minimum of 256MB of RAM for the bot to operate.
* License [can be obtained on our Discord after purchase](https://bbb.crafttale.eu)

## **Steps to set up NovaBot**

### Step 1: Create a Discord Application
1. Go to the [Discord Developer Portal](https://discord.com/developers/applications).
2. Click on the "New Application" button.
3. Give your application a name and click "Create".

### Step 2: Create a Bot User
1. In your new application, navigate to the "Bot" tab on the left.
2. You can customize your bot's profile by setting an avatar and name.
3. Turn "Public Bot" setting off.

!!! tip 
    In "General Information" you can set up display name for your bot and description (bio).

### Step 3: Get Your Bot’s credentials (Token/Application ID)
1. In the "Bot" tab, under the "TOKEN" section, click "Copy" to get your bot's token. **Keep this token secret**.
2. ApplicationID can be found in "General Information".
3. Place both of these values into bot configuration file in root folder of the bot.
4. Turn on all intents "Presence Intent", "Server Members Intent" and "Message Content Intent" to ensure bot's full functionality.

### Step 4: Invite Your Bot to a Server
1. Go to the "Installation" tab on the left.
2. Under "Installation Contexts", select the "Guild Install".
3. Under "Install Link", select the "Discord Provided Link".
4. Under "Default Install Settings" choose "application.commands" and "bot".
5. Save changes and copy the generated URL from **step 3** and open it in your browser.
6. Select the server you want to invite your bot to and click "Authorize".

## **Steps to set up MongoDB Cluster**

### Step 1: Register for a MongoDB Atlas Account
1. Visit the [MongoDB Atlas registration page](https://www.mongodb.com/cloud/atlas/register).
2. Fill in the required information such as name, email, and password.
3. Click the "Get started free" button.
4. Verify your email address by clicking on the verification link sent to your email.

### Step 2: Log in and Create a Cluster
1. Log in to your MongoDB Atlas account using your registered email and password.
2. Once logged in, you will be directed to the Atlas dashboard. Click on "New Project" to create a new project.
3. Enter a project name and click "Next".
4. Click on "Build a Cluster" to create a new cluster.
5. Choose your preferred cloud provider and region.
6. Select the cluster tier (for the free tier, choose M0 Sandbox).
7. Click "Create Cluster".

### Follow-up Steps
1. Set up IP Adress of your bot to secure connect into the MongoDB cluster to ensure proper access control and data security.
2. Connection string can be get trough clicking in cluster on "Connect" button with **Mongoose** driver selected (latest version) and you'll get something like `mongodb+srv://<name>:<db_password>@novabotdatacluster.something.mongodb.net/?retryWrites=true&w=majority&appName=myAppName`
3. Change `<name>` and `<db_password>` with your created credentials and copy the whole string into bot's configuration.

### Final: Run Your Bot
In your terminal, run `node index.js`.

 <!-- Do not translate "Pterodactyl Panel", only underneath -->
??? tip "Pterodactyl Panel"
    For Pterodactyl panel type `index.js` into `Main file` in `Startup` tab.

!!! success
    That's it! You have successfully set up your NovaBot.