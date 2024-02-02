title: Alcance de variable

# Alcance de una variable

<label class="revision">Rev. 11/01/2024</label>

Un concepto muy importante en programación es lo que llamamos alcance de una variable (_variable scope_).

!!! abstract "Definición"
    El alcance de una variable se refiere a la parte del código donde una variable existe y es accesible para poder ser utilizada por el programa. 
    
    Hay dos tipos principales de alcance: **local**, limitado a la parte del código donde esa variable existe y puede ser accedida; o **global**, accesible desde cualquier parte del código.

## ¿Qué es el ámbito de aplicación?

En el contexto de la programación, los términos "ámbito" y "alcance" se utilizan a menudo de manera intercambiable para referirse a la región o parte de código donde una variable es visible y accesible.

Por ejemplo, si decimos que una variable tiene "alcance local", significa que la variable es accesible solo dentro de la región o parte de código donde se declara. De manera similar, si decimos que una variable está en el "ámbito local", estamos diciendo lo mismo.

Entonces, el **ámbito** de aplicación de una variable es el **alcance** que tiene la variable, que no es ni más ni menos que la región o parte de código donde la variable existe y es accesible.

Por lo tanto, puedes usar cualquiera de los dos términos para describir dónde una variable puede ser utilizada en tu código.

## ¿Ámbito global o ámbito local?

Hemos dicho que básicamente podemos dividir a las variables, en función del ámbito de aplicación donde existen y son accesibles, como **locales** o **globales**.  
Y que la principal diferencia entre una variable global y otra local radica en su alcance o ámbito de aplicación, es decir, en la región o parte de código donde son visibles y accesibles.

Evaluemos un ejemplo de utilización de variables globales y locales en Python:

``` py title="Python" linenums="1"
# Variable global
a = 10

def mi_funcion():
    # Variable local
    b = 20
    print(a)  # Esto es válido, porque 'a' es global
    print(b)  # Esto es válido, porque 'b' es local a esta función

mi_funcion()

print(a)  # Esto es válido, porque 'a' es global
print(b)  # Esto dará un error, porque 'b' es local a 'mi_funcion' y no existe aquí
```

> El código anterior demuestra la diferencia entre las variables globales y las variables locales:

> `a = 10`: Aquí, `a` es una variable global. Se declara fuera de cualquier función, por lo que es accesible desde cualquier lugar del código.
> 
> `def mi_funcion()`: Esta es la definición de una función llamada `mi_funcion`.
> 
> `b = 20`: Dentro de `mi_funcion`, se declara `b` como una variable local. Solo es accesible dentro de `mi_funcion`.
> 
> `print(a)`: Dentro de `mi_funcion`, se puede acceder a la variable global `a`. Por lo tanto, esta línea imprimirá el valor de `a`, que es `10`.
> 
> `print(b)`: También se puede acceder a la variable local `b` dentro de `mi_funcion`. Esta línea imprimirá el valor de `b`, que es `20`.
> 
> `mi_funcion()`: Esta línea llama a `mi_funcion`, lo que provocará que se impriman los valores de `a` y `b`.
> 
> `print(a)`: Después de llamar a `mi_funcion`, esta línea imprime el valor de la variable global `a` nuevamente. Esto es válido y imprimirá `10`.
> 
> `print(b)`: Intenta imprimir el valor de `b`. Sin embargo, dado que `b` es una variable local a `mi_funcion`, no es accesible fuera de esa función. Por lo tanto, esta línea dará un error, indicando que `b` no está definida.

Estudiaremos estos conceptos con mayor profundidad, a continuación.

### Variable de alcance global

El ámbito donde se encuentra el código principal de un programa, generalmente definido como `main()` en algunos lenguajes, se llama **ámbito global**. 

!!! important "¡Para recordar!"
    En la mayoría de los lenguajes de programación, incluyendo Python, cualquier código que no está dentro de una función o clase se ejecuta en el ámbito global.

Por lo tanto, una variable global es aquella que se define en el código principal de un programa fuera de cualquier otro ámbito, como ser funciones o bloques de código, por ejemplo. 

Las variables globales existen, son visibles, son accesibles y pueden ser modificadas desde cualquier parte del código. Por este motivo, su uso debe ser limitado ya que puede llevar a comportamientos inesperados debido a modificaciones no controladas.

Aquí tenemos varios ejemplos en diferentes lenguajes:

``` py title="Python"
variable_global = "Soy una variable global"

def mi_funcion():
    print(variable_global)  # Esto es válido! Output : Soy una variable global

mi_funcion()  
```

``` js title="JavaScript"
var variableGlobal = "Soy una variable global";

function miFuncion() {
    console.log(variableGlobal);  // Esto es válido! Output : Soy una variable global
}

miFuncion();  
```

``` Java title="Java"
public class Main {
    static String variableGlobal = "Soy una variable global";

    public static void main(String[] args) {
        System.out.println(variableGlobal);  // Esto es válido! Output : Soy una variable global
    }
}
```

``` C++ title="C++"
#include <iostream>

std::string variableGlobal = "Soy una variable global";

int main() {
    std::cout << variableGlobal;  // Esto es válido! Output : Soy una variable global
    return 0;
}
```

De todos estos códigos, solo nos detendremos en el detalle de que la variable global se declara en el ámbito global, fuera de cualquier función, y luego es accedida desde algún ámbito, en cualquier parte del código.

!!! warning "¡Atención!"
    Es importante tener cuidado al usar variables globales, ya que pueden ser modificadas desde cualquier parte del código, lo que puede llevar a comportamientos inesperados. 

### Variable de alcance local

