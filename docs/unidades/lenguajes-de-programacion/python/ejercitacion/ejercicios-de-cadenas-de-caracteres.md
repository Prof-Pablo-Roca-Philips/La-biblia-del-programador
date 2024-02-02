1. Dada la siguiente cadena "*** Hola Mundo ***" escribe un programa que imprima en pantalla lo siguiente:

    ``` title="Terminal (Entrada/Salida)"
    *** Hola Mundo ***
     Hola Mundo
     Hola Mundo ***
    *** Hola Mundo
    Hola Mundo
    ```

    !!! warning "¡Presta mucha atención a las salidas propuestas, sobre todo, los espacios y las alineaciones!"

    ??? example "Ver solución propuesta"
        ``` py title="Python"
        cadena = "*** Hola Mundo ***"

        print(cadena)
        print(cadena.strip("*"))
        print(cadena.lstrip("*"))
        print(cadena.rstrip("*"))
        print(cadena.strip("*").strip())
        ```
    ---

# Para enunciar:

# find() devuelve la posición de la primera ocurrencia de un caracter
cadena = "Es una cadena nada de nada"
print(cadena)
print(cadena.find("nada"))         # devuelve la posición de la primera ocurrencia de "nada"
print(cadena.find("nada", 15))     # busca desde la posición 15
print(cadena.find("nada", 0, 10))  # -1 es que no encontró
print()


# rfind() devuelve la posición de la última ocurrencia de un caracter
cadena = "Es una cadena nada de nada"
print(cadena)
print(cadena.rfind("nada"))         # devuelve la posición de la última ocurrencia de "nada"
print(cadena.rfind("nada", 15))     # busca desde el final hasta la posición 15
print(cadena.rfind("nada", 10, 20)) # busca desde la posición 10 hasta la posición 20
print()

# ------------------------------------------------------------
# Ejemplo 6
# ------------------------------------------------------------
numero = 12
color = "verde"
print("El color es: " + color + " y el número es: " + str(numero))
print( f"El color es: {color} y el número es: {numero}")


# ------------------------------------------------------------
# Ejemplo 7
# ------------------------------------------------------------
numero = 12
color = "verde"
print("El color es: " + color + "\n y el número es: " + str(numero))


# Operador de "escape"


print('El \'color\' es: ' + color + '\n y el \'número\' es: ' + str(numero))
print("a \t \t \t otros \t espacios")
print("a \t c \t varios \t espacios")

# ------------------------------------------------------------
# Ejemplo 8
# ------------------------------------------------------------
print( "C:\nombre\Juan\Desktop\Python\Python1\05_Strings1.py" )
print( r"C:\nombre\Juan\Desktop\Python\Python1\05_Strings1.py" ) #Raw String
color = "verde"
print( rf"El \numero\ es color: {color}" )

Formato de cadenas de caracteres
nombre = "Juan"
apellido = "Perez"
edad = 30

print ("Hola, {} {}, tienes {} años".format(nombre, apellido, edad))
print ("Hola, {1} {0}, tienes {2} años".format(nombre, apellido, edad))


# Slicing (cadenas y listas)
# Get the characters from position 2 to position 5 (not included):
b = "Hello, World!"
print(b[2:5])

# Slice From the Start
# By leaving out the start index, the range will start at the first character:
# Get the characters from the start to position 5 (not included):
b = "Hello, World!"
print(b[:5])

# Negative Indexing
# Use negative indexes to start the slice from the end of the string:
# Example
# Get the characters:
# From: "o" in "World!" (position -5)
# To, but not included: "d" in "World!" (position -2):
b = "Hello, World!"
print(b[-5:-2])