title: Introducción a las sentencias de control de flujo

## Introducción

Los programas usan sentencias de control de flujo para ejecutar sentencias condicionalmente, repetir sentencias o saltar a otra parte del programa. 

## ¿Qué es una sentencia de control de flujo?

Cuando se escribe un programa, se están escribiendo sentencias (¡Para recordar! que son instrucciones o declaraciones) en un archivo. Sin sentencias de control de flujo, el programa se ejecuta en el orden en que aparecen escritas las sentencias en el archivo, de izquierda a derecha y de arriba a abajo. 

Para alterar este comportamiento de manera condicional (esto es a partir de validar o no una condición específica) se deben incluir sentencias de control de flujo de control.

Estas sentencias permiten que el flujo del programa ejecute o no ejecute determinadas sentencias, o que ejecute repetidamente una o más sentencias agrupadas en un bloque, o que pueda cambiar su secuencia normal saltando a otra secuencia del programa de manera no secuencial, es decir, saltando a otra sentencia en otra ubicación no consecutiva a la sentencia que se encuentra en ejecución.

Por ejemplo, en el siguiente fragmento de código, la instrucción _si_ ejecuta condicionalmente la salida por pantalla de un mensaje según el resultado que devuelva la expresión que evalúa si el valor almacenado en una variable se encuentra en mayúsculas o no:

``` js title="Código generalizado"
char letra

⋮

letra = input("Ingrese una letra por teclado: ")

si letra está en mayusculas entonces
    print("la letra " + letra + " está en mayúsculas.")
fin si

⋮
```

## Estructuras de control de flujo

!!! success "¡Hablemos con propiedad!"
    Si bien en unidades pasadas hablamos de **sentencias de control de flujo**, lo correcto es llamarlas **estructuras de control de flujo** puesto que si bien son sentencias, en realidad, estas sentencias se encuentran estructuradas, agrupadas, con cierta coherencia para que se comporten de determinada manera a lo largo de la ejecución del programa.

Las estructuras de control de flujo modifican la ejecución secuencial de las sentencias que forman un programa.

### Estructura de selección

La estructura de selección (control de flujo condicional), también conocida como estructura de toma de decisiones o _decision making_, se usa para decidir el control de flujo, basadas en una condición, usando la cláusula _if_.

Se utilizan para ejecutar selectivamente un conjunto de sentencias, según se satisfaga o no una condición.

* control de flujo condicional _if_ 

Se utiliza para ejecutar un bloque de código, solo si la condición es verdadera. Si la condición es falsa, no ejecuta ningún otro bloque relacionado al if y el programa continúa con la siguiente instrucción.
 
    ``` js title="Código generalizado" 
    if (x > 10) {
        
        // el bloque de código que contiene esta rama de la estructura alternativa se ejecuta solo si x es mayor a 10
        print ("El número es mayor a 10.")
    
    }
    ```

Ejercicio de aplicación:

    Ingresar un número entero por teclado.  
    Luego imprimir en pantalla si el número ingresado es positivo.

    Ver resultado (1)
        { .annotate }

        1. :material-code-tags-check:  
   
        ``` py title="Python"
        n = int(input("ingrese un numero: ")) # el comando *input* siempre devuelve una cadena. Es preciso convertirla a entero.

        if n > 0:
            print(n, "es positivo.") # usamos la coma ( , ) en lugar del operador de concatenación ( + ) 
        ```
        
        > En este ejercicio, al imprimir utilizando la coma en lugar del operador de concatenación, lo que se está haciendo es imprimir un conjunto de argumentos en lugar de armar una cadena de texto.  
        > Esto permite "mezclar" distintos tipos de dato entre si, porque en realidad no se está mezclando nada.  
        > Si en lugar de utilizar la coma se hubiera utilizado el operador de concatenación, se tendría que haber compatibilizado todos los tipos de dato como cadenas:

        ``` py title="Python"
        print(str(n) + " es positivo.")
        ```

* control de flujo condicional _if … else_ 

