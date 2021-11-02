# GRID-GARDEN

- Cuando grid-column-start se usa solo, la expansión por defecto del elemento en la cuadrícula será de exactamente una columna. No obstante, puedes extender el elemento varias columnas añadiendo la propiedad grid-column-end.

- Al emparejar grid-column-start y grid-column-end, podrías asumir que el valor final tiene que ser mayor que el valor inicial. 
  
 - Si prefieres contar las líneas de la cuadrícula comenzando por la derecha, puedes dar a grid-column-start y grid-column-end valores negativos. Por ejemplo, puedes establecerlos a -1 para indicar la primera línea comenzando por la derecha.

- En lugar de definir un elemento en la cuadrícula basado en la posicion inicial y final, puedes definirlo basado en la longitud de columnas deseada usando la palabra clave span. Ten presente que span solo funciona con valores positivos.

- Escribir ambos grid-column-start y grid-column-end cada vez puede resultar cansado. Afortunadamente, grid-column es una propiedad abreviada que acepta ambos valores a la vez, separados por una barra oblicua.

- Si escribir grid-column y grid-row se te hace demasiado pesado, aquí tienes otra propiedad abreviada. grid-area admite cuatro valores separados por barras oblicuas: grid-row-start, grid-column-start, grid-row-end, seguido de grid-column-end.
Un ejemplo de esto podría ser grid-area: 1 / 1 / 3 / 6;.

- Si los elementos de la cuadrícula no se sitúan explícitamente con grid-area, grid-column, grid-row, etc., se sitúan automáticamente de acuerdo al orden en el código fuente. Puedes sobrescribir esto usando la propiedad order, que es una de las ventajas de la cuadrícula frente al diseño basado en tablas.

- Por defecto, el valor de order de todos los elementos es igual a 0, pero puede ser establecido a cualquier valor positivo o negativo, de manera similar a z-index.

- Esto ha sido establecido con las propiedades grid-template-columns: 20% 20% 20% 20% 20%; y grid-template-rows: 20% 20% 20% 20% 20%;. Cada propiedad tiene cinco valores que crean cinco columnas, cada una establecida al 20% de la anchura total del jardín.

- Especificar un puñado de columnas con la misma anchura puede ser aburrido. Afortunadamente hay una función repeat que te ayudará con eso.

- Por ejemplo, previamente hemos definido cinco columnas al 20% de anchura mediante grid-template-columns: 20% 20% 20% 20% 20%;. Esto puedes simplificarse como grid-template-columns: repeat(5, 20%);

- Usando grid-template-columns con la función repeat, crea ocho columnas, cada una con una anchura del 12.5%. 

