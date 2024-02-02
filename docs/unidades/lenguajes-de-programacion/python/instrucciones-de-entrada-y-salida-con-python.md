title: Instrucciones de I/O (entrada/salida) con Python

# Variable = input("Mensaje para usuario") Para que el usuario ingrese un valor en la variable
# El "int" se utiliza para darle a la variable el valor de un número entero, si no, se guarda texto

num1 = int(input("Ingrese el primer número: "))

# Se imprime la variable, la coma es para que haya un espacio, sino se usa +

print("El valor almacenado en num1 es" , num1) 

# Evitar el salto de linea implícito
print("Esta linea arranca con un print", end=" ")
print("y termina con otro print")

print("Hola", end=" hermoso divino genial ") # Todo print tiene implicito el parametro end="\n" que imprime salto del linea al final
print("Mundo") 

print()
print("Hola Mundo")
print("Hola" + " Mundo") # Concatenacion de cadenas de caracteres
print("Hola", "Mundo") # impresion de varios argumentos. La coma, por defecto, agrega un espacio

print("Hola", end=" ") # el parametro end, por defecto es ENTER (end="\n"), permite modificar el final de la impresion
print("Mundo", end="\n\n")
print("\nprimer\nparametro") # Puedo incluir el salto de linea (\n) dentro de mi cadena de texto

print("hipo", "potamo", sep="") # sep es un parametro para imprimir algo el lugar de la coma (por defecto es sep=" ")
print("1", "2", "3", sep=", ") # Esto imprime 1, 2, 3

a = 1
b = 2

print(a + b) # imprime 3
print(str(a) + str(b)) # imprime 12. str( valor ) convierte en cadena. Se lee "12"

a = "1"
b = "2"

print(int(a) + int(b)) # imprime 3. int( cadena ) convierte en entero.

print(f"Hola {nombre}. Tienes {edad} años.") # al ejecutar, la compu hace: Hola Pablo. Tienes 45 años / Es es siempre que nombre sea Pablo y edad sea 45. Reemplaza las variables por su contenido dentro de la cadena de texto. NO OLVIDAR LA f ADELANTE DE LA COMILLA DE APERTURA


## Entrada de datos al programa



### Ejercicios de aplicación

1. Escribe un programa que solicite el ingreso por teclado de datos referidos al nombre, la edad y la nacionalidad de una persona.  
Luego que imprima por pantalla una salida de información formateada de la siguiente manera:

    ``` title="Terminal (Entrada/Salida)"
    Hola {nombre}! Tienes {edad} años. Eres de nacionalidad {nacionalidad}
    ```
    
    ??? example "Ver solución propuesta"
        ``` py title="Python"
        nombre = input("Ingrese su nombre: ")
        edad = input("Ingrese su edad: ")
        nacionalidad = input("Ingrese su nacionalidad: ")
        
        print(f"Hola {nombre}! Tienes {edad} años. Eres de nacionalidad {nacionalidad}")
        ```

    ---

1. Escribe un programa que solicite el ingreso por teclado de datos referidos al nombre, la dirección y el teléfono de una persona.  
Luego que imprima por pantalla una salida de información formateada de la siguiente manera:

    ``` title="Terminal (Entrada/Salida)"
    Nombre: {nombre}
    Dirección: {direccion}
    Teléfonno: {telefono}
    ```
    
    !!! warning "¡Atención! Alcance y Limitación"
        La impresión en pantalla se debe realizar utilizando un solo comando _print_.

    ??? example "Ver solución propuesta"
        ``` py title="Python"
        nombre = input("Ingresa tu nombre: ")
        direccion = input("Ingresa tu direccion: ")
        telefono = input("Ingresa tu telefono: ")
        
        print(f"Nombre: {nombre} \nDireccion: {direccion} \nTelefono: {telefono}")
        ```

        > El `\n` en un comando _print_ se llama "caracter de nueva línea" (_newline character_).  
        > Se utiliza para indicar el final de una línea y el comienzo de una nueva.  
        > Cuando se usa en una cadena dentro de un comando _print_, hace que todo lo que sigue se imprima en la siguiente línea.

        Otra manera de resolver el ejercicio sería:

        ``` py title="Python"
        nombre = input("Ingresa tu nombre: ")
        direccion = input("Ingresa tu direccion: ")
        telefono = input("Ingresa tu telefono: ")
        
        print(f"Nombre: {nombre}", f"Direccion: {direccion}", f"Telefono: {telefono}", sep="\n")
        ```

        > El `\n` como argumento del parámetro _sep_ le indica al comando _print_ que debe hacer un salto de línea al terminar de imprimir cada uno de los argumentos suministrados.

    ---