Se utiliza para ejecutar un bloque de código si la condición es verdadera y otro bloque si la condición es falsa.

    ``` js title="Código generalizado" 
    if (x > 10) {
    
        // el bloque de código que contiene esta rama de la estructura alternativa se ejecuta solo si x es mayor a 10
        print ("El número es mayor a 10.")
    
    } else {
    
        // el bloque de código que contiene esta rama de la estructura alternativa se ejecuta solo si x NO es mayor a 10
        print ("El número no es mayor a 10.")
    
    }
    ```

Ejercicio de aplicación:

    Ingresar un número entero por teclado.  
    Luego imprimir en pantalla si el número ingresado es positivo o negativo.

    !!! warning "¡Atención! Limitación"
        En este ejercicio vamos a descartar el cero. No lo tenemos en cuenta.

    Ver resultado (1)
        { .annotate }

        1. :material-code-tags-check:  
   
        ``` py title="Python"
        n = int(input("ingrese un numero: ")) # el comando *input* siempre devuelve una cadena. Es preciso convertirla a entero.

        if n > 0:
            print(n, "es positivo.") # usamos la coma ( , ) en lugar del operador de concatenación ( + ) 
        
        else
            print(n, "es negativo.") # usamos la coma ( , ) en lugar del operador de concatenación ( + ) 
        ```
        

* control de flujo condicional _if … else_ anidada

Aquí, se utilizan múltiples _if … else_ para decidir el flujo de control, respetando la lógica arriba explicada.

    ``` js title="Código generalizado" 
    if (x > 10) {

        // el bloque de código que contiene esta rama de la estructura alternativa se ejecuta solo si x es mayor a 10
        print ("El número es mayor a 10.")
    
    } else if (x == 10) {
    
        // el bloque de código que contiene esta rama de la estructura alternativa se ejecuta solo si x es igual a 10
        print ("El número es igual a 10.")
    
    } else {
    
        // el bloque de código que contiene esta rama de la estructura alternativa se ejecuta solo si x NO es mayor y NO es igual a 10
        print ("El número no es mayor y no es igual a 10. Es menor.")
    
    }
    ```

!!! important "¡Para recordar!"
    Dependiendo del lenguaje de programación, la estructura _else if_ podría escribirse diferente, como _elseif_ o _elif_ por ejemplo.

Ejercicio de aplicación:

    Ingresar un número entero por teclado.  
    Luego imprimir en pantalla si el número ingresado es positivo, negativo o neutro.

    Ver resultado (1)
        { .annotate }

        1. :material-code-tags-check:  
   
        ``` py title="Python"
        n = int(input("ingrese un numero: ")) # el comando *input* siempre devuelve una cadena. Es preciso convertirla a entero.

        if n > 0:
            print(n, "es positivo.") # usamos la coma ( , ) en lugar del operador de concatenación ( + ) 
       
        elif n < 0:
            print(n, "es negativo.") # usamos la coma ( , ) en lugar del operador de concatenación ( + ) 
        
        else:
            print(n, "es neutro.") # usamos la coma ( , ) en lugar del operador de concatenación ( + ) 
        ```

### Diferencia entre _if_ como expresión vs. _if_ como sentencia

!!! success "¡Importante!"
    La diferencia entre **expresiones** y **sentencias** es que las **expresiones devuelven un valor** y, por lo tanto, se pueden usar en lugares donde se requieren valores, mientras que las **sentencias son instrucciones o bloque de instrucciones que se ejecutan en un programa**, pero **en si, no devuelven ningún valor si no a través de una expresión contenida en la sentencia**. 

Así, el resultado de una expresión se puede usar como valor para almacenar en una variable, como argumento para pasar a una función, o como operando para realizar alguna operación con operadores; mientras que las sentencias no devuelven ningún resultado .

Si la estructura _if_ se utiliza como expresión, podrías hacer esto: 

``` js title="Código generalizado"
const miValor = if condición { valor1 } else { valor2 }
```

Si la estructura _if_ se utiliza como sentencia, podrías hacer esto: 

``` js title="Código generalizado"
int miValor
if condición {
    miValor = valor1
} else {
    miValor = valor2
}
```

* control de flujo condicional _switch_

Se usa para decidir el control de flujo, basadas en casos, usando la cláusula switch. 

la sentencia _switch_ también entra en esta categoría, donde la selección se realiza utilizando las declaraciones de case y default. Es una manera alternativa a la sentencia if-else anidada para evaluar decisiones múltiples.  
Esta sentencia se combina con sentencias de interrupción o salto y sentencias etiquetadas, como veremos más adelante.

