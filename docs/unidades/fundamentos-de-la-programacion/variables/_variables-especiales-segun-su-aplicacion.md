title: Variables especiales según su aplicación

## Acumulador

* Es una variable cuyo valor aumenta o disminuye en una cantidad variable cada vez que se produce un determinado suceso o acción.
* Debe ser inicializada.

``` py title="Python: Se desea acumular las notas de prácticas de un alumno."
suma = 0 # el valor de sum es 0
suma = suma + 13 # el valor de sum es 13
suma = suma + 10 # el valor de sum es 23
```

## Contador

* Es un acumulador cuyo valor aumenta o disminuye en una cantidad constante cada vez que se produce un determinado suceso o acción.
* Se usa para contar sucesos

``` py title"=Python: Contar número de aprobados."
aprobados = 0 # la cantidad de aprobados es 0
for nota in listado_de_notas:
    if (nota >= 6):
        aprobados = aprobados + 1 # la cantidad de aprobados se incrementa en 1
```

## Resumen

!!! success "¡Muy importante!"
    Una variable es un espacio de almacenamiento (dirección) reservado en la memoria (RAM) de una computadora, que tiene un nombre o identificador único asociado dentro de su ámbito o alcance, y cuyo tamaño está definido por el tipo de dato asociados y que contiene un valor o una referencia a un valor.

Por lo tanto, todo dato que vaya a ser introducido a la computadora, y todo dato que vaya a ser generado o calculado a partir de otros datos para obtener algún resultado, debe identificarse y manejarse como variable. 

Una variable posee 4 características:

* El alcance, que determinará en qué partes del programa (región del programa) la variable podrá ser accedida o utilizada.
* El identificador o nombre, que servirá para referenciarla a lo largo de la ejecución del programa. 
* El tipo de dato, que determinará como va a almacenar un dato para evitar errores.
* El dato o información que se almacenará durante la ejecución del programa.

El ciclo de vida de una variable puede variar según el lenguaje de programación utilizado y el alcance en el que se utiliza la variable. Por ejemplo, en algunos lenguajes, las variables pueden tener un alcance limitado a una función o bloque de código, mientras que en otros pueden tener un alcance global en todo el programa. Este tema lo veremos más adelante.

Resumiendo, es importante destacar que los detalles específicos de la creación de variables pueden variar según el lenguaje de programación que estés utilizando. Algunos lenguajes tienen reglas y convenciones adicionales para la creación de variables, como restricciones en los nombres o requisitos de ámbito.

Durante la etapa de utilización de una variable, estas se utilizan en expresiones y operaciones como asignación de valores, lectura de valores, modificación de valores y se tiene en cuenta el alcance y el tipo de dato de la variable. Esto permite utilizar las variables para almacenar y manipular datos en el programa de acuerdo con su propósito y alcance.

Por último, en la etapa de destrucción de una variable se llevan a cabo acciones para liberar los recursos asociados a ella y finalizar su existencia en el programa. Esto puede implicar la liberación de memoria asignada o la finalización del ámbito en el que se encuentra. Los detalles específicos de la destrucción pueden variar según el lenguaje de programación utilizado. Algunos lenguajes tienen mecanismos adicionales de gestión de memoria, como destructores o métodos especiales, que permiten ejecutar acciones personalizadas antes de la destrucción de una variable, como liberar otros recursos o realizar tareas de limpieza.

!!! info "¡Importante!"
    En la mayoría de los lenguajes de programación, antes de que una variable pueda ser usada en un programa, esta debe ser declarada, incluyendo el tipo de dato que serán almacenados en ella. 

Declarar una variable significa crear una nueva variable en el programa, definiendo su identificador y reservando el espacio necesario en la memoria según el tipo de dato que almacenará durante la ejecución del programa, pero sin asignarle valor.

Para declarar una variable, se debe especificar su nombre, su tipo y su alcance, si aplica. 

Una vez que se ha declarado una variable, podemos asignarle un valor utilizando el operador de asignación =

Asignar un valor a una variable significa almacenar un valor en el espacio de memoria reservado para ella.

Inicializar una variable significa declararla y, además, asignarle un valor inicial.

D (eclaración) + A (signación) = I (nicialización)

|Declaración + Asignación | Inicialización |
|:---:|:---:|
| int edad | int edad = 18 |
| edad = 18 | |

!!! important "¡Para recordar!"
    Hablando de como se lee la sintaxis en un lenguaje humanizado, cualquier lectura que lleve a la correcta interpretación de la instrucción, es válida. Para que ello ocurra, no puede existir ambigüedad posible. Si la lectura puede interpretarse de dos o maneras diferentes, entonces será inválida.

Recordemos la sintaxis:

``` title="Declaración"

nombre_de_tipo_de_dato nombre_de_variable
```

``` title="Asignación"

nombre_de_variable = expresión (asignación_de_valor)
```

``` title="Inicialización"

nombre_de_tipo_de_dato nombre_de_variable = expresión (asignación_de_valor)
```

La estructura de la sintaxis dependerá de si la acción es una declaración, una inicialización o una asignación.

También dependerá de como se escriba en cada lenguaje particular.
