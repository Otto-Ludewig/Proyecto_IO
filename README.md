# Programacion Entera, Transporte y Variables Binarias

En este repositorio estan recopilados los Python Notebook que repasan los contenidos y las herramientas que resuelven los dos modelos evaluados en la ultima asignacion de Investigacion de Operaciones I. A su vez, he hecho un esfuerzo por recluirme exclusivamente a las herramientas que, hasta ahora, desconocia en el planteamientos y resolucion de problemas de Optimizacion, como lo son Python, Jupyter, Markdown y GitHub. Ha sido un camino intenso de dos semanas que culminan en este mismo repositorio.
Antes de entrar de lleno con los Notebook, sera cuestion de repasar los principios teoricos que sustentan este trabajo, partiendo de la Programacion Entera.

***

# Programacion Entera
 
La Programacion Entera es el area de problemas y modelos de la Programacion Lineal que restringen los valores de las variables de decision a valores enteros. Esto  es importante a la hora de trabajar planteamientos donde los valores no pueden tomar cantidades continuas, como cantidad de cajas en un vehiculo de transporte, cantidad de vehiculos que transitan en una ruta planificada o la construccion de instalaciones nuevas para la extension de una empresa. Desde lineas de ensamblaje hasta cadenas de suministro, muchas veces se necesitan plantear los problemas con restricciones enteras para hallarles verdaderas aplicaciones, obligando a matematicos, computistas, administradores y demas profesionales del area a idear y concebir metodos que encuentren esas soluciones.

## Branch and Bound

Como ejemplo de lo previamente dicho esta el metodo *Branch and Bound*, que construye nuevas restricciones sobre un modelo de Programacion Lineal. 
Para esto empezamos desde una **solucion relajada**. La solucion relajada es un conjunto de valores $x_{i} \in \mathbb{R}$ que maximizan (o minimizan) nuestra funcion:
$$\sum c_{i}x_{i} = Z$$
Partiendo de una solucion relajada, buscamos el valor $x_{i}$
