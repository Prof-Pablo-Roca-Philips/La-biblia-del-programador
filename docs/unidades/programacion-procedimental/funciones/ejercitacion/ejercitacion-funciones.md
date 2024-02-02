title: Ejercitación de funciones generales

1. Escribir un programa que contenga una función que reciba una lista con valores numéricos enteros como argumento para calcular y devolver el valor máximo de dichos números.

    ``` js title="JavaScript"
    function encontrarMaximo(numeros) {
        let maximo = numeros[0]
        
        for (let i = 1; i < numeros.length; i++) {
            if (numeros[i] > maximo) {
                maximo = numeros[i]
            }
        }
        
        return maximo
    }

    let listaNumeros = [5, 15, 20, 10]
    let resultado = encontrarMaximo(listaNumeros)
    console.log("Máximo: ", resultado)
    ```

    ``` title="Terminal (Entrada/Salida)"
    Promedio: 20
    ```
    > En este ejercicio, la función encontrarMaximo() encuentra el valor máximo en una lista de números. 
    > La variable local maximo se utiliza para realizar el seguimiento del valor máximo encontrado hasta el momento.

    ---
    
1. Calcular el factorial de un número utilizando una variable local en una función.  
Por ejemplo:

    ``` title="Terminal (Entrada/Salida)"
    El factorial de 5 es: 120
    ```

    ??? example "Ver solución propuesta"
        ``` py title="Python"
        # Definición de funciones
        def factorial(n):
            resultado = 1
            
            for i in range(1, n + 1):
                resultado *= i
            
            return resultado

        # Bloque principal del programa
        numero = 5

        resultado = factorial(numero)

        print("El factorial de", numero, "es:", resultado)
        ```

        En esta solución propuesta la función _factorial()_ calcula el factorial del número 5 utilizando una variable local _resultado_ para almacenar el resultado intermedio.

    ---

1. Determinar si una palabra es un palíndromo (es igual si se lee de izquierda a derecha que de derecha a izquierda) utilizando variables locales.  
Por ejemplo:

    ``` title="Terminal (Entrada/Salida)"
    anilina es un palíndromo (se escribe igual al derecho y al revés).
    ```

    ??? example "Ver solución propuesta"
        ``` py title="Python"
        # Definición de funciones
        def es_palindromo(palabra):
            palabra = palabra.lower()
            palabra_invertida = palabra[::-1]
            
            if palabra == palabra_invertida:
                return True
            else:
                return False

        # Bloque principal del programa
        palabra = ”anilina”

        if es_palindromo(palabra):
            print(palabra, "es un palíndromo (se escribe igual al derecho y al revés).")
        else:
            print(palabra, "no es un palíndromo.")
        ```

        En esta solución propuesta la función _es_palindromo()_ verifica si una palabra es un palíndromo utilizando una variable local _palabra_invertida_ para almacenar la versión invertida de la palabra almacenada en la variable _palabra_.

        !!! question "¿Para qué se utiliza el método `lower()`?"

        !!! question "¿Qué hace la instrucción `palabra[::-1]`?"

    ---

1. Calcular la suma de los dígitos de un número utilizando variables locales.  
Por ejemplo:

    ``` title="Terminal (Entrada/Salida)"
    La suma de los dígitos de 12345 es: 15
    ```

    ??? example "Ver solución propuesta"
        ``` py title="Python"
        # Definición de funciones
        def suma_de_los_digitos(numero):
            total = 0
            
            while numero > 0:
                digito = numero % 10
                total += digito
                numero //= 10
            
            return total

        # Bloque principal del programa
        numero = 12345
        resultado = suma_de_los_digitos(numero)
        print(”La suma de los dígitos de", numero, ”es:", resultado)
        ```

        En esta solución propuesta la función _suma_de_los_digitos()_ calcula la suma de los dígitos de un número utilizando una variable local _total_ para almacenar la suma acumulada.

        !!! question "¿Para qué se utiliza el signo % ?"

        !!! question "¿Qué hace el operador // ?"

    ---
    
1. Escribe una función que tome dos listas como argumentos y devuelva True si tienen algún elemento en común, utilizando operadores booleanos.
   
    ---
    
2. Escribe una función que tome tres números como argumentos y devuelva True si el tercero está dentro del rango definido por los primeros dos números.

    ---

3. Escribe una función que tome una cadena de caracterescomo argumento y devuelva True si contiene al menos una letra mayúscula y al menos un número. 

    ---
    
4. Escribe una función que tome un año como argumento y determine si es bisiesto o no. Un año bisiesto es divisible entre 4, pero no entre 100, a menos que también sea divisible entre 400.