title: Identificador de una constante

# Identificador de una constante

<label class="revision">Rev. 15/01/2024</label>

!!! abstract "Definición"
    El identificador de una constante es el nombre que se le da a la constante para identificarla en el código. A partir de los identificadores, los programadores pueden referirse a cada constante en otras partes del código.

Generalmente, se diferencia una constante de una variable en que el nombre de la constante está definido todo en mayúsculas. Por ejemplo:

``` Go title="Código generalizado"
int MI_CONSTANTE = 10
print(MI_CONSTANTE) // Output: 10
```

> En el código anterior `int MI_CONSTANTE = 10`, `MI_CONSTANTE` es el identificador de la constante. Cada vez que se usa `MI_CONSTANTE` en el código, se está haciendo referencia al valor almacenado en ella, el valor `10`.

Además, en muchos lenguajes de programación, las constantes se definen usando una palabra clave especial, que generalmente suele ser `const`. Veamos algunas declaraciones de constantes en diferentes lenguajes:

``` js title="JavaScript"
const PI = 3.14159;
```

``` C++ title="C++"
const double PI = 3.14159;
```

``` C# title="C#"
const double PI = 3.14159;
```

>> En otros lenguajes, la palabra clave puede variar, como en Java, donde se pueden declarar constantes utilizando la palabra clave `final`:

``` java title="Java"
public static final double PI = 3.14159;
```

En todos estos lenguajes, una vez que se ha asignado un valor a la constante PI, no se puede cambiar. Si intentas hacerlo, el compilador o el intérprete te dará un error.

!!! warning "¿Qué ocurre en Python?"
    En Python, una constante es un tipo de variable cuyo valor no se puede cambiar. Aunque Python no tiene soporte nativo para constantes, por convención, los desarrolladores usan nombres de variables en mayúsculas para indicar que una variable debe tratarse como una constante y no debe modificarse.

    ``` py title="Python"
    PI = 3.14159
    ```

    En este ejemplo, `PI` es una "constante". Debería ser entendido que no se debe cambiar el valor de `PI` en ninguna parte del código después de su definición inicial, aunque técnicamente es posible hacerlo y durante la ejecución del programa no se sucederá ningún error.

## Reglas para definir el identificador de una constante

En la mayoría de los lenguajes de programación, las reglas para los identificadores de constantes son las mismas que para las variables.

Las convenciones de nombramiento (_naming conventions_), son reglas o guías que se utilizan para determinar cómo nombrar las constantes en la programación. Estas convenciones pueden variar dependiendo del lenguaje de programación. Pero recuerda que son las mismas reglas o guías que se utilizan para determinar cómo nombrar las variables. Así que, si necesitas repasarlas, puedes acceder a la documentación haciendo clic [aquí](../../variables/identificador-de-una-variable/#pautas-generales para-nombrar-variables){:target="_blank"}.

!!! important "¡Para recordar!"
    Es importante notar que aunque las reglas para los identificadores son las mismas, las constantes y las variables se comportan de manera diferente. Una vez que se asigna un valor a una constante, no puedes cambiarlo, mientras que si puedes cambiar el valor de una variable las veces que quieras.