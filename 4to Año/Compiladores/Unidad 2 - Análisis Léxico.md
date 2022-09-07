El **analizador léxico** realiza la primera fase del compilador. Su principal función consiste en leer los caracteres de entrada (el código fuente) y elaborar como salida una secuencia de unidades sintácticas con sentido lógico, a las cuales se les llama _componentes_ _léxicos_ o _tokens_, que utiliza el analizador sintáctico para hacer el análisis.

Básicamente hay dos formas de construir un analizador léxico:
- Implementarlo como un módulo dentro de un programa, escribiendo los pasos para reconocer cada token. 
- Usar una herramienta que genere el código del analizador léxico a partir de especificar los patrones de los componentes léxicos.

# Fases de un compilador
![[Pasted image 20220904180444.png]]

# Analizador Léxico
## Tareas
• Leer el programa (de izquierda a derecha), tomar secuencias de caracteres, y convertirlas/ubicarlas en una categoría conocida como componentes léxicos o tokens
• Eliminar espacios en blanco y comentarios
• Informar errores léxicos, indicar número de línea de los errores encontrados

## Token
secuencia de caracteres con significado colectivo
representan a los nombres de las variables, operadores, etiquetas, y todo lo que comprende el programa fuente.

# Análisis Léxico
![[Pasted image 20220904180717.png]]
![[Pasted image 20220904180730.png]]

## Definiciones
- Token o componente léxico: una entidad lógica
	- “id” (identificador “posicion”)
- Lexema: secuencia de caracteres que forman el token
	- “posicion” (string de 8 caracteres)
- Atributo(s): otra información adicional sobre el token que sea útil para el análisis sintáctico y semántico
	- Esta información se va guardando en la tabla de símbolos
	- (id, “posicion”, …)

Los tokens se tratan como símbolos terminales de la gramática del lenguaje fuente.

![[Pasted image 20220904181030.png]]

## Tokens
![[Pasted image 20220904181213.png]]
![[Pasted image 20220904181336.png]]
![[Pasted image 20220904181444.png]]

• Algunos tokens no son empleados por el analizador sintáctico, por lo
tanto, son descartados por el analizador léxico:
• comentarios, que documentan el programa pero que no tienen un uso gramatical
	• espacios en blanco, que sirven para dar legibilidad a lo escrito
	• separadores (TAB, Salto de linea)

## Preanálisis
![[Pasted image 20220904181547.png]]

# Construcción de Analizador Léxico
## Ejemplo
![[Pasted image 20220904181721.png]]
![[Pasted image 20220904181737.png]]

## Vista General
![[Pasted image 20220904181916.png]]

## Generador de analizadores léxicos
![[Pasted image 20220904181937.png]]
