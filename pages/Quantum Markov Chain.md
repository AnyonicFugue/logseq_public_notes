alias:: Quantum Markov State

- Definition #card
  card-last-interval:: 32.57
  card-repeats:: 1
  card-ease-factor:: 2.6
  card-next-schedule:: 2024-04-23T14:15:22.056Z
  card-last-reviewed:: 2024-03-22T01:15:22.056Z
  card-last-score:: 5
	- A tripartite state with fixed subsystems $A,B,C$, such that the [[Conditional Mutual Information]] is zero,
	  $$I(A:C|B)=0$$
- Physical meaning
- # Properties
	- Petz Recovery #card
	  id:: 659f5206-6b2d-4b8a-a381-8d16e20644f7
		- Put plainly, if $I(A: C \mid B)_\rho=0$, then $\rho_{AB}$ and $\rho_{BC}$ fix $\rho_{ABC}$.
		- Comments
			- Of course we have tripartite states with $I(A:C|B) \neq 0$. Could $\rho_{ABC}$ be recovered from parts? Under what condition?
			  background-color:: red
			- [[2020_Shi_Kato_Kim_Fusion rules from entanglement]] used the property extensively to prove merging. Can we find more elegant structures?
		-
		- Lemma. Let $\rho_{A B C}$ and $\sigma_{A B C}$ be density matrices such that (1) $\rho_{A B}=\sigma_{A B}$ and $\rho_{B C}=\sigma_{B C}$;
		  (2) $I(A: C \mid B)_\rho=I(A: C \mid B)_\sigma=0$. Then $\rho_{A B C}=\sigma_{A B C}$.
		- Lemma. (Petz recovery map) For any tripartite state $\rho_{A B C}, I(A: C \mid B)_\rho=0$ if and only if
		  $$
		  \rho_{A B C}=\mathcal{E}_{B \rightarrow B C}^\rho\left(\rho_{A B}\right),
		  $$
		  where $\mathcal{E}_{B \rightarrow B C}^\rho$ (the Petz recovery map) is defined as
		  $$
		  \mathcal{E}_{B \rightarrow B C}^\rho\left(X_B\right)=\rho_{B C}^{\frac{1}{2}} \rho_B^{-\frac{1}{2}} X_B \rho_B^{-\frac{1}{2}} \rho_{B C}^{\frac{1}{2}}
		  $$
			- The map recovers $\rho_{ABC}$ from its reduced density matrices.
			-
	- Semi-Separability
	  id:: 65bdae23-c5a5-47c2-a2ab-552bbabb08cf
		- There is a decomposition of the Hilbert space $\mathcal{H}_B$ into a direct sum of tensor products $\mathcal{H}_B=\bigoplus_j \mathcal{H}_{b_j^L} \otimes \mathcal{H}_{b_j^R}$ such that
		  $$
		  \rho_{A B C}=\bigoplus_j p_j \rho_{A b_j^L} \otimes \rho_{b_j^R C},
		  $$
			- $\left\{p_j\right\}$ is a probability distribution
			- $\rho_{A b_j^L}$ is a density matrix on $\mathcal{H}_A \otimes \mathcal{H}_{b_j^L}$ and $\rho_{A b_j^R}$ is a density matrix on $\mathcal{H}_{b_i^R} \otimes \mathcal{H}_C$
		- Note that this implies $\operatorname{Tr}_B \rho_{A B C}=\sum_j p_j \rho_A^j \otimes \rho_C^j$ is separable.