En términos generales, en la mayoría de los lenguajes de programación, una variable local es una variable que se declara dentro un ámbito local como una función o un bloque de código. 

Esta variable solo puede ser accesible y modificada dentro de dicho ámbito, es decir, su ámbito se limita al bloque de código donde se declara. Esto proporciona un control más estricto sobre su utilización. 

A su vez, los ámbitos que se encuentren contenidos dentro del ámbito de declaración también tendrán visibilidad y acceso a la variable en cuestión.

Una vez que la ejecución del programa abandona el ámbito en cuestión, la variable local deja de existir (es destruida) y ya no será posible acceder a ella.

Por ejemplo, si declaras una variable dentro de una función, esa variable es local a esa función. No puedes acceder a esa variable fuera de la función o desde otras funciones. Esto ayuda a evitar conflictos de nombres de variables y a mantener el código más organizado y legible.

Aquí tienes un ejemplo genérico:

``` py title="Código genérico"
def mi_funcion():
    variable_local = "Soy una variable local"
    print(variable_local)  # Esto es válido! Output : Soy una variable local

print(variable_local)  # Esto dará un error porque 'variable_local' no está definida en este ámbito
```

> En este ejemplo, `variable_local` es una variable local a `mi_funcion` y solo puede ser utilizada dentro de `mi_funcion`. Intentar acceder a `variable_local` fuera de `mi_funcion` dará un error.

Los ámbitos de aplicación de una variable local pueden ser los siguientes:

1. **Ámbito de función**: Una variable local declarada dentro de una función solo puede ser accedida dentro de esa función. No es visible fuera de la función.

    ``` py title="Python"
    def func():
        j = 20  # Esta es una variable local
        print(j)  # Podemos acceder a la variable local 'j'

    func()  # Output : 20
    print(j)  # Esto dará un error porque 'j' no está definida en el ámbito global
    ```

    > En el código, `j` es una variable local a la función `func()`. No puede ser accedida fuera de `func()`, por lo que el intento de imprimir `j` fuera de la función resulta en un error.

2. **Ámbito de bloque**: En algunos lenguajes de programación, una variable local puede tener un ámbito limitado a un bloque específico de código, como un bucle o una estructura condicional. 

    Aquí tienes ejemplos de cómo se maneja el ámbito de bloque en diferentes lenguajes de programación:

    ``` js title="JavaScript"
    for (let i = 0; i < 5; i++) {
        let x = i;  // En JavaScript, la palabra clave 'let' declara la variable como local. Así, 'x' NO es accesible fuera del bucle
    }

    console.log(x);  // Esto dará un error en JavaScript
    ```
    
    ``` Java title="Java"
    for (int i = 0; i < 5; i++) {
        int x = i;  // En Java, 'x' NO es accesible fuera del bucle
    }

    System.out.println(x);  // Esto dará un error en Java
    ```
    
    ``` C++ title="C++"
    for (int i = 0; i < 5; i++) {
        int x = i;  // En C++, 'x' NO es accesible fuera del bucle
    }

    std::cout << x;  // Esto dará un error en C++
    ```

    En los tres códigos, donde se utilizan variables locales de bloque, estas variables solo son accesibles dentro de ese bloque.
    
    ??? question "¿Qué ocurre con las variables locales de bloque en Python?"
        En Python, sin embargo, las variables declaradas dentro de un bloque de código como un bucle _`for`_ o una declaración _`if`_ no son locales a ese bloque solamente. En cambio, son visibles en el alcance en el que se encuentra ese bloque. 
        
        Aquí tienes un ejemplo:

        ``` py title="Python"
        for i in range(5):
            x = i  # En Python, 'x' es accesible fuera del bucle

        if (x > 0):
            print("x es mayor que 0 y vale", x)  # Esto es válido! Output : x es mayor que 0 y vale 4
            variable_en_bloque = "Soy una variable en un bloque"

        print(variable_en_bloque)  # Esto es válido! Output : Soy una variable en un bloque
        ```

        > Este es un ejemplo de cómo Python maneja el ámbito de las variables. Aquí está lo que sucede paso a paso:
 
        > El bucle `for` se ejecuta 5 veces, con `i` tomando los valores de `0` a `4`. En cada iteración, `i` se asigna a `x`. Por lo tanto, al final del bucle, `x` es igual a `4`.

        > Después del bucle, hay una estructura alternativa `if` que comprueba si `x` es mayor que `0`. Dado que `x` es `4`, la condición es verdadera, por lo que se ejecuta el bloque de código dentro del `if`.

        > Dentro de dicho bloque, se imprime un mensaje que dice "x es mayor que 0 y vale 4". Luego, se declara una variable llamada `variable_en_bloque` y se le asigna la cadena "Soy una variable en un bloque".

        > Después de estructura alternativa `if`, se imprime `variable_en_bloque`. Aunque `variable_en_bloque` se declaró dentro de la estructura alternativa `if`, todavía es accesible fuera de ella. 
        
        > Esto se debe a que Python no tiene un ámbito de bloque como algunos otros lenguajes de programación; en su lugar, tiene un ámbito de función.

        > Por lo tanto, la salida de este código será:

        > ``` title="Terminal (Entrada/Salida)"
        > x es mayor que 0 y vale 4
        > Soy una variable en un bloque
        > ```

        Como podemos evaluar, las variables locales de bloque en Python se comportan de manera diferente a muchos otros lenguajes de programación, donde las variables declaradas dentro de un bloque de código son locales a ese bloque solamente. 

        !!! important "¡Para recordar!"
            En Python, las variables son locales a las funciones, no a los bloques de código.

