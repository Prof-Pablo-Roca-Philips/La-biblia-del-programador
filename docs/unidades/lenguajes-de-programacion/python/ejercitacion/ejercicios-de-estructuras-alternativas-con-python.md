title: Python: ejercicios de estructuras alternativas

1. Ingresa una cadena de caracterespor teclado.  
Si es "Hola" mostrarla en pantalla.

    Ver resultado (1)
    { .annotate }

     1. :material-code-tags-check:  

        ``` py title="Python"
        cadena = input("Ingrese una cadena: ")
        
        if cadena == "Hola":
            print(cadena)
        ```

    ---

1. Escribe un programa que pida al usuario un número entero y muestre por pantalla si es par o impar.

    Ver resultado (1)
    { .annotate }

     1. :material-code-tags-check:  

        ``` py title="Python"
        numero = int(input("Ingrese un número entero: "))

        # El operador % realiza la división y devuelve el resto de esta
        if numero % 2 == 0:
            print("El número es par")

        else:
            print("El número es impar")
        ```
        
    ---

1. Ingresa un número entero por teclado.
Imprime en pantalla si es divisible por 5 o no.

    Ver resultado (1)
    { .annotate }

     1. :material-code-tags-check:  

        ``` py title="Python"
        numero = int(input("Ingrese un número: "))

        # El operador % realiza la división y devuelve el resto de esta
        if numero % 5 == 0:
            print("El número ingresado es divisible por 5")

        else:
            print("El número ingresado no es divisible por 5")  
        ```

    ---  

1. Escribe un programa que pida al usuario dos números y muestre por pantalla su división. 

    !!! warning "¡Atención! Alcance y Limitación"
        Si el divisor es cero  programa debe mostrar un error y no realizar la división.

    Ver resultado (1)
    { .annotate }

     1. :material-code-tags-check:  

        ``` py title="Python"
        dividendo = float(input("Ingrese el dividendo: "))
        divisor = float(input("Ingrese el divisor: "))

        # Controlar que el divisor no sea 0 evitará que la expresión `dividendo / divisor` retorne un error no esperado
        if divisor == 0:
            print("Error: El divisor no puede ser cero")
        
        else:
            print(dividendo / divisor)  
        ```

        > Es importante realizar control de errores que puedan sucederse durante la ejecución del programa para evitar que este falle y se fuerce su finalización de manera abrupta.
    
    --- 
    
1. Ingresa tu edad por teclado.  
Imprime en pantalla si eres mayor o menor de edad.
¡Para recordar! que una persona es mayor de edad al cumplir 18 años.

Respeta la sintaxis de salida como muestran los ejemplos:

    ``` title="Terminal (Entrada/Salida)"
    Ingrese su edad: 21
    Usted es mayor de edad con 21 años.

    Ingrese su edad: 18
    Usted es mayor de edad con 18 años.

    Ingrese su edad: 5
    Usted es menor de edad con 5 años.
    ```

    !!! warning "¡Atención! Alcance y Limitación"
        Asumimos que el usuario siempre va a ingresar una edad válida.
        Para cualquier otro caso, se desestimará el resultado obtenido.

    ??? example "Ver solución propuesta"
        ``` py title="Python"
        '''
        Solicita el ingreso de la edad por teclado. 
        Convierte el dato devuelto por el comando input (siempre devuelve una cadena) en entero. 
        Almacena el dato convertido en la variable edad
        '''
        edad = int(input("Ingrese su edad: "))

        # Evalua si la edad ingresada corresponde a un mayor de edad o a un menor de edad

        # Si la edad es mayor o igual a 18
        if edad >= 18:
            print("Usted es mayor de edad con", edad, "años.")
       
        # Si la edad no es mayor ni igual a 18
        else:
            print("Usted es menor de edad con", edad, "años.")
        ```

    --- 

1. Copia el código del ejercicio anterior y a contiunación modifícalo para que realice lo siguiente:
El programa, luego de almacenar la edad ingresada, debe imprimir en pantalla el resultado correspondiente en el siguiente orden de evaluación:

    * Eres mayor de edad (si has cumplido 18 años)
      * Eres un adulto joven (si no has cumplido 35 años)
      * Eres un adulto mayor (si has cumplido 65 años)
    * Eres menor de edad (si no has cumplido 18 años)
      * Eres un adolescente (si has cumplido 13 años)
      * Eres un niño (si has cumplido 2 años)
      * Eres un bebé (si no has cumplido 2 años)

    ??? example "Ver solución propuesta"
        ``` py title="Python"
        edad = int(input("Ingrese su edad: "))

        if edad >= 18:
            print("Eres mayor de edad")
            if edad < 35:
                print("Eres un adulto joven")
            elif edad >= 65:
                print("Eres un adulto mayor")
        else:
            print("Eres menor de edad")
            if edad >= 13:
                print("Eres un adolescente")
            elif edad >= 2:
                print("Eres un niño")
            else:
                print("Eres un bebé")
        ```

        > Este programa primero pide al usuario que ingrese su edad.  

        > Luego, verifica si la edad es mayor o igual a 18.  
        > Si es así, imprime "Eres mayor de edad" y luego verifica si la edad es menor a 35 o mayor o igual a 65 para imprimir "Eres un adulto joven" o "Eres un adulto mayor" respectivamente.  
        
        > Si la edad es menor a 18, imprime "Eres menor de edad" y luego verifica si la edad es mayor o igual a 13, mayor o igual a 2 o menor a 2 para imprimir "Eres un adolescente", "Eres un niño" o "Eres un bebé" respectivamente.

    ---

