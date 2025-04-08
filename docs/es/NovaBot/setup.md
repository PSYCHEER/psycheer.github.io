---
title: Configurando el bot
description: Guía para la configuración de NovaBot
icon: fontawesome/solid/gear
---

# :fontawesome-solid-gear: Configurar el bot de Discord

## **Prerequisitos**
* Servidor para el bot de Discord
* [NodeJS v22 is LTS](https://nodejs.org/en "Long Term Support") o más reciente
* Licencia [que puede ser obtenida después de comprarse el bot](https://bbb.crafttale.eu)

## **Pasos para instalar el bot**

### Paso 1: Crea la aplicación en Discord
1. Ve al [Portal de Desarrollador de Discord](https://discord.com/developers/applications).
2. Haz clic en el botón de "Nueva aplicación".
3. Dale un nombre a tu aplicación y haz click en "Crear".

### Paso 2: Crea un usuario (bot)
1. En tu nueva aplicación, navega hasta la pestaña "Bot" en la parte izquierda.
2. Puedes customizar el perfil de tu bot estableciendo un avatar y un nombre.
3. Mantén la opción "Bot público" apagada.

!!! tip 
    En la sección de "Información general" puedes establecer un nombre y descripción para tu bot (su biografía).

### Paso 3: Obtén las credenciales de tu bot (Token/Application ID)
1. En la sección "Bot", bajo la sección "TOKEN" dale click a "copiar" para obtener tu Token. **Mantén esto completamente oculto de otros**.
2. El ApplicationID se puede obtener en la sección "Información general".
3. Coloca ambos valores en el archivo de configuración de tu bot en la carpeta raíz (o root) de tu bot.
4. Enciende todas las intenciones, esto incluye "Intención de presencia", "Intención de miembros del servidor" e "Intención de contenido del mensaje" para asegurarte de que todas las funcionalidades del bot no serán limitadas por los permisos de la aplicación.

### Paso 4: Invita al bot a tu servidor de discord
1. Ve a la sección "Instalación" en tu panel lateral izquierdo.
2. En "Contextos de instalación", selecciona "Instalación de hermandad" (o "Instalación de servidor").
3. En "Link de instalación", selecciona el "Enlace proveido por discord".
4. En "Instalaciones por defecto" elige "application.commands" y "bot".
5. Guarda los cambios y copia la URL generada en el **paso 3** y ábrelo en tu navegador.
6. Selecciona el servidor donde quieras invitarle y presiona "Autorizar".

## **Pasos para instalar el MongoDB Cluster (base de datos)**

### Paso 1: Regístrate para obtener cuenta de MongoDB Atlas
1. Visita la [página de registro de MongoDB Atlas](https://www.mongodb.com/cloud/atlas/register).
2. Rellena la información requerida como el nombre, correo y contraseña.
3. Haz click en el botón "Get started free" que será para crear una cuenta gratuita.
4. Verifica tu correo haciendo click en el correo de verificación mandado.

### Paso 2: Identifícate y crea un Cluster
1. Identifícate en la página de MongoDB Atlas usando tu correo y contraseña creados.
2. Una vez identificado, serás redirigido al panel de Atlas. Haz cli en "New project" para crear un nuevo proyecto.
3. Escribe un nombre para el proyecto y presiona "Next".
4. Haz click en "Build a Cluster" para crear un nuevo Cluster.
5. Elige tu proveedor de espacio en la nube y tu región.
6. Selecciona el tier del Cluster (para el gratuito, elige M0 Sandbox)-
7. Haz click en "Create cluster".

### Siguientes pasos
1. Establece la IP de tu bot para asegurarte de que conectará con el MongoDB Cluster y asegurar el correspondiente acceso de control y seguridad.
2. La dirección de conexión (o connection string) puede ser obtenida haciendo click en el cluster en el botón de "Connect" cuando seleccionad el driver **Mongoose** (en su última versión) y obtendrás algo como `mongodb+srv://<name>:<db_password>@novabotdatacluster.something.mongodb.net/?retryWrites=true&w=majority&appName=myAppName`
3. Cambia `<name>` y `<db_password>` con tus credenciales generadas y pega la dirección en la configuración de tu bot.

### Final: Inicia tu bot
En tu terminal, ejecutan `node index.js`.

!!! success
    ¡Ya está! ¡Has creado y ejecutado con éxito tu NovaBot!