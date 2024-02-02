title: tipo de dato de una variable

# Tipo de dato de una variable

<label class="revision">Rev. 11/01/2024</label>

!!! abstract "Definición"
	En programación, el tipo de dato de una variable se refiere al tipo de dato o información que puede ser almacenado en ella. 
	
	El tipo de dato de una variable determina cómo la computadora almacena la variable en la memoria central (RAM), cómo interpreta el valor almacenado y qué operaciones se pueden realizar.

!!! important "¡Para recordar!"
	A partir de este momento y por practicidad, cada vez que hablemos de **dato**, dependiendo del contexto, podríamos estar incluyendo a la **información** en la mención. Es decir, que si hablamos de **dato**, en realidad y por contexto hablamos de **dato y/o información**.

El tipo de dato de una variable es una característica que determina qué tipo de valores puede contener una variable. Cada tipo de dato tiene sus propias características y restricciones. Por ejemplo, una variable de tipo entero puede almacenar números enteros (sin decimales), una variable de tipo flotante puede almacenar números con decimales, y una variable de tipo cadena de caracteres puede almacenar texto. 

La importancia del tipo de dato radica en varios aspectos:

1. **Almacenamiento**: Diferentes tipos de datos requieren diferentes cantidades de memoria. Por ejemplo, un entero puede requerir menos memoria que una cadena de caracteres.

2. **Operaciones permitidas**: Las operaciones que puedes realizar con una variable dependen de su tipo de dato. Por ejemplo, puedes sumar dos enteros, pero no puedes sumar una cadena de caracteres y un entero.

3. **Precisión de los datos**: Algunos tipos de datos pueden almacenar información con más precisión que otros. Por ejemplo, un número flotante puede almacenar números con decimales, mientras que un entero no.

4. **Seguridad del tipo**: Al especificar el tipo de dato, puedes evitar errores en tiempo de ejecución. Por ejemplo, si intentas realizar una operación no permitida con un tipo de dato, el compilador o el intérprete te advertirá.

!!! important "¡Para recordar!"
	Es crucial seleccionar el tipo de dato correcto para tus variables para garantizar que tu programa funcione correctamente y de manera eficiente.

## Lenguajes fuertemente tipados

Los lenguajes de programación que requieren especificar el tipo de dato al crear una variable se llaman lenguajes de **tipado estático** o **fuerte**. Algunos ejemplos de estos lenguajes son:

* Java
* C++
* C#
* Rust
* Go
* Swift

En estos lenguajes, **una vez que una variable ha sido declarada con un tipo de dato, no puede cambiar a otro tipo de dato**. Esto puede ayudar a prevenir errores de tipo en tiempo de compilación.

Por ejemplo:

``` Java title="Lenguaje de tipado estático - Java"
int a = 10; // Inicialización de una variable de tipo entero
a = "Hello, World!"; // Esto dará un error de compilación porque se está intentando asignar una cadena a una variable de tipo entero
```

En el ejemplo de Java, el compilador arrojará un error porque se está intentando cambiar el tipo de la variable `a` de `int` a `String`.

## Lenguajes débilmente tipados

Los lenguajes de programación que no requieren especificar el tipo de dato al crear una variable se llaman lenguajes de **tipado dinámico** o **débil**. Algunos ejemplos de estos lenguajes son:

* Python
* JavaScript
* Ruby
* PHP
* Perl

En estos lenguajes, **el tipo de una variable puede cambiar en tiempo de ejecución**, lo que proporciona una mayor flexibilidad pero también puede llevar a errores de tipo más difíciles de detectar.

Por ejemplo:

``` py title="Lenguaje de tipado dinámico - Python"
a = 10  # Inicialización de una variable con un entero
a = "Hello, World!"  # Ahora a es una cadena. En Python, esto es válido porque es un lenguaje de tipado dinámico.
```

En el ejemplo de Python, no hay ningún problema en cambiar el tipo de la variable a de un entero a una cadena. El problema se va a presentar si el dato almacenado no corresponde con el tipo de dato que el programa espera.

