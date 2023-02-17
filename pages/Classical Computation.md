- [[Turing Machine]]
	- Memory ⇒ 'Tape'
	- Control unit ⇒ 'Finite internal states(and the transition formula)
	- IO ⇒ 'Read-write head'
-
- Church-Turing Thesis
	- Computable equals Turing-computable
-
- [[Computational Complexity]]
	- Def
		- (Asymptotically) minimal amount of resource scales. (Space or time)
	-
	- Common types
		- P
			- Exist polynomial-time algorithm
		- BPP
			- Exist polynomial-time algorithm to obtain the right answer with $p>1/2+\delta$. Thus we can reduce the probability of error by $k\sim O(\ln(\frac 1 \epsilon))$.
		- BQP
			- Similar to BPP, but for quantum algorithms
	-
	- Typical Problems
		- P ⇒ Eulerian cycle
		- NP ⇒ Hamiltonian cycle, k-SAT, Minimal spanning tree
-
- Theorem. And, Or, Not, FANOUT is a set of universal gates.
	- Equivalently, NAND is universal. We can try to use other gates to generate them./ex
-
- Reversible computation
	- Landauer's principle #card
	  card-last-interval:: 25.01
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2023-03-08T10:58:29.177Z
	  card-last-reviewed:: 2023-02-11T10:58:29.178Z
	  card-last-score:: 5
		- Erasing a bit costs dissipation $\Delta E\geq kT\ln2$
	- Toffoli gate
		- a,b would not be modified
		- $c'=c\oplus ab$