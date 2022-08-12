## Planificar la Gestión de los Costos
**AC, PD, FA, OPAs** // **JE, AD, Reu**
// **PGC**

```mermaid
flowchart TD;
	proceso[Planificar la Gestión de los Costos]
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

## Estimar los Costos
**PD, DP, FA, OPAs** // **JE, EstAn, EstP, EstAsc, Est3V, AD, SIDP, TD** // **EstCost, BEst, ADP**

```mermaid
flowchart TD;
	proceso[Estimar los Costos]
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
		EstAsc
		Est3V
		Ad
		SIDP
		TD
	end
	subgraph Salidas
		EstCost
		BEst
		ADP
	end
	proceso --> Entradas
	Entradas --> HyT
	HyT --> Salidas
```

## Determinar el Presupuesto
**PD, DP, DN, A, FA, OPAs** // **JE, CA, AD, RIH, CLF, Fi** // **LBCost, RFP, ADP**

```mermaid
flowchart TD;
	proceso[Determinar el Presupuesto]
	subgraph Entradas
		PD
		DP
		DN
		A
		FA
		OPAs
	end
	subgraph HyT
		JE
		CA
		AD
		RIH
		CLF
		Fi
	end
	subgraph Salidas
		LBCost
		RFP
		ADP
	end
	proceso --> Entradas
	Entradas --> HyT
	HyT --> Salidas
```

## Controlar los Costos
**PD, DP, RFP, DDT, OPAs** // **JE, AD, IDTC, SIDP** // **IDT, PCost, SC, APD, ADP**

```mermaid
flowchart TD;
	proceso[Controlar los Costos]
	subgraph Entradas
		PD
		DP
		RFP
		DDT
		OPAs
	end
	subgraph HyT
		JE
		AD
		IDTC
		SIDP
	end
	subgraph Salidas
		IDT
		PCost
		SC
		APD
		ADP
	end
	proceso --> Entradas
	Entradas --> HyT
	HyT --> Salidas
```
