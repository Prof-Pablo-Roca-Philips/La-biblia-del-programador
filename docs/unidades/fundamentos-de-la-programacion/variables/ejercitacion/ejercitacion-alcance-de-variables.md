Variables: ejercitación sobre alcance

1. Ejercicios de acceso a variables globales desde ámbitos locales:

    1. Crear una función que acceda a una variable global que inicialmente tiene almacenado el valor 10. Dentro de la función imprimir el valor de la variable global.

        ``` py title="Python"
        var_global = 10

        def acceso_global():
            print("Variable global:", var_global)

        acceso_global()
        ```

        ``` title="Terminal (Entrada/Salida)"
        Variable global: 10
        ```

        > En este ejercicio, la función acceso_global() imprime el valor de la variable global var_global.  
        > No es necesario utilizar la palabra clave global dentro de la función, ya que solo se accede a la variable global sin realizar modificaciones.

        ---

    1. Crear una función que acceda a una variable global de valor 10. Dentro de la función incrementar dicho valor en 5. imprimir el valor de la variable antes y después de hacer la llamada a la función.

        ``` py title="Python"
        var_global = 10

        def modificar_global():
            global var_global
            var_global += 5

        print("Variable global antes de la modificación:", var_global)

        modificar_global()

        print("Variable global después de la modificación:", var_global)
        ```

        ``` title="Terminal (Entrada/Salida)"
        Variable global antes de la modificación: 10
        Variable global después de la modificación: 15
        ```

        > En este ejercicio, la función modificar_global() modifica el valor de la variable global var_global al agregarle 5. 
        >Se utiliza la palabra clave global dentro de la función para indicar que se está accediendo a la variable global y no creando una variable local con el mismo nombre.

        --- 

    1. Crear una variable global de valor 10. En una función crear una variable local de igual nombre a la global pero de valor 15. Imprimir la variable antes, durante y después de la llamada a la función.

        ``` py title="Python"
        variable = 10

        def imprimir_variable():
            variable = 15
            print(”La variable fuera de la función vale:”, variable)

        print(”La variable fuera de la función vale:”, variable)

        imprimir_variable()

        print(”La variable fuera de la función vale:”, variable)
        ```

        ``` title="Terminal (Entrada/Salida)"
        La variable fuera de la función vale: 10
        La variable dentro de la función vale: 15
        La variable fuera de la función vale: 10
        ```

        > En este ejercicio, la función imprimir_variable() inicializa una variable local de valor 15 y luego imprime su contenido.
        > Nótese que antes y después de ello, por fuera de la función, también se imprime el valor de la variable creada globalmente. Pero, 

        !!! question "Hay que preguntarse..."
            ¿Por qué tienen diferentes valores?
            
            ¿Por qué no se modificó el valor dentro de la función?
            
            ¿Es la misma variable?
            
            ¿Qué ocurre con la variable creada dentro de la función?
