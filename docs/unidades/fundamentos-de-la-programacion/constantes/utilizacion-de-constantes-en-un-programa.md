title: Utilización de constantes en un programa

# Utilización de constantes en un programa

<label class="revision">Rev. 11/01/2024</label>

La utilización de una constante en un programa es cuando una instrucción de código accede a la constante para realizar alguna operación o acción con ella. 

## Sintaxis

En muchos lenguajes de programación, las constantes se declaran utilizando una sintaxis específica, usando una palabra clave especial, que generalmente suele ser `const`, y suelen seguir una convención de nombres en mayúsculas para diferenciarlas de las variables, que suelen tener nombres en minúsculas. 

``` js title="Sintaxis"

const nombre_del_tipo_de_dato NOMBRE_DE_CONSTANTE = asignación_de_valor
```

Es importante tener en cuenta que algunos lenguajes de programación también permiten especificar el tipo de dato de manera específica.

La sintaxis puede variar ligeramente entre los diferentes lenguajes de programación, por lo que es recomendable consultar la documentación oficial del lenguaje que estés utilizando para obtener detalles específicos sobre cómo definir constantes con tipos de dato específicos. 

``` js title="Declaración de constantes indicando el tipo de dato"
const float PI = 3.14159265359
const int HORAS_DEL_DIA = 24
const string NOMBRE_PLANETA = ”Tierra”
const int NUM1 = 4, NUM2 = 67
const char AFIRMACION = "s", NEGACION = "n"
```

``` js title="Declaración de constantes sin indicar el tipo de dato"
const PI = 3.14159265359
const HORAS_DEL_DIA = 24
const NOMBRE_PLANETA = ”Tierra”
const NUM1 = 4, NUM2 = 67
const AFIRMACION = "s", NEGACION = "n"
```

!!! important "¡Para recordar!"
    Como hemos dicho, las constantes se declaran utilizando una sintaxis específica, y suelen seguir una convención de nombres en mayúsculas para diferenciarlas de las variables, que suelen tener nombres en minúsculas.

Por ejemplo, en el lenguaje de programación C++, se puede declarar una constante entera de la siguiente manera:

``` c++ title="C++"
// Inicialización de la constante MI_CONSTANTE del tipo entero, con valor 10
const int MI_CONSTANTE = 10;
```

> En este caso, `MI_CONSTANTE` es el nombre de la constante y se le asigna el valor entero de 10. 

!!! warning "¡Muy importante!"
    Una vez inicializada la constante, el valor almacenado en ella no podrá ser modificado durante el resto del la ejecución del programa.

``` c++ title="C++"
// Inicialización de la constante PI del tipo de punto flotante, con valor 3.14
const float PI = 3.14; 

// Inicialización de la variable r del tipo de punto flotante, con valor 4
float r = 4;
std::cout << "Un círculo de radio " << r << " cm tiene " << (2 * PI * r) << " cm de perímetro.";
```

> En el ejemplo anterior, el programa imprimirá en pantalla "Un círculo de radio 2 cm tiene 25.12 cm de perímetro."









