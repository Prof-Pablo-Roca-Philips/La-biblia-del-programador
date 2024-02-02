title: Python: ejercicios de estructuras de datos

## Ejercicios con listas

1. Crea una lista con 8 elementos (números enteros del 1 al 8).  
Imprime en pantalla la lista.  
Luego, agrega 2 elementos más (9 y 10) al final de la lista, uno a la vez.  
Imprime en pantalla la lista.  
Luego, reemplaza el valor almacenado en el quinto elemento por -5.  
Imprime en pantalla la lista.  
Luego, elimina la posición 5. Almacena el valor en la variable _elemento\_eliminado_.
Imprime en pantalla la lista.  
Luego, vuelve a almacenar el valor 5 insertándolo en la posición 5. Esto significa que todos los elementos se correrán una posición a partir de la posición 5.  
Imprime en pantalla la lista.  
Luego, agrega el valor almacenado en la variable _elemento\_eliminado_ al final de la lista.  
Imprime en pantalla la lista.  
Luego, elimina el elemento que contenga el valor almacenado en la variable _elemento\_eliminado_.  
Imprime en pantalla la lista.

    ``` title="Terminal (Entrada/Salida)"
    [1, 2, 3, 4, 5, 6, 7, 8]

    [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

    [1, 2, 3, 4, -5, 6, 7, 8, 9, 10]

    [1, 2, 3, 4, 6, 7, 8, 9, 10]

    [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

    [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, -5]

    [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
    ```

    ??? example "Ver solución propuesta"
        ``` py title="Python"
        # Crea una lista con 8 elementos 
        lista_de_numeros = [1, 2, 3, 4, 5, 6, 7, 8]

        print(lista_de_numeros)

        # Agrega 2 elementos más al final de la lista, uno a la vez
        lista_de_numeros.append(9)
        lista_de_numeros.append(10)

        print(lista_de_numeros)

        # Reemplaza el valor almacenado en el quinto elemento por -5
        lista_de_numeros[4] = -5

        print(lista_de_numeros)

        # Luego, elimina la posición 5 almacenando el valor en la variable *elemento_eliminado*
        elemento_eliminado = lista_de_numeros.pop(4)

        print(lista_de_numeros)
        
        # Almacena el valor 5 insertándolo en la posición 5 de la lista
        lista_de_numeros.insert(4, 5)

        print(lista_de_numeros)

        # Agrega el valor almacenado en la variable *elemento_eliminado* al final de la lista  
        lista_de_numeros.append(elemento_eliminado)

        print(lista_de_numeros)

        # Elimina el elemento que contenga el valor almacenado en la variable *elemento_eliminado*  
        lista_de_numeros.remove(elemento_eliminado)

        print(lista_de_numeros)    
        ```

    ---

## Ejercicios con _for … in_

1. Dada la siguiente lista:

    ``` py title="Python"
    numeros = [4, -78, 9, 84, -7, 0, 1]
    ```

    Imprime en pantalla cada uno de los elementos que la componen, renglón por renglón:

    ``` title="Terminal (Entrada/Salida)"
    4
    -78
    9
    84
    -7
    0
    1
    ```

    ??? example "Ver solución propuesta"
        ``` py title="Python"
        numeros = [4, -78, 9, 84, -7, 0, 1]

        for numero in numeros:
            print(numero)
        ```

    ---

## Ejercicios con _for … in enumerate_

1. Crea dos listas según el ejemplo:

    ``` py title="Python"
    lista_1 = [1, 2, 3, 4, 5]

    lista_2 = [10, 9, 8, 7, 6]
    ```

    Luego, une ambas listas en una tercera lista llamada _lista\_unida_.  
    Luego, imprime la _lista\_unida_, en una misma línea, separados por una coma.  
    Presta atención que el último número no debe tener una coma a continuación.

    ??? example "Ver solución propuesta"
        ``` py title="Python"
        lista_1 = [1, 2, 3, 4, 5]
        lista_2 = [10, 9, 8, 7, 6]

        # Une las 2 listas con el operador de adición y asigna el resultado a la lista_unida
        lista_unida = lista_1 + lista_2

        # Imprime la lista_unida en un solo renglón, separando los elementos con una coma, sin incluir la coma al final
        for index, numero in enumerate(lista_unida):
            print(numero, end=", " if index < (len(lista_unida) - 1) else "\n")
        ```

    ---