!!! important "¡Para recordar!"
	Si el lenguaje de programación es estático o debilmente tipado será necesario asociar el tipo de dato a una variable cuando se esta sea creada.
	
	Si el lenguaje de programación es dinámico o fuertemente tipado el propio lenguaje podrá ser capaz de asociar el tipo de dato a una variable basándose en el dato que se le está asignando, sin necesidad de especificarlo en el código.

## Tipos de dato básicos

Los tipos de dato básicos son:

* **Enteros** (_int_): números pertenecientes a un subconjunto finito de los números enteros. Los enteros son números sin decimales.

	```
	1  2  -3  0
	```

* **Reales** (_float_): números pertenecientes a un subconjunto finito de los números reales. Los números reales constan de una parte entera y una parte decimal, es decir, son números con decimales. También se los conoce como flotantes o de punto flotante.
	
	```
	3.14  2.5  -0.5  5.0  0.09
	```

* **Caracteres** (_char_): son un conjunto finito de caracteres reconocidos por la computadora. Los caracteres son letras, números y símbolos individuales.
  
	```
	alfabéticos: A  B  C  ... Z    a  b  c ... z
	numéricos:   0  1  2  3  4  5  6  7  8  9  0
	símbolos:    +  -  *  /  ^  ,  ;  <  >  $  @
	```

* **Lógicos** (_bool_): también conocidos como booleanos son dos valores lógicos: verdadero (_true_) o falso (_false_).

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

	Esta es la salida en pantalla:

	``` title="Terminal (Entrada/Salida)"
	Valor 1:  True
	Valor 2:  False

	True  AND  False  	=  False
	True  OR  False  	=  True
	NOT  False  		=  True
	```

	!!! question "¿Entiendes todo lo que ocurre, línea tras línea?"

!!! important "¡Para recordar!"
	No todos los tipos de dato existen en todos los lenguajes de programación. Hay lenguajes más ricos que otros en este sentido.  
	Si un tipo de dato no existiese en un determinado lenguaje, será necesario suplantarlo con el tipo de dato que más se asemeje a sus características y restricciones.

## Estructuras de datos

Los tipos de dato vistos anteriormente se suelen denominar elementales o básicos. 

Una estructura de datos es una forma particular de organizar y almacenar datos en una computadora para que puedan ser utilizados de manera eficiente. 

Dependiendo de las necesidades de la aplicación, se pueden utilizar diferentes tipos de estructuras de datos.  
A modo introductorio, enumeraremos las siguientes estructuras de datos solo para mostrarte el amplio universo de posibilidades:

* **Cadena de caracteres (_string_)**: Una secuencia de caracteres. Se utiliza para representar texto.

* **Lista (_list_)**: Una colección ordenada de elementos. Los elementos pueden ser de cualquier tipo y se pueden modificar después de su creación.

* **Lista enlazada (_linked list_)**: Una colección de nodos que juntos representan una secuencia. Cada nodo está compuesto por un valor y una referencia al siguiente nodo en la secuencia.

* **Matriz (_matrix_)**: Una colección bidimensional de números dispuestos en filas y columnas.

* **Tupla (_tuple_)**: Similar a una lista, pero inmutable. Esto significa que una vez creada, no puede ser modificada.

* **Arreglo (_array_)**: Una colección de elementos de un mismo tipo. Los elementos están indexados por un número entero.

* **Diccionario (_dict_)**: Una colección de pares clave-valor. Las claves son únicas dentro de un mismo diccionario.

* **Pila (_stack_)**: Una colección de elementos con dos operaciones principales: push (agregar un elemento al final) y pop (remover el último elemento).

* **Cola (_queue)**: Similar a una pila, pero el elemento removido es el que está al principio.

* **Conjunto (_set_)**: Una colección de elementos únicos, es decir, no contiene duplicados.

* **Grafo (_graph_)**: Un conjunto de nodos y aristas que conectan estos nodos.

