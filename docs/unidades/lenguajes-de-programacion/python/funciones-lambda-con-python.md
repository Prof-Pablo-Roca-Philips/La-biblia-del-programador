## sintaxis:

!!! warning "Completar esta parte"

variable = lambda parámetro_1, ... , parametro_n: return expresión 

### Ejemplos de aplicación simple

Ejemplo 1: calcular el cuadrado de un número.

``` py title="Python"
# Definición de funciones

# Función lambda para calcular el cuadrado de un número
# Retorna el cuadrado de cada número pasado a la función
calcular_cuadrado = lambda x: x**2


# Bloque principal del programa

valor = 4
print("El cuadrado de", valor, "es", calcular_cuadrado(valor))
```

``` title="Terminal (Entrada/Salida)"
El cuadrado de 4 es 16
```

Ejemplo 2: determinar si un número es par o impar.

``` py title="Python"
# Definición de funciones

# Función lambda para determinar si un número es par o impar
# Retorna "par" o "impar"
validar_si_numero_es_par_o_impar = lambda x: "par" if x % 2 == 0 else "impar" 


# Bloque principal del programa

numero = 13
print(f"El {numero} es un número {validar_si_numero_es_par_o_impar(numero)}")

numero = 16
print(f"El {numero} es un número {validar_si_numero_es_par_o_impar(numero)}")
```

``` title="Terminal (Entrada/Salida)"
El 13 es un número impar
El 16 es un número par
```

Ejemplo 3: determinar si un número es múltiplo de otro.

``` py title="Python"
# Definición de funciones

# Función lambda para determinar si un número es múltiplo de otro
# Retorna "es múltiplo" o "no es múltiplo"
validar_si_es_multiplo = lambda x, y: "es múltiplo" if x % y == 0 else "no es múltiplo"


# Bloque principal del programa

valor_menor = 5 
valor_mayor = 15
print("El " + str(valor_mayor) + " " + validar_si_es_multiplo(valor_mayor, valor_menor) + " de " + str(valor_menor))

valor_menor = 4 
valor_mayor = 19
print("El " + str(valor_mayor) + " " + validar_si_es_multiplo(valor_mayor, valor_menor) + " de " + str(valor_menor))

```

``` title="Terminal (Entrada/Salida)"
El 15 es múltiplo de 5
El 19 no es múltiplo de 4
```

### Ejemplos de aplicación con _map_

Ejemplo 1: calcular el cuadrado de una lista de números.

``` py title="Python"
# Definición de funciones

# Función lambda para calcular el cuadrado de un número
# Retorna una tupla con el número y su cuadrado
calcular_cuadrado = lambda x: (x, x**2) 


# Bloque principal del programa

# Inicializa una lista de números
lista_de_numeros = [1, 2, 3, 4, 5]

# Emplea la función *map* para iterar con la lista, invocando a la función calcular_cuadrado() con cada elemento como argumento y al finalizar almacena los resultados de cada invocación en una lista
lista_de_cuadrados = list(map(calcular_cuadrado, lista_de_numeros))

# Itera con la lista de cuadrados imprimiendo en pantalla los resultados obtenidos para cada elemento de la lista de números
for nro, cuadrado_de_nro in lista_de_cuadrados:
    print("El cuadrado de", nro, "es", cuadrado_de_nro)
```

``` title="Terminal (Entrada/Salida)"
El cuadrado de 1 es 1
El cuadrado de 2 es 4
El cuadrado de 3 es 9
El cuadrado de 4 es 16
El cuadrado de 5 es 25
```

### Ejemplos de aplicación con _map_ y lista de funciones