## Ejercicios con _while … loop_

1. Ingresa números por teclado y almacénalos en una lista.  
Repite la operación hasta que se ingrese un 0 por teclado.  
El 0 no debe ser almacenado en la lista.  
Luego, imprime en pantalla la cantidad de elementos que posee la lista.

    Por ejemplo:

    ``` title="Terminal (Entrada/Salida)"
    Ingrese un número o el cero para terminar el ingreso: 5
    Ingrese un número o el cero para terminar el ingreso: 7
    Ingrese un número o el cero para terminar el ingreso: 3
    Ingrese un número o el cero para terminar el ingreso: 9
    Ingrese un número o el cero para terminar el ingreso: 0
    La lista posee 4  elementos.
    Estos son:  [5, 7, 3, 9]
    ```
    
    ??? example "Ver solución propuesta"
        ``` py title="Python"
        lista = []

        # Limpia la pantalla
        print("\033[2J\033[1H")
        
        
        # Solicita el ingreso de números y los almacena en la lista hasta que se ingrese un 0
        while True:
            n = int(input("Ingrese un número o el cero para terminar el ingreso: "))
            if n == 0:
                break
            lista.append(n)

        # Imprime por pantalla la longitud de la lista
        print("La lista posee", len(lista), " elementos.")

        # Imprime por pantalla los elementos almacenados en la lista
        print("Estos son:", lista)
        ```

    ---

## Ejercicios con cadenas de caracteres

1. Ingresa tu nombre por teclado y almacénalo en una variable.  
Luego imprime en pantalla si posee letras repetidas.  
Puedes usar otras estructuras de datos para realizar la tarea de manera más simple.

    Por ejemplo:

    ``` title="Terminal (Entrada/Salida)"
    Ingrese su nombre: Pablo Andres
    Su nombre posee letras repetidas.
    ```

    ``` title="Terminal (Entrada/Salida)"
    Ingrese su nombre: Ramon Fidel
    Su nombre no posee letras repetidas.
    ```
    
    ??? example "Ver solución propuesta"
        ``` py title="Python"
        # Solicita el ingreso de datos por teclado y los convierte en minúsculas antes de almacenarlos en la variable
        nombre = input("Ingrese su nombre: ").lower()

        # Elimina los espacios que puedan existir almacenados en la variable
        nombre = nombre.replace(" ", "")

        # Convierte cada caracter de la cadena de caracteresen elementos de una lista 
        letras = list(nombre)

        # set es un comando que evalúa un conjunto de elementos y devuelve un conjunto de elementos únicos (elimina los duplicados)
        if (len(letras) == len(set(letras))):
            print("Su nombre no posee letras repetidas.")
        else:
            print("Su nombre posee letras repetidas.")
        ```

    ---

1. Ingresa una palabra por teclado.  
Luego imprime cuantas letras la componen.
Luego imprime todas sus letras de manera ordenada alfabéticamente.
Luego imprime todas sus letras de manera ordenada alfabéticamente inversa.
Antes de empezar el ejercicio, analiza el ejemplo siguiente. Las salidas por pantalla deben ser iguales en su estructura.

    Por ejemplo:

    ``` title="Terminal (Entrada/Salida)"
    Ingrese una palabra: paracaidas
    La palabra paracaidas contiene 10 letras.
    Las letras ordenadas alfabéticamente son a, a, a, a, c, d, i, p, r, s
    Las letras ordenadas alfabéticamente inversoa son s, r, p, i, d, c, a, a, a, a
    ```

    ??? example "Ver solución propuesta"
        ``` py title="Python"
        palabra = input("Ingrese una palabra: ")

        print("La palabra", palabra, "contiene", len(palabra), "letras.")

        letras = list(palabra)

        # Ordena los elementos de la lista de manera alfabética
        letras.sort()
        
        print("Las letras ordenadas alfabéticamente son", ', '.join(letras))

        # Ordena los elementos de la lista de manera alfabética inversa
        letras.sort(reverse=True)
        
        print("Las letras ordenadas alfabéticamente inversoa son", ', '.join(letras))
        ```

        > En este código `', '.join(letras)` une todos los elementos de la lista en una cadena, con cada elemento separado por una coma y un espacio.

    ---

