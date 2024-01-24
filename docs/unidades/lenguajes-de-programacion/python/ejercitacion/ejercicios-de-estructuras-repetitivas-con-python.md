title: Python: ejercicios de estructuras repetitivas

## Ejercicios con _for … in range_

1. Imprime en pantalla la secuencia de números desde el 1 hasta el 10, de 1 en 1, utilizando un ciclo cerrado.

    Por ejemplo:

    ``` title="Terminal (Entrada/Salida)"
    1
    2
    3
    4
    5
    6
    7
    8
    9
    10
    ```
    
    Ver resultado (1)
    { .annotate }

    1. :material-code-tags-check:  

        ``` py title="Python"
        for n in range(1, 11):
            print(n)
        ```
    
        !!! question "¿Por qué aparece un 11 en el código?"
            Recuerda que la sintaxis de esta estructura indica que el parámetro que representa al valor final del ciclo no lo incluye en este.  
            Por lo tanto, como se ve en el ejercicio, el ciclo iterará entre el 1 y el 10.  
            El 11 sería el primer valor que hace falsa la condición que permite la iteración.

            Recuerda también que por iteración entendemos que es el proceso de repetir una estructura de código determinada una cierto número de veces.

    ---

1. Copia el código del ejercicio anterior y a contiunación modifícalo para que realice lo siguiente:  
Imprime en pantalla la misma secuencia, pero de 2 en 2.

    Por ejemplo:

    ``` title="Terminal (Entrada/Salida)"
    1
    3
    5
    7
    9
    ```
    
    Ver resultado (1)
    { .annotate }

    1. :material-code-tags-check:  

        ``` py title="Python"
        for n in range(1, 11, 2):
            print(n)
        ```

    ---

1. Copia el código del ejercicio anterior y a contiunación modifícalo para que realice lo siguiente:  
Inicializa una variable que será utilizada para controlar el paso del ciclo, con el valor 3.
Imprime en pantalla la misma secuencia, utilizando el valor ingresado como paso de número en número.

    Por ejemplo:

    ``` title="Terminal (Entrada/Salida)"
    1
    4
    7
    10
    ```
    
    !!! question "Para pensar"
        ¿Qué nombre le darías a la variable que será utilizada para controlar el paso del ciclo?
        
    Ver resultado (1)
    { .annotate }

    1. :material-code-tags-check:  

        ``` py title="Python"
        paso = 3

        for n in range(1, 11, paso):
            print(n)
        ```

    ---

1. Copia el código del ejercicio anterior y a contiunación modifícalo para que realice lo siguiente:  
Solicita el ingreso de un número entero que le indique el paso al ciclo.
Imprime en pantalla la misma secuencia, utilizando el valor ingresado como paso.

    Por ejemplo:

    ``` title="Terminal (Entrada/Salida)"
    Ingrese un número para el paso: 3 
    
    1
    4
    7
    10
    ```
    
    Ver resultado (1)
    { .annotate }

    1. :material-code-tags-check:  

        ``` py title="Python"
        paso = int(input("Ingrese un número para el paso: "))

        for n in range(1, 11, paso):
            print(n)
        ```

    ---

1. Escribe en pantalla los múltiplos de 3 entre 1 y 100.  
Súmalos y muestra la suma al finalizar el ciclo.

    !!! warning "¡Atención! Alcance y Limitación"
        El valor inicial del ciclo debe ser 1 y el valor inicial debe ser 100.

    Ver resultado (1)
    { .annotate }

    1. :material-code-tags-check:  

        ``` py title="Python"
        # Inicializa la variable acumuladora
        suma = 0

        for n in range(1, 101):
            if n % 3 == 0:
                print(n)    # Imprime en pantalla el múltiplo de 3
                suma += n   # Suma el múltiplo de 3 en la variable acumuladora
                
        print("La suma de los múltiplos de 3 impresos es:", suma)
        ```

    ---

1. Escribe en pantalla la serie de números enteros entre dos números enteros solicitados al usuario.
  

