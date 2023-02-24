type:: paper_reading

-
- ![2022_Fisher_Khemani et al_Random Quantum Circuits.pdf](file://zotero_link/Physics/Quantum/Quantum Circuit Dynamics/2022_Fisher_Khemani et al_Random Quantum Circuits.pdf)
- # Intro
  collapsed:: true
	- An interesting question: ((63ec434b-cf63-4e66-a0d3-ee29500cd09f))
	- Approaches
	  collapsed:: true
		- ((63ec4400-959f-46af-8d71-1290dcdbf604))
		- Thus we need new approaches.
		- ((63ec4421-118a-4f69-9497-2083815547a1))
			- ((63ec4464-1934-4619-9987-ebf33d2bd23f))
				- Can we start from the principles and deduce the possible physical quantities? #Possibility
			- Quantum mechanics is linear, of course; but this illustrates that **not all nonlinear functions are useless.** #[[Thoughts/Math and Physics]]
			-
	- Significance #card
		- [[Entanglement]] is deeply related with [[Thermalization]].
			- Intuition: Local thermalization -> Long-range entanglement
		- Entanglement could be an organizing principle for quantum matters.
			- Manifest in topo orders.
		- Quantum info provide proxies for certain kinds of classical hardness, thus helping to understand ((63e86248-136d-4d42-9012-f111fcc231cc))
		- Simple models provide playgrounds for ((63ef28fe-44d3-44b1-826c-793191d74b54)).
			- Randomness is a tool to promote solvability. #[[Thoughts/Math and Physics]]
				- Not only in random circuits, but also random matrices, Sachdev-Ye-Kitaev model
	- Role of randomness
		- ((63ec4a4e-1f16-46b5-9195-fa5ab3d8c15f))
- # ((63ec4bcc-2e23-4ce2-8b37-6579aa2fddfe))
  collapsed:: true
	- ## Setup and Notations
		- Objects to study
			- ((63ec4bf1-a0de-4842-8594-b85e207d2433)) arranged in a spatially local fashion
		- CZ gate
		  id:: 63ed8b1d-eedb-43d0-bde1-5dcd72f9ed85
			- $$
			  \mathrm{CZ}_{12} \equiv \exp \left[i \frac{\pi}{4}\left(1-Z_1\right)\left(1-Z_2\right)\right]
			  $$
			- It is a [[Clifford Gate]]. That is, it evolves a Pauli operator to another one.
			- Actually it is an entangling gate.
				- The definition is 'mapping at least one product state to an entangled state'.
				- CZ is only diagonal in the eigenbasis of $Z_1Z_2$
				-
	- ## Simplest Case: 1 and 2 qubits
		- ((63ed8b1d-eedb-43d0-bde1-5dcd72f9ed85)) creates entanglement for input $|\psi\rangle=|\rightarrow \rightarrow\rangle$, but not for $|\uparrow \uparrow\rangle$
		- Measurement on a single spin always **destroys entanglement**.
	- ## A bit complicated: A chain of qudits
	  collapsed:: true
		- The length of the chain is $L$
		- The building blocks are local gates acting on adjacent qudits.
		- Minimally-structured case
			- Every local gate $u_{x, \tau}$ is drawn randomly and independently of all the others from the uniform distribution on the unitary group $\mathrm{U}\left(q^2\right)$.
				- This uniform (Haar) distribution is defined by the invariance of all averages involving the random unitary $u_{x, \tau}$ under both left and right unitary rotations, $u_{x, \tau} \rightarrow v u_{x, \tau} w$.
			- Facts
				- Locally the state would finally equilibrate at an uniform distribution of ensembles.
					- ((63ef2614-4b9b-4177-934e-bf85dbc568e1))
				- ((63ef267f-ff5a-4caf-a00d-c6368d7605b3))
					- In contrast, conventional many-body systems have well-defined ground states at low temperature. Thus the notion of quasiparticles.
					- However, random circuits are more useful for describing nonintegrable dynamics in higher temperatures.
			-
- # ((63ef2f9d-32d7-43f8-9d6e-960280a201db))
	- ## Entanglement membrane and the pairing order parameter
		- Consider the [[Entanglement Entropy]] for a finite spatial region A in a large system composed of qudits.
			- At small times, entanglement is ((63ef3032-fbea-4bca-bdd0-d6a0c7eb223e)).
			- At infinite time, the entanglement entropy would reach the max possible value (infinite temperature), thus $S_A \propto V_A$
		- Membrane picture: $S_A$ can be obtained by minimizing an effective 'entanglement energy' for a $D$-dim membrane in the $(D+1)$-dim spacetime.
			- eg. 1D chain
				- The membrane is then a trajectory $x({t^{\prime}})$ with $x(t)=y$ and $x(0)$ free
				- $S_y(t)=s_{\mathrm{eq}} \min \left(\int_0^t \mathrm{~d} t^{\prime} \mathcal{E}(\dot{x})+S_{x_0}(0)\right)$, where $\epsilon(v)$ is model-dependent.
- # Topics
	- ## [[Monitored Dynamics]]
		- ((63ec4af1-74e6-4064-963e-81e25d09e85f))
		- ## Interesting points
			- It actually induces a random walk in the Hilbert space.
				- Moreover, due to the structure of local decomposition, **not** all points of the Hilbert space are equivalent.
		- ## Defining universal classes
			- Defs
				- Quantum trajectory #card
					- The sequence of measurement results $\mathbf{m}=\left(m_1, \ldots, m_M\right)$
					-
	- ## Quantum-Classical mappings
		-
	- ## A tensor-network perspective
		- ((63ed8e34-04c9-4844-bdb6-f00461024e05))
			- A spacetime diagram, but we may also contract the 'bricks' to obtain the overall tensor.