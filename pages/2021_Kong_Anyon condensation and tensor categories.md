- ![2021_Kong_Anyon condensation and tensor categories.pdf](file://zotero_link/Research/Quantum Matters/Topological order/Anyon Condensation/2021_Kong_Anyon condensation and tensor categories.pdf)
- # Basic Idea
	- Most concrete examples are too simple and contain too many accidental structures.
	- Therefore we take a [[Bootstrap]] approach and introduce as few assumptions as possible.
- # ((6531dac7-62c6-45fc-b29a-1be214fc5d57)) #card
	- Anyons in $\mathcal D$ should originate from anyons in $\mathcal C$. Moreover, the vacuum $\mathbf 1_{\mathcal D}$ is a simple object $A$ in $\mathcal C$.
	  collapsed:: true
		- Note that simple anyons in $\mathcal C$ may become composite anyons in $\mathcal D$ after the condensation, i.e. they may split.
		  background-color:: yellow
	- The vacuum of $\mathcal C$ should condense into vacuum of $\mathcal D$. This means that there exists a morphism $\iota_A: \mathbf{1} \rightarrow A$ in $\mathcal{C}$.
	- All fusion-splitting channels in $\mathcal D$ should originate from those in $\mathcal C$. Therefore, we must have an embedding:
	  collapsed:: true
	  $$
	  \operatorname{hom}_{\mathcal{D}}(M, N) \hookrightarrow \operatorname{hom}_{\mathcal{C}}(M, N), \quad \forall M, N \in \mathcal{D} .
	  $$
		- In other words, $\mathcal{D}$ can be viewed as a (not full) subcategory of $\mathcal{C}$.
	- Moreover, we expect that there is an onto map, called **condensation map** in $\mathrm{C}$ :
	  $$
	  \rho_{M, N}: M \otimes N \rightarrow M \otimes_{\mathcal{D}} N
	  $$
	  and a canonical morphism
	  $$
	  e_{M, N}: M \otimes_{\mathcal{D}} N \rightarrow M \otimes N
	  $$
	  such that $\rho_{M, N} \circ e_{M, N}=\operatorname{id}_{M \otimes_{\mathcal{D}} N}$.
		- Since $\mathbf{1}_{\mathcal{D}}=A$, we must have $A \otimes_{\mathcal{D}} A=A$ and $A \otimes_{\mathcal{D}} M=M=M \otimes_{\mathcal{D}} A$.
		- We denote the map $\rho_{A, A}: A \otimes A \rightarrow A=A \otimes_{\mathcal{D}} A$ by $\mu_A$ and $e_{A, A}$ by $e_A$.
		-
	- ## Properties of the condensable algebra $A$
		- **Associativity**. The condensation process should be associative, i.e. if we condense three anyons, it should not matter which two we condense first, i.e.
		  ((6531dfc9-7dbf-40f4-ab4b-cde607162dde))
		- **Unit Property**. We should feel free to add vacuums:
		  ((6531e017-5a53-493d-95d9-1af66ff5f2de))
		- **Commutativity**. The condensation should not be affected by braidings:
		  ((6531e065-0efd-4248-a545-fc52edbd9701))
		- **Stability of the vacuum**. The vacuum should not be broken by 'fuse with another copy of vacuum', i.e. the following two maps must be **zero**:
		  ((6531e0c2-2077-4589-81b7-86e2972f7c81))
		- **Connectedness**. 
		  ((6531e133-0455-4b1e-8235-afa333e109fc))
			- Why it is called connectedness?
			  background-color:: red