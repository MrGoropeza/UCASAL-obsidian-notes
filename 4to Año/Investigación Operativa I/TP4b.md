# Ejercicio 1
## Inciso a
Max z= 5x1 + 6x2

Sujeto a:
-2.x1 + 3.x2 + **R1**= 3
x1 + 2.x2  + **S1** <= 5
6.x2 + 7.x2 + **S2** <= 3

De esa forma , la función objetivo queda como:

Máx z = 5.x1 + 6.x2 + 0.S1 + 0.S2 - M.R1

`-M` porque estamos en un problema de maximización.
`R1` la variable artificial


## Inciso b
Max z= 2.x1 + 7.x2 

Sujeto a:
-2.x1 +3.x2 = 3
4.x1 + 5.x2 >= 10
6.x1 + 7.x2 <= 3
4.x1 + 8.x2 >= 5


Transformación:
max z = 2.x1 + 7.x2 - M.R1 - M.R2 - M.R3

-2.x1 +3.x2 + **R1** = 3
4.x1 + 5.x2 - **S1** + **R2** = 10
6.x1 + 7.x2  + **S2** = 3
4.x1 + 8.x2 - **S3** + **R3** = 5

Básicas | z | x1 | x2 | S1 | S2 | R1 | Solucióm
	  - | - | - | - | - | - | - | -
    z| 0  | -5 | -6 | 0 | 0 | M | 0
    R1| 0  | -2 | 3 | 0 | 0 | 1 | 3
    S1| 0  | 1 | 2 | 1 | 0 | 0 | 5
S2 | 0 | 6 | 7 | 0 | 1 | 0 | 3

Entonces:

Z = Zanterior + (M.renglon R1 . M.renglon R2)
