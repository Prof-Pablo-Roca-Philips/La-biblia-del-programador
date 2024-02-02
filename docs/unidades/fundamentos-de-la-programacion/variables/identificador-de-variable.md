title: Identificador de una variable

# Identificador de una variable

<label class="revision">Rev. 11/01/2024</label>

!!! abstract "Definición"
    El identificador de una variable es el nombre que se le da a la variable para identificarla en el código. A partir de los identificadores, los programadores pueden referirse a cada variable en otras partes del código.

Por ejemplo:

``` Go title="Código generalizado"
int mi_variable = 10
print(mi_variable) // Output: 10
```

> En el código anterior `int mi_variable = 10`, `mi_variable` es el identificador de la variable. Cada vez que se usa `mi_variable` en el código, se está haciendo referencia al espacio de memoria que almacena el valor `10`.

Los identificadores de las variables deben seguir ciertas reglas y convenciones dependiendo del lenguaje de programación.

## Reglas para definir el identificador de una variable

Las convenciones de nombramiento (_naming conventions_), son reglas o guías que se utilizan para determinar cómo nombrar las variables en la programación. Estas convenciones pueden variar dependiendo del lenguaje de programación.

Estudiemos las reglas más importantes que suelen aplicarse en la mayoría de los lenguajes:

1. **Evitar elegir nombres crípticos**: Los nombres crípticos son aquellos que no son claros o intuitivos, lo que dificulta la comprensión del código. Es decir, que resultan incomprensibles o enigmáticos para quien no posea una clave de interpretación adecuada.

    !!! failure "Mala práctica"
        ``` py
        p = 3.14159
        x1 = 10
        n = "John Doe"
        f = calculate()
        ```

    > ¿Qué representa `p`? Podría ser más claro si se llamara `pi`.  
    > ¿Qué es `x1`? ¿Hay un `x2`? ¿Por qué no `primer_valor` o algo similar?  
    > ¿Qué es `n`? ¿Un nombre? ¿Un número? Sería más claro si se llamara `nombre`.  
    > ¿Qué es `f`? ¿Una función? ¿Un resultado? ¿Por qué no `resultado`?

2. **Evitar abreviaturas**: A menos que la abreviatura sea ampliamente conocida, es mejor evitarla para mantener la legibilidad del código.

3. **Elegir nombres claros y descriptivos (semánticos)**: Las variables deben tener nombres que indiquen claramente qué datos almacenan, facilitando la lectura y fácil entendimiento del código. Por ejemplo, en lugar de nombrar una variable `x`, sería mejor nombrarla `edad` si almacena la edad de una persona:

    !!! failure "Mala práctica"
        ``` py
        dato = "Pablo"
        x = 45 
        n = 1
        ```

    !!! success "Buena práctica"
        ``` py
        nombre = "Pablo"
        edad = 45 
        mascotas = 1
        ```

    Como se ve en el ejemplo, utiliza sustantivos: las variables suelen representar objetos o valores en el código, por lo que es recomendable utilizar sustantivos para identificarlas.  

4. **Elegir nombres en tu idioma**: Los identificadores deben estar escritos en tu idioma, a menos que estés trabajando en un proyecto que especifique otro idioma diferente.
  
    Esto mantendrá la consistencia de idioma entre variables y los textos, facilitando el entendimiento del código y la colaboración con otros desarrolladores.  

    Eso si, procura no utilizar caracteres especiales como los acentuados o la letra eñe. ya que podría originar problemas a la hora de ejecutar el programa por alguna compatibilidad de caracteres.

5. **Evitar elegir nombres largos**: Aunque es importante que el nombre sea descriptivo, evita nombres demasiado largos. Es conveniente que la longitud de nombre no pase de 10 caracteres. Y nunca más de 32 caracteres.  

    Nombres demasiado largos pueden hacer que el código sea difícil de leer y escribir.  

    Encuentra un equilibrio entre la claridad y la concisión.

6. **Iniciar con una letra o guión bajo**: La mayoría de los lenguajes de programación requieren que los nombres de las variables comiencen con una letra o un guión bajo ( _ ), pudiendo contener tanto letras mayúsculas y minúsculas como dígitos o guiones bajo combinados como se desee; pero **nunca deben comenzar con un número** porque la computadora confundirá el identificador con un número decimal inválido.

    ``` Go title="Código generalizado"
    1er_jugador = "Pablo" 
    ```

    > `1er_jugador` no es un identificador de variable válido porque se confunde con un número decimal inválido.

    > Al ejecutar el código, la computadora confundirá el nombre de la variable con un número inválido, deteniendo la ejecución del programa por un error de sintaxis:

    ``` title="Terminal (Entrada/Salida)"
    File "…", line 1
        1er_jugador = "Pablo"
        ^
    SyntaxError: invalid decimal literal
    ```

