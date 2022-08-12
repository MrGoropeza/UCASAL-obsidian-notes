# Ejercicio 1
## 1. Se tiene el siguiente programa lineal:
$$\begin{gather}  \text{max} \quad z=2x_{1} + 3x_{2} \\
\text{sujeto a:}
\begin{cases} 
x_{1}+3x_{2} \leq 6 \\
3x_{1}+2x_{2} \leq 6 \\
x_{1},x_{2} \geq 0
\end{cases}
\end{gather}$$
### a) Exprese el problema en forma de ecuaciones
$$
\begin{cases}
z - 2x_{1} - 3x_{2} = 0 \\
x_{1} + 3x_{2} + S_{1} = 6 \\
3x_{1} + 2x_{2} + S_{2} = 6 \\
\end{cases}
$$
### b) Determine todas las soluciones básicas del problema, y clasifíquelas como factibles y no factibles.
Básica | z | x1 | x2 | S1 | S2 | Solución | 
------ | - | -- | -- | -- | -- | -------- | ---
    z  | 1 | -2 | -3 | 0  | 0  | 0        | Fila z
	S1 | 0 | 1  | 3  | 1  | 0  | 6        | Fila S1
	S2 | 0 | 3  | 2  | 0  | 1  | 6        | Fila S2

# Ejercicio 2




# Ejercicio 5
## Inciso a
Primero usamos el criterio de optimalidad. Nos fijamos que variable optimiza más.
Seguiremos el camino:
A ==> G ==> F ==> E, ya que x2 optimiza mejor la función objetivo.

## Inciso b
Por el criterio de optimalidad, x1 optimiza mejor, por lo que recorreremos de la siguiente manera:
A ==> B ==> C ==> D ==> E

Por el criterio de factibilidad: tomar el mínimo de los valores que puede tomar x1:
Min{2, 3, 5} = 2

## Inciso c
Criterio de optimalidad: x2
Criterio de factibilidad: min{1,2,4}=1
Diferencia en Z = deltaZ = 4x2 = 4 . 1 = 4


# Punto 4


