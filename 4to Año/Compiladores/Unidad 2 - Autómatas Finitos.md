# Definición Automáta
Máquina automática programable capaz de realizar determinadas operaciones de manera autónoma y sustituir a los seres humanos en algunas tareas _pesadas, repetitivas o peligrosas_.

## Según la profe:
Es una máquina que tiene movimientos, y, si es programable, se puede asociar a un robot.

## Teoría de autómatas
Estudio matemátio de máquinas abstractas, las cuales vemos en la unidad 2.

# ¿Qué es?
Un autómata finito es un modelo matemático que tiene entradas y produce salidas discretas. En un momento dado puede estar en cualquiera de los estados o configuraciones. Para determinar cuál es el comportamiento del autómata, basta con conocer cuál es el estado actual y cuál es la entrada actual.

# ¿Por qué es importante estudiar autómatas?
Existen disciplinas que utilizan la teoría de autómatas para resolver distintos problemas. En nuestro caso, esta teoría nos va permitir implementar el análisis léxico, que es una de las fases del proceso de compilación. 

- Analizador léxico de un compilador
- Software para diseñar/verificar circuitos digitales
- En robótica para diseñar e implementar un comportamiento
- En minería de texto para detectar palabras, frases u otros patrones.
- Software que verifique sistemas de todo tipo que tienen un número finito de estados distintos (ej: protocolos de comunicaciones)
- En industrias, control de procesos, envasado, embotellado, etc

# Ejemplo
## Contexto
Modelar el comportamiento de una máquina expendedora de boletos

## Estado inicial
Máquina lista para recibir boleto

## Estado final
Máquina devuelve boleto correctamente

## Estados del Contexto

 ``` mermaid
 flowchart TD;
	I(Inicial)
	T(Tarjeta Puesta)
	E(Error de lectura)
	D(Descuento de saldo)
	F(Final)

	I --> T
	T --> E
	T --> D
	D --> F
 ```

# Autómata Finito
Es una máquina conceptual, un dispositivo que puede estar en cualquiera de un número finito de estados, de los cuales uno es el inicial y uno o más son de aceptación.

![[Pasted image 20220807050513.png]]


## Formas de representarlo
### Diagrama
Es un diagrama de transiciones, osea, una colección finita de círculos con nombre, que son los estados.

#### Sintaxis del diagrama

Los estados están conectados por flechas o arcos y deben estar etiquetados con uno o más símbolos del alfabeto del lenguaje de entrada.

Un **estado inicial** debe estar marcado con una flecha.

Uno o más **estados finales o de aceptación** que designan posiciones del diagrama donde se ha reconocido una cadena válida.

![[Pasted image 20220807050911.png]]
**doble circulo**: estado de aceptación
**Circulo simple**: estado de error

#### Ejemplo diagrama
![[Pasted image 20220807050941.png]]

la cadena _"2indice"_ termina en el estado 2, osea en error
cualquier otra cadena que no empieze en número termina en el estado 3, osea que es aceptada

## Tabla de transiciones
Es una matriz bidimensional que resume el diagrama de transiciones
![[Pasted image 20220807051455.png]]

# Autómata Finito Determinista AFD
es una quíntupla $$ M = \{S, \Sigma, \delta, s_{0}, F\} $$
- **S**:  es un **conjunto finito de estados**
- **Sigma** (signo de sumatoria): **alfabeto de la máquina**
- **Delta**: una **función de transicón**
- **S_{0}**: el **estado inicial**, que pertence a S
- **F**: subconjunto de S, que agrupa a **estados de aceptación**

## Ejemplo
![[Pasted image 20220807052356.png]]

# Aceptación de cadenas
Un AF acepta una cadena de entrada si, tras comenzar sus cálculos en el estado inicial con la cabeza de lectura en el primer símbolo de la cinta de entrada, la máquina queda en un estado de aceptación después de leer el último símbolo de la cadena. Si no queda en un estado de aceptación, la cadena ha sido rechazada.

![[Pasted image 20220807052614.png]]

