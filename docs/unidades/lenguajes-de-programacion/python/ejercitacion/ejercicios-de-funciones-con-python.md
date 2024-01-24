title: Python: ejercicios de funciones

1. Ingresa 2 números por teclado.  
Almacénalos en 2 variables.  
Luego, imprime en pantalla cada valor ingresado.  
Luego, crea una función con 2 parámetros que reciban los dos números para devolverlos intercambiados.  
Los valores intercambiados deben ser almacenados en las variables iniciales.  
Luego, imprime en pantalla los valores intercambiados.

    Por ejemplo, para los valores 4 y 5 la salida sería:

    ``` title="Terminal (Entrada/Salida)"
    Ingrese el primer número: 4
    Ingrese el segundo número: 5

    El valor almacenado en num1 es 4
    El valor almacenado en num2 es 5
    
    Ahora, el valor almacenado en num1 es 5
    Ahora, el valor almacenado en num2 es 4
    ```
    
    Ver resultado (1)
    { .annotate }

    1. :material-code-tags-check:  

        ``` py title="Python"
        # Definición de funciones (se utiliza la palabra clave "def")
        def intercambiar(numero1 , numero2):

            # El comando *return* se utiliza para devolver un valores desde la función hacia la línea de código que originó la llamada a la función
            return numero2 , numero1

        # Bloque principal del programa

        # Almacena 2 valores ingresados por teclado en 2 variables
        num1 = int(input("Ingrese el primer número: "))
        num2 = int(input("Ingrese el segundo número: "))

        # Se imprimen los valores almacenados en las variables
        print("El valor almacenado en num1 es" , num1) 
        print("El valor almacenado en num2 es" , num2)

        num1, num2 = intercambiar(num1, num2)   

        print("Ahora, el valor almacenado en num1 es" , num1) 
        print("Ahora, el valor almacenado en num2 es" , num2)
        ```

    ---

1. Escribe un programa que defina una función que retorne por resultado un triángulo es rectángulo o no, a partir de la longitud de sus catetos e hipotenusa.
Una terna pitagórica es una _tupla_ ordenada de tres valores positivos `a`, `b`, `c` que se pueden asociar con las longitudes de los dos catetos y de la hipotenusa correspondiente, formando un triángulo rectángulo.

    Por ejemplo, utilizando la siguiente lista:

    ``` py title="Python"
    triangulos = [(3,4,5), (5,12,13), (9,15,17), (12,35,37), (13,36,39)]
    ```

    El programa deberá devolver los siguientes resultados:
    
    ``` title="Terminal (Entrada/Salida)"
    El triángulo de catetos de 3 cm. y 4 cm. y de hipotenusa de 5 cm. es rectángulo.
    El triángulo de catetos de 5 cm. y 12 cm. y de hipotenusa de 13 cm. es rectángulo.
    El triángulo de catetos de 9 cm. y 15 cm. y de hipotenusa de 17 cm. no es rectángulo.
    El triángulo de catetos de 12 cm. y 35 cm. y de hipotenusa de 37 cm. es rectángulo.
    El triángulo de catetos de 13 cm. y 36 cm. y de hipotenusa de 39 cm. no es rectángulo.
    ```

    !!! tip "¡Una ayudita!"
        La función debe contener la siguiente sentencia:

        ``` py title="Python"
        hipotenusa_calculada = (cateto1 ** 2 + cateto2 ** 2) ** 0.5
        ```

        > Recuerda que `**` en Python es el operador de potencia.  
        > `** 2` equivale a potencia de 2. `** 0.5` equivale a raíz cuadrada.
        
        `cateto1` y `cateto2` son los parámetros que recibe la función.  
        Luego del cálculo deberás hacer algo con `hipotenusa_calculada` y la hipotenusa que reciba la función por parámetro para retornar un resultado que sirva para determinar si el triángulo es o no es rectángulo.

    Analiza el siguiente fragmento del programa para poder completarlo correctamente.

    ``` py title="Python"
    ⋮
    # Lista de triángulos identificados por (cateto1, cateto2, hipotenusa) en cm.
    triangulos = [(3,4,5), (5,12,13), (9,15,17), (12,35,37), (13,36,39)]

    # Se evalua la lista de triangulos
    for cateto1, cateto2, hipotenusa in triangulos:
        # Invocamos a la funcion area_triangulo():
        print(f"\nEl triángulo de catetos de {cateto1} cm. y {cateto2} cm. y de hipotenusa de {hipotenusa} cm. {"es" if es_triangulo_rectángulo(cateto1, cateto2, hipotenusa) else "no es"} rectángulo.")
    ⋮
    ```

    Ver resultado (1)
    { .annotate }

    1. :material-code-tags-check:  

        ``` py title="Python"
        # Definición de funciones 

        def es_triangulo_rectángulo(cateto1, cateto2, hipotenusa):
            hipotenusa_calculada = (cateto1 ** 2 + cateto2 ** 2) ** 0.5

            if hipotenusa_calculada == hipotenusa:
                return True
            else:
                return False


        # Bloque principal del programa

        # Lista de triángulos identificados por (cateto1, cateto2, hipotenusa) en cm.
        triangulos = [(3,4,5), (5,12,13), (9,15,17), (12,35,37), (13,36,39)]

        # Se evalúa la lista de triangulos
        for cateto1, cateto2, hipotenusa in triangulos:

            # Se invoca a la función area_triangulo() dentro del argumento del comando print directamente
            print(f"\nEl triángulo de catetos de {cateto1} cm. y {cateto2} cm. y de hipotenusa de {hipotenusa} cm. {"es" if es_triangulo_rectángulo(cateto1, cateto2, hipotenusa) else "no es"} rectángulo.")
        ```

    ---

