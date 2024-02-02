title: Python: ejercicios de listas

# Ejercitación de listas con Python

1. Escribe un programa que solicite una palabra por teclado.  
Luego, convierte los caracteres de la palabra ingresada en una lista de elementos.  
A continuación, imprime en pantalla la lista.  
Por último, imprime en pantalla todos los elementos de la lista, un elemento por renglón.

    ``` title="Terminal (Entrada/Salida)"
    Ingrese una palabra: palabra
    ['p', 'a', 'l', 'a', 'b', 'r', 'a']
    p
    a
    l
    a
    b
    r
    a
    ```
    
    ??? example "Ver solución propuesta"
        ``` py title="Python"
        palabra = input("Ingrese una palabra: ")
        lista = list(palabra)
        print(lista)
        for elemento in lista:
            print(elemento)
        ```

    ---

1. Escribe un programa que cree una lista con los siguientes elementos: blanco, rojo, violeta, azul, gris, verde y amarillo.

    ??? example "Ver solución propuesta"
        ``` py title="Python"
        colores = ["blanco", "rojo", "violeta", "azul", "gris", "verde", "amarillo"]
        ```

    ---

1. Copia aquí el código del ejercicio anterior y a contiunación realiza lo siguiente:  
Imprime en pantalla cuantos elementos contiene la lista, con el siguiente formato y utilizando _f-strings_ (si no ¡Para recordar!s que son las _f-strings_ puedes repasarlo [aquí](../../estructuras-de-datos/cadenas-de-caracteres/uso-de-cadenas-de-caracteres-en-python/#uso-de-f-strings)).

    ``` title="Terminal (Entrada/Salida)"
    La lista contiene 7 elementos.
    ```

    ??? example "Ver solución propuesta"
        ``` py title="Python"
        print(f"La lista contiene {len(colores)} elementos.")
        ```

    ---

1. Copia aquí el código del ejercicio anterior y a contiunación realiza lo siguiente:
    1. Agrega el color "lila" al final de la lista
    2. Agrega el color "Celeste" insertándolo en la posición 4 (piensa, no es un reemplazo y hablamos de ubicación)
    3. Agrega el color "Marrón" insertándolo luego de "azul" (debes encontrar la posición de "azul" primero)
    4. Por último, imprime la nueva longitud de la lista con la misma salida que el ejercicio anterior, pero empleando el método _format()_ (si no ¡Para recordar!s el método _format()_ puedes repasarlo [aquí](../../estructuras-de-datos/cadenas-de-caracteres/uso-de-cadenas-de-caracteres-en-python/#uso-del-metodo-format)).

    Imprime la lista luego de cada instrucción para visualizar como se va modificando.
    
    ``` title="Terminal (Entrada/Salida)"
    ⋮
    ['blanco', 'rojo', 'violeta', 'azul', 'gris', 'verde', 'amarillo', 'lila']
    ['blanco', 'rojo', 'violeta', 'celeste', 'azul', 'gris', 'verde', 'amarillo', 'lila']
    ['blanco', 'rojo', 'violeta', 'celeste', 'azul', 'Marrón', 'gris', 'verde', 'amarillo', 'lila']
    La lista contiene 10 elementos.
    ```
    
    ??? example "Ver solución propuesta"
        ``` py title="Python"
        colores = ["blanco", "rojo", "violeta", "azul", "gris", "verde", "amarillo"]

        print(f"La lista contiene {len(colores)} elementos.")

        colores.append("lila")
        print(colores)

        colores.insert(3, "celeste")
        print(colores)

        posicion = colores.index("azul")
        colores.insert((posicion + 1), "Marrón")
        print(colores)

        print("La lista contiene {} elementos.".format(len(colores)))
        ```

    ---

1. Escribe un programa que sume las siguientes listas y las muestre en pantalla:

    ``` title="Terminal (Entrada/Salida)"
    lista1 = [ 1, 2, 3, 4, 5 ]
    lista2 = [ 6, 7, 8, 9, 10]
    ```
    La suma debe efectuarse de la siguiente manera:
        
        1. Utilizando el operador de concatenación.
        
        2. Utilizando el método extend().

    ??? example "Ver solución propuesta"
        ``` py title="Python"
        lista1 = [ 1, 2, 3, 4, 5 ]
        lista2 = [ 6, 7, 8, 9, 10]

        print(lista1 + lista2) # Output : [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

        lista1.extend(lista2)
        print(lista1) # Output : [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
        ```

        !!! question "Para pensar"
            ¿Cuál es la diferencia más importante que observar al emplear cada manera?

            ¿Podemos decir que una es destructiva y la otra no? ¿Por qué?

    ---

1. Dada la siguiente lista:

    ``` title="Terminal (Entrada/Salida)"
    lista = [ 1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
    ```

    Modifica los valores pares para que sean iguales al doble de su valor.

    ``` title="Terminal (Entrada/Salida)"
    lista = [ 1, 4, 3, 8, 5, 12, 7, 16, 9, 20]
    ```

    ??? example "Ver solución propuesta"
        ``` py title="Python"
        lista = [ 1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

        for i in range( 1, len(lista), 2):
            lista[i] = 2 * lista[i]
            
        print(lista)
    ---

1. Dada la siguiente lista:

    ``` title="Terminal (Entrada/Salida)"
    lista = [10, 3, 4, 9, 6, 8, 4]
    ```

    Imprime en pantalla empleando textos formateados:

    1. La lista.
    
    2. Cual es el mayor valor.
    
    3. Cual es el menor valor.
    
    4. El tercer valor.
    
    5. El quinto valor.
    
    6. La suma del segundo y del cuarto valor.
    
    7. La lista es una serie de valores, pero están desordenados. Ordénala de manera ascendente.
    
    8. Cuantas veces aparece el valor 4 en la lista.
   
    9. Elimina los elementos duplicados utilizando el método correspondiente.

    10. La lista final.

    ??? example "Ver solución propuesta"
        ``` py title="Python"
        lista = [10, 3, 4, 9, 6, 8, 4]

        print("La lista es", lista)

        print(f"El mayor valor es {max(lista)}")

        print(f"El menor valor es {min(lista)}")

        print(f"El tercer valor es {lista[2]}")

        print(f"El quinto valor es {lista[4]}")

        print( f"La suma del segundo y del cuarto valor es {lista[1] + lista[3]}")

        lista.sort()

        print(f"El 4 aparece {lista.count(4)} veces en la lista")

        lista.remove(4)

        print("La lista sin duplicados es", lista)
        ```
        
        ``` title="Terminal (Entrada/Salida)"
        La lista es [10, 3, 4, 9, 6, 8, 4]
        El mayor valor es 10
        El menor valor es 3
        El tercer valor es 4
        El quinto valor es 6
        La suma del segundo y del cuarto valor es 12
        El 4 aparece 2 veces en la lista
        La lista es [3, 4, 6, 8, 9, 10]
        ```

    ---

1. Dada la siguiente lista:

    ``` title="Terminal (Entrada/Salida)"
    colores = [ 'rojo', 'azul', 'verde', 'amarillo' ]
    ```

    Imprímela al derecho y al revés sin utilizar ningún bucle ni otras variables o listas.

    ??? example "Ver solución propuesta"
        ``` py title="Python"
        print(colores)

        colores.reverse()

        print(colores)
        ```
        
    ---

1. Dada la siguiente lista:

    ``` title="Terminal (Entrada/Salida)"
    countdown = [0, 1, 2, 3, 4, 5]
    ```

    Utilízala para tomar cada valor e imprimir una cuenta regresiva.  

    !!! warning "¡Atención! Alcance y Limitación"
        Puedes modificar la lista a tu conveniencia pero solo un elemento a la vez.
        No puedes agregar elementos ni cambiar el valor de un elemento existente.  
        Debes utilizar un ciclo abierto para controlar el funcionamiento del programa.

    ??? example "Ver solución propuesta"
        ``` py title="Python"
        countdown = [0, 1, 2, 3, 4, 5]

        while len(countdown) > 0:
            num = countdown.pop()
            print(num)
        ```
        
    ---

2. Escribe un programa que realice lo siguiente:
    1. Crear una lista de valores del 1 al 5.
    2. Imprimir la lista en pantalla.
    3. Desempaqueta la lista en variables.
    4. Utilizando las variables, imprime la siguiente salida:

        ``` title="Terminal (Entrada/Salida) los valores entre llaves son los almacenados en las variables"
        n1 vale {n1}, n2 vale {n2}, n2 vale …
        ```

    Ver resultado (1)
    { .annotate }

    5. :material-code-tags-check:  

        ``` py title="Python"
        # Crea la lista
        numeros = list(range(1, 6))

        # Imprime la lista
        print(numeros)

        # Desempaca la lista en variables
        n1, n2, n3, n4, n5 = numeros

        # Imprime en pantalla
        print(f"n1 vale {n1}, n2 vale {n2}, n3 vale {n3}, n4 vale {n4}, n5 vale {n5}")
        ```
        
    ---

3. Escribe un programa que solicite un número del 1 al 10.  
Luego, que cree una lista de la tabla de multiplicar del número ingresado.  
Por último, que genere en pantalla una salida como la siguiente, para el número 4 por ejemplo:

    ``` title="Terminal (Entrada/Salida)"
    Ingrese un número entre 1 y 10: 4

    Tabla de multiplicación para 4:

    4 x 1 = 4
    4 x 2 = 8
    4 x 3 = 12
    4 x 4 = 16
    4 x 5 = 20
    4 x 6 = 24
    4 x 7 = 28
    4 x 8 = 32
    4 x 9 = 36
    4 x 10 = 40
    ```

    ??? example "Ver solución propuesta"
        ``` py title="Python"
        # Solicita un número al usuario entre 1 y 10
        num = int(input("Ingrese un número entre 1 y 10: "))

        # Crea una lista con los múltiplos del número ingresado
        # multiplos = [num * i for i in range(1, 11)] sería una excelente solución
        multiplos = list(range(num, (10 * num) + 1, num))

        # Imprime los múltiplos de num en un formato agradable
        print(f"\nTabla de multiplicación para {num}:\n")

        for i in range(1, 11):
            print(f"{num} x {i} = {multiplos[i-1]}")
        ```

    ---









    ``` title="Terminal (Entrada/Salida)"

    ```

    Ver resultado (1)
    { .annotate }

    2. :material-code-tags-check:  

        ``` py title="Python"

        ```

    ---