La salida por pantalla debe ser como el ejemplo:

    ``` title="Terminal (Entrada/Salida)"
    Escriba el número inicial de la serie (Debe ser el menor): 1
    Escriba el número final de la serie (Debe ser el mayor): 9
    Escriba el número para indicar el incremento entre cada número de la serie (el paso del ciclo): 5

    Imprimiendo una serie de 2 valores, entre el 1 y el 9 de 5 en 5
    
    El valor número 1 en un ciclo de 5 en 5 es 1
    El valor número 2 en un ciclo de 5 en 5 es 6
    ```

    !!! warning "¡Atención! Alcance y Limitación"
        El problema debe resolverse implementando un ciclo cerrado.
        Asumimos que el primer valor ingresado será menor o igual al segundo valor ingresado.
        Para cualquier otro caso, se desestimará el resultado obtenido.

    !!! tip "¡Una ayudita!"
        Para calcular la cantidad de valores que serán impresos de acuerdo con el valor inicial, el valor final y el valor de paso ingresados, utiliza la siguiente expresión:

        ``` py title="Python"
        ((valor_final - valor_inicial) // paso) + 1
        ```

        > Recuerda que `//` en Python es el operador de división entera. Devuelve el cociente entero, sin decimales.  
        > Si programas en otro lenguaje, deberás utilizar el operador o comando correspondiente para conseguir el mismo resultado.
        
    Ver resultado (1)
    { .annotate }

    1. :material-code-tags-check:  

        ``` py title="Python"
        valor_inicial = int(input("Escriba el número inicial de la serie (Debe ser el menor): "))
        valor_final = int(input("Escriba el número final de la serie (Debe ser el mayor): "))
        paso = int(input("Escriba el número para indicar el incremento entre cada número de la serie (el paso del ciclo): "))

        nro_valor = 1

        print("Imprimiendo una serie de", ((valor_final - valor_inicial) // paso) + 1,"valores, entre el", valor_inicial,"y el",valor_final, "de", paso,"en", paso)

        for valor in range(valor_inicial, valor_final + 1, paso):
            print("El valor número", nro_valor, "en un ciclo de", paso,"en", paso, "es", valor)
            nro_valor +=1
        ```

    ---

1. Ingresa una cadena de caracterespor teclado.  
Simula una línea de texto que se desplaza de izquierda a derecha, a lo largo de 40 caracteres.  
Para ello, debes limpiar la pantalla antes de cada impresión.  
Y luego de imprimir cada línea, el programa deberá esperar 0.1 segundos antes de volver a limpiar la pantalla y e imprimir el texto un caracter corrido hacia la derecha.

    Por ejemplo:

    ``` title="Terminal (Entrada/Salida)"
    Ingrese una cadena de texto: * * * Coma en lo de Charly * * *
    ```

    Al ingresar el texto, limpia la pantalla y muestra el texto por primera vez, pegado a la izquierda del terminal

    ``` title="Terminal (Entrada/Salida)"
    * * * Coma en lo de Charly * * *
    ```

    0.1 segundos más tarde, se limpia la pantalla y se muestra el texto un caracter corrido hacia la derecha:

    ``` title="Terminal (Entrada/Salida)"
     * * * Coma en lo de Charly * * *
    ```

    0.1 segundos más tarde, se limpia la pantalla y se muestra el texto un caracter corrido hacia la derecha:

    ``` title="Terminal (Entrada/Salida)"
      * * * Coma en lo de Charly * * *
    ```

    0.1 segundos más tarde, se limpia la pantalla y se muestra el texto un caracter corrido hacia la derecha:

    ``` title="Terminal (Entrada/Salida)"
       * * * Coma en lo de Charly * * *
    ```

    ⋮

    Finalmente, 0.1 segundos más tarde, se limpia la pantalla y se muestra el texto corrido 40 caracteres hacia la derecha:

    ``` title="Terminal (Entrada/Salida)"
                                        * * * Coma en lo de Charly * * *
    ```
    
    Ver resultado (1)
    { .annotate }

    1. :material-code-tags-check:  

        ``` py title="Python"
        import os, time
    
        texto = input("Ingrese una cadena de texto: ")

        for cant_espacios in range(0, 41):
            os.system("cls")

            print(" " * cant_espacios + texto)
            time.sleep(0.1)
        ```

    ---

## Ejercicios con _while … loop_