7. **No usar caracteres especiales**: Exceptuando el guión bajo ( _ ), los nombres de las variables no deben contener caracteres especiales como el guión medio, el punto, la coma, las comillas, porcentaje, numeral, etc. puesto que estos símbolos cumplen con otras funciones y si se intentan utilizar como parte de un identificador, esto resultará en un error de sintaxis inválida:

    ``` py
    string %_de_desaprobados = 30
    ```

    > Al ejecutar el código, el programa se detendrá con un mensaje de error:

    ``` title="Terminal (Entrada/Salida)"
    File "…", line 1
        %_de_desaprobados = 10
        ^
    SyntaxError: invalid syntax
    ```

8. **Case sensitive**: En muchos lenguajes de programación, los nombres de las variables distinguen entre mayúsculas y minúsculas. Por lo tanto, `variable`, `Variable` y `vARIABLE` serían tres variables diferentes.

9. **No debe contener espacios**: El nombre de una variable no puede estar compuesto por dos o más palabras separadas por espacios, puesto que la computadora no puede discriminar cuando esto equivale a un nombre compuesto o no. Es decir, no puede delimitar que palabras pertenecen a un único nombre o pertenecen a algo más, resultando en una sintaxis inválida:
    
    ``` py
	nombre y apellido = "Pablo Roca"
    ```

    > El identificador es inválido porque resulta en un conjunto de palabras que arman una sintaxis inválida. Al ejecutar el código, el programa se detendrá con un mensaje de error:

    ``` title="Terminal (Entrada/Salida)"
    File "…", line 1
        nombre y apellido = "Pablo Roca"
               ^
    SyntaxError: invalid syntax
    ```


10. **Usar camelCase o snake_case (_casing_)**: Ambas convenciones de nombramiento forman parte del concepto de _casing_ que determina cómo se combinan las palabras y cómo se utilizan las letras mayúsculas y minúsculas en un identificador. La elección entre una y otra dependerá del lenguaje de programación y las convenciones del equipo de desarrollo. Veremos este tema en un momento.

    * En **_camelCase_**, la primera letra de cada palabra, excepto la primera, es mayúscula (por ejemplo, `miVariable`). 

    * En **_snake_case_**, todas las letras son minúsculas y las palabras se separan con guiones bajos (por ejemplo, `mi_variable`). 

    Antes de empezar a escribir con tu código, elige un estilo de _casing_ y aplícalo de manera consistente y unificada a tus identificadores a lo largo de todo el código.

11. **Evitar elegir palabras reservadas**: Los nombres de las variables no deben ser palabras reservadas en el lenguaje de programación. Las palabras reservadas son palabras que tienen un significado especial en un lenguaje de programación y no pueden ser utilizadas para otros propósitos, como nombres de variables o funciones. 

    Aquí enumeramos algunos ejemplos de palabras reservadas en varios lenguajes de programación:

    <div class="force-word-wrap">

    ``` title="Python"
    and, as, assert, break, class, continue, def, del, elif, else, except, False, finally, for, from, global, if, import, in, is, lambda, None, nonlocal, not, or, pass, raise, return, True, try, while, with, yield
    ```

    ``` title="JavaScript"
    abstract, arguments, await, boolean, break, byte, case, catch, char, class, const, continue, debugger, default, delete, do, double, else, enum, eval, export, extends, false, final, finally, float, for, function, goto, if, implements, import, in, instanceof, int, interface, let, long, native, new, null, package, private, protected, public, return, short, static, super, switch, synchronized, this, throw, throws, transient, true, try, typeof, var, void, volatile, while, with, yield
    ```

    ``` title="Java"
    abstract, assert, boolean, break, byte, case, catch, char, class, const, continue, default, do, double, else, enum, extends, final, finally, float, for, goto, if, implements, import, instanceof, int, interface, long, native, new, package, private, protected, public, return, short, static, strictfp, super, switch, synchronized, this, throw, throws, transient, try, void, volatile, while
    ```

    ``` title="Python"
    alignas, alignof, and, and_eq, asm, auto, bitand, bitor, bool, break, case, catch, char, char8_t, char16_t, char32_t, class, compl, concept, const, consteval, constexpr, constinit, const_cast, continue, co_await, co_return, co_yield, decltype, default, delete, do, double, dynamic_cast, else, enum, explicit, export, extern, false, float, for, friend, goto, if, inline, int, long, mutable, namespace, new, noexcept, not, not_eq, nullptr, operator, or, or_eq, private, protected, public, register, reinterpret_cast, requires, return, short, signed, sizeof, static, static_assert, static_cast, struct, switch, template, this, thread_local, throw, true, try, typedef, typeid, typename, union, unsigned, using, virtual, void, volatile, wchar_t, while, xor, xor_eq
    ```

    </div>

    Estas palabras reservadas varían de un lenguaje a otro, por lo que es importante conocer las palabras reservadas del lenguaje que estás utilizando para evitar utilizarlas como identificadores.

!!! important "¡Para recordar!"
    Cuando definas los identificadores para tus variables, es importante respetar las convenciones de nombramiento (**_naming convention_**) para hacer tu código legible y permitir un mantenimiento ágil y simple.

