title: Dato asignado a una variable

# Dato asignado a una variable

<label class="revision">Rev. 11/01/2024</label>

!!! abstract "Definición"
    Se denomina **dato asignado** al dato o información que se almacena en una variable, en la memoria central (RAM), para poder ser utilizado por el programa.

    Este dato asignado deberá ser del mismo tipo de dato asociado a la variable.

Por ejemplo, 

``` Go title="Código generalizado"
int a = 10;
```

> El dato almacenado en la variable `a` es el número entero `10`. 

``` Go title="Código generalizado"
string b = "Hello, World!";
```

> El dato almacenado en la variable `b` es la cadena de caracteres `"Hello, World!"`.

La variable, mientras exista y sea visible, puede ser accedida y el dato almacenado en ella puede ser leído y modificado durante la ejecución del programa.

El espacio en memoria que ocupa la variable se liberará cuando la variable deje de existir (por ejemplo, cuando se salga del alcance en el que fue declarada, cuando se elimine la variable o cuando el programa finalice su ejecución).

## Proceso de asignación de un dato a la variable

La asignación de un dato a una variable se realiza mediante una sentencia de asignación durante el programa:

``` title="Pseudocódigo"
# representación simplificada de cómo se asigna un valor a una variable en programación

variable ⬅ valor_para_asignar
```

> `valor_para_asignar` es el valor que quieres guardar, y `variable` es el identificador de la variable en la que quieres guardar dicho valor.
> 
> El símbolo ⬅ representa la operación de asignación.  
> En la mayoría de los lenguajes de programación, esta operación se representa con el símbolo igual ( = ). 

Por ejemplo, en Python, la instrucción se vería así:

``` py title="Python"
variable = valor_para_asignar
```

> En este código, el valor de `valor_para_asignar` es asignado a la variable `variable`. Después de esta operación, siempre que se utilice `variable` en el programa, devolverá el valor que le fuera asignado, hasta que dicho valor cambie, o la variable se destruya o finalice el programa.
>
> Este valor puede ser, por ejemplo:
> 
> * un dato o información ingresada al programa (a través del teclado por ejemplo)
> * el dato almacenado en otra variable (en este caso sería la variable `valor_para_asignar`)
> * el resultado de una expresión (en este caso la expresión estaría representada por `valor_para_asignar`)
> * el resultado retornado por una función (en este caso la función estaría representada por `valor_para_asignar`)

Por ejemplo, se puede asignar el valor `10` a la variable `x` de la siguiente manera:

``` py title="Código generalizado"
int x   # Declara la variable x como tipo de dato entero
x = 10  # Asigna el valor 10 a la variable x
```

Después de esta operación, la variable `x` contendrá el valor asignado `10`.  
Este valor permanecerá almacenado en la memoria central (RAM) reservada para la variable, hasta que sea reemplazado, o que la variable sea destruida (eliminada del programa), o que el programa finalice.
Mientras tanto, es posible acceder al valor simplemente invocando a la variable por su identificador:

``` py title="Código generalizado"
print(x)  # Imprime 10 en pantalla

print(x * 2)  # Imprime 20 en pantalla

print(x < 20)  # Imprime False en pantalla
```

Siempre que se utilice la variable `x` en ele programa, representará el valor que se le asignó (`10`).

## Proceso de reemplazo del dato asignado a una variable

Es importante entender que acceder a un dato almacenado en una variable para efectuar operaciones no es la única acción que se puede realizar con la variable.  

Es posible que sea necesario, durante la ejecución del programa, modificar el dato almacenado en una variable por otro dato, actualizado al momento de ejecución.

Esta modificación, en realidad, es un reemplazo de un dato por otro dato que, aunque represente el mismo valor, siempre va a ser distinto.

Esto significa que cuando se reemplaza un dato almacenado por otro dato, el dato anterior se elimina, se pierde para siempre.

Si volvemos al ejemplo anterior, `x` tiene asignado el valor `10`. Ahora vamos a reemplazar ese valor por el doble. Y luego lo vamos a reemplazar por el valor `7`, imprimiendo el valor que posea `x` luego de cada operación:

``` py title="Código generalizado"
int x   # Declara la variable x como tipo de dato entero
x = 10  # Asigna el valor 10 a la variable x
print(x)  # Imprime 10 en pantalla

x = x * 2  # Duplica el valor de x y asigna el resultado a la variable x
print(x)  # Imprime 20 en pantalla

x = 7  # Asigna el valor 7 a la variable x
print(x)  # Imprime 7 en pantalla
```

