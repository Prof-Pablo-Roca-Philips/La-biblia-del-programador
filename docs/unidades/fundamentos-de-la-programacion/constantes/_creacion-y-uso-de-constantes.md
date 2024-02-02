title: Creación y uso de constantes

!!! warning "reformular"

!!! important "¡Para recordar!"
    Como hemos dicho, las constantes se declaran utilizando una sintaxis específica, y suelen seguir una convención de nombres en mayúsculas para diferenciarlas de las variables, que suelen tener nombres en minúsculas.

Por ejemplo, en el lenguaje de programación C++, se puede declarar una constante entera de la siguiente manera:

``` c++ title="C++"
// Inicialización de la constante MI_CONSTANTE del tipo entero, con valor 10
const int MI_CONSTANTE = 10;
```

> En este caso, MI_CONSTANTE es el nombre de la constante y se le asigna el valor entero de 10. 

``` warning "¡Muy importante!"
Una vez inicializada la constante, el valor almacenado en ella no podrá ser modificado durante el resto del la ejecución del programa.
```

``` c++ title="C++"
// Inicialización de la constante PI del tipo de punto flotante, con valor 3.14
const float PI = 3.14; 

// Inicialización de la variable r del tipo de punto flotante, con valor 4
float r = 4;
std::cout << "Un círculo de radio " << r << " cm tiene " << (2 * PI * r) << " cm de perímetro.";
```

> En el ejemplo anterior, el programa imprimirá en pantalla "Un círculo de radio 2 cm tiene 25.12 cm de perímetro."