3. **Ámbito de clase (en lenguajes orientados a objetos)**: En lenguajes de programación orientados a objetos como Python, Java, C++, etc., una variable local puede ser declarada dentro de un método de una clase. Esta variable solo será accesible dentro de ese método.

    ??? example "Puedes analizar un ejemplo aquí:"
    
        ``` py title="Python"
        class Mi_Clase:
            def mi_metodo(self):
                x = 10  # Variable local
                print(x)  # Esto es válido

            def otro_metodo(self):
                print(x)  # Esto dará un error, 'x' no es accesible fuera de 'mi_metodo'

        obj = Mi_Clase()
        obj.mi_metodo()
        obj.otro_metodo()
        ```

        > Este código define una clase llamada `Mi_Clase` que tiene dos métodos: `mi_metodo` y `otro_metodo`.

        > En el método `mi_metodo`, se declara una variable local `x` y se le asigna el valor `10`. Luego, este valor se imprime.

        > En el método `otro_metodo`, se intenta imprimir la variable `x`. Sin embargo, dado que `x` es una variable local dentro del método `mi_metodo`, no es accesible desde `otro_metodo`. Por lo tanto, este intento de imprimir `x` resultará en un error.

        > Finalmente, se crea un objeto `obj` de la clase `Mi_Clase` y se llaman ambos métodos. La llamada a `obj.mi_metodo()` imprimirá `10`, mientras que la llamada a `obj.otro_metodo()` dará un error porque `x` no está definida en ese contexto.

4. **Ámbito de objeto**: En la programación orientada a objetos, las variables definidas dentro de un objeto (a menudo llamadas propiedades o atributos del objeto) tienen un ámbito local al objeto.

    ??? example "Puedes analizar un ejemplo aquí:"

        ``` py title="Python"
        class MiClase:
            def __init__(self, valor):
                self.mi_variable = valor

            def muestra_variable(self):
                print(self.mi_variable)


        # Crear un objeto de MiClase
        objeto = MiClase("Hola, mundo!")

        # Acceder a mi_variable a través del objeto
        print(objeto.mi_variable)  # Esto imprimirá: Hola, mundo!

        # Usar un método del objeto para acceder a mi_variable
        objeto.muestra_variable()  # Esto también imprimirá: Hola, mundo!   
        ```

        > En este código, `mi_variable` tiene un ámbito de objeto. Solo es accesible a través de una instancia de `MiClase` (en este caso, `objeto`). Dentro de la clase, puedes acceder a `mi_variable` usando `self.mi_variable`. Fuera de la clase, puedes acceder a `mi_variable` usando `objeto.mi_variable`.

Existen otros ámbitos más específicos que por su utilización, solo vamos a referenciarlos:

1. **Ámbito de módulo o archivo**: En algunos lenguajes de programación como Python o JavaScript (Node.js), las variables definidas en un archivo o módulo son locales a ese archivo. No son accesibles desde otros archivos a menos que se exporten o se importen explícitamente.

    ??? example "Puedes analizar un ejemplo aquí:"
        En Python, las variables definidas en un archivo son locales a ese archivo. Aquí tienes un ejemplo:

        Supongamos que tienes dos archivos Python: `archivo1.py` y `archivo2.py`.

        En `archivo1.py`, defines una variable:

        ``` py title="Python"
        # archivo1.py
        mi_variable = "Hola, mundo!"
        ```

        Si intentas acceder a `mi_variable` desde `archivo2.py` sin importarla explícitamente, obtendrás un error:

        ``` py title="Python"
        # archivo2.py
        print(mi_variable)  # Esto dará un error, mi_variable no está definida en este archivo
        ```

        Para acceder a `mi_variable` desde `archivo2.py`, necesitas importarla:

        ``` py title="Python"
        # archivo2.py
        from archivo1 import mi_variable

        print(mi_variable)  # Esto imprimirá: Hola, mundo!
        ```

        > En este código, `mi_variable` tiene un ámbito de módulo o archivo. Solo es accesible dentro de `archivo1.py` a menos que se importe explícitamente en otro archivo.

1. **Ámbito de espacio de nombres (namespace)**: En lenguajes como C++ o Python, puedes definir espacios de nombres que proporcionan ámbitos para las variables. Las variables definidas dentro de un espacio de nombres son locales a ese espacio de nombres.

    ??? example "Puedes analizar un ejemplo aquí:"
        En Python, un espacio de nombres (namespace) es una forma de encapsular variables, funciones y clases. Un ejemplo común de un espacio de nombres es un módulo. 
        
        Supongamos que tienes dos archivos Python: `modulo1.py` y `modulo2.py`.

        En `modulo1.py`, defines una variable y una función:

        ``` py title="Python"
        # modulo1.py
        mi_variable = "Hola, mundo!"

        def mi_funcion():
            return "¡Hola desde modulo1!"
        ```

        En `modulo2.py`, puedes acceder a `mi_variable` y `mi_funcion()` importándolas desde `modulo1`:

        ``` py title="Python"
        # modulo2.py
        import modulo1

        print(modulo1.mi_variable)  # Esto imprimirá: Hola, mundo!
        print(modulo1.mi_funcion())  # Esto imprimirá: ¡Hola desde modulo1!
        ```

        > En este código, `modulo1` es un espacio de nombres. `mi_variable` y `mi_funcion()` están en el espacio de nombres de `modulo1`, y puedes acceder a ellas usando la sintaxis `modulo1.mi_variable` y `modulo1.mi_funcion()`. Esto ayuda a evitar conflictos entre nombres de variables y funciones en diferentes módulos.