!!! warning "¡Olvidar estas reglas te dará mucho dolor de cabeza!"
    Estas reglas son generales, muy importantes y pueden variar dependiendo del lenguaje de programación que estés utilizando. 
      
    ¡Desconocerlas te llevará a nombrar tus variables de manera incorrecta y seguramente esto hará que tu código falle!

## Ejemplos de identificadores válidos

* **numero**: Este es un identificador válido en la mayoría de los lenguajes de programación. Se puede usar para representar un número, como un entero o un flotante.

* **dia_del_mes**: Este es un identificador válido en lenguajes que permiten el uso de guiones bajos en los nombres de las variables. Se puede usar para representar un día del mes.

* **pinguino1**: Este es un identificador válido en la mayoría de los lenguajes de programación. Se puede usar para representar un objeto, como un pinguino en un juego.

* **ciudad**: Este es un identificador válido en la mayoría de los lenguajes de programación. Se puede usar para representar una cadena de texto, como el nombre de una ciudad.

* **x**: Este es un identificador válido en la mayoría de los lenguajes de programación. Se puede usar para representar cualquier tipo de dato.

* **_x**: Este es un identificador válido en la mayoría de los lenguajes de programación. Aunque no es común, se permite que los identificadores comiencen con un guión bajo.

## Ejemplos de identificadores inválidos

* **123**: Este es un identificador inválido en la mayoría de los lenguajes de programación porque los identificadores no pueden comenzar con un número.

* **_día**: Este es un identificador inválido en algunos lenguajes de programación porque contiene un carácter especial (la tilde). Los identificadores deben consistir solo en letras no acentuadas, números y guiones bajos.

* **numero***: Este es un identificador inválido en la mayoría de los lenguajes de programación porque contiene un carácter especial (el asterisco). Los identificadores no pueden contener caracteres especiales.

* **lugar de nacimiento**: Este es un identificador inválido en la mayoría de los lenguajes de programación porque contiene un espacio. Los identificadores no pueden contener espacios.

* **año**: Este es un identificador inválido en algunos lenguajes de programación porque contiene un carácter especial (la tilde o virgulilla). Los identificadores deben consistir solo en letras no acentuadas, números y guiones bajos.

* **print**: Este es un identificador inválido en algunos lenguajes de programación porque es una palabra reservada. Las palabras reservadas no pueden usarse como identificadores.

!!! important "¡Para recordar!"
    Los identificadores de las variables deben seguir ciertas reglas y convenciones dependiendo del lenguaje de programación.  
    Por lo general, deben comenzar con una letra o un guion bajo ( _ ), y pueden contener letras, números y guiones bajos.  
    No pueden contener caracteres ni símbolos especiales que cumplan otras funciones dentro del lenguaje de programación.  
    Tampoco, pueden ser palabras reservadas del lenguaje de programación.

    El nombre asignado como identificador de una variable debe ser descriptivo y significativo, de manera que refleje el propósito o contenido del dato que almacenará la variable.  
    Las convenciones de nombramiento pueden variar según el lenguaje de programación que estés utilizando, así como las directrices establecidas por la comunidad o los estándares de codificación. 

    Es recomendable consultar la documentación o guías de estilo correspondientes al lenguaje o entorno en el que estés trabajando para seguir las mejores prácticas específicas.

## _Casing_ para identificador de variable

El concepto de _casing_ en programación se refiere a la convención utilizada para escribir identificadores, como identificadores de variables, funciones, clases, etc. cuando, en general, dicho identificador se compone de dos o más palabras para nombrarlo. 

El _casing_ determina cómo se combinan las palabras y cómo se utilizan las letras mayúsculas y minúsculas en un identificador. 

Aquí hay algunos ejemplos de estilos de _casing_:

* **Camel Case** (camelCase): La primera letra del identificador es minúscula, y la primera letra de cada palabra subsiguiente es mayúscula, sin espacios ni guiones entre las palabras. 

    ```
    cosasParaHacer, edadDelAmigo, valorFinal
    ```

* **Pascal Case** (PascalCase): También conocido como Upper Camel Case, la primera letra de cada palabra en el identificador es mayúscula, sin espacios ni guiones entre las palabras.

    ```
    CosasParaHacer, EdadDelAmigo, ValorFinal
    ```

* **Snake Case** (snake_case): Todas las letras son minúsculas y las palabras se separan con guiones bajos ( _ ). 

    ```
    cosas_para_hacer, edad_del_amigo, valor_final
    ```     

* **Kebab Case** (kebab-case): Todas las letras son minúsculas y las palabras se separan con guiones medios ( - ). 
		
    ```
    cosas-para-hacer, edad-del-amigo, valor-final
    ```
    
    !!! warning "¡Presta atención y cuidado!"
        Los nombre de variable en Kebab Case, en algunos lenguajes son interpretados como la resta de dos o más variables.

El uso de estas convenciones ayudan a mejorar la legibilidad del código y a mantener la consistencia en todo el código fuente. 

!!! important "¡Para recordar!"
    La elección de la convención de _casing_ puede depender del lenguaje de programación, del equipo de desarrollo, o de las preferencias personales.
    