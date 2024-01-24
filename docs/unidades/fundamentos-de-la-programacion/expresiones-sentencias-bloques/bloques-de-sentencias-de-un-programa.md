title: Bloques de sentencias de un programa

## ¿Qué es un bloque de sentencias (_block statements_)?

!!! success "Definición"
    Un bloque de sentencias es una sección de un programa que está agrupada por cero o más sentencias, delimitada por un conjunto de llaves equilibradas ( { } ), o “indentados”, es decir, visualmente alineadas y desplazadas hacia la derecha mediante espacios o tabulaciones (creando una estructura jerárquica y facilitando la legibilidad del código), o mediante palabras clave específicas del lenguaje de programación utilizado. 

    Estos bloques pueden contener una o más sentencias o instrucciones que se ejecutan secuencialmente cuando el programa ingresa en ellos.

    Un bloque de sentencias también puede identificarse como sentencia compuesta.

``` js title="Bloques de sentencias utilizando llaves"
if (x > 5) {
    print("x es mayor que 5");
    print("Sigo dentro del bloque if");
}
print("Fuera del bloque if");
```

``` py title:"Bloques de sentencias utilizando indentación"
if x > 5:
    print("x es mayor que 5")
    print("Sigo dentro del bloque if")
print("Fuera del bloque if")
```

Los bloques de código se utilizan para agrupar lógicamente un conjunto de instrucciones que deben ejecutarse juntas como una unidad. Pueden ser utilizados en diversas estructuras de control, como bucles o condicionales, y también pueden ser definidos en funciones o métodos.

!!! info "Para tener en cuenta"
    Los bloques de sentencias ayudan a organizar y estructurar el código fuente, permitiendo una mejor legibilidad y comprensión del programa, así como también facilitan la reutilización de fragmentos de código y el control del flujo de ejecución.