2. **Ámbito de cierre (closure)**: En algunos lenguajes de programación que admiten funciones de primera clase o funciones anidadas, una variable definida en una función externa puede ser accesible en una función interna. Este es un concepto avanzado conocido como cierre o closure.

    ??? example "Puedes analizar un ejemplo aquí:"
        Un cierre en Python es una función que recuerda los valores de las variables del ámbito en el que fue creada, incluso si ese ámbito ya no existe.
        
        ``` py title="Python"
        def funcion_externa(x):
            def funcion_interna(y):
                return x + y
            return funcion_interna

        mi_closure = funcion_externa(10)

        # Aunque la función externa ya ha terminado de ejecutarse,
        # mi_closure recuerda el valor de x
        print(mi_closure(5))  # Esto imprimirá: 15   
        ```

        > En este código, `funcion_interna` es un cierre que recuerda el valor de `x` del ámbito de `funcion_externa`. Cuando llamamos a `mi_closure(5)`, `funcion_interna` todavía puede acceder al valor de `x`, incluso aunque `funcion_externa` ya ha terminado de ejecutarse. Esto es posible gracias al ámbito de cierre.

---        

!!! important "¡Para recordar!"
    El ámbito de una variable determina dónde puede ser accesible en el código. 
    
    Una variable global es accesible y modificable desde todo el código del programa.
    
    Una variable local es accesible y modificable solo dentro del ámbito donde es accesible y modificable, ya sea una función, un bloque de código específico o un método de una clase; y no desde todo el código del programa.

    Es importante entender estos ámbitos para evitar errores y escribir código más limpio y mantenible.

## Ventajas de utilizar variables locales

Las variables locales tienen varias ventajas sobre las variables globales:

1. **Evitan colisiones de nombres**: Las variables locales existen solo dentro de la función donde se definen, lo que significa que puedes usar el mismo nombre de variable en diferentes funciones sin que se produzcan conflictos.

2. **Facilitan la lectura y el mantenimiento del código**: Al limitar el alcance de una variable a una sola función, se hace más fácil entender qué hace esa variable y cómo se utiliza.

3. **Promueven la modularidad y la reutilización del código**: Las funciones que utilizan solo variables locales (y parámetros) son independientes del estado global del programa, lo que significa que pueden ser fácilmente reutilizadas en diferentes contextos.

4. **Evitan efectos secundarios inesperados**: Cuando usas variables globales, cualquier función podría cambiar su valor, lo que puede llevar a comportamientos inesperados. Con las variables locales, tienes un control total sobre cuándo y cómo cambia su valor.

!!! success "Buena práctica"    
    Es una buena práctica de programación limitar el uso de variables globales y utilizar variables locales siempre que sea posible para evitar colisiones de nombres, facilitar la lectura y el mantenimiento del código, promover la modularidad y la reutilización del código y evitar efectos secundarios inesperados.











---


En Python, el ámbito de una variable se refiere a la parte del código donde esa variable es accesible. Aquí están los ámbitos en los que una variable puede existir:

Ámbito Local: Una variable declarada dentro de una función o método es local a esa función o método. Solo puede ser accedida dentro de esa función o método.

Ámbito Encerrado (Nonlocal): Este ámbito se refiere a las variables en la función más cercana que encierra a la función actual. Específicamente, se aplica a las funciones anidadas. Una variable declarada en la función externa es accesible en la función interna, pero no al revés.

Ámbito Global: Una variable declarada fuera de todas las funciones es una variable global. Puede ser accedida desde cualquier parte del código, aunque para modificarla dentro de una función, necesitas declararla como global dentro de esa función.

Ámbito Incorporado (Built-in): Este es el ámbito más amplio. Incluye nombres predefinidos en Python, como funciones incorporadas (built-in functions) y excepciones. Estos nombres están disponibles en todas partes en tu código.

Estos ámbitos se buscan en el orden: Local → Encerrado (Nonlocal) → Global → Incorporado (Built-in). Este es el concepto de LEGB en Python.







En Python, por ejemplo, hay cuatro tipos principales de alcance que son la base de la regla _LEGB_. 
_LEGB_ significa Local (Local) &#x2192; Envolvente, Padre o Superior (Enclosing) &#x2192; Global (Global) &#x2192; Integrado o Incorporado (_Built-in_) y es la lógica seguida por un intérprete de Python cuando ejecuta su programa.

![Alt text](imagenes/alcance-de-variable-en-python.png){: class="center back-white border-round"}

## Diferentes ámbitos de alcance de una variable

Como dijimos, en programación, el alcance de una variable se refiere a la parte del código donde esta es declarada y puede ser accedida. Los tipos más comunes de alcances en la programación son:

1. **Ámbito global (Global)**: las variables declaradas como globales en el bloque principal del programa, afuera de una función, método, clase, instancia o bloque de código, tienen un ámbito y una duración global, y son accesibles durante toda la ejecución del programa desde cualquier lugar del bloque principal del programa, función, clase, instancia o bloque de código. 

1. **Ámbito local (Local)**: las variables declaradas dentro de una función, método, clase, instancia o bloque de código tienen un ámbito local. Solo son accesibles dentro de esa función, método, clase, instancia o bloque de código y tienen una duración que se extiende desde el punto de declaración hasta el final de la mencionada función, método, clase, instancia o bloque de código.

1. **Ámbito envolvente (Enclosing)**: todas las variables locales declaradas dentro de un bloque son accesibles dentro de los bloques internos que este bloque contenga, por no viceversa. Es decir que todas las variables locales declaradas dentro del bloque interno no son accesibles en el bloque externo. Al **ámbito envolvente** se lo considera un **ámbito anidado (Nested scope)**.

