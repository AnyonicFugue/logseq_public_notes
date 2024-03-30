- ![2019_Headrick_Lectures on entanglement entropy in field theory.pdf](file://zotero_link/Research/Entanglement/Field Theory/2019_Headrick_Lectures on entanglement entropy in field theory.pdf)
- # Setup
	- Notations
		- $$
		  \left\langle\mathcal{O}_a\right\rangle_{\vec{p}}=\sum_a \mathcal{O}_a p_a
		  $$
			- For example, the entropy could be defined as
			  $$
			  S(\vec{p}):=\left\langle-\ln p_a\right\rangle_{\vec{p}}=-\sum_a p_a \ln p_a
			  $$
	- Definitions
		- Classical probability
			- Marginal distribution of $\vec{p}_{AB}$
				- $$
				  \left(p_A\right)_a=\sum_b\left(p_{A B}\right)_{a b}
				  $$
			- Conditional probability $\vec p_{A|b}$
				- $$
				  \left(p_{A \mid b}\right)_a=\frac{\left(p_{A B}\right)_{a b}}{\left(p_B\right)_b}
				  $$
				- Proposition. 
				  $$
				  \left\langle S\left(\vec{p}_{A \mid b}\right)\right\rangle_{\vec{p}_B}=S\left(\vec{p}_{A B}\right)-S\left(\vec{p}_B\right)
				  $$
			- Conditional entropy $H(A|B)$
			  id:: 66066aef-cf20-45c6-92cd-ba34b683703d
				- $$
				  H(A \mid B):=S(A B)-S(B)
				  $$
				- Meaning: On average, how much we still **do not** know about $A$ even after learning about $B$.
		- Quantum information
			- Modular Hamiltonian
				- $$
				  \rho_A=\frac{1}{Z} e^{-H_A}
				  $$
			- Separable states
				- $$
				  \rho=\sum_i p_i \rho_A^i \otimes \rho_B^i
				  $$
		-
- Hard question: How to tell whether a bipartite state is separable?
  background-color:: red
	- There is no smoking-gun test here.
- Entanglement in Heisenberg picture
	- Q: The state doesn't evolve, so how could the entanglement change under evolution?
	- A: The factorization of the Hilbert space into $\mathcal{H}_A \otimes \mathcal{H}_B$ evolves!
	- More precisely:
	  collapsed:: true
	  $$
	  \mathcal{H}_{A B} \cong \mathcal{H}_A \otimes \mathcal{H}_B
	  $$
	  where $\cong$ means isomorphic. 
	  In the Heisenberg picture the isomorphism is **time-dependent**.
		- Specifically, as one can see from the usual relation between the Schrödinger and Heisenberg pictures, the unitary map $U$ : $\mathcal{H}_A \otimes \mathcal{H}_B \rightarrow \mathcal{H}_{A B}$ evolves according to
		  $$
		  U^{\dagger} \frac{d U}{d t}=i H_{A B}
		  $$
		- Whether a given state $|\psi\rangle_{A B}$ in $\mathcal{H}_{A B}$ is isomorphic to a tensor product $\left|\psi^{\prime}\right\rangle_A \otimes\left|\psi^{\prime \prime}\right\rangle_B \in \mathcal{H}_A \otimes \mathcal{H}_B$ depends on the isomorphism and therefore on the time.
		- Thus, in the Heisenberg picture, when factorizing a Hilbert space into $\mathcal{H}_A \otimes \mathcal{H}_B$ and computing $\rho_A, S(A)$, etc., we need to specify not only the subsystems $A$ and $B$ but also the time at which we are looking at them.
- # ((66066fe9-88d1-4f2d-8277-c09cee530276))
	- Difficulties
		- On lattices we can divide the system into two disjoint parts, while in field theories things are ambiguous near the **entangling surface**.
		-