# Game-of-Life

Materia: Algoritmos y Programación 1


Catedra: Essaya

Practica: Grace

Padron: 103471

Ayudante a Cargo: Daniela Riesgo

Alumno: Colombo, Juan Ignacio


El problema de calcular la cantidad de células adyacentes fue el que mas trabajo me dio.Primero tenia el problema de como calcular las celdas adyacentes, para ver esto se me ocurrió dibujar las celdas adyacentes a una para así analizar bien que necesitaba.Al analizarlo me di cuenta que el resultado para calcular las adyacentes a una, era hacer una matriz 3x3 en la cual el centro era la célula y las demás 8 celdas eran las adyacentes. Ya con eso calculado ya tenemos masomenos la estructura de como va a tener que ser nuestra función. Luego de hacer esto y de implementar el código, fui teniendo ciertos errores, como por ejemplo que mis células adyacentes eran mas de lo que tenían que ser o menos. Para darme cuenta bien de cuales erran los errores, fui poniendo prints en las variables y así analizar los datos que me daba la función y compararlo con los resultados de los asserts para así ir viendo cual era el resultado esperado. La funcion recibía una parte del juego life y así mismo una fila y columna.Para hacer esta matriz con centro que seria la celda a calcular sus adyacentes lo que se tenia que hacer es recibido una celda determinada, recorrerla desde la fila anterior hasta su posterior así, lo mismo con las columnas, para esto use 2 for, el primero que recorre las filas en un rango de la fila recibida menos uno , hasta la recibida mas 2, ya que el ultimo parámetro no es inclusivo, con las columnas pase a hacer lo mismo.El primer error que corregí, fue que cuando la función recorría la matriz y pasaba por el centro, esta no tenia que contarla ya que  es la celda a la que se le quieren calcular las adyacentes.Despues mi mayor problema era ver como hacer para calcular las demás ya que cuando el programa corría me saltaba un lis out of range. Despues de analizarlo vi que pasaba porque la función recibía a veces una lista con un carácter y al querer recorrer esa matriz cuando se me salía del rango.Despues de verlo un rato pude ver que cuando la función recorría la matriz y llegaba al largo de la lista, al ser un tablero infinito tenia que seguir recorriendo. Para esto hice que cuando llegue a ese punto que seria igual a la longitud de la lista, vuelva al valor -1 ya que usando slices python reconoce valores negativos. Despues las demás funciones no me presentaron muchas complicaciones, capas tenia errores y no sabia porque , pero me fue de mucha ayuda ver los asserts , para saber que se esperaba de una funcion, y también ver bien que recibía esta, ya que muchas veces no me salía porque ponía mal los parámetros recibidos.