1. **Ámbito de bloque (Block)**: algunos lenguajes de programación, como C, C++ y JavaScript, permiten ámbitos de nivel de bloque. Las variables declaradas dentro de un bloque, como dentro de una estructura alternativa o de un bucle, tienen un alcance limitado a ese bloque. Solo son accesibles dentro del bloque y sus bloques anidados. La vida útil de las variables de ámbito de bloque depende del idioma y el contexto específico.

1. **Ámbito de función (Function)**: las variables declaradas dentro de una función se comportan como variables locales. Solo son accesibles dentro de esa función y tienen una duración que se extiende desde el punto de declaración hasta el final de la mencionada función.

1. **Ámbito de clase (Class)**: en la programación orientada a objetos, las variables declaradas dentro de una clase pero fuera de cualquier método se conocen como variables de clase o variables estáticas. Estas variables pertenecen a la clase misma en lugar de instancias de la clase. Son accesibles para todas las instancias de la clase y tienen una duración vinculada a la duración del programa.

1. **Ámbito de instancia (Instance)**: las variables de instancia se declaran dentro de una clase y se asocian con instancias u objetos específicos de esa clase. Cada instancia de la clase tiene su propio conjunto de variables de instancia, y solo se puede acceder a ellas a través de la instancia misma. Las variables de instancia tienen una vida útil vinculada a la vida útil del objeto correspondiente.

1. **Ámbito integrado (Built-in)**: El ámbito integrado está comprendido por la colección de identificadores y funciones predefinidos que están automáticamente disponibles para cualquier parte del programa sin necesidad de una declaración o importación explícita. Estos identificadores y funciones son parte de la biblioteca estándar o funcionalidad principal de cada lenguaje de programación e incluyen operaciones fundamentales, tipos de dato, estructuras de control y funciones de utilidad que se usan comúnmente en la programación. 

    Esta colección puede variar según el lenguaje de programación, pero algunos ejemplos comunes son:

    1. tipos de dato básicos: el ámbito integrado suele incluir tipos de dato estándar, como números enteros, números de punto flotante, valores booleanos, caracteres, cadenas, matrices y, en ocasiones, estructuras de datos más complejas, como listas o diccionarios.
    1. Funciones matemáticas: muchos lenguajes de programación proporcionan funciones matemáticas integradas, como funciones trigonométricas (sin, cos, tan), funciones logarítmicas (log, exp) y operaciones aritméticas (suma, resta, multiplicación, división, etc.).
    1. Funciones de entrada/salida: las funciones integradas suelen estar disponibles para realizar operaciones de entrada/salida, como leer o escribir en la consola, leer y escribir archivos y manejar la entrada del usuario.
    1. Estructuras de control: las estructuras de control básicas como alternativas (if, switch) y bucles (for, while) suelen formar parte del ámbito integrado.
    1. Manejo de errores: la funcionalidad integrada a menudo incluye mecanismos para manejar las excepciones o los errores que pueden ocurrir durante la ejecución del programa, como los bloques try-catch o las funciones de informe de errores.
    1. Manipulación de cadenas: las funciones para operaciones de cadenas como la concatenación, la extracción de sub cadenas, la búsqueda y el reemplazo a menudo se proporcionan en el ámbito integrado.
    1. Funciones de fecha y hora: muchos lenguajes de programación incluyen funciones integradas para manejar fechas, horas y zonas horarias, lo que permite operaciones como formateo de fechas, cálculo de horas y conversiones de zonas horarias.

Los elementos y las funcionalidades específicas pueden variar significativamente entre los lenguajes de programación, por lo que es importante consultar la documentación o los recursos específicos del lenguaje para explorar el alcance integrado de un lenguaje de programación en particular.

## ¿Cómo identificar el ámbito de una variable?

Cada variable solo existe y es accesible dentro del ámbito en el que ha sido declarada. Cuando hablamos de la existencia y accesibilidad dentro de un ámbito, nos referimos a su **alcance**. 

Para determinar su ámbito, hay que identificar las marcas de apertura y cierre de bloque de código más cercanas que rodean la declaración de la variable. 

!!! important "¡Para recordar!"
    La mayoría de los lenguajes de programación utilizan llaves ( {} ) para marcar el principio y el final de un bloque de código.

    Una **variable global** estará disponible en todos los bloques de código dentro del programa.

    Y una **variable local** solo estará disponible dentro del bloque de código en el que se haya declarado. Si este bloque contiene a su vez otros bloques, la **variable local** también será accesible dentro de ellos. 

![Alt text](imagenes/identificacion-de-alcance-de-variables-en-js.png){: class="center back-white border-round"}

Aquí vemos que la variable _soyGlobal_ ha sido declarada entre las dos llaves marcadas con un círculo azul. El alcance de esa variable es todo lo que se encuentra entre esas dos llaves. 
El mismo concepto se aplica para las variables _localVarB1_ y _localVarB2_, cuyos alcances están limitados por las llaves de cada función marcadas con un círculo verde.

!!! question "Para pensar:"
    ¿Qué ocurre, entonces, con las variables _localVarB1_ y _localVarB2_ cuando son accedidas dentro de las funciones _bloque1()_ y _bloque2()_?

En caso de que se utilice el mismo nombre de variable declarado en varios niveles de anidamiento (significa que hay al menos un bloque dentro de otro bloque), prevalecerá la declaración del bloque más interno, evitando el acceso, durante la ejecución del bloque interno, a la variable declarada en el bloque externo.

![Alt text](imagenes/identificacion-de-alcance-de-variables-en-js-2.png){: class="center back-white border-round"}

