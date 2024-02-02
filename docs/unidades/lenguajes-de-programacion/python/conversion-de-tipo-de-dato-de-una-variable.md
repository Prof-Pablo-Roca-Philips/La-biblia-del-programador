a = int("3") + 4

b = str(3) + "4"

print(a, b)


## Ejercicios de aplicación

1. Escribe un programa que solicite el ingreso por teclado de datos referidos al nombre, el precio unitario y la cantidad de unidades vendidas de un producto.
Luego que imprima por pantalla una salida de información formateada de la siguiente manera:

    ``` title="Terminal (Entrada/Salida)"
    Ingrese el nombre del producto: Palta
	Ingrese el precio unitario del producto: 510.30
	Ingrese la cantidad de unidades compradas: 3

	Producto: Palta
	Precio unitario: 510.30
	Cantidad: 3
	----------------------------------
	Costo total de compra: 1530.90
    ```
    
	!!! warning "¡Atención! Alcance y Limitación"
		El costo total debe calcularse antes de realizar la impresión en pantalla.
		Presta atención al tratamiento de los decimales. Estamos hablando de dinero en algunos casos.

    ??? example "Ver solución propuesta"
        ``` py title="Python"
		nombre = input("Ingrese el nombre del producto: ")
		precio_unitario = float(input("Ingrese el precio unitario del producto: "))
		cantidad = int(input("Ingrese la cantidad de unidades compradas: "))

		costo_total = precio_unitario * cantidad

		print(f"Producto: {nombre}")
		print(f"Precio unitario: {format(precio_unitario, '.2f')}")
		print(f"Cantidad: {cantidad}")
		print("-"*34)
		print(f"Costo total de compra: {format(costo_total, '.2f')}")
		```

		!!! question "¡Para pensar!"
			¿Qué crees que hace la siguiente instrucción `format(precio_unitario, '.2f')`?

	---