1. Inicializa una variable con la cadena de caracteres"La mar estaba serena serena estaba la mar".  
Luego imprime en pantalla cuantos caracteres tiene la cadena de texto.  
Luego imprime en pantalla toda la cadena de texto, en un solo renglón, caracter por caracter.  
Luego imprime en pantalla, renglón por renglón, cada una de las palabras de la cadena de texto. (Puedes utilizar otra estructura de datos que te facilite el trabajo).  

    ``` title="Terminal (Entrada/Salida)"
    La cadena de caracteres"La mar estaba serena serena estaba la mar" tiene 41 caracteres.
    
    La mar estaba serena serena estaba la mar
    
    La
    mar
    estaba
    serena
    serena
    estaba
    la
    mar
    ```

    ??? example "Ver solución propuesta"
        ``` py title="Python"
        texto = "La mar estaba serena serena estaba la mar"

        # Imprime en pantalla cuantos caracteres tiene la cadena de texto
        print("La cadena de caracteres\"" + texto + "\" tiene", len(texto), "caracteres.")

        # Imprime en pantalla toda la cadena de texto, en un solo renglón, caracter por caracter
        for letra in texto:
            print(letra, end="")
        
        # Al finalizar el cclo, el cursor quedó a continuación de la última letra impresa.
        # Entonces, es necesario realizar un salto de línea para que el próximo contenido que se imprima en pantalla, se haga en un renglón siguiente.

        # Emtonces, imprime en pantalla el salto de línea
        print()

        # Separa la cadena de caracteresen palabras, almacenándolas como elementos de la lista *palabras*
        palabras = texto.split(" ")

        # Imprime en pantalla, renglón por renglón, cada una de las palabras de la cadena de texto
        for palabra in palabras:
            print(palabra)
        ```

    ---

1. Copia el código del ejercicio anterior y a contiunación agrega el código necesario para que realice lo siguiente:  
Reemplaza todas las vocales por la letra "a".
Imprime en pantalla la cadena de texto.
Repite la operación con todas las vocales.

    ``` title="Terminal (Entrada/Salida)"
    ⋮
    La mar astaba sarana sarana astaba la mar
    Le mer estebe serene serene estebe le mer
    Li mir istibi sirini sirini istibi li mir
    Lo mor ostobo sorono sorono ostobo lo mor
    Lu mur ustubu surunu surunu ustubu lu mur
    ```

    ??? example "Ver solución propuesta"
        ``` py title="Python"
        texto = "La mar estaba serena serena estaba la mar"

        # Imprime en pantalla cuantos caracteres tiene la cadena de texto
        print("La cadena de caracteres\"" + texto + "\" tiene", len(texto), "caracteres.")

        # Imprime en pantalla toda la cadena de texto, en un solo renglón, caracter por caracter
        for letra in texto:
            print(letra, end="")

        # Al finalizar el cclo, el cursor quedó a continuación de la última letra impresa.
        # Entonces, es necesario realizar un salto de línea para que el próximo contenido que se imprima en pantalla, se haga en un renglón siguiente.

        # Emtonces, imprime en pantalla el salto de línea
        print()

        # Separa la cadena de caracteresen palabras, almacenándolas como elementos de la lista *palabras*
        palabras = texto.split(" ")

        # Imprime en pantalla, renglón por renglón, cada una de las palabras de la cadena de texto
        for palabra in palabras:
            print(palabra)

        # Reemplaza todas las vocales por la "a"
        for vocal in 'aeiouAEIOU':
            texto = texto.replace(vocal, 'a')

        # Imprime el texto resultante en pantalla
        print(texto)

        # Reemplaza la vocal del texto (son todas la misma) por la siguiente vocal e imprime el texto resultante en pantalla
        texto = texto.replace('a', 'e')
        print(texto)
        texto = texto.replace('e', 'i')
        print(texto)
        texto = texto.replace('i', 'o')
        print(texto)
        texto = texto.replace('o', 'u')
        print(texto)
        ```
        
        Podemos mejorar el código implementando diccionario de mapeo (_mapping dictionary_) y un ciclo:

        ``` py title="Python"
        ⋮
        # Reemplaza la vocal del texto (son todas la misma) por la siguiente vocal e imprime el texto resultante en pantalla
        mapping = {'a': 'e', 'e': 'i', 'i': 'o', 'o': 'u'}
        for k, v in mapping.items():
            texto = texto.replace(k, v)
            print(texto)
        ```
        
        > Aquí, `k` representa la llave (_key_) y el caracter a reemplazar  
        > Y `v` representa el valor asociado (_value_) y el caracter de reemplazo

    --- 

