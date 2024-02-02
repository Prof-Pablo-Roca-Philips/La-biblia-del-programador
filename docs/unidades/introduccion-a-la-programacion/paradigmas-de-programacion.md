title: Paradigmas de programación

# Paradigmas de programación

<label class="revision">Rev. 10/01/2024</label>

## ¿Qué es un paradigma?

!!! abstract "Definición"
    Los paradigmas de programación son una manera de clasificar los lenguajes de programación según sus características.  
    Se trata de modelos formados por un conjunto de métodos sistemáticos aplicables en todos los niveles del diseño de programas para resolver problemas computacionales. 

Existen varios paradigmas de programación que se utilizan para desarrollar software. Cada paradigma proporciona un enfoque particular para resolver problemas y organizar el código del programa. 

Los paradigmas de programación han evolucionado a lo largo del tiempo, a medida que los desarrolladores han buscado nuevas formas de abordar los problemas de programación. 

Aquí está una cronología aproximada de los principales paradigmas:

### Programación imperativa/procedural (1950s)

Este es uno de los paradigmas más antiguo, básico y ampliamente utilizado. Los programas consisten en una sucesión de instrucciones detalladas y concretas sobre cómo se deben ejecutar las tareas en orden. 

Utiliza instrucciones que cambian el estado del programa. Los programas imperativos consisten en comandos para la computadora, detallando paso a paso cómo se deben ejecutar las tareas.

Los lenguajes de programación imperativos suelen utilizar variables, asignaciones, estructuras repetitivas (bucles) y estructuras alternativas (condicionales) para controlar el flujo de ejecución. Los bucles, como _for_ y _while_, se utilizan para repetir un bloque de código varias veces. Las estructuras condicionales, como _if_ y _switch_, se utilizan para ejecutar diferentes bloques de código dependiendo de ciertas condiciones. Estas estructuras de control son fundamentales para la programación imperativa y permiten a los programadores escribir código que puede manejar, paso por paso, una variedad de situaciones y realizar tareas complejas.

Los lenguajes como Fortran y COBOL, C, Pascal y C++ son ejemplos de este paradigma.

### Programación procedimental (1950s)

La programación procedimental es un subtipo del paradigma de programación imperativa donde el flujo de la ejecución del programa se controla con procedimientos, o rutinas, que son llamados en un orden específico. Estos procedimientos, que engloban un número de expresiones repetidas, son llamados cada vez que tengan que ser ejecutadas las mencionadas expresiones y pueden modificar el estado del programa.

Por lo tanto, los programas se construyen a partir de procedimientos, también conocidos como funciones o rutinas, que son una serie de instrucciones que realizan una tarea específica en un determinado momento de ejecución del programa. 

Los procedimientos pueden ser llamados por otros procedimientos, permitiendo la reutilización de código y la estructuración del programa en bloques de código más manejables. 

Los procedimientos pueden manipular variables, realizar operaciones y controlar el flujo del programa a través de estructuras de control como bucles y condicionales.

Algunos lenguajes de programación que utilizan el paradigma procedimental incluyen Fortran, COBOL, Pascal, C y C++.

### Programación funcional (1950s-1980s) 

La programación procedimental y la programación funcional son dos paradigmas de programación diferentes, aunque ambos involucran el uso de funciones.

El énfasis de la programación funcional está en la evaluación de expresiones y en la aplicación de funciones matemáticas, evita el uso de estados mutables (evita cambiar el estado) y bucles, y se enfoca en la inmutabilidad de los datos. 

El cálculo lambda, que es la base de la programación funcional, es un sistema formal en la lógica matemática y la ciencia de la computación que se utiliza para investigar funciones, aplicaciones de funciones y la recursión. 

Se basa en la abstracción de funciones y la aplicación de funciones. En términos simples, permite tratar las funciones como entidades de primera clase (funciones puras), lo que significa que las funciones pueden ser pasadas como argumentos a otras funciones, devueltas como valores de otras funciones, y asignadas a variables. 

Estas funciones no tienen efectos secundarios y siempre producen el mismo resultado para los mismos datos de entrada.

