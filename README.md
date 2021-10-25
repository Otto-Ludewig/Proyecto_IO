# Programacion Entera, Transporte y Variables Binarias

En este repositorio estan recopilados los Python Notebook que repasan los contenidos y las herramientas que resuelven los dos modelos evaluados en la ultima asignacion de Investigacion de Operaciones I. A su vez, he hecho un esfuerzo por recluirme exclusivamente a las herramientas que, hasta ahora, desconocia en el planteamientos y resolucion de problemas de Optimizacion, como lo son Python, Jupyter, Markdown y GitHub. Ha sido un camino intenso de dos semanas que culminan en este mismo repositorio.
Antes de entrar de lleno con los Notebook, sera cuestion de repasar los principios teoricos que sustentan este trabajo, partiendo de la Programacion Entera.

***

# Programacion Entera
 
La Programacion Entera es el area de problemas y modelos de la Programacion Lineal que restringen los valores de las variables de decision a valores enteros. Esto  es importante a la hora de trabajar planteamientos donde los valores no pueden tomar cantidades continuas, como cantidad de cajas en un vehiculo de transporte, cantidad de vehiculos que transitan en una ruta planificada o la construccion de instalaciones nuevas para la extension de una empresa. Desde lineas de ensamblaje hasta cadenas de suministro, muchas veces se necesitan plantear los problemas con restricciones enteras para hallarles verdaderas aplicaciones, obligando a matematicos, computistas, administradores y demas profesionales del area a idear y concebir metodos que encuentren esas soluciones.

## Branch and Bound

Como ejemplo de lo previamente dicho esta el metodo *Branch and Bound*, que construye nuevas restricciones sobre un modelo de Programacion Lineal. 
Para esto empezamos desde una **solucion relajada**. La solucion relajada es un conjunto de valores reales que maximizan (o minimizan) nuestra ![funcion](https://user-images.githubusercontent.com/92872432/138626944-31e16eb7-ddc5-44dd-bbd6-b0b363f39850.png) objetivo sobre la que buscamos el valor ![con la mayor expresion decimal](https://user-images.githubusercontent.com/92872432/138627352-15e2a23d-2974-4813-a3f3-b90b59ecf73c.png) entre todas las variables de decision. A partir de aqui estudiamos agregar , ![una de dos restricciones nuevas](https://user-images.githubusercontent.com/92872432/138627696-20deaf00-6473-4cd2-99ff-49d950520d4d.png), la que mejor se adecua a buscar el resultado deseado en Z. Este proceso sigue hasta hallar la solucion con valores enteros mas alta posible, en cada iteracion agregando una nueva restriccion.

## Algunas caracteristicas de la Programacion Entera

- La programacion entera nos permite modelar tomas de decisiones binarias (Tal y como se explora en el ejercicio 11.1) ya que podemos restringir toda variable a tener valores de 0 y 1. Esto nos permite extender los limites de lo que era matematicamente eramos capaces de modelar, formalizando las tomas de decisiones a nuevas areas de trabajo.
- Una de las aplicaciones mas extensas de la Programacion Entera Lineal son los problemas de Transporte, donde tenemos una tabla de Costes entre un conjunto de espacios de salida, un conjunto de espacios de llegada, conectadas a traves de distintos caminos con distintos "costes" entre uno y otro, obligandonos a tomar solo un subconjunto de ellos en medidas especificas para hallar resultados optimos. Esto es util, por ejemplo,  a la hora de planificar rutas entre N Enlatadoras y M Almacenes, con MxN caminos entre si. Este principio lo expandemos en el ejercicio 8.1
- Si bien ![existen nociones de dualidad para modelos PEL](https://coral.ise.lehigh.edu/~ted/files/talks/DUALITY09.pdf) hay conceptos que toca redefinir o desechar de nuestros estudios en Optimizacion para ello, como los precios sombra. En vista de que los valores de las variables de decision no son continuas, no tenemos forma especifica de definir como afectan los cambios en las restricciones al valor de Z, ya que el conjunto de soluciones posibles permanece incierto.
***

Visto esta introduccion teorica hacia los temas de este proyecto, queda definir las herramientas de trabajo. Utilizaremos **PuLP** para modelar y resolver los planteamientos del ejercicio 8.1, un paquete de ```Python``` usado para este tipo de labores.

***

Sin nada mas que aportar, concluyo este documento, disponiendo de los Notebook referidos en este mismo repositorio.
