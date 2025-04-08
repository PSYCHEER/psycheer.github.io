---
title: 'Cómo contribuir'
description: 'Guía sobre cómo añadir contribuciones a la wiki'
hide:
    - footer
icon: material/github
---

# Cómo contribuir en Github

Contribuir en los repositorios de GitHub es una forma estupenda de ayudar a mejorar proyectos. Para ello, sigue estos pasos para contribuir:

## 1. Copia el repositorio

Primero, deberás copiar el repositorio (en inglés, esta acción es llamada Fork). Esto creará una copia del repositorio en tu propia cuenta de GitHub.

1. Ve al repositorio: [PSYCHEER/psycheer.github.io](https://github.com/PSYCHEER/psycheer.github.io).
2. Dale click al botón llamado "Fork" en la parte superior derecha del repositorio.

## 2. Clona el repositorio copiado

A continuación, copia el repositorio clonado en tu máquina local.

```sh
git clone https://github.com/PSYCHEER/psycheer.github.io.git
cd psycheer.github.io
```

## 3. Crea una nueva rama

Crea una nueva rama (o Branch en inglés) para subir tus cambios.
```sh
git checkout -b my-new-branch
```

Reemplaza el texto que dice my-new-branch con un título descriptivo para tu rama.

## 4. Edita los archivos

Haz los cambios necesarios a los archivos. Puedes usar cualquier editor de texto o IDE para editar éstos.
??? tip
    Nuestra recomendación es usar [VS-Code](https://code.visualstudio.com)

## 5. Sube los cambios

Después de realizar los cambios, guárdalos y súbelos a tu rama (esta acción se llama Commit en inglés).

```sh
git add .
git commit -m "Description of the changes"
```

## 6. Envía los cambios

Envía los cambios a tu repositorio de GitHub (esta acción se llama Push en inglés).

```sh
git push origin my-new-branch
```

## 7. Crea una petición de unión (o Pull request)

Finalmente, puedes crear una nueva petición de unión (o Pull request en inglés) para que tus cambios se unan al repositorio original.

1. Ve a tu repositorio copiado en Github.
2. Dale al botón que dice "Compare & pull request", que te dejará ver los diferenciales y enviar la petición.
3. Escribe un título y una descripción a corde a los cambios realizados.
4. Dale al botón "Create pull request", que enviará esta petición finalmente.

Tu petición será revisada y, si todo está en orden, se unirá como parte oficial del código del proyecto.

¡Gracias por tu contribución! 💖👑