Aunque Lisp, uno de los primeros lenguajes funcionales, se desarrolló en los años 50, este paradigma no se popularizó hasta los años 80 con lenguajes como ML y Haskell, más tarde con Java, Scala y Kotlin y más recientemente con versiones funcionales de lenguajes como JavaScript y Python.

### Programación estructurada (1960s)

La programación estructurada surgió como una manera de mejorar la claridad y la eficiencia de los programas escritos en lenguajes de programación imperativos. 

Por lo tanto, es un subtipo de programación imperativa que introduce conceptos adicionales para mejorar la claridad y eficiencia del código. La programación estructurada enfatiza un flujo de control claro y estructurado, utilizando estructuras de control como bucles y condicionales, y evitando el uso de instrucciones de salto como "goto". La idea es dividir un programa en partes más pequeñas o secciones, generalmente utilizando subrutinas (también conocidas como funciones o procedimientos).

Por lo tanto, la principal diferencia entre la programación imperativa y la programación estructurada es que la programación estructurada introduce reglas y prácticas adicionales para mejorar la claridad y la eficiencia del código. Todos los programas estructurados son imperativos, pero no todos los programas imperativos son estructurados.

### Programación orientada a objetos / OOP (1960s-1970s) 

Este paradigma se centra en la organización del código para construir modelos de objetos (estructura abstracta que, de manera más fiable, describe un posible objeto del mundo real y su relación con el resto del mundo que lo rodea a través de interfaces), que son instancias de clases, que representan elementos (objetos) del problema a resolver. 

Estos objetos tienen atributos o propiedades (datos) y métodos (funciones), y se comunican entre sí a través de mensajes, permitiendo separar los diferentes componentes de un programa, simplificando así su creación, depuración y posteriores mejoras. 

Se popularizó con lenguajes como Simula y Smalltalk, y más tarde con C++, Java, C# y Python.

Permite el encapsulamiento de datos y la modularidad, como características principales, disminuyendo los errores y promocionando la reutilización del código. 

Este paradigma es una manera especial de programar, que se acerca de alguna manera a cómo expresaríamos las cosas en la vida real, puesto que se sirve de diferentes conceptos como:

  * Abstracción de datos
  
  * Encapsulamiento
  
  * Eventos
  
  * Modularidad
  
  * Herencia
  
  * Polimorfismo

### Programación modular (1960s-1070s)

La programación modular es un paradigma que enfatiza la separación de la funcionalidad de un programa en módulos independientes e intercambiables, cada uno de los cuales contiene todo lo necesario para ejecutar una única función de la lógica del programa, con el fin de hacerlo más manejable y legible, permitiendo resolver problemas de programación más complejos.

La programación modular fue popularizada por lenguajes como Modula, Ada y, más recientemente, Python y Java.

Los lenguajes que soportan la programación modular incluyen, pero no se limitan a, Python, Java, C, C++, JavaScript, Ruby, Swift, y muchos otros.

La programación modular es un subparadigma de la programación procedimental, pero también se puede utilizar en otros paradigmas como la programación orientada a objetos. La idea es que los módulos pueden ser probados de manera independiente y luego ensamblados para formar un programa completo, lo que puede mejorar la reutilización del código, la legibilidad y el mantenimiento.

### Programación lógica (1970s)

En este paradigma, los programas son un conjunto de declaraciones lógicas, y la ejecución del programa es un proceso de inferencia lógica. 

Es decir, se basa en la lógica formal y en la resolución de problemas mediante la deducción lógica. 

Los programas lógicos están compuestos por reglas y por hechos y se utiliza la inferencia lógica para derivar conclusiones. 

Prolog, desarrollado en los años 70, es el principal representante de este paradigma.

### Programación declarativa (1980s)

La programación declarativa es un paradigma de programación que se centra en "qué" se debe hacer, en lugar de "cómo" se debe hacer. En otras palabras, en lugar de escribir código detallado paso a paso para lograr una tarea, simplemente se declara lo que se desea y se deja que el lenguaje y el sistema de tiempo de ejecución figuren cómo hacerlo.

Asi, no necesita definir algoritmos puesto que describe el problema en lugar de encontrar una solución al mismo.

Este paradigma utiliza el principio del razonamiento lógico para responder a las preguntas o cuestiones consultadas.

