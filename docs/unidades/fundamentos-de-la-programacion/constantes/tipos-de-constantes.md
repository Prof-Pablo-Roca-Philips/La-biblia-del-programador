title: Tipos de constantes

# Tipos de contantes

<label class="revision">Rev. 15/01/2024</label>

Existen dos tipos principales de constantes: constantes literales y constantes de nombre simbólico.

* **Constante expresada por su valor literal**: Una constante literal es un valor específico, expresado en forma explícita, que se utiliza directamente en el código. Se escribe como tal en el código y no puede ser referenciado ya que no posee un identificador asociado.

    ``` Go title="Constante literal"
    print(3.14159) 
    ```

    > `3.14159` es una constante literal. Se utiliza directamente en el código y no puede ser referenciado ya que no posee un identificador asociado.

* **Constante expresada con un nombre simbólico**: Una constante de nombre simbólico es un identificador, escrito en mayúsculas, que se utiliza para representar un valor constante. En lugar de utilizar directamente el valor en el código, se utiliza el nombre simbólico para referirse a él. Esto hace que el código sea más legible y fácil de mantener, ya que si el valor de la constante cambia, solo es necesario actualizar el valor en un solo lugar.

    ``` Go title="Constante de nombre simbólico"
    float PI = 3.14159
    print (PI)
    ```
 
    > `PI` es una constante de nombre simbólico. El valor `3.14159` se encuentra almacenado en un espacio de memoria asociado a un nombre simbólico `PI`. Este nombre asociado siempre se escribe en mayúsculas. Así, este valor se referencia en el código a partir de su identificador asociado. 
    
    > Si el valor de `PI` cambia en el futuro, solo es necesario actualizar el valor en un solo lugar (la declaración de la constante "`PI`") en lugar de buscar y reemplazar todas las ocurrencias del valor literal en el código. Esto hace que el código sea más legible y menos propenso a errores.

### Ventajas y desventajas de cada tipo

**Ventajas de las constantes literales:**

  * Son simples y directas.
  * No requieren ninguna declaración previa.

**Desventajas de las constantes literales:**

  * No son descriptivas. No es inmediatamente claro qué representa el valor.
  * Si necesitas cambiar el valor, tendrías que buscar y cambiar todas las ocurrencias en el código.

**Ventajas de las constantes de nombre simbólico:**

  * Son descriptivas. El nombre de la constante puede indicar claramente qué representa el valor.
  * Si necesitas cambiar el valor, solo necesitas cambiarlo en la declaración de la constante.

**Desventajas de las constantes de nombre simbólico:**

  * Requieren una declaración previa.
  * Pueden ocupar más espacio en el código, especialmente si el nombre de la constante es largo.

!!! important "¡Para recordar!"
    Las constantes de nombre simbólico tienen varias ventajas en la programación: 

    * En primer lugar, ayudan a mejorar la legibilidad del código, ya que proporcionan información clara sobre el propósito o el significado de un valor en particular. 
    * Además, el uso de nombres simbólicas en lugar de valores literales directamente en el código hace que sea más fácil realizar cambios y actualizaciones en el programa, ya que solo es necesario modificar el valor de la constante en un lugar para que tenga efecto en todo el programa donde es utilizada.