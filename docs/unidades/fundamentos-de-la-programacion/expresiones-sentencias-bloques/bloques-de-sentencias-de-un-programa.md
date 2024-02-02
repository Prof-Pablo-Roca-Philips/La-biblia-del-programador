title: Bloques de sentencias de un programa

## ¿Qué es un bloque de sentencias (_block statements_)?

!!! abstract "Definición"
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

!!! important "¡Para recordar!"
    Los bloques de sentencias ayudan a organizar y estructurar el código fuente, permitiendo una mejor legibilidad y comprensión del programa, así como también facilitan la reutilización de fragmentos de código y el control del flujo de ejecución.

### ¿Qué es la indentación?

La indentación en programación es un concepto y una convención. Es un aspecto del estilo de codificación que implica agregar espacios en blanco al comienzo de las líneas de código para indicar bloques de código y mejorar la legibilidad.

Es decir, que se utiliza para estructurar visualmente el código y hacerlo más legible, indicando el comienzo y el final de los bloques de código, como las declaraciones de funciones, bucles, condicionales, entre otros.

En algunos lenguajes de programación, como Python, la indentación es una parte fundamental de la sintaxis del lenguaje y se utiliza para indicar bloques de código, como las funciones, los bucles y las declaraciones condicionales, y definir el alcance de estos.

Aquí hay un ejemplo:

``` py title="Python"
def funcion():
    print("Esta línea está indentada, por lo que forma parte de la función.")

print("Esta línea no está indentada. A partir de esta línea inclusive, el resto de las líneas no forman parte de la función.")
```

Por otro lado, en lenguajes como Java o C++, la indentación no afecta la funcionalidad del código, pero es una buena práctica seguir convenciones de indentación para hacer que el código sea más legible y fácil de mantener.

Por ejemplo:

``` Java title="Java"
public class Main {
    public static void main(String[] args) {
        System.out.println("Esta línea está indentada, por lo que se puede ver que forma parte de la función main.");
    }
}
```

En ambos ejemplos, la línea que imprime el mensaje está indentada para indicar que forma parte de la función.

!!! important "Definición"
    Por lo tanto, puedes pensar en la indentación como un sistema para organizar y estructurar tu código de una manera que sea fácil de leer y entender.
