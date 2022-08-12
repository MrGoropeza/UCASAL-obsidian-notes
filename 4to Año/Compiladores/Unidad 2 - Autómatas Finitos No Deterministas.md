# Autómata Finito No Determinista
La definición de autómata finito determinista es determinista: dado un _estado_ y un _símbolo de entrada_, el _próximo estado_ queda determinado _unívocamente_. La característica de **no determinismo** le da al autómata finito la posibilidad de cambiar de estados en una forma que está solo parcialmente determinada por el símbolo actual y el estado actual, pues también _depende de una elección_. Si bien el concepto de no determinismo aparece como una extensión de determinismo y en muchos casos simplifica la descripción de los autómatas, es una característica no esencial ya que para todo autómata finito no determinista existe uno equivalente determinista.

Básicamente, existen más de una transición para el mismo símbolo.

## Definición
Un AFND es una quíntupla M = {S, sigma, delta, s0, F}

La diferencia con los AFD es la función delta de transición.

Al evaluar una entrada con la función, devuelve uno o más estados, un subconjunto de estados del autómata.

Una cadena de símbolos es aceptada por el AFND si existe una computación (camino) que acepta la cadena

Facilitan la construcción de autómatas complejos
![[Pasted image 20220812012542.png]]

La tabla de transición es parecida a los AFD,
Las celdas de la tabla ya no tienen un único estado, sino que tienen conjuntos de estados

## Transiciones e
Utilizamos la cadena vacia para pasar de un estado a otro sin avanzar en la cinta de entrada.

## Transformación en código
Los AFND son dificiles de codificar.

## Equivalencia entre AFD y AFND
Teorema: Para cada AFND existe un AFD que acepta exactamente el mismo lenguaje.

### Demostración
Para probar el teorema, hay que demostrar:
1. Se puede construir un AFD M' a partir de un AFND M
2. M' acepta el mismo lenguaje que M


## Convertir AFND a AFD
Dado AFND M = (Q, Σ, delta, q0 , F) vamos a obtener AFD M' =(Q' , Σ' , delta', q0', F')

Q’ = los estados de M’ serán los subconjuntos de estados de M, es decir
Q’ = P(Q) (el número de estados de M’ es 2 a la cantidad de estados de Q)

Σ' = Σ

q0 ’ = `[q0]`

F’ = es el conjunto de todos los estados de Q’ que contengan por lo menos un elemento de F

![[Pasted image 20220812013451.png]]

![[Pasted image 20220812014242.png]]

De la transfromación surgen estados inalcanzables, los cuales podemos eliminar
![[Pasted image 20220812014547.png]]

![[Pasted image 20220812014634.png]]

Los estados inalcanzables son aquellos que no aparecen en la parte interna de la tabla de transiciones

# Ejercicios
a. indicar cuales son las cadenas reconocidas
b. construir un AFD equivalente
## primero
![[Pasted image 20220812014917.png]]
acepta las cadenas de 0's y 1's que terminen en "01"

AFD equivalente:
Q' = {[s0], [s1], [s2], [s0, s1], [s1, s2], [s0, s2], [s0, s1, s2], []}
F' = {[s2], [s1, s2], [s0, s2], [s0, s1, s2]}

funcion de transición delta:
delta'([s0], 0) = delta([s0], 0) = [s0, s1]
delta'([s0], 1) = [s0]

delta'([s1], 0) = []
delta'([s1], 1) = [s2]

delta'([s2], 0) = []
delta'([s2], 1) = []

delta'([s0, s1], 0) = delta([s0], 0) U delta([s1], 0) = [s0, s1] U [] = [s0, s1]
delta'([s0, s1], 1) = delta([s0], 1) U delta([s1], 1) = [s0] U [s2] = [s0, s2]

delta'([s1, s2], 0) = delta([s1], 0) U delta([s2], 0) = [] U [] = []
delta'([s1, s2], 1) = delta([s1], 1) U delta([s2], 1) = [s2] U [] = [s2]

delta'([s0, s2], 0) = delta([s0], 0) U delta([s2], 0) = [s0, s1] U [] = [s0, s1]
delta'([s0, s2], 1) = delta([s0], 1) U delta([s2], 1) = [s0] U [] = [s0]

delta'([s0, s1, s2], 0) = delta([s0], 0) U delta([s1], 0) U delta([s2], 0) = [s0, s1] U [] U [] = [s0, s1]
delta'([s0, s1, s2], 1) = delta([s0], 1) U delta([s1], 1) U delta([s2], 1) = [s0] U [s2] U [] = [s0, s2]

