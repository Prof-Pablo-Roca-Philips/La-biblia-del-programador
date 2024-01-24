print = "7"

print(print)


### Uso del operador \ en cadenas para partirlas en más de una línea 

Puedes usar el operador de continuación de línea ( \\ ) para dividir una cadena de texto en varias líneas sin interrumpir la cadena. 

Aquí tienes un ejemplo:

``` py title="Python"
cadena = "Esta es una cadena de texto muy larga que queremos dividir \
en varias líneas para mejorar la legibilidad del código."

print(cadena)
```

Cuando ejecutes este código, verás que la cadena se imprime como una sola línea, a pesar de que en el código fuente está dividida en dos líneas. Esto es porque el operador de continuación de línea ( \\ ) al final de la línea le dice a Python que la línea actual continúa en la siguiente línea.

``` title="Terminal (Entrada/Salida)"
Esta es una cadena de texto muy larga que queremos dividir en varias líneas para mejorar la legibilidad del código.
```

!!! warning "¡Atención!"
    Asegúrate de que no haya ningún espacio o cualquier otro carácter después del operador de continuación de línea ( \\ ), de lo contrario, Python interpretará el \ como un carácter literal en lugar de un indicador de continuación de línea.

!!! info "No solo con cadenas"
    El operador de continuación de línea ( \\ ) también se utiliza en Python para indicar que una línea de código continúa en la siguiente línea.  
    Esto es útil cuando tienes una línea de código muy larga y quieres dividirla en varias líneas para mejorar la legibilidad de este.

    ``` py title="Python"
    # Sin el operador de continuación de línea
    suma = 1 + 2 + 3 + 4 + 5 + 6 + 7 + 8 + 9 + 10

    # Con el operador de continuación de línea 
    # (Recuerda que no debe posee más caracteres a continuación)
    suma = 1 + 2 + 3 + 4 + \
        5 + 6 + 7 + 8 + \
        9 + 10

    print(suma)  # Output: 55
    ```