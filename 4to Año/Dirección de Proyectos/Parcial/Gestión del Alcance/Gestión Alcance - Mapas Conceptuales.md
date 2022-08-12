## Planificar la gestión del Alcance
**[[Conceptos#Acta de Constitución del Proyecto AC|AC]], PD, FA, OPAs** // **JE, AD, Reu** // **PGA, PGR**

```mermaid
flowchart TD;
	proceso[Planificar la Gestión del Alcance]
	subgraph Entradas
		AC
		PD
		FA
		OPAs
	end
	subgraph HyT
		JE
		AD
		Reu
	end
	subgraph Salidas
		PGA
		PGR
	end

	proceso --> Entradas
	Entradas --> HyT
	HyT --> Salidas
```

## Recopilar Requisitos 
**AC, PD, DP, DN, A, FA, OPAs** // **JE, RD, TD, RepDatos, HIE, DC, Prot** // **DR, MTR**

```mermaid
flowchart TD;
	proceso[Recopilar Requisitos]
	subgraph Entradas
		AC
		PD
		DP
		DN
		A
		FA
		OPAs
	end
	subgraph HyT
		JE
		RD
		TD
		RepDatos
		HIE
		DC
		Prot
	end
	subgraph Salidas
		DR
		MTR
	end
	proceso --> Entradas
	Entradas --> HyT
	HyT --> Salidas
```

## Definir el Alcance
**AC, PD, DP, FA, OPAs** // **JE, AD, TD, HIE, AP** // **EAP, ADP**

```mermaid
flowchart TD;
	proceso[Definir el Alcance]
	subgraph Entradas
		AC
		PD
		DP
		FA
		OPAs
	end
	subgraph HyT
		JE
		AD
		TD
		HIE
		AP
	end
	subgraph Salidas
		EAP
		ADP
	end
	proceso --> Entradas
	Entradas --> HyT
	HyT --> Salidas
```

## Crear el EDT
**PD, DP, FA, OPAs** // **JE, Desc** // **LBA, ADP**

```mermaid
flowchart TD;
	proceso[Crear el EDT]
	subgraph Entradas
		PD
		DP
		FA
		OPAs
	end
	subgraph HyT
		JE
		Desc
	end
	subgraph Salidas
		LBA
		ADP
	end
	proceso --> Entradas
	Entradas --> HyT
	HyT --> Salidas
```

## Validar el Alcance
**PD, DP, EV, DDT** // **Ins, TD** // **EA, IDT, SC, ADP**

```mermaid
flowchart TD;
	proceso[Validar el Alcance]
	subgraph Entradas
		PD
		DP
		EV
		DDT
	end
	subgraph HyT
		Ins
		TD
	end
	subgraph Salidas
		EA
		IDT
		SC
		ADP
	end
	proceso --> Entradas
	Entradas --> HyT
	HyT --> Salidas
```

## Controlar el Alcance
**PD, DP, DDT, OPAs** // **AD** // **IDT, SC, APD, ADP**

```mermaid
flowchart TD;
	proceso[Controlar el Alcance]
	subgraph Entradas
		PD
		DP
		DDT
		OPAs
	end
	subgraph HyT
		AD
	end
	subgraph Salidas
		IDT
		SC
		APD
		ADP
	end
	proceso --> Entradas
	Entradas --> HyT
	HyT --> Salidas
```
