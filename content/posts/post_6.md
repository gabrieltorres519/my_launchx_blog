---
title: "TDD: Las pruebas NO SON NEGOCIABLES!!"
date: 2022-04-26
description: 'Launch X Backend'
---

TDD 🖥️

## Creación de un proyecto de NodeJS aproximación con TDD

1. npm init
2. npm install --save-dev jest
3.  crear el archivo .gitignore y dentro escribir /node_modules para no versionarlos
4. agregar el script de test “node ./node_modules/.bin/jest”  esto en Linux
5. git init
6. git remote add origin url
7. git status
8. git add *
9. git commit -m “1. Primer commit, proyecto iniciado y jest instalado”
10. git push origin master
11. npm install express --save  (en casos de que vallas a crear un servidor)
12. crear el archivo app.js  (en casos de que vallas a crear un servidor)
    
    

Scripts necesarios en el package.json

```jsx
"scripts": {
"test": "node ./node_modules/.bin/jest",
"linter": "node ./node_modules/eslint/bin/eslint.js .",
"linter-fix": "node ./node_modules/eslint/bin/eslint.js . --fix"
}
```


## Cuándo usar git pull?

Cuando realizaste algún commit desde la herramienta visual de GitHub pero ya lo estabas trabajando desde la terminal de tu PC, estos no serán iguales y no te permitirá seguir haciendo más commits, hasta que retornes al estado del repositorio en GitHub, así que descargas la “fotografía del estado” con **git pull origin master**

## ¿Qué es Postman?

“Postman is a full feature API Development Tool which helps you to manage your APIs at every stage of your development, form designing and testing to publishing. También nos sirve para monitorear nuestra API”.
