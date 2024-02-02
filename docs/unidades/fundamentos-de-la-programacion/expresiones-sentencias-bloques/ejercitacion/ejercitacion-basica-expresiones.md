title: Expresiones: ejercitación básica

Estos ejercicios deberían ayudarte a familiarizarte con los operadores y las expresiones. ¡Buena suerte!

1. Resuelve las siguientes expresiones indicando el valor que será almacenado en x:

    ``` py linenums="1" 
    x = 5 + 3   Ver resultado#(1)!
    
    x = (5 + 3) * (2 - 1)   Ver resultado#(2)!
    
    x = 2 ** 3   Ver resultado#(3)!
    
    x = 16 ** (1/2)   Ver resultado#(4)!
    
    x = 10 // 3   Ver resultado#(5)!
    
    x = 10 % 3   Ver resultado#(6)!
    
    x = 10
    x = x + 5   Ver resultado#(7)!
    
    x = 10
    x = x / 2   Ver resultado#(8)!
    
    x = 10
    x += 5   Ver resultado#(9)!
    
    x = 10
    x /= 2   Ver resultado#(10)!
    
    x = "Hola" + " " + "Mundo!"   Ver resultado#(11)!
    
    x = "40" + "35"   Ver resultado#(12)!

    x = 10
    x++   Ver resultado#(13)!
    
    x = 10
    x--   Ver resultado#(14)!
    
    x = True && True   Ver resultado#(15)!
    
    x = True && False   Ver resultado#(16)!
    
    x = False && True   Ver resultado#(17)!
    
    x = False && False   Ver resultado#(18)!
    
    x = True || True   Ver resultado#(19)!
    
    x = True || False   Ver resultado#(20)!
    
    x = False || True   Ver resultado#(21)!
    
    x = False || False   Ver resultado#(22)!
    
    x = !(True)   Ver resultado#(23)!
    
    x = !(False)   Ver resultado#(24)!
    
    a = 2, b = 10, c = 5
    x = (a > 0) && (b < 10) || (c == 5) || !(False)   Ver resultado#(25)!
    ```

    1. :material-code-tags-check:  
    x =     8
    2. :material-code-tags-check:  
    x = 8
    3. :material-code-tags-check:  
    x = 8
    4. :material-code-tags-check:  
    x = 4
    5. :material-code-tags-check:  
    x = 3     
    6. :material-code-tags-check:  
    x = 1     
    7. :material-code-tags-check:  
    x = 15     
    8. :material-code-tags-check:  
    x = 5    
    9. :material-code-tags-check:  
    x = 15
    10. :material-code-tags-check:  
    x = 5    
    11. :material-code-tags-check:  
    x = "Hola Mundo!"    
    12. :material-code-tags-check:  
    x = "4035"    
    13. :material-code-tags-check:  
    x = 11
    14. :material-code-tags-check:  
    x = 9
    15. :material-code-tags-check:  
    x = True
    16. :material-code-tags-check:  
    x = False
    17. :material-code-tags-check:  
    x = False
    18. :material-code-tags-check:  
    x = False
    19. :material-code-tags-check:  
    x = True
    20. :material-code-tags-check:  
    x = True
    21. :material-code-tags-check:  
    x = True
    22. :material-code-tags-check:  
    x = False
    23. :material-code-tags-check:  
    x = False
    24. :material-code-tags-check:  
    x = True
    25. :material-code-tags-check:  
    x = True
    
    ---

