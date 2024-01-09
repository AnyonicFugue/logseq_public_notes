- We need to give at least to constructions:
	- The underlying lattice/manifold (correspondingly, the Hilbert space)
	- The Hamiltonian
- Mimic direct limit? What problems will arise?
- # Questions and Problems
	- What's is the role of topological invariance? A fix-point property, or a general requirement?
	  collapsed:: true
		- #+BEGIN_TIP
		  But what is 'topological invariance'? Should the property be captured by LU, GSD, entanglement, or anything else?
		  #+END_TIP
		- String-net models are 'obviously' topologically invariant, while the [[Kitaev Honeycomb]] isn't so manifest.
			- However, if we perform the JW transformation, then the viewpoint of gauging a fSPT seems also 'topologically invariant'.
			- #+BEGIN_NOTE
			  The problem is how to define the elementary transformations, both on the lattice and on the Hamiltonian.
			  #+END_NOTE
			-
- # Ideas
	- Attack step by step. 一口吃不成胖子。
		- At the first step, we can require very strong constraints on the Hamiltonian, e.g. translation invariance.
		  The most urgent problem to solve is the manifold: Finite disk? Infinite disk? Closed manifold?
		- Then we could gradually remove and add constraints.
			- Remove translation invariance
			- Add local homeomorphism, invariance under insertion of local product DOF, etc.