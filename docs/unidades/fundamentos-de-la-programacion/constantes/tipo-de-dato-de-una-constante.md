title: Tipo de dato de una constante

# Tipo de dato de una constante

<label class="revision">Rev. 15/01/2024</label>

!!! abstract "Definición"
    El tipo de dato de una constante se refiere al tipo de valor que la constante puede almacenar. Este tipo de dato se determina en el momento de la declaración de la constante, de manera explícita (con una palabra clave) o por el valor que se le asigna, y no puede cambiarse después.

El tipo de dato de una constante determina qué tipo de operaciones puedes realizar con la constante y cómo se comportará en diferentes contextos. Por ejemplo, no puedes realizar operaciones matemáticas con una constante de tipo cadena, y no puedes usar una constante de tipo entero o flotante donde se espera una cadena.

En algunos lenguajes de programación, como Java y C++, debes especificar explícitamente el tipo de dato de la constante en el momento de la declaración. Por ejemplo:

``` Java title="Java"
public static final int INT_CONST = 10;
public static final String STRING_CONST = "Hello, world!";
public static final boolean BOOLEAN_CONST = true;
```

``` C++ title="C++"
const int INT_CONST = 10;
const char* STRING_CONST = "Hello, world!";
const bool BOOLEAN_CONST = true;
```

En otros lenguajes de programación, como JavaScript, el tipo de dato de la constante se infiere del valor que se le asigna en el momento de la declaración. No necesitas especificar explícitamente el tipo de dato. Por ejemplo:

``` js title="JavaScript"
const NUMBER_CONST = 10;
const STRING_CONST = 'Hello, world!';
const BOOLEAN_CONST = true;
const OBJECT_CONST = { key: 'value' };
const ARRAY_CONST = [1, 2, 3];
```

Por lo tanto, aunque la sintaxis y las reglas exactas pueden variar, la idea general de que las constantes tienen un tipo de dato asociado es común en muchos lenguajes de programación.