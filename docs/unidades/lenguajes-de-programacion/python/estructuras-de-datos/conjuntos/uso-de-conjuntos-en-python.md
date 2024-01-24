# Creación de un conjunto:
nombres = {"Juan", "Pedro", "Maria", "Luis"}
print (nombres)

# Podemos agregar elementos al conjunto:
nombres.add("Ana")
print (nombres)

# Desempaquetado:
alumno1, alumno2, alumno3, alumno4, alumno5 = nombres
print (alumno1)
print (alumno2)
print (alumno3)
print (alumno4)
print (alumno5)


# NO PODEMOS agregar elementos duplicados al conjunto:
nombres.add("Ana") # No da error, pero no se agrega.
print (nombres) 


!!! warning "Cuidado"
    En el siguiente ejemplo, al crear un set numérico, este se crea ordenadamente.
    Pero al crear un set alfanumérico, este se crea de manera desordenada.

# Definición de funciones 

def intersectar_listas(lista1, lista2):
    
    # Se inicializa la lista que contendrá los elementos que se encuentren en ambas listas pasadas a la función
    lista_interseccion = []
    
    # Se crea un conjunto de cada lista para eliminar los elementos duplicados
    lista1 = set(lista1)
    lista2 = set(lista2)
    
    print(lista1)
    print(lista2)

    # elemento por elemento del conjunto de la lista1
    for elemento in lista1: 
        
        # Se valida si el elemento se encuentra dentro del conjunto de la lista2
        if elemento in set(lista2):
            
            # Se agrega el elemento a la lista de elementos en común
            lista_interseccion.append(elemento)
    
    # Se retorna la lista resultante   
    return lista_interseccion


# Bloque principal del programa

# Se inicializan las listas con sus elementos

lista1 = [5, 7, 3, 4, 1]
lista2 = [8, 4, 6, 7, 5]

# Se invoca a la función pasándole las dos listas y se almacena la lista retornada por la función en la lista de intersección
lista_interseccion = intersectar_listas(lista1, lista2)

print(lista_interseccion)


lista1 = ['a', 'b', 'c', 'd', 'e']
lista2 = ['c', 'd', 'e', 'a', 'g']

lista_interseccion = intersectar_listas(lista1, lista2)

print(lista_interseccion)


# ------------------------------------------------------------
# TIP: Claramente, esta función tambien puede trabajar con 
# listas cuyos elementos no sean numéricos:
#
# lista1 = ['a', 'b', 'c', 'd', 'e']
# lista2 = ['c', 'd', 'e', 'f', 'g']
# print(funcion_interseccion(lista1, lista2))
#
# ------------------------------------------------------------