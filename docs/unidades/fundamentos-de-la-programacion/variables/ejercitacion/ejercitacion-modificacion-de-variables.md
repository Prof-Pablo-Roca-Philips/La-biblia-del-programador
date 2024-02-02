title: Ejercitación: Modificación de variables

# Ejercicios sobre modificación de variables

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

    Declarar la variable 'saludo'
    Inicializar la variable 'saludo' con el valor de la cadena concatenada ("Hola, mi nombre es " + 'nombre' + " y vivo en " + 'ciudad')
    Fin
    ```

    Complétalo para resolver lo siguiente:

    Cambia el valor de la variable ciudad a otra ciudad.  
    Imprime el valor de ciudad para verificar que ha cambiado.  
    Cambia el valor de saludo para que incluya la nueva ciudad.  
    Cambia el valor de esEstudiante al valor opuesto.  

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

        Declarar la variable 'saludo'
        Inicializar la variable 'saludo' con el valor de la cadena concatenada ("Hola, mi nombre es " + 'nombre' + " y vivo en " + 'ciudad')

        // Cambia el valor de la variable ciudad a otra ciudad
        Asignar el valor "Rosario" a la variable 'ciudad'

        // Imprime el valor de ciudad para verificar que ha cambiado
        Imprimir 'ciudad'

        // Cambia el valor de saludo para que incluya la nueva ciudad
        Declarar la variable 'saludo'
        Asignar a la variable 'saludo' el valor de la cadena concatenada ("Hola, mi nombre es " + 'nombre' + " y vivo en " + 'ciudad')
        Imprimir 'saludo'

        // Cambia el valor de esEstudiante al valor opuesto
        Si 'esEstudiante' es Falso entonces
            Asignar el valor Verdadero a 'esEstudiante'
        Sino
            Asignar el valor Falso a 'esEstudiante'
        FinSi

        Imprimir 'esEstudiante'
        Fin
        ```
        
        > Este pseudocódigo primero declara e inicializa varias variables.  
        > Luego cambia el valor de la variable `ciudad` a "Rosario".  
        > Luego, imprime el nuevo valor de `ciudad`.  
        > Luego, cambia el valor de `saludo` para incluir la nueva ciudad.  
        > Luego, imprime el valor de `saludo`.  
        > Luego, cambia el valor de `esEstudiante` al valor opuesto.  
        > Finalmente, imprime el valor de `esEstudiante`  

    ---
