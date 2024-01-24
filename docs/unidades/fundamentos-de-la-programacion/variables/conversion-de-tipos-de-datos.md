title: Conversión de tipos de datos

## Definición

En la programación existen situaciones en las que se necesita cambiar el tipo de dato en otro.

Las variables tienen un tipo de datos asociado que define el tipo de valor que pueden almacenar: números enteros, números de punto flotante, cadenas de caracteres y booleanos, entre otros. A veces es necesario interpretar el tipo de datos de dicho valor como si fuera otro, para realizar ciertas operaciones o para satisfacer requisitos específicos del programa. Esta conversión es necesaria cuando se desean realizar operaciones o comparaciones específicas que requieren tipos de datos compatibles.

!!! info "Definición"
    Para cambiar el tipo de datos de una variable en la mayoría de los lenguajes de programación, puedes utilizar un proceso llamado casting o conversión de tipo. Esto implica interpretar el tipo de datos del valor de una variable como si fuera otro tipo de datos.

Hay dos tipos principales de conversiones de tipo de datos: implícita y explícita.

## Conversión implícita

Ocurre automáticamente cuando el lenguaje de programación realiza la conversión de tipo de datos de forma implícita para mantener la coherencia entre diferentes tipos de datos. 

Por ejemplo, en muchos lenguajes, se puede sumar un entero y un número de punto flotante, y el resultado será un número de punto flotante debido a la conversión implícita:

``` py title="Python"
entero = 5
flotante = 2.5

# La conversión implícita convierte 'entero' a un número de 'punto flotante'
resultado = entero + flotante  

print(resultado)  # imprime 7.5
```

## Conversión explícita

También conocida como **"casting explícito"**, ocurre cuando el programador especifica manualmente el tipo de conversión deseado. 

Esto se hace utilizando funciones o sintaxis específicas proporcionadas por el lenguaje de programación.

### Sintaxis

La sintaxis para realizar un cambio de tipo de datos puede variar dependiendo del lenguaje de programación utilizado. 

En Python, por ejemplo, puedes utilizar las funciones **str()**, **int()**, **float()**, **bool()** para convertir entre tipos de datos:

``` py title="Python"
# Conversión de entero a cadena
numero = 42
cadena = str(numero)
print(type(cadena))  # imprime <class 'str'>

# Conversión de cadena a entero
cadena = "42”
numero = int(cadena)
print(type(numero))  # imprime <class 'int'>

# Conversión de cadena a flotante
cadena = "3.14”
flotante = float(cadena)
print(type(flotante))  # imprime <class 'float'>

# Conversión de entero a booleano
numero = 0
booleano = bool(numero)
print(type(booleano))  # imprime <class 'bool'>
```

En JavaScript, hay funciones como **toString()**, **parseInt()**, **parseFloat()**, **Boolean()** para realizar conversiones de tipo. La variable resultante adquiere el nuevo tipo de dato asignado:

``` js title="Javascript"
// Conversión de número a cadena
var numero = 42
var cadena = numero.toString()
console.log(typeof cadena);  // imprime string

// Conversión de cadena a número entero
var cadena = "42"
var numero = parseInt(cadena)
console.log(typeof numero);  // imprime number
console.log(Number.isInteger(numero));  // imprime true


// Conversión de cadena a número de punto flotante
var cadena = "3.14"
var flotante = parseFloat(cadena)
console.log(typeof flotante);  // imprime number
console.log(Number.isInteger(numero));  // imprime false

// Conversión de valor a booleano
var valor = 0
var booleano = Boolean(valor)
console.log(typeof booleano);  // imprime boolean

```

!!! warning "Para tener en cuenta"
    Es importante destacar que, al igual que con la conversión de tipo de dato, es necesario tener en cuenta las posibles implicaciones y restricciones de la operación de **"casting"**.  
    Algunos lenguajes de programación pueden permitir **"casting"** implícitos entre tipos de datos compatibles, mientras que otros requieren **"casting"** explícitos. 

Estos son solo ejemplos básicos. Los métodos y funciones específicas para realizar el cambio de tipo de datos pueden variar según el lenguaje de programación que estés utilizando. 
Asegúrate de consultar la documentación del lenguaje específico para obtener más información sobre cómo realizar cambios de tipo de datos en ese contexto.

!!! info "Ten en cuenta"
    Existen diversas funciones en cada lenguaje que te ayudarán en la conversión de tipo de datos.

!!! success "¡Importante!"
    Es importante tener en cuenta que, al realizar una conversión de tipo explícita, debes asegurarte de que la operación sea válida y que no se produzca una pérdida de información o resultados inesperados. Por ejemplo, al convertir un número de punto flotante a un entero, se perderá la parte decimal del número.

    Por lo tanto, es fundamental comprender los tipos de datos y las implicaciones de la conversión antes de aplicarla en el código.

    Además, ten en cuenta que las opciones de conversión de tipo pueden variar según el lenguaje de programación que estés utilizando. Asegúrate de consultar la documentación específica del lenguaje para obtener más información sobre cómo realizar cambios de tipo de datos en ese contexto. Algunos lenguajes de programación pueden permitir casts implícitos entre tipos de datos compatibles, mientras que otros requieren casts explícitos. 


### Ejemplos de aplicación

Evaluemos las siguientes conversiones:

``` py title="Python" linenums="1"
valor1 = str(12)
valor2 = "Hola"
valor3 = float("14.34")

print ("Valor 1: ", type(valor1), "   valor:", valor1)
print ("Valor 2: ", type(valor2), "   valor:", valor2)
print ("Valor 3: ", type(valor3), "   valor:", valor3)

valor4 = int("14.34") 
valor5 = int(valor2)
```

!!! question "¿Qué crees que ocurrirá en cada caso?"

Ver resultado (1)
{ .annotate }

1. :material-code-tags-check:  

    ``` title="Terminal (Entrada/Salida)"
    Valor 1:  <class 'str'>    valor: 12
    Valor 2:  <class 'str'>    valor: Hola
    Valor 3:  <class 'float'>    valor: 14.34

    Traceback (most recent call last):
      File " … ", line 9, in <module>
        valor4 = int("14.34")
                 ^^^^^^^^^^^^
    ValueError: invalid literal for int() with base 10: '14.34'

    Traceback (most recent call last):
      File " … ", line 10, in <module>
        valor5 = int(valor2)
                 ^^^^^^^^^^^
    ValueError: invalid literal for int() with base 10: 'Hola'
    ```
    
    > La línea 9 devolverá un error de conversión ya que no es posible convertir un valor de punto flotante en entero, forzando la finalización del programa.

    > Si la línea 9 no devolviera un error, La línea 10 devolverá un error de conversión ya que no es posible convertir una cadena en entero, forzando la finalización del programa.