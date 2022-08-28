# Proceso de Resolución de Problemas
Es un nivel de abstracción suficientemente alto, la mente humano resuelve todos los problemas con el mismmo **proceso de resolución**.
![[Pasted image 20220529023850.png]]

# Proceso de Construcción de Software
Es la transformación de una necesidad (problema) en un software (solución automatizada) que satisface esa necesidad.
![[Pasted image 20220529024040.png]]

**Modelo Conceptual**: Validez, Modelos declarativos
**Modelo Formal**: Corrección, Modelos procedimentales computables

**Existen muchas respuestas potenciales a una necesidad**. El modelo conceputal limita la elección a una. Cada clase de modelo conceptuual define muchos modelos formales y muchas posibles programaciones para cada modelo formal.

Hay que trabajar en dos dominios, con dos tipos de modelo y gestionando elecciones que, necesariamente, **están basadas en el juicio y la experiencia**.

# Proceso Software
## Frente a Ciclo de Vida
El proceso mínimo necesario para resolver el problema de la **construcción de software** es:
![[Pasted image 20220529024407.png]]

## Frente a Ciclo de Vida del Producto
![[Pasted image 20220529024527.png]]

# Desarrollo del Software vs Software
![[Pasted image 20220529024631.png]]

# Tipos de Ciclo de Vida Iniciales
## Ciclo de Vida Clásico
La evolución del producto software procede a través de una secuencia ordenada de transiciones de una fase a la otra según un orden lineal.
![[Pasted image 20220529024914.png]]

## Ciclo de Vida Clásico Alternativo
![[Pasted image 20220529024932.png]]

## Ciclo de Vida Prototipo
![[Pasted image 20220529025005.png]]

## Ciclo de Vida Prototipo Alternativo
![[Pasted image 20220529025045.png]]

## Ciclo de Vida Espiral
![[Pasted image 20220529025137.png]]

## Ciclo de Vida Paralelo
La estregia de desarrollar un sistema complejo dividiendo el trabajo por Subsistemas (Si), permite organizar las tareas de cada rol, de manera que se optimice la afectación del recurso humano.
![[Pasted image 20220529025307.png]]

## Ciclo de Vida Incremental
Antes de iniciar la construcción, se define en base a un bosquejo (esquema inicial), los servicios o funcionalidades que debe prestar el software, y, con participación del usuario, se divide el sistema en entregas parciales, o **incrementos**, priorizados según sus necesidades.
![[Pasted image 20220529025334.png]]

# Tipos de Ciclos de Vida Actuales
## Análisis Estructurado Moderno (1993)
Es un método de análisis de requerimientos basado en la creación de **modelos** que reflejan el flujo y el contenido de la información (datos y control); partimos del sistema funcionalmente y, según distintos comportamientos, **establecemos la esencia de lo que se debe construir.**
![[Pasted image 20220529232311.png]]

## Proceso Unificado de Desarrollo de Software (1999)
![[Pasted image 20220529232346.png]]

![[Pasted image 20220529232439.png]]

## Desarrollo de Software Basado en Componentes (2000+)
### Componente
Un **Componente** es una pieza de funcionalidad entregable de manera independiente, que provee acceso a sus servicios a través de interfaces.
#### Propiedades
- Unidad de utilización independiente
- Unidad de composición de terceras partes
- No tiene estado permanente

### Definición
**Es una unidad entregable**. Tiene las características de un paquete ejecutable de software. Provee **una funcionalidad útil** que ha sido reunida conjuntamente para satisfacer alguna necesidad. **Ofrece servicios a través de interfaces**, por lo que para usarlos se deben requerir los servicios a través de las interfaces.
![[Pasted image 20220529233128.png]]

### Contrato Público
Contiene una definición de estándares para implementación, documentación y aspectos de despliegue del componente. Permite asegurar al desarrollador, que el componente a incorporar le resultará de utilidad.

Involucra definiciones relacionadas con:
- Interfaces
- Uso
- Implementación

### Contrato Privado
Permite al desarrollador acceder al código fuene del componente.

### Proceso CBSE
![[Pasted image 20220529233444.png]]

## Desarrollo de Software Distribuido (2007+)
La mayoría de los grandes sistemas software de la actualidad, implican numerosas computadoras.

### Sistemas Distribuidos
> [!quote] Tanenbaum y Van Steet
> Una colección de computadoras independiente que aparecen al usuario como un solo sistema coherente.

Los conflictos surgen porque los componentes del sistema pueden estar en ejecución en simultáneo en distintas computadoras con administración independiente y éstas se comunican a través de una red.
#### Ventajas
- Recursos Compartidos
- Apertura
- Concurrencia
- Escalabilidad
- Tolerancia a fallas

#### Consideraciones de diseño
El rendimiento ya no sólo depende de la velocidad de ejecución en un procesador, sino también del ancho de banda de la red; la carga de la red y la velocidad de todos los activos que conforman el sistema.
En la WWW, por ejemplo, no se puede predecir el tiempo de respuesta.

#### Conflictos de diseño
- Transparencia
- Apertura
- Seguridad
	- Intercepción (confidencialidad)
	- Interrupción
	- Modificación
	- Fabricación
- Escalabilidad
	- Tamaño: expandir (scaling up), ampliar (scaling out)
	- Distribuión
	- Manejabilidad
- Calidad de servicio
- Gestión de fallas