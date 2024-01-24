## Funciones sin parámetros

``` py title="Python"
# Definición de funciones
        
# Definimos una función que imprime en pantalla un saludo
def saludar():
    print ("Hola, ¿cómo estás?")


# Bloque principal del programa

# Llamamos (invocamos) a la función saludar()
saludar()
```

## Funciones con parámetros

``` py title="Python"
# Definición de funciones

# Definimos una función que suma dos números pasados como argumentos desde la llamada a la función
# La función posee dos parámetros, uno para cada uno de los argumentos mencionados
def sumar(num1, num2):
    print(f"La suma de los números enteros {num1} y {num2} es {num1 + num2}.")


# Bloque principal del programa

# Llamamos (invocamos) a la función sumar():
sumar(1, 100)
```

``` title="Terminal (Entrada/Salida)"
La suma de los números enteros 1 y 100 es 101.
```

### Ejemplo de aplicación

Teniendo en cuenta el ejemplo anterior, modificar el programa para que sume todos los números enteros entre 2 números específicos.

``` py title="Python"
# Definición de funciones

# Definimos una función que suma todos los números enteros entre dos números pasados como argumentos desde la llamada a la función
# La función posee dos parámetros, uno para cada uno de los argumentos mencionados
def sumar_entre(num_menor, num_mayor):
    # Inicializamos la variable acumuladora
    suma = 0   

    for num in range(num_menor, num_mayor + 1):
        suma += num
        
    print(f"La suma de todos los números los enteros entre {num_menor} y {num_mayor} es {suma}.")


# Bloque principal del programa

# Llamamos (invocamos) a la función sumar_entre():
sumar_entre(1, 100)
```

``` title="Terminal (Entrada/Salida)"
La suma de todos los números los enteros entre 1 y 100 es 5050.
```

