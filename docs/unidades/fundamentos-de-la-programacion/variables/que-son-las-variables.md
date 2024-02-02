title: ¿Qué son las variables?

# ¿Qué son las variables?

<label class="revision">Rev. 11/01/2024</label>

!!! abstract "Definición"
    Una variable es un espacio de almacenamiento reservado en la memoria central (RAM) de una computadora, que tiene un nombre o identificador único asociado dentro de su ámbito o alcance, y cuyo tamaño está definido por el tipo de dato asignado y que puede contener un valor o una referencia a un valor que puede ser reemplazado durante la ejecución de un programa.

Analicemos esta definición:

* Una variable es un elemento fundamental de la programación que permiten almacenar un dato en la memoria RAM para luego poder ser accedido y reemplazado en algún momento de la ejecución del programa. 

* Para poder llegar a este dato almacenado, la variable debe contar con un nombre único que la identifique respecto de otras variables en un conjunto determinado de variables que se encontrará aislado de otros posibles conjuntos de variables existentes durante la ejecución del programa.

* A su vez, la variable deberá tener asignado un espacio de almacenamiento lo suficientemente grande para albergar al mayor de los valores de un determinado tipo de dato sin que se pierda parte de su contenido.

**Identificador**, **alcance**, **tipo de dato** y **valor** son características de una variable que estudiaremos a más adelante.

!!! success "¡Para pensar!"
    Las variables pueden ser consideradas como la base de la programación. Un programa que debe resolver un problema, si no tuviera variables para almacenar datos, no habría datos para procesar y por consiguiente no habría información procesada para que el programa la presente como solución.

    Por lo tanto, una variable actúa como un contenedor que puede almacenar un dato.

Por ejemplo, si estamos escribiendo un algoritmo que pide al usuario que ingrese su edad, podemos crear una variable llamada _edad_ que será utilizada para almacenar el dato ingresado por el usuario:

``` title="Lenguaje natural" linenums="1"
Solicitar al usuario que ingrese su edad
Almacenar el dato ingresado por el usuario en la variable *edad*
```

A continuación, podemos realizar diferentes procesos con el dato ingresado simplemente con acceder a la variable en cuestión simplemente con nombrarla:

``` title="Lenguaje natural" linenums="3"
Si *edad* es mayor o igual a 18 entonces indicar al usuario que es mayor de edad.
Si no, indicar al usuario que no es mayor de edad.
```

También podemos crear variables que almacenen datos o información producidos dentro del programa. Por ejemplo, si quisiéramos llevar la cuenta de cuantos mayores de edad interactuaron con el programa, deberíamos modificarlo de la siguiente manera:

``` title="Lenguaje natural" linenums="1"
Crear la variable *cant_mayores* con un valor inicial de 0

Solicitar al usuario que ingrese su edad
Almacenar el dato ingresado por el usuario en la variable *edad*

Si *edad* es mayor o igual a 18 entonces 
    Indicar al usuario que es mayor de edad
    Incrementar en 1 el valor de la variable *cant_mayores*
Si no, indicar al usuario que no es mayor de edad.
```

> Nota que las líneas 7 y 8 están indentadas, tabuladas, es decir, corridas ligeramente en su alineación hacia la derecha, respecto del código principal. Esto significa que nuestro algoritmo posee un bloque de código dentro de otro bloque de código y que se va a comportar de una manera específica. En este caso, este bloque de código compuesto por las líneas 7 y 8 solo se ejecutarían si la condición indicada en la línea 6 fuese verdadera.

!!! important "¡Para recordar!" 
    Todo dato que se introduce en un programa o que se genere como consecuencia de algún proceso durante la ejecución del programa debe ser almacenado en una variable. Caso contrario, dicho dato se perderá para siempre al finalizar la línea de código que lo solicitó o generó y pasar a la siguiente línea de código.
    