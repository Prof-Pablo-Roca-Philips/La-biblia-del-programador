title: Cadenas de caracteres en Python

Python, al igual que la mayoría de los lenguajes de programación actuales, provee un tipo de dato específico para tratar las cadenas de caracteres (strings).

Se trata de un tipo de dato con longitud variable, ya que deben adecuarse a la cantidad de caracteres que albergue la cadena.

Este tipo de dato posee una buena cantidad de métodos y propiedades que facilita su uso.

El siguiente código demuestra como es posible almacenar una cadena de caracteres en una variable. Este procedimiento se denomina **inicialización** cuando se crea la variable por primera vez en el programa y se la almacena un primer valor; o **asignación** cuando la variable ya existe en el programa y se le almacena un nuevo valor.

``` py title="Python - Inicialización de variables de cadena de caracteres"
# Definición de cadenas de caracteres usando comillas dobles
dia1 = "Lunes"
vacio = ""

# Definición de cadenas de caracteres usando comillas simples
dia2 = 'Martes'
numero_que_no_es_numero = "121"
```

> `vacio` es una cadena de caracteres de longitud cero.  
> `numero_que_no_es_numero` contiene números, pero es una cadena de caracteres porque estos números están entre comillas.

## Ingreso de cadenas vacías

En Python, cuando el usuario presiona solo ENTER en respuesta a la función `input()`, se devuelve una cadena vacía.  
Por lo tanto, puedes verificar si el usuario presionó solo ENTER comprobando si dato es una cadena vacía: 

``` py title="Python"
valor_ingresado = input("Ingrese algo por teclado (o solo ENTER para ingresar una cadena vacía): ")

if valor_ingresado == '':
    print("Has ingresado una cadena vacía.")
else:
    print("Has ingresado", valor_ingresado)
```

``` title="Terminal (Entrada/Salida)"
Ingrese algo por teclado (o solo ENTER para ingresar una cadena vacía): Pablo 
Has ingresado Pablo

Ingrese algo por teclado (o solo ENTER para ingresar una cadena vacía): 
Has ingresado una cadena vacía.
```

## Uso de triple comillas en cadenas de más de una línea

El uso de triple comillas para crear una cadena de caracteres provee un método sencillo para usar más de una línea de código para definir su contenido:

``` py title="Python"
# Definición de cadenas usando comillas dobles triples:
cadena1 = """En Python es posible 
definir cadenas de caracteres 
utilizando más de una línea de código"""

# Definición de cadenas usando comillas simples triples:
cadena2 = '''Por supuesto, se puede hacer lo mismo 
utilizando comillas simples'''

print(cadena1)
print(cadena2)
```

``` title="Terminal (Entrada/Salida)"
En Python es posible
definir cadenas de caracteres 
utilizando más de una línea de código

Por supuesto, se puede hacer lo mismo 
utilizando comillas simples
```

## Iterar sobre una cadena de caracteres

Como hemos visto anteriormente, `for` es una estructura de control que permite repetir un bloque de código un número determinado de veces. 

En Python, puedes usar un bucle for para iterar sobre cada carácter en una cadena. Aquí tienes un ejemplo:

``` py title="Python"
cadena = "Hola Mundo"

for caracter in cadena:
    print(caracter)
```

``` title="Terminal (Entrada/Salida)"
H
o
l
a

M
u
n
d
o
```

> En este código, `for caracter in cadena:` inicia un bucle que itera sobre cada carácter en cadena.  
> En cada iteración del bucle, `caracter` es una cadena de un solo carácter de `cadena`, y `print(caracter)` imprime este carácter.  

> Por lo tanto, este código imprime cada carácter en `cadena` en una línea separada.

Otro ejemplo podría ser enumerar cada caracter como se ve en la salida:

``` title="Terminal (Entrada/Salida)"
1°: H  /  2°: o  /  3°: l  /  4°: a  /  5°:    /  6°: M  /  7°: u  /  8°: n  /  9°: d  /  10°: o
```

Esto requiere que el programa sea más complejo para lograr el resultado propuesto.

``` py title="Python"
cadena = "Hola Mundo"

# Se utiliza para controlar como debe comportarse *print*
# en cada iteración del ciclo
pos = 1

# Se utiliza para modificar el comportamiento del parámetro *end* 
# de *print* durante la ejecución del ciclo
char_end = "  /  "

for caracter in cadena:
    
    # Modifica el comportamiento del parámetro *end* 
    # si es la última iteración del ciclo
    if pos == len(cadena):
        char_end = "\n"
        
    print(pos, "°: ", caracter, sep="", end = char_end)
    pos = pos + 1
```

!!! question "Para pensar"
    Analiza el último código para entender como es el funcionamiento.

## Acceso a cada caracter de una cadena de caracteres

Para entenderlo de manera muy simple, una cadena de caracteres es como una fila ordenada de caracteres donde cada caracter se ubica en una posición única, uno a continuación de otro, y cuyo primer valor posicional es el cero [0].

**Esta posición se denomina índice (_index_)**. 

También se lo suele llamar subíndice aunque este nombre no es correcto y no debe ser adoptado para identificar posiciones.

Asi, en Python se puede acceder a uno o a un conjunto de caracteres dentro de una cadena de caracteres simplemente con llamar el nombre de la variable de la cadena de caracteres seguido del índice de referencia:

``` py title="Python"
cadena = "Hola Mundo!"

print(cadena[0])
print(cadena[5])
```

``` title="Terminal (Entrada/Salida)"
H # Es el primer caracter de la cadena, identificado con el índice 0
M # Es el sexto caracter de la cadena, identificado con el índice 5
```

Cuando el índice es negativo, las posiciones se identifican de atrás para adelante, siendo -1 el índice del último caracter, siendo -2 el índice del ante último caracter y así sucesivamente.

!!! important "¡Para recordar!"
    Cuando utilizas índices negativos, la primera posición no es 0, es -1

``` py title="Python"
cadena = "Hola Mundo!"

print(cadena[-1])
print(cadena[-2])
```

``` title="Terminal (Entrada/Salida)"
! # Es el primer caracter de la cadena de atrás para adelante, identificado con el índice -1
o # Es el segundo caracter de la cadena de atrás para adelante, identificado con el índice -2
```

## Rebanadas (_Slicing_)

Las rebanadas o _slicing_ en Python se utilizan para extraer una parte de la cadena de caracteres (un intervalo de posiciones de la cadena de caracteres). 

Aquí tienes un ejemplo básico:

``` py title="Python"
# Crear una cadena
mi_cadena = "Hola Mundo"

# Obtener los caracteres del índice 5 al índice 9 (el 10 se excluye)
sub_cadena = mi_cadena[5:10]

print(sub_cadena)
```

``` title="Terminal (Entrada/Salida)"
Mundo
```

> En este código, `mi_cadena[5:10]` crea una nueva cadena que contiene los caracteres de `mi_cadena` desde el índice 5 hasta el índice 9.  

> Además, puedes omitir el índice inicial para empezar desde el principio de la cadena, o puedes omitir el índice final para ir hasta el final de la cadena. 

