title: Expresiones, sentencias y bloques de sentencias: resumen

## Expresiones

Una expresión está conformada por un operando (variable, constante literal o resultado de una llamada a función o método) o la combinación de uno o más operandos y operadores (aritméticos, lógicos o relacionales), construida de acuerdo con la sintaxis del lenguaje, que, al ser procesada (evaluada o sometida a un cálculo u operación), devuelve como resultado un valor.

Por lo tanto, el resultado de una expresión se puede calcular realizando las operaciones en el orden dictado por la precedencia de los operadores.

Las expresiones realizan el trabajo de un programa. Entre otras cosas, las expresiones se utilizan para calcular y asignar valores a las variables y para ayudar a controlar el flujo de ejecución de un programa. 

El trabajo de una expresión es doble: 
* realizar el cálculo indicado por los elementos de la expresión; y 
* devolver un valor que es el resultado de dicho cálculo.

Una expresión válida puede ser simple o compleja. También puede haber una expresión como parte de otra, o como argumento de una función. Esto se denomina anidamiento de una expresión.

* Expresiones con **operadores de asignación**
* Expresiones con **operadores aritméticos**
* Expresiones con **operadores de comparación**
* Expresiones con **operadores de concatenación**
* Expresiones con **operadores de repetición**
* Expresiones **con operadores lógicos**
* Expresiones **con operadores de incremento**
* Expresiones **con operadores de decremento**

Puede escribir expresiones compuestas combinando expresiones siempre que los tipos de dato requeridos por todos los operadores involucrados en la expresión compuesta sean correctos. 

Al escribir expresiones compuestas, debe ser explícito e indicar entre paréntesis qué operadores deben evaluarse primero. Si elige no usar paréntesis, se evalúa la expresión compuesta en el orden dictado por la precedencia del operador. 

Puedes combinar expresiones simples utilizando operadores y agrupando las expresiones con paréntesis para obtener resultados más complejos y realizar tareas más avanzadas en tus programas.

Llamamos expresiones literales al ejemplo más simple de expresión que representa directamente a su valor. 

Cada lenguaje de programación tiene su propia sintaxis aunque los conceptos básicos se mantienen consistentes en la mayoría de los casos.

Cuando las expresiones contienen operandos de diferentes tipos de dato, algunas operaciones se llevan a cabo de manera directa y otras mediante una conversión (casting) implícita de estos tipos de dato, si es necesario, dependiendo de las reglas del lenguaje específico. Así, La manera en que se realizan las asignaciones puede variar según las operaciones y el tipo de dato utilizado.

## Sentencias

Una expresión es siempre parte de una sentencia, también conocida como instrucción o declaración. Incluso si es solo una expresión únicamente.

Una sentencia es un conjunto de expresiones que permiten ejecutar una determinada acción y, dependiendo del lenguaje de programación, es necesario que termine con un punto y coma. 

Las sentencias más comunes son: 
* sentencias de declaración
* sentencias de expresión
* sentencias de flujo de control

En términos generales, una sentencia es una unidad de instrucciones con significado completo (también llamada línea de código), que puede ser comprendida en el contexto del lenguaje natural o interpretada y ejecutada por un programa informático, cuya acción resuelve una parte o la totalidad de un problema. 
Cada sentencia, siempre, contiene una o más expresiones.

* Las expresiones que son procesadas siempre retornan un valor. 
* Cada sentencia, siempre, contiene una o más expresiones.
* Un programa consiste en una serie de sentencias.

Estos son algunos de los tipos de sentencias más utilizados en programación:

* **Sentencias de declaración** (_declaration statements_)  
* **Sentencias de inicialización** (_inline initialization statements_)  
* **Sentencias de asignación** (_assignment statements_)  
* **Sentencias de expresión** (_expression statements_) 
* **Sentencias de control de flujo** (_flow control statements_)
    * **Sentencias de selección** (_selection statements_) 
    * **Sentencias de iteración** (_iteration statements_) 
    * **Sentencias de salto** (_jump statements_) 
    * **Sentencias de manejo de excepciones** (_exception handling statements_)
* **Sentencias etiquetadas** (_labeled statements_) 
* **Sentencias de llamada a función** (_function call statements_)
* **sentencias compuestas** (_compound statements_) 

!!! important "¡Para recordar!"
    Puedes agrupar dos o más sentencias juntas en un bloque con llaves ( { } ) o indentando (tabulando), según el lenguaje de programación en cuestión, formando el bloque de sentencias correspondiente.

    Aunque no es obligatorio, se recomienda usar bloques en las sentencias de control de flujo, aún si solo hay una sentencia en el bloque. Esto permite una lectura más agil y ordenda del programa.

    Es importante siempre consultar la documentación del lenguaje de programación específico que estés utilizando para obtener información precisa sobre las operaciones disponibles y cómo utilizarlas correctamente en tu programa. 
