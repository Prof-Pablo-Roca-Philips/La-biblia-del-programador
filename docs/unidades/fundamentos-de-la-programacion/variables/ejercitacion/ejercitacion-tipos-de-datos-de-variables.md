title: Ejercitación: Tipos de datos de variables

# Ejercicios sobre tipos de datos de variables

<label class="revision">Rev. 11/01/2024</label>

Aquí tienes una serie de ejercicios que te ayudarán a entender cómo el tipo de dato asociado a las variables afecta su comportamiento.

Recuerda que la sintaxis exacta para realizar estos ejercicios dependerá del lenguaje de programación que estés utilizando.

O puedes resolverlos en lenguaje natural o pseudocódigo si lo prefieres. Lo importante es que la solución que plantees se pueda convertir en código, ejecutar como programa en algún lenguaje de programación y que resuelva el problema.

!!! warning "¡Para tener en cuenta!"
    En estos ejercicios emplearemos las comillas simples en nuestro Pseudocódigo para identificar las variables. 
    
    Cuando veas una palabra entre comillas simples, recuerda que no son cadenas de caracteres literales sino identificadores de variables.

1. Crea variables de diferentes tipos de datos que permitan almacenar los siguientes datos:

    * 10
    * 3.14
    * "Hola Mundo!"
    * True

    Elige un nombre coherente para cada variable y almacena el valor correspondiente en cada una de ellas.

    ??? example "Ver solución propuesta" 
        ``` Go title="Pseudocódigo"
        Iniciar
        Declarar la variable 'puntaje' como entero e inicializarla con el valor 10
        Declarar la variable 'pi' como flotante e inicializarla con el valor 3.14
        Declarar la variable 'saludo' como cadena e inicializarla con el valor "Hola Mundo!"
        Declarar la variable 'estoyEstudiandoMucho' como booleana e inicializarla con el valor True
        Fin
        ```
    
    ---

1. Dado el siguiente pseudocódigo pero teniendo en cuenta las operaciones entre tipo de datos:

    ``` Go title="Pseudocódigo"
    Iniciar
    Declarar la variable 'puntaje' como entero e inicializarla con el valor 10
    Declarar la variable 'nombre' como cadena e inicializarla con el texto "Pablo"
    Declarar la variable 'informacion' como cadena de caracteres
    Inicializar 'informacion' con el texto resultante de concatenar ('nombre' + " ha obtenido " + 'puntaje' + " puntos.") para formar una frase completa.
    Imprimir el texto almacenado en 'informacion'
    Fin
    ```

    !!! question "¿Qué sucede y por qué?"
        ??? example "Ver respuesta" 

            ``` Go title="Pseudocódigo" hl_lines="5"
            Iniciar
            Declarar la variable 'puntaje' como entero e inicializarla con el valor 10
            Declarar la variable 'nombre' como cadena e inicializarla con el texto "Pablo"
            Declarar la variable 'informacion' como cadena de caracteres
            Inicializar 'informacion' con el texto resultante de concatenar ('nombre' + " ha obtenido " + 'puntaje' + " puntos.") para formar una frase completa.
            Imprimir el texto almacenado en 'informacion'
            Fin
            ```
            
            > Hay un problema con este pseudocódigo. En la mayoría de los lenguajes de programación, no puedes concatenar directamente una cadena de texto y un número. Necesitarías convertir primero el número a una cadena de texto. Veamos cómo:

            ``` Go title="Pseudocódigo"
            Iniciar
                Declarar la variable 'puntaje' como entero e inicializarla con el valor 10
                Declarar la variable 'nombre' como cadena e inicializarla con el valor "Pablo"
                Declarar la variable 'informacion' como cadena
                Convertir 'puntaje' a cadena
                Inicializar 'informacion' con la cadena concatenada ('nombre' + " ha obtenido " + 'puntaje' + " puntos.")
                Imprimir 'informacion'
            Fin
            ```

            > Ahora si, cuando se ejecute este pseudocódigo, se imprimirá "Pablo ha obtenido 10 puntos.".  

            > Pero hay que observar que al convertir la variable `puntaje` a cadena, el valor 10 deja de ser un número para convertirse en una cadena de caracteres "10" compuesta por el caracter uno seguido del caracter cero. Y se lee "uno cero", no 10. 

            > Por lo tanto, esta es una solución deficiente. Lo correcto sería efectuar una "conversión de tipo", "casteo" o _casting_ de la variable para que se comporte solamente durante la ejecución de la instrucción como si fuera una variable de cadena, pero sin modificar su tipo de dato realmente:

            ``` Go title="Pseudocódigo"
            Iniciar
                Declarar la variable 'puntaje' como entero e inicializarla con el valor 10
                Declarar la variable 'nombre' como cadena e inicializarla con el valor "Pablo"
                Declarar la variable 'informacion' como cadena
                Convertir 'puntaje' a cadena
                Inicializar 'informacion' con la cadena concatenada ('nombre' + " ha obtenido " + ("casteo" del valor de 'puntaje' como cadena) + " puntos.")
                Imprimir 'informacion'
            Fin
            ```

            > Cuando se ejecute este pseudocódigo, también se imprimirá "Pablo ha obtenido 10 puntos.". Pero la variable `puntaje` no sufrirá ninguna alteración en su tipo de dato ni valor almacenado, seguirá conteniendo el valor 10. 

    ---

1. Escribe el pseudocódigo que resuelva como pasar del dato de entrada a la información de salida efectuando las conversiones necesarias:
    
    variable ➞ salida en pantalla

    * dato1 = "10" ➞ salida1 = 10
    * dato2 = 5.45 ➞ salida2 = 5
    * dato3 = 30 ➞ salida3 = "3030"

    ??? example "Ver solución propuesta" 

        La primera solución posible:
        
        ``` Go title="Pseudocódigo"
        Iniciar
        Declarar la variable 'dato1' como cadena e inicializarla con el valor "10"
        Declarar la variable 'dato2' como flotante e inicializarla con el valor 5.45
        Declarar la variable 'dato3' como entero e inicializarla con el valor 30

        Declarar la variable 'salida1' como entero
        Declarar la variable 'salida2' como entero
        Declarar la variable 'salida3' como cadena

        Convertir 'dato1' a entero y almacenar el resultado en 'salida1'
        Convertir 'dato2' a entero y almacenar el resultado en 'salida2'
        Convertir 'dato3' a cadena, concatenar ('dato3' + 'dato3') y almacenar el resultado en 'salida3'

        Imprimir 'salida1'  // Debería imprimir: 10
        Imprimir 'salida2'  // Debería imprimir: 5
        Imprimir 'salida3'  // Debería imprimir: "3030"
        Fin
        ```

        La segunda solución posible:

        ``` Go title="Pseudocódigo"
        Iniciar
        Declarar la variable 'dato1' como cadena e inicializarla con el valor "10"
        Declarar la variable 'dato2' como flotante e inicializarla con el valor 5.45
        Declarar la variable 'dato3' como entero e inicializarla con el valor 30

        Imprimir el "casteo" del valor de 'dato1' como entero  // Debería imprimir: 10
        Imprimir el "casteo" del valor de 'dato2' como entero  // Debería imprimir: 5
        Imprimir (el "casteo" del valor de 'dato3' como cadena + el "casteo" del valor de 'dato3' como cadena)  // Debería imprimir: "3030"
        Fin
        ```

    ---