> También puedes usar un tercer número para especificar el paso de la rebanada. Por ejemplo, mi_lista[::2] obtendría todos los elementos de mi_lista con índices pares.

### Ejemplos de aplicación

``` py title="Python"
cadena = "Hola Mundo!"

# Imprime los caracteres en los índices 5 y 6 ("Mu")
print(cadena[5:7])      

# Imprime los caracteres en los índices -10, -9 y -8 ("ola")
print(cadena[-10:-7])   

# Imprime los caracteres desde el índice 5 hasta el final ("Mundo!")
print(cadena[5:])       

# Imprime los caracteres desde el inicio hasta el índice 3 ("Hola")
print(cadena[:4])      

# Imprime cada segundo carácter desde el índice 2 hasta el 10 ("l ud")
print(cadena[2:11:2])  

# Imprime la cadena completa ("Hola Mundo!")
print(cadena[:])       

# Imprime cada segundo carácter de la cadena completa ("Hl ud!")
print(cadena[::2])      

# Imprime la cadena en orden inverso ("!odnuM aloH")
print(cadena[::-1])  
```

> Cada línea imprime una parte diferente de la cadena, utilizando diferentes maneras de indexación y segmentación.

``` title="Terminal (Entrada/Salida)"
# Son los caracteres comprendidos en el intervalo de posiciones sexta hasta séptima, con índices 5 al 6  
Mu      

# Son los caracteres comprendidos en el intervalo de posiciones décima desde atrás hasta octava desde atrás, con índices -10 al -8 
ola     

# Son los caracteres comprendidos en el intervalo de posiciones sexta hasta el final, con índices 5 en adelante 
Mundo!  

# Son los caracteres comprendidos en el intervalo de posiciones primera hasta cuarta, con índices 0 al 3 
Hola    

# Son los caracteres comprendidos en el intervalo de posiciones tercera hasta undécima, saltando de dos en dos, con índices 2 al 10 con paso 2
l ud    

# Son todos los caracteres de la cadena, desde el inicio hasta el final
Hola Mundo! 

# Son los caracteres comprendidos en toda la cadena, saltando de dos en dos, con índices desde el inicio hasta el final con paso 2
Hl ud!  

# Son todos los caracteres de la cadena, desde el final hasta el inicio, es decir, la cadena invertida
!odnuM aloH 
```

!!! important "¡Para recordar!"
    El subconjunto resultante de la cadena de caracteres incluye el valor del índice de inicio, pero no el valor del índice de fin si no su valor anterior.

    Y un tercer valor permite determinar un paso, que incluso puede ser negativo.

!!! warning "¡Precaución!"
    Cuando trabajas con índices, estos siempre deben ser válidos.  
    Cualquier intento de acceso a una posición inexistente (fuera de rango) resultará en un error de ejecución del programa.

    ``` py title="Python"
    print(cadena[-2:-6]) # No devuelve ninguna subcadena
    print(cadena[-6:10]) # Output: Mundo
    print(cadena[5:-1]) # Output: Mundo
    print(cadena[5:15]) # Output: Mundo!

    print(cadena[15]) IndexError: string index out of range

    print(cadena[-16]) IndexError: string index out of range
    ```

    > Presta atención que según el caso, utilizar un índice fuera de rango no siempre resulta en error.  

    > En el primer ejemplo, la rebanada no devuelve ninguna subcadena porque los índices están invertidos.  
    
    > En el cuarto ejemplo, la rebana se realiza sin problemas. Claro, independientemente que el índice de fin esté fuera de rango, la rebanada se efectuará desde la sexta posición (índice 5) hasta la quinceava posición (índice 14) o hasta alcanzar el final de la cadena de caracteres, lo que ocurra primero.

    > Pero en el quinto y sexto ejemplo si se produce un error de fuera de rango ya que la cadena no posee 16 caracteres.

## Uso de operadores con cadenas de caracteres

### Uso del operador \ en cadenas para partirlas en más de una línea 

Puedes usar el operador de continuación de línea ( \\ ) para dividir una cadena de texto en varias líneas sin interrumpir la cadena. 

Aquí tienes un ejemplo:

``` py title="Python"
cadena = "Esta es una cadena de texto muy larga que queremos dividir \
en varias líneas para mejorar la legibilidad del código."

print(cadena)
```

Cuando ejecutes este código, verás que la cadena se imprime como una sola línea, a pesar de que en el código fuente está dividida en dos líneas. Esto es porque el operador de continuación de línea ( \\ ) al final de la línea le dice a Python que la línea actual continúa en la siguiente línea.

``` title="Terminal (Entrada/Salida)"
Esta es una cadena de texto muy larga que queremos dividir en varias líneas para mejorar la legibilidad del código.
```

!!! warning "¡Atención!"
    Asegúrate de que no haya ningún espacio o cualquier otro carácter después del operador de continuación de línea ( \\ ), de lo contrario, Python interpretará el \ como un carácter literal en lugar de un indicador de continuación de línea.

!!! info "No solo con cadenas"
    El operador de continuación de línea ( \\ ) también se utiliza en Python para indicar que una línea de código continúa en la siguiente línea.  
    Esto es útil cuando tienes una línea de código muy larga y quieres dividirla en varias líneas para mejorar la legibilidad de este.

    ``` py title="Python"
    # Sin el operador de continuación de línea
    suma = 1 + 2 + 3 + 4 + 5 + 6 + 7 + 8 + 9 + 10

    # Con el operador de continuación de línea 
    # (¡Para recordar! que no debe posee más caracteres a continuación)
    suma = 1 + 2 + 3 + 4 + \
        5 + 6 + 7 + 8 + \
        9 + 10

    print(suma)  # Output: 55
    ```

### Replicación de cadenas de caracteres

Una cadena puede replicarse con el operador de repetición ( * ):

``` py title="Python"
risa = 'ja'
carcajada = risa * 5 # jajajajaja

asteriscos = "*" * 10

print(carcajada)
print(asteriscos)
```

``` title="Terminal (Entrada/Salida)"
jajajajaja
**********
```

### Concatenación de cadenas de caracteres

Las cadenas de caracteres pueden concatenarse (Unir o enlazar dos o más cadenas) utilizando el operador de concatenación ( + ):

``` py title="Python"
mensaje ="Buenos días"
nombre = "Pablo"
apellido = "Roca"

saludo = mensaje + " " + nombre + " " + apellido

print(saludo)
```

``` title="Terminal (Entrada/Salida)"
Buenos días Pablo Roca
```

!!! warning "¡Para recordar!"
    La función de concatenación es propia de las cadenas de caracteres.  
    El uso del operador de concatenación ( + ) en otro tipo o estructura de datos podría comportarse de diferente manera o devolver un error.

    ``` py title="Python"
    var1 = 3 + 5        # 8 (entero)
    var2 = "3" + "5"    # 35 (cadena de caracteres)
    var3 = str(3) + "5" # 35 (cadena de caracteres)
    var4 = 3 + int("5") # 8 (entero)
    var5 = 3 + "5"      # TypeError: unsupported operand type(s) for +: 'int' and 'str'   
    ```