!!! question "Para pensar:"
    ¿Qué ocurre ahora, en cada caso, con la variable declarada dentro de cada bloque con el mismo nombre _localVar_ cuando se accede a su valor?

!!! warning "Importante"
    Dada su escasa legibilidad, las declaraciones anidadas de un mismo nombre de variable son situaciones que nunca deberían ocurrir en un programa bien diseñado.

## Alcance global

``` js title="JavaScript"
function mostrarNombre() {
   // Acceder a la variable global
   console.log("Mi nombre es " + nombre)
}
// Bloque principal (main)
{
// Definición de variable global
   var nombre = "Juan"

   mostrarNombre()  // Salida: Mi nombre es Juan
}
```

> En este ejemplo, la variable nombre se declara como global fuera de cualquier tipo de bloque de código.  
> Sin embargo, al ser global, la función mostrarNombre() puede acceder a ella y mostrar su valor en la consola

## Alcance local

``` js title="JavaScript"
function calcularSuma(a, b) {
   // Definición de variable local
   let suma = a + b
   return suma
}
// Bloque principal (main)
{ 
   console.log(calcularSuma(5, 3))  // Salida: 8
   console.log(suma); // Error: suma no está definida (solo existe dentro de la función calcularSuma)
}
```

> En este ejemplo, la variable suma se declara dentro de la función calcularSuma() y, por lo tanto, tiene un alcance local.  
> La variable solo puede ser accedida dentro de la función y no está disponible fuera de ella.

## Alcance de bloque

``` js title="JavaScript"
function verificarNumero(numero) {
   if (numero >= 0) {
      let info = "El número es positivo"; // Definición de variable de bloque
      console.log(info)
   } else {
      let info = "El número es negativo"; // Definición de variable de bloque
      console.log(info)
   }
}
// Bloque principal (main)
{
   verificarNumero(5)  // Salida: El número es positivo
   verificarNumero(-3)  // Salida: El número es negativo
   console.log(info)  // Error: mensaje no está definido (fuera de ambos bloques de la estructura if)
}
```

> En este ejemplo, se declaran dos variables, una dentro de un bloque verdadero y el otra dentro del bloque falso de la estructura alternativa, con el mismo nombre info.  
> Al tener, cada una, un alcance de bloque (local), solo existirán dentro del bloque de código donde fueran declaradas.  }
> Fuera de su bloque, cada variable no está disponible, produciendo un error al intentar acceder a ellas.

## Caso práctico 1 de análisis e identificación de ámbitos de variables

!!! question "¿Para pensar?"
    ¿Puedes analizar y entender como funciona este programa?
    
    Guíate por los colores. Si no, continúa leyendo y ¡lograrás entenderlo!

![Alt text](imagenes/alcance-de-variable-en-python.png){: class="center back-white border-round"}


```{.js .blue title="JavaScript" linenums="1"}
// Global scope (main)
{
   var g = 0  // Declara x como global en el cuerpo principal del programa (main)
   outer()  // Llama a la función outer() dentro del cuerpo principal del programa
   console.log("La variable global g vale ", x)  // Imprime 0
}
```
```{.js .green .consecutive  linenums="7"}
function outer() {  // Es una función (equivale a un bloque de código) llamada en main
   // Local scope de outer() y Enclosing scope respecto de inner()
   let x = 1  // Declara x localmente en outer()
   let y = 1  // Declara y localmente en outer()
```
```{.js .purple .consecutive  linenums="11"}
   function inner() {  // Es una función (equivale a un bloque de código) dentro de outer()
      // Local scope de inner()
      let x = 2  // declara x localmente en inner()
      console.log("La variable local x dentro de inner() vale ", x)  // Imprime 2
      console.log("La variable local y declarada en outer() vale ", y)  // Imprime 1
   }
```
```{.js .green .consecutive  linenums="17"}
   inner()  // Llama a la función inner() dentro de outer()
   console.log("La variable local x dentro de outer() vale ", x)  // Imprime 1
   console.log("La variable global g dentro de outer() vale ", x)  // Imprime 0
}
```

``` title="Terminal (Entrada/Salida)"
Esto se ejecuta en el ámbito de inner():
La variable local x dentro de inner() vale  2
La variable local y declarada en outer() vale  1

Esto se ejecuta en el ámbito de outer():
La variable local x dentro de outer() vale  1
La variable global g dentro de outer() vale  0

Esto se ejecuta en el ámbito principal del programa:
La variable global x vale  0
```

## Caso práctico 2 de análisis e identificación de ámbitos de variables

!!! question "¿Para pensar?"
    Aquí existe una ligera diferencia en la declaración de una variable,
    
    ¿Puedes analizar y entender cuál es el error de este programa?
    
    Si no, continúa leyendo y ¡lograrás entenderlo!


```{.js .blue title="JavaScript" hl_lines="3" linenums="1"}
// Global scope (main)
{
   let g = 0  // Declara x como local en el cuerpo principal del programa (main)
   outer()  // Llama a la función outer() dentro del cuerpo principal del programa
   console.log("La variable local g vale ", x)  // Imprime 0
}
```
```{.js .green .consecutive linenums="7"}
function outer() {  // Es una función (equivale a un bloque de código) llamada en main
   // Local scope de outer() y Enclosing scope respecto de inner()
   let x = 1  // Declara x localmente en outer()
   let y = 1  // Declara y localmente en outer()
```
```{.js .purple .consecutive linenums="11"}
   function inner() {  // Es una función (equivale a un bloque de código) dentro de outer()
      // Local scope de inner()
      let x = 2  // declara x localmente en inner()
      console.log("La variable local x dentro de inner() vale ", x)  // Imprime 2
      console.log("La variable local y declarada en outer() vale ", y)  // Imprime 1
   }
```
```{.js .green .consecutive hl_lines="3" linenums="17"}
   inner()  // Llama a la función inner() dentro de outer()
   console.log("La variable local x dentro de outer() vale ", x)  // Imprime 1
   console.log("La variable local g dentro de outer() vale ", x)  // ¿ Imprime 0 ?
}
```

