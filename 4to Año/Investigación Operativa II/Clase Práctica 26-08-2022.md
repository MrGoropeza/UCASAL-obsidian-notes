TP1:
- Estrategia Dominantes
- Estrategia Minimax/Maximin
- Estrategias Mixtas

# Ejemplo 

x | 1 | 2 | 3 | 4
-- | -- | -- | -- | --
1 | 2 | -3 | -1 | 1
3 | -1 | 1 | -2 | 2
3 | -1 | 2 | -1 | 3


Punto silla: punto de equilibrio, ninguno de los dos jugadores va a elegir otra estrategia llegado al punto silla, ya que va a perder
Minimax: minimizar la pérdida máxima
Maximin: maximizar la ganacia miníma

## Relizacion de minimax
estrategias | 1 | 2 | 3 | 4 | minimos filas
-- | -- | -- | -- | -- | --
1 | 2 | -3 | -1 | 1 | -3
2 | -1 | 1 | -2 | 2 | -2
3 | -1 | 2 | -1 | 3 | -1
maximos columnas | 2 | 2 | -1 | 3

Jugador 1: Maximo de los menores (minimax): -1 (estrategia 3)

Jugador 2: Mínimos de los mayores (maximin): -1 (estrategia 3)


Resultado del juego en el punto silla: El jugador 2 gana 1 unidad.
- Valor del juego: -1
- Resultado del juego: gana jugador 2
- Punto silla: estrategia(3, 3) mu_{s} = (3, 3)

Si minimax != maximin, entonces estamos en un juego inestable.


Teoria de la dualidad: para un modelo de programacion lineal de ciertas caracteristicas, existe un modelo igual pero distinto