1. Escribe un programa que pida al usuario un número entero. 
Si el número es mayor a 10, mostrar si es par o impar.

    !!! warning "¡Atención! Alcance y Limitación"
        recuerda que todo programa siempre debe dar un resultado cada vez que se ejecute.
        No puede haber ejecución sin un resultado asociado. 

    ??? example "Ver solución propuesta"
        ``` py title="Python"
        numero = int(input("Ingrese un número entero: "))
        
        if numero > 10:
        
            if numero % 2 == 0:
                print("El número ingresado es par")
        
            else:
                print("El número ingresado es impar")
        
        else:
            print("El número ingresado no es mayor a 10")
        ```

    ---

1. Escribe un programa que pida al usuario un número entero. 
Si el valor ingresado es 2, 4 o 6 muestra en pantall su valor en letras.

    !!! warning "¡Atención! Alcance y Limitación"
        recuerda que todo programa siempre debe dar un resultado cada vez que se ejecute.
        No puede haber ejecución sin un resultado asociado. 

    ??? example "Ver solución propuesta"
        ``` py title="Python"
        numero = int(input("Ingrese un número entero: "))

        if numero == 2:
            print("El número ingresado es el DOS")
        
        elif numero == 4:
            print("El número ingresado es el CUATRO")
        
        elif numero == 6:
            print("El número ingresado es el SEIS")
        
        else:
            print("El número ingresado no el es 2 ni el 4 ni el 6")
        ```

    ---

1. Ingresa 2 números por teclado.  
Almacénalos en 2 variables.  
Luego, imprime en pantalla cada valor ingresado.  
Luego, imprime en pantalla si el primer número es mayor, igual o menor que el segundo número.

    Por ejemplo, para los valores 4 y 5 la salida sería:

    ``` title="Terminal (Entrada/Salida)"
    Ingrese el primer número: 4
    Ingrese el segundo número: 5

    El valor almacenado en num1 es 4
    El valor almacenado en num2 es 5
    
    4 es menor que 5
    ```
    
    ??? example "Ver solución propuesta"
        ``` py title="Python"
        # Almacena 2 valores ingresados por teclado en 2 variables
        num1 = int(input("Ingrese el primer número: "))
        num2 = int(input("Ingrese el segundo número: "))

        # Se imprimen los valores almacenados en las variables
        print("El valor almacenado en num1 es" , num1) 
        print("El valor almacenado en num2 es" , num2)

        # Estructura alternativa anidada
        if (num1 > num2):
            print(num1 , "es mayor que" , num2)
            
        elif (num2 == num1):
            print(num1 , "es igual a" , num2)

        else:   
            print(num1 , "es menor que" , num2)    
        ```

    ---

1. Escribe un programa que solicite al usuario que ingrese su nombre, su nacionalidad y su edad. 
Si la nacionalidad es argentina y el usuario es mayor de edad, permitirle votar.
Si no, indicarle el motivo por el cual no puede votar.

    ``` title="Terminal (Entrada/Salida)"
    Ingrese su nombre: Pablo
    Ingrese su nacionalidad: argentina
    Ingrese su edad: 45

    Bienvenido Pablo. Puedes pasar a votar.
    ```
    
    ``` title="Terminal (Entrada/Salida)"
    Ingrese su nombre: Pablo
    Ingrese su nacionalidad: argentina 
    Ingrese su edad: 17

    Lo lamento Pablo. No puedes pasar a votar porque no eres mayor de edad.
    ```

    ``` title="Terminal (Entrada/Salida)"
    Ingrese su nombre: Pablo
    Ingrese su nacionalidad: ingles 
    Ingrese su edad: 56
    
    Lo lamento Pablo. No puedes pasar a votar porque no eres de nacionalidad argentina.
    ```

    ``` title="Terminal (Entrada/Salida)"
    Ingrese su nombre: Pablo
    Ingrese su nacionalidad: ingles
    Ingrese su edad: 17
    
    Lo lamento Pablo. No puedes pasar a votar porque no eres de nacionalidad argentina y no eres mayor de edad.
    ```       

    ??? example "Ver solución propuesta"
        ``` py title="Python"
        nombre = input("Ingrese su nombre: ")
        nacionalidad = input("Ingrese su nacionalidad: ")
        edad = int(input("Ingrese su edad: "))

        # La persona es argentina y es mayor de edad
        if nacionalidad == "argentina" and edad >= 18:
            print(f"Bienvenido {nombre}. Puedes pasar a votar.")
        
        else:
            print(f"Lo lamento {nombre}. No puedes pasar a votar porque", end=" ")
            
            # La persona no es argentina ni es mayor de edad
            if nacionalidad != "argentina" and edad < 18:
                print("no eres de nacionalidad argentina ni eres mayor de edad.")
            
            # La persona no es argentina
            elif nacionalidad != "argentina":
                print("no eres de nacionalidad argentina.")
            
            # La persona no es mayor de edad
            else:
                print("no eres mayor de edad.")
        ```

    ---

1. Escribe un programa que solicite al usuario que ingrese un texto.  
El Programa deberá indicar, luego, si el texto está todo en mayúsculas o todo en minúsculas.

    !!! warning "¡Para recordar!"
        Todo programa, siempre, debe devolver un resultado.

    !!! warning "¡Atención! Alcance y Limitación"
    Asumimos que el usuario siempre va a ingresar un texto válido. Es decir, con letras.  
    Para cualquier otro caso, se desestimará el resultado obtenido.
    
    ??? example "Ver solución propuesta"
        ``` py title="Python"
        texto = input("Ingrese un texto: ")

        if texto.isupper():
            print("Todo el texto está en mayúsculas.")
        elif texto.islower():
            print("Todo el texto está en minúsculas.")
        else:
            print("El texto está en mayúsculas y en minúsculas.")
        ```
    
    ---


