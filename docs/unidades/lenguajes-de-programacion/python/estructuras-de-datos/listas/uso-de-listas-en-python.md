title: Listas en Python

Una lista en Python es una estructura de datos que puede contener múltiples elementos, que pueden ser de diferentes tipos (por ejemplo, números enteros, flotantes, cadenas, etc.), aunque esto último es poco frecuente.  Por lo general, todos los elementos de una lista son del mismo tipo o estructura de datos.

``` py title="Python"
mi_lista = [1, 2, "tres", 4.0]
```

> En este ejemplo, `mi_lista` es una lista que contiene cuatro elementos: dos números enteros, una cadena y un número flotante.

Los elementos en una lista están ordenados en secuencia y tienen un índice definido, que comienza desde 0 para el primer elemento.

Las listas son mutables, lo que significa que puedes cambiar sus elementos después de que la lista ha sido creada. Puedes agregar, eliminar y modificar elementos en una lista en cualquier momento de la ejecución del programa.

## Declaración de una lista

Las listas se crean asignando a una variable una secuencia de elementos encerrados entre corchetes ( [] )y separados por comas. 

Se puede crear una lista vacía, y las listas pueden ser elementos de otras listas. Para incluir una lista como parte de otra, basta con incluirla separada por comas de los elementos restantes.

Aquí tienes varios ejemplos de cómo se ve una lista en Python:

``` py title="Python"
numeros = [1,2,3,4,5] # Lista de números
dias = ["Lunes", "Martes", "Miércoles", "Jueves", "Viernes", "Sábado", "Domingo"] # Lista de cadenas de caracteres
elementos = [] # Lista vacía
matriz = [ [1,2,3], [4,5,6] ] # lista de listas (también llamada matriz)
```

!!! info "Para tener en cuenta"
    Las listas se suelen nombrar en plural. 


## Acceso a los elementos de una lista

En Python, puedes acceder a los elementos de una lista utilizando su índice, que es la posición del elemento en la lista. Los índices en Python comienzan en 0, por lo que el primer elemento de la lista está en el índice 0, el segundo elemento está en el índice 1, y así sucesivamente.

Aquí tienes varios ejemplos:

``` py title="Python"
# Definir la lista
mi_lista = [1, 2, "tres", 4.0]

# Acceder al primer elemento
print(mi_lista[0])  # Output: 1

# Acceder al segundo elemento
print(mi_lista[1])  # Output: 2

# Acceder al último elemento
print(mi_lista[-1])  # Output: 4.0
```

> En este código, `mi_lista[0]` accede al primer elemento de mi_lista, `mi_lista[1]` accede al segundo elemento, y `mi_lista[-1]` accede al último elemento.  
> Los índices negativos cuentan desde el final de la lista, por lo que -1 es el último elemento, -2 es el penúltimo elemento, y así sucesivamente.

!!! warning "¡Muy importante!"
    Intentar acceder a un elemento con un índice fuera de rango generará un error: 

    ``` py title="Python" linenums="1" hl_lines="6"
    # Definir la lista
    mi_lista = [1, 2, "tres", 4.0]

    # La lista solo tiene índices 0 al 3 (4 elementos)
    # Acceder a un elemento con índice fuera de rango
    print(mi_lista[4])
    ```

    ``` title="Terminal (Entrada/Salida)"
    Traceback (most recent call last):
    File "…", line 6, in <module>
        print(mi_lista[4])
            ~~~~~~~~^^^
    IndexError: list index out of range
    ```

## Impresión de listas

La impresión de listas en Python se refiere a mostrar en la consola o terminal los elementos de la lista.  Para imprimir una lista, puedes usar la función `print()`.

Aquí tienes un ejemplo:

``` py title="Python"
mi_lista = [1, 2, "tres", 4.0]
print(mi_lista)
```

``` title="Terminal (Entrada/Salida)"
[1, 2, 'tres', 4.0]
```

En este código, `print(mi_lista)` imprime la representación de la lista `mi_lista`, que incluye los corchetes que delimitan la lista y las comas que separan los elementos.

