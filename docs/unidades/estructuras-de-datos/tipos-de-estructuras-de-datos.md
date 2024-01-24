title: Tipos de estructuras de datos

## ¿Qué es una estructura de datos?

Las estructuras de datos son formas de organizar y almacenar datos en un programa de computadora para que puedan ser utilizados de manera eficiente. Algunos de los tipos más comunes de estructuras de datos incluyen:

* Cadenas de caracteres (Strings): Representan una secuencia de caracteres. En muchos lenguajes de programación se definen usando comillas simples (') o dobles (").

* Arreglos (Arrays): Una colección de elementos identificados por índices o claves. Todos los elementos son del mismo tipo.

* Listas: Similar a un arreglo, pero puede cambiar de tamaño y puede contener elementos de diferentes tipos.

* Tuplas: Similar a una lista, pero es inmutable, lo que significa que no puede cambiar una vez que se ha creado.

* Conjuntos (Sets): Una colección de elementos únicos, es decir, no permite duplicados.

* Diccionarios: Una colección de pares clave-valor. Las claves son únicas y los valores pueden ser de cualquier tipo.

* Pilas (Stacks): Una colección de elementos con dos operaciones principales: push (agregar un elemento al final) y pop (eliminar el último elemento).

* Colas (Queues): Similar a una pila, pero los elementos se agregan al final y se eliminan del principio.

* Árboles: Una estructura de datos no lineal que tiene un nodo raíz y un conjunto de nodos secundarios que forman un subárbol.

* Grafos: Una colección de nodos y aristas que conectan los nodos. Puede ser dirigido (las aristas tienen una dirección) o no dirigido.

Cada una de estas estructuras de datos tiene sus propias ventajas y desventajas, y se utilizan en diferentes situaciones dependiendo de las necesidades del programa.

## Listas

Una lista (_list_) es una colección de datos. Según el lenguaje de programación, esa lista estará conformada por los mismos o por diferentes tipos de datos.
	
```
lista_de_datos_de_diferente_tipo = [1, "Hola", True, 3.14]
lista_de_datos_de_igual_tipo = [10, -5, 0]
```

''' warning "¡Recuerda!"
    Es importante tener en cuenta que, aunque las listas pueden contener elementos de diferentes tipos de datos, esto puede hacer que sea más difícil de manejar y procesar. 
    
    En general, es mejor mantener los elementos de una lista del mismo tipo de datos siempre que sea posible para evitar confusiones y errores.

### Ejemplo

En este ejemplo, crearemos una lista llamada mi_lista que contiene los números del 1 al 5.  
Luego, accederemos a algunos elementos de la lista utilizando sus índices y modificaremos y agregaremos elementos.   
Finalmente, eliminaremos un elemento y obtendremos la longitud de la lista (número de elementos en ella).

``` py title="Python"
# creación de una lista
mi_lista = [1, 2, 3, 4, 5]

# acceso a elementos de la lista
primer_elemento = mi_lista[0]  # el primer elemento es 1
tercer_elemento = mi_lista[2]  # el tercer elemento es 3

# modificación de elementos de la lista
mi_lista[4] = 6  # cambiamos el último elemento de 5 a 6

# agregando elementos a la lista
mi_lista.append(7)  # agrega el número 7 al final de la lista

# eliminando elementos de la lista
mi_lista.remove(2)  # elimina el número 2 de la lista

# longitud de la lista
longitud = len(mi_lista)  # longitud de la lista es 4
```

## Pilas

!!! warning "Completar"

## Colas

!!! warning "Completar"

## Matrices

Una matríz (_matrix_) es una lista de listas. Cada lista interna representa una fila de la matriz. Cada elemento de cada lista representa una columna de la matriz.

### Ejemplo

En este ejemplo, matriz será una lista de tres elementos, cada uno de los cuales será a su vez una lista de tres elementos.  
Cada lista interna representará una fila de la matriz, y cada elemento de la lista interna representará una columna de la matriz.  

``` py title="Python"
# creación de una matriz de 3x3
matriz = [
            [1, 2, 3],
            [4, 5, 6],
            [7, 8, 9]
         ]

# devuelve el elemento en la fila 0, columna 1
print(matriz[0][1]) // salida: 2
```

!!! warning "Este ejemplo debiera ir luego de explicar ciclos"

Podreemos acceder a los elementos individuales de la matriz utilizando la sintaxis de índice.  
Así, `matriz[0][1]` devolverá el elemento en la fila 0 y la columna 1 de la matriz, que es el valor 2. 

Ahora, podremos recorrer la matriz utilizando bucles `for` anidados para acceder a cada elemento de la matriz.  

``` py title="Python"
matriz = [
            [1, 2, 3],
            [4, 5, 6],
            [7, 8, 9]
         ]

for fila in matriz:
    for columna as elemento in fila:
        print(columna, end=" ") # imprime el valor almacenado en cada columna (elemento)
    print() # imprime un salto de linea
```

``` title="Terminal (Entrada/Salida)"
1 2 3 
4 5 6 
7 8 9 
```

En este ejemplo, el programa itera sobre cada fila de la matriz, que a su vez itera sobre cada columna de cada fila e imprime el valor almacenado.     
Al finalizar la iteracón de cada fila, el programa imprime un salto de línea y vuelve a repetir la ejecución de iterarción en la siguiente fila.

!!! alert "Para tener en cuenta si trabajas con matrices en Python"
    En Python, la longitud de cada fila de la matriz no tiene por qué ser la misma.  
    Esto permite representar **matrices irregulares**, donde cada fila puede tener una longitud diferente.
    
    Sin embargo, **trabajar con matrices irregulares puede ser más complicado que trabajar con matrices regulares de tamaño fijo**.

## Tuplas

Una tupla (_tuple_) es similar a una lista, aunque sus elementos son inmutables. Es decir, no pueden ser modificados una vez que la tupla sea creada.

```
mi_tupla = (1, 2, 3, 4, 5)
```

### Ejemplos

Crearemos una tupla llamada mi_tupla que contendrá los números del 1 al 5.  
Luego, accederemos a algunos elementos de la tupla utilizando sus índices y obtendremos la longitud de la tupla.  

``` py title="Python" linenums="1" hl_lines="12"
# creación de una tupla
mi_tupla = (1, 2, 3, 4, 5)

# acceso a elementos de la tupla
primer_elemento = mi_tupla[0]  # el primer elemento es 1
tercer_elemento = mi_tupla[2]  # el tercer elemento es 3

# longitud de la tupla
longitud = len(mi_tupla)  # longitud de la tupla es 5

# la siguiente generará un error ya que las tuplas son inmutables
mi_tupla[4] = 6 # no se pueden modificar elementos de la tupla
```

Sin embargo, cuando intentamos modificar un elemento de la tupla, se produce un error ya que las tuplas son inmutables y no se pueden modificar sus elementos después de su creación.

``` title="Terminal (Entrada/Salida)"
Traceback (most recent call last):
  File "c:\ejemplo.py", line 12, in <module>
    mi_tupla[4] = 6
    ~~~~~~~~^^^
TypeError: 'tuple' object does not support item assignment
```

Otro ejemplo de gran aplicación práctica es el intercambio de valores almacenados en dos variables sin necesidad de una tercera variable temporal:

``` py title="Python"
a = 1
b = 2

print("El valor que tiene almacenado `a` es", a)
print("El valor que tiene almacenado `b` es", b)

print("Ahora se ejecuta la instrucción `a, b = b, a`")
a, b = b, a

print("El valor que tiene almacenado ahora `a` es", a)
print("El valor que tiene almacenado ahora `b` es", b)
```

En Python, `a, b = b, a` es una forma de intercambiar los valores de las variables `a` y `b`.

``` title="Terminal (Entrada/Salida)"
El valor que tiene almacenado `a` es 1
El valor que tiene almacenado `b` es 2

Ahora se ejecuta la instrucción `a, b = b, a`

El valor que tiene almacenado ahora `a` es 2
El valor que tiene almacenado ahora `b` es 1
```

Inicialmente, `a` es 1 y `b` es 2. Después de `a, b = b, a`, `a` será 2 y `b` será 1.

Esto es posible gracias a la capacidad de Python para empaquetar y desempaquetar tuplas.  

Python primero empaqueta los valores de `b` y `a` en una tupla (2, 1), para luego desempaquetar esa tupla almacenando los valores en `a` y `b` respectivamente.  

!!! success "¿Cómo funciona la cosa?"
    Respetando el orden de empaquetado y desempaquetado es como se produce el intercambio de valores.
    
    En realidad no es un intercambio si no una asignación de valores a las variables que previamente habían provisto dichos valores pero en orden de acceso inverso.

## Arreglos

Un arreglo (_array_) se puede utilizar para almacenar una secuencia de elementos del mismo tipo de datos.  
A diferencia de las listas, los arrays están diseñados para ser más eficientes en términos de espacio y tiempo de procesamiento para operaciones numéricas y matemáticas.

!!! info "Para tener en cuenta"
    En algunos lenguajes, los arreglos pueden contener elementos de diferentes tipos de datos.  
    Esto puede hacer que sea más difícil de manejar y procesar. 
    
    En general, es mejor mantener los elementos de un array del mismo tipo de datos siempre que sea posible para evitar confusiones y errores.

### Ejemplo

Crearemos un arreglo llamado mi_array que contendrá 3 números enteros (1, 2 y 3) como elementos.  
El primer argumento del método `array()` especificará el tipo de datos de los elementos del arreglo.

> Para utilizar arreglos en Python, primero debemos importar el módulo array. Si bien esta operación, en general se denomina importación de librería, en Python no existen las librerías y en su lugar existen los módulos.
> Luego, podremos crear un nuevo arreglo utilizando la función `array()` y pasando como argumentos el tipo de datos de los elementos y una secuencia de valores. 

``` py title="Python"
import array

mi_array = array.array('i', [1, 2, 3])

print(mi_array)  # salida: array('i', [1, 2, 3])
```

> 'i' significa que los elementos que almacenará el arreglo serán números enteros.

Ahora, Podemos acceder a los elementos del arreglo utilizando su índice, de la misma manera que lo hacíamos con las listas:

``` py title="Python"
print(mi_array[0])  # salida: 1
print(mi_array[1])  # salida: 2
print(mi_array[2])  # salida: 3
```

También podemos modificar los elementos del arreglo asignando nuevos valores a sus índices:

``` py title="Python"
mi_array = array.array('i', [1, 2, 3]) 
mi_array[1] = 4
print(mi_array)  # salida: array('i', [1, 4, 3]) 
```

En este ejemplo, estamos modificando el segundo elemento del arreglo (mi_array[1]) y asignándole un nuevo valor (4). 
El array resultante se imprimirá en la consola como 
array('i', [1, 4, 3]).

Es importante tener en cuenta que los arreglos en algunos lenguajes, como Python, están limitados a un solo tipo de datos, lo que significa que no podemos mezclar diferentes tipos de datos en un solo arreglo.

Además, los arreglos en Python son estáticos, lo que significa que no pueden cambiar de tamaño una vez que se han creado. 

Si necesitamos un tipo de datos que pueda cambiar de tamaño, podemos utilizar una lista en su lugar.

## Diccionarios

Un diccionario (_dict_) es una colección de pares clave-valor, en la que cada valor se almacena junto con una clave que lo identifica. 

También se los conoce como mapas.

!!! warning "Buscar mapas y chequear info"

```
mi_diccionario = {"nombre": "Juan", "edad": 30, "ciudad": "Bs As"}
```

### Ejemplo

Crearemos un diccionario llamado mi_diccionario que contiene información sobre una persona.  
Luego, accederemos a algunos elementos del diccionario utilizando sus claves y modificaremos y agregaremos elementos.  
Finalmente, eliminaremos una clave y su valor del diccionario y obtendremos la longitud del diccionario.

``` py title="Python"
# creación de un diccionario
mi_diccionario = {"nombre": "Juan", "edad": 30, "ciudad": "Bs As"}

# acceso a elementos del diccionario
nombre = mi_diccionario["nombre"]  # el valor de "nombre" es "Juan”
edad = mi_diccionario["edad"]  # el valor de "edad" es 30

# modificación de elementos del diccionario
mi_diccionario["edad"] = 31  # cambiamos el valor de "edad" a 31

# agrega un nuevo par clave-valor (elemento) al diccionario
mi_diccionario["trabajo"] = "programador"

# elimina la clave "ciudad" y su valor (elemento) del diccionario
del mi_diccionario["ciudad"]

# longitud del diccionario
longitud = len(mi_diccionario)  # longitud del diccionario es 3
```

## Conjuntos

Un conjunto (_set_) es una colección de valores únicos. Es decir que no hay elementos duplicados en un conjunto.

``` py
mi_set = {1, 2, 3, 3, 4, 5, 5} # creación de un set con elementos duplicados
print(mi_set) # imprime {1, 2, 3, 4, 5} eliminando los duplicados
```

### Ejemplo

Crearemos un conjunto llamado mi_set y le asignaremos los siguientes valores: 1, 2, 3, 3, 4, 5, 5

!!! success "¡Importante!"
    Hay que tener en cuenta que los conjuntos son colecciones no ordenadas y no permiten elementos duplicados.  
    En caso de asignarle elementos duplicados, estos serán eliminados automáticamente.

Luego, agregaremos un nuevo elemento al conjunto y eliminaremos otro.  
También comprobaremos si un valor determinado está en el conjunto utilizando el operador `in`.   
Finalmente, obtendremos la longitud del conjunto. 

``` py title="Python"
# creación de un conjunto con elementos duplicados
mi_set = {1, 2, 3, 3, 4, 5, 5}

# imprimiendo el conjunto
print(mi_set)  # salida: {1, 2, 3, 4, 5}

# agregando elementos al conjunto
mi_set.add(6)  # agrega el número 6 al conjunto

# comprobando si un elemento está en el conjunto
esta_en_conjunto = 4 in mi_set # devuelve True ya que 4 está en el conjunto

# eliminando elementos del conjunto
mi_set.remove(3)  # elimina el número 3 del conjunto

# longitud del conjunto
longitud = len(mi_set)  # longitud del conjunto es 5
```

### Árboles

!!! warning "Falta"

## Funciones

!!! warning "Dejamos esto aca?"

En algunos lenguajes, las funciones son consideradas como un tipo de dato y pueden ser asignadas a variables de la misma manera que asignamos otros tipos de datos, como una cadena o un número entero. Para hacerlo, simplemente escribimos el nombre de la variable, seguido del signo igual (=) y el nombre de la función sin paréntesis.

### Ejemplo

``` py title="Python"
def sumar(a, b):  // la función sumar toma dos números como argumentos y devuelve la suma de esos números
    resultado = a + b
    return resultado

mi_funcion = sumar
resultado = mi_funcion(2, 3)

print(resultado)  # salida: 5
```

Aquí se define una función llamada sumar que luego es asignada a la variable mi_funcion. Más tarde, se llama a la función a través de la variable, pasando los dos argumentos necesarios para realizar la operación de suma dentro de la función; y esta devuelve el resultado que es finalmente almacenado en la variable resultado que luego es impresa por pantalla.

!!! success "¡Importante!"
    Hay que tener en cuenta que, cuando asignamos una función a una variable, estamos asignando la función en sí misma, no el resultado de la función.  
    Esto significa que podemos llamar a la función en cualquier momento simplemente utilizando la variable a la que se ha asignado, con argumentos diferentes, si es preciso, para obtener diferentes resultados.

## Objeto como instancia de una clase

!!! warning "Dejamos esto aca?"

Una clase es un tipo de datos personalizado que define un conjunto de atributos y métodos
que se pueden utilizar para crear objetos.

Por ejemplo, podemos definir una clase Persona que tenga atributos como nombre, edad y ocupación, y métodos como caminar(), correr() y hablar().

### Ejemplo

Definiremos la clase Persona con un constructor que toma tres parámetros (nombre, edad y ocupacion) y dos métodos (\__init__\() y hablar()).   
Luego, crearemos el objeto persona1 de la clase Persona y le pasaremos algunos valores para los atributos nombre, edad y ocupacion.   
Finalmente, llamaremos al método hablar() en el objeto persona1.

!!! success "¡ Muy importante!"
    Hay que tener en cuenta que en Python, todo es un objeto, incluso los tipos de datos básicos como enteros, flotantes y cadenas. Por lo tanto, podemos tratarlos como objetos y llamar a sus métodos y atributos.


## Objeto como variable

Como bien dijimos, en algunos lenguajes como Python todo es un objeto, incluso las variables.

Ya que una variable es simplemente una referencia a un objeto, cuando creamos una variable y le asignamos un valor, lo que realmente estamos haciendo es crear un objeto y asignar una referencia a ese objeto a la variable. 

``` py title="Python"
# creación de un objeto entero y asignación a una variable
mi_variable = 42

# creación de una lista y asignación a una variable
mi_otra_variable = [1, 2, 3]
```

En el ejemplo anterior, creamos dos objetos: 
    * un objeto entero con un valor de 42; y 
    * una lista con tres elementos. 
   
Luego, asignamos referencias a esos objetos a dos variables diferentes: mi_variable y mi_otra_variable, respectivamente.

!!! success "¡Importante!"
Es importante tener en cuenta que, en Python, las variables no tienen un tipo de datos asociado, sino que los objetos a los que hacen referencia sí lo tienen. Por lo tanto, una variable puede referenciar a un objeto de cualquier tipo de datos en cualquier momento, incluso si anteriormente se referenciaba a un objeto de otro tipo de datos.