Cuando el valor de opcion no se corresponde con ningún case y existe el caso default, se ejecuta el bloque correspondiente al caso default.

Las declaraciones _case_ y _default_ no interrumpen por sí mismas el flujo de control del programa. Por ello, es necesario una sentencia de salto (normalmente la instrucción _break_).

Si se omite el _break_ al final de un caso, el programa pasa a ejecutar las sentencias de los casos siguientes hasta encontrar un _break_ o hasta el final del _switch_.

Se recomienda situar el caso _default_ en último lugar e incluir siempre un _break_ al final de su secuencia de sentencias asociada.

    ``` js title="Código generalizado"
    int opcion = 2;
    
    switch (opcion) {
        case 1:
            print("Esta rama de flujo del programa se recorre cuando se elige la opción 1.");
            break;

        case 2:
            print("Esta rama de flujo del programa se recorre cuando se elige la opción 2.");

        default:
            print("Esta rama de flujo del programa se recorre por defecto si no hay una opción case que concuerde.");
            break;   
    }  	
    ```

    > No pueden existir dos casos iguales en un mismo switch (un mismo caso, sí puede ocurrir en distintos switch anidados).

!!! important "¡Para recordar!"
    Una sentencia switch es más eficiente que una escalera de if-else anidada.

#### Sentencias de iteración

Se utilizan para seguir ejecutando una sentencia o un bloque de sentencias mientras se cumpla o hasta que se cumpla una cierta condición. 

también conocidas como sentencias de bucle o looping, se utiliza para repetir el mismo bloque de código una y otra vez hasta un número determinado de veces o basado en la veracidad o falsedad de una condición. Existen tres tipos de sentencias de iteración:

* bucle o ciclo cerrado _for … next_ 

Se utiliza para repetir un bloque de código un número específico de veces, en función de la veracidad de una condición, simple o compuesta.

    ``` js title="Código generalizado"
    for (i = 1; i <= 5; i++) {
        print (i);
    } // la llave cerrada representa next i
    ```

* bucle o ciclo abierto con la condición a la entrada _while … loop_ | _until … loop_ 

Se utiliza para repetir un bloque de código mientras o hasta que se cumpla una condición.

La comprobación de la condición se realiza antes de la ejecución del bloque de sentencias, y por tanto puede que éste no se ejecute ni una vez.

    ``` js title="Código generalizado"
    j = 0;
    while (j < 5) {

        // este bloque de código se va a repetir mientras j sea menor a 5
        print (j);
        j++;

    } // la llave cerrada representa loop

    // El ejemplo de arriba tiene el mismo comportamiento que el de abajo. 
    // La diferencia está en como se arma la condición para que el ciclo 
    // se repita bajo los mismos parámetros de evaluación.

    j = 0;
    until (j >= 5) {
        print (j);
        j++;
    } // la llave cerrada representa loop    
    ```

* bucle o ciclo abierto con la condición a la salida _do … loop while_ | _do … loop until_

Se utiliza para repetir un bloque de código mientras o hasta que se cumpla una condición, simple o compuesta.

La comprobación de la condición se realiza después de la ejecución del bloque de sentencias, y por tanto éste siempre se ejecuta al menos una vez.

    ``` js title="Código generalizado"
    do {
        n = input("Ingrese un número o 0 para terminar");
    } loop while (n != 0)

    // El ejemplo de arriba tiene el mismo comportamiento que el de abajo. 
    // La diferencia está en como se arma la condición para que el ciclo 
    // se repita bajo los mismos parámetros de evaluación.

    do {
        n = input("Ingrese un número o 0 para terminar");
    } loop until (n == 0)
    ```

    > Como se puede observar en ambos ciclos abiertos, la palabra reservada `while` está de un color mientras que `until` no lo está.
    > Esto se debe a que no es común encontrar disponible la segunda opción en la mayoría de los lenguajes.  
    > Sin embargo, corresponde informar acerca de su existencia ya que en caso de existir, es válido utilizarla si con ella se mejora la formulación de la condición de repitancia del ciclo.

### Estrutura de manejo de excepciones

