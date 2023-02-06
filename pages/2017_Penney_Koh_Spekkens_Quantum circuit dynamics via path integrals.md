type:: paper_reading

- ![2017_Penney_Koh_Spekkens_Quantum circuit dynamics via path integrals.pdf](file://zotero_link/Physics/Quantum/Quantum Circuit Dynamics/2017_Penney_Koh_Spekkens_Quantum circuit dynamics via path integrals.pdf)
-
- # Abstract
	- Goal
		- Define an action for discrete-time processes, eg. quantum circuit
			- Such that the relative phases are correct.
	- Results
		- Show the case for Clifford systems, either continuous or of **odd-prime dimensions**.
			- 'Using tools from algebraic geometry...'
- # Intro
	- Another usage of [[Path Integral]]
		- ((63e04c6e-7302-4ac7-9284-36890bc9292a))
			- With an example in the following paragraph.
			- Does 'modular' mean that the information of phases are lost? #Learning-TODO
	- ## Setup and Notations
	  collapsed:: true
		- Configuration
			- $\vec{q} \equiv\left(q^{(1)}, \ldots, q^{(n)}\right)$
				- n sub systems
				- This should be understood as an element of the basis of product states
		- The total unitary is $\hat{U}=\hat{U}_N \hat{U}_{N-1} \cdots \hat{U}_2 \hat{U}_1$
			- Time is discretized into $N$ slices.
		- A path is $\gamma=\left(\vec{q}_0, \vec{q}_1, \ldots, \vec{q}_N\right)$
		- Propagator
			- $A(\gamma)=\prod_{k=1}^N\left\langle\vec{q}_k\left|\hat{U}_k\right| \vec{q}_{k-1}\right\rangle$
		- Analogy to path integral
			- $$\left\langle\vec{q}_N|\hat{U}| \vec{q}_0\right\rangle=\sum_{\vec{q}_{N-1} \in\left(\mathbb{Z}_d\right)^n} \cdots \sum_{\vec{q}_1 \in\left(\mathbb{Z}_d\right)^n} \prod_{k=1}^N\left\langle\vec{q}_k\left|\hat{U}_k\right| \vec{q}_{k-1}\right\rangle\\=\sum_{\gamma \in \mathbb{P}_0\left(\vec{q}_0, \vec{q}_N\right)} A(\gamma)$$
			- ((63e04fde-62f6-4565-bb51-7911b1dd9e7b))
		- Possible restrictions to the paths
			- $\left\langle q_k\left|\hat{U}_k\right| q_{k-1}\right\rangle \propto \delta\left(q_k-q_{k-1}\right) \delta\left(q_k-x\right)$ for a slit at x
			- $\delta\left(\vec{q}_k-f\left(\vec{q}_{k-1}\right)\right)$ for a known function $f$
		-
			-
	- ## Difficulty
		- Continuous path integral: Equal norm for each path, only a difference in phase
		- This **fails** in circuit scenario.
	- ## Specialization: Balanced
		- Motivation
			- Certain sets of universal gates are balanced.
				- Hadamard plus Toffoli
				- [[Clifford Circuit]]
			- This property could be used to provide simple proofs for, eg, $\mathrm{BQP} \subseteq \mathrm{PP}$.
			-
		- ((63e05361-7761-4f07-bdd5-b7774673645b)) Let $|\vec{q}\rangle$ denote the basis elements for the inputs of the gate and let $|\vec{Q}\rangle$ denote the basis elements for its outputs. The gate $\hat{U}$ is said to be **balanced** if
		  $$
		  \forall \vec{q}, \vec{Q} \in \mathbb{R}^m\left(\text { or }\left(\mathbb{Z}_d\right)^m\right):\langle\vec{Q}|\hat{U}| \vec{q}\rangle=\mathfrak{N} e^{i S(\vec{q}, \vec{Q})} \delta(g(\vec{q}, \vec{Q}))
		  $$
		  where $\mathfrak{N}$ is a complex constant, $S(\vec{q}, \vec{Q})$ is a function of $\vec{q}$ and $\vec{Q}$ with values in the field $\mathbb{R}, g$ is a smooth map $\mathbb{R}^m \times \mathbb{R}^m \rightarrow \mathbb{R}^m$ (or $\left(\mathbb{Z}_d\right)^m \times\left(\mathbb{Z}_d\right)^m \rightarrow\left(\mathbb{Z}_d\right)^m$ ) and $\delta$ is a Dirac-delta function on $\mathbb{R}^m$ (or a Kronecker delta function on $\left.\left(\mathbb{Z}_d\right)^m\right)$.
			- In other words, all non-zero amplitudes are equal.
		- Examples
			- Pauli-Z: Trivial-transition amplitudes are 1
			- Pauli-X and Pauli-Y: Flipping amplitudes are 1
		- Now we may write $\left\langle\vec{q}_N|\hat{U}| \vec{q}_0\right\rangle=\mathfrak{N} \sum_{\mathbb{P}\left(\vec{q}_0, \vec{q}_N\right)} e^{i S(\gamma)}$
			- Note that the delta is absorbed in the measure.
	-
-