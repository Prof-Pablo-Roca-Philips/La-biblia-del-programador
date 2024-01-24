title: Paradigmas de la programación

## ¿Qué es un paradigma?

!!! abstract "Definición"
    Un paradigma de programación es una manera o estilo de programación de software. 

    Se trata de un modelo formado por un conjunto de métodos sistemáticos aplicables en todos los niveles del diseño de programas para resolver problemas computacionales. 

Existen varios paradigmas de programación que se utilizan para desarrollar software. Cada paradigma proporciona un enfoque particular para resolver problemas y organizar el código del programa. 

A continuación, se presentan algunos de los paradigmas de programación más comunes:

### Paradigma imperativo

Este es uno de los paradigmas más antiguos y ampliamente utilizados. Los programas consisten en una sucesión de instrucciones detalladas y concretas sobre cómo se deben ejecutar las tareas. 

Los lenguajes de programación imperativos suelen utilizar variables, asignaciones, bucles y estructuras condicionales para controlar el flujo de ejecución. Así, el desarrollador describe en el código, paso por paso, todo lo que hará su programa.

Algunos lenguajes basados en el paradigma imperativo son Pascal, COBOL, FORTRAN, C y C++
Otros enfoques subordinados al paradigma de programación imperativa son:

* **Programación estructurada**: es un tipo de programación imperativa donde el control de flujo se define mediante bucles anidados, condicionales y subrutinas, en lugar de a través de GOTO; y se enfoca en la organización del código en estructuras lógicas claras. Este paradigma busca mejorar la legibilidad y mantenibilidad del código.

* **Programación procedimental**: consiste en basarse en un número muy bajo de expresiones repetidas, englobarlas todas en un procedimiento o función y llamarlo cada vez que tenga que ejecutarse.

* **Programación modular**: consiste en dividir un programa en módulos o subprogramas con el fin de hacerlo más manejable y legible. Se trata de una evolución de la programación estructurada para resolver problemas de programación más complejos.

### Paradigma declarativo

Este paradigma no necesita definir algoritmos puesto que describe el problema en lugar de encontrar una solución al mismo. Este paradigma utiliza el principio del razonamiento lógico para responder a las preguntas o cuestiones consultadas.

Este paradigma a su vez se divide en dos:

* **Programación Lógica**: se basa en la lógica formal y en la resolución de problemas mediante la deducción lógica. Los programas lógicos están compuestos por reglas y hechos, y se utiliza la inferencia lógica para derivar conclusiones. El lenguaje de programación Prolog es uno de los más conocidos.

* **Programación funcional**: el énfasis de la programación funcional está en la evaluación de expresiones y en la aplicación de funciones matemáticas. Se basa en el concepto de funciones puras, que no tienen efectos secundarios y siempre producen el mismo resultado para los mismos datos de entrada. La programación funcional evita el uso de estados mutables y bucles, y se enfoca en la inmutabilidad de los datos. Los lenguajes de programación Lisp, Scala, Java, Kotlin son los más conocidos.

#### Ejemplo de paradigma imperativo vs. paradigma declarativo

Como dijimos, el paradigma imperativo consiste en explicar muy bien cómo funciona un algoritmo. Las instrucciones de nuestro programa deben ser bastante explícitas. El "cómo" se realiza cada paso del algoritmo debe ser muy claro.

Por ejemplo, si queremos crear imperativamente una lista de números del 1 al 10, podemos declarar una lista vacía y una variable contadora y, luego, agregar el valor de la variable contadora como un elemento más a la lista en cada repetición de una estructura iterativa (cíclica), mientras se va incrementando de uno en uno el valor de la variable contadora hasta llegar al 10, inclusive. 

La programación declarativa, contrariamente, prioriza la claridad del resultado por encima que la claridad del paso a paso.

Entonces, para crear una lista del 1 al 10, no definiríamos explícitamente el paso a paso de agregar un número a la lista en cada iteración del ciclo. Más bien, utilizaríamos una función que agregue la cantidad de números que necesitemos.

No te preocupes por tanta terminología, la iremos aprendiendo más adelante. Lo importante para resaltar es la diferencia en el código escrito en cada caso. Veamos:

``` py title="Programación imperativa"
int lista = []
int contador = 1
while contador < 10:
    lista.append(contador)
    contador = contador + 1
```
``` py title="Programación declarativa"
lista(range(1, 10))
```

### Paradigma de la programación orientada a objetos

En este modelo de paradigma se centra en la organización del código para construir modelos de objetos (estructura abstracta que, de manera más fiable, describe un posible objeto del mundo real y su relación con el resto del mundo que lo rodea a través de interfaces), que son instancias de clases, que representan elementos (objetos) del problema a resolver. 

Estos objetos tienen atributos (datos) y métodos (funciones), y se comunican entre sí a través de mensajes, permitiendo separar los diferentes componentes de un programa, simplificando así su creación, depuración y posteriores mejoras. 

La programación orientada a objetos permite el encapsulamiento de datos y la modularidad, como características principales, disminuye los errores y promociona la reutilización del código. Es una manera especial de programar, que se acerca de alguna manera a cómo expresaríamos las cosas en la vida real.

Ejemplos de lenguajes de programación orientados a objetos serían Java, Python o C#.
La programación orientada a objetos se sirve de diferentes conceptos como:

* Abstracción de datos
* Encapsulación
* Eventos
* Modularidad
* Herencia
* Polimorfismo

### Paradigma de la programación reactiva

La programación reactiva es un paradigma enfocado en el trabajo con flujos de datos finitos o infinitos de manera asíncrona. Se basa en escuchar lo que emite un evento o cambios en el flujo de datos, en donde los objetos reaccionan a los valores que reciben de dicho cambio. 

Las librerías más conocidas son Project Reactor, y RxJava. 

React/Angular usan RxJs para hacer uso de la programación reactiva.

Su concepción y evolución ha ido ligada a la publicación del Reactive Manifesto, que establecía las bases de los sistemas reactivos, los cuales deben ser:

* **Responsivos**: aseguran la calidad del servicio cumpliendo unos tiempos de respuesta establecidos.
* **Resilientes**: se mantienen responsivos incluso cuando se enfrentan a situaciones de error.
* **Elásticos**: se mantienen responsivos incluso ante aumentos en la carga de trabajo.
* **Orientados a mensajes**: minimizan el acoplamiento entre componentes al establecer interacciones basadas en el intercambio de mensajes de manera asíncrona.

La motivación detrás de este nuevo paradigma procede de la necesidad de responder a las limitaciones de escalado presentes en los modelos de desarrollo actuales, que se caracterizan por su desaprovechamiento del uso de la CPU debido a la interacción de entrada y salida (I/O), el sobre uso de memoria y la ineficiencia de las interacciones bloqueantes.

!!! info "Para recordar"
     Los lenguajes de programación adoptan uno o varios paradigmas en función del tipo de órdenes que permiten implementar como, por ejemplo, _Python_ o _JavaScript_ que son multiparadigmas.