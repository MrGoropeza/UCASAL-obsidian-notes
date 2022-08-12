# Planificar la Gestión del Cronograma
**AC, PD, FA, OPAs** // **JE, AD, Reu** // **PGC**

```mermaid
flowchart TD;
	proceso[Planificar la Gestión del Cronograma]
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
		PGC
	end
	proceso --> Entradas
	Entradas --> HyT 
	HyT --> Salidas
```

# Definir las Actividades
**PD, FA, OPAs** // **JE, Desc, PG, Reu** // **LA, AdA, LH, SC, APD**

```mermaid
flowchart TD;
	proceso[Definir las Actividades]
	subgraph Entradas
		PD
		FA
		OPAs
	end
	subgraph HyT
		JE
		Desc
		PG
		Reu
	end
	subgraph Salidas
		LA
		AdA
		LH
		SC
		APD
	end
	proceso --> Entradas
	Entradas --> HyT
	HyT --> Salidas
```

# Secuenciar las Actividades
**PD, DP, FA, OPAs** // **MDP, DID, AyR, SIDP** // **DRC, ADP**

```mermaid
flowchart TD;
	proceso[Secuenciar las Actividades]
	subgraph Entradas
		PD
		DP
		FA
		OPAs
	end
	subgraph HyT
		MDP
		DID
		AyR
		SIDP
	end
	subgraph Salidas
		DRC
		ADP
	end
	proceso --> Entradas
	Entradas --> HyT
	HyT --> Salidas
```

# Estimar la Duración de las Actividades
**PD, DP, FA, OPAs** // **JE, EstAn, EstP, Est3V, EstAsc, AD, TD, Reu** // **EstDur, BEst, ADP**

```mermaid
flowchart TD;
	proceso[Estimar la Duración de las Actividades]
	subgraph Entradas
		PD
		DP
		FA
		OPAs
	end
	subgraph HyT
		JE
		EstAn
		EstP
		Est3V
		EstAsc
		AD
		TD
		Reu
	end
	subgraph Salidas
		EstDur
		BEst
		ADP
	end
	proceso --> Entradas
	Entradas --> HyT
	HyT --> Salidas
```
# Desarrollar el Cronograma
**PD, DP, A, FA, OPAs** // **ARC, MRC, OR, AD, AyR, CC, SIDP, PAL** // **LBC, CP, DatCron, CalProy, SC, APD, ADP**

```mermaid
flowchart TD;
	proceso[Desarrollar el Cronograma]
	subgraph Entradas
		PD
		DP
		A
		FA
		OPAs
	end
	subgraph HyT
		ARC
		MRC
		OR
		AD
		AyR
		CC
		SIDP
		PAL
	end
	subgraph Salidas
		LBC
		CP
		DatCron
		CalProy
		SC
		APD
		ADP
	end
	proceso --> Entradas
	Entradas --> HyT
	HyT --> Salidas
```
# Controlar el Cronograma
**PD, DP, DDT, OPAs** // **AD, MRC, SIDP, OR, AyR, CC** // **IDT, PC, SC, APD, ADP**

```mermaid
flowchart TD;
	proceso[Controlar el Cronograma]
	subgraph Entradas
		PD
		DP
		DDT
		OPAs
	end
	subgraph HyT
		AD
		MRC
		SIDP
		OR
		AyR
		CC
	end
	subgraph Salidas
		IDT
		PC
		SC
		APD
		ADP
	end
	proceso --> Entradas
	Entradas --> HyT
	HyT --> Salidas	
```
