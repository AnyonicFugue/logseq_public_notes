type:: paper_reading

- ![2017_Penney_Koh_Spekkens_Quantum circuit dynamics via path integrals.pdf](file://zotero_link/Physics/Quantum/Quantum Circuit Dynamics/2017_Penney_Koh_Spekkens_Quantum circuit dynamics via path integrals.pdf)
-
- # Abstract
  collapsed:: true
	- ### Central question: ((63e1f3ac-c7b0-48fd-8803-6e5b78245829))
	- Significance
		- Provide insight into the relationship between classical and quantum
		- Hints on how to quantize certain systems, i.e. Discrete d.o.f.
		- Even more. A quantum Hilbert space is countable-dimensional, but the classical phase space is of uncountable size. So the knowledge might provide insights on how to deal with countability and regularize [[Path Integral]]! #Possibility [[Mar 5th, 2023]]
			- Is the number of d.o.f. of the universe a huge prime?
	- Goal
		- Define an action for discrete-time processes, eg. quantum circuit
			- Such that the relative phases are correct.
	- Results
		- Show the case for Clifford systems, either continuous or of **odd-prime dimensions**.
			- 'Using tools from algebraic geometry...'
- # Intro
  collapsed:: true
	- Another usage of [[Path Integral]]
		- ((63e04c6e-7302-4ac7-9284-36890bc9292a))
			- With an example in the following paragraph.
			- Does 'modular' mean that the information of phases are lost? #Learning-TODO
	- ## Difficulty
	  collapsed:: true
		- Continuous path integral: Equal norm for each path, only a difference in phase
		- This **fails** in circuit scenario.
	- ## Specialization: Balanced
	  collapsed:: true
		- Motivation
			- Certain sets of universal gates are balanced.
				- Hadamard plus Toffoli
				- [[Clifford Circuit]]
			- This property could be used to provide simple proofs for, eg, $\mathrm{BQP} \subseteq \mathrm{PP}$.
			-
		- ((63e05361-7761-4f07-bdd5-b7774673645b)) Let $|\vec{q}\rangle$ denote the basis elements for the inputs of the gate and let $|\vec{Q}\rangle$ denote the basis elements for its outputs. The gate $\hat{U}$ is said to be **balanced** if
		  collapsed:: true
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
	- ## Two Roles of the [[Action]]
	  collapsed:: true
		- Determine the trajectory via the least-action principle, which is well-known.
		- Generate a symplectomorphism associated with the evolution
			- Specifically, let 
			  $$G_\phi(\vec{q}, \vec{Q}) \equiv S\left[\gamma_{\mathrm{cl}}\right]=\int_0^T \mathcal{L}\left(\vec{q}_{\mathrm{cl}}(t), \dot{\vec{q}}_{\mathrm{cl}}(t)\right) \mathrm{d} t$$
			  , then 
			  $$p^{(i)}=-\frac{\partial G_\phi(\vec{q}, \vec{Q})}{\partial q^{(i)}}, P^{(i)}=\frac{\partial G_\phi(\vec{q}, \vec{Q})}{\partial Q^{(i)}}$$
				- Don't say 'P depends on p via evolution'; here p and P can be arbitrarily chosen, with the trajectory determined by functional analysis.
			- ((63e1f6f4-67aa-442d-9e66-4c1e238e7b24))
	- ## Define action for discrete-time discrete-DOF systems #card
	  card-last-interval:: 30
	  card-repeats:: 2
	  card-ease-factor:: 2.7
	  card-next-schedule:: 2023-06-02T00:45:20.202Z
	  card-last-reviewed:: 2023-05-03T00:45:20.202Z
	  card-last-score:: 5
		- The classical counterpart for a quantum system with discrete d.o.f. is ((63e35114-4fc2-470f-9ace-c8d3fbe19ef6)).
			- ((63e35121-4bf6-4ae7-9809-a5fc8ceb8b28)).
			- [[Non-Contextual]]
				- Non-contextual hidden variables are those that fix values or probabilities or expectation values for all quantum mechanical observables, independent of any experimental context.
		- Therefore, we could define the Discrete-Time Action in terms of the **generating function** instead of the non-existent Lagrangian
			- $S(\gamma)=S\left(\vec{q}_0, \ldots, \vec{q}_N\right)=\sum_{k=1}^N G_{\phi_k}\left(\vec{q}_{k-1}, \vec{q}_k\right)$.
		- Problem: How to define such 'generating function', which often uses differentiation, in the case of discrete variables?
		  background-color:: red
			- An answer of genius: ((63e1facc-b1ac-48f9-ac79-d9d60f150fa2))! #Strategy
				- This allows countless discoveries on finite fields.
				- The underlying idea: Structures of a space <-> structures on its algebra of functions.
			- ((63e1fb28-0bf1-4292-8254-e0649f2c1bad))
				- Under this duality, the algebraic counterpart of an **affine space** over Zd is an **algebra of polynomials** with coefficients in Zd, where the number of variables equals the dimension of the affine space.
					- ((63e1fbe5-5ccc-4d46-ade8-66cf04335482))
					- For example, for a symplectomorphism $\phi:\left(\mathbb{Z}_d\right)^2 \times\left(\mathbb{Z}_d\right)^2 \rightarrow\left(\mathbb{Z}_d\right)^2 \times\left(\mathbb{Z}_d\right)^2$ on a pair of two systems, the associated generating function is a **polynomial** with coefficients in $Z_d$, $G_\phi(\vec{q}, \vec{Q}):\left(\mathbb{Z}_d\right)^2 \times\left(\mathbb{Z}_d\right)^2 \rightarrow \mathbb{Z}_d$
				- [[Algebraic Geometry]] tells us that the dual of a differential structure is the Kahler differential forms
		- Can we also define some sort of least-action principle for discrete variables? #[[Open problem]]
			- 'Extremize' is meaningless here because $Z_d$ isn't ordered.
			- We should be able to talk about some sort of 'stability with respect to variations', with the differential variation substituted by Kahler differential forms.
			- On the other hand, could we link the two roles, both in classical mechanics (symplectic manifolds) and algebraic geometry?
				- Maybe we should ask Langlands for help...
				- Or even better, create some sort of 'functional Langlands correspondence'
- # Setup and Notations
	- ((63e35d05-cd98-44e0-ae12-48e71a6e4134))
	  collapsed:: true
		- Arrows $(\vec{x})$ indicate vector quantities and bracketed superscripts $\left(x^{(i)}\right)$ their components.
		- Subscripts $\left(x_k\right)$ will be used to index time steps.
		- Hats $(\hat{x})$ indicate operators.
		- $\mathbb{Z}_d$ denotes the ring of integers modulo d.
		- Complex conjugation will be represented by an overbar $(\bar{z})$.
	- ## [[Clifford Circuit]]
		- ### Continuous-Variable
			- n-system CV Clifford group
			  collapsed:: true
				- The $n$-system **CV Pauli group** $\mathcal{G}_n$, is the subgroup of $U\left(L^2\left(\mathbb{R}^n\right)\right)$ that is generated by $\left\{\hat{X}_i(\tau), \hat{Z}_i(\sigma): \tau, \sigma \in \mathbb{R}, i \in\{1, \ldots, n\}\right\}$ where $\hat{X}_i(\tau)$ is the operator that translates system $i$ by $\tau$ and $\hat{Z}_i(\sigma):=e^{i \sigma \hat{q}_i}$ is the operator that boosts system $i$ by $\sigma$.
				- ((63e49488-c73b-4569-ac5c-a42c56720cc5)). The n-system **CV Clifford group,** $C_n$, is defined to be the normaliser of the n-system CV Pauli group inside $U\left(L^2\left(\mathbb{R}^n\right)\right)$, that is, $C_n:=N\left(\mathcal{G}_n\right)$
					- The normalizer of a set $S$ is $\mathrm{N}_G(S)=\{g \in G \mid g S=S g\}=\left\{g \in G \mid g S g^{-1}=S\right\}$
					- If $S$ is a group, $N_G(S)$ is also the largest group containing $S$ as a normal subgroup.
			- Generating set
				- $$
				  \begin{aligned}
				  \hat{F} & =e^{-i \frac{\pi}{4}\left(\hat{q}^2+\hat{p}^2\right)} \\
				  \hat{P}(\eta) & =e^{-i \frac{\eta}{2} \hat{q}^2}, \quad \eta \in \mathbb{R} \\
				  \hat{X}(\tau) & =e^{-i \tau \hat{p}}, \quad \tau \in \mathbb{R} \\
				  \hat{\Sigma} & =e^{-i \hat{q}^{(1)} \otimes \hat{p}^{(2)}}
				  \end{aligned}
				  $$
				  Along with their Hermitian conjugates.
				- This is a generating set for $C_n / U(1)$, i.e. up to phase factors.
				- Names
					- $F$: Fourier gate
					- $P$: Phase gate. 'Squeezing the phase space in a position-dependent manner'
					- $X$: Coordinate translation
					- $\Sigma$: Sum gate, analogous to CNOT.
			- Matrix elements
			  id:: 63e495fd-d3a5-402d-8581-e1a27e51d137
			  collapsed:: true
				- $$
				  \begin{aligned}
				  & \langle Q|\hat{F}| q\rangle=\frac{1-i}{2 \sqrt{\pi}} e^{-i Q q} \\
				  & \langle Q|\hat{F}^{\dagger}| q\rangle=\frac{1+i}{2 \sqrt{\pi}} e^{i Q q} \\
				  & \langle Q|\hat{P}(\eta)| q\rangle=e^{-i \frac{\eta}{2} q^2} \delta(Q-q) ; \\
				  & \langle Q|\hat{X}(\tau)| q\rangle=\delta(Q-(q+\tau)) ; \\
				  & \left\langle Q^{(1)}, Q^{(2)}\left|\hat{\Sigma}\right| q^{(1)}, q^{(2)}\right\rangle=\delta\left(Q^{(1)}-q^{(1)}\right) \delta\left(Q^{(2)}-\left(q^{(2)}+q^{(1)}\right)\right) \\
				  & \left\langle Q^{(1)}, Q^{(2)}\left|\hat{\Sigma}^{\dagger}\right| q^{(1)}, q^{(2)}\right\rangle=\delta\left(Q^{(1)}-q^{(1)}\right) \delta\left(Q^{(2)}-\left(q^{(2)}-q^{(1)}\right)\right)
				  \end{aligned}
				  $$
				- It follows that they're all **balanced**.
			- Notation of the circuit
				- ((63e49c76-5b6e-452b-a653-461d1a220b02))
				  id:: 63e49c78-056d-4d5e-81b7-44a43887c6ba
				- Inputs at the leftmost
				- Outputs at the rightmost
				- Labels $x_j$ following the j^{th} $F$ or $F^\dag$
			- Constraint function
			  id:: 63e49d2c-9cd4-4aa0-b69d-9497a8c8ca81
			  collapsed:: true
				- For every $i \in\{1, \ldots, n\}$, define 
				  $$B^{(i)}(\vec{x})$$
				   to be the configuration of the $i$ th system at the output of the circuit as a function of the free configuration parameters, $\vec{x}$.
					- The form of this function can depend on the configurations of the input systems, $\vec{q}_0$, which are given as initial conditions, as well as the $\tau$ and $\eta$ parameters of the $X(\tau)$ and $P(\eta)$ gates which are given by the specification of the circuit.
				- For example, 
				  $$
				  \begin{aligned}
				  & B^{(1)}(\vec{x})=x_1+\tau, \\
				  & B^{(2)}(\vec{x})=q_0^{(2)}-x_1, \\
				  & B^{(3)}(\vec{x})=x_2 .
				  \end{aligned}
				  $$
				  in the [circuit](((63e49c78-056d-4d5e-81b7-44a43887c6ba))) above.
				- Thus for a general circuit $\mathfrak{C}$, the vector of free configuration parameters, $\vec{x}$, is constrained to the set $\mathbb{F}_{\mathfrak{C}}\left(\vec{q}_0, \vec{q}_f\right)$, where
				  $$
				  \mathbb{F}_{\mathfrak{C}}\left(\vec{q}_0, \vec{q}_f\right) \equiv\left\{\vec{x} \mid B^{(i)}(\vec{x})=q_{\mathrm{f}}^{(i)}, \forall i \in\{1, \ldots, n\}\right\}
				  $$
				-
		- ### Discrete
			-
	- Configuration
	  collapsed:: true
		- $\vec{q} \equiv\left(q^{(1)}, \ldots, q^{(n)}\right)$
			- n sub systems
			- This should be understood as an element of the basis of product states
	- The total unitary is $\hat{U}=\hat{U}_N \hat{U}_{N-1} \cdots \hat{U}_2 \hat{U}_1$
	  collapsed:: true
		- Time is discretized into $N$ slices.
	- A path is $\gamma=\left(\vec{q}_0, \vec{q}_1, \ldots, \vec{q}_N\right)$
	- Propagator
	  collapsed:: true
		- $A(\gamma)=\prod_{k=1}^N\left\langle\vec{q}_k\left|\hat{U}_k\right| \vec{q}_{k-1}\right\rangle$
	- Analogy to path integral
	  collapsed:: true
		- $$\left\langle\vec{q}_N|\hat{U}| \vec{q}_0\right\rangle=\sum_{\vec{q}_{N-1} \in\left(\mathbb{Z}_d\right)^n} \cdots \sum_{\vec{q}_1 \in\left(\mathbb{Z}_d\right)^n} \prod_{k=1}^N\left\langle\vec{q}_k\left|\hat{U}_k\right| \vec{q}_{k-1}\right\rangle\\=\sum_{\gamma \in \mathbb{P}_0\left(\vec{q}_0, \vec{q}_N\right)} A(\gamma)$$
		- ((63e04fde-62f6-4565-bb51-7911b1dd9e7b))
	- Possible restrictions to the paths
		- $\left\langle q_k\left|\hat{U}_k\right| q_{k-1}\right\rangle \propto \delta\left(q_k-q_{k-1}\right) \delta\left(q_k-x\right)$ for a slit at x
		- $\delta\left(\vec{q}_k-f\left(\vec{q}_{k-1}\right)\right)$ for a known function $f$
	-
		-
-
- # Continuous-Variable Clifford Circuits
	- ## ((63e49263-6edf-4a59-b143-f5652df7b73d))
		- Contributions of gates from the ((63e495fd-d3a5-402d-8581-e1a27e51d137))
		  collapsed:: true
			- They're summarized formally in ((63e4999e-fdff-4dbb-b6ae-85684d51cadf)).
			  collapsed:: true
				- ((63e499d0-4b44-4558-b263-0a6724314fb9))
			- First of all, each $\hat{F}$ gate introduces a path-independent **overall factor** of $\frac{1-i}{2 \sqrt{\pi}}$ and similarly for $\hat F ^\dag$
			- Phase factors, or action
			  collapsed:: true
				- Each $\hat{F}$ gate introdu a phase factor of $e^{-i Q \text { (gate) } q(\text { gate) }}$
				- Each $\hat{F}^{\dagger}$ gate a phase factor of $e^{i Q \text { (gate) } q(\text { gate) }}$
				- Each $\hat{P}(\eta)$ gate a phase factor $e^{-i \frac{\eta}{2} q(\text { gate })^2}$.
			- **Constraints** on the allowed paths from the $\mathbb{1}, \hat{P}(\eta), \hat{X}(\tau), \hat{\Sigma}$ and $\hat{\Sigma}^{\dagger}$ gates.
			  collapsed:: true
				- $$
				  \begin{aligned}
				  & \mathbb{1}, \hat{P}(\eta) \text { gates }: Q(\text { gate })=q(\text { gate }) \\
				  & \hat{X}(\tau) \text { gates }: Q(\text { gate })=q(\text { gate })+\tau \\
				  & \hat{\Sigma} \text { gates }: Q^{(1)}(\text { gate })=q^{(1)}(\text { gate }), \quad Q^{(2)}(\text { gate })=q^{(1)}(\text { gate })+q^{(2)}(\text { gate }) \\
				  & \hat{\Sigma}^{\dagger} \text { gates }: Q^{(1)}(\text { gate })=q^{(1)}(\text { gate }), \quad Q^{(2)}(\text { gate })=q^{(2)}(\text { gate })-q^{(1)}(\text { gate })
				  \end{aligned}
				  $$
		- Configuration parameters
			- Note that $F$ and $F^\dag$ allow all output configurations. Therefore, ((63e49af5-2559-437d-bb0b-85bb2edf287a)).
			- We will call these the **free configuration parameters** and denote them by $x_1, \ldots, x_L$, with the collection represented by the vector $\vec{x} \equiv\left(x_1, \ldots, x_L\right)$.
				- The number $L$ of parameters sufficient to describe the space of allowed paths is just the sum of the number of $\hat{F}$ gates and the number of $\hat{F}^{\dagger}$ gates, $L \equiv \#(\hat{F})+\#\left(\hat{F}^{\dagger}\right)$.
			- It follows that every allowed path can be expressed as a function of these parameters, $\gamma(\vec{x})$. However, the path $\gamma(\vec{x})$ may **not** be an allowed path for all choices of values for the $L$ parameters, and so the parameters are **constrained to live in some subspace** of $\mathbb{R}^L$.
				- See ((63e49d2c-9cd4-4aa0-b69d-9497a8c8ca81)).
			- Now we may write the path integral as an integration over the allowed subspace (which could be empty), 
			  $$\left\langle\vec{q}_{\mathrm{f}}|\hat{U}| \vec{q}_0\right\rangle=\mathfrak{N}_{\mathfrak{C}} \int_{\mathbb{F}_{\mathfrak{C}}\left(\vec{q}_0, \vec{q}_f\right)} e^{i S_{\mathfrak{C}}(\gamma(\vec{x}))} \mathrm{d}^L x$$
				- The phase factor depends on the configuration parameters.
		-
			-