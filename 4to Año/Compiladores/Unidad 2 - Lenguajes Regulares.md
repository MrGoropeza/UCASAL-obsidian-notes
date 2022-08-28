# Cadena
## Definición
Es una secuencia de símbolos del alfabeto Σ (Σ es el alfabeto)

La longitud de una cadena |w| es el número de símbolos de la cadena w

Σ*: conjunto de todas las cadenas que pueden formarse a partir de Σ
- ε siempre pertenece a Σ*

## Operaciones sobre cadenas
### Concatenación
Si x e y son cadenas, x.y es la concatenación de x e y
El operador “concatenación” es `.` pero se omite
![[Pasted image 20220828135748.png]]

### Exponenciación
Concatenación repetida de la misma cadena
![[Pasted image 20220828135801.png]]

# Lenguaje
## Definición
Lenguaje: es un subconjunto de Σ*
- un conjunto de cadenas definidas sobre un alfabeto Σ

## Lenguaje Regular
Si M=(S, Σ, δ, s0 , F), el lenguaje aceptado por M => L(M) es la colección de cadenas que M acepta y es un subconjunto de Σ*
`w ϵ L(M) <=> δ(s0 , w) ϵ F`

Un lenguaje L(M), donde M es un autómata finito se denomina lenguaje regular 

## Ejemplos
### Primero
![[Pasted image 20220828140055.png]]

### Segundo
![[Pasted image 20220828140104.png]]

### Casos especiales
Los 3 son lenguajes regulares:
![[Pasted image 20220828140126.png]]

## Operaciones sobre lenguajes
Dados dos lenguajes L y M:
### Unión
L U M = {s | s ϵ L ó s ϵ M}

### Concatenación
LM = {st | s ϵ L y t ϵ M}

### Estrella de Kleene
![[Pasted image 20220828140259.png]]

### Cerradura Positiva
![[Pasted image 20220828140309.png]]

### Ejemplos
![[Pasted image 20220828140355.png]]

### Teorema
![[Pasted image 20220828140409.png]]
#### Demostración
Si L1 y L2 son lenguajes regulares entonces son reconocidos por AFs
![[Pasted image 20220828140457.png]]

![[Pasted image 20220828140508.png]]

![[Pasted image 20220828140519.png]]

![[Pasted image 20220828140526.png]]


# Límites de los autómatas finitos
Existen lenguajes que no son regulares, no pueden ser reconocidos por AFs (deterministas o no)
Ej: expresiones matemáticas con paréntesis -> deben estar bien balanceados (anidados)
• Ej. (4+(2*(8-1))) -> ((( )))
• Ej. (4-1)+(2*(8-1)) -> ()(( ))

# Lema de bombeo
## Lema de bombeo para lenguajes regulares (informal) 
Cualquier palabra suficientemente larga en un lenguaje puede ser bombeada o sea repetir una sección de la palabra un número arbitrario de veces y producir una nueva palabra que también pertenece al mismo lenguaje

## Demostración (intuitiva)
![[Pasted image 20220828140920.png]]
![[Pasted image 20220828140928.png]]

## Consecuencias
![[Pasted image 20220828140953.png]]

- Los AFs pueden encargarse de reconocer algunos componentes de un lenguaje de programación
	- Ej. reconocer identificadores, palabras reservadas, operadores (análisis léxico)
- Pero no pueden encargarse de los aspectos de la sintaxis de un lenguaje de programación
	- Para el análisis sintáctico necesitaremos otro tipo de autómatas más potentes

# Expresiones Regulares
Describe un conjunto de cadenas sin enumerar sus elementos.
	Ej. el grupo formado por las cadenas Handel, Händel y Haendel se describe mediante el patrón H(a|ä|ae)ndel
- es una forma de representar a los lenguajes regulares (finitos o infinitos)
- se construye utilizando símbolos del alfabeto sobre el cual se define el lenguaje
- operadores unión, concatenación y clausura de Kleene
## Definición
![[Pasted image 20220828163246.png]]

## Ejemplos
![[Pasted image 20220828163258.png]]

# Teorema de Kleene
Un lenguaje es regular si y solo si es reconocido por un autómata finito

## Demostración 1 (ER -> AF)
Teorema: Dado un lenguaje regular, representado por una ER, existe un AFND que lo reconoce Demostración:
- Por construcción del AFND (construcción de Thompson)
- Para cada la regla que define expresiones regulares se pueden escribir un AFND con transiciones ε
![[Pasted image 20220828163440.png]]
![[Pasted image 20220828163447.png]]

## Demostración 2 (AF -> ER)
Lema: Si ω, β y γ son expresiones regulares sobre el alfabeto Σ y L(γ) no contiene la cadena ε, entonces la ecuación ω=β + ω γ tiene una única solución ω=β γ*

• Con este lema podemos resolver ecuaciones sobre cadenas
• Hay que encontrar una forma (un algoritmo) de expresar la información del AF en ecuaciones y luego resolverlas

![[Pasted image 20220828163555.png]]
![[Pasted image 20220828163603.png]]

## Ejemplo
![[Pasted image 20220828163644.png]]
![[Pasted image 20220828163652.png]]
![[Pasted image 20220828163705.png]]