1. Escribe un programa que defina una función que reciba 2 listas de elementos y retorne otra lista con los elementos que se encuentran en ambas listas solamente.

    Por ejemplo, utilizando la siguientes listas:

    ``` py title="Python"
    lista1 = [1, 2, 3, 4, 5]
    lista2 = [4, 5, 6, 7, 8]
    ```

    El programa deberá devolver el siguiente resultado:
    
    ``` title="Terminal (Entrada/Salida)"
    lista_interseccion = [4, 5]
    ```

    Y utilizando la siguientes listas:

    ``` py title="Python"
    lista1 = ['a', 'b', 'c', 'd', 'e']
    lista2 = ['c', 'd', 'e', 'f', 'g']
    ```

    El programa deberá devolver el siguiente resultado:
    
    ``` title="Terminal (Entrada/Salida)"
    lista_interseccion = ['c', 'd', 'e']
    ```

    Ver resultado (1)
    { .annotate }

    1. :material-code-tags-check:  

        ``` py title="Python"
        # Definición de funciones 

        def intersectar_listas(lista1, lista2):
            
            # Se inicializa la lista que contendrá los elementos que se encuentren en ambas listas pasadas a la función
            lista_interseccion = []
            
            # Se crea un conjunto de cada lista para eliminar los elementos duplicados
            lista1 = set(lista1)
            lista2 = set(lista2)

            # elemento por elemento del conjunto de la lista1
            for elemento in lista1: 
                
                # Se valida si el elemento se encuentra dentro del conjunto de la lista2
                if elemento in set(lista2):
                    
                    # Se agrega el elemento a la lista de elementos en común
                    lista_interseccion.append(elemento)
            
            # Ordena la lista alfabéticamente y/o numéricamente ascendente
            lista_interseccion.sort()
            
            # Se retorna la lista resultante   
            return lista_interseccion


        # Bloque principal del programa

        # Se inicializan las listas con sus elementos
        lista1 = [1, 2, 3, 4, 5]
        lista2 = [4, 5, 6, 7, 8]

        # Se invoca a la función pasándole las dos listas y se almacena la lista retornada por la función en la lista de intersección
        lista_interseccion = intersectar_listas(lista1, lista2)

        # Se imprime en pantalla la lista resultante
        print("lista_interseccion =", lista_interseccion)

        # Se inicializan las listas con otros elementos
        lista1 = ['a', 'b', 'c', 'd', 'e']
        lista2 = ['c', 'd', 'e', 'f', 'g']

        # Se invoca a la función pasándole las dos listas y se almacena la lista retornada por la función en la lista de intersección
        lista_interseccion = intersectar_listas(lista1, lista2)
        
        # Se imprime en pantalla la lista resultante
        print("lista_interseccion =", lista_interseccion)
        ```

        !!! tip "Claramente el programa puede funcionar con elementos de tipo numérico como alfanumérico.

    ---

