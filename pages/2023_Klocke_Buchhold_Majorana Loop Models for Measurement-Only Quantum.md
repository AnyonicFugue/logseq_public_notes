type:: paper_reading

-
- ![2023_Klocke_Buchhold_Majorana Loop Models for Measurement-Only Quantum.pdf](file://zotero_link/Research/2023 Summer Intern/2023_Klocke_Buchhold_Majorana Loop Models for Measurement-Only Quantum.pdf)
- # TODOs
	- DONE How to compute quantum-information quantities (entanglement entropy, mutual information) from majorana configurations?
		- DONE Entanglement entropy
		- DONE Mutual information
	- What are the main ideas and results of the paper?
	-
	- ((64d29fee-c6a3-466f-acbb-853a3872528c))
- # Setup
	- We consider an 1D chain of spin-1/2, evolving under Pauli measurements.
	- By JW transformation we represent the Pauli operators by majorana operators.
	- ## Gaussian Measurements
		- Def. Measurements which could be written as $\hat{O}=i \gamma_l \gamma_m$
		- $$
		  \mathcal{P}_{l m} \equiv \frac{1}{2}(\mathbb{1}+\hat{O})=\frac{1}{2}\left(\mathbb{1}+i \gamma_l \gamma_m\right)
		  $$
			- i.e. measurement outcome $+1$. For $-1$ we just replace + by -.
			- Physical meaning?
				- Note that for $i c_{2k-1}c_{2k}= 2 a_k^\dagger a_k - 1=2 \sigma^z_k-1$, thus the measurement denotes the occupation number (i.e. the Z-spin).
		- $$\mathcal{R}_{l m} \equiv \exp \left(i \frac{\pi}{4} O\right)=\frac{1}{\sqrt{2}}\left(\mathbb{1}-\gamma_l \gamma_m\right)$$
			- It swaps (braids) Majoranas $\gamma_l \leftrightarrow \gamma_m$, which can be verified by
			  $$\mathcal{R}_{l m}^{-1} \gamma_l \mathcal{R}_{l m}=-\gamma_m \\
			   \mathcal{R}_{l m}^{-1} \gamma_m \mathcal{R}_{l m}=\gamma_l$$
			- The motivation is that we want to reduce the general setting to adjacent majoranas.
	- ## The Diagram Representation
		- Each non-zero parity corresponds to a loop arc connecting sites $l,m$ with the length of the arc defined as $\mathcal l=|l-m|$.
- # Basic Facts
  collapsed:: true
	- \begin{aligned}
	  0 & =\left[\mathcal{P}_{l m}, \mathcal{P}_{n s}\right]=\left[\mathcal{R}_{l m}, \mathcal{R}_{n s}\right], \\
	  \mathcal{P}_{l m} & =\mathcal{P}_{l m}^2=\mathcal{P}_{l m} \mathcal{P}_{n l} \mathcal{P}_{l m}, \\
	  \mathcal{P}_{l m} & =\mathcal{R}_{m s}^{\dagger} \mathcal{P}_{l s} \mathcal{R}_{m s}, \mathcal{R}_{l m}=\mathcal{R}_{m s}^{\dagger} \mathcal{R}_{l s} \mathcal{R}_{m s} \\
	  \mathcal{R}_{l m}^4 & =\mathbb{1}
	  \end{aligned}
		- ((64d14b46-9ea8-4276-9f71-bdaec6ae69d8))
		- (1): Measurements and braidings at disjoint sites commute.
		- (2): The first equality says its a projective measurement.
		  The second isn't an operator equality, but only holds up to normalization. It says something like the Yang-Baxter equation.
		- (3): The first equation serves as a 'basis transformation'.
		  The second equation is precisely Yang-Baxter.
		- (4): Phases of Ising anyons are unity roots of order 4.
	- Corollary. By virtue of Eq. (3), any non-local swap $\mathcal{R}_{l m}$ or measurement $\mathcal{P}_{l m}$ with $|l-m|>1$ can be expressed via a sequence of **nearest-neighbor** swaps, e.g., $\mathcal{P}_{1,3}=\mathcal{R}_{2,3}^{\dagger} \mathcal{P}_{1,2} \mathcal{R}_{2,3}$.
	- ((64d298c9-91cf-4aee-9c50-ab160ca34abf))
	  id:: 64d298b1-9de3-4093-9a10-7f5aa3b43471
		- Side evidence: It is a **projective** representation of the braid group, in the sense that braiding by $R$ must incur a minus for one of the majorana operators.
		- ((64d298cf-2bb8-4434-a692-c647b0f65a84))
		- ((64d29931-0650-4bed-af1c-f78d3003f248))
- # Examples
  collapsed:: true
	- 2 qubits
		- JW Transformation
			- Definition:
			  $$
			  \begin{aligned}
			  & a_j^{\dagger}=e^{\left(i \pi \sum_{k=1}^{j-1} f_k^{\dagger} f_k\right)} \cdot f_j^{\dagger} \\
			  & a_j=e^{\left(i \pi \sum_{k=1}^{j-1} f_k^{\dagger} f_k\right)} \cdot f_j
			  \end{aligned}
			  $$
			-
			- $$
			  \begin{aligned}
			  & a_1^{\dagger}=f_1^{\dagger}= \left(\sigma_1^x+i \sigma_1^y\right) / 2\\
			  & a_1=f_1=\left(\sigma_1^x-i \sigma_1^y\right) / 2
			  \end{aligned}
			  $$
			- $$
			  \begin{aligned}
			  & a_2^{\dagger}=\sigma^z_1 f_2^{\dagger}= \sigma^z_1 \left(\sigma_2^x+i \sigma_2^y\right) / 2\\
			  & a_2=\sigma^z_1 f_2= \sigma^z_1 \left(\sigma_2^x-i \sigma_2^y\right) / 2
			  \end{aligned}
			  $$
		- Majorana representation
			- $$
			  c_{1}=a_1+a_1^{\dagger}, \ c_{2}=\frac{a_1-a_1^{\dagger}}{i}, \quad c_{3}=a_2+a_2^{\dagger}, \ c_{4}=\frac{a_2-a_2^{\dagger}}{i}
			  $$
			-
			- $$
			  c_{1}=a_1+a_1^{\dagger}=\sigma_1^x, \ c_{2}=\frac{a_1-a_1^{\dagger}}{i}=\sigma_1^y
			  $$
			- $$
			  c_{3}=a_2+a_2^{\dagger}=\sigma_1^z \sigma_2^x, \ c_{4}=\frac{a_1-a_1^{\dagger}}{i}=\sigma_1^z \sigma_2^y
			  $$
			- The strategy is very clear: apply strings of $\sigma^z$ in the front to ensure anti-commutativity.
		- Measurement
			- $$
			  \mathcal{P}_{l m} \equiv \frac{1}{2}(\mathbb{1}+\hat{O})=\frac{1}{2}\left(\mathbb{1}+i \gamma_l \gamma_m\right)
			  $$
			-
			- $$
			  \mathcal{P}_{12} =\frac{1}{2}\left(\mathbb{1}+i \gamma_1 \gamma_2\right)=\frac 1 2 (1+\sigma_1^z)
			  $$
		- Braiding operator
			- $$\mathcal{R}_{l m} \equiv \exp \left(i \frac{\pi}{4} O\right)=\frac{1}{\sqrt{2}}\left(\mathbb{1}-\gamma_l \gamma_m\right)$$
			-
			- $$\mathcal{R}_{12}=\frac{1}{\sqrt{2}}\left(\mathbb{1}-\gamma_1 \gamma_2\right)=\frac{1}{\sqrt{2}}\left(\mathbb{1}-i \sigma_1^z\right)$$
				- It is indeed unitary.
- # II Map to Loop Models
  collapsed:: true
	- # ((64d29a3e-69e7-4309-8072-529f13a59245))
	  collapsed:: true
		- We are interested in bulk and boundary observables of the circuit.
			- Boundary observable: Physical quantities in the final state $\rho(T)$, e.g. entanglement entropy, correlation
		- Claim. ((64d29abd-5144-4737-9303-12195a226010))
		- ## Loop Length
		- ## ((64d29b1e-ec3a-4bb6-b57f-c92c2cc4830d))
			- Claim. In a Gaussian circuit, both $S_A$ and $I_2(A, B)$ are determined by the set of fermion parities $\left|\left\langle\gamma_l \gamma_m\right\rangle_T\right|=1$, i.e., by the loop arcs at $t=T$.
				- Then $S_A=N_A$ is the number of arcs crossing the regions (by viewing them as stabilizers).
				- The mutual information $I_2(A, B)$ is twice the number of loops with one endpoint in $A$ and the other endpoint in $B$.
					- For Gaussian circuits and loop models, mutual information is **additive**, i.e., $I_2(A, B C)=I_2(A, B)+I_2(A, C)-I_2(A, B \cap C)$.
		- ## ((64d29ef6-d145-4682-9c94-3c20472c196b))
		- ## ((64d29f63-6253-411e-ba7d-d8c22e0fc9cc))
			- Def. Spanning number $n_s(T)$
				- The number of worldlines connecting the t = 0 and t = T temporal boundaries of the circuit.
				- Intuitively, this corresponds to those majoranas never measured in the process.
			- Proposition. It is the mutual information between the initial and the final state, thus quantifies the survival of information during the evolution.
				- Firstly, when the initial state is maximally mixed, it hosts only unpaired Majorana worldlines and the spanning number counts all unpaired Majorana world lines at time T .
				  id:: 64d29fee-c6a3-466f-acbb-853a3872528c
	- # ((64d5401c-0014-4785-8faa-f90981cbd6a3))
	  collapsed:: true
		- Motivation
			- A counterpart of time-reversal symmetry.
				- Physically, $\gamma_j$ with j odd are 'real part' of fermions while those with j even are 'imaginary part' of fermions.
			- Properties of dense loop models depend significantly on orientability.
				- When the local orientations are conserved, the order parameter takes values in $\mathbb{C P}^{n-1}$. If instead orientability is broken, as in CPLC, the order parameter is reduced to $\mathbb{R P}^{n-1}$.
				- Once orientability is broken sufficiently strongly, the corresponding NL $\sigma \mathrm{M}$ features a phase transition from a short-loop phase to a symmetry-broken, so-called Goldstone phase.
		- Def. Orientability
			- The existence of a consistent orientation (arrows) on each string, upwards for odd strings and downwards for even strings.
			-
			- ((64d54056-d46c-4bcf-93af-3473e32ae0d0))
				- (a) is orientable, since each string could be consistently oriented.
				- However we can see braidings would break the orientation in (b)(c)(d).
					- Note that (c)(d) is an adjacent braiding plus an adjacent measurement
		- Generally, any measurement $P_{l,l+m}$ with m odd (even) preserves (violates) the orientation, whereas any swap $R_{l,l+m}$ with m even (odd) preserves (violates)
		  the orientation.
		-
	- # ((64d63b4d-91df-4e2a-aeae-a187fcbec370))
		- Orientability is related to multiple properties of CPLC, thus the circuit.
		- The author cited one of his previous papers.
	- # ((64d63db8-931a-4dde-b5ad-62bdeb129512))
	  collapsed:: true
		- Idea: Treat non-Gaussian measurements as perturbations which is irrelevant in RG.
		- *In the viewpoint of anyons, this is just the fusion of multiple anyons...
		- ## Two Limits
			- Gaussian limit
				- Intuitively, most of the fusion tree would be fixed by previous or later Gaussian (two-anyon) measurements.
			- Non-Gaussian limit
				- The fusion tree would still be a huge superposition.
	- # ((64d63fbd-f5d3-4e52-98bd-244c02b78f79))
		- This is more tricky in the viewpoint of anyons.
			- If we fuse three $\sigma$ together, the result must still be $\sigma$.
			- On the other hand, if we measure a single majorana operator $\gamma$, the result could be $\pm 1$, which needs explanation in the anyon framework.
			- Reset any fusion result?
		- Strategy: Add an ancilla qubit (two ancilla majoranas) and connect one of the ancilla majoranas to restore parity.
			- The connected majorana operator is in a definite $+1$ eigenstate.
		- ((64d64291-e6db-4779-bee9-84a7dd98de80))
- # ((64d64308-65bb-4c8b-8c80-bfd70c5b26bb))
	- Summary
		- Measurements connecting nearest or next-nearest majoranas are performed according to some probability.
		- When orientable, the Gaussian circuits realize loop models corresponding to variants of the 1-state Potts model, and critical behavior corresponding to the 2D bond percolation universality class.
		- ((64d6435c-e357-422f-84dc-33bb3422b45e))
	- ((64d64685-0207-4ed0-b9c0-a3a26c9bdab6))
		- What is a 1-state Potts model?
	- Therefore the phase transition is described by the critical 1-state Potts model
-