Una cadena de símbolos es aceptada por el autómata finito, sí y solo sí, los símbolos que aparecen en la cadena corresponden a una secuencia de arcos desde el estado inicial a un estado final

## Definición matemáticamente
![[Pasted image 20220807052757.png]]

## Caso especial: Cadena vacía
- Se representa con la letra griega epsilon (o lambda)
- Un AF acepta epsilon (o lambda), sí y solo sí, el estado inicial es un estado de aceptación
- La máquina llega al final de la cinta sin leer ningún símbolo
![[Pasted image 20220807053155.png]]

# Determinismo
Un AF es determinista si de cada estado a lo sumo sale un arco por cada símbolo del alfabeto.
![[Pasted image 20220807053326.png]]

En la práctica no se muestran todos los arcos, aunque existan, porque con alfabetos grandes, puede resultar muy complejo el diagrama

Las transiciones no definidas (error) se dirigen a un nodo "sumidero", que por convención no se muestra en el diagrama.


# Implementación en código
![[Pasted image 20220807053808.png]]

# Ejercicios
## Construir un AF que determine si un número entero positivo es divisible por 2 
### (v1)
![[Pasted image 20220807060233.png]]
S = {1, 2, 3, 4, 5, 6, 7, 8, 9}

Alfabeto: todo x tal que, x pertenece a los reales

Estado inicial: 1

Estados de aceptación: {5}

Función de transición:

estado / entrada | numero entero positivo par | numero entero positivo impar | numero entero negativo | numero decimal | texto
-- | -- | -- | -- | -- | --
1 | 2 | 2 | 2 | 2 | 6
2 | 3 | 3 | 3 | 7
3 | 4 | 4 | 8
4 | 5 | 9 |
5 (F) | 5 | 5 | 5 | 5 | 5
6 | error | error | error | error | error
7 | error | error | error | error | error
8 | error | error | error | error | error
9 | error | error | error | error | error

### (v2)
![[Pasted image 20220807202755.png]]
S = {1, 2,3}
Alfabeto = todo x tal que, x pertenece a los enteros positivos
Estado inicial = 1
Estados de aceptación = {2}
Función de transición:
estado / entrada | numero entero positivo par | numero entero positivo impar
-- | -- | --
1 | 2 | 3
2 | 2 | 2
3 | error | error

### v3
![[Pasted image 20220808162744.png]]


## Construir un AF con alfabeto = {x, y} que acepte cadenas de longitud par y mayor que 1
### v1
![[Pasted image 20220807205616.png]]
Estados = {1, 2, 3, 4, 5, 6, 7}
Alfabeto = {x, y}
Estado inicial = 1
Estados de aceptación = {3, 4, 6, 7}
Función de transición:
estado / entrada | x | y
-- | -- | --
1 | 2 | 3
2 | 3 | 4
3 | 2 | 5
4 | 2 | 5
5 | 6 | 7
6 | 2 | 5
7 | 2 | 5

### v2
![[Pasted image 20220807210448.png]]
Estados = {1, 2, 3}
Alfabeto = {x, y}
Estado inicial = 1
Estados de aceptación = {3}
Función de transición:
estado / entrada | x | y
-- | -- | --
1 | 2 | 2
2 | 3 | 3
3 | 2 | 2

## Construir un AF que acepte enteros y reales
![[Pasted image 20220808165445.png]]
Estados = {1, 2, 3, 4}
Alfabeto = {-, ., 0, 1, 2, 3, 4, 5, 6, 7, 8, 9}
Estado inicial = 1
Estados de Aceptación = {2, 3}
Función de transición:
estado / entrada | digito | signo menos | signo punto
-- | -- | -- | --
1 | 2 | 4 | error
2 | 2 | error | 3
3 | 3 | error | error
4 | 2 | error | error

decimal | binario
-- | --
0 | 0
1 | 1
2 | 10
3 | 11
4 | 100
5 | 101
6 | 110
7 | 111
8 | 1000
9 | 1001
10 | 1010
11 | 1011
12 | 1100
13 | 1101
14 | 1110
15 | 1111
16 | 10000
