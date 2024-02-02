title: Ejercitación: Alcance de variables

# Ejercicios sobre alcance de variables

<label class="revision">Rev. 11/01/2024</label>

Aquí tienes una serie de ejercicios que te ayudarán a entender cómo el alcance de las variables afecta su accesibilidad y modificación en diferentes partes de tu código.

Recuerda que la sintaxis exacta para realizar estos ejercicios dependerá del lenguaje de programación que estés utilizando.

O puedes resolverlos en lenguaje natural o pseudocódigo si lo prefieres. Lo importante es que la solución que plantees se pueda convertir en código, ejecutar como programa en algún lenguaje de programación y que resuelva el problema.

!!! warning "¡Para tener en cuenta!"
    En estos ejercicios emplearemos las comillas simples en nuestro Pseudocódigo para identificar las variables. 
    
    Cuando veas una palabra entre comillas simples, recuerda que no son cadenas de caracteres literales sino identificadores de variables.

1. Ejercicio con variables locales

    Dado el siguiente pseudocódigo:
    
    ``` Go title="Pseudocódigo"
    Inicio
    Definir función miFuncion()
        Declarar 'variableLocal' como cadena e inicializarla con el texto "Hola, mundo!"
    FinDefinir

    Llamar a miFuncion()

    Imprimir 'variableLocal'
    Fin
    ```

    !!! question "¿Qué sucede y por qué?"
        ??? example "Ver respuesta" 
            ``` Go title="Pseudocódigo" hl_lines="8"
            Inicio
            Definir función miFuncion()
                Declarar 'variableLocal' como cadena e inicializarla con el texto "Hola, mundo!"
            FinDefinir

            Llamar a miFuncion()

            Imprimir 'variableLocal'
            Fin
            ```

            > Este pseudocódigo retornará un error en la línea resaltada al intentar imprimir `variableLocal` fuera de `miFuncion`.

            > Esto se debe a que `variableLocal` es una variable local, lo que significa que solo existe dentro de la función `miFuncion`.  
            > Fuera de esta función, `variableLocal` no está definida, por lo que intentar imprimir `variableLocal` resultará en un error que indica que la variable no está definida.

            > Este concepto se conoce como "alcance de las variables". Las variables locales solo tienen alcance dentro de la función en la que se definen. No se pueden acceder ni modificar fuera de esa función.

    ---
    
1. Ejercicio con variables globales

    Dado el siguiente pseudocódigo:
    
    ``` Go title="Pseudocódigo"
    Inicio
    Declarar 'variableGlobal' como cadena e inicializarla con el texto "Hola, mundo global!"
    
    Definir función miFuncion()
        Imprimir 'variableGlobal'
    FinDefinir

    Llamar a miFuncion()
    Fin
    ```

    !!! question "¿Qué sucede y por qué?"
        ??? example "Ver respuesta" 
            ``` Go title="Pseudocódigo" hl_lines="5"
            Inicio
            Declarar 'variableGlobal' como cadena e inicializarla con el texto "Hola, mundo global!"
            
            Definir función miFuncion()
                Imprimir 'variableGlobal'
            FinDefinir

            Llamar a miFuncion()
            Fin
            ```
        
            > Este pseudocódigo imprime "¡Hola, mundo global!".

            > Esto se debe a que `variableGlobal` es una variable global, lo que significa que su alcance es todo el programa, y no solo la función o el bloque principal en el que se declaró. Por lo tanto, es posible acceder a `variableGlobal` dentro de la función `miFuncion` y cuando se pide imprimir `variableGlobal` dentro de `miFuncion`, se imprime su valor.

            > Este concepto se conoce como "alcance de las variables". Las variables globales tienen alcance en todo el programa y se pueden acceder y modificar desde cualquier parte del código, a diferencia de las variables locales que solo tienen alcance dentro de la función o bloque en el que se definen.

    ---

1. Ejercicio con modificación de variables globales

    Dado el siguiente pseudocódigo:
    
    ``` Go title="Pseudocódigo"
    Inicio
    Declarar 'miVariable' como cadena e inicializarla con "valor inicial"
    
    Definir función modificarVariable()
        Asignar "valor modificado" a 'miVariable'
    FinDefinir

    Llamar a modificarVariable()

    Imprimir 'miVariable'
    Fin
    ```

    !!! question "¿Qué sucede y por qué?"
        ??? example "Ver respuesta" 

            ``` Go title="Pseudocódigo" hl_lines="5 10"
            Inicio
            Declarar 'miVariable' como cadena e inicializarla con "valor inicial"
            
            Definir función modificarVariable()
                Asignar "valor modificado" a 'miVariable'
            FinDefinir

            Llamar a modificarVariable()

            Imprimir 'miVariable'
            Fin
            ```       

            > Este pseudocódigo declara una variable global.
            > Luego define una función que modifica esa variable.
            > Luego llama a la función.
            > Finalmente imprime el valor de la variable "valor modificado".

            > Cuando se declara una variable fuera de cualquier función, se convierte en una variable global. Esto significa que puede ser accedida y modificada desde cualquier parte del código, incluyendo dentro de las funciones.

            > En este caso, `miVariable` es una variable global. Cuando llamamos a la función `modificarVariable`, esta cambia el valor de `miVariable`. Dado que `miVariable` es global, el cambio se refleja en todo el código, no solo dentro de la función. Por lo tanto, cuando imprimimos `miVariable` después de llamar a `modificarVariable`, se imprime el nuevo valor asignado dentro de la función, es decir "valor modificado".

    ---
    
1. Ejercicio con variables locales con el mismo nombre que las variables globales

    Dado el siguiente pseudocódigo:
    
    ``` Go title="Pseudocódigo"
    Inicio
    Declarar 'duplicado' como entero e inicializarla con el valor 10
    
    Definir función funcionDuplicado()
        Declarar 'duplicado' como entero e inicializarla con el valor 20
        Imprimir 'duplicado'
    FinDefinir

    Imprimir 'duplicado'
    Fin
    ```
    
    !!! question "¿Qué sucede y por qué?"
        ??? example "Ver respuesta" 

            ``` Go title="Pseudocódigo" hl_lines="6 9"
            Inicio
            Declarar 'duplicado' como entero e inicializarla con el valor 10
            
            Definir función funcionDuplicado()
                Declarar 'duplicado' como entero e inicializarla con el valor 20
                Imprimir 'duplicado'
            FinDefinir

            Imprimir 'duplicado'
            Fin
            ```

            ``` title="Terminal (Entrada/Salida)"
            20
            10
            ```
    
            > Cuando se ejecuta este pseudocódigo, se espera que la impresión dentro de la función `funcionDuplicado` muestre el valor de la variable local `duplicado`, es decir 20, mientras que la impresión fuera de la función `funcionDuplicado` muestre el valor de la variable global `duplicado`, es decir 10.  
            
            > Esto se debe al alcance de las variables: la variable local `duplicado` solo existe dentro de la función `funcionDuplicado`, mientras que la variable global `duplicado` existe en todo el programa.

            > Si una variable local tiene el mismo nombre que una variable global, la variable local "reemplaza" u "oculta" a la variable global dentro de su ámbito de declaración o de los ámbitos contenidos dentro de su ámbito de declaración. Esto se conoce como "sombreado" o "_shadowing_".  
            > Así, por más que ambas variables se llamen igual, `duplicado`, son variables distintas y sus valores son independientes uno del otro.

    ---
