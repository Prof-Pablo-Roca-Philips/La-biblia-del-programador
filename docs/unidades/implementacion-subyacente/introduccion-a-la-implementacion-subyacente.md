title: Implementación subyacente

## Introducción

La implementación subyacente se refiere a la forma en que se lleva a cabo o se realiza una determinada acción o proceso en un programa.

Es la parte interna o detrás de escena que permite que una funcionalidad o característica se ejecute correctamente.

## Definición

``` title="subyacente" linenums="1" 
Que subyace.
```

``` title="subayer" linenums="1"
Yacer o estar debajo de algo.
Dicho de una cosa: Estar oculta tras otra.
```

En el contexto del desarrollo de software, la implementación subyacente se refiere al código fuente y la lógica que se utiliza para construir una funcionalidad específica. 

Puede variar en diferentes aspectos de la programación como algoritmos generales o específicos como los de aprendizaje automático, estructuras de datos, bibliotecas, o cualquier otro componente necesario para lograr el resultado deseado.

## ¿Cómo se puede aplicar la implementación subyacente en un programa?

¿Cómo la implementación subyacente puede variar en diferentes aspectos de la programación, como algoritmos, estructuras de datos, comunicación en red y algoritmos de aprendizaje automático?

1. Implementación subyacente de un algoritmo de ordenamiento:
    * Ordenamiento de burbuja: usa comparaciones y swaps repetidos para ordenar una lista de elementos.
    * Ordenamiento por inserción: recorre una lista de elementos y los inserta en la posición correcta dentro de una sub lista ordenada.
1. Implementación subyacente de una estructura de datos:
    * Lista enlazada: usa nodos enlazados para almacenar elementos en secuencia, donde cada nodo contiene un valor y una referencia al siguiente nodo.
    * Árbol binario: usa nodos con referencias a un máximo de dos hijos para almacenar elementos jerárquicamente.
1. Implementación subyacente de un algoritmo de aprendizaje automático e inteligencia artificial:
    * Regresión lineal: usa una combinación lineal de características para predecir una variable continua.
    * Árbol de decisión: divide repetidamente el conjunto de datos en función de características para realizar predicciones basadas en reglas de decisión.
    * Redes neuronales: cómo se definen, conectan y actualizan las neuronas para realizar tareas de aprendizaje automático y reconocimiento de patrones.
1. Implementación subyacente de una función criptográfica:
    * Cálculos matemáticos: se refiere a cómo se realizan los cálculos matemáticos necesarios para la encriptación

No te preocupes por toda esta terminología. Es solo para que veas que la implementación subyacente existe en todo programa, de las maneras más diversas. Ya iremos aprendiendo muchas de ellas a lo largo de la materia.

## Ejemplos de implementación subyacente con funciones 

Aquí tienes un ejemplo de implementación subyacente en Python utilizando una función para calcular la suma de dos números:

``` py title="Python"
def suma(num_a, num_b):
    return num_a + num_b

# Ejemplo de uso
a = 5
b = 10
print("La suma de", a, "y", b, "es:", suma(a, b))
```

En este ejemplo, la función suma() es la implementación subyacente. Utiliza el operador + para sumar los valores de num_a y num_b. Luego retorna el resultado.

Al ejecutar este código, obtendrás la salida:

```
La suma de 5 y 10 es: 15
```

---

Aquí tienes un ejemplo de implementación subyacente en Python utilizando una función para calcular el promedio de una lista de números:

``` py title="Python"
def calcular_promedio(datos):
    suma = 0
    cantidad = len(datos)
    for num in datos:
        suma += num
    promedio = suma / cantidad
    return promedio

# Ejemplo de uso
numeros = [5, 10, 15, 20]
promedio = calcular_promedio(numeros)
print("El promedio es:", promedio)
```
En este ejemplo, la función calcular_promedio() es la implementación subyacente. Toma una lista de números como entrada y utiliza un bucle para iterar sobre cada número de la lista. Luego, acumula la suma de todos los números y divide esta suma por la cantidad de números para obtener el promedio.

La implementación subyacente también incluye la declaración de variables, como suma para almacenar la suma parcial de los números y cantidad para contar cuántos números hay en la lista. Finalmente, se retorna el promedio calculado.

Al ejecutar este código, obtendrás la salida:

```
El promedio es: 12.5
```

---

Aquí tienes un ejemplo de implementación subyacente en Python de una función recursiva de cálculo factorial:

