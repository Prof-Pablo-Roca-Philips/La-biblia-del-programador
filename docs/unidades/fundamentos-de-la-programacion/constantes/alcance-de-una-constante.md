title: Alcance de una constante

# Alcance de una constante

<label class="revision">Rev. 15/01/2024</label>

En la mayoría de los lenguajes de programación, al igual que las variables, las constantes tienen un alcance.

!!! abstract "Definición"
    El alcance de una constante en programación se refiere a la región o parte de código donde una constante existe y es accesible para poder ser utilizada. 

Es importante tener en cuenta que el alcance de una constante va a estar determinado por el ámbito en el que se declara.

En muchos lenguajes de programación, el alcance de una constante es global, lo que significa que la constante es accesible desde cualquier parte del programa. Por ejemplo, si se declara una constante al inicio del programa, esa constante puede ser utilizada en cualquier función, clase o módulo dentro del programa.

Sin embargo, algunos lenguajes de programación permiten declarar constantes con alcance local, limitando su visibilidad y acceso a una función, bloque o ámbito específico. Por ejemplo, si se declara una constante dentro de una función, esa constante solo será visible dentro de esa función y no estará disponible fuera de ella, en otras partes del programa.

Así, el alcance de una constante determina dónde es visible y accesible en el código. Aquí hay algunos ejemplos en diferentes lenguajes para que veas, pero no te preocupes si la sintaxis te resulta compleja, son solo ejemplos:


* JavaScript: Las constantes declaradas con `const` tienen un alcance de bloque, lo que significa que sólo son accesibles dentro del bloque en el que se declararon.

``` js title="JavaScript"
{
    const MY_CONST = 'Hello, world!';
    console.log(MY_CONST); // 'Hello, world!'
}
console.log(MY_CONST); // ReferenceError: MY_CONST is not defined
```

* Java: Las constantes en Java, declaradas con final, tienen un alcance dependiendo de dónde se declaren. Si se declaran dentro de un método, sólo son accesibles dentro de ese método. Si se declaran a nivel de clase, son accesibles para toda la clase.

``` Java title="Java"
public class Main {
    final static String CLASS_CONSTANT = "Class constant";

    public static void main(String[] args) {
        final String METHOD_CONSTANT = "Method constant";
        System.out.println(CLASS_CONSTANT); // "Class constant"
        System.out.println(METHOD_CONSTANT); // "Method constant"
    }

    public static void anotherMethod() {
        System.out.println(CLASS_CONSTANT); // "Class constant"
        System.out.println(METHOD_CONSTANT); // Error: Cannot resolve symbol 'METHOD_CONSTANT'
    }
}
```

* C++: Las constantes en C++, declaradas con const, tienen un alcance que depende de dónde se declaren. Si se declaran dentro de una función, sólo son accesibles dentro de esa función. Si se declaran fuera de todas las funciones, son accesibles para todo el archivo.

``` C++ title="C++"
#include <iostream>

const int GLOBAL_CONSTANT = 10;

int main() {
    const int LOCAL_CONSTANT = 20;
    std::cout << GLOBAL_CONSTANT << std::endl; // 10
    std::cout << LOCAL_CONSTANT << std::endl; // 20
}

void anotherFunction() {
    std::cout << GLOBAL_CONSTANT << std::endl; // 10
    std::cout << LOCAL_CONSTANT << std::endl; // Error: 'LOCAL_CONSTANT' was not declared in this scope
}
```

Por lo tanto, aunque la sintaxis y las reglas exactas pueden variar, la idea general de que las constantes tienen un alcance es común en muchos lenguajes de programación.

Recuerda que todos los conceptos de alcance que se aplican a las constantes son los mismos que los aplicados a las variable. Así que, si necesitas repasarlos, puedes acceder a la documentación haciendo clic [aquí](../../variables/alcance-de-una-variable/){:target="_blank"}.
