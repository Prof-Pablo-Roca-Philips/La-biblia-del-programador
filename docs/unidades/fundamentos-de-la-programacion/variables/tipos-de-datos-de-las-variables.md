title: Tipos de datos de una variable

## Introducción

Se denomina dato a cualquier objeto manipulable por la computadora. Un dato puede ser un caracter leído de un teclado, datos o información almacenada en un disco, pendrive o cualquier otra unidad de almacenamiento, un valor que se encuentra en la memoria central (RAM), etc.

Los distintos tipos de datos se representan en diferentes formas en la computadora: por ejemplo, no se almacena internamente de la misma manera un número entero que un caracter. 

Aunque los lenguajes de alto nivel permiten en alguna medida ignorar la representación interna de los datos, es preciso conocer algunos conceptos mínimos.

A nivel de máquina todos los datos se representan utilizando una secuencia finita de bits. De este hecho ya se deduce que no todos los datos son representables en una computadora. 

La deﬁnición de un tipo de dato incluye la deﬁnición del conjunto de valores permitidos y las operaciones que se pueden llevar a cabo sobre estos datos.

Cuando se utiliza un dato en un programa es preciso que esté determinado su tipo para que el la computadora sepa cómo debe tratarlo y almacenarlo. 

Dependiendo del lenguaje puede o no ser preciso declarar expresamente en el programa el tipo de cada dato. 

No todos los tipos de datos existen en todos los lenguajes de programación. Hay lenguajes más ricos que otros en este sentido. 

## ¿Qué es el tipo de dato de una variable?

En programación, el tipo de dato de una variable se refiere al tipo de valor que puede ser almacenado en ella. Cada tipo de dato tiene sus propias características y restricciones. 

Los tipos de datos básicos más usuales son:

* Enteros (_int_): números pertenecientes a un subconjunto finito de los números enteros. Los enteros son números sin decimales.

	```
	1  2  -3  0
	```

* Reales (_float_): números pertenecientes a un subconjunto finito de los números reales. Los números reales constan de una parte entera y una parte decimal, es decir, son números con decimales. También se los conoce como flotantes o de punto flotante.
	
	```
	3.14  2.5  -0.5  5.0  0.09
	```

* Caracteres (_char_): son un conjunto finito de caracteres reconocidos por la computadora. Los caracteres son letras, números y símbolos individuales.
  
	```
	alfabéticos: A  B  C  ... Z    a  b  c ... z
	numéricos:   0  1  2  3  4  5  6  7  8  9  0
	símbolos:    +  -  *  /  ^  ,  ;  <  >  $  @
	```

* Lógicos (_bool_): también conocidos como booleanos son dos valores lógicos: verdadero (_true_) o falso (_false_).

	```
	verdadero:  1  	true 	(True)
	falso:      0  	false	(False)
	```

	Por ejemplo, tenemos el siguiente programa:

	``` py title="Python" linenums="1"
	valor1 = True
	valor2 = False

	print ("Valor 1: ", valor1)
	print ("Valor 2: ", valor2)

	print (valor1, " AND ", valor2 , " = ", valor1 and valor2)
	print (valor1, " OR ", valor2 , " = ", valor1 or valor2)
	print ("NOT ", valor2 , " = ", not valor2)
	```

	Esta es la respuesta:

	``` title="Terminal (Entrada/Salida)"
	Valor 1:  True
	Valor 2:  False
	True  AND  False  =  False
	True  OR  False  =  True
	NOT  False  =  True
	```

	!!! question "¿Entiendes todo lo que ocurre, línea tras línea?"

## ¿Cómo determino el tipo de una variable?

En la mayoría de los lenguajes de programación existen comandos que pueden evaluar el tipo de dato de un valor almacenado en un variable.
Así, podemos evaluar y manipular las variables de manera correcta durante la ejecución de un programa.

Por ejemplo, en Python podemos hacer lo siguiente:

``` py title="Python"
valor1 = True
valor2 = 12
valor3 = "Hola"
valor4 = 14.34

print ("Valor 1: ", type(valor1))
print ("Valor 2: ", type(valor2))
print ("Valor 3: ", type(valor3))
print ("Valor 4: ", type(valor4))
```

``` title="Terminal (Entrada/Salida)"
Valor 1:  <class 'bool'>
Valor 2:  <class 'int'>
Valor 3:  <class 'str'>
Valor 4:  <class 'float'>
```

## Estructuras de datos

Los tipos de datos vistos anteriormente se suelen denominar elementales o básicos. 

Una estructura de datos o tipo de datos estructurado es un tipo de dato construido a partir de otros tipos de datos. 
Podemos enumerar las siguientes estructuras:

```
Cadenas de caracteres (_string_)
Listas (_list_)
Matrices (_matrix_)
Tuplas (_tuple_)
Arreglos (_array_)
Diccionarios (_dict_)
Conjuntos (_set_)
```
	
Este tema es bastante largo y complejo por lo que merece una unidad de estudio aparte.  
Puedes acceder a la misma, haciendo clic [aquí](/unidades/estructuras-de-datos/introduccion-a-las-estructuras-de-datos.md).

### Ejercicios de aplicación

1. Escribe un programa que solicite el ingreso por teclado de datos referidos al nombre, el precio unitario y la cantidad de unidades vendidas de un producto.
Luego que imprima por pantalla una salida de información formateada de la siguiente manera:

    ``` title="Terminal (Entrada/Salida)"
    Ingrese el nombre del producto: Palta
	Ingrese el precio unitario del producto: 510.30
	Ingrese la cantidad de unidades compradas: 3

	Producto: Palta
	Precio unitario: 510.30
	Cantidad: 3
	----------------------------------
	Costo total de compra: 1530.90
    ```
    
	!!! warning "¡Atención! Alcance y Limitación"
		El costo total debe calcularse antes de realizar la impresión en pantalla.
		Presta atención al tratamiento de los decimales. Estamos hablando de dinero en algunos casos.

    Ver resultado (1)
    { .annotate }

    1. :material-code-tags-check:  

        ``` py title="Python"
		nombre = input("Ingrese el nombre del producto: ")
		precio_unitario = float(input("Ingrese el precio unitario del producto: "))
		cantidad = int(input("Ingrese la cantidad de unidades compradas: "))

		costo_total = precio_unitario * cantidad

		print(f"Producto: {nombre}")
		print(f"Precio unitario: {format(precio_unitario, '.2f')}")
		print(f"Cantidad: {cantidad}")
		print("-"*34)
		print(f"Costo total de compra: {format(costo_total, '.2f')}")
		```

		!!! question "¡Para pensar!"
			¿Qué crees que hace la siguiente instrucción `format(precio_unitario, '.2f')`?

	---

