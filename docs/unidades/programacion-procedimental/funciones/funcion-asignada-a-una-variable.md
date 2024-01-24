title: Función asignada a una variable

## Introducción

!!! warning "Chequear esta info"

Las funciones son consideradas como un tipo de dato y pueden ser asignadas a variables de la misma manera que asignamos otros tipos de datos, como una cadena o un número entero. Para hacerlo, simplemente escribimos el nombre de la variable, seguido del signo igual (=) y el nombre de la función sin paréntesis.

!!! info "Definición"
    Una función es un tipo de dato que representa un bloque de sentencias (o sentencia compuesta) reutilizable y autónomo que realiza una tarea específica. En términos más generales, una función es una secuencia de instrucciones que toma uno o más argumentos, realiza un conjunto de operaciones y devuelve un resultado.

Toda función debe contener al menos una sentencia compuesta.

La función puede tener instrucciones que realicen cálculos, operaciones, manipulación de datos, llamadas a otras funciones, entre otras acciones.

Una función se define utilizando la palabra clave def, seguida del nombre de la función, paréntesis que pueden contener los argumentos de la función y dos puntos ":". A continuación, se escribe el bloque de código que conforma la función, indentado con espacios o tabulaciones.

``` py title="Python
# Definición de funciones
def sumar(a, b):
    resultado = a + b
    return resultado
```

Veamos ejemplo de definición de una función en Python llamada sumar que toma dos números como argumentos y devuelve la suma de esos números:

``` py title="Python"
# Definición de funciones
def sumar(a, b):
    resultado = a + b
    return resultado
```

Aquí se define una función llamada _sumar_ que toma dos argumentos, _a_ y _b_. La función realiza la suma de los dos argumentos y los almacena una la variable _resultado_. Luego, devuelve el valor almacenado en la variable _resultado_.  
Podemos asignar esta función a una variable y luego llamarla utilizando esa variable:

``` py title="Python"
# Definición de funciones
def sumar(a, b):
    resultado = a + b
    return resultado

# Bloque principal del programa
mi_funcion = sumar
resultado = mi_funcion(2, 3)
print(resultado)
```

``` title="Terminal (Entrada/Salida)"
5
```

> En el ejemplo anterior, asignamos la función _sumar_ a una variable llamada _mi_funcion_. Luego, llamamos a la función utilizando la variable y pasando los argumentos _2_ y _3_.  
> La función devuelve la suma de los dos números, que se almacena en la variable _resultado_.
> Luego, se imprime el valor almacenado en la consola.

!!! alert "¡Importante!"
    Cuando asignamos una función a una variable, estamos asignando la función en sí misma, no el resultado de la función. Esto significa que podemos llamar a la función en cualquier momento simplemente utilizando la variable a la que se ha asignado.

Las funciones también se pueden pasar como argumentos a otras funciones. Por ejemplo, podemos definir una función llamada _aplicar_funcion_ que toma una función y dos argumentos y devuelve el resultado de aplicar la función a los dos argumentos:

``` py title="Python
# Definición de funciones
def aplicar_funcion(funcion, a, b):
    return funcion(a, b)

# Bloque principal del programa
resultado = aplicar_funcion(sumar, 2, 3)
print(resultado)
```

``` title="Terminal (Entrada/Salida)"
5
```

> En el ejemplo anterior, pasamos la función _sumar_ como argumento a la función _aplicar_funcion_. La función _aplicar_funcion_ llama a la función pasada como argumento (_sumar_) con los dos argumentos (_2_ y _3_) y devuelve el resultado de la función (5).

!!! Success "¡Para tener en cuenta!"
    En resumen, en lenguajes como Python, las funciones son objetos de primera clase, lo que significa que se pueden tratar como cualquier otro tipo de dato, como números, cadenas o listas.  
    Esto permite que las funciones se asignen a variables, se pasen como argumentos a otras funciones, se devuelvan como resultados de funciones y se almacenen en estructuras de datos como listas o diccionarios.

