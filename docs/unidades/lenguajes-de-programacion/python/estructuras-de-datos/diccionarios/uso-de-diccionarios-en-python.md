





* **min(iterable, *[, clave, valor_defecto])**,
* **max(iterable, *[, clave, valor_defecto])**: Se utilizan para obtener el valor mínimo y máximo de un iterable, una lista en este caso.

 * **clave** (opcional): Una función para servir como clave o criterio de ordenación. La función `min()` o `max()` aplicará esta función a cada elemento del iterable y devolverá el elemento para el cual la función key devuelve el valor mínimo o máximo.

 * **valor_defecto** (opcional): Un valor por defecto que se devuelve si el iterable está vacío.

``` py title="Python"
lista = [1, 2, 3, 4, 5]

# Obtener el valor mínimo de una lista
minimo = min(lista)
print(minimo)  # Output: 1

# Obtener el valor máximo de una lista
maximo = max(lista)
print(maximo)  # Output: 5

# 
```

> En este código, `min(lista)` y `max(lista)` devuelven el valor mínimo y máximo de `lista`, respectivamente. 

``` py title="Python"
# Lista de diccionarios
lista = [{'nombre': 'Ana', 'edad': 27}, {'nombre': 'Luis', 'edad': 30}, {'nombre': 'Carlos', 'edad': 22}]


# Obtener la persona más joven
persona_mas_joven = min(lista, key=lambda x: x['edad'], default={'nombre': 'N/A', 'edad': 0})
print(persona_mas_joven)  # Output: {'nombre': 'Carlos', 'edad': 22}

# Obtener la persona más vieja
persona_mas_vieja = max(lista, key=lambda x: x['edad'], default={'nombre': 'N/A', 'edad': 0})
print(persona_mas_vieja)  # Output: {'nombre': 'Luis', 'edad': 30}


# Intentar obtener la persona más joven de una lista vacía
lista_vacia = []
persona_mas_joven = min(lista_vacia, key=lambda x: x['edad'], default={'nombre': 'N/A', 'edad': 0})
print(persona_mas_joven)  # Output: {'nombre': 'N/A', 'edad': 0}
```

> En este código, `min(lista, key=lambda x: x['edad'], default={'nombre': 'N/A', 'edad': 0})` devuelve la persona más joven de lista. Si lista estuviera vacía, devolvería el valor por defecto `{'nombre': 'N/A', 'edad': 0}`.  
> De manera similar, `max(lista, key=lambda x: x['edad'], default={'nombre': 'N/A', 'edad': 0})` devuelve la persona más vieja de lista, o el valor por defecto si lista está vacía.













# Creación de un diccionario
alumnos = {'Juan': 8, 'Pedro': 9, 'Maria': 10, 'Luis': 7}
print(alumnos)

# Se pueden crear por compresión:
cuadrados = {x: x**2 for x in range(11)}
print(cuadrados)

#-------------------------------------------------------
#Acceso a los elementos. Hay varias maneras.
#-------------------------------------------------------
print(alumnos.get("Juan")) # Devuelve el valor de la clave Juan
print(alumnos.get("Ana"))  # Devuelve "None", no existe "Ana"


# Acceso por clave, usando keys():
print(alumnos.keys())  # Muestra todas las claves

# Podemos recorrer el diccionario con un for y keys():
for i in alumnos.keys():
    print(i)

# items() devuelve una tupla con las claves y los valores:
for clave, valor in alumnos.items():
    print("Alumno:", clave, "Nota:", valor)


# ------------------------------------------------------------
# PYTHON 3 - Diccionarios
# Ejemplo más elaborado
# -----------------------------------------------------------

# Defino la varible 'futbolistas' como un diccionario. No es necesario declarar que tipo de dato es
futbolistas = dict()

futbolistas = {
    1 : "Casillas", 15 : "Ramos",
    3 : "Pique", 5 : "Puyol",
    11 : "Capdevila", 14 : "Xabi Alonso",
    16 : "Busquets", 8 : "Xavi Hernandez",
    18 : "Pedrito", 6 : "Iniesta",
    7 : "Villa"
}


# Recorrer un diccionario, imprimiendo su clave-valor
for k,v in futbolistas.items():
    print ("%s -> %s" %(k,v)) 


# Vemos cuantos elementos tiene nuestro diccionario
numElem = len(futbolistas)
print ("\nNumero de elementos del diccionario: ", numElem)


# Imprimimos una lista con las claves del diccionario
keys = futbolistas.keys()
print ("\nClaves del diccionario:", keys)

# Imprimimos en una lista los valores del diccionario
values = futbolistas.values()
print ("\nValores del diccionario:", values)

# Obtenemos el valor de un elemento dada su clave
elem = futbolistas.get(6)
print ("\nObtenemos el valor cuya clave es '6':", elem)

# Añadimos un nuevo elemento a la lista
futbolistas[22] = 'Navas'
print ("\nDiccionario tras añadir un elemento:", futbolistas)

# Insertamos un elemento en el array. Si la clave ya existe no inserta el elemento
elem2 = futbolistas.setdefault(10,'Cesc')
print ("\nInsertamos un elemento en el diccionario. Si la clave existe no lo inserta\nfutbolistas.setdefault(10,'Cesc'):", elem2)

# Eliminamos un elemento del diccionario dada su clave
futbolistas.pop(22)
print ("\nDiccionario tras eliminar el elemento '22':",futbolistas)

# Hacemos una copia del diccionario
futbolistasCopy = futbolistas.copy()
print ("\nRealizamos una copia del diccionario: \n", futbolistas)

# Mergeamos dos diccionarios
suplentes = {
    4:'Marchena', 9:'Torres', 12:'Valdes',
    13:'Mata' , 17:'Arbeloa', 19:'Llorente',
    20:'Javi Martinez', 21:'Silva', 23:'Reina'
}

futbolistas.update(suplentes)
print ("\nAñadimos los elementos de un diccionario a otro: \n", futbolistas)