Un ejemplo de programación declarativa podría ser una consulta SQL. En lugar de describir exactamente cómo obtener los datos de una base de datos (recorrer filas, abrir y cerrar conexiones, etc.), simplemente declaras lo que quieres:

``` sql title="Programación declarativa"
SELECT name, age FROM users WHERE age > 18;
```

> En este código, simplemente estás declarando que quieres los nombres y las edades de los usuarios que son mayores de 18 años. No te preocupas por cómo SQL va a buscar esa información.

Algunos lenguajes que utilizan el paradigma de programación declarativa son:

  * **SQL**: utilizado para consultas de bases de datos.

  * **HTML**: utilizado para describir la estructura de las páginas web. Sí, HTML (HyperText Markup Language) es considerado un lenguaje declarativo. No es un lenguaje de programación en el sentido tradicional, ya que no tiene estructuras de control como bucles o condicionales. Sin embargo, es un lenguaje en el sentido de que tiene una sintaxis y reglas definidas que se utilizan para describir la estructura de las páginas web. En este contexto, "declarativo" significa que con HTML declaras qué elementos deben aparecer en la página web y en qué orden, pero no cómo deben implementarse o renderizarse, eso es manejado por el navegador web.

  * **CSS**: utilizado para describir la presentación de las páginas web. Sí, CSS (Cascading Style Sheets) es considerado un lenguaje declarativo. Al igual que HTML, no es un lenguaje de programación en el sentido tradicional, ya que no tiene estructuras de control como bucles o condicionales. Sin embargo, es un lenguaje en el sentido de que tiene una sintaxis y reglas definidas que se utilizan para describir la presentación de las páginas web. En este contexto, "declarativo" significa que con CSS declaras cómo deben verse los elementos en la página web, pero no cómo se implementa esa presentación, eso es manejado por el navegador web.

  * **Prolog**: utilizado en inteligencia artificial y lingüística computacional.

  * **Haskell**: un lenguaje de programación funcional que también es declarativo.

  * **XSLT**: utilizado para transformar documentos XML.

  * **Terraform**: utilizado para describir infraestructura como código.

### Programación reactiva (2000s) 

La programación reactiva es un paradigma enfocado en la programación y el trabajo con flujos de datos finitos o infinitos de manera asíncrona y la propagación de cambios. Se basa en escuchar lo que emite un evento o cambios en el flujo de datos, en donde los objetos reaccionan a los valores que reciben de dicho cambio.

Ha ganado popularidad en los últimos años con lenguajes y bibliotecas como React.js y RxJava.

React/Angular usan RxJs para hacer uso de la programación reactiva.

Su concepción y evolución ha ido ligada a la publicación del Reactive Manifesto, que establecía las bases de los sistemas reactivos, los cuales deben ser:

  * **Responsivos**: aseguran la calidad del servicio cumpliendo unos tiempos de respuesta establecidos.

  * **Resilientes**: se mantienen responsivos incluso cuando se enfrentan a situaciones de error.

  * **Elásticos**: se mantienen responsivos incluso ante aumentos en la carga de trabajo.

  * **Orientados a mensajes**: minimizan el acoplamiento entre componentes al establecer interacciones basadas en el intercambio de mensajes de manera asíncrona.

La motivación detrás de este nuevo paradigma procede de la necesidad de responder a las limitaciones de escalado presentes en los modelos de desarrollo actuales, que se caracterizan por su desaprovechamiento del uso de la CPU debido a la interacción de entrada y salida (I/O), el sobre uso de memoria y la ineficiencia de las interacciones bloqueantes.

!!! important "¡Para recordar!"
    Cada paradigma tiene sus propias ventajas y desventajas, y se adapta mejor a ciertos tipos de problemas que a otros. 

    Es importante tener en cuenta que estos paradigmas no son mutuamente excluyentes.  
    
    Muchos lenguajes modernos, como Python y JavaScript, adoptan uno o varios paradigmas en función del tipo de órdenes que permiten implementar, es decir, son soportan múltiples paradigmas o son multi paradigmas.  
    
    Además, nuevos paradigmas continúan emergiendo a medida que los desarrolladores buscan nuevas formas de abordar los problemas de programación.
