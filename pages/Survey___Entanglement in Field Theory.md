- Summary
	- Here a state is defined as a map from the operator algebra $\mathcal B$ (observables) to $\mathbb C$ (complex numbers).
		- A theorem states that we can find an element $a \in \mathcal B$ such that $F(O)=\operatorname{Tr}(aO)$.
	- Trace is defined by a trace structure.
	- Entropy is defined by $Tr(a \log a)$.
		- $\log$ is defined by a series.
- TODOs: Verify known things in lattice quantum information
	- Strong additivity
		- For three arbitrary disjoint regions A, B, C, and an arbitrary quantum state defined on $A \cup B \cup C$, we should have
		  $$S_{AB}+S_{BC}-S(B)-S(ABC) \geq 0$$
	- Triangle inequality (Araki-Lieb)
		- $$\left|S\left(\rho_A\right)-S\left(\rho_B\right)\right| \leq S\left(\rho_{A B}\right)$$
	- A new recovery map for four disjoint regions A, B, C, D
		- {{embed ((65ab687d-244f-4792-8b78-fabf3a6937a4))}}
		- See 1505.01917 for reference. Highly technical!
	- Afterwards, we can try to define anyons in field theories.
- Attempts
	- Definition. Partial trace
		- For a region $B \sub A$, the inclusion of operator algebras $M(B) \hookrightarrow M(A)$ naturally induces a map of space states $S(A) \to S(B)$ by mapping a state $\rho$ to
		  $$M(B) \overset{i}{\hookrightarrow} M(A) \overset{\rho}{\rightarrow} \mathbb C$$
		-