* **Árbol (_tree_)**: Un tipo especial de grafo, donde cualquier dos nodos están conectados por exactamente un camino.

La elección de la estructura de datos a menudo afecta la eficiencia de un programa, por lo que es un aspecto importante en el diseño de software.

Por lo general, una estructura de datos está compuesta por elementos de tipos de dato básicos o incluso por otras estructuras de datos, por lo que se la suele denominar como de tipo de dato complejo o tipo de dato estructurado.

Por su extensión y complejidad, este tema merece un capítulo aparte que abordaremos más adelante para estudiarlo en profundidad; o podrías consultar el tema ahora, si quisieras, haciendo clic [aquí](../../estructuras-de-datos/introduccion-a-las-estructuras-de-datos/){:target="_blank"}. 

!!! important "¡Para recordar!"
	La definición de un tipo de dato o de una estructura de datos incluye la definición del conjunto de valores permitidos y las operaciones que se pueden llevar a cabo sobre estos datos.

## tipos de dato que no se pueden representar

Existen ciertos tipos de datos que no se pueden representar exactamente en una computadora. 

Aquí hay algunos ejemplos:

* **Números reales infinitos**: Las computadoras tienen una capacidad de memoria limitada, por lo que no pueden representar números reales con una precisión infinita. Por ejemplo, el número pi o la raíz cuadrada de 2 no se pueden representar exactamente.

* **Números muy grandes o muy pequeños**: Las computadoras tienen límites para los números más grandes y más pequeños que pueden representar. Por ejemplo, en la mayoría de los sistemas, un número entero de 64 bits puede representar valores desde -9,223,372,036,854,775,808 hasta 9,223,372,036,854,775,807.

* **Información continua**: Las computadoras son dispositivos digitales y no pueden representar información continua directamente. Por ejemplo, el sonido y las imágenes se digitalizan para su procesamiento y almacenamiento.

* **Datos ambiguos o inciertos**: Las computadoras requieren precisión y no manejan bien la ambigüedad o la incertidumbre. Los datos que no son claros o que tienen múltiples posibles representaciones pueden ser difíciles de representar.

Estos son solo algunos ejemplos y hay muchas otras situaciones en las que los datos pueden no ser representables en una computadora.

## ¿Cómo determino el tipo de dato asociado a una variable?

En la mayoría de los lenguajes de programación existen comandos que pueden evaluar el tipo de dato de un dato almacenado en un variable. Así, podemos evaluar y manipular las variables de manera correcta durante la ejecución de un programa.

Por ejemplo, en Python podemos utilizar la palabra clave _type_ para conocer el tipo de dato de una variable:

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

**Referencias**

[^1]:
    Un bit es la unidad más básica de información ,o mínima unidad de información, en la computación y la tecnología digital. El nombre es una contracción de _**BI**nary digi**T**_, que en español se traduce como "dígito binario". 
	
	Un bit solo puede tener uno de dos valores: 0 o 1. Estos valores pueden interpretarse como encendido/apagado, verdadero/falso, sí/no, etc., dependiendo del contexto. 
	
	Los bits se agrupan para formar estructuras de datos más grandes, como los bytes[^2] (que constan de 8 bits).

	Las computadoras utilizan el sistema binario (basado en bits) para almacenar y procesar datos, ya que su diseño electrónico les permite manejar fácilmente este sistema de dos estados.	

[^2]:
	Un byte es una unidad de información digital, o mínima unidad de palabra (un caracter), que se compone de 8 bits. Es la unidad de almacenamiento de datos más comúnmente utilizada en la computación y la tecnología digital.

	Cada bit en un byte puede tener uno de dos valores (0 o 1), lo que significa que un byte puede representar 256 (2^8^) valores diferentes. Esto puede ser cualquier cosa desde un número individual hasta un carácter de texto.

	Por ejemplo, en el sistema de codificación ASCII (American Standard Code for Information Interchange), el carácter 'A' se representa con el número 65, que en binario se escribe como 01000001. Este es un ejemplo de cómo se puede representar un carácter como un byte.