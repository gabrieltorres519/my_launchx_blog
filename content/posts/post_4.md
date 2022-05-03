---
title: "Los objetos pelones de Javascript y Modularización!!"
date: 2022-04-21
description: 'Launch X Backend'
---

Objetos pelones de Javascript 🖥️

### Los objetos

Los conceptos principales de javascript son los objetos (let dentro de funciones, var fuera de funciones, const para objetos casi siempre).

Un objeto es como un diccionario donde puedes poner una llave y un valor.

Ejemplo la llave que nombramos model:

```jsx
let mycar = new Objetc();

mycar.model = "Audi"
```

Mismo procedimiento en consola con el REPL de node.

Se permiten tantas llaves y valores como quieras.

### El concepto de modularización.

Si el código no se hace modular lidias con variables globales para todo el archivo, si solo lo separabas era lo mismo porque al final todo se iba a cargar en el mismo concepto de la página.

En node puedes tener objetos y funciones, en Javascrip-Node las funciones se usan para aislar infomración, para artificialmente crear la “encapsulación” de parámetros (o también de atributos para POO).

Una función en sintaxis de Javascript luce así.

```jsx
let myFunction = (argumentos) => {lo que harás}
```


En el contexto de los objetos de javascript las funciones nos servirán para aislar información.

Nos sirven para aislar información pues como podemos ver, solo lo que la función exporte es lo que podremos ver o acceder (forma artificial de hacer encapsulación POO).

No se nos permite acceder a privatefoo y verlo con console.log pues no es exportado por la función.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/bb72eb3c-7ffb-4530-8a23-5b10ee6552f2/Untitled.png)

Así escondemos info.

Ya que esto es un concepto de Javascript y no propiamente de node de momento, podemos trabajar esto en la consola del navegador que nativamente sabe javascript.

Es recomendable probar el comportamiento de nuestro código javascript en la consola del navegador para ver su comportamiento ya en el navegador.

Esta encapsulación artificial con funciones es lo que nos permitirá modularizar nuestro proyecto en realidad.

Todo esto es necesario para encapsular en Javascrip pero NodeJS nos resuelve esta modularización para que no la tengamos que hacer manualmente con funciones.

La modularización con funciones es manejada en commonjs con exports.

**Formas de exportar contenidos dentro de archivos.**

- exports.nombre_de_mi_función_flecha = (input) = > { console.log(` myinfo jeje: ${input} `); }
- module.exports = nombre_de_clase_que_queramos_exportar
- export default class clase_Creada {}  //También se pueden exportar así funciones y constantes.

Una ventaja de module.exports es que podemos exportar objetos ya instanciados y no solo la clase entera.

module.exports = new myClass(’contenido para su constructor’);

**Formas de importar archivos.**

1 Con la sintaxis de Commonjs que se creo para modularizar el código js. 

- const nombre = require(’./ruta_del_archivo_con_las_funciones_y_objetos_que_ocupo’);Con

2 Con la sintaxis de Ecmascript optimizada para el uso de package.json y con ello uso de módulos de terceros que son muy grandes y solo queremos jalar partes específicas.

- *import* { función_u_objeto_o_variable_exportada_en_el_archivo } *from* './archivo.js'

El equivalente en Ecmascript para importar el archivo completo como en Commonjs es así:

- *import* * *as* loggerModule *from* './logger.js'
