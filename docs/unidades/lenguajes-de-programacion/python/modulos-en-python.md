title: Uso de módulos en Python

``` py title="Python"
# Importa el módulo os
import os

# Limpia la pantalla
os.system("cls")
```

También es posible importar solamente una parte del módulo, para ahorrar espacio en memoria:

``` py title="Python"
# Importa la módulo os
from os import system

# Limpia la pantalla
system("cls")
```

> Cabe aclarar que la importación de módulos ocupa espacio en memoria. Si se puede evitar, hay que tratar de hacerlo.
> Por ejemplo, el siguiente código cumple con la mimsa tarea a nivel visual:

``` py title="Python"
# Limpia la pantalla
print("\033[2J\033[1H") 
```
