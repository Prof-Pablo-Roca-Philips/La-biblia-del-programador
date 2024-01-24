title: Identificador de una variable

## Definición

El nombre de una variable en programación debe ser descriptivo y significativo, de manera que refleje el propósito o contenido del valor que almacenará la variable. 

Utiliza nombres que sean claros y comprensibles: elige nombres que sean fácilmente entendibles para cualquier persona que lea tu código. Evita utilizar nombres crípticos o abreviaturas confusas.

Utiliza nombres en español: a menos que estés trabajando en un proyecto específico en otro idioma, se recomienda utilizar nombres de variables en español para mantener la consistencia y facilitar la colaboración con otros desarrolladores. Eso si, procura no utilizar caracteres especiales como los acentuados o la ñ. Esto podría acarrear problemas a la hora de la compilación o interpretación del programa.

Utiliza sustantivos para nombrar objetos y variables: las variables suelen representar objetos o valores en tu código, por lo que es recomendable utilizar sustantivos para nombrarlas. Por ejemplo, en lugar de usar dato o valor, utiliza nombres más específicos como nombre, edad, resultado, etc.

Elige un estilo de casing (como camel case o snake case): aplíca el estilo de manera consistente en tus nombres de variables. Esto mejorará la legibilidad del código y facilitará la diferenciación de palabras dentro del nombre de la variable.

Evita nombres demasiado largos: aunque es importante que el nombre de la variable sea descriptivo, trata de no excederte en longitud. Nombres demasiado largos pueden hacer que el código sea difícil de leer y escribir. Encuentra un equilibrio entre la claridad y la concisión.

## Pautas generales para nombrar variables

Cuando se nombran variables, es importante seguir algunas convenciones de nombramiento (naming convention) para hacer el código legible y permitir un mantenimiento ágil y simple:

* El nombre debe ser semántico y descriptivo del valor asignado a la variable.
```
int edad # edad almacenará un dato entero referido a la edad de algo o alguien
```

* Es conveniente que la longitud no pase de 20 caracteres. Y nunca más de 32 caracteres.

* Debe iniciar con una letra o símbolo _, NUNCA CON UN NÚMERO, pudiendo contener a continuación tanto letras como números
```
int numero1, _numero1, 1numero # el identificador de la última variable es inválido
```

* Se pueden utilizar combinaciones de letras mayúsculas y minúsculas, dígitos y el símbolo _

* En algunos lenguajes, las mayúsculas y minúsculas de una misma letra son tratadas diferente
```
int nombre, Nombre, nombrE, NombrE # todas son diferentes variables
```

* Debe responder a un estilo de nombre válido (ver convención utilizada para nombrar variables aquí)
```
camel_case, snakeCase, PascalCase, InValid_Case # El último estilo no está estandarizado
```

* Se deben emplear mayúsculas para indicar constantes.

## Convención utilizada para nombrar variables (_casing_)

En programación, el término **casing** se refiere a la convención que se utiliza para nombrar variables, funciones y otros elementos en el código fuente, cuando dicho nombre se compone de dos o más palabras. 

Hay varios estilos de **casing** comunes utilizados en programación, que incluyen:

* **Camel Case**: En este estilo, la primera letra de la primera palabra se escribe en minúscula y la primera letra de las palabras siguientes se escribe en mayúscula, sin espacios ni guiones entre las palabras. 
		
    ```
    cosasParaHacer, edadDelAmigo, valorFinal
    ```

* **Pascal Case**: También conocido como Upper Camel Case, en este estilo, la primera letra de cada palabra se escribe en mayúscula, sin espacios ni guiones entre las palabras.
		
    ```
    CosasParaHacer, EdadDelAmigo, ValorFinal
    ```

* **Snake Case**: En este estilo, todas las letras se escriben en minúscula y las palabras se separan mediante guiones bajos (_).

    ```
    cosas_para_hacer, edad_del_amigo, valor_final
    ```     

* **Kebab Case**: Similar al Snake Case, pero las palabras se separan mediante guiones (-) en lugar de guiones bajos. 
		
    ```
    cosas-para-hacer, edad-del-amigo, valor-final
    ```
    
    !!! warning "Presta atención y cuidado!"
        Los nombre de variable en Kebab Case, en algunos lenguajes son interpretados como la resta de dos o más variables.

### Ejemplos

```
numero
dia_del_mes
pinguino1
ciudad
z
mes
Mes (distinto al anterior – case sensitive)
```

## ¿cómo no debe llamarse una variable?

Las siguientes pautas son muy importantes.  
¡Desconocerlas puede llevar a nombrar variables de manera incorrecta!

* No es conveniente utilizar nombres sin sentido semántico o descriptivo
	```
    string a # si bien sabemos que **a** almacenará una cadena, ¿De qué dato se tratará?
    ```

* NUNCA debe iniciar el nombre con UN NÚMERO, debe hacerlo con una letra o guión bajo
	```
    int numero1, _numero1, 1numero # el identificador de la última variable es inválido
    ```

* No debe ser palabra reservada (if, else, while, print, input, etc.) de la biblioteca del lenguaje

* No debe contener espacios
    ```
	string mi variable no puede tener espacios # este identificador es inválido
    ```

* No debe contener símbolos especiales como guiones, puntos, comas, comillas, etc. (excepto el guión bajo _ )

!!! success "¡Recuerda!"
    Las convenciones de nombramiento pueden variar según el lenguaje de programación que estés utilizando, así como las directrices establecidas por la comunidad o los estándares de codificación. 

    Es recomendable consultar la documentación o guías de estilo correspondientes al lenguaje o entorno en el que estés trabajando para seguir las mejores prácticas específicas.

### Ejemplos

```
123
_día
numero*
lugar de nacimiento
año
print
int
```