```title="Terminal (Entrada/Salida)"
Esto se ejecuta en el ámbito de inner():
La variable local x dentro de inner() vale  2
La variable local y declarada en outer() vale  1

Esto se ejecuta en el ámbito de outer():
La variable local x dentro de outer() vale  1

```
```{.js .consecutive}
index.js:19
  console.log("La variable local g dentro de outer() vale ", g)
                                                             ^
ReferenceError: g is not defined
```

## Uso de variables globales en funciones locales

``` py title="Python"
global_var = 10

def local_function():
    global global_var
    local_var = 20
        
    print("Var local:", local_var)
    print("Var global:", global_var)

local_function()
```

> En Python se utiliza la palabra clave global seguida del nombre de la variable dentro de la función local para poder tener alcance a la variable.  
> Esto permite que la función tenga acceso tanto a las variables locales definidas dentro de ella como a las variables globales definidas fuera de ella.

``` c++ title="C++"
#include <iostream>

int global_Var = 10;

void local_function() {
    int local_Var = 20;
    std::cout << "Var local: " << local_Var << std::endl;
    std::cout << "Var global: " << global_Var << std::endl;
}

int main() {
    local_function();
    return 0;
}
```

``` js title="JavaScript"
function localFunction() {
    let localVar = 20
    console.log("Var local:", localVar)
    console.log("Var global:", globalVar)
}

// Bloque principal (main)
{ 
   var globalVar = 10
   localFunction();
}
```

> En JavaScript y C++ se accede directamente a la variable global dentro de la función local para poder utilizarla.  
> Esto permite que la función tenga acceso tanto a las variables locales definidas dentro de ella como a las variables globales definidas fuera de ella.

En todos los ejemplos, se obtendría el siguiente resultado:

``` title="Terminal (Entrada/Salida)"
Var local: 20
Var global: 10
```

## Modificación de variables globales en funciones locales

``` py title="Python"
global_var = 10

def modify_global():
    global global_var
    global_var += 5

def use_global_locally():
    local_var = global_var * 2
    print("Var local:", local_var)

modify_global()
use_global_locally()

print("Var global:", global_var)
```

``` js title="JavaScript"
function modifyGlobal() {
    globalVar += 5
}

function useGlobalLocally() {
    let localVar = globalVar * 2
    console.log("Var local:", localVar)
}

// Bloque principal (main)
{ 
   var globalVar = 10
   modifyGlobal()
   useGlobalLocally()
   console.log("Var global:", globalVar)
}

```

``` c++ title="C++"
#include <iostream>
int global_var = 10;

void modifyGlobal() {
    global_var += 5;
}
void useGlobalLocally() {
    int local_var = global_var * 2;
    std::cout << "Var local: " << local_Var << std::endl;
}
int main() {
    modifyGlobal();
    useGlobalLocally();
    std::cout << "Var global: " << global_Var << std::endl;
    return 0;
}
```

> En estos ejemplos, la función modify_global() o modifyGlobal() según el lenguaje, incrementa el valor de la variable global, mientras que la función use_global_locally() o useGlobalLocally() utiliza la variable global en una variable local y la imprime.  
> Al ejecutar el código, puedes ver cómo los cambios en la variable global se reflejan tanto dentro como fuera de la función.

En todos los ejemplos, se obtendría el siguiente resultado:

``` title="Terminal (Entrada/Salida)"
Var local: 30
Var global: 15
```

## Conversión de variables globales en locales

``` py title="Python"
global_var = 10

def convert_global_to_local():
    global_var = 20
    print("Var local:", global_var)

convert_global_to_local()

print("Var global:", global_var)
```

``` js title="JavaScript"
function convertGlobalToLocal() {
    let globalVar = 20;
    console.log("Var local:", globalVar);
}

// Bloque principal (main)
{ 
   var globalVar = 10
   convertGlobalToLocal();
   console.log("Var global:", globalVar);
}

```

``` c++ title="C++"
#include <iostream>
int global_var = 10;

void convertGlobalToLocal() {
    int global_var = 20;
    std::cout << "Var local: " << global _Var << std::endl;
}
int main() {
    convertGlobalToLocal();

    std::cout << "Var global: " << global_Var << std::endl;

    return 0;
}
```

> En estos ejemplos, la función convert_global_to_local() declara una nueva variable local llamada global_var con un valor de 20. Dentro del ámbito de la función, cuando se hace referencia a global_var, se hace referencia a la variable local en lugar de la variable global.  
> Fuera de la función, la variable global mantiene su valor original de 10.

``` title="Terminal (Entrada/Salida)"
Var local: 20
Var global: 10
```

## ¿Puede una variable local reemplazar a una global?

!!! important "¡Para recordar!"
   Los conceptos vistos solo afectan a la variable dentro del ámbito de la función o del bloque en los que se declara la variable local.

   Fuera de esa función o bloque, la variable global seguirá existiendo y mantendrá su valor original.

   Asimismo, la variable local será destruida al finalizar la función o el bloque donde fuera creada. Así, su acceso o modificación será imposible a partir de dicha finalización.

Veamos el siguiente ejemplo:

