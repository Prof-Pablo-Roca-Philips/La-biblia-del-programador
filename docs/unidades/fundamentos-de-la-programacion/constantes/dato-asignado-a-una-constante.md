title: Dato asignado a una constante

# Dato asignado a una constante

<label class="revision">Rev. 15/01/2024</label>

!!! abstract "Definición"
    Un **dato asignado** a una constante es un valor que se establece al definir la constante y que no puede cambiar durante la ejecución del programa. En otras palabras, una vez que se asigna un valor a una constante, ese valor permanece inmutable, no puede ser modificado posteriormente.
    
    Este dato asignado deberá ser del mismo tipo de dato asociado a la constante.

Por ejemplo, las constantes se utilizan para representar valores que son fijos, como el número pi en matemáticas, o configuraciones que no deben cambiar una vez que el programa está en ejecución, como una cadena de conexión a una base de datos.

``` Go title="Código generalizado"
const float PI = 3.14159;
```

> El dato almacenado en la constante `PI` es el número flotante `3.14159`. 

La constante, mientras exista y sea visible, puede ser accedida y el dato almacenado en ella puede ser leído ¡pero no puede ser modificado!

## Proceso de asignación de un dato a la constante

En la mayoría de los lenguajes de programación, la asignación de un dato a una constante se realiza en el momento de la declaración. Una vez que se asigna el dato, no se puede cambiar. Aquí hay algunos ejemplos en diferentes lenguajes de programación:

``` js title="JavaScript"
const CONSTANTE = "Valor";
```

``` Java title="Java"
final String CONSTANTE = "Valor";
```

``` C++ title="C++"
const std::string CONSTANTE = "Valor";
```

En todos estos ejemplos, si intentas cambiar el valor de CONSTANTE después de su declaración, el compilador o el intérprete te dará un error.

!!! important "¡Para recordar!"
    En Python, no existen las constantes en el sentido estricto. Sin embargo, por convención, los nombres de las variables en mayúsculas se utilizan para indicar que una variable debe tratarse como una constante y no debe modificarse.

    ``` py title="Python"
    CONSTANTE = "Valor"
    ```
    
    Recuerda, aunque hemos llamado a CONSTANTE una "constante", en realidad es una variable en Python. Python no impedirá que cambies el valor de CONSTANTE más adelante en el código. La idea de usar mayúsculas es simplemente para indicar a otros desarrolladores que esta variable no debería cambiarse.

## Proceso de destrucción de una constante

En muchos lenguajes de programación, una vez que se declara una constante, no puede ser destruida o eliminada durante la ejecución del programa. Esto se debe a que las constantes están diseñadas para ser valores inmutables que no cambian.

Entonces, si la constante el global, existirá, será visible y podrá ser accedida desde que sea declarada hasta la finalización de la ejecución del programa.

Por otra parte, si la constante es local, existirá, será visible y podrá ser accedida desde que sea declarada hasta que el flujo del programa salga de la región o parte del código donde fuera declarada.

Sin embargo, en algunos lenguajes de programación puede existir una función que permita su eliminación. Para tal caso, deberás consultar la bibliografía correspondiente del lenguaje de programación en cuestión.

## ¿Qué es la asignación múltiple?

La asignación múltiple de constantes es similar a la asignación múltiple de variables, pero con la diferencia de que los valores asignados no pueden ser modificados después de su declaración. 

En algunos lenguajes de programación, como JavaScript (ES6 y posteriores), puedes declarar múltiples constantes en una sola línea de la siguiente manera:

``` js title="JavaScript"
const a = 1, b = 2, c = 3;
```

> En este código, 1 se asigna a `a`, 2 se asigna a `b`, y 3 se asigna a `c`. Recuerda que, a diferencia de las variables, las constantes no pueden cambiar su valor una vez que se han asignado.

La asignación múltiple puede hacer que el código sea más conciso y legible, pero también puede hacer que el código sea más difícil de entender si se usa de manera excesiva o en situaciones complejas.

Así, puede ser tanto una buena como una mala práctica, dependiendo del contexto y de cómo se utilice.

!!! success "Es una buena práctica cuando:"
    * Mejora la legibilidad del código al agrupar las declaraciones relacionadas.
    * Reduce la cantidad de líneas de código, lo que puede hacer que el código sea más fácil de leer y mantener.
    * Puede ser una mala práctica cuando:

!!! failure ""Es una mala práctica cuando:"
    * Se utiliza en exceso o en situaciones complejas, lo que puede hacer que el código sea más difícil de entender.
    * Se asignan valores a múltiples variables que no están relacionadas, lo que puede confundir a otros desarrolladores que intentan entender el código.

!!! important "¡Para recordar!"
En general, como con muchos aspectos en la programación, la clave está en el equilibrio. Utiliza la asignación múltiple cuando mejore la legibilidad y la comprensión del código, pero evítala cuando pueda causar confusión.