## Ejercicios compuestos

1. Copia el código del ejercicio anterior y a contiunación modifícalo para que realice lo siguiente:
La impresión en pantalla de los elementos debe realizarse en el mismo renglón, separándolos con un espacio y sin corchetes.  
Luego, se debe imprimir en pantalla la serie de números entre el valor del primer elemento almacenado y el valor del último elemento almacenado, incluyéndolos.

    Por ejemplo:

    ``` title="Terminal (Entrada/Salida)"
    Ingrese un número o el cero para terminar el ingreso: 4
    Ingrese un número o el cero para terminar el ingreso: -6
    Ingrese un número o el cero para terminar el ingreso: 9
    Ingrese un número o el cero para terminar el ingreso: 8
    Ingrese un número o el cero para terminar el ingreso: 0
    La lista posee 4 elementos.
    Estos son: 4 -6 9 8 
    Los números entre 4 y 8, incluyéndolos, son: 4 5 6 7 8
    ```

    !!! warning "¡Para recordar!"
        La serie de números podría resultar ascendente, como en el ejemplo, o podría resultar descendente.
        El programa debe funcionar correctamente en ambos sentidos.
    
    ??? example "Ver solución propuesta"
        ``` py title="Python"
        lista = []

        # Limpia la pantalla
        print("\033[2J\033[1H")


        # Solicita el ingreso de números y los almacena en la lista hasta que se ingrese un 0
        while True:
            n = int(input("Ingrese un número o el cero para terminar el ingreso: "))
            if n == 0:
                break
            lista.append(n)

        # Imprime por pantalla la longitud de la lista
        print("La lista posee", len(lista), "elementos.")

        # Imprime por pantalla los elementos almacenados en la lista
        print("Estos son:", end=" ")

        for n in lista:
            print(n, end=" ")

        print() # Realiza el salto de línea luego de la impresión de los elementos en el ciclo anterior

        # Almacena el primer y el último elemento en dos variables 
        primer_elemento = lista[0]
        ultimo_elemento = lista[-1] # len(lista)-1

        # La variable paso almacenará uno positivo o uno negativo, con el objetivo de configurar el ciclo cerrado a continuación para su correcto funcionamiento.
        paso = 1 if primer_elemento <= ultimo_elemento else - 1

        # Imprime en pantalla los números comprendidos entre el valor del primer elemento y el valor del último elemento de la lista

        print("Los números entre " + str(primer_elemento) + " y " + str(ultimo_elemento) + ", incluyéndolos, son:", end=" ")

        for n in range(primer_elemento, ultimo_elemento + paso, paso):
            print(n, end=" ")
        ```

    ---

