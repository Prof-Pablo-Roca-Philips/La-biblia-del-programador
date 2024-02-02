title: Fundamentos de la programación: Ejercitación final

1. Crea una variable que contenga tu nombre y apellido a continuación del código abajo escrito.  
Luego, Imprime un saludo utilizando los datos almacenados en la variable.

    ``` py title="Python"
    print("\033[2J\033[1H") # Limpia la pantalla
    ```
    
    ??? example "Ver solución propuesta"
        ``` py title="Python"
        # Bloque principal del programa
        print("\033[2J\033[1H") # Limpia la pantalla

        nombre = "Pablo Martinez Roca"
        print("Hola", nombre)
        ```

        ``` title="Terminal (Entrada/Salida)"
        Hola Pablo Martinez Roca
        ```

    ---

2. Copia el código del ejercicio anterior y a contiunación realiza lo siguiente:  
 
    Ingresa tu edad por teclado (escribe una oración amigable que le solicite al usuario que ingrese su edad).  
    
    Luego, imprime tu edad en pantalla (escribe una oración amigable que le indique al usuario su edad).

    ??? example "Ver solución propuesta"
        ``` py title="Python"
        # Bloque principal del programa
        print("\033[2J\033[1H") # Limpia la pantalla

        nombre = "Pablo Martinez Roca"
        print("Hola", nombre)

        edad = int(input("Ingresa tu edad: "))

        print("Tienes", edad, "años.")
        ```

        ``` title="Terminal (Entrada/Salida)" 
        Hola Pablo Martinez Roca
        Ingresa tu edad: 45
        Tienes 45 años.
        ```

    ---

1. Copia el código del ejercicio anterior y a contiunación modifícalo para que responda a lo siguiente:  

    Imprime en pantalla: "Hola (tu nombre). Tu edad es (tu edad) años." en un mismo renglón, sin utilizar la coma (,).

    Por ejemplo:

    ``` title="Terminal (Entrada/Salida)"
    Ingresa tu edad: 45
    Hola Pablo Martinez Roca. Tu edad es 45 años.
    ```

    ??? example "Ver solución propuesta"
        ``` py title="Python"
        # Bloque principal del programa
        print("\033[2J\033[1H") # Limpia la pantalla

        nombre = "Pablo Martinez Roca"

        edad = int(input("Ingresa tu edad: "))

        print("Hola " + nombre + ". Tu edad es " + str(edad) + " años.")
        ```

        ``` title="Terminal (Entrada/Salida)" 
        Ingresa tu edad: 45
        Hola Pablo Martinez Roca. Tu edad es 45 años.
        ```
    
    ---

1. Copia aquí el código del ejercicio anterior y a contiunación realiza lo siguiente:  

    Utiliza el siguiente código para simular una pausa: 

    ``` py 
    input("Presiona enter para continuar...")
    ```

    Luego agrega el código del ejercicio 1 que sirve para limpiar la pantalla.  
    
    A continuación, imprime en pantalla si tu edad es par o impar (utiliza el operador módulo ( % ) para calcular el resto de una división).  
    
    La salida en pantalla debe ser exactamente de la siguiente forma: 
    
    ``` title="Terminal (Entrada/Salida)"
    Tu edad es par ( *edad* )
    ```
    
    o 
    
    ``` title="Terminal (Entrada/Salida)"
    Tu edad es impar ( *edad* )
    ```
    
    > Donde \*edad\* es el número almacenado en la variable _edad_, ingresado por teclado.  

    ??? example "Ver solución propuesta"
        ``` py title="Python"
        # Bloque principal del programa
        print("\033[2J\033[1H") # Limpia la pantalla

        nombre = "Pablo Martinez Roca"

        edad = int(input("Ingresa tu edad: "))

        print("Hola " + nombre + ". Tu edad es " + str(edad) + " años.")

        input("Presiona enter para continuar...") # Simula una pausa

        print("\033[2J\033[1H") # Limpia la pantalla

        if edad % 2 == 0:
            print("Tu edad es par (" +  str(edad) + ")")
        else:
            print("Tu edad es impar (" +  str(edad) + ")")
        ```

        ``` title="Terminal (Entrada/Salida)" 
        Ingresa tu edad: 45
        Hola Pablo Martinez Roca. Tu edad es 45 años.

        Presiona enter para continuar...

        (... limpia la pantalla...)

        Tu edad es impar (45)
        ```

    ---

