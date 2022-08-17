# Series de Fourier
Tenemos ondas de tipo **senoidales** y **no senoidales** (cualquier forma que periódica que difiera de la función senoidal fundamental)

La serie de Fourier es una serie de términos que puede usarse para representar una forma de onda **periódica** no senoidal.

![[Pasted image 20220816163801.png]]

Según la forma de onda, podría requerirse una gran cantidad de estos términos para aproximar la forma de onda lo más fielmente posible para efectos del análisis del circuito.

## Componente fundamental
Es el primer término de la serie. Representa el término de frecuencia mínima requerido para representar una forma de onda particular. También tiene la misma frecuencia que la forma de onda que se está representando.

## Armónicos
Son los demás términos de la serie. Tienen frecuencia mayor al componente fundamental ya que son múltiplos enteros de la misma.
- **Armónicos impares**: Términos de la expansión de la serie de Fourier cuyas **frecuencias** son múltiplos impares del componente fundamental
- **Armónicos pares**: Términos de la expansión de la serie de Fourier cuyas **frecuencias** son múltiplos pares del componente fundamental

## Función Impar
$$ f(t) = -f(-t) $$

![[Pasted image 20220816164918.png]]

## Función Par
$$f(t)=f(-t)$$
![[Pasted image 20220816165127.png]]

## Simetría de espejo o de media onda
$$f(t)=-f(t+(T/2))$$
![[Pasted image 20220816165222.png]]

## Repetitiva en el medio ciclo
$$f(t)=f(t+(T/2))$$
![[Pasted image 20220816165303.png]]

# Instrumentos
![[Pasted image 20220816170058.png]]
## Osciloscopio
Muestra en pantalla una forma de onda de voltaje (eje vertical) versus el tiempo (eje horizontal). En este caso, se dice que la imagen está en el **dominio del tiempo**.

## Analizador de espectro
Genera una imagen a menor escala en dB (eje vertical) contra frecuencia (eje horizontal). La imagen está en el **dominio de la frecuencia**
![[Pasted image 20220816170118.png]]