tabla de transiciones completa:
delta' | 0 | 1
-- | -- | --
->		[s0] | [s0, s1] | [s0]
		[s1] | [] | [s2]
(F)		[s2] | [] | []
	[s0, s1] | [s0, s1] | [s0, s2]
(F)	[s1, s2] | [] | [s2]
(F) [s0, s2] | [s0, s1] | [s0]
(F) [s0, s1, s2] | [s0, s1] | [s0, s2]
		[]   | [] | []

tabla de transiciones sin estados inalcanzables:
delta' | 0 | 1
-- | -- | --
		->[s0] | [s0, s1] | [s0]
	[s0, s1] | [s0, s1] | [s0, s2]
(F) [s0, s2] | [s0, s1] | [s0]

![[Pasted image 20220812044643.png]]

## segundo
![[Pasted image 20220812014951.png]]

acepta: cadena vacia y cadenas de formato: "a1b00c" donde:
- a: cualquier cadena binaria
- b: cadena de 0's de cualquier tamaño
- c: cadena de 1's de cualquier tamaño


AFD equivalente:
Q' = {[s0], [s1], [s2], [s3], [s0, s1], [s0, s2], [s0, s3], [s1, s2], [s1, s3], [s2, s3], [s0, s1, s2], [s0, s2, s3], [s0, s1, s3], [s1, s2, s3], [s0, s1, s2, s3], []}

F' = {[s0], [s3], [s0, s1], [s0, s2], [s0, s3], [s1, s3], [s2, s3], [s0, s1, s2], [s0, s2, s3], [s0, s1, s3], [s1, s2, s3], [s0, s1, s2, s3]}

**solo voy a ir calculando los estados que aparezcan**
delta'([s0], 0) = delta([s0], 0) = [s0]
delta'([s0], 1) = delta([s0], 1) = [s0, s1]

delta'([s0, s1], 0) = delta([s0], 0) U delta([s1], 0) = [s0] U [s1, s2] = [s0, s1, s2]
delta'([s0, s1], 1) = delta([s0], 1) U delta([s1], 1) = [s0, s1] U [] = [s0, s1]

delta'([s0, s1, s2], 0) = delta([s0], 0) U delta([s1], 0) U delta([s2], 0) = [s0] U [s1, s2] U [s3] = [s0, s1, s2, s3]
delta'([s0, s1, s2], 1) = delta([s0], 1) U delta([s1], 1) U delta([s2], 1) = [s0, s1] U [] U [] = [s0, s1]

delta'([s0, s1, s2, s3], 0) =
	delta([s0], 0) U delta([s1], 0) U delta([s2], 0) U delta([s3], 0) =
	[s0] U [s1, s2] U [s3] U [] = [s0, s1, s2, s3]
delta'([s0, s1, s2, s3], 1) =
	delta([s0], 1) U delta([s1], 1) U delta([s2], 1) U delta([s3], 1) =
	[s0, s1] U [] U [] U [s3] = [s0, s1, s3]

delta'([s0, s1, s3], 0) = delta([s0], 0) U delta([s1], 0) U delta([s3], 0) = [s0] U [s1, s2] U [] = [s0, s1, s2]
delta'([s0, s1, s3], 1) = delta([s0], 1) U delta([s1], 1) U delta([s3], 1) = [s0, s1] U [] U [s3] = [s0, s1, s3]

tabla de transiciones:
delta' | 0 | 1
-- | -- | --
-> (F)			[s0] | [s0] | [s0, s1]
(F)			[s0, s1] | [s0, s1, s2] | [s0, s1]
(F)	    [s0, s1, s2] | [s0, s1, s2, s3] | [s0, s1]
(F) [s0, s1, s2, s3] | [s0, s1, s2, s3] | [s0, s1, s3]
(F)		[s0, s1, s3] | [s0, s1, s2] | [s0, s1, s3]
![[Pasted image 20220812044633.png]]

# Observaciones conversión AFND a AFD
1. El AFD puede verse más complejo por tener más estados y transiciones, pero es más sencillo de programar que el AFND
2. No siempre es sencillo ver que cadenas aceptan los automatas, más adelante vemos como obtener las cadenas aceptadas
3. Los estados tienen nombres, pueden renombrarse
4. Existe un algoritmo para optimizar un automata finito, el cual va a tener menos estados

# Autómatas Finitos Traductores
Existen otros tipos de autómatas finitos, que además de reconocer cadenas, pueden generar un cómputo, es decir tienen una salida. Se trata de los autómatas finitos traductores, en particular, describimos los autómatas:
- **Máquina de Moore:** el resultado está asociado al estado donde finaliza el autómata
- **Máquina de Mealy**: el resultado está asociado a las transiciones del autómata
