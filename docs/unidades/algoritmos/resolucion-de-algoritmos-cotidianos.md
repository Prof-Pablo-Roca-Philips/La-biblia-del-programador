title: Resolución de algoritmos cotidianos

## Cómo ordenar una lista de números

Supongamos que tenemos una lista de números y queremos ordenarla de forma ascendente utilizando el algoritmo de burbuja. Aquí está el pseudocódigo del algoritmo:

``` title="Pseudocódigo"
Inicio
    1. Leer la lista de números.
    2. Establecer una variable "cambio" en verdadero.
    3. Mientras cambio sea verdadero, hacer:
    4. Establecer cambio en falso.
    5. Para cada par de elementos adyacentes en la lista, hacer:
        6. Si los elementos están en el orden incorrecto, intercambiarlos.
        7. Establecer cambio en verdadero.
    8. Imprimir la lista ordenada.
Fin
```

Este algoritmo recorre repetidamente la lista de números, comparando los elementos adyacentes y realizando intercambios si es necesario. Continúa haciendo esto hasta que no se realicen más intercambios, lo que indica que la lista está ordenada.

## Cómo cambiar la rueda de un auto

Existen algoritmos, que los ejecutamos casi sin darnos cuenta, que nos ayudan a resolver problemas diarios. 
Por ejemplo, el algoritmo para cambiar la rueda de un choche:

``` title="Pseudocódigo"
Inicio
    1. Agarrar el gato del auto
    2. Levantar el coche con el gato
    3. Aflojar tornillos de la rueda
    4. Sacar los tornillos de la rueda
    5. Quitar la rueda
    6. Agarrar la rueda de auxilio
    7. Poner la rueda de auxilio
    8. Poner los tornillos en la rueda de auxilio
    9. Ajustar los tornillos en la rueda de auxilio 
    10. Bajar el coche con el gato
    11. Sacar el gato
    12. Guardar el gato 
    13. Guardar la rueda sacada
Fin
```

!!! Question "Para resolver"
    ¿De qué manera podemos mejorar este algoritmo en términos de precisión, eficiencia y generalidad?
    
    Asumimos que, así como está planteado, ya cumple con la característica de ser finito.

## Cómo aceptar o rechazar el pedido de compra de un cliente

Veamos otro ejemplo: ¿qué pasa cuando un cliente realiza un pedido de compra a una fábrica? 

La fábrica examina en su banco de datos la cuenta del cliente. Si el cliente tiene crédito entonces la fábrica acepta el pedido, en caso contrario rechaza el pedido.

``` title="Pseudocódigo"
Inicio
    1. Recibir el pedido
    2. Examinar la cuenta del cliente
    3. Si el cliente tiene crédito entonces
        4. Aceptar el pedido
    5. Si no
        6. Rechazar el pedido
    7. Fin Si
Fin
```

!!! Question "Para resolver"
    ¿De qué manera podemos mejorar este algoritmo en términos de precisión, eficiencia y generalidad?

    Asumimos que, así como está planteado, ya cumple con la característica de ser finito.

## Cómo lavarse los dientes

!!! Question "Para resolver"
    ¿Cómo sería el algoritmo que ejecutamos cada vez que nos lavamos los dientes?

``` title="Pseudocódigo"
Inicio
    ...
    lavar los dientes
    ...
Fin
```

## Cómo tomar un café

!!! Question "Para resolver"
    ¿Cómo sería el algoritmo que ejecutamos cada vez que queremos tomar un café?

``` title="Pseudocódigo"
Inicio
    ...
    tomar el café
    ...
Fin
```