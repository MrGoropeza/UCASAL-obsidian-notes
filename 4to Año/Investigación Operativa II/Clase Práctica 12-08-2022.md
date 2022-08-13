# Ejercicio Adicional 1
Pedrio subasta un billete de 50 euros entre Carlos y Blanca con las siguientes reglas: se juega por turnos. Aquel a quien le toca jugar puede pasar, o pujar con 20 euros más que el anterior (suponiendo que los tiene). Empieza Blanca (pasando o pujando con 20 euros). Si un jugador dcide pasar, ya no puede pujar en una jugada posterior. Gana el último en jugar, que se lleva el billete. Si ninguno ha pujado se llevan 25 euros cada uno. Ambos jugadores deben pagar su última puja. Aparte de las reglas es de conocimiento común que cada jugador tiene solo 60 euros.

```mermaid
flowchart TD;
	t1(Jugador 1)
	t2-1(Jugador 2)
	t2-2(Jugador 2)

	t1 --$20--> t2-1
	t1 --pasa--> t2-2

	empate(25, 25)
	gana2(0, 30)
	
	t2-2 --$20--> gana2
	t2-2 --pasa--> empate

	t3-1(Jugador 1)
	t3-2(30, 0)

	t2-1 --$20--> t3-1
	t2-1 --pasa--> t3-2

	t4-1( -10, -40)
	t4-2( -20, 10)

	t3-1 --$40--> t4-1
	t3-1 --pasa--> t4-2

```

# Ejercicio Adicional 2
Los jugadores (1 y 2) depositan de manera simultánea sendas monedas de un euro sobre una mesa.
Si resultan dos caras o dos cruces, el jugador 1 recoge los dos euros, mientras que si hay una cara y
una cruz, el jugador 2 se lleva los dos euros.

```mermaid
flowchart TD;
	t0(Jugada J1, J2 )

	2caras(1, -1)
	2cruz(1, -1)
	1cx( -1, 1)
	1xc( -1, 1)

	t0 --cara, cara--> 2caras
	t0 --cruz, cruz--> 2cruz
	t0 --cara, cruz--> 1cx
	t0 --cruz, cara--> 1xc
```
La version 1 esta mal porque cada nodo debe representar un jugador y cada flecha la estrategia por jugador.

Diagrama correcto:

```mermaid
flowchart TD;
	t0(Jugador1)
	t1-1(Jugador2)
	t1-2(Jugador2)

	t0 --C--> t1-1
	t0 --X--> t1-2

	t1-1-1(1, -1)
	t1-1-2( -1, 1)

	t1-2-1( -1, 1)
	t1-2-2( 1, -1)

	t1-1 --C--> t1-1-1
	t1-1 --X--> t1-1-2

	t1-2 --C--> t1-2-1
	t1-2 --X--> t1-2-2
```


# Trabajo Practico 1
## Ejercicio 1
Tabla de pagos:
Sindicato | 1,60 | 1,50 | 1,40 | 1,30 | 1,20 | 1,10
-- | -- | -- | -- | -- | -- | --
Compañia | - | - | - | - | - | -
1,10 | $1,35 | $1,50 | $1,40 | $1,30 | $1,20 | $1,10 
1,20 | $1,20 | $1,35 | $1,40 | $1,30 | $1,20 | $1,10
1,30 | $1,30 | $1,30 | $1,35 | $1,30 | $1,20 | $1,10
1,40 | $1,40 | $1,40 | $1,40 | $1,35 | $1,20 | $1,10
1,50 | $1,50 | $1,50 | $1,50 | $1,50 | $1,35 | $1,10
1,60 | $1,60 | $1,60 | $1,60 | $1,60 | $1,60 | $1,35

Tabla de suma cero (desde la vista de la compañia):
Sindicato | 1,60 | 1,50 | 1,40 | 1,30 | 1,20 | 1,10
-- | -- | -- | -- | -- | -- | --
Compañia | - | - | - | - | - | -
1,10 | -0,25 | -0,40 | -0,30 | -0,20 | -0,10 | 0 
1,20 | 0 | -0,25 | -0,40 | -0,30 | 0 | -0,10
1,30 | 0 | 0 | -0,25 | 0 | -0,20 | -0,10
1,40 | 0 | 0 | 0 | -0,25 | -0,20 | -0,10
1,50 | 0 | 0 | 0 | 0 | -0,25 | -0,10
1,60 | 0 | 0 | 0 | 0 | 0 | -0,25