### Comparación de cadenas de caracteres

Es posible comparar dos o más cadenas de caracteres en una expresión utilizando los operadores de comparación:

``` py title="Python"
cadena1 = "caso"
cadena2 = "caos"

print(cadena1 > cadena2)
print(cadena1 == cadena2)
print(cadena1 < cadena2)
```

La comparación no es por cantidad de caracteres sino por el caracter que se encuentra en cada posición de una cadena respecto del caracter que se encuentra en la misma posición de otra cadena:

``` title="Terminal (Entrada/Salida)"
True
False
False
```

> Solo la primera comparación del ejemplo anterior es verdadera: recién hay diferencia de caracteres en la tercera posición donde `cadena1` posee una `s` y `cadena2` posee una `o`, siendo la `s` mayor en valor posicional a la `o`

Lo mismo ocurre con la comparación de caracteres numéricos cuando estos son almacenados como caracteres de texto:

``` py title="Python"
cadena1 = "num_10"
cadena2 = "num_2"

print(cadena1 > cadena2)
print(cadena1 == cadena2)
print(cadena1 < cadena2)
```

``` title="Terminal (Entrada/Salida)"
False
False
True
```

> Solo la tercera comparación del ejemplo anterior es verdadera: recién hay diferencia de caracteres en la quinta posición donde `cadena1` posee un caracter `1` y `cadena2` posee un caracter `2`, siendo el `1` menor en valor posicional al `2`

!!! warning "¡Para recordar!"
    En Python, la comparación es _case sensitive_, es decir, que distingue entre mayúsculas y minúsculas:

    ``` py title="Python"
    cadena1 = "Mundo"
    cadena2 = "mundo"
    print(cadena1 == cadena2)
    ```

    ``` title="Terminal (Entrada/Salida)"
    False
    ```

### Comprobar si una subcadena se encuentra, o no, dentro de una cadena de caracteres

Las subcadenas son caracteres secuenciales dentro de una cadena de caracteres.  

Por ejemplo, la cadena "abc" tiene las siguientes subcadenas:  
"" , "a" , "ab" , "abc" , "b" , "bc" , "c"

Para comprobar si una subcadena se encuentra, o no, dentro de una cadena de caracteres, se utilizan los siguientes operadores:

* **in**: devuelve True si un valor se encuentra en la secuencia y False de lo contrario.
  
* **not in**: devuelve True si un valor no se encuentra en la secuencia y False de lo contrario.

```py title="Python"
cadena = "Hola, mundo!"

print("mundo" in cadena)  # Output: True
print("adios" in cadena)  # Output: False

print("mundo" not in cadena)  # Output: False
print("adios" not in cadena)  # Output: True
```

Más adelante veremos que podremos realizar estas comparaciones directamente mediante el uso de métodos.

