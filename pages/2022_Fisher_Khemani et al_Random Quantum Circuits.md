type:: paper_reading

-
- ![2022_Fisher_Khemani et al_Random Quantum Circuits.pdf](file://zotero_link/Physics/Quantum/Quantum Circuit Dynamics/2022_Fisher_Khemani et al_Random Quantum Circuits.pdf)
- # Intro
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
	- Role of randomness
		- ((63ec4a4e-1f16-46b5-9195-fa5ab3d8c15f))
- # ((63ec4bcc-2e23-4ce2-8b37-6579aa2fddfe))
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
	- ## Simple Case: 1 and 2 qubits
		- ((63ed8b1d-eedb-43d0-bde1-5dcd72f9ed85)) creates entanglement for input $|\psi\rangle=|\rightarrow \rightarrow\rangle$, but not for $|\uparrow \uparrow\rangle$
		- Measurement on a single spin always **destroys entanglement**.
		-
- # Miscellaneous Topics
	- [[Monitored Dynamics]]
		- ((63ec4af1-74e6-4064-963e-81e25d09e85f))
	- A tensor-network perspective
		- ((63ed8e34-04c9-4844-bdb6-f00461024e05))
			- A spacetime diagram, but we may also contract the 'bricks' to obtain the overall tensor.