title: Alcance de una variable

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

??? success "Buenas prácticas para el uso de variables globales"
    Las mejores prácticas para el uso de variables globales en programación son las siguientes:

    1. **Minimizar su uso**: En general, es mejor evitar el uso de variables globales siempre que sea posible. Las variables globales pueden hacer que el código sea difícil de entender y mantener, ya que pueden ser modificadas desde cualquier parte del programa.

    1. **Usar constantes globales**: Si necesitas una variable que sea accesible desde todas partes del código, a menudo es mejor hacerla una constante (es decir, un valor que no cambia una vez que se establece). Esto puede evitar muchos problemas asociados con las variables globales.

    1. **Encapsulamiento en objetos o módulos**: Si necesitas compartir un estado entre varias funciones, a menudo es mejor encapsular ese estado en un objeto o módulo. Esto puede hacer que el código sea más fácil de entender y mantener.

    1. **Documentar su uso**: Si debes usar una variable global, asegúrate de documentar claramente dónde y cómo se utiliza. Esto puede ayudar a prevenir errores y hacer que el código sea más fácil de entender.

    1. **Evitar el uso en funciones multi hilo (_multi thread_)**: Las variables globales pueden causar problemas en programas multi hilo, ya que diferentes hilos pueden intentar acceder o modificar la variable al mismo tiempo. Si estás trabajando con hilos, es mejor evitar las variables globales.

    Iremos viendo cada concepto más adelante. Por ahora no te preocupes por entender al máximo de que trata cada uno.

    Recuerda, cada lenguaje de programación tiene sus propias convenciones y características, por lo que estas prácticas pueden variar dependiendo del lenguaje que estés utilizando.

### Variable de alcance local

En términos generales, en la mayoría de los lenguajes de programación, una variable local es una variable que se declara dentro un ámbito local como una función o un bloque de código. 

Esta variable solo puede ser accesible y modificada dentro de dicho ámbito, es decir, su ámbito se limita al bloque de código donde se declara. Esto proporciona un control más estricto sobre su utilización. 

A su vez, los ámbitos que se encuentren contenidos dentro del ámbito de declaración también tendrán visibilidad y acceso a la variable en cuestión.

## ¿Qué ocurre si se intenta acceder a una variable local fuera de su alcance?

Cuando intentas acceder a una variable local fuera de su alcance, en la mayoría de los lenguajes obtendrás un error (JavaScript, por ejemplo, posee un mecanismo que evita el error, pero es considerado mala práctica). 

Debido a que una variable local tiene un alcance limitado a la región o parte de código donde es declarada, cuando el flujo de ejecución del programa sale de dicha región la variable deja de existir y ya no es visible ni accesible.

Por lo tanto, las variables locales son aquellas que se definen dentro de una región o parte de código, como una función o un bloque de código. Solo existen dentro de ese ámbito y no son reconocibles fuera de él.

Por ejemplo, en Python, el siguiente código devolverá un mensaje de error:

``` py title="Python" linenums="1"
def mi_funcion():
    variable_local = "Soy local"

print(variable_local)
```

``` py title="Terminal (Entrada/Salida)"
Traceback (most recent call last):
  File "…", line 4, in <module>
    print(variable_local)
          ^^^^^^^^^^^^^^
NameError: name 'variable_local' is not defined
```

> Este código devuelve `NameError` que dice que `variable_local` no está definida. Esto se debe a que estás intentando acceder a `variable_local` fuera de su alcance, que es dentro de la función `mi_funcion`.

Para resolver este problema, es necesario que la función retorne el dato almacenado en la variable `variable_local` dentro de la función para ser utilizado en el ámbito donde se originó la llamada a la función:

``` py title="Python" linenums="1" hl_lines="4 6 9" 
def mi_funcion():
    variable_local = "Soy local"

    return variable_local

variable_global = mi_funcion()  # el dato retornado desde la función se almacena en una variable
print(variable_global) # Se imprime el dato almacenado en la variable que recibió el dato desde la función

print(mi_funcion()) # Se imprime directamente el dato retornado desde la función
```

``` title="Terminal (Entrada/Salida)"
Soy local
Soy local
```

> Este código llama dos veces a la función y en ambos casos la función retorna el mismo dato desde la línea 4:  
>   
> * La primera llamada ocurre en la línea 6. El dato retornado desde la función se almacena en una variable que luego es impresa en la línea 7.  
> 
> * La segunda llamada ocurre en la línea 9. El dato retornado desde la función se imprime directamente.  
> 
> Empleando este procedimiento es como podemos acceder y utilizar el dato almacenado en `variable_local` dentro de la función, fuera de ella, sin que el programa devuelva un mensaje de error y se detenga de manera inesperada.

