Variables: ejercitación de listas

1. Ejercicios de listas:

    1. Escribir un programa que contenga una función que reciba una lista con valores numéricos enteros como argumento para calcular y devolver el promedio de dichos números.

        ``` py title="Python"
        def calcular_promedio(numeros):
            total = 0
            contador = 0
            
            for num in numeros:
                total += num
                contador += 1
            
            promedio = total / contador
            return promedio

        lista_numeros = [5, 10, 15, 20]
        resultado = calcular_promedio(lista_numeros)
        print(”Promedio: ", resultado)
        ```

        ``` title="Terminal (Entrada/Salida)"
        Promedio: 12.5
        ```

        > En este ejercicio, la función calcular_promedio() calcula el promedio de una lista de números pasada como argumento. 
        > Se utilizan las variables locales total, contador y promedio para realizar los cálculos dentro de la función.

        ---
