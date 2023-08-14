# Significance
	- [[Entanglement]] is deeply related with [[Thermalization]].
		- Intuition: Local thermalization -> Long-range entanglement
	- Quantum info provide proxies for certain kinds of classical hardness, thus helping to understand ((63e86248-136d-4d42-9012-f111fcc231cc))
-
-
- # Thoughts
	- 'If you work too hard you get nothing'. Equal-weight superposition of all configurations doesn't work, but partial sum does.
	- Low-entanglement states can be approximated by states with a small Schmidt number (nonzero eigenvalues of reduced density matrices)
- # Quantifications
	- [[von-Neumann Entropy]]
	- [[Renyi Entropy]]
	- [[Mutual Information]]
	- Refs given in [[2023_Li_Sang_Hsieh_Entanglement Dynamics of Noisy Random Circuits]]
		- [[Entanglement Negativity]] #[[Research/To Be Investigated]]
		- [[Operator Entanglement Entropy]] #[[Research/To Be Investigated]]
	- Entanglement Negativity
		- Def
			- Given a state $\rho_{A \cup B}$ defined on $A \cup B$, the logarithmic entanglement negativity (or simply EN) of subsystem $A$ is defined as
			  $$
			  N_A\left(\rho_{A \cup B}\right)=\ln \left\|\rho_{A \cup B}^{\Gamma_A}\right\|_1=\ln \sum_i\left|\lambda_i\right| .
			  $$
			  where $\Gamma_A$ is the partial transpose operation of $\rho$ with respect to $A$, and $\lambda$ are the eigenvalues of $\rho^{\Gamma_A}$.
			-
			- Mutual negativity:
			  $$N_{A, B}:=N_A\left(\rho_{A \cup B}\right)=N_B\left(\rho_{A \cup B}\right)$$
			-
		- In general it's hard to compute, but simpler for stabilizer states
			- $$
			  \rho_{A \cup B}=\frac{1}{2^{|A \cup B|}} \sum_{g \in \mathcal{S}} g .
			  $$
				- S is the stabilizer group on $A \cup B$.
			- $$
			  N_A\left(\rho_{A \cup B}\right)=\frac{1}{2} \ln \left|\frac{\operatorname{proj}_A(\mathcal{S})}{Z\left(\operatorname{proj}_A(\mathcal{S})\right)}\right|
			  $$
			- Here $\operatorname{proj}_A(\mathcal{S})$ is the group obtained from $\mathcal{S}$ by "restricting" Pauli strings in $\mathcal{S}$ on $A$, and is in general non-abelian; $Z\left(\operatorname{proj}_A(\mathcal{S})\right)$ is the center of $\operatorname{proj}_A(\mathcal{S})$.
			-
	-
	-
-