1. Imprime en pantalla la secuencia de números desde el 1 hasta el 10, de 1 en 1, utilizando un ciclo abierto.

    Ver resultado (1)
    { .annotate }

    1. :material-code-tags-check:  

        ``` py title="Python"
        # Inicializa las variables para controlar la ejecución del ciclo abierto
        n = 1

        while n <= 10:
            print(n)
            n += 1

    ---

1. Escribe en pantalla la serie de números enteros entre dos números enteros solicitados al usuario.

    !!! warning "¡Atención! Alcance y Limitación"
        El problema debe resolverse implementando un ciclo abierto.
        Asumimos que el primer valor ingresado será menor o igual al segundo valor ingresado.
        Para cualquier otro caso, se desestimará el resultado obtenido.

    Ver resultado (1)
    { .annotate }

    1. :material-code-tags-check:  

        ``` py title="Python"
        valor_inicial = int(input("Escriba el número inicial de la serie (Debe ser el menor): "))
        valor_final = int(input("Escriba el número final de la serie (Debe ser el mayor): "))
        
        print("Imprimiendo la serie de números entre", valor_inicial, "y", valor_final)

        while valor_inicial <= valor_final:
            print(valor_inicial)

            valor_inicial += 1
        ```
        
        > En este caso, el nombre de la variable _valor_inicial_ queda raro respecto de su aplicación. Sin embargo, en estos casos no es necesario desperdiciar recursos en otra variable solamente para que la semántica del programa quede prolija. 

    ---

1. Escribe un programa que solicite al usuario que ingrese números enteros positivos y los muestre por pantalla hasta que ingrese un número negativo cualquiera.  
Al finalizar, el programa debe informar la cantidad de números positivos ingresados.

    !!! warning "¡Atención! Alcance y Limitación"
        Al finalizar el ingreso de números positivos, la respuesta que de el programa debe ser gramaticalmente correcta (singular / plural)

    Ver resultado (1)
    { .annotate }

    1. :material-code-tags-check:  

        ``` py title="Python"
        # Inicializa la variable acumuladora
        n_positivos = 0

        while True:
            n = int(input("Ingrese un número positivo (o un número negativo para finalizar el ingreso): "))

            if n < 0:
                break
            
            print("El número ingresado fue", n)
            n_positivos += 1

        # De acuerdo a la cantidad de números ingresaros, se muestra la respuesta gramaticalmente correcta
        if n_positivos == 0:
            print("No se ingresaron números positivos.")

        elif n_positivos == 1:
            print("Se ingresó 1 número positivo.")

        else:
            print("Se ingresaron", n_positivos, "números positivos.")
        ```
    
    ---

1. Leer números enteros, y contar la cantidad de pares e impares que se han ingresado hasta que se ingrese un número negativo.

    !!! warning "¡Atención! Alcance y Limitación"
        Al finalizar el ingreso de números, la respuesta que de el programa debe ser gramaticalmente correcta (singular / plural)

    Ver resultado (1)
    { .annotate }

    1. :material-code-tags-check:  

        ``` py title="Python"
        # Inicializa las variables acumuladoras
        pares = 0
        impares = 0

        while True:
            n = int(input("Ingrese un número positivo (o un número negativo para finalizar el ingreso): "))
            
            if n < 0:
                break
            
            if n % 2 == 0:
                pares += 1
            
            else:
                impares += 1

        # Imprime en pantalla cuantos números son pares
        if pares == 0:
            print("No hay números pares ingresados.")

        elif pares == 1:
            print("1 número ingresado es par.")

        else:    
            print(pares, "números ingresados son pares.")
            
        # Imprime en pantalla cuantos números son impares
        if impares == 0:
            print("No hay números impares ingresados.")

        elif impares == 1:
            print("1 número ingresado es impar.")

        else:    
            print(impares, "números ingresados son impares.")      
        ```
        
    ---

1. Recordando el siguiente ejercicio:  

    Escribe en pantalla los múltiplos de 3 entre 1 y 100.  
    Súmalos y muestra la suma al finalizar el ciclo.

    ``` py title="Python"
    # Inicializa la variable acumuladora
    suma = 0

    for n in range(1, 101):
        if n % 3 == 0:
            print(n)    # Imprime en pantalla el múltiplo de 3
            suma += n   # Suma el múltiplo de 3 en la variable acumuladora
            
    print("La suma de los múltiplos de 3 impresos es:", suma)
    ```

El primer problema de eficiencia que se presenta aquí es que se repite el código 100 veces, solo para aprovechar un tercio de esas repeticiones.

Podríamos, entonces, pensar en modificar el _paso_ del ciclo para que sea de 3 en 3, pero si el ciclo debe iniciar en 1, entonces los valores serían 1, 4, 7, 10... y ninguno sería múltiplo de 3.

    ``` py title="Python"
    ⋮
    for n in range(1, 101, 3):
        print(n)
    ⋮
    ```

    > Imprime el 1, 4, 7, 10 ...

Entonces, podríamos utilizar una variable para el _paso_ y pensar en algo como esto:

    ``` py title="Python"
    ⋮
    paso = 1

    for n in range(1, 101, paso):
        if n % 3 == 0:
            paso = 3
            print(n) 
    ⋮
    ```

    > n va a valer 1, 2, 3, 6, 9, 12 ...

En la mayoría de los lenguajes, cuando n valga 3, se imprime el 3 y además se modifica la variable _paso_ para que a partir de ahora el ciclo se repita con n de 3 en 3.

Sin embargo, en Python el valor del paso en la función _range()_ se establece cuando se crea el objeto _range_, y no se puede cambiar después. Por lo tanto, aunque cambies el valor de paso a 3 dentro del ciclo, el ciclo seguirá incrementando n en pasos de 1.

Si necesitas un comportamiento donde el paso cambie durante la ejecución, tendrás que implementarlo manualmente usando un ciclo _while_. Entonces, refactoriza el ejercicio utilizando un ciclo abierto.

    !!! warning "¡Atención! Alcance y Limitación"
        El valor inicial a validar en el ciclo debe ser 1.

    Ver resultado (1)
    { .annotate }

    1. :material-code-tags-check:  

        ``` py title="Python"
        # Inicializa la variable acumuladora
        suma = 0

        # Inicializa las variables para controlar la ejecución del ciclo abierto
        n = 1
        paso = 1

        while n < 101:

            if n % 3 == 0:
                paso = 3
                print(n)    # Imprime en pantalla el múltiplo de 3
                suma += n   # Suma el múltiplo de 3 en la variable acumuladora
            
            n += paso
                
        print("La suma de los múltiplos de 3 impresos es:", suma)
        ```

    ---

1. Ingresa números enteros por teclado hasta que se ingrese un cero, el cual no será contabilizado.  
Luego imprime por pantalla la cantidad de números ingresados.  
Luego imprime por pantalla la cantidad de números positivos ingresados.  
Luego imprime por pantalla la cantidad de números negativos ingresados.  
Luego imprime en pantalla cuantos números son pares.  
Luego imprime en pantalla cuantos números son impares.  
Luego imprime en pantalla en una misma línea cuales fueron el menor y el mayor número ingresado.  
Luego, si hay menor y mayor, imprime la secuencia de números entre el mayor y el menor, sin incluirlos, de la siguiente manera:


    ``` title="Terminal (Entrada/Salida)" hl_lines="1-2 8"
    Ingrese un numero o el 0 para terminar el ingreso (no se contabilizará): 8
    Ingrese un numero o el 0 para terminar el ingreso (no se contabilizará): 4
    Ingrese un numero o el 0 para terminar el ingreso (no se contabilizará): 0
    Se han ingresado 2 números.
    Todos han sido positivos. 2 en total.
    2 números son pares.
    No hay números impares.
    El menor valor fue el 4 y el mayor valor fue el 8
    Los números entre el 8 y el 4 son: 7 6 5
    ```
    
    ``` title="Terminal (Entrada/Salida)" hl_lines="1-2 8"
    Ingrese un numero o el 0 para terminar el ingreso (no se contabilizará): 5
    Ingrese un numero o el 0 para terminar el ingreso (no se contabilizará): 4
    Ingrese un numero o el 0 para terminar el ingreso (no se contabilizará): 0
    Se han ingresado 2 números.
    Todos han sido positivos. 2 en total.
    1 números son pares.
    1 números son impares.
    El 4 ha sido el menor valor y el 5 ha sido el mayor valor.
    No hay números entre el mayor y el menor.
    ```

    !!! warning "¡Atención! Limitación"
        No está permitido emplear una variable para almacenar la cantidad total de números ingresados.  
        No está permitido utilizar ninguna variable para almacenar la cantidad de números impares.
        Para imprimir la secuencia de números entre el mayor y el menor solo se permite implementar un ciclo abierto con la condición a la entrada.
        No se permite modificar el valor de las variables que contengan los valores de mayor y menor para imprimir la secuencia.

    Ver resultado (1)
        { .annotate }

        1. :material-code-tags-check:  

            ``` py title="Python"
            #variables acumuladoras
            pos = 0
            neg = 0

            pares = 0

            mayor = False # Identificar inicialmente al mayor como False significa que aun no hay un mayor almacenado 
            menor = False # Identificar inicialmente al menor como False significa que aun no hay un menor almacenado 

            # Solicita el ingreso de numeros hasta que se ingrese el 0
            while True:
                n = int(input("Ingrese un numero o el 0 para terminar el ingreso (no se contabilizará): "))
                
                # Si el numero ingresado es el 0, fuerza la salida del ciclo
                if n == 0:
                    break
                
                # Detecta si el numero ingresado es positivo o negativo
                if n > 0:
                    pos += 1 # pos = pos + 1
                else:
                    neg += 1 # neg = neg + 1

                # Detecta si el numero ingresado es par
                if n % 2 == 0:    
                    pares += 1

                # Detecta si el numero ingresado es el mayor
                if not mayor: 
                    mayor = n
                elif n > mayor:
                    mayor = n

                # Detecta si el numero ingresado es el menor
                if not menor:
                    menor = n 
                if n < menor:
                    menor = n
                    
            # Imprime en pantalla la respuesta adecuada a la cantidad de números ingresados, tanto positivos como negativos
            if pos == 0 and neg == 0:
                print("No se han ingresado números.")

            else:    
                print("Se han ingresado", pos + neg, "números.")
                
                if pos == 0:
                    print("Todos han sido negatidos.", neg, "en total.")
                
                elif neg == 0:
                    print("Todos han sido positivos.", pos, "en total.")
                    
                else:
                    print(pos, "han sido positivos.")
                    print(neg, "han sido negativos.")

                # Imprime en pantalla cuantos números son pares
                if pares > 0:
                    print(pares, "números son pares.")
                else:
                    print("No hay números pares.")
                    
                # Imprime en pantalla cuantos números son impares
                if pares == pos + neg:
                    print("No hay números impares.")
                else:
                    print(pos + neg - pares, "números son impares.")

                # Imprime en pantalla el mayor y el menor numero ingresado solo si hay más de un número ingresado y no son los mismos
                if mayor == menor:
                    print("No hay un valor mayor y otro valor menor ingresados porque", end=" ")
                    if pos + neg == 1:
                        print("solo se ha ingresado un número.")
                    else:
                        print("todos los números ingresados son iguales.")
                else:
                    print("El", menor, "ha sido el menor valor y el", mayor, "ha sido el mayor valor.")
                    
                    numero = mayor - 1
                    
                    if not (numero > menor):
                        print("No hay números entre el mayor y el menor.")
                    
                    else:
                        print("Los números entre el", mayor, "y el", menor, "son: ", end="")
                        while numero > menor:
                            print(numero, end=" ")
                            numero -= 1
            ```

    ---

1. Escribe un programa que solicite un número o una palabra por teclado.
Luego, que indique si es capicúa (se lee igual de izquierda a derecha como de derecha a izquierda) o no.
El programa debe repetirse hasta que no se ingrese ningún número o palabra.

    !!! warning "¡Atención! Alcance y Limitación"
        El programa solo debe evaluar el número o la palabra si tiene al menos 2 caracteres de longitud.

    Por ejemplo:

    ``` title="Terminal (Entrada/Salida)"
    Ingrese el número o la palabra para validar si es capicúa (o solo ENTER para finalizar): 12
    12 no es capicúa!

    Ingrese el número o la palabra para validar si es capicúa (o solo ENTER para finalizar): 1
    El dato ingresado debe tener al menos 2 caracteres para evaluar si es capicúa!

    Ingrese el número o la palabra para validar si es capicúa (o solo ENTER para finalizar): capicua
    capicua no es capicúa!

    Ingrese el número o la palabra para validar si es capicúa (o solo ENTER para finalizar): a
    El dato ingresado debe tener al menos 2 caracteres para evaluar si es capicúa!

    Ingrese el número o la palabra para validar si es capicúa (o solo ENTER para finalizar): neuquen
    neuquen es capicúa!

    Ingrese el número o la palabra para validar si es capicúa (o solo ENTER para finalizar): _
    ⋮
    ```

     Ver resultado (1)
    { .annotate }

    1. :material-code-tags-check:  

        ``` py title="Python"
        # Limpia la pantalla
        print("\033[H\033[J")

        while True:
            # El dato ingresado se convierte a minúsculas para que la comparación de caracteres sea exacta por letra y se almacena como cadena
            dato = input("Ingrese el número o la palabra para validar si es capicúa (o solo presiona ENTER para finalizar): ").lower()
            
            # Si solo se presionó ENTER el comando *input* devolvió una cadena vacía forzando la finalización del ciclo
            if dato == "":
                break

            # Si la cadena ingresada no posee al menos 2 caracteres, no se evaluará si es capicúa
            if len(dato) < 2:
                print("El dato ingresado debe tener al menos 2 caracteres para evaluar si es capicúa!")
                
            else:   
                
                #El ciclo recorrerá la cadena almacenada, caracter por caracter, desde el extremo hacia el centro de la misma.
                for n in range(1, len(dato) + 1):
                    
                    # Si en algún punto de la cadena almacenada el los caracteres a igual distancia de los extremos no coinciden se fuerza la salida del ciclo
                    if dato[n - 1] != dato[-n]:
                        break
                
                # Se evalúa el valor de n respecto de la longitud de la cadena
                # Si no son iguales, significa que en algún punto de la cadena no hubo igualdad de caracteres    
                if n == len(dato):
                    print(dato, "es capicúa!")
                
                else:
                    print(dato, "no es capicúa!")
        ```
        
    ---
