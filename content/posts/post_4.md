---
title: "Los objetos pelones de Javascript!!"
date: 2022-04-21
description: 'Launch X Backend'
---

Objetos pelones de Javascript 🖥️

Los conceptos principales de javascript son los objetos (let dentro de funciones, var fuera de funciones, const para objetos casi siempre).

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/07214928-bfd2-4460-90ce-055715812efc/Untitled.png)

Un objeto es como un diccionario donde puedes poner una llave y un valor.

Ejemplo la llave que nombramos model:

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/2813408d-2c1a-4c7f-b543-73170a62e6ab/Untitled.png)

Mismo procedimiento en consola con el REPL de node.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/61d0bc10-3147-4833-9454-c8bd91660082/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/c9eb7f46-a1ec-469c-b239-db286c0ebc44/Untitled.png)

Se permiten tantas llaves y valores como quieras.

Vamos a comentar el concepto de modularización.

Si el código no se hace modular lidias con variables globales para todo el archivo, si solo lo separabas era lo mismo porque al final todo se iba a cargar en el mismo concepto de la página.

En node puedes tener objetos y funciones, en Javascrip-Node las funciones se usan para aislar infomración, para artificialmente crear la “encapsulación” de parámetros (o también de atributos para POO).

Una función en sintaxis de Javascript luce así.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/b341978d-9a82-492d-82ab-7262a1735a88/Untitled.png)

En el contexto de los objetos de javascript las funciones nos servirán para aislar información.

 

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/a1c0bae6-0102-49b2-814f-e1e276012a92/Untitled.png)

Nos sirven para aislar información pues como podemos ver, solo lo que la función exporte es lo que podremos ver o acceder (forma artificial de hacer encapsulación POO).

No se nos permite acceder a privatefoo y verlo con console.log pues no es exportado por la función.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/bb72eb3c-7ffb-4530-8a23-5b10ee6552f2/Untitled.png)

Así escondemos info.

Ya que esto es un concepto de Javascript y no propiamente de node de momento, podemos trabajar esto en la consola del navegador que nativamente sabe javascript.

Es recomendable probar el comportamiento de nuestro código javascript en la consola del navegador para ver su comportamiento ya en el navegador.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/15bfd533-7187-49b3-99db-d6d91bf2acbb/Untitled.png)

Esta encapsulación artificial con funciones es lo que nos permitirá modularizar nuestro proyecto en realidad.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/e9fbbc3c-a95e-44c8-bbe6-3f4078224e75/Untitled.png)

En navegador si escribimos mymodule nos regresará una función

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/8708d760-8ffe-47e6-a3fb-06b0f11dddb7/Untitled.png)

Pare ejecutar la función usamos myModule()

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/d16e3171-2d66-47f0-83dc-366812fbab81/Untitled.png)

Nótese que la función retorna un objeto y para extraer el atributo del objeto retornado se usa la función con el operador punto myModule().publicFoo.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/f9423c1e-4605-40e5-92e5-54ff6236ac13/Untitled.png)

Todo esto es necesario para modularizar Javascrip pero NodeJS nos resuelve esta modularización para que no la tengamos que hacer manualmente con funciones.

La modularización con funciones es manejada en commonjs con exports.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/042c44fc-b30d-4c4c-aa55-092cbafe48e6/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/c0804f11-81e5-4c6a-b193-939545abdb60/Untitled.png)

Estas funciones son exportadas y las podemos importar desde cualquier otro archivo (el nombre se le puso logger porque lo único que hace es exportar funciones que hacen console.log()).

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/f6fc797e-07ba-46f0-99ee-8053616a3952/Untitled.png)

Por convención “require(’./ruta_del_archivo_con_las_funciones_y_objetos_que_ocupo’)” se usa en proyecto server.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/700e259e-fa7a-45c0-88b8-860aacedcda8/Untitled.png)

Al correr con NodeJS nuestro archivo main.js podemos ver que ha obtenido correctamente los contenidos de las funciones en el archivo logger.js
