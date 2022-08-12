## Planificar la Gestión de los Recursos
**AC, PD, DP, FA, OPAs** // **JE, RepDat, TO, Reu** // **PGR, ACE, ADP**

```mermaid
flowchart TD;
	proceso[Planificar la Gestión de los Recursos]
	subgraph Entradas
		AC
		PD
		DP
		FA
		OPAs
	end
	subgraph HyT
		JE
		RepDat
		TO
		Reu
	end
	subgraph Salidas
		PGR
		ACE
		ADP
	end
	proceso --> Entradas
	Entradas --> HyT
	HyT --> Salidas
```

## Estimar los Recursos de las Actividades
**PD, DP, FA, OPAs** // **JE, EstAsc, EstAn, EstP, AD, SIDP, Reu** // **RR, BEst, EDR, ADP**

```mermaid
flowchart TD;
	proceso[Estimar los Recursos de las Actividades]
	subgraph Entradas
		PD
		DP
		FA
		OPAs
	end
	subgraph HyT
		JE
		EstAsc
		EstAn
		EstP
		AD
		SIDP
		Reu
	end
	subgraph Salidas
		RR
		BEst
		EDR
		ADP
	end
	proceso --> Entradas
	Entradas --> HyT
	HyT --> Salidas
```

## Adquirir Recursos
**PD, DP, FA, OPAs** // **TD, HIE, APrev, EqVirt** // **ARF, AEP, CalRec, SC, APD, ADP, AFA, AOPAs**

## Desarrollar el Equipo 
**PD, DP, FA, OPAs** // **CU, EqVirt, TecC, HIE, RyR, Cap, EIE, Reu** // **EDE, SC, APD, ADP, AFA, AOPAs**

## Dirigir al Equipo
**PD, DP, InfDT, EDE, FA, OPAs** // **HIE, SIDP** // **SC, APD, ADP, AFA**

## Controlar los Recursos
**PD, DP, DDT, A, OPAs** // **AD, RP, HIE, SIDP** // **IDT, SC, APD, ADP**