5. Copia aquí el código del ejercicio anterior y a contiunación realiza lo siguiente:  

    Agrega el código que sirve para simular una pausa.  

    Luego agrega el código que sirve para limpiar la pantalla.  

    Ingresa otro número por teclado.  

    Imprime en pantalla si el número es mayor, igual o menor que tu edad, en ese orden de comparación. Arma una oración con el número, tu edad y el resultado de la comparación.  

    ??? example "Ver solución propuesta"
        ``` py title="Python"
        # Bloque principal del programa
        print("\033[2J\033[1H") # Limpia la pantalla

        nombre = "Pablo Martinez Roca"

        edad = int(input("Ingresa tu edad: "))

        print("Hola " + nombre + ". Tu edad es " + str(edad) + " años.")

        input("Presiona enter para continuar...") # Simula una pausa

        print("\033[2J\033[1H") # Limpia la pantalla

        if edad % 2 == 0:
            print("Tu edad es par (" +  str(edad) + ")")
        else:
            print("Tu edad es impar (" +  str(edad) + ")")

        input("Presiona enter para continuar...") # Simula una pausa

        print("\033[2J\033[1H") # Limpia la pantalla

        numero = int(input("Ingresa un número cualquiera: "))

        if numero > edad:
            print("El número (" + str(numero) + ") es mayor a tu edad (" + str(edad) + ").")
        elif numero == edad:
            print("El número (" + str(numero) + ") es igual a tu edad (" + str(edad) + ").")
        else:
            print("El número (" + str(numero) + ") es menor a tu edad (" + str(edad) + ").")
        ```

        ``` title="Terminal (Entrada/Salida)" 
        Ingresa tu edad: 45
        Hola Pablo Martinez Roca. Tu edad es 45 años.

        Presiona enter para continuar...

        (... limpia la pantalla...)

        Tu edad es impar (45)

        Presiona enter para continuar...

        (... limpia la pantalla...)

        Ingresa un número cualquiera : 7
        El número (7) es menor a tu edad (45).
        ```

    ---

6. Copia aquí el código del ejercicio anterior y a contiunación realiza lo siguiente:  

    Modifica el código para que cuando el número sea igual que tu edad, solicite números hasta que se rompa la igualdad.  

    Luego, que imprima si el número es menor o mayor que tu edad armando una oración con el número, tu edad y el resultado de la comparación, tal como has hecho en el ejercicio anterior.

    ??? example "Ver solución propuesta"
        ``` py title="Python"
        # Bloque principal del programa
        print("\033[2J\033[1H") # Limpia la pantalla

        nombre = "Pablo Martinez Roca"

        edad = int(input("Ingresa tu edad: "))

        print("Hola " + nombre + ". Tu edad es " + str(edad) + " años.")

        input("Presiona enter para continuar...") # Simula una pausa

        print("\033[2J\033[1H") # Limpia la pantalla

        if edad % 2 == 0:
            print("Tu edad es par (" +  str(edad) + ")")
        else:
            print("Tu edad es impar (" +  str(edad) + ")")

        input("Presiona enter para continuar...") # Simula una pausa

        print("\033[2J\033[1H") # Limpia la pantalla

        numero = int(input("Ingresa un número cualquiera: "))

        while numero == edad:
            print("El número ingresado (" + str(numero) + ") es igual a tu edad (" + str(edad) + "), pero no pueden ser iguales.")
            numero = int(input("Ingresa un número distinto: "))

        if numero > edad:
            print("El número (" + str(numero) + ") es mayor a tu edad (" + str(edad) + ").")
        else:
            print("El número (" + str(numero) + ") es menor a tu edad (" + str(edad) + ").")
        ```

        ``` title="Terminal (Entrada/Salida)" 
        Ingresa tu edad: 45
        Hola Pablo Martinez Roca. Tu edad es 45 años.

        Presiona enter para continuar...

        (... limpia la pantalla...)

        Tu edad es impar (45)

        Presiona enter para continuar...

        (... limpia la pantalla...)

        Ingresa un número cualquiera: 45

        El número ingresado (45) es igual a tu edad (45), pero no pueden ser iguales.
        Ingresa un número distinto: 45

        El número ingresado (45) es igual a tu edad (45), pero no pueden ser iguales.
        Ingresa un número distinto: 52

        El número (52) es mayor a tu edad (45).
        ```

    ---