## Longitud de una lista

La función `len()` devuelve la cantidad de elementos en un objeto iterable, en este caso, una lista. 

Por lo tanto, `len(lista)` devolverá el número de elementos en la lista `lista`.

Aquí tienes un ejemplo:

``` py title="Python"
mi_lista = [1, 2, 3, 4, 5]
print(len(mi_lista))  # Output: 5
```

> En este código, `len(mi_lista)` devuelve 5, porque hay cinco elementos en la lista `mi_lista`.

## Iterar sobre una lista

Una de las tareas más comunes que se realizan con listas es recorrer su contenido con el objetivo de conocer como está compuesta:

### Impresión de los elementos de una lista

Si quieres imprimir los elementos de una lista, uno por uno, puedes hacerlo de diferentes maneras:

1. Emplear un bucle _for … in_ para acceder a cada elemento:

    La estructura _for … in_ permite acceder a cada uno de los elementos de una lista y almacenar una copia en la variable de control:

    ``` py title="Python"
    mi_lista = [1, 2, "tres", 4.0]

    for elemento in mi_lista:
        print(elemento)
    ```

    Este código imprimirá cada elemento de la lista en una línea separada:

    ``` title="Terminal (Entrada/Salida)"
    1
    2
    tres
    4.0
    ```

1. Emplear un bucle _for … in range_ o un bucle _while_ para generar la secuencia de índices para acceder a cada elemento:

    Emplear un bucle tradicional no permite acceder directamente al elemento de la lista pero si permite generar una secuencia de índices par luego referencia cada posición de la lista para acceder al elemento almacenado en ella:

    ``` py title="Python"
    lista = [1, 2, "tres", 4.0]

    for i in range(len(lista)):
        print(lista[i])
    ```

    ``` title="Terminal (Entrada/Salida)"
    1
    2
    tres
    4.0
    ```

    ``` py title="Python"
    lista = [1, 2, "tres", 4.0]

    i = 0
    while i < len(lista):
        print(lista[i])
        i = i + 1
    ```

    ``` title="Terminal (Entrada/Salida)"
    1
    2
    tres
    4.0
    ```

## Desempaquetado de listas

El desempaquetado de listas, también conocido como _unpacking_, es un proceso que permite asignar los valores de una lista a variables individuales. 

!!! info "Esto se hace utilizando la asignación múltiple."

Aquí tienes un ejemplo:

``` py title="Python"
numeros = [1, 2, 3]
a, b, c = numeros

print(a)  # Output: 1
print(b)  # Output: 2
print(c)  # Output: 3
```

En este código, `a, b, c = numeros` desempaqueta la lista `numeros` en las variables `a`, `b` y `c`. La variable `a` recibe el primer valor de la lista, `b` el segundo y `c` el tercero.

!!! warning "¡Muy importante!"
    Hay que tener en cuenta que el número de variables debe coincidir con el número de elementos en la lista. Si no coinciden, Python lanzará un error.

## Uso de operadores con cadenas de caracteres

### Concatenación de listas

La concatenación de listas en Python es el proceso de unir o combinar dos o más listas. Esto se puede hacer utilizando el operador de concatenación ( + ).

Aquí tienes un ejemplo:

``` py title="Python"
lista1 = [1, 2, 3]
lista2 = [4, 5, 6]
lista_concatenada = lista1 + lista2

print(lista_concatenada)  # Output: [1, 2, 3, 4, 5, 6]
```

En este código, `lista1 + lista2` concatena `lista1` y `lista2` para formar una nueva lista que contiene todos los elementos de `lista1` seguidos de todos los elementos de `lista2`.

### Comprobar si un elemento se encuentra, o no, dentro de una lista

Los operadores **in** y **not in** también se pueden usar con listas en Python para verificar si un elemento está o no en la lista. Aquí hay un ejemplo:

* **in**: devuelve True si un elemento se encuentra en la lista y False de lo contrario.
  