``` py title="Python" linenums="1"
# Definición de funciones

# Función lambda para calcular el cuadrado de un número
# Retorna el cuadrado de cada número pasado a la función
calcular_cuadrado = lambda x: x**2

# Función lambda para determinar si un número es par o impar
# Retorna "par" o "impar"
validar_si_numero_es_par_o_impar = lambda x: "par" if x % 2 == 0 else "impar"


# Bloque principal del programa

# Se define la lista de funciones que se invocarán
lista_de_funciones = [calcular_cuadrado, validar_si_numero_es_par_o_impar]

# Inicializa una lista de números
lista_de_numeros = [1, 2, 3, 4, 5]


# Recorro la lista de valores y aplico las funciones de la lista:
for elemento in lista_de_numeros:
    
    valores = list(map(lambda x: x(elemento), lista_de_funciones))
    
    print(f"{elemento} es {valores[1]}, y elevado al cuadrado es {valores[0]}")
```

``` title="Terminal (Entrada/Salida)"
1 es impar, y elevado al cuadrado es 1
2 es par, y elevado al cuadrado es 4
3 es impar, y elevado al cuadrado es 9
4 es par, y elevado al cuadrado es 16
5 es impar, y elevado al cuadrado es 25
```

Si analizamos concretamente como resulta la estructura de datos, podemos reemplazar en nuestro código inicial desde la línea 21 por el siguiente código:

``` py title="Python"
# Recorro la lista de valores y aplico las funciones de la lista:
for elemento in lista_de_numeros:
    
    valores = list(map(lambda x: x(elemento), lista_de_funciones))
    
    print(elemento, "--->", valores)
```

Y podremos ver el siguiente resultado:

``` title="Terminal (Entrada/Salida)"
1 ---> [1, 'impar']
2 ---> [4, 'par']
3 ---> [9, 'impar']
4 ---> [16, 'par']
5 ---> [25, 'impar']
```

Por un lado, tenemos los elementos de la lista de números y, por otro lado, tenemos los elementos compuestos por la lista de resultados obtenidos para cada número de la lista de números, almacenados en otra lista distinta.

Es decir, los números y los resultados obtenidos a partir de ellos no están asociados o vinculados de ninguna manera.  
Esto puede resultar peligroso a nivel de integridad referencial de datos. Es decir, no hay una "cadena" que los ate de manera que no se pierdan ni se mezclen.

Si quisiéramos evitar este problema, deberíamos vincular los elementos de ambas listas de manera ordenada en una única lista.  
Para ello, podríamos escribir un código con sentencias más complejas como las que veremos a continuación y reemplazar el código original a partir de la línea 21: 

``` py title="Python"
# Emplea la función *map* para iterar con la lista de elementos y, en cada iteración emplea otra función *map* para iterar con la lista de funciones invocando a cada una  con cada elemento de la lista de elementos como argumento y al finalizar almacena el valor del elemento y los resultados de cada invocación en una lista

# El uso del operador de desempaquetado (unpacking operator) ( * ) permite desempaquetar la lista de elementos que genera la función *map* en elementos individuales
lista_de_valores = list(map(lambda elemento: list((elemento, *map(lambda x: x(elemento), lista_de_funciones))), lista_de_numeros))

# Itera con la lista de valores imprimiendo en pantalla los resultados obtenidos para cada elemento de la lista de números
for elemento, cuadrado, paridad in lista_de_valores:
    print(f"{elemento} es {paridad}, y elevado al cuadrado es {cuadrado}")
```

``` title="Terminal (Entrada/Salida)"
1 es impar, y elevado al cuadrado es 1
2 es par, y elevado al cuadrado es 4
3 es impar, y elevado al cuadrado es 9
4 es par, y elevado al cuadrado es 16
5 es impar, y elevado al cuadrado es 25
```

Como podemos observar, el resultado final es el mismo, pero si analizamos concretamente como resulta la estructura de datos ahora veremos que es mucho más ordenada y robusta en cuanto a la vinculación de todos los elementos:

``` py title="Python"
print(lista_de_valores)
```

``` title="Terminal (Entrada/Salida)"
[[1, 1, 'impar'], [2, 4, 'par'], [3, 9, 'impar'], [4, 16, 'par'], [5, 25, 'impar']]
```

> Observamos que la lista contiene elementos que son listas que contienen elementos que corresponden al número de la lista de números, al cuadrado de dicho número y al tipo de paridad de dicho número. 