!!! important "¡Para recordar!"
    Si declaras una variable dentro de una función, esa variable es local a esa función. No podrás acceder a esa variable fuera de la función o desde otras funciones. 
    
    Esto ayuda a evitar conflictos de nombres de variables y a mantener el código más organizado y legible y más fácil de mantener.

### ¿Cuáles son los ámbitos locales más comunes?

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

2. **Ámbito de espacio de nombres (namespace)**: En lenguajes como C++ o Python, puedes definir espacios de nombres que proporcionan ámbitos para las variables. Las variables definidas dentro de un espacio de nombres son locales a ese espacio de nombres.

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

3. **Ámbito de cierre (closure)**: En algunos lenguajes de programación que admiten funciones de primera clase o funciones anidadas, una variable definida en una función externa puede ser accesible en una función interna. Este es un concepto avanzado conocido como cierre o closure.

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

## ¿Cómo identificar el ámbito de aplicación de una variable?

Para identificar el ámbito de aplicación de una variable, es preciso detectar las "marcas" de apertura y de cierre de la región o parte de código que contiene la declaración de dicha variable.

!!! important "¡Para recordar!"
    La mayoría de los lenguajes de programación, como JavaScript, utilizan llaves ( { } ) para marcar el principio y el final de un bloque de código. 
    
    Otros lenguajes, como Python, emplean la indentación, un aspecto del estilo de codificación que implica agregar espacios en blanco al comienzo de las líneas de código para indicar bloques de código y mejorar la legibilidad. 

    Una **variable global** es visible y accesible en todas las regiones o partes de código.

    Una **variable local** solo puede ser accesible y modificada dentro del ámbito de la región o parte de código donde sea declarada.

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


### Primer caso práctico de estudio

```{.js .blue title="JavaScript" linenums="1"}
// Global scope main()
{
   var g = 0  // Declara g como global en el cuerpo principal del programa main()
   
   outer()  // Llama a la función outer() dentro del cuerpo principal del programa
   
   console.log("La variable global g vale ", g)  // Imprime 0
}
```
```{.js .green .consecutive  linenums="7"}
function outer() {  // Es una función (equivale a un bloque de código) llamada en main()
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
   console.log("La variable global g dentro de outer() vale ", g)  // Imprime 0
}
```

!!! question "¿Para pensar?"
    ¿Puedes analizar y entender como funciona este programa?
    
    Guíate por los colores. Si no, continúa leyendo y ¡lograrás entenderlo!


``` title="Terminal (Entrada/Salida)"
// Esto se ejecuta en el ámbito de inner():
La variable local x dentro de inner() vale  2
La variable local y declarada en outer() vale  1

// Esto se ejecuta en el ámbito de outer():
La variable local x dentro de outer() vale  1
La variable global g dentro de outer() vale  0

// Esto se ejecuta en el ámbito principal del programa:
La variable global x vale  0
```

### Segundo caso práctico de estudio

```{.js .blue title="JavaScript" linenums="1"}
// Global scope main()
{
   let g = 0  
   
   outer()  
   
   console.log("La variable local g vale ", g)  
}

```
```{.js .green .consecutive linenums="7"}
function outer() {  // Es una función (equivale a un bloque de código) llamada en main()
   // Local scope de outer() y Enclosing scope respecto de inner()
   let x = 1  
   let y = 1  

```
```{.js .purple .consecutive linenums="11"}
   function inner() {  // Es una función (equivale a un bloque de código) dentro de outer()
      // Local scope de inner()
      let x = 2
      
      console.log("La variable local x dentro de inner() vale ", x)  
      console.log("La variable local y declarada en outer() vale ", y)  
   }

```
```{.js .green .consecutive hl_lines="3" linenums="17"}
   inner()  // Llama a la función inner() dentro de outer()
   
   console.log("La variable local x dentro de outer() vale ", x)  
   console.log("La variable local g dentro de outer() vale ", g)  
}
```

!!! question "¿Para pensar?"
    En este programa existe una ligera diferencia en la declaración de una de las variables ¿Puedes analizar y entender cuál es el error conceptual que hace que el programa devuelva un error?
    
    Guíate por los colores. Si no, continúa leyendo y ¡lograrás entenderlo!