7. Copia aquí el código del ejercicio anterior y a contiunación realiza lo siguiente:  

    Agrega el código que sirve para simular una pausa.  

    Luego agrega el código que sirve para limpiar la pantalla.  

    Agrega el código con las estructuras y variables necesarias para imprimir la secuencia de números desde tu edad hasta el segundo número ingresado.  
    Ten en cuenta que puede ser una secuencia ascendente o descendente. 

    Por ejemplo si tu edad es 5 y el segundo número ingresado es 10, la secuencia a imprimir será:

    ``` title="Terminal (Entrada/Salida)"
    5 6 7 8 9 10
    ```

    Pero si tu edad es 10 y el segundo número ingresado es 5, la secuencia a imprimir será:

    ``` title="Terminal (Entrada/Salida)"
    10, 9, 8, 7, 6, 5  
    ```

    ??? example "Ver solución propuesta"
        ``` py title="Python"
        # Bloque principal del programa
        print("\033[2J\033[1H") # Limpia la pantalla

        nombre = "Pablo Martinez Roca"

        edad = int(input("Ingresa tu edad: "))

        print("Hola " + nombre + ". Tu edad es " + str(edad) + " años.")

        input("Presiona enter para continuar...") # Simula una pausa

        print("\033[2J\033[1H") # Limpia la pantalla

        if edad % 2 == 0:
            print("Tu edad es par (" +  str(edad) + ")")
        else:
            print("Tu edad es impar (" +  str(edad) + ")")

        input("Presiona enter para continuar...") # Simula una pausa

        print("\033[2J\033[1H") # Limpia la pantalla

        numero = int(input("Ingresa un número cualquiera: "))

        while numero == edad:
            print("El número ingresado (" + str(numero) + ") es igual a tu edad (" + str(edad) + "), pero no pueden ser iguales.")
            numero = int(input("Ingresa un número distinto: "))

        if numero > edad:
            print("El número (" + str(numero) + ") es mayor a tu edad (" + str(edad) + ").")
        
            paso = 1 # Esta será la variable que controle el incremento o decremento de valores que imprimirá el ciclo

        else:
            print("El número (" + str(numero) + ") es menor a tu edad (" + str(edad) + ").")

            paso = -1 # Esta será la variable que controle el incremento o decremento de valores que imprimirá el ciclo

        input("Presiona enter para continuar...") # Simula una pausa

        print("\033[2J\033[1H") # Limpia la pantalla

        for n in range(edad, numero + paso, paso):
            print(n, end= " ")
        ```

        ``` title="Terminal (Entrada/Salida)" 
        Ingresa tu edad: 45
        Hola Pablo Martinez Roca. Tu edad es 45 años.

        Presiona enter para continuar...

        (... limpia la pantalla...)

        Tu edad es impar (45)

        Presiona enter para continuar...

        (... limpia la pantalla...)

        Ingresa un número cualquiera: 45

        El número ingresado (45) es igual a tu edad (45), pero no pueden ser iguales.
        Ingresa un número distinto: 45

        El número ingresado (45) es igual a tu edad (45), pero no pueden ser iguales.
        Ingresa un número distinto: 52

        El número (52) es mayor a tu edad (45).

        Presiona enter para continuar...

        (... limpia la pantalla...)

        45 46 47 48 49 50 51 52
        ```

    ---