## Sentencias de control de flujo

Ahora si podemos hablar de un último grupo de instrucciones que si pueden llamarse **sentencias de control de flujo**:

### Sentencias de salto

Se utilizan para alterar de manera incondicional el orden de ejecución de las sentencias de un programa. Sólo deberían utilizarse con el fin de simplificar o mejorar los algoritmos.

## Expresiones condicionales _if … else_ y el operador ternario

Una expresión condicional que no sea una declaración podría referirse al uso de operadores condicionales que evalúan una condición y retornan un valor en lugar de controlar el flujo de ejecución.

Entonces, se utiliza la estructura **_if … else_ como expresión** para producir un valor basado en una condición. Esto puede ser útil para asignaciones concisas u operaciones condicionales en una línea de código, ya que permite devolver **un valor específico basado en una condición**, dependiendo de si esta condición es verdadera o falsa. 

El **operador ternario**, también conocido como operador condicional, es un operador utilizado en muchos lenguajes de programación, como JavaScript, para evaluar una condición y seleccionar uno de dos valores posibles, dependiendo del resultado de esa condición. 

El operador ternario se llama "ternario" porque toma tres operandos: 
    * la condición a evaluar, 
    * el valor que se devuelve si la condición es verdadera, y 
    * el valor que se devuelve si la condición es falsa.

En otras palabras, el operador ternario permite asignar un valor o ejecutar una expresión basándose en una condición de una manera más concisa.

Sin embargo, es importante no abusar de su uso excesivo para mantener la claridad y la legibilidad del código.

!!! info "¡Importante!"
    Es importante mencionar que la sintaxis y la manera de utilizar las expresiones condicionales pueden variar según el lenguaje de programación.

    Cada lenguaje tiene su propia sintaxis y convenciones para expresiones condicionales. Por lo tanto, siempre es recomendable consultar la documentación específica del lenguaje para obtener información detallada sobre las expresiones condicionales disponibles en ese contexto.

A continuación, veamos algunos ejemplos en varios lenguajes:

``` js title="JavaScript: sintaxis"
condición ? valor_si_verdadero : valor_si_falso
```
> Aquí, condición es una expresión booleana que se evalúa. Si la condición es verdadera, se devuelve  valor_si_verdadero. Si la condición es falsa, se devuelve valor_si_falso.

``` js title="JavaScript"
const edad = 25
const es_adulto = edad >= 18 ? "Es adulto" : "No es adulto"
console.log(es_adulto)  // Salida: Es adulto
```

> En este ejemplo, se evalúa la condición **edad >= 18**. Si esta es verdadera (lo cual es cierto en este caso), se devuelve la cadena "Es adulto". De lo contrario, se hubiera devuelto la cadena "No es adulto". El valor devuelto es asignado a la variable **es_adulto**. Luego, el valor almacenado en esta se imprime en la consola.

Recreemos el mismo programa pero en otro lenguaje de programación cuya sintaxis se escribe diferente:

``` py title="Python: sintaxis"
valor_si_verdadero if condición else valor_si_falso
```
> Aquí, la expresión que contiene a la instrucción _if_ evalúa la condición. Si la condición es verdadera, se devuelve el valor especificado antes de la instrucción _if_. Si la condición es falsa, se devuelve el valor especificado después de la instrucción else.

``` py title="Python"
edad = 25
es_adulto = "Es adulto" if edad >= 18  else "No es adulto"
print(es_adulto)  // Salida: Es adulto
```

Volvamos al ejercicio de aplicación que hicimos hace un tiempo atrás:

    Ingresar un número entero por teclado.  
    Luego imprimir en pantalla si el número ingresado es positivo, negativo o neutro.

    ``` py title="Python"
    n = int(input("ingrese un numero: ")) # el comando *input* siempre devuelve una cadena. Es preciso convertirla a entero.

    if n > 0:
        print(n, "es positivo.") # usamos la coma ( , ) en lugar del operador de concatenación ( + ) 
    
    elif n < 0:
        print(n, "es negativo.") # usamos la coma ( , ) en lugar del operador de concatenación ( + ) 
    
    else:
        print(n, "es neutro.") # usamos la coma ( , ) en lugar del operador de concatenación ( + ) 
    ```