!!! question "¿Conoces la historia del pequeño Gauss y la suma de los números enteros entre 1 y 100?"

    "... Ocurrió en la escuela de Brunswick, cierto día de 1786, cuando Gauss contaba nueve años. El maestro encargó a sus alumnos que hiciesen como ejercicio de adición la suma de todos los números enteros desde el 1 hasta el 100, ambos inclusive.  
    Se trataba de sumar la sucesión 1, 2, 3, 4, ... , 99, 100.  
    Los alumnos, con una sola excepción, empezaron sumando 1 + 2; al resultado de esta suma, 3, le añadieron el 3, lo cual les dio 6, luego 4, obteniendo 10 y así sucesivamente.  
    La suma de los cien sumandos (cada una de las cantidades parciales que han de acumularse o añadirse unas a otras para formar la suma o cantidad total que se busca) por este procedimiento había de tener ocupados a los estudiantes por un buen rato. Sin embargo, cuentan las crónicas que, al poco tiempo de propuesta la tarea, cierto alumno, llamado Carl Friedrich Gauss, se presentó a su maestro con el resultado correcto: 5050.   
    El maestro, perplejo, le preguntó al pequeño cómo se las había arreglado para hacer la tarea tan pronto. Gauss le explicó que los números que se iban a sumar se podían agrupar en parejas: 1 + 100, 2 + 99, 3 + 98, etc. cada una de las parejas sumando 101.   
    Como se formaban 50 parejas, bastaba hacer 101 · 50 = 5050.  
    Gauss había descubierto por sí solo y a la edad de nueve años el **método para obtener la suma de las sucesiones aritméticas** ..."

    > "Gauss, un genio sobrehumano" por Paulino Valderas
    > [Link al documento](https://docs.google.com/document/d/11FflElHsMbA9y86LrPDVGS7cmmTxOgHuRxkYSEFfhYI/preview?hgd=1)

Este método permite optimizar de manera increíble el algoritmo del programa para que sea mucho más eficiente en términos de rapidez:

``` py title="Python"
# Definición de funciones

def sumar_numeros_entre(num_menor, num_mayor):
    # Inicializamos la variable acumuladora
    suma = 0   

    for num in range(num_menor, num_mayor + 1):
        suma += num
        
    print(f"La suma de todos los números los enteros entre {num_menor} y {num_mayor} es {suma}.")

def sumar_sucesiones_aritmeticas(num_menor, num_mayor):
    valor_pareja = num_menor + num_mayor
    cant_parejas = (num_mayor - num_menor + 1) // 2
    numero_intermedio_si_cant_numeros_es_impar = 0 # El 0 al ser neutro, es como si no existiese valor para sumar más adelante
    
    # Esta estructura alternativa detecta si la cantidad de números es impar
    # En caso de ser asi, el número del medio de la serie no tendría pareja
    # Por lo tanto, necesita sumarse solo al conjunto de parejas
    if (num_mayor - num_menor + 1) % 2 != 0:
        numero_intermedio_si_cant_numeros_es_impar = (num_mayor - num_menor) // 2 + num_menor
    
    # Cálculo según el algoritmo desarrollado por Gauss        
    suma = valor_pareja * cant_parejas + numero_intermedio_si_cant_numeros_es_impar

    print(f"La suma de todos los números los enteros entre {num_menor} y {num_mayor} es {suma}.")


# Bloque principal del programa

# Llamamos (invocamos) a la función sumar_entre():
sumar_numeros_entre(5, 20)

# Llamamos (invocamos) a la función sumar_sucesiones_aritmeticas():
sumar_sucesiones_aritmeticas(5, 20)
```

``` title="Terminal (Entrada/Salida)"
La suma de todos los números los enteros entre 5 y 20 es 200.
La suma de todos los números los enteros entre 5 y 20 es 200.
```

!!! success "Para tener en cuenta"
    Analizando ambas funciones del ejercicio anterior, podemos deducir que muchas veces la simplicidad del código puede representar una ejecución poco eficiente mientras que un código con mayor complejidad (no siempre más líneas significan mayor complejidad) puede representar una ejecución muy eficiente.

    Por eficiencia podemos hablar de velocidad en tiempo de ejecución y/o cantidad de instrucciones ejecutadas y/o cantidad de recursos físicos empleados (lease memoria RAM por ejemplo) entre otros parámetros.

!!! question "¿Por qué la eficiencia de un algoritmo es muy importante?"
    Podríamos hablar del tema durante horas y debatir mil cuestiones. Pero solo vamos a ir a un ejemplo concreto siguiendo con el método Gauss:

    Ejecutamos ambos programas para calcular la suma de valores entre 1 y 100000

    El resultado fue determinante en cuestiones de tiempo de ejecución:

    ``` title="Terminal (Entrada/Salida)"
    # Sin aplicar el método de Gauss
    La suma de todos los números los enteros entre 1 y 100000 es 5000050000.
    La función se ejecutó en: 15.763926029205322 segundos (1705702169.002692 -> 1705702184.766618)
    
    # Aplicando el método de Gauss
    La suma de todos los números los enteros entre 1 y 100000 es 5000050000.
    La función se ejecutó en: 0.0 segundos (1705702184.766618 -> 1705702184.766618)
    ```

    > Los dos valores entre paréntesis representan el momento en que se inició y finalizó la ejecución de la función.

## Funciones con parámetros opcionales

Para entender el concepto de parámetro opcional, vamos a modificar el código del ejemplo anterior para que:

* Se puedan ingresar los 2 números para realizar la suma
* Se pueda elegir, opcionalmente, si se desea conocer el tiempo que hubiera tardado la computadora en hacer el cálculo con y sin el método de Gauss

``` py title="Python"
# Importación de los módulos necesarios para la ejecución del programa

import time


# Definición de funciones

def sumar_numeros_entre(num_menor, num_mayor, ver_tiempo_ejecucion = False):
    suma = 0   

    if ver_tiempo_ejecucion:
        start_time = time.time()

    for num in range(num_menor, num_mayor + 1):
        suma += num
    
    if ver_tiempo_ejecucion:
        end_time = time.time()
        execution_time = end_time - start_time
        print(f"La función sin el método de Gauss se ejecutó en: {execution_time} segundos\n{start_time} -> {end_time} = {end_time-start_time}")
    
    print(f"La suma de todos los números los enteros entre {num_menor} y {num_mayor} es {suma}.")

def sumar_sucesiones_aritmeticas(num_menor, num_mayor, ver_tiempo_ejecucion = False):
    
    if ver_tiempo_ejecucion:
        start_time = time.time()
        
    valor_pareja = num_menor + num_mayor
    cant_parejas = (num_mayor - num_menor + 1) // 2
    numero_intermedio_si_cant_numeros_es_impar = 0 

    if (num_mayor - num_menor + 1) % 2 != 0:
        numero_intermedio_si_cant_numeros_es_impar = (num_mayor - num_menor) // 2 + num_menor
        
    suma = valor_pareja * cant_parejas + numero_intermedio_si_cant_numeros_es_impar
    
    if ver_tiempo_ejecucion:
        end_time = time.time()
        execution_time = end_time - start_time
        print(f"La función con el método de Gauss se ejecutó en: {execution_time} segundos\n{start_time} -> {end_time} = {end_time-start_time}")
    
    print(f"La suma de todos los números los enteros entre {num_menor} y {num_mayor} es {suma}.")


# Bloque principal del programa

num_inicial = int(input("Ingrese el número inicial de la serie: "))
num_final = int(input("Ingrese el número final de la serie: "))

ver_tiempo_ejecucion = True if input("Desea ver el tiempo de ejecución (s/n)? ").lower() == "s" else False


if ver_tiempo_ejecucion:
    sumar_numeros_entre(num_inicial, num_final, ver_tiempo_ejecucion)
    sumar_sucesiones_aritmeticas(num_inicial, num_final, ver_tiempo_ejecucion)
    
else:
    sumar_sucesiones_aritmeticas(num_inicial, num_final)
```

``` title="Terminal (Entrada/Salida)"
Ingrese el número inicial de la serie: 1
Ingrese el número final de la serie: 100000
Desea ver el tiempo de ejecución (s/n)? s

La función sin el método de Gauss se ejecutó en: 0.0008780956268310547 segundos 
1705704419.080389 -> 1705704419.081267 = 0.0008780956268310547

La suma de todos los números los enteros entre 1 y 100000 es 5000050000.


La función con el método de Gauss se ejecutó en: 0.0 segundos 
1705704419.081267 -> 1705704419.081267 = 0.0

La suma de todos los números los enteros entre 1 y 100000 es 5000050000.
```

## Funciones con parámetros posicionales o con parámetros identificados

Veamos el caso de un programa que saluda al usuario de manera personalizada.  
Podría darse el caso donde se conoce o no se conoce el nombre del usuario para nombrarlo.  
También podría saludar en función del momento del día: mañana, tarde o noche.
Incluso podría evaluar si el usuario utiliza poco o mucho el programa en función del tiempo transcurrido desde su último uso. Y alentarlo a que lo haga más seguido.

``` py title="Python"
# Importación de los módulos necesarios para la ejecución del programa

import datetime
from os import system

# Definición de funciones

def saludar(nombre=None, momento_dia=None, ultimo_uso=None):
    
    if momento_dia == "tarde":
        print("¡Buenas tardes!")
    
    elif momento_dia == "noche":
        print("¡Buenas noches!")
    
    else:
        print("¡Buenos días!")
    
    print("¿Cómo te encuentras hoy", f", {nombre}" if nombre else "", "?", sep="")

    if ultimo_uso:
        tiempo_transcurrido = datetime.datetime.now() - ultimo_uso
        
        if tiempo_transcurrido.days > 30:
            print("Hace mucho que no usas el programa. ¡Qué bueno verte de nuevo por aquí!")
        elif tiempo_transcurrido.days < 5:
            print("¡Gracias por usar el programa regularmente!")


# Bloque principal del programa

# Inicialización de la variable de último uso para la simulación de último acceso
ultimo_uso = None

system("cls")

# Ejemplo de uso de la función saludar():

# 1) Pasando todos los argumentos en el orden que los recibirán los parámetros (manera tradicional):
print("\n\nUsuario 1:")
ultimo_uso = datetime.datetime.now() - datetime.timedelta(days=31)
saludar("Juan", "tarde", ultimo_uso) # Argumentos pasados a parámetros posicionales

# 2) Pasando todos los argumentos identificando los parámetros que los recibirán:
print("\n\nUsuario 2:")
ultimo_uso = datetime.datetime.now() - datetime.timedelta(days=15)
saludar(nombre="José", ultimo_uso=ultimo_uso, momento_dia="noche") # Argumentos pasados a parámetros identificados

# 3) Pasando todos los argumentos de manera mezclada:
print("\n\nUsuario 3:")
ultimo_uso = datetime.datetime.now() - datetime.timedelta(days=4)
saludar("Pedro", ultimo_uso=ultimo_uso, momento_dia="noche") # Lee el destacado más abajo para entender esta sintaxis

# 4) Pasando algunos argumentos solamente:
print("\n\nUsuario 4:")
saludar(momento_dia="dia") # Lee el destacado más abajo para entender esta sintaxis
```

!!! warning "¡Muy importante!"
    En el ejemplo anterior, vemos que podemos mezclar el orden de los argumentos dentro de la llamada a la función respecto del orden de los parámetros en la definición de la función si indicamos su nombre. 
    
    Pero siempre es necesario que aquellos argumentos identificados con el nombre del parámetro estén a la derecha de los argumentos que pasarán a los parámetros posicionales, es decir, aquellos argumentos que se indican en la llamada a la función sin especificar el nombre del parámetro y que se asocian por su posición.

    Y si no pasas todos los argumentos porque la función posee parámetros opcionales, deberás identificar todos los argumentos a partir del primer argumento pasado que no se encuentre en la posición del parámetro que debe recibirlo.


``` title="Terminal (Entrada/Salida)"
Usuario 1:
¡Buenas tardes!
¿Cómo te encuentras hoy, Juan?
Hace mucho que no usas el programa. ¡Qué bueno verte de nuevo por acá!


Usuario 2:
¡Buenas noches!
¿Cómo te encuentras hoy, José?


Usuario 3:
¡Buenas noches!
¿Cómo te encuentras hoy, Pedro?
¡Gracias por usar el programa regularmente!


Usuario 4:
¡Buenos días!
¿Cómo te encuentras hoy?
```

## Funciones que retornan un valor (_return_)

La mayoría de las funciones de un programa cumplen con la tarea de realizar algún cálculo y retornar el resultado obtenido para ser utilizado en el bloque principal del programa.

Por ejemplo, podemos definir una función que calcule el área de un triangulo en base a determinados argumentos recibidos para luego retornar el resultado obtenido:

``` py title="Python"
# Definición de funciones

def area_triangulo(base, altura):
    
    area = (base * altura) / 2
    
    return area


# Bloque principal del programa

# Solicita al usuario que ingrese las medidas del triángulo
base = float(input("Ingrese la base del triángulo (en cm.): "))
altura = float(input("Ingrese la altura del triángulo (en cm.): "))

# Se invoca a la función area_triangulo() para luego almacenar el valor retornado en la variable *area*
area = area_triangulo(base, altura)

# Imprime en pantalla el resultado obtenido
print(f"\nEl área de un triángulo con base = {base} cm. y altura = {altura} cm. es {area} cm².")
```

``` title="Terminal (Entrada/Salida)"
Ingrese la base del triángulo (en cm.): 10
Ingrese la altura del triángulo (en cm.): 8

El área de un triángulo con base = 10.0 cm. y altura = 8.0 cm. es 40.0 cm².
```

!!! success "¡Para tener en cuenta!"
    Recuerda que en Python todo es un objeto. Con esto en mente, es natural que una función pueda devolver cualquier objeto.  
    Asi, como en el ejemplo anterior devuelve un valor de punto flotante, también podría devolver un valor entero, o un valor booleano, o un caracter, o incluso una estructura de datos como una cadena de texto, una lista, un diccionario, una tupla, un conjunto o cualquier otra estructura válida.

## Funciones que retornan más de un valor

Python permite definir funciones que retornan más de un valor.

Por ejemplo, definamos una función que reciba una lista de números y devuelva el mayor y el menor de los números que se encuentren en ella:

``` py title="Python"
# Definición de funciones

# Esta función recibe una lista de números y retorna una tupla con el mayor y el menor valor
def funcion_mayor_menor(lista):
    
    if len(lista) == 0:
        return None, None # Si la lista está vacía, no hay mayor ni menor valor
    
    mayor = max(lista)
    menor = min(lista)
    
    # Retorna una tupla
    if mayor == menor:
        return None, None # Si mayor y menor son iguales, no hay mayor ni menor porque hay un solo valor o todos los valores son iguales    
    
    else:
        return (mayor, menor) # También funciona sin aplicar los paréntesis


# Bloque principal del programa

# Inicializa la lista de números
numeros = [1, 1, 2, 3, 4, 5, 5]

# Se invoca a la función con la lista de números y se recibe una tupla que es desempaquetada en 2 variables
num_mayor, num_menor = funcion_mayor_menor(numeros)

if num_mayor and num_menor:
    # Imprime en pantalla el resultado obtenido
    print(f"El mayor valor de la lista {numeros} es {num_mayor} y el menor valor es {num_menor}.")

else:
    print(f"La lista {numeros} no posee mayor ni menor valor.")
```

``` title="Terminal (Entrada/Salida)"
El mayor valor de la lista [1, 1, 2, 3, 4, 5, 5] es 5 y el menor valor es 1.
```