Como podemos observar, la sintaxis es la misma siempre: `variable = valor_para_asignar`:

``` py title="Código generalizado"
⋮
x = 10  # Asigna el valor 10 a la variable x
⋮
x = x * 2  # Duplica el valor de x y asigna el resultado a la variable x
⋮
x = 7  # Asigna el valor 7 a la variable x
⋮
```

!!! important "¡Para recordar!"
    En ciertos lenguajes de programación dinámicos, el tipo de dato de una variable puede cambiar con cada nueva asignación de valor:

    ``` py title="Python"
    # Asignación de un número entero
    variable = 10
    print(type(variable))  # <class 'int'>

    # Asignación de un texto
    variable = "Hola Mundo"
    print(type(variable))  # <class 'str'>

    # Asignación de una lista
    variable = [1, 2, 3]
    print(type(variable))  # <class 'list'>

    # Asignación de un número flotante
    variable = 3.14
    print(type(variable))  # <class 'float'>
    ```

    > En este código, la variable `variable` cambia de tipo con cada nueva asignación de valor. Primero es un entero, luego una cadena de texto, luego una lista y finalmente un número flotante.

## Proceso de eliminación del dato asignado a una variable

En la mayoría de los lenguajes de programación, no se puede **eliminar** un dato de una variable en el sentido de dejar la variable en un estado no asignado. En su lugar, puedes asignar un **valor nulo** o predeterminado a la variable.

Por ejemplo, en Python, puedes asignar `None` a una variable para indicar que no tiene un valor:

``` py title="Python"
variable = 10
print(variable)  # Imprime 10

variable = None
print(variable)  # Imprime None
```

En lenguajes como C++ o Java, puedes asignar un valor predeterminado como `0` o `NULL`:

``` Java title="Java"
int variable = 10;
System.out.println(variable);  // Imprime 10

variable = 0;
System.out.println(variable);  // Imprime 0
```

``` c++ title="C++"
int variable = 10;
std::cout << variable << std::endl;  // Imprime 10

variable = NULL;
std::cout << variable << std::endl;  // Imprime 0
```

!!! important "¡Para recordar!"
    La asignación de un valor nulo o predeterminado es diferente de **eliminar** la variable. 
    
    La variable todavía existe en la memoria, simplemente su valor ha sido cambiado. Ya estudiaremos como eliminar una variable, más adelante.

## ¿Qué es la asignación múltiple?

La asignación múltiple, válido en ciertos lenguajes como Python, JavaScript (ES6 y posteriores), PHP y Ruby, entre otros, es una característica que permite asignar valores a varias variables al mismo tiempo en una sola línea de código. Esto se puede hacer de varias maneras.

Asignación de múltiples variables:

``` py title="Python"
a, b, c = 1, 2, 3
```

> En este código, 1 se asigna a `a`, 2 se asigna a `b`, y 3 se asigna a `c`.

Asignación de un mismo valor a múltiples variables:

``` py title="Python"
a = b = c = 1
```

> En este código, a `a`, a `b` y a `c` se les asigna 1.

Desempaquetado de listas o tuplas:

``` py title="Python"
numeros = [1, 2, 3]
a, b, c = numeros
```

> En este código, los valores de la lista `numeros` son asignados en orden de posición a `a`, a `b` y a `c` respectivamente.

La asignación múltiple puede hacer que el código sea más conciso y legible, pero también puede hacer que el código sea más difícil de entender si se usa de manera excesiva o en situaciones complejas.

Así, puede ser tanto una buena como una mala práctica, dependiendo del contexto y de cómo se utilice.

!!! success "Es una buena práctica cuando:"
    * Mejora la legibilidad del código al agrupar las declaraciones relacionadas.
    * Reduce la cantidad de líneas de código, lo que puede hacer que el código sea más fácil de leer y mantener.
    * Puede ser una mala práctica cuando:

!!! failure ""Es una mala práctica cuando:"
    * Se utiliza en exceso o en situaciones complejas, lo que puede hacer que el código sea más difícil de entender.
    * Se asignan valores a múltiples variables que no están relacionadas, lo que puede confundir a otros desarrolladores que intentan entender el código.

!!! important "¡Para recordar!"
En general, como con muchos aspectos en la programación, la clave está en el equilibrio. Utiliza la asignación múltiple cuando mejore la legibilidad y la comprensión del código, pero evítala cuando pueda causar confusión.
