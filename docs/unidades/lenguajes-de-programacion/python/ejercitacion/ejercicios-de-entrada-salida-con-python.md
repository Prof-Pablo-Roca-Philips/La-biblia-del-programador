title: Python: ejercicios de I/O (entrada/salida)

1. Imprime en pantalla "Hola Mundo!"

    ??? example "Ver solución propuesta"
        ``` py title="Python"
        # Imprime en pantalla "Hola Mundo!"
        print("Hola Mundo!")
        ```

    ---

1. Imprime en pantalla "Hola Mundo!" concatenando ambas palabras y el signo al momento de la impresión.

    ??? example "Ver solución propuesta"
        ``` py title="Python"
        # Imprime en pantalla "Hola Mundo!"
        print("Hola" + " " + "Mundo" + "!")
        ``` 

        !!! question "Para pensar"
            ¿Se lograría el mismo efecto de impresión si en lugar del operador de concatenacion ( + ) se usara la coma ( , )?

            Es decir `print("Hola" , " " , "Mundo" , "!")`

    --- 

1. Almacena en una variable la frase "Hola Mundo!".  
Luego, imprime en pantalla el contenido de la variable.

    ??? example "Ver solución propuesta"
        ``` py title="Python"
        # Almacena "Hola Mundo!" en una variable
        frase = "Hola Mundo!"

        # Imprime en pantalla el contenido de la variable
        print(frase)
        ```

    ---

1. Genera una línea en blanco en la pantalla.

    ??? example "Ver solución propuesta"
        ``` py title="Python"
        print()
        ```

        > La ejecución del comando *print* sin argumentos -los paréntesis vacíos- imprime un salto de línea solamente.

    ---

1. Elije dos números enteros diferentes.  
Imprime la suma entre ambos, pero haciendo el cálculo mental primero.  
No puedes usar ninguna expresión de cálculo en el programa.   

    La salida en pantalla debe ser como se ve en el ejemplo:

    ``` title="Terminal (Entrada/Salida)"
    La suma de 4 y de 7 es 11.
    ```

    ??? example "Ver solución propuesta"
        ``` py title="Python"
        # Imprime en pantalla la suma de 4 y de 7
        print("La suma de 4 y de 7 es 11.")
        ```

    ---

1. Modifica el ejercicio anterior para almacenar los números en dos variables distintas.  
Imprime la suma de ambos números almacenados.  
Ahora si puedes utilizar expresiones de cálculo para realizar la tarea.  

    La salida en pantalla debe ser como se ve en el ejemplo:

    ``` title="Terminal (Entrada/Salida)"
    La suma de 4 y de 7 es 11.
    ```

    ??? example "Ver solución propuesta"
        ``` py title="Python"
        # Inicializa dos variables con los valores enteros
        n1 = 4
        n2 = 7
        
        # Imprime en pantalla la suma de los valores almacenados en n1 y n2
        print("La suma de", n1, "y de", n2, " es ", n1+n2, ".")
        ```

        !!! question "¡Para pensar!"
            ¿Por qué siempre conviene resolver problemas como en este ejercicio y no como en el ejercicio anterior?

            ¿Qué ocurriría en cada caso si se precisan modificar los números?

    ---

1. Ingresa un número entero por teclado.  
Imprímelo en pantalla como el siguiente ejemplo (en este caso, se ingresó un 10):

    ``` title="Terminal (Entrada/Salida)"
    El número ingresado es 10.
    ```

    ??? example "Ver solución propuesta"
        ``` py title="Python"
        # Ingresar un numero por teclado y almacenarlo como entero
        n = int(input("Ingrese un numero: "))
        
        # Imprime en pantalla el número
        print("El numero ingresado es", n)
        ```

        !!! warning "¡Para recordar!"
            El comando *input* recibe un dato por teclado y siempre lo conviente a cadena de caracteres(*str*).

            Si es preciso almacenar dicho dato con otro tipo de dato, será necesario convertirlo antes del almacenamiento.

    ---

1. Ingresa un número entero por teclado.  
Imprime en pantalla el doble del valor ingresado.

    Por ejemplo:

    ``` title="Terminal (Entrada/Salida)"
    Ingrese un numero: 5
    El doble de 5 es 10
    ```

    ??? example "Ver solución propuesta"
        ``` py title="Python"
        # Ingresa un numero por teclado. 
        # Lo convierte a entero. 
        # Lo almacena en una variable.
        n = int(input("Ingrese un numero: ")) # recuerda que el comando *input* siempre devuelve una cadena de texto

        # Imprime en pantalla el doble del valor ingresado
        print("El doble de", n, "es", n*2)
        ```
        
    ---

