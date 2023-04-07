type:: paper_reading

-
- ![2023_Li_Sang_Hsieh_Entanglement Dynamics of Noisy Random Circuits.pdf](file://zotero_link/Physics/Quantum/Quantum Circuit Dynamics/2023_Li_Sang_Hsieh_Entanglement Dynamics of Noisy Random Circuits.pdf)
-
- Also a good source of refs.
- # Significance
	- Understand quantum thermalization
	- Understand quantum devices and quantum advantage, since real systems must live with noises
	-
- # Intro
	- Approach
		- Study a minimal model (1D qudit chain) acted on by random local unitaries and local depolarization channels.
		- Map the model to a stat-mech system
		- Evaluate mutual info, operator entanglement, entanglement negativity, etc.
	- Main results #card
	  card-last-interval:: 30
	  card-repeats:: 2
	  card-ease-factor:: 2.7
	  card-next-schedule:: 2023-05-07T11:23:56.312Z
	  card-last-reviewed:: 2023-04-07T11:23:56.313Z
	  card-last-score:: 5
		- The entanglement quantities first grow linearly, reach its peak, then drop to zero.
			- The peaks are reached at a system-size-independent time
		- Area-law peak for depolarization everywhere; volume-law peak for depolarization on the boundary
			- [[Bulk-Boundary Relation]]?
	- ## Setup
		- 1D qudit chain
		- Dynamics
			- ((63f0312f-73e7-40e1-b789-e4b5d4157107))
				- Representing each $\rho$ (and $|\rho\rangle$ ) as a single-layer circuit (here the convention is that a pure state and its "dual" together form a layer).
				- Blue blocks: Haar random unitaries chosen randomly
				- Yellow strips: Depolarizing channels, with p fixed
			- Analytically, $\Phi(\rho)=(1-p) U \rho U^{\dagger}+\frac{p \operatorname{tr}(\rho)}{d^2} \mathbb{I}_2$
			  collapsed:: true
				- First term: Not depolarized
				- Second term: Depolarized
					- $\rho$ is the density matrix on **two** qudits, so dimension is $d^2$.
						- Is it the reduce density matrix? #Learning-TODO
						- I think reduce density matrices don't contain all information. Maybe only action on the part of the system?
					- $tr(\rho)$ and $1/d^2$ serve as normalization factors.
					  background-color:: red
					- That is, $tr(\rho)$ could be other than 1?
					-
		- Quantities of interest
			- Average of Renyi-2 mutual information $$\overline{I_2}(t)=\mathbb{E}_U\left[I_2\left(\rho_t\right)\right]$$
			  id:: 63f0330d-dee8-4d29-8305-860fb390a544
				- The average is taken over the whole ensemble of trajectories.
				- $\begin{aligned} I_2(A:B) & =S_{2, A}+S_{2, B}-S_{2, A B} \\ & =-\log \operatorname{tr} \rho_A^2-\log \operatorname{tr} \rho_B^2+\log \operatorname{tr} \rho_{A B}^2\end{aligned}$
					- Note: $S_n(\rho)=\frac{ln(Tr(\rho^n))}{1-n}$, $I_{AB}=S_A+S_B-S_{AB}$
		-
- # ((63f039a9-eef5-443e-a327-686da202145a))
	- The goal is to calculate the mutual information
	- ## Summary of Techniques
	  collapsed:: true
		- Replica Trick: $\mathbb{E} \log X=\left.\frac{\partial}{\partial \alpha} \mathbb{E} X^\alpha\right|_{\alpha=0}=\left.\frac{\partial}{\partial \alpha} \log \mathbb{E} X^\alpha\right|_{\alpha=0}$ #card
		  card-last-interval:: 30
		  card-repeats:: 1
		  card-ease-factor:: 2.6
		  card-next-schedule:: 2023-05-05T11:16:31.750Z
		  card-last-reviewed:: 2023-04-05T11:16:31.751Z
		  card-last-score:: 5
			- Write $\mathbb E(X^\alpha)=\int dV X^\alpha \rho(X)=\int dV e^{\alpha \ln(X)}\rho(X)$, then everything follows.
		- Average the random unitary by “Weingarten calculus” transformation ((63f03c10-91cd-4750-a5a3-0e18c646964f))
			- This transforms each unit to a different form in which two effective "spin" degrees of freedom taking values in $S_Q$, the permutation group of $Q$ elements, are summed over. Here $Q$ is the number of layers evolved.
	- ## ((63f03c81-78ab-46a7-b40e-2bd58b0adba2))
		-