``` py title="Python"
global_var = 10

def modify_global():
    global global_var
    global_var += 5

def use_global_locally():
    local_var = global_var * 2
    print("Var local:", local_var)

print("Var global:", global_var)

modify_global()
use_global_locally()

print("Var global:", global_var)
print("Var local:", local_var)
```

!!! question ¿¿Qué ocurrirá cuando se ejecute la última línea del programa?

``` title="Terminal (Entrada/Salida)"
Var global: 10
Var local: 20
Var global: 10
```
``` {.py .consecutive}
Error: NameError: name ‘local_var' is not defined
```

## Error al acceder a una variable local fuera de su alcance (scope)

Cuando intentas acceder a una variable local fuera de su alcance, es posible que encuentres un error dependiendo del lenguaje de programación que estés utilizando. Por lo general, las variables locales tienen un alcance limitado dentro del bloque de código donde se definen. Una vez que el flujo de ejecución sale de ese bloque, las variables locales ya no son accesibles.

En el siguiente ejemplo, local_var se define dentro del ámbito de la función local_function(). Cuando intentemos acceder a ella fuera de la función, recibiremos un error de ReferenceError o de NameError (el nombre del error dependerá del lenguaje empleado) porque la variable no está definida en el ámbito (scope) actual.

``` py title="Python" linenums="1"
def local_function():
    local_var = 10
    return local_var

result = local_function()

print(result)  
print(local_var)  
```

``` title="Terminal (Entrada/Salida)"
10 # Imprime la línea 7
Error: NameError: name 'local_var' is not defined # Error devuelto por la línea 8
```

``` js title="JavaScript" linenums="1"
function local_function() {
  let local_var = 10
  return local_var
}
// Bloque principal (main)
{
   let result = myFunction();
   console.log(result);  
   console.log(local_var); 
}
```

``` title="Terminal (Entrada/Salida)"
10 # Imprime la línea 8
Error: ReferenceError: local_var is not defined # Error devuelto por la línea 9
```

Para resolver este problema, es necesario que el código devuelva el valor almacenado en la variable local desde la función y para ser almacenado en un variable en el ámbito de llamada. 

En el ejemplo, devolvemos el valor de `local_var` desde la función `local_function()` y lo asignamos a la variable result en el ámbito de la llamada. Así, podremos acceder y utilizar el valor fuera de la función sin encontrar un error.



---


En Python, las variables que se declaran dentro de un bloque de código, como un bucle for o una declaración if, son visibles en el alcance en el que se encuentra ese bloque. No son locales al bloque en sí. Aquí tienes un ejemplo:

``` py
if True:
    variable_en_bloque = "Soy una variable en un bloque"
print(variable_en_bloque)  # Esto es válido y imprimirá "Soy una variable en un bloque"
```
En este ejemplo, variable_en_bloque se declara dentro del bloque if, pero aún así es accesible fuera de ese bloque, en el mismo alcance en el que se encuentra el bloque if.

Sin embargo, si la variable se declara dentro de una función, entonces sí es una variable local a esa función:

``` py
def mi_funcion():
    variable_local = "Soy una variable local"

mi_funcion()
print(variable_local)  # Esto dará un error porque variable_local no está definida en este alcance
```

En este segundo ejemplo, variable_local solo es accesible dentro de mi_funcion, y cualquier intento de acceder a ella fuera de la función dará un error.

---

En Python, el ámbito de una variable local se refiere al lugar en el código donde esa variable puede ser accedida. Aquí están los ámbitos en los que una variable local puede existir:

Funciones: Una variable local declarada dentro de una función solo puede ser accedida dentro de esa función. No es visible fuera de la función. Por ejemplo:

``` py
def mi_funcion():
    variable_local = "Soy una variable local"
    print(variable_local)  # Esto es válido

mi_funcion()
print(variable_local)  # Esto dará un error porque variable_local no está definida en este alcance
```

Clases: Una variable local declarada dentro de un método de una clase solo puede ser accedida dentro de ese método. No es visible fuera del método. Por ejemplo:

``` py
class MiClase:
    def mi_metodo(self):
        variable_local = "Soy una variable local"
        print(variable_local)  # Esto es válido

obj = MiClase()
obj.mi_metodo()
print(variable_local)  # Esto dará un error porque variable_local no está definida en este alcance
```

Comprensiones de listas: En Python 3, las variables definidas en una comprensión de lista son locales a la comprensión. Por ejemplo:

``` py
[x for x in range(10)]
print(x)  # Esto dará un error porque x no está definida en este alcance
```

En todos estos casos, la variable local solo es visible dentro del bloque de código donde se declara. Intentar acceder a la variable fuera de ese bloque de código dará un error.


--- 


En Python, puedes acceder a variables globales desde un ámbito local (como una función), pero si intentas modificarlas directamente, Python las tratará como variables locales. Para modificar una variable global dentro de un ámbito local, debes usar la palabra clave global antes de la variable.

Aquí tienes un ejemplo:

``` py title="Python"
# Variable global
x = 10

def test():
    # Intentando modificar la variable global
    global x
    x = 20

test()

# Imprime: 20
print(x)
```

En este ejemplo, x es una variable global. Dentro de la función test, usamos la palabra clave global para indicar que queremos usar la variable global x, no una nueva variable local con el mismo nombre. Luego, modificamos x a 20. Cuando imprimimos x después de llamar a test, obtenemos 20, lo que indica que la variable global x ha sido modificada dentro de la función.

Sin embargo, el uso de variables globales debe minimizarse ya que pueden hacer que el código sea difícil de entender y propenso a errores. Es mejor pasar las variables como argumentos a las funciones y devolver los resultados.