* **not in**: devuelve True si un elemento no se encuentra en la lista y False de lo contrario.

```py title="Python"
lista = ["manzana", "banana", "cereza"]

print("manzana" in lista)  # Output: True
print("naranja" in lista)  # Output: False

print("manzana" not in lista)  # Output: False
print("naranja" not in lista)  # Output: True
```

> En este código, `"manzana" in lista` devuelve `True` porque "manzana" es un elemento de la lista. Por otro lado, `"naranja" in lista` devuelve `False` porque "naranja" no es un elemento de la lista.

> De manera similar, `"manzana" not in lista` devuelve `False` porque "manzana" es un elemento de la lista, y `"naranja" not in lista` devuelve `True` porque "naranja" no es un elemento de la lista.

Más adelante veremos que podremos realizar estas comparaciones directamente mediante el uso de métodos.

''' info "¡Recuerda que estos operadores también funcionan con otras estructuras de datos!"

## Uso de funciones con listas

* **list([iterable])**: Es un _constructor_ de listas. Se utiliza para crear una lista a partir de un iterable (como una cadena, tupla, conjunto, etc.) o para crear una lista vacía si no se proporciona el parámetro _iterable_.

Aquí está la sintaxis básica:

``` py title="Python"
list([iterable])
```

> Donde iterable es opcional. Si se proporciona, list() crea una lista donde cada elemento es un elemento del iterable. Si no se proporciona iterable, list() crea una lista vacía.

Aquí tienes algunos ejemplos de cómo usar list():

``` py title="Python"
# Crear una lista vacía
lista_vacia = list()
print(lista_vacia)  # Output: []

# Crear una lista a partir de una cadena
lista_cadena = list("Hola")
print(lista_cadena)  # Output: ['H', 'o', 'l', 'a']

# Crear una lista a partir de una tupla
lista_tupla = list((1, 2, 3))
print(lista_tupla)  # Output: [1, 2, 3]

# Crear una lista a partir de un conjunto
lista_conjunto = list({1, 2, 3})
print(lista_conjunto)  # Output: [1, 2, 3]
```

> Recuerda que una cadena de caracteres es una estructura de datos que alberga uno o mas elementos, en este caso, caracteres.

> Aún no hemos visto en profundidad que son tuplas y conjuntos pero, por el momento y para clarificar los ejemplos, una tupla es una colección de objetos que son ordenados e inmutables. Esto significa que una vez que una tupla es creada, no puedes cambiar sus elementos o su tamaño. Por lo tanto, si precisaras modificarla por algún motivo, es necesario convertirla en una lista, aplicar las modificaciones, y luego volver a convertirla en una tupla. Un conjunto es una colección de elementos que no están ordenados y no tienen índices y tampoco permiten elementos duplicados. Esto significa que si es preciso trabajar con índices, ordenamiento o duplicar elementos es necesario convertirlo en una lista, realizar las tareas correspondientes, y luego volver a convertirlo en un conjunto.

!!! warning "¡Para recordar!"
    `list()` crea una **nueva lista**. Si el iterable es mutable (como una lista o un conjunto), los cambios en el iterable utilizado para crear la lista no afectarán a la lista creada, y viceversa.

* **range([inicio,] fin[, paso])**: Se utiliza para generar una secuencia de números.  
Aunque no se utiliza directamente con listas, se puede utilizar para generar listas de números si se combina con la función _list()_.  

Donde:

    * **inicio**: Opcional. Un número entero que especifica en qué posición empezar. El valor predeterminado es 0.

    * **fin**: Requerido. Un número entero que especifica en qué posición parar.

    * **paso**: Opcional. Un número entero que especifica el incremento. El valor predeterminado es 1. Dependiendo del valor de inicio y de fin, _paso_ debe ser positivo o negativo.

    Aquí hay algunos ejemplos de cómo usar range() para generar listas:

    ``` py title="Python"
    # Generar una lista de números del 0 al 9
    lista1 = list(range(10))
    print(lista1)  # Output: [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]

    # Generar una lista de números del 5 al 9
    lista2 = list(range(5, 10))
    print(lista2)  # Output: [5, 6, 7, 8, 9]

    # Generar una lista de números del 0 al 9, pero con pasos de 2
    lista3 = list(range(0, 10, 2))
    print(lista3)  # Output: [0, 2, 4, 6, 8]
    ```

    También puedes usar _range()_ con listas existentes para iterar sobre ellas, como hemos visto previamente:

    ``` py title="Python"
    lista = ['a', 'b', 'c', 'd', 'e']

    # Imprimir cada elemento de la lista usando range()
    for i in range(len(lista)):
        print(lista[i])
    ```

    > En este código, `range(len(lista))` genera una lista de números del 0 al 4, que son los índices de los elementos en `lista`. Luego, en cada iteración del bucle `for`, se utiliza el número generado por `range()` como índice para acceder a cada elemento de lista.

* **sum(iterable[, inicio])**: Se utiliza para sumar todos los elementos de una lista. 

Donde:

  * **iterable**: es una secuencia (como una lista, tupla, etc.) o una colección (como un conjunto, diccionario, etc.) de números (enteros y flotantes).  

  * **inicio**: es un número opcional que se suma al resultado de sumar los elementos del iterable. Si se omite start, la suma comienza desde cero.

Aquí tienes un ejemplo:

``` py title="Python"
lista = [1, 2, 3, 4, 5]
suma = sum(lista)
print(suma)  # Output: 15

suma_con_inicio = sum(lista, 10)
print(suma_con_inicio)  # Output: 25
```

> En este código, `sum(lista)` suma todos los elementos de lista, y sum`(lista, 10)` suma todos los elementos de lista y luego añade 10 al resultado.

!!! warning "¡Importante!"
    Es importante mencionar que `sum()` sólo puede sumar elementos que sean números. Si intentas usar `sum()` en una lista que contiene elementos que no son números, Python lanzará un error.

* **min(iterable, *[, clave, valor_defecto])**,
* **max(iterable, *[, clave, valor_defecto])**: Se utilizan para obtener el valor mínimo y máximo de un iterable, una lista en este caso.

    * **clave** (opcional): Una función para servir como clave o criterio de ordenación. La función `min()` o `max()` aplicará esta función a cada elemento del iterable y devolverá el elemento para el cual la función key devuelve el valor mínimo o máximo.

    * **valor_defecto** (opcional): Un valor por defecto que se devuelve si el iterable está vacío.

``` py title="Python"
lista = [1, 2, 3, 4, 5]

# Obtener el valor mínimo de una lista
minimo = min(lista)
print(minimo)  # Output: 1

# Obtener el valor máximo de una lista
maximo = max(lista)
print(maximo)  # Output: 5 
```

> En este código, `min(lista)` y `max(lista)` devuelven el valor mínimo y máximo de `lista`, respectivamente. 

Por el momento utilizaremos ambas funciones sin aplicar los parámetros opcionales.

## Uso de métodos de listas

Los métodos de las listas en Python son funciones incorporadas que se pueden usar para realizar diferentes operaciones en las listas. 

Algunos de los métodos más comunes que poseen las listas en Python incluyen los que veremos a continuación. Para ello, primero crearemos una lista:

``` py title="Python"
lista = [1, 2, 3, 4, 5]
```

Y ahora efectuaremos una serie de procesos para ir describiendo los diferentes funcionamientos. Recuerda ir siguiendo lo que ocurre con la lista, ejecución tras ejecución.

* **append(elemento)**: Agrega un elemento al final de la lista.

    ``` py title="Python"
    lista.append(6)
    print(lista)  # Output: [1, 2, 3, 4, 5, 6]
    ```

    !!! info "Para tener en cuenta"
        El método _append(elemento)_ equivale a sumar una lista con el elemento para agregar a continuación de la lista que recibirá el elemento:

        ``` py title="Python"
        lista = [1, 2, 3, 4, 5]
        lista = lista + [6]
        print(lista)  # Output: [1, 2, 3, 4, 5, 6]
        ```

* **extend()**: Agrega todos los elementos de una lista a otra lista.

    ``` py title="Python"
    lista.extend([7, 8, 9])
    print(lista)  # Output: [1, 2, 3, 4, 5, 6, 7, 8, 9]
    ```

    > La ejecución de este método equivale a concatenar dos listas.

* **insert(posicion, elemento)**: Inserta un elemento en una posición específica de la lista.

    Los parámetros son:

    * **posicion**: Es el índice donde se insertará el nuevo elemento. Los índices en Python comienzan en 0, por lo que si quieres insertar un elemento al inicio de la lista, la posición sería 0.

    * **elemento**: Es el valor que se insertará en la lista.

    ``` py title="Python"
    lista.insert(0, 0)
    print(lista)  # Output: [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
    ```

* **remove(valor)**: Elimina la primera aparición de un elemento en la lista.

    ``` py title="Python"
    lista.remove(0)
    print(lista)  # Output: [1, 2, 3, 4, 5, 6, 7, 8, 9]
    ```

* **pop()**: Elimina y devuelve el elemento en una posición dada. Si no se proporciona ninguna posición, elimina y devuelve el último elemento de la lista.

``` py title="Python"
elemento = lista.pop(0)
print(elemento)  # Output: 1
print(lista)  # Output: [2, 3, 4, 5, 6, 7, 8, 9]
```

* **index(valor[, inicio[, fin]])**: Devuelve el índice del primer elemento que coincide con el valor especificado.

    Donde:

    * **inicio** (opcional): Es el índice inicial desde donde se debe comenzar la búsqueda.
    * **fin** (opcional): Es el índice final donde se debe detener la búsqueda.

    ``` py title="Python"
    lista = [1, 2, 3, 4, 5, 4, 4]

    indice = lista.index(5)
    print(indice)  # Output: 4

    indice = lista.index(4)
    print(indice)  # Output: 3

    indice = lista.index(4, 4, 7)
    print(indice)  # Output: 5
    ```

    !!! warning "¡Para tener en cuenta!"
        Si el valor no se encuentra en la lista, se lanza una excepción `ValueError`.

        ``` py title="Python"
        lista = [1, 2, 3, 4, 5, 4, 4]

        indice = lista.index(4, 2, 3)
        print(indice)  # Output: ValueError: 4 is not in list
        ```

* **count(valor)**: Devuelve el número de veces que un valor específico aparece en la lista.

    ``` py title="Python"
    conteo = lista.count(5)
    print(conteo)  # Output: 1
    ```

* **sort([reverse=False])**: Ordena los elementos de la lista en un orden específico: ascendente o descendente.  
Tiene un parámetro opcional _reverse_, que por defecto es False. Si no se especifica, la lista se ordenará en orden ascendente. Si el parámetro _reverse_ se establece en True, entonces la lista se ordenará en orden descendente.

    ``` py title="Python"
    lista.sort()
    print(lista)  # Output: [2, 3, 4, 5, 6, 7, 8, 9]
    
    lista.sort(reverse=True)
    print(lista)  # Output: [9, 8, 7, 6, 5, 4, 3, 2]
    ```

* **reverse()**: Invierte el orden de los elementos de la lista.

    ``` py title="Python"
    lista.reverse()
    print(lista)  # Output: [2, 3, 4, 5, 6, 7, 8, 9]
    ```

    > La ejecución de este método equivale a ejecutar el método _sort(reverse=True)_

* **clear()**: Se utiliza para eliminar todos los elementos de la lista. Después de usar este método, la lista se convierte en una lista vacía.

    ``` py title="Python"
    lista.clear()
    print(lista)  # Output: []
    ```

Estos métodos proporcionan una forma conveniente de manipular y trabajar con listas en Python.

!!! warning "¡Para recordar!"
    Cada uno de estos métodos modifica la lista original y no devuelve una nueva lista, **excepto el método _pop()_**, que devuelve el elemento eliminado.