1. ¿Cuál será el valor almacenado en la variable correspondiente en cada caso?
 
    ``` js
    a = 5
    b = 3
    resultado = a + b 
    ```

    ??? example "Ver solución propuesta"    El operador de suma (+) se utiliza para sumar los valores de las variables a y b, y el resultado se asigna a la variable resultado.  
    En este caso, será 8.

    ``` js
    a = 5
    b = 3
    resultado = a > b
    ```

    Ver resultado (1)
    { .annotate }

    2. :material-code-tags-check:  
    En este caso, el operador de comparación mayor que (>) compara los valores de a y b y devuelve verdadero si a es mayor que b.  
    El resultado se asigna a la variable resultado, que contendrá el valor booleano verdadero.

    ``` js
    a = 5
    b = 3
    resultado = (a > b) && (b != 0)
    ```

    Ver resultado (1)
    { .annotate }

    3. :material-code-tags-check:  
    En este caso, el operador de comparación mayor que (>) compara los valores de a y b, y el operador de desigualdad (!=) verifica si b no es igual a cero.  
    El operador de conjunción lógica (&&) combina estas dos expresiones y devuelve verdadero solo si ambas son verdaderas.  
    El resultado se asigna a la variable resultado.

    ``` js
    x = 5
    x += 3 
    x?
    ```

    Ver resultado (1)
    { .annotate }

    4. :material-code-tags-check:  
    En este caso, la variable x se inicializa con el valor 5.  
    Luego, se utiliza el operador (+=) para sumar 3 al valor actual de x.  
    La operación x += 3 es equivalente a x = x + 3.  
    Como resultado, el valor de x se actualiza a 8.

    ``` js
    cadena = "Hola"
    cadena += " mundo"
    cadena?
    ```

    Ver resultado (1)
    { .annotate }

    5. :material-code-tags-check:  
    En este caso, el operador (+=) también se puede utilizar con otros tipos de dato, como cadenas de caracteres, para realizar operaciones de concatenación.
    El resultado almacenado en cadena es "Hola mundo".


    ``` js
    lista = [1, 2, 3]
    lista += [4, 5]
    lista?
    ```

    ??? example "Ver solución propuesta"    En este caso, el operador (+=) también se puede utilizar con otros tipos de dato, como listas, para realizar operaciones de agregación de elementos.  
    El resultado almacenado en lista es [1, 2, 3, 4, 5].

    --- 