??? success "Puedes ver el resultado haciendo clic aquí."
    ```{.js .blue title="JavaScript" hl_lines="3" linenums="1"}
    // Global scope main()
    {
        let g = 0  // Declara g como local en el cuerpo principal del programa (main)
        
        outer()  // Llama a la función outer() dentro del cuerpo principal del programa
        
        console.log("La variable local g vale ", g)  // Imprime 0
    }

    ```
    ```{.js .green .consecutive linenums="7"}
    function outer() {  // Es una función (equivale a un bloque de código) llamada en main()
        // Local scope de outer() y Enclosing scope respecto de inner()
        let x = 1  // Declara x localmente en outer()
        let y = 1  // Declara y localmente en outer()
    }
    ```
    ```{.js .purple .consecutive linenums="11"}
        function inner() {  // Es una función (equivale a un bloque de código) dentro de outer()
            // Local scope de inner()
            let x = 2  // declara x localmente en inner()
            console.log("La variable local x dentro de inner() vale ", x)  // Imprime 2
            console.log("La variable local y declarada en outer() vale ", y)  // Imprime 1
        }

    ```
    ```{.js .green .consecutive hl_lines="4" linenums="17"}
        inner()  // Llama a la función inner() dentro de outer()
        
        console.log("La variable local x dentro de outer() vale ", x)  // Imprime 1
        console.log("La variable local g dentro de outer() vale ", g)  // ¿ Imprime 0 ? La variable local g solo existe en main()
    }
    ```

    ```title="Terminal (Entrada/Salida)"
    // Esto se ejecuta en el ámbito de inner():
    La variable local x dentro de inner() vale  2
    La variable local y declarada en outer() vale  1

    // Esto se ejecuta en el ámbito de outer():
    La variable local x dentro de outer() vale  1

    ```
    ```{.js .consecutive}
    index.js:20
        console.log("La variable local g dentro de outer() vale ", g)
                                                                   ^
    ReferenceError: g is not defined
    ```

## Uso de variables globales en funciones (ámbitos locales)

El uso de variables globales en ámbitos locales varía entre los diferentes lenguajes de programación, pero la idea general es la misma: una variable global es accesible desde cualquier parte del código, incluyendo funciones o métodos (ámbitos locales).

Aquí vemos cómo se maneja en algunos lenguajes:

``` py title="Python"
# Variable global
global_var = 10

def funcion_local():
    global global_var  # Visibilidad de la variable global
    local_var = 10  # Variable local

    print("Var local:", local_var)  # Acceso a la variable local
    print("Var global desde otro ámbito:", global_var)  # Acceso a la variable global

    global_var = global_var + local_var  # Modificación de la variable global

funcion_local()

print("Var global desde su ámbito:", global_var)  # Acceso a la variable global desde su ámbito
```

``` title="Terminal (Entrada/Salida)"
Var local: 10
Var global desde otro ámbito: 10
Var global desde su ámbito: 20
```

> `global_var` es una variable global. Dentro de la función `funcion_local`, usamos la palabra clave `global` para indicar que queremos usar la variable global `global_var`, y no una nueva variable local con el mismo nombre. Esto permite que la función tenga acceso tanto a las variables locales definidas dentro de ella como a las variables globales definidas fuera de ella.

``` js title="JavaScript"
// Variable global por estar declarada en el ámbito principal
let globalVar = 10;

function funcion_local() {
    let localVar = 10  // Variable local

    console.log("Var local:", localVar)  // Acceso a la variable local
    console.log("Var global desde otro ámbito:", globalVar)  // Acceso a la variable global
    globalVar = globalVar + localVar; // Modifica la variable global
}

funcion_local();
console.log("Var global desde su ámbito:", globalVar)  // Acceso a la variable global desde su ámbito
```

``` title="Terminal (Entrada/Salida)"
Var local: 10
Var global desde otro ámbito: 10
Var global desde su ámbito: 20
```

> En JavaScript, aunque la inicialización `let globalVar = 10;` indique que la variable es local, al declararla en el ámbito principal, la variable será global.  
> Así se accede directamente a la variable `globalVar` dentro de `función_local` para poder utilizarla.  
> Esto permite que la función tenga acceso tanto a las variables locales definidas dentro de ella como a las variables globales definidas fuera de ella.

``` C++ title="C++"
#include <iostream>

// Variable global
int globalVar = 10;

void funcion_local() {
    int localVar = 10;  // Variable local

    std::cout << "Var local: " << localVar << std::endl;  // Acceso a la variable local
    std::cout << "Var global desde otro ámbito: " << globalVar << std::endl;  // Acceso a la variable global
    globalVar = globalVar + localVar;  // Modifica la variable global
}

int main() {
    funcion_local();
    std::cout << "Var global desde su ámbito: " << globalVar << std::endl;  // Acceso a la variable global desde su ámbito
    return 0;
}
```

