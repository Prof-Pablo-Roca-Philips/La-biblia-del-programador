title: ¿Qué son las constantes?

# ¿Qué son las constantes?

<label class="revision">Rev. 15/01/2024</label>

!!! abstract "Definición"
    En programación, una constante es un tipo de identificador en programación que almacena un valor inmutable (que no puede ser modificado durante la ejecución del programa) una vez que se ha asignado, durante la ejecución del programa. 

    Las constantes se utilizan para representar valores que son fijos, literales, que se conocen de antemano como el número pi en matemáticas, o configuraciones que no deben cambiar una vez que el programa está en ejecución, como números específicos, valores _booleanos_ que representen un estado particular (verdadero/falso) o una cadena de conexión a una base de datos.
    
Cuando se declara una constante, se le asigna un valor inicial y este valor permanece inmutable durante todo el ciclo de vida del programa.

Cuando se dice que una constante se trata como un valor literal en el código, significa que cada vez que se usa la constante en el código, se reemplaza directamente por su valor. No es una referencia a una ubicación de memoria, como puede ser una variable. Por lo tanto, no puedes cambiar el valor de una constante como podrías hacer con una variable.

Las constantes, al igual que las variables, tienen **Identificador**, **alcance**, **tipo de dato** y **valor**, aunque este último es inmutable.

!!! success "¡Para recordar!"
    Ya vimos que una variable es un identificador que se utiliza para almacenar un valor que puede cambiar durante la ejecución del programa. 
    
    A diferencia de una constante, una variable es una referencia a una ubicación en la memoria donde se almacena un valor. Esto significa que puedes cambiar el valor almacenado en esa ubicación de memoria, haciendo referencia a la variable.

    Si necesitas un valor que no cambie durante la ejecución de tu programa, debes usar una constante. Si necesitas un valor que pueda cambiar, debes usar una variable.

    La forma exacta de definir una constante puede variar de un lenguaje de programación a otro, pero el concepto subyacente es el mismo.