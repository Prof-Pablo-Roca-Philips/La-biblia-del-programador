title: Ejercitación: Uso de variables

# Ejercicios sobre uso de variables

<label class="revision">Rev. 11/01/2024</label>

Aquí tienes una serie de ejercicios para entender las variables en un lenguaje de programación generalizado.

Recuerda que la sintaxis exacta para realizar estos ejercicios dependerá del lenguaje de programación que estés utilizando.

O puedes resolverlos en lenguaje natural o pseudocódigo si lo prefieres. Lo importante es que la solución que plantees se pueda convertir en código, ejecutar como programa en algún lenguaje de programación y que resuelva el problema.

!!! warning "¡Para tener en cuenta!"
    En estos ejercicios emplearemos las comillas simples en nuestro Pseudocódigo para identificar las variables. 
    
    Cuando veas una palabra entre comillas simples, recuerda que no son cadenas de caracteres literales sino identificadores de variables.

1. Dado el siguiente pseudocódigo:

    ``` Go title="Pseudocódigo"
    Inicio
    Declarar la variable 'nombre'
    Inicializar la variable 'nombre' con el valor "Pablo"
    Declarar la variable 'edad'
    Inicializar la variable 'edad' con el valor 10
    Declarar la variable 'ciudad'
    Inicializar la variable 'ciudad' con el valor "CABA"
    Declarar la variable 'esEstudiante'
    Inicializar la variable 'esEstudiante' con el valor Falso
    Fin
    ```

    Complétalo para resolver lo siguiente:

    Imprime el valor de cada variable que declaraste en el primer ejercicio.  
    Crea una nueva variable llamada saludo y asigna una cadena de caracteres que incluya las variables nombre y ciudad en una oración coherente y se imprima.  
    Crea una variable mensaje que combine todas las variables anteriores en una oración coherente y se imprima.  

    ??? example "Ver solución propuesta"
        ``` Go title="Pseudocódigo"
        Inicio
        Declarar la variable 'nombre'
        Inicializar la variable 'nombre' con el valor "Pablo"
        Declarar la variable 'edad'
        Inicializar la variable 'edad' con el valor 10
        Declarar la variable 'ciudad'
        Inicializar la variable 'ciudad' con el valor "CABA"
        Declarar la variable 'esEstudiante'
        Inicializar la variable 'esEstudiante' con el valor Falso

        Imprimir 'nombre'
        Imprimir 'edad'
        Imprimir 'ciudad'
        Imprimir 'esEstudiante'

        Declarar la variable 'saludo'
        Inicializar la variable 'saludo' con el valor de la cadena concatenada ("Hola, mi nombre es " + 'nombre' + " y vivo en " + 'ciudad')

        Declarar la variable 'mensaje'
        Inicializar la variable 'mensaje' con el valor de la cadena concatenada ('saludo' + ". Tengo " + 'edad' + " años. " + "¿Soy estudiante? " + 'esEstudiante')

        Imprimir 'saludo'
        Imprimir 'mensaje'
        Fin
        ```
        
        > Este pseudocódigo primero declara e inicializa varias variables.  
        > Luego imprime el valor de cada una.  
        > Luego crea una nueva variable `saludo` que es una cadena de caracteres, que combina las variables `nombre` y `ciudad` en una oración coherente y la imprime.  
        > Finalmente, crea una variable `mensaje` que combina todas las variables anteriores en una oración coherente y la imprime.
    
    ---