``` title="Terminal (Entrada/Salida)"
Var local: 10
Var global desde otro ámbito: 10
Var global desde su ámbito: 20
```

> En C++ se accede directamente a la variable `globalVar` dentro de `función_local` para poder utilizarla.  
> Esto permite que la función tenga acceso tanto a las variables locales definidas dentro de ella como a las variables globales definidas fuera de ella.

En todos estos códigos, se declara una variable global y luego se accede y se modifica desde una función (en ámbito distinto al que fuera declarada la variable).  
Por último, se accede a la variable modificada desde su ámbito, demostrando el peligro que conlleva utilizar variables globales por los motivos que ya hemos visto y que volvemos a enunciar a continuación:

!!! failure "Mala práctica"
    El uso excesivo de variables globales puede llevar a un código confuso y propenso a errores, por lo que generalmente se recomienda minimizar su uso.

!!! success "Buena práctica"
    Cuando se trata de usar variables globales en funciones, es mejor pasar las variables como argumentos a las funciones y retornar los resultados.

    Este concepto lo estudiaremos en profundidad más adelante. Por el momento, te dejo la buena práctica.

## ¿Puede una variable local, dentro de su ámbito, reemplazar a una variable global?

Sí, si una variable local tiene el mismo nombre que una variable global, la variable local "reemplaza" u "oculta" a la variable global dentro de su ámbito de declaración o de los ámbitos contenidos dentro de su ámbito de declaración. Esto se conoce como "sombreado" o "_shadowing_". 

Sin embargo, este reemplazo es solo temporal y solo aplica dentro del ámbito local donde se declaró la variable local con el mismo nombre que la variable global.

Por ejemplo, en Python:

``` py title="Python"
x = 10  # Esta es una variable global

def mi_funcion():
    x = 5  # Esta es una variable local
    print(x)  # Imprime 5

mi_funcion()
print(x)  # Imprime 10
```

> En este código, dentro de `mi_funcion`, la variable local `x` reemplaza a la variable global `x`. Pero fuera de `mi_funcion`, la variable global `x` retiene su valor original.

!!! failure "Mala práctica"
    Es importante tener en cuenta que el uso de variables locales con el mismo nombre que las variables globales puede ser confuso y generalmente se considera una mala práctica de programación. 
    
    Es mejor usar nombres de variables únicos para evitar confusiones.

## ¿Puede una variable local, fuera de su ámbito, reemplazar a una variable global?

No, una variable local no puede reemplazar a una variable global fuera de su ámbito de declaración. El ámbito de una variable local está limitado la región o parte de código, como una función o un bloque, en el que se declara. Fuera de ese ámbito, la variable local no es reconocida por el programa.

Por ejemplo, en Python:

``` py title="Python"
x = 10  # Esta es una variable global

def mi_funcion():
    x = 5  # Esta es una variable local
    print(x)  # Imprime 5

mi_funcion()
print(x)  # Imprime 10
```

En este ejemplo, la variable local `x` solo existe dentro de `mi_funcion`. Fuera de `mi_funcion`, la variable local `x` no existe y no puede reemplazar a la variable global `x`.

!!! important "¡Para recordar!"
    Si intentas acceder a una variable local fuera de su ámbito, obtendrás un error porque la variable no está definida en ese ámbito.

Veamos si entendimos los conceptos.

!!! question "¿Qué ocurrirá cuando se ejecute la última línea del siguiente programa?"

    ``` py title="Python"
    global_var = 10

    def modificar_var_global():
        global global_var
        global_var += 5

    def usar_var_global_localmente():
        local_var = global_var * 2
        print("Var local:", local_var)

    print("Var global:", global_var)

    modificar_var_global()
    usar_var_global_localmente()

    print("Var global:", global_var)
    print("Var local:", local_var)
    ```

    Ver resultado (1)
    { .annotate }

    1. :material-code-tags-check:

        ``` title="Terminal (Entrada/Salida)"
        Var global: 10
        Var local: 30
        Var global: 15
        ```
        ``` {.py .consecutive}
        Traceback (most recent call last):
        File "…", line 17, in <module>
            print("Var local:", local_var)
                                ^^^^^^^^^
        Error: NameError: name ‘local_var' is not defined
        ```