Si resolviésemos este ejercicio implementando el operador ternario, sería mucho mas corto.

¡Inténtalo!

    Ver resultado (1)
        { .annotate }

        1. :material-code-tags-check:  
   
        ``` py title="Python"
        n = int(input("ingrese un numero: ")) # el comando *input* siempre devuelve una cadena. Es preciso convertirla a entero.

        print(n, "es", "positivo" if n > 0 else ("negativo" if n < 0 else "neutro"))
        ```

        !!! question "¡Para analizar!"
            ¿Cuántos operadores ternarios se utilizaron en el ejercicio? 
            
            ¿Puedes identificarlo o identificarlos si fueron más de uno?

## Expresiones condicionales _if … else_ y el operador lógico _OR_

En algunos lenguajes, como **JavaScript**, además del operador ternario existe otra forma de realizar una estructura condicional como expresión, conocida como estructura alternativa u operador lógico _OR_. En JavaScript se emplea con doble barra vertical ( || ). 

Esta estructura se puede utilizar para asignar un valor basado en una condición sin necesidad de usar un bloque if o el operador ternario.

Esta estructura alternativa se basa en la evaluación de cortocircuito del operador lógico _OR_.   
El operador OR devuelve el primer valor verdadero que encuentre en una serie de condiciones representadas como expresiones evaluadas en orden. Si todas las expresiones son falsas, devuelve el último valor.

``` js title="JavaScript: sintaxis"
condición_1 (|| … condición_2 || … condición_n) || valor_si_falso
```

> Aquí, condición_1 es una expresión que se evalúa. Si la expresión es verdadera, se devuelve el valor de la condición_1. Pero si la expresión es falsa, se devuelve el valor_si_falso.

!!! info "Atención"
    Esta estructura alternativa puede ser útil cuando se desea asignar un valor predeterminado o un valor alternativo en caso de que una variable sea falsa o no esté definida. 
    
    Sin embargo, es importante tener en cuenta que este enfoque solo es adecuado para casos en los que se desea asignar un valor específico o predeterminado y no para realizar acciones más complejas como ejecutar bloques de código.

### Ejemplos

Las siguientes expresiones condicionales permiten asignar un valor o realizar operaciones basadas en una condición en una única línea de código sin afectar directamente el flujo de ejecución.

``` js title="JavaScript: asignación de un valor predeterminado"
const nombre = ''
const nombre_valido = nombre || 'Nombre desconocido'
console.log(nombre_valido); // Salida: 'Nombre desconocido'
```

> En este ejemplo, la variable nombre se evalúa en un **contexto booleano**. Si el valor de nombre es una cadena vacía (falso), null o indefinido, se devuelve el valor *Nombre desconocido*. Si nombre tuviera un valor distinto de una cadena vacía (verdadero), se devolvería el valor almacenado en nombre.

``` js title="JavaScript: validación de argumentos de una función"
function saludar(nombre) {
    nombre = nombre || 'Invitado'
    console.log(`¡Hola, ${nombre}!`)
}

saludar(); // Salida: ¡Hola, Invitado!
saludar('Pedro'); // Salida: ¡Hola, Pedro!
```

> En este ejemplo, si no se proporciona un argumento al parámetro nombre al llamar a la función saludar(), se asignará automáticamente el valor 'Invitado'.

!!! info "Para saber un poco mas"
    &#96`${nombre}`&#96 : El uso de las comillas invertidas ( ` ) con el signo pesos seguido de una variable encerrada entre llaves permite reemplazar dicha variable por su valor almacenado dentro de una cadena de texto.

``` js title="JavaScript: uso en una expresión booleana"
const es_valido = respuesta === ‘si' || respuesta === 'yes'
```

> En este ejemplo, *es_valido* se evalúa como true si la variable respuesta tiene el valor si o yes.

``` js title="JavaScript : selección de valor basado en condiciones"
const mensaje = (estado === 'error' || estado === 'fallido') ? 'Ha ocurrido un error.' : 'Operación exitosa.'
```

> Aquí, el valor de mensaje se selecciona dependiendo del valor de estado. Si estado es igual a error o fallido, se asigna el mensaje de error. De lo contrario, se asigna el mensaje de operación exitosa.