1. Escribe el pseudocódigo o el código en un lenguaje de programación válido, de los siguientes ejercicios.  
   En cada caso, si hay entrada de datos debe efectuarse por teclado y la salida de resultados debe efectuarse por pantalla:

    1. Ejercicios con operadores de asignación:  

        1. Escribe un programa que, dada la variable x = 4, calcule cada expresión utilizando el operador de asignación simple, una por línea de código:
           * Aumente el número en 5.
           * Multiplique el resultado por 2.
           * Divida el resultado entre 3.
           * Reste 4 al resultado.
           * Imprima el resultado final.

        2. Escribe un programa que, dada la variable x = 4, calcule cada expresión utilizando el operador de asignación compuesta, una por línea de código:
           * Multiplique el número por 3.
           * Sume 7 al resultado.
           * Divida el resultado entre 2.
           * Imprima el resultado final.

        3. Escribe un programa que:
           * Solicite al usuario un número entero
           * Le sume 5 utilizando el operador de asignación compuesta. 
           * Luego, muestre el resultado por pantalla.

    1. Ejercicios con operadores aritméticos:  

        1. Escribe un programa que solicite al usuario dos números enteros y muestre por pantalla la suma, la resta, la multiplicación, la división, la división entera y el módulo de ambos números.   
          Cuidado, en el caso de las divisiones y del módulo, el divisor debe ser el menor valor.

              imprimir(nombre + apellido)
        2. Escribe un programa que solicite al usuario un número y realice las siguientes operaciones:
              * Calcule el cuadrado del número.
              * Calcule la raíz cuadrada del número.

        3. Escribe un programa que solicite al usuario que ingrese la base y la altura para calcular el área de un rectángulo utilizando la fórmula: 
              ```
              area = base * altura
              ```

        4. Escribe un programa similar al anterior, que calcule el área de un triángulo.  
        Piensa que fórmula utilizar. 

    2. Ejercicios con operadores de concatenación de cadenas de caracteres:

        1. ¿Qué resultado tendrá el siguiente ejercicio? ¿Por qué?
            
            ``` js 
            nombre = "Juan", apellido = "Pérez"
            ```

        2. ¿Y si la instrucción de impresión fuera la siguiente? ¿Por qué?

            ``` js 
            nombre = "Juan", apellido = "Pérez"
            imprimir(nombre + " " + apellido)
            ```

        3. Escribe un programa que solicite al usuario su nombre y su edad, y luego muestre un mensaje que diga 
            
            ``` js title="Terminal (Entrada/Salida)"
            Hola, [nombre]. Tienes [edad] años.
            ```

            > Cuando queremos mencionar variables en una cadena de texto, lo hacemos entre corchetes.  
            > Esto significa que durante la ejecución del programa, estas variables deberán ser reemplazadas por el valor almacenado en cada una de ellas.

        4. Escribe un programa similar al anterior pero, en lugar de la edad, debe solicitar el año de nacimiento.  
        El mensaje de salida debe ser el mismo.  
        Por ejemplo:

            ``` title="Terminal (Entrada/Salida)"
            
            ```

            !!! question "¿Cómo se te ocurre que puedes resolver el problema a partir del año de nacimiento?"
            
            Ver resultado (1)
            { .annotate }

            1. :material-code-tags-check:  

                ``` py title="Python"
                anio_actual = 2023
                
                nombre_completo = input("Ingresa tu nombre completo: ")
                anio_nacimiento = int(input("Ingresa tu año de nacimiento: "))
                
                edad = anio_actual - anio_nacimiento
                
                mensaje = "Hola, " + nombre_completo + ". Tienes " + str(edad) + " años."
                
                print(mensaje)
                ```

        5. Escribe un programa que solicite al usuario dos palabras. Luego, que las imprima en orden alfabético y, luego, en orden alfabético inverso. 
        
        6. Escribe un programa que solicite al usuario cuatro cadenas de caracteres y las muestre concatenadas.

        7.  Escribe un programa que solicite al usuario cuatro cadenas de caracteres y con ellas arme y muestre una oración (piensa en las reglas ortográficas).
        
        8.  Escribe un programa que solicite al usuario dos cadenas de caracteres y que informe que cadena es más larga y por cuantos caracteres de más.
        
        9.  Escribe un programa que solicite al usuario su nombre completo. Luego que solo muestre las iniciales de cada palabra en mayúsculas separadas por un espacio.

        Por ejemplo:

            ``` title="Entrada"
            pablo martinez roca
            ```

            ``` title="Terminal (Entrada/Salida)"
            P M R
            ```

            Ver resultado (1)
            { .annotate }

            1. :material-code-tags-check:  

                ``` py title="Python"
                # Bloque principal del programa
                nombre_completo = input("Ingresa tu nombre completo: ")
                iniciales = ""

                palabras = nombre_completo.split()
                
                for palabra in palabras:
                    iniciales += palabra[0].upper() + " "
                print("Las iniciales son:", iniciales)
                                
                ```     

        10. Escribe un programa que solicite una frase y muestre solo las palabras que empiezan con 'a' en una nueva cadena separadas por comas.

        Por ejemplo:

            ``` title="Terminal (Entrada/Salida)"
            
            ```

            Ver resultado (1)
            { .annotate }

            1. :material-code-tags-check:  

                ``` py title="Python"
                # Bloque principal del programa
                frase = input("Ingresa una frase: ")

                palabras = frase.split()

                palabras_con_a = []

                for palabra in palabras:
                    if palabra[0].lower() == 'a':
                        palabras_con_a.append(palabra)

                palabras_con_a_str = ", ".join(palabras_con_a)

                print("Palabras que empiezan con 'a':", palabras_con_a_str)
                ```

                ``` js title="JavaScript"
                // Bloque principal del programa
                var frase = prompt("Ingresa una frase:");

                var palabras = frase.split(" ");
                var palabrasConA = "";

                for (var i = 0; i < palabras.length; i++) {
                    if (palabras[i][0].toLowerCase() === 'a') {
                        palabrasConA += palabras[i] + ",";
                    }
                }

                palabrasConA = palabrasConA.slice(0, -1);

                console.log("Palabras que empiezan con 'a':", palabrasConA);               
                ```

        11. Escribe un programa que solicite al usuario una cadena de caracteresy muestre la primera y última palabra separadas por un guion.
        Por ejemplo:

            ``` title="Terminal (Entrada/Salida)"
            
            ```

            Ver resultado (1)
            { .annotate }

            1. :material-code-tags-check:  

                ``` py title="Python"
                # Bloque principal del programa
                cadena = input("Ingresa una cadena de texto: ")

                palabras = cadena.split()

                primera_palabra = palabras[0]
                ultima_palabra = palabras[-1]

                resultado = primera_palabra + "-" + ultima_palabra
                
                print("Primera y última palabra:", resultado)
                ```

        12. Escribe un programa que solicite al usuario una oración y luego  indique si las palabras están, o no, ordenadas en orden alfabético. 
        
        13. Escribe un programa que tenga una lista de palabras predefinidas. El programa debe seleccionar una palabra al azar y solicitar al usuario que la adivine. El usuario tiene un número limitado de intentos. El programa debe indicar si la palabra del usuario es mayor o menor alfabéticamente que la palabra seleccionada, y continuar pidiendo al usuario que adivine hasta que acierte o se agoten los intentos.
        
        14. Verificar validez de una expresión matemática:
        
        Escribe un programa que solicite al usuario una expresión matemática que incluya paréntesis, corchetes y llaves. El programa debe verificar si los símbolos de apertura y cierre están correctamente balanceados. Por ejemplo, "(2 + [3 * {5 - 1}])" es una expresión válida, mientras que "(2 + [3 * {5 - 1])" no lo es.
        
        15. Juego de piedra, papel o tijera:
        
        Escribe un programa que permita al usuario jugar piedra, papel o tijera contra la computadora. El programa debe solicitar la opción del usuario, generar una opción aleatoria para la computadora y determinar quién gana según las reglas del juego.
        
        16. Validación de tarjeta de crédito:
        
        Escribe un programa que solicite al usuario un número de tarjeta de crédito y verifique si es válido utilizando el algoritmo de Luhn. El programa debe imprimir un mensaje indicando si la tarjeta es válida o no.
        
        17. Juego del ahorcado:
         Escribe un programa que seleccione una palabra al azar de una lista predefinida. El programa debe permitir al usuario adivinar letras de la palabra y mostrar su progreso. El usuario tiene un número limitado de intentos para adivinar la palabra completa. El programa debe indicar si las letras adivinadas por el usuario están en la palabra y mostrar el progreso actualizado.
        
      1. Ejercicios con operadores de incremento y decremento:

          1. ¿Para qué se utiliza el operador ++?

            Ver resultado (1)
            { .annotate }

            1. :material-code-tags-check:  
            Este operador incrementa el valor de la variable en 1.   

          2. ¿Para qué se utiliza el operador --?
            
            Ver resultado (1)
            { .annotate }

            1. :material-code-tags-check:  
            Este operador decrementa el valor de la variable en 1.

          3. ¿Qué valor se le asigna a la variable **y** si se utiliza el operador como sufijo? ¿Cómo operaría el sufijo en la expresión?

            ``` js
            int x = 5
            int y = x++
            ```

            Ver resultado (1)
            { .annotate }

            1. :material-code-tags-check:  
            Este operador incrementa el valor de la variable después de utilizar su valor actual en la expresión.  
            Es útil cuando se desea utilizar el valor original de la variable en una operación y luego incrementarla.  
            El valor de y es 5. 

          4. ¿Qué valor se le asigna a la variable **y** si se utiliza el operador como prefijo? ¿Cómo operaría el prefijo en la expresión?

            ``` js
            int x = 5
            int y = ++x
            ```

            Ver resultado (1)
            { .annotate }

            1. :material-code-tags-check:  
            Este operador incrementa el valor de la variable antes de utilizar su valor en la expresión.  
            Es útil cuando se desea utilizar el valor incrementado de la variable inmediatamente.  
            El valor de y es 6.

      2. Ejercicios con operadores de comparación:

            1. Escribe un programa que tome un número del usuario y verifique si es positivo, negativo o igual a cero.
            
            2. Escribe un programa que solicite al usuario dos números enteros y determine si el primero es mayor que el segundo. 
            
            3. Escribe un programa que solicite al usuario dos números enteros y determine si ambos son pares. 
            
            4. Escribe un programa que solicite al usuario un número entero y determine si es par y positivo al mismo tiempo.
            
            5.  Escribe un programa que solicite al usuario un número entero y determine si es divisible por 3 y 5 al mismo tiempo. 
            
            6.  Escribe un programa que solicite al usuario un número entero y determine si dicho número es impar y múltiplo de 3 al mismo tiempo.

            7. Escribe un programa que pida al usuario dos números enteros y verifique si al menos uno de ellos es positivo y el otro es negativo.

            8. Escribe un programa que solicite al usuario un número y verifique si está dentro de un rango dado.

            9. Escribe un programa que solicite al usuario su nombre y lo compare con el nombre "Juan". Si son iguales, que diga "Hola Juan". 

            10. Escribe un programa que solicite al usuario una contraseña y verifique si coincide con una contraseña predefinida.

            11. Escribe un programa que genere un número aleatorio entre 1 y 100.  
            Luego, que solicite al usuario que adivine el número generado.  
            El programa debe indicar si el número del usuario es mayor o menor que el número generado, y continuar pidiendo al usuario que adivine hasta que acierte. Al acertar, debe indicar en cuantos intentos lo hizo.

            12. Modificar el programa anterior para que tenga un número máximo de intentos.

            13. Modificar el programa anterior para que tenga una tabla de puntuaciones más altas (high scores).

      3. Ejercicios con operadores lógicos (booleanos):

          1. Escribe un programa que solicite al usuario dos valores booleanos (verdadero o falso) y realice las siguientes operaciones:
            * mostrar la operación lógica AND entre los dos valores.
            * mostrar la operación lógica OR entre los dos valores.
            * mostrar la operación lógica NOT del primer valor y del segundo valor.

          2. Escribe un programa que solicite al usuario dos valores booleanos y determine si ambos son iguales. 

          3. Escribe un programa que solicite al usuario dos valores booleanos y determine si ambos son diferentes.  
          Es decir, uno es True y el otro es False, o viceversa.

          4.  Escribe un programa que solicite al usuario dos valores booleanos y determine si ambos son verdaderos o si son falsos.

          5. Escribe un programa que solicite al usuario dos valores booleanos y determine si al menos uno de ellos es verdadero.

      4. Ejercicio de operaciones de conversión de tipos:
            1. Escribe un programa que solicite al usuario un número entero y un número decimal, y realice las siguientes operaciones:
               1. Convierte el número entero a decimal.
               2. Convierte el número decimal a entero.
      
      5. Ejercicio de expresiones condicionales (if-else):
            1. Escribe un programa que solicite al usuario su edad y determine si es mayor de edad (18 años o más). Muestra el resultado por pantalla.
            2. Escribe un programa que solicite al usuario un número entero y determine si es positivo, negativo o cero. Muestra el resultado por pantalla.
      
      6.  Ejercicio de expresiones de bucles:
            1. Escribe un programa que solicite al usuario un número entero y muestre por pantalla todos los números desde 1 hasta ese número utilizando un bucle while.
            2. Escribe un programa que solicite al usuario un número entero y muestre por pantalla todos los números pares desde 0 hasta ese número utilizando un bucle for.
      
      7.  Ejercicio de llamadas a funciones:
            1. Escribe una función llamada "calcular_promedio" que reciba tres números como argumentos y devuelva el promedio de esos números. Luego, utiliza la función para calcular el promedio de tres números ingresados por el usuario.
            2. Escribe un programa que solicite al usuario un número entero y calcule su factorial utilizando una función recursiva. Muestra el resultado por pantalla.
      
      8.  Ejercicio de acceso a elementos:
            1. Escribe un programa que solicite al usuario una lista de palabras separadas por comas. Luego, muestra por pantalla la primera y la última palabra de la lista.
            2. Escribe un programa que solicite al usuario una lista de números separados por comas. Luego, encuentra el número más grande y el número más pequeño de la lista y muéstralos por pantalla.
            3. Escribe un programa que compare dos listas y determine si son iguales (es decir, si contienen los mismos elementos en el mismo orden).
            4. Escribe un programa que encuentre el valor máximo en una lista de números.
            5. Escribe un programa que solicite al usuario una lista de números y los ordene de menor a mayor utilizando el algoritmo de ordenamiento de burbuja. Luego, muestra la lista ordenada al usuario.
            6. Escribe un programa que solicite al usuario el número de estudiantes en una clase, y luego pida al usuario ingresar las notas de cada estudiante. El programa debe calcular el promedio de las notas y determinar cuántos estudiantes obtuvieron una nota por encima del promedio.