``` py title="Python"
def factorial(n):
    if n <= 1: 
        return 1
    else:
        return n * factorial(n - 1)

# Ejemplo de uso
n = 6
print("El factorial de", n, "es:", factorial(n))
```

En este ejemplo, la función factorial() es la implementación subyacente. Utiliza recursión para calcular el factorial de un número n. Se multiplica n por el factorial del número anterior (n - 1) hasta llegar a 1. Luego retorna el resultado.

Al ejecutar este código, obtendrás la salida:

```
El factorial de 6 es: 720
```

Estos son solo ejemplos básicos, pero muestra cómo la **implementación subyacente se refiere al código real y a la lógica que se utiliza para llevar a cabo una tarea específica**.

## Ejemplos de implementación subyacente y abstracción para la representación y estructuras de datos

A partir de la **implementación subyacente** y aplicando el concepto de **abstracción** se puede trabajar con la **representación y estructuras de datos**, de manera abstracta y eficiente, definiendo tipos de datos personalizados que encapsulen los datos y las operaciones relacionadas con ellos, sin pensar en cómo debe ser la lógica de trabajo.

Aquí tienes un ejemplo de una estructura de datos abstracta, en este caso una pila, junto con su implementación subyacente en Python.

La clase **Pila** define una estructura de datos abstracta que representa una pila. La implementación subyacente utiliza una lista (self.items) para almacenar los elementos de la pila. La clase proporciona métodos para realizar operaciones en la pila, como apilar(), desapilar(), esta_vacia() y tamano().

La implementación subyacente utiliza la lista para agregar elementos al final de la pila (apilar()), eliminar elementos del final de la pila (desapilar()), verificar si la pila está vacía (esta_vacia()), y obtener el tamaño actual de la pila (tamano()).

``` py title="Python"
class Pila:
    def __init__(self):
        self.items = []

    def esta_vacia(self):
        return len(self.items) == 0

    def apilar(self, elemento):
        self.items.append(elemento)

    def desapilar(self):
        if self.esta_vacia():
            return None
        return self.items.pop()

    def tamano(self):
        return len(self.items)

pila = Pila() # Ejemplo de uso
pila.apilar(1)
pila.apilar(2)
print("Tamaño de la pila:", pila.tamano())
elemento = pila.desapilar()
print("Elemento desapilado:", elemento)
print("¿La pila está vacía?", pila.esta_vacia())
```

Al ejecutar este código, obtendrás la salida:

```
Tamaño de la pila: 3
Elemento desapilado: 3
¿La pila está vacía? False
```

La clase Pila proporciona una abstracción para trabajar con una pila, ocultando los detalles de implementación subyacentes, como el uso de una lista para almacenar los elementos, permitiendo usar la pila de manera intuitiva y acceder a sus operaciones básicas sin preocuparse por la implementación interna.

---

Aquí tienes un ejemplo de implementación subyacente de un algoritmo de encriptación en Python utilizando el cifrado de sustitución.

La función cifrado_sustitucion() toma un texto como entrada y utiliza un diccionario llamado clave que contiene pares de valores (caracter original, caracter encriptado). El algoritmo de encriptación sustituye cada caracter del texto original por su correspondiente carácter encriptado según la clave.

La implementación subyacente utiliza un bucle para iterar sobre cada caracter del texto. Si el caracter se encuentra en el diccionario clave, se agrega su valor encriptado al resultado. Si el caracter no está en el diccionario (como espacios, signos de puntuación, etc.), se agrega directamente al resultado sin cambios.

``` py title="Python"
def cifrado_sustitucion(texto):
    clave = {
        'a': 'x',
        'b': 'y',
        'c': 'z',
        'd': 'a',
        'e': 'b',
        # Resto del alfabeto...
    }

    resultado = ""

    for caracter in texto:
        if caracter in clave:
            resultado += clave[caracter]
        else:
            resultado += caracter

    return resultado

# Ejemplo de uso
texto_original = "Hola, mundo!"
texto_encriptado = cifrado_sustitucion(texto_original)
print("Texto encriptado:", texto_encriptado)
```

En el ejemplo de uso, se encripta el texto original "Hola, mundo!" utilizando el cifrado de sustitución. El resultado encriptado se imprime en la consola:

```
Texto encriptado: Xyzb, pmtkp!
```

Es importante saber que este ejemplo de cifrado de sustitución también es muy simple y no se utiliza en aplicaciones reales de seguridad, por ser de muy baja confiabilidad y fortaleza contra ataques externos.

