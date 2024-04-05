# [[Questions]]
	- [[Quantum Marginal Problem]]
		-
	- Could all topological data be obtained from a single ground state?
		- This concerns the definition of topological phases: Is it a property of a state or the Hamiltonian?
		- What we know
			- Fusion rules
			- S-matrix
			- Chiral central charge
		- However, Kong claims that 'TO are defined on infinite open disks', where the notion of GSD is dubious.
- # Significance
	- [[Entanglement]] is deeply related with [[Thermalization]].
		- Intuition: Local thermalization -> Long-range entanglement
	- Quantum info provide proxies for certain kinds of classical hardness, thus helping to understand ((63e86248-136d-4d42-9012-f111fcc231cc))
- # Thoughts
	- Should we discern $|Bell_{12}\rangle \otimes |Bell_{34}\rangle$ from $|Bell_{12}\rangle \otimes |Bell_{34}\rangle$?
		- $|Bell_{12}\rangle$ means a Bell pair between qubit 1 and qubit 2.
	-
	- 'If you work too hard you get nothing'. Equal-weight superposition of all configurations doesn't work, but partial sum does.
	- Low-entanglement states can be approximated by states with a small Schmidt number (nonzero eigenvalues of reduced density matrices)
- # Properties
	- Monogamy
	  id:: 6591147e-e39c-4000-af3a-f30c39cbba4a
		- For example, if AB is a Bell state and BC is also a Bell state, there cannot be an extension of these density matrices into a single state acting on ABC.
		- Even stronger, if AB is maximally entangled, then they cannot entangle with a third state C!
			- But what is maximally entangled actually?
	- ((6590e5bc-7f96-4144-a03b-c8b4ece60d31)) of entanglement entropy
- # Quantifications
  collapsed:: true
	- [[von-Neumann Entropy]]
	- [[Renyi Entropy]]
	-
	- Refs given in [[2023_Li_Sang_Hsieh_Entanglement Dynamics of Noisy Random Circuits]]
		- [[Entanglement Negativity]]
		- [[Operator Entanglement Entropy]] #[[Research/To Be Investigated]]
	- [[Conditional mutual information]]
	  id:: 658b78c9-df4c-47bf-b17f-c4c459d25fa6
	- [[Relative Entropy]] #card
	  card-last-interval:: 31.26
	  card-repeats:: 2
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2023-09-12T19:17:45.971Z
	  card-last-reviewed:: 2023-08-12T13:17:45.972Z
	  card-last-score:: 5
		- Motivation: a measurement of how close two distributions are.
			- An alternative of fidelity.
		- $S(\rho \| \sigma)=-Tr(\rho \log \sigma)-(-Tr(\rho \log \rho))=\operatorname{Tr} \rho(\log \rho-\log \sigma)$ 
		  The sign is positive.
		- Property: positive-definite.
		-
		- [en.wikipedia.org/wiki/Quantum relative entropy](https://en.wikipedia.org/wiki/Quantum_relative_entropy)
	- Fidelity #card
	  card-last-interval:: 25.01
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2023-02-26T03:50:21.794Z
	  card-last-reviewed:: 2023-02-01T03:50:21.794Z
	  card-last-score:: 5
	  collapsed:: true
		- $F(\rho, \sigma)=\operatorname{tr} \sqrt{\sqrt{\rho} \sigma \sqrt{\rho}}$
		- A measure of how close two density matrices are.
		-
		- Properties: $F(\rho, \sigma)\le1$, with the equality sign holds only for $\rho=\sigma$
		-
	-
- # Area-Law
  id:: 654078ce-2ffb-4f24-be56-31c8887e8cb9
	- [[0705.2024] An Area Law for One Dimensional Quantum Systems (arxiv.org)](https://arxiv.org/abs/0705.2024) proves that entanglement gapped 1D quantum systems could at most scale as area law.
	- [[cond-mat/0305505] Lieb-Schultz-Mattis in Higher Dimensions (arxiv.org)](https://arxiv.org/abs/cond-mat/0305505) and [[cond-mat/0405587] Locality in Quantum and Markov Dynamics on Lattices and Networks (arxiv.org)](https://arxiv.org/abs/cond-mat/0405587) showed the exponential decay of correlation functions.
- [[Quantum Markov Chain]]