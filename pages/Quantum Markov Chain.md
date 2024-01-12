alias:: Quantum Markov State

- Definition #card
	- A tripartite state with fixed subsystems $A,B,C$, such that the ((658b78c9-df4c-47bf-b17f-c4c459d25fa6)) is zero,
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