''' info "¡¡Para recordar! que estos operadores también funcionan con otras estructuras de datos!"

## Uso de funciones con cadenas de caracteres

### Longitud de una cadena de caracteres

Python posee la función `len()` que retorna la longitud de una cadena de caracteres:

``` py title="Python"
cadena = "Hola Mundo!"
print("La cadena de caracteres", cadena, "tiene", len(cadena), "caracteres.")
```

``` title="Terminal (Entrada/Salida)"
La cadena de caracteres Hola Mundo! tiene 11 caracteres.
```

!!! warning "¡Para recordar!"
    `len()` cuenta todos los caracteres: los 4 de 'Hola', los 5 de 'Mundo', 1 del signo de exclamación y 1 del espacio, totalizando 11.  
    Es decir, que cualquier caracter que se encuentre dentro de las comillas será contado.

### Mínimo y máximo elemento de una cadena de caracteres

Las funciones min() y max() también pueden ser utilizadas con cadenas:

* min(): devuelve el carácter con el valor ASCII más pequeño.

* max() devuelve el carácter con el valor ASCII más grande.

Aquí tienes un ejemplo:

``` py title="Python"
cadena = "HolaMundo"

print(min(cadena))  # Output: 'H'
print(max(cadena))  # Output: 'u'
```

> En este caso, 'H' tiene el valor ASCII más pequeño en la cadena y 'u' tiene el valor ASCII más grande.  

## Uso de métodos de cadenas de caracteres

En general, las funciones son bloques de código independientes que realizan una tarea específica y pueden ser llamadas por su nombre. 

Los métodos, por otro lado, están asociados a un objeto específico (en este caso, una cadena de caracteres) y pueden modificar el estado de ese objeto o realizar una operación que está de alguna manera relacionada con ese objeto.

Las cadenas de caracteres en Python tienen muchos métodos incorporados para realizar diversas operaciones. 

Aquí están algunos de los más comunes:

* **format(\*args, \*\*kwargs)**: Realiza una operación de formato de cadena. Este método será explicado más adelante cuando tratemos el tema de formateo de cadenas de caracteres.

* **capitalize()**: Convierte el primer carácter a mayúsculas.

* **title()**: Devuelve una copia de la cadena convirtiendo la primera letra de cada palabra de la cadena a mayúsculas y el resto de las letras a minúsculas. 

    ``` py title="Python"
    cadena = "hola MUNDO"

    cadena_titulada = cadena.title()

    print(cadena_titulada)  # Output: "Hola Mundo"
    ```
    
    > En este código, `cadena.title()` convierte la cadena "hola mundo" a "Hola Mundo", donde la primera letra de cada palabra es mayúscula y todas las demás letras son minúsculas.


* **lower()**: Devuelve una copia de la cadena convirtiendo toda la cadena a minúsculas.

* **upper()**: Devuelve una copia de la cadena convirtiendo toda la cadena a mayúsculas.

* **swapcase()**: Devuelve una copia de la cadena invirtiendo el caso (mayúsculas &#10231; minúsculas) de cada carácter.

    ``` py title="Python"
    cadena = "hola Mundo"

    print(cadena.capitalize())  # Output: "Hola mundo"

    print(cadena.lower())       # Output: "hola mundo"

    print(cadena.upper())       # Output: "HOLA MUNDO"

    print(cadena.swapcase())    # Output: "HOLA mUNDO"

    print(cadena)               # Output: "hola Mundo"
    ```

    > Estos métodos no modifican la cadena de caracteres original.

* **istitle()**: Comprueba si la cadena está formateada como título.
    
* **islower()**: Comprueba si todos los caracteres en la cadena están en minúsculas.

* **isupper()**: Comprueba si todos los caracteres en la cadena están en mayúsculas.

* **isspace()**: Comprueba si todos los caracteres en la cadena son espacios en blanco.

* **isprintable()**: Comprueba si todos los caracteres en la cadena son imprimibles o no.
  
    ``` py title="Python"
    cadena1 = "Hola Mundo"
    cadena2 = "hola mundo"
    cadena3 = "HOLA MUNDO"

    print(cadena1.istitle())  # Output: True
    print(cadena1.islower())  # Output: False
    print(cadena1.isupper())  # Output: False

    print(cadena2.istitle())  # Output: False
    print(cadena2.islower())  # Output: True
    print(cadena2.isupper())  # Output: False

    print(cadena3.istitle())  # Output: False
    print(cadena3.islower())  # Output: False
    print(cadena3.isupper())  # Output: True

    cadena4 = "          "
    cadena5 = ""

    print(cadena4.isspace())  # Output: True
    print(cadena5.isspace())  # Output: False

    cadena6 = "Hola Mundo"
    cadena7 = "Hola Mundo\t\n"
    cadena8 = "\t\n"

    print(cadena6.isprintable())  # Output: True
    print(cadena7.isprintable())  # Output: False
    print(cadena8.isprintable())  # Output: False
    ```

    Existen otros métodos para validar el contenido de una cadena de caracteres:

    * isascii(): Comprueba si todos los caracteres en la cadena son ASCII.

    * isidentifier(): Comprueba si la cadena es un identificador válido de Python.

* **join(iterable)**: Si el argumento es un iterable, une los elementos de este (como una lista) en una sola cadena.
  
    Aquí tienes un ejemplo de cómo se usa join() con una lista:

    ``` py title="Python"
    # Lista de cadenas
    palabras = ["Hola", "mundo"]

    # Usa join para unir las palabras con un espacio
    frase = " ".join(palabras)

    print(frase)  # Output: Hola mundo
    ```

    > En este código, `" ".join(palabras)` une las cadenas en la lista `palabras` con un espacio entre ellas, resultando en la cadena `"Hola mundo"`.

    También puedes usar otros caracteres o cadenas como separador.  
    Por ejemplo, puedes usar `join()` para unir las cadenas con un guión:

    ``` py title="Python"
    # Lista de cadenas
    palabras = ["Hola", "mundo"]

    # Usa join para unir las palabras con un guión
    frase = "-".join(palabras)

    print(frase)  # Output: Hola-mundo
    ```

* **join(cadena)**: Si el argumento es una cadena, devuelve una cadena que es la unión de cada caracter que conforma la cadena del argumento a través de la cadena especificada como separador.

    Aquí tienes un ejemplo de cómo se usa join() con una cadena:

    ``` py title="Python"
    # Cadena de caracteres
    cadena = "12345"

    # Usa join para unir los caracteres que conforman *cadena*
    # '-' es la cadena que utilizará el método como separador de cada caracter durante la unión
    cadena_resultante = '-'.join(cadena) 

    print(cadena_resultante)  # Output: 1-2-3-4-5
    ```

    > En este código, `'-'` es el separador que se inserta entre cada carácter de la cadena original. El resultado es la cadena `"1-2-3-4-5"`.

* **count(subcadena[, inicio[, fin]])**: Se utiliza para contar el número de veces que una subcadena aparece en la cadena. 

    ``` py title="Python"
    cadena = "Hola mundo, mundo. Mundo, mundo."
    conteo = cadena.count("mundo")
    print(conteo)  # Output: 3
    ```
    
    > En este código, `cadena.count("mundo")` cuenta el número de veces que la subcadena "mundo" aparece en la variable `cadena`.  
    > En este caso, la subcadena "mundo" aparece tres veces (el tercer "Mundo" empieza con mayúsculas), por lo que el método count() devuelve 3.
    
    !!! warning "¡Para recordar!"
        `count()` es sensible a mayúsculas y minúsculas, por lo que "Mundo" y "mundo" se consideran diferentes.

    También puedes especificar un rango para la búsqueda con los parámetros opcionales start y end:

    ``` py title="Python"
    cadena = "Hola mundo, mundo. Mundo, mundo."
    print(cadena.count("mundo", 0, 14))  # Output: 1
    ```

    > En este código, `cadena.count("mundo", 0, 14)` cuenta cuántas veces la subcadena "mundo" aparece en la variable `cadena` entre los índices 0 y 14. En este caso, la subcadena "mundo" aparece una vez en ese rango, por lo que el método count() devuelve 1.

* startswith(prefijo[, inicio[, fin]]): Comprueba si la cadena comienza con el prefijo especificado.

* endswith(sufijo[, inicio[, fin]]): Comprueba si la cadena termina con el sufijo especificado.

    ``` py title="Python"
    cadena = "Hola mundo"

    # Comprobar si la cadena comienza con "Hola"
    if cadena.startswith("Hola"):
        print("La cadena comienza con 'Hola'.")
    else:
        print("La cadena no comienza con 'Hola'.")

    # Comprobar si la cadena termina con "mundo"
    if cadena.endswith("mundo"):
        print("La cadena termina con 'mundo'.")
    else:
        print("La cadena no termina con 'mundo'.")

    # Comprobar si la subcadena "ola" comienza en la posición 1
    if cadena.startswith("ola", 1):
        print("La subcadena 'ola' comienza en la posición 1.")
    else:
        print("La subcadena 'ola' no comienza en la posición 1.")

    # Comprobar si la subcadena "mun" termina en la posición 7
    if cadena.endswith("mun", 0, 7):
        print("La subcadena 'mun' termina en la posición 7.")
    else:
        print("La subcadena 'mun' no termina en la posición 7.")
    ```

    > En este código, `cadena.startswith("Hola")` devuelve `True` si cadena comienza con "Hola", y `False` en caso contrario.  
    > De manera similar, `cadena.endswith("mundo")` devuelve `True` si cadena termina con "mundo", y False en caso contrario.

    > Además, `cadena.startswith("ola", 1)` devuelve `True` si la subcadena de cadena que comienza en la posición 1 comienza con "ola", y False en caso contrario.  
    > De manera similar, `cadena.endswith("mun", 0, 7)` devuelve `True` si la subcadena de cadena que termina en la posición 7 termina con "mun", y False en caso contrario.

* **replace(cadena_buscada, cadena_nueva[, contador])**: Devuelve una copia de la cadena con las ocurrencias de la subcadena especificada en _cadena_buscada_ reemplazadas por otra cadena especificada en _cadena_nueva_.  
Si no se especifica _contador_ devuelve todas las ocurrencias reemplazas.  
Si se especifica _contador_, su valor representa el número (máximo) de ocurrencias que serán reemplazadas.

    ``` py title="Python"
    # Ejemplo de uso de replace(old, new)
    cadena = "Hola mundo, mundo"
    nueva_cadena = cadena.replace("mundo", "Python")

    print(nueva_cadena)  # Output: "Hola Python, Python"
    ```

    > En el primer ejemplo, `replace("mundo", "Python") `reemplaza todas las apariciones de "mundo" por "Python".

    ``` py title="Python"
    # Ejemplo de uso de replace(old, new, count)
    cadena = "Hola mundo, mundo"
    nueva_cadena = cadena.replace("mundo", "Python", 1)

    print(nueva_cadena)  # Output: "Hola Python, mundo"
    ```

    > En el segundo ejemplo, `replace("mundo", "Python", 1)` reemplaza solo la primera aparición de "mundo" por "Python", porque se especificó un conteo de 1.

* **split(separador=None[, maxsplit=-1])**: Divide la cadena en subcadenas usando  _separador_ como la cadena delimitadora; y las devuelve como una lista de elementos.  
Si _maxsplit_ no se especifica, se realizan todas las divisiones posibles.  
Si se especifica _maxsplit_, su valor representa el número (máximo) de divisiones que serán efectuadas.

    ``` py title="Python"
    # Ejemplo de uso de split(separador=None, maxsplit=-1)
    cadena = "Hola mundo Python"
    lista_palabras = cadena.split()

    print(lista_palabras)  # Output: ['Hola', 'mundo', 'Python']
    ```

    > En el primer ejemplo, `split()` divide la cadena en palabras, utilizando espacios como delimitadores.

    ``` py title="Python"
    # Ejemplo de uso de split(separador=None, maxsplit=1)
    cadena = "Hola mundo Python"
    lista_palabras = cadena.split(maxsplit=1)

    print(lista_palabras)  # Output: ['Hola', 'mundo Python']
    ```

    > En el segundo ejemplo, `split(maxsplit=1)` divide la cadena en palabras, pero solo realiza una división porque se especificó un `maxsplit` de 1.

    ``` py title="Python"
    # Ejemplo de uso de split(separador)
    cadena = "manzana,banana,fruta"
    lista_frutas = cadena.split(",")

    print(lista_frutas)  # Output: ['manzana', 'banana', 'fruta']
    ```

    > En el tercer ejemplo, `split(",")` divide la cadena en subcadenas, utilizando la coma como delimitador.

* rsplit(separador=None[, maxsplit=-1]): Divide una cadena en subcadenas a partir del final, usando  _separador_ como la cadena delimitadora; y las devuelve como una lista de elementos.  
Si no se especifica un separador, se utilizan espacios en blanco.  
Si _maxsplit_ no se especifica, se realizan todas las divisiones posibles.  
Si se especifica _maxsplit_, su valor representa el número (máximo) de divisiones que serán efectuadas.

    ``` py title="Python"
    # Ejemplo de uso de rsplit() sin especificar un separador
    cadena = "Hola mundo Python"
    lista_palabras = cadena.rsplit()
    print(lista_palabras)  # Output: ['Hola', 'mundo', 'Python']
    ```

    > En el primer ejemplo, `cadena.rsplit()` divide la cadena en palabras, utilizando espacios en blanco como delimitadores.

    ``` py title="Python"
    # Ejemplo de uso de rsplit() especificando un separador
    cadena = "manzana,banana,frutilla"
    lista_frutas = cadena.rsplit(',')
    print(lista_frutas)  # Output: ['manzana', 'banana', 'frutilla']
    ```

    > En el segundo ejemplo, `cadena.rsplit(',')` divide la cadena en palabras, utilizando comas como delimitadores.

    ``` py title="Python"
    # Ejemplo de uso de rsplit() especificando un separador y un maxsplit
    cadena = "manzana,banana,frutilla"
    lista_frutas = cadena.rsplit(',', 1)
    print(lista_frutas)  # Output: ['manzana,banana', 'frutilla']
    ```

    > En el tercer ejemplo, `cadena.rsplit(',', 1)` divide la cadena en palabras, utilizando comas como delimitadores, pero solo realiza una división desde el final porque se especificó un _maxsplit_ de 1.

* **partition(separador)**: Divide una cadena en una tupla de 3 elementos basándose en la primera aparición de un _separador_ especificado.  
La tupla resultante contiene la parte de la cadena antes del separador, el separador mismo, y la parte de la cadena después del separador.

* **rpartition(separador)**: Hace lo mismo que **partition(separador)**, pero comienza a buscar el separador desde el final de la cadena.

    ``` py title="Python"
    cadena = "hola mundo mundo"
    resultado = cadena.partition(" ")

    print(resultado)  # Output: ('hola', ' ', 'mundo mundo')
    ```

    >  En el primer ejemplo, `cadena.partition(" ")` divide `cadena` en la primera aparición del espacio en blanco, que es el separador especificado.  
    > Como resultado, obtenemos la tupla `('hola', ' ', 'mundo mundo')`.

    ``` py title="Python"
    cadena = "hola mundo mundo"
    resultado = cadena.rpartition(" ")

    print(resultado)  # Output: ('hola mundo', ' ', 'mundo')
    ```

    > En el segundo ejemplo, `cadena.rpartition(" ")` divide cadena en la última aparición del espacio en blanco.  
    > Como resultado, obtenemos la tupla `('hola mundo', ' ', 'mundo')`.

Si el _separador_ no se encuentra en la cadena, la tupla contendrá la cadena original, seguida de dos cadenas vacías.

``` py title="Python"
cadena = "hola mundo"
resultado = cadena.partition(" ")

print(resultado)  # Output: ('hola', ' ', 'mundo')
```

> En este código, `cadena.partition(" ")` divide cadena en la primera aparición del espacio en blanco, que es el separador especificado. Como resultado, obtenemos la tupla `('hola', ' ', 'mundo')`.

Y aquí tienes un ejemplo donde el separador no se encuentra en la cadena:

``` py title="Python"
cadena = "hola"
resultado = cadena.partition(" ")

print(resultado)  # Output: ('hola', '', '')
```

En este código, como el espacio en blanco no se encuentra en cadena, `cadena.partition(" ")` devuelve la tupla `('hola', '', '')`.

* **isalnum()**,
* **isalpha()**, 
* **isdigit()**: En Python, las cadenas tienen varios métodos útiles para detectar tipos de dato.
  
    * **isalnum()**: Comprueba si todos los caracteres en la cadena son alfanuméricos. Devuelve True si todos los caracteres en la cadena son alfanuméricos (letras o dígitos) y hay al menos un carácter, False en caso contrario.
    
        ``` py title="Python"
        print('abc123'.isalnum())  # Output: True
        print('abc 123'.isalnum())  # Output: False
        ```
    
    * **isalpha()**: Comprueba si todos los caracteres en la cadena son alfabéticos. Devuelve True si todos los caracteres en la cadena son letras del alfabeto y hay al menos un carácter, False en caso contrario.
    
        ``` py title="Python"
        print('abc'.isalpha())  # Output: True
        print('abc123'.isalpha())  # Output: False
        ```
    
    * **isdigit()**: Comprueba si todos los caracteres en la cadena son dígitos. Devuelve True si todos los caracteres en la cadena son dígitos y hay al menos un carácter, False en caso contrario.
    
        ``` py title="Python"
        print('123'.isdigit())  # Output: True
        print('abc123'.isdigit())  # Output: False
        ```

        > En el último ejemplo, `isalnum()` devuelve `False` porque la cadena contiene un espacio, que no es ni una letra ni un dígito.
    
    Existen otros métodos para validar el contenido de una cadena de caracteres:

    * isdecimal(): Comprueba si todos los caracteres en la cadena son decimales.

    * isnumeric(): Comprueba si todos los caracteres en la cadena son numéricos.

* **center(ancho[, caracter_de_relleno])**,
* **ljust(ancho[, caracter_de_relleno])**, 
* **rjust(ancho[, caracter_de_relleno])**: Alinean la cadena en un campo de un ancho especificado.  
Si no se especifica _caracter_de_relleno_, se rellenan con espacios los caracteres faltantes hasta completar el ancho de la cadena centrada.    
Si se especifica _caracter_de_relleno_, es el caracter que rellena los espacios adicionales hasta completar el ancho hacia ambos lados de la cadena centrada.

    * **center(ancho[, caracter_de_relleno])**: Centra la cadena en un campo de un ancho especificado.  

        ``` py title="Python"
        cadena = "hola mundo"

        cadena_centralizada = cadena.center(20)
        print(cadena_centralizada)  # Output: "    hola mundo     "

        cadena_centralizada_con_relleno = cadena.center(20, '*')
        print(cadena_centralizada_con_relleno)  # Output: "****hola mundo*****"
        ```

        > En el primer ejemplo, `cadena.center(20)` centra la cadena "hola mundo" en un campo de 20 caracteres de ancho, llenando los espacios hacia ambos lados de la cadena con espacios. 

        > En el segundo ejemplo, `cadena.center(20, '*')` hace lo mismo, pero rellena los espacios con asteriscos en lugar de espacios.

    * **ljust(ancho[, caracter_de_relleno])**: Devuelve la cadena justificada a la izquierda en un campo de un ancho especificado.

        ``` py title="Python"
        cadena = "hola mundo"

        cadena_justificada_izquierda = cadena.ljust(20)
        print(cadena_justificada_izquierda)  # Output: "hola mundo         "

        cadena_justificada_izquierda_con_relleno = cadena.ljust(20, '*')
        print(cadena_justificada_izquierda_con_relleno)  # Output: "hola mundo*********"
        ```
    
    * **rjust(ancho[, caracter_de_relleno])**: Devuelve la cadena justificada a la derecha en un campo de un ancho especificado.

        ``` py title="Python"
        cadena = "hola mundo"

        cadena_justificada_derecha = cadena.rjust(20)
        print(cadena_justificada_derecha)  # Output: "         hola mundo"

        cadena_justificada_derecha_con_relleno = cadena.rjust(20, '*')
        print(cadena_justificada_derecha_con_relleno)  # Output: "*********hola mundo"
        ```

* **zfill(ancho)**: Devuelve una copia de la cadena rellena con ceros a la izquierda hasta alcanzar el ancho especificado.  
Si la cadena ya comienza con un signo ( + / - ), el relleno de ceros se realiza después del signo.

    Aquí tienes un ejemplo:

    ``` py title="Python"
    cadena = "123"

    cadena_con_ceros = cadena.zfill(5)
    print(cadena_con_ceros)  # Output: "00123"
    ```
    
    > En este código, `cadena.zfill(5)` agrega ceros al principio de la cadena "123" hasta que su longitud sea 5, resultando en "00123".

    Aquí tienes otro ejemplo con un número negativo:

    ``` py title="Python"
    cadena = "-123"
    cadena_con_ceros = cadena.zfill(5)
    print(cadena_con_ceros)  # Output: "-0123"
    ```
    
    > En este código, `cadena.zfill(5)` agrega ceros después del signo '-', resultando en "-0123".

* **lstrip([cadena])**,
* **rstrip([cadena])**,
* **strip([cadena])**: Se utilizan para eliminar caracteres no deseados (espacios en blanco por defecto) de las cadenas.  
También se puede especificar un conjunto de caracteres para eliminar en lugar de espacios en blanco si se indica la _cadena_ correspondiente.
  
    * **lstrip([cadena])**: Devuelve una copia de la cadena luego de efectuar la eliminación correspondiente de caracteres al inicio de la cadena original.
    
        ``` py title="Python"
        # lstrip() elimina los espacios al principio de la cadena
        cadena = "   hola mundo"
        cadena_sin_espacios_izq = cadena.lstrip()
        print(cadena_sin_espacios_izq)  # Output: "hola mundo"

        # Eliminar caracteres específicos al principio de la cadena
        cadena = "+++hola mundo+++"
        cadena_sin_mas_izq = cadena.lstrip('+')
        print(cadena_sin_mas_izq)  # Output: "hola mundo+++"
        ```

    * **rstrip([cadena])**: Devuelve una copia de la cadena luego de efectuar la eliminación correspondiente de caracteres al final de la cadena original.

        ``` py title="Python"
        # rstrip() elimina los espacios al final de la cadena
        cadena = "hola mundo   "
        cadena_sin_espacios_der = cadena.rstrip()
        print(cadena_sin_espacios_der)  # Output: "hola mundo"

        # Eliminar caracteres específicos al final de la cadena
        cadena_sin_mas_der = cadena.rstrip('+')
        print(cadena_sin_mas_der)  # Output: "+++hola mundo"
        ```

    * **strip([cadena])**: Devuelve una copia de la cadena luego de efectuar la eliminación correspondiente de caracteres al inicio y al final de la cadena original.

        ``` py title="Python"
        # strip() elimina los espacios al principio y al final de la cadena
        cadena = "   hola mundo   "
        cadena_sin_espacios = cadena.strip()
        print(cadena_sin_espacios)  # Output: "hola mundo"

        # Eliminar caracteres específicos al principio y al final de la cadena
        cadena_sin_mas = cadena.strip('+')
        print(cadena_sin_mas)  # Output: "hola mundo"
        ```

* **find(subcadena[, inicio[, fin]])**,
* **rfind(subcadena[, inicio[, fin]])**,
* **index(subcadena[, inicio[, fin]])**,
* **rindex(subcadena[, inicio[, fin]])**: Los métodos index() / rindex() y find() / rfind() son similares ya que ambos buscan una subcadena en una cadena y devuelven el índice (la posición en la cadena) de la primera aparición de la subcadena.  
Sin embargo, difieren en su comportamiento cuando la subcadena no se encuentra en la cadena:

    * los métodos index() y rindex() lanzan una excepción _ValueError_. Esto significa que el programa se detendrá inesperadamente, a menos que la excepción se encuentre manejada por el programa para evitar la detención.
    
    * los métodos find() y rfind() devuelven -1

Opcionalmente, es posible indicar los índices de inicio y/o de fin de búsqueda.  

    * **find(subcadena[, inicio[, fin]])**,
    * **index(subcadena[, inicio[, fin]])**: Devuelve el índice más bajo en la cadena donde se encuentra la subcadena. Es decir, la primera ocurrencia posible.

    * **rfind(subcadena[, inicio[, fin]])**,
    * **rindex(subcadena[, inicio[, fin]])**: Devuelve el índice más alto en la cadena donde se encuentra la subcadena. Es decir, la última ocurrencia posible.

        ``` py title="Python"
        cadena = "Hola Mundo, Hola Python"

        # Uso de find()
        indice = cadena.find("Hola")
        print(indice)  # Output: 0

        # Uso de rfind()
        indice = cadena.rfind("Hola")
        print(indice)  # Output: 12

        # Uso de index() con índice de inicio
        indice = cadena.index("Hola", 3)
        print(indice)  # Output: 12

        # Uso de rindex() con índice de inicio y de fin
        indice = cadena.rindex("Hola", 0, 10)
        print(indice)  # Output: 0

        # Buscar una subcadena que no existe
        indice = cadena.find("Java")
        print(indice)  # Output: -1

        indice = cadena.index("Java")  # Output: ValueError: substring not found  
        print(indice) 
        ```

        > En el primer ejemplo, `cadena.find("Hola")` devuelve 0 porque la primera ocurrencia de "Hola" se encuentra en el caracter 1.

        > En el segundo ejemplo, `cadena.rfind("Hola")` devuelve 12 porque la última aparición de "Hola" se encuentra en el caracter 13.

        > En el tercer ejemplo, `cadena.index("Hola")` devuelve 12 porque, a partir del caracter 4, la primera ocurrencia de "Hola" se encuentra en el caracter 13.

        > En el cuarto ejemplo, `cadena.rindex("Hola")` devuelve 0 porque la última ocurrencia de "Hola" entre el caracter 1 y el caracter 11 se encuentra en el caracter 0.

        > En el quinto ejemplo, `cadena.find("Java")` devuelve -1 porque "Java" no se encuentra en la cadena.

        > En el sexto ejemplo, `cadena.index("Java")` devuelve la excepción `ValueError: substring not found` porque no se encuentra en la cadena.

        !!! important "¡Para recordar!"
            Si esperas que la subcadena pueda no estar en la cadena y no quieres manejar una excepción, `find()` puede ser una mejor opción.  

            Si esperas que la subcadena siempre esté en la cadena y quieres un error si no lo está, `index()` puede ser una mejor opción.

Estos son solo algunos ejemplos. Python tiene muchos más métodos de cadena incorporados:

* **casefold()**: Convierte la cadena a minúsculas, es similar a lower(), pero más agresivo porque está diseñado para eliminar todas las diferencias de caso que puedan afectar la comparación de cadenas.

* **encode([encoding[, errors]])**: Devuelve una versión codificada de la cadena como un objeto bytes.

* **expandtabs([tabsize])**: Devuelve una copia de la cadena donde todos los caracteres de tabulación se reemplazan por uno o más espacios.

* **format_map(mapping)**: Realiza una operación de formato de cadena.

* **maketrans(x[, y[, z]])**: Devuelve una tabla de traducción utilizable para str.translate().

* **splitlines([keepends])**: Devuelve una lista de las líneas en la cadena.

* **translate(table)**: Devuelve una copia de la cadena en la que cada carácter ha sido mapeado a través de la tabla de traducción proporcionada. La tabla de traducción debe ser creada con el método maketrans().

## Formateo de cadenas de caracteres 

### Uso del método format()

El método **format(\*args, \*\*kwargs)** realiza una operación de formato de cadena, es decir que se utiliza para formatear una cadena insertando valores en ella. 

Aquí tienes algunos ejemplos:

1. Formateo básico:

``` py title="Python"
print("Hola, {}!".format("Mundo"))
print("Hola, {} y {}!".format("Mundo", "Python"))
```

``` title="Terminal (Entrada/Salida)"
Hola, Mundo!
Hola, Mundo y Python!
```

1. Formateo con índices posicionales:

``` py title="Python"
print("Hola, {0} y {1}!".format("Mundo", "Python"))
print("Hola, {1} y {0}!".format("Mundo", "Python"))
```

``` title="Terminal (Entrada/Salida)"
Hola, Mundo y Python!
Hola, Python y Mundo!
```

1. Formateo con argumentos clave:

``` py title="Python"
print("Hola, {nombre}!".format(nombre="Mundo"))
print("Hola, {adjetivo} {nombre}!".format(adjetivo="gran", nombre="Mundo"))
print("Hola, {adjetivo} {nombre}!".format(nombre="Mundo", adjetivo="gran"))
```

``` title="Terminal (Entrada/Salida)"
Hola, Mundo!
Hola, gran Mundo!
Hola, gran Mundo!
```

1. Formateo con precisión para números de punto flotante:

``` py title="Python"
print("El valor de PI aproximado es 3.14159265358979323846…")
print("El valor de PI menos aproximado es {0:.7f}".format(3.14159265358979323846))
print("El valor de PI menos aproximado aún es {0:.4f}".format(3.14159265358979323846))
print("El valor de PI que normalmente utilizamos en matemáticas es {0:.2f}".format(3.14159265358979323846))
```

``` title="Terminal (Entrada/Salida)"
El valor de PI aproximado es 3.14159265358979323846…
El valor de PI menos aproximado es 3.1415927
El valor de PI menos aproximado aún es 3.1416
El valor de PI que normalmente utilizamos en matemáticas es 3.14
```

1. Formateo con alineación:
``` py title="Python"
print("|{:<10}|{:^10}|{:>10}|".format('izq', 'centro', 'der'))
```

``` title="Terminal (Entrada/Salida)"
|izq       |  centro  |       der|
```

En estos ejemplos, las llaves ( {} ) se utilizan como marcadores de posición donde se insertarán los valores proporcionados a format(). Los números, las palabras clave y las especificaciones de formato dentro de las llaves controlan qué valores se insertan y cómo se formatean.

### Uso de _f-Strings_

Las _f-strings_ son una característica de Python que permite la interpolación de cadenas de una manera más concisa y legible. 

Las _f-strings_ se crean poniendo una `f` o `F` antes de la cadena y poniendo las variables que quieres interpolar entre llaves {} dentro de la cadena.

Aquí tienes un ejemplo:

``` py title="Python"
nombre = "Pablo"
edad = 45
print(f"Hola, mi nombre es {nombre} y tengo {edad} años.")
```

> En este código, `{nombre}` y `{edad}` dentro de la _f-string_ se reemplazan por los valores de las variables `nombre` y `edad`, respectivamente. Por lo tanto, la salida de este código sería: "Hola, mi nombre es Juan y tengo 30 años."

También es posible utilizar las _f-strings_ como expresión para crear una cadena de caracteres y almacenarla en una variable, por ejemplo:

``` py title="Python"
nombre = "Pablo"
edad = 45

cadena = f"Hola, mi nombre es {nombre} y tengo {edad} años."

print(cadena) # Output: Hola, mi nombre es Pablo y tengo 45 años.
```

Las _f-strings_ también pueden contener expresiones arbitrarias dentro de las llaves, que se evaluarán y luego se convertirán en una cadena. 

Por ejemplo:

``` py title="Python"
a = 5
b = 10
print(f"La suma de {a} y {b} es {a + b}.")
```

La salida de este código sería: "La suma de 5 y 10 es 15."

!!! success "¡Bienvenidas las _f-strings_!"
    Esta sintaxis para escribir cadenas de caracteres interpoladas es una gran característica de Python y debes aprovecharla.

    Te vas a ahorrar muchos dolores de cabeza a la hora de concatenar diferentes tipos de dato a la hora de mostrar información en pantalla o crear una cadena de texto para utilizarla en expresiones o almacenarla en una variable, por ejemplo.

### Uso del operador de formateo ( % )

El operador de formateo de cadenas ( % ) en las cadenas de Python se utiliza para el formateo de cadenas. Es similar a la función `printf` en C. 

Aquí tienes algunos ejemplos:

``` py title="Python"
nombre = "Pablo"
print("Hola, %s" % nombre)
```

``` title="Terminal (Entrada/Salida)"
Hola, Pablo
```

``` py title="Python"
apellido = "Roca"
print("Hola, %s %s" % (nombre, apellido))
```

``` title="Terminal (Entrada/Salida)"
Hola, Pablo Roca
```

``` py title="Python"
edad = 45
print("Hola, %s %s, tienes %d años" % (nombre, apellido, edad))
```

``` title="Terminal (Entrada/Salida)"
Hola, Pablo Roca, tienes 30 años
```

``` py title="Python"
pi = 3.14159
print("El valor de pi es aproximadamente %f" % pi)
print("El valor de pi es aproximadamente %.2f" % pi)
```

``` title="Terminal (Entrada/Salida)"
El valor de pi es aproximadamente 3.141590
El valor de pi es aproximadamente 3.14
```

> En estos ejemplos, `%s` es un marcador de posición para una cadena, `%d` es un marcador de posición para un número entero y `%f` es un marcador de posición para un número de punto flotante.  
> Los valores después del `%` se insertan en la cadena en los lugares donde están los marcadores de posición.

!!! info "¡Atención!"
    Aunque **este método de formateo** de cadenas todavía es válido en Python, **se considera antiguo** y se recomienda usar el método `format()` o las _f-strings_ (en Python 3.6 y versiones posteriores) para el formateo de cadenas.

Para terminar de entender la sintaxis, analicemos una de las instrucciones de impresión que utiliza el antiguo estilo de formateo de cadenas.

``` py title="Python"
print ("Hola, %s %s, tienes %d años" % (nombre, apellido, edad))
```

Aquí está lo que hace cada parte:

    * **print**: Esta es la función de Python para imprimir texto en la consola.

    * **"Hola, %s %s, tienes %d años"**: Esta es la cadena que se va a imprimir. Los %s y %d son marcadores de posición que se reemplazarán con los valores proporcionados después del %.

    * **%s**: Este es un marcador de posición para una cadena. Se reemplazará con una cadena.

    * **%d**: Este es un marcador de posición para un número entero. Se reemplazará con un número entero.

    * **nombre**, **apellido**, **edad**: Estos son los valores que se insertarán en la cadena en los lugares donde están los marcadores de posición. 
 
    El primer %s se reemplazará con el valor de nombre, el segundo %s se reemplazará con el valor de apellido, y el %d se reemplazará con el valor de edad.

Por lo tanto, si nombre es "Pablo", apellido es "Roca" y edad es 45, la salida de esta línea de código sería:

``` title="Terminal (Entrada/Salida)"
Hola, Pablo Roca, tienes 45 años
```

### Uso del operador \ en cadenas para partirlas en más de una línea 

Puedes usar el operador de continuación de línea ( \\ ) para dividir una cadena de texto en varias líneas sin interrumpir la cadena. 

Aquí tienes un ejemplo:

``` py title="Python"
cadena = "Esta es una cadena de texto muy larga que queremos dividir \
en varias líneas para mejorar la legibilidad del código."

print(cadena)
```

Cuando ejecutes este código, verás que la cadena se imprime como una sola línea, a pesar de que en el código fuente está dividida en dos líneas. Esto es porque el operador de continuación de línea ( \\ ) al final de la línea le dice a Python que la línea actual continúa en la siguiente línea.

``` title="Terminal (Entrada/Salida)"
Esta es una cadena de texto muy larga que queremos dividir en varias líneas para mejorar la legibilidad del código.
```

!!! warning "¡Atención!"
    Asegúrate de que no haya ningún espacio o cualquier otro carácter después del operador de continuación de línea ( \\ ), de lo contrario, Python interpretará el \\ como operador de "escape" (lo veremos en un momento) en lugar de un indicador de continuación de línea.

!!! info "No solo con cadenas"
    El operador de continuación de línea ( \\ ) también se utiliza en Python para indicar que una línea de código continúa en la siguiente línea.  
    Esto es útil cuando tienes una línea de código muy larga y quieres dividirla en varias líneas para mejorar la legibilidad de este.

    ``` py title="Python"
    # Sin el operador de continuación de línea
    suma = 1 + 2 + 3 + 4 + 5 + 6 + 7 + 8 + 9 + 10

    # Con el operador de continuación de línea 
    # (¡Para recordar! que no debe posee más caracteres a continuación)
    suma = 1 + 2 + 3 + 4 + \
        5 + 6 + 7 + 8 + \
        9 + 10

    print(suma)  # Output: 55
    ```

### Uso del operador de escape ( \\ ) en cadenas

El operador de "escape" ( \\ ) en las cadenas de Python se utiliza para introducir secuencias de escape, que son representaciones de caracteres especiales que no se pueden escribir de manera literal.

Por ejemplo, `\\t` es una secuencia de escape que representa un carácter de tabulación.    
Otras secuencias de escape comunes incluyen `\\n` para una nueva línea, `\\'` para una comilla simple y `\\"` para una comilla doble.

``` py title="Python"
print("Hola\nMundo")  # \n es una secuencia de escape para una nueva línea
print("Hola\tMundo")  # \t es una secuencia de escape para una tabulación
print("Ella dijo: \"Hola Mundo\"")  # \" es una secuencia de escape para una comilla doble
print('It\'s a beautiful day')  # \' es una secuencia de escape para una comilla simple
```

Estos códigos imprimirán en pantalla:

``` title="Terminal (Entrada/Salida)"
Hola
Mundo
Hola	Mundo
Ella dijo: "Hola Mundo"
It's a beautiful day
```

!!! info "Para recordar"
    Como puedes ver, el operador de escape ( \\ ) permite insertar caracteres especiales en las cadenas que de otra manera serían difíciles o imposibles de incluir.

#### Comandos de "escape" disponibles

```
Secuencia Escape  	Significado
------------------------------------------------------------------------------------
\newline      	    Ignorado
\\	                Backslash (\)
\'	                Comillas simple (')
\"            	    Comillas doble (")
\a	                Bell ASCII (BEL)
\b            	    Backspace ASCII (BS)
\f	                Formfeed ASCII (FF)
\n	                Linefeed ASCII (LF)
\N{name}	        Carácter llamado name en base de datos Unicode (solo Unicode)
\r	                Carriage Return ASCII (CR)
\t	                Tabulación Horizontal ASCII (TAB)
\uxxxx	            Carácter con valor hex 16-bit xxxx (solo Unicode). Ver hex.
\Uxxxxxxxx    	    Carácter con valor hex 32-bit xxxxxxxx (solo Unicode). Ver hex.
\v	                Tabulación Vertical ASCII (VT)
\ooo              	Carácter con valor octal ooo. Ver octal.
\xhh          	    Carácter con valor hex hh. Ver hex.
``` 
