title: Características de las constantes

# Características de las constantes

<label class="revision">Rev. 15/01/2024</label>

Al igual que las variables, las constantes poseen cuatro características distintivas:

* **Tipo de dato asociado**

    El tipo de dato de una constante se refiere al tipo de valor que la constante puede almacenar. Este tipo de dato se determina en el momento de la declaración de la constante, de manera explícita (con una palabra clave) o por el valor que se le asigna, y no puede cambiarse después.

    Los tipos de datos comunes incluyen números enteros, números flotantes (números con decimales), caracteres (_char_), valores lógicos o _booleanos_ (verdadero o falso), entre otros.

    Es importante definir correctamente el tipo de dato de la constante para poder almacenar el valor correspondiente de manera exacta.
    
    Además, los diferentes tipos de dato pueden afectar las operaciones que puedes realizar con la constante.

    Estudiaremos esta característica más adelante; o podrías consultarla ahora, si quisieras, haciendo clic [aquí](../tipo-de-dato-de-una-constante){:target="_blank"}.

    ---

* **Identificador o Nombre**

    El identificador de una constante es el nombre que se le da a la constante.
    
    Se utiliza para referenciar, es decir identificar, la constante durante de la ejecución del programa, desde el momento en que se crea la constante hasta el momento en que se destruye o que finaliza el programa, lo que ocurra primero. También se suele hablar de **nombre** de constante.

    En la mayoría de los lenguajes de programación, las reglas para los identificadores de constantes son las mismas que para las variables. Estas reglas pueden variar de un lenguaje a otro, pero generalmente el identificador de una constante se define todo en mayúsculas, respetando las reglas.

    Así, para definir un _identificador_ válido, se deberá elegir un nombre en mayúsculas y respetar las convenciones de nombramiento (**_naming convention_**) para hacer el código legible y permitir un mantenimiento ágil y simple.
    
    Estudiaremos esta característica más adelante; o podrías consultarla ahora, si quisieras, haciendo clic [aquí](../identificador-de-una-constante/#pautas-generales-para-nombrar-constantes){:target="_blank"}.

    ---

* **Alcance**

    El alcance de una constante se refiere a la región o parte de código donde una constante existe y es accesible para poder ser utilizada. 
    
    Hay dos tipos principales de alcance: **local**, limitado a la parte del código donde esa constante existe y puede ser accedida; o **global**, accesible desde cualquier parte del código.
    
    Es fundamental que la constante cuente con el alcance adecuado para que sea visible y pueda ser accedida en las regiones o partes de código que precisen interactuar con ella.

    Estudiaremos esta característica más adelante; o podrías consultarla ahora, si quisieras, haciendo clic [aquí](../alcance-de-una-constante/){:target="_blank"}.

    ---

* **Dato asignado**

    Un **dato asignado** a una constante es un valor que se establece al definir la constante y que no puede cambiar durante la ejecución del programa. En otras palabras, una vez que se asigna un valor a una constante, ese valor permanece inmutable.
    
    Este dato asignado deberá ser del mismo tipo de dato asociado a la constante.

    Estudiaremos esta característica más adelante; o podrías consultarla ahora, si quisieras, haciendo clic [aquí](../dato-asignado-a-una-constante/){:target="_blank"}.

En términos generales, un dato asignado a una constante es un valor que no cambia durante la ejecución del programa. Una vez que se asigna un valor a una constante, no puede ser modificado posteriormente.