2. Problemas complejos para resolver:

    1. Escribe un programa que genere un número aleatorio entre 1 y 1000. El programa debe permitir al usuario adivinar el número, pero esta vez proporcionando pistas. Después de cada intento, el programa debe indicar si el número del usuario es mayor o menor que el número generado, y también indicar qué tan cerca está el número del usuario del número generado (por ejemplo, "Estás a menos de 50 unidades de distancia"). El usuario tiene un número limitado de intentos para adivinar el número correcto.
    
    2. Ordenar una lista de objetos personalizados: Escribe un programa que solicite al usuario ingresar información sobre varias personas, como su nombre, edad y altura. Luego, el programa debe ordenar la lista de personas en función de algún criterio, como la edad o la altura, utilizando operadores de comparación personalizados.
    
    3. Juego del laberinto: Escribe un programa que represente un laberinto como una matriz bidimensional. El programa debe permitir al usuario moverse por el laberinto utilizando comandos de dirección (arriba, abajo, izquierda, derecha) y verificar si el usuario ha llegado a la salida del laberinto.
    
    4. Juego de estrategia basado en turnos: Escribe un programa que simule un juego de estrategia basado en turnos. El programa debe permitir a dos jugadores realizar acciones, como mover unidades o atacar, y verificar el resultado de cada acción utilizando operadores de comparación para determinar el éxito del ataque o la efectividad de las defensas.
    
    5. Análisis de datos complejos: Escribe un programa que lea un archivo de datos complejos, como datos de sensores o registros médicos, y realice análisis utilizando operadores de comparación. Por ejemplo, puedes encontrar valores atípicos, identificar tendencias o realizar cálculos basados en ciertos criterios de comparación.4
    
    6. Crea un programa que solicite al usuario una contraseña y verifique si cumple con los siguientes requisitos: debe tener al menos 8 caracteres, contener al menos una letra minúscula, una letra mayúscula y un número.
