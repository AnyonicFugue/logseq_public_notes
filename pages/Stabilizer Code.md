- Ref
	- ((6385f734-efe2-495a-b391-7de87b0e5590))
-
- # Defs
  collapsed:: true
	- ${G}_n=\{\pm 1, \pm i\} \otimes\left\{I, \sigma_x, \sigma_y, \sigma_z\right\}^{\otimes n}$
		- The spanning set of all possible operators.
		- This ensures that the anti-commutators are only $\pm1$.
	- $\mathcal S$, the stablizer, is an abelian subgroup of $G_n$
		- Why abelian? #card
		  card-last-score:: 5
		  card-repeats:: 3
		  card-next-schedule:: 2023-03-16T11:34:45.161Z
		  card-last-interval:: 61.44
		  card-ease-factor:: 2.56
		  card-last-reviewed:: 2023-01-14T01:34:45.162Z
			- 1. Abelian allows them to be diagonalized simultaneously and find the preserved eigenspace.
			- 2. More importantly, the measurements of the operators won't cause extra collapses of states.
	- Stabilizer code space $\mathcal H_S$
		- $|\psi\rangle \in \mathcal{H}_S \Longleftrightarrow M|\psi\rangle=|\psi\rangle, \quad \forall M \in \mathcal{S}$
		- i.e. Simultaneous eigenvectors with eigenvalue 1
	- Syndrome
		- The set of all measured eigenvalues $\{m_j\}$, which are all from $\pm1$.
		- In other words, they indicate the error.
	- Logical operators
		- Operators commuting with $S$ but outside it, which means the code space is an invariant subspace of these operators.
	- Equivalent Codes
		- Two stabilizer codes are said to be equivalent if they only differ by permutation of qubits and single-qubit transformations.
			- Not general basis transformations!
		-
- # Basic Facts
  collapsed:: true
	- Theorem. $\left\langle\psi\left|E_a^{\dagger} E_b\right| \psi\right\rangle=C_{a b}$ iff either one of the following holds:
	  collapsed:: true
	  (1) $E_a^{\dagger} E_b \in \mathcal{S}$;
	  (2) There is an $M \in \mathcal{S}$ that anti-commutes with $E_a^{\dagger} E_b$.
		- (1) is 'non-distinguishability'. Prove orthogonality of different states as an exercise! #Learning-TODO
		- (2) means that $E_a^{\dagger} E_b$ flips the eigenvalue of $M$, thus detectable.
	- Theorem. If the stabilizers has only one common +1 eigenstate, the density matrix of the stabilizer is
	  card-last-score:: 5
	  card-repeats:: 1
	  card-next-schedule:: 2023-08-17T19:03:43.949Z
	  card-last-interval:: 31.26
	  id:: 64b2d7a5-5f96-414a-8dd5-5649cdf05cd9
	  card-ease-factor:: 2.6
	  card-last-reviewed:: 2023-07-17T13:03:43.950Z
	  $$
	  \rho=\frac{1}{|G|} \sum_{g \in S} g
	  $$ #card
		- **Idea**
			- The key insight is $\mathcal L(V) \simeq V \otimes V^* \simeq V \otimes V$.
			  Therefore we can **lift** a state into a linear operator, which is vaguely analogous to lifting to the [[Covering space]].
				- In principle we can also select other liftings...
			- Then the eigenvalue problem is converted into an invariance problem, which can be solved by the strategy of ((64b53e14-4877-4132-8efd-8eda1934a887)).
		- Due to rearrangement lemma, this expression does satisfy $g\rho=\rho$ and $\rho^2=\rho$.
		- We only need to prove $\operatorname{Tr}\rho=1$.
		  Surprisingly, this is best proved by representation theory.
			- We should view the stabilizers as a **representation** $T: G \to GL(V)$.
				- Note that all irreducible subreps of $T$ are 1D representations (commutativity) and only one of them is trivial (requirement of unique stabilizer state)
			- $$\operatorname{Tr}\rho=\frac{1}{|G|} \sum_{g \in S} \operatorname{Tr}(T(g)) 
			  \\=\sum_{j \in irreps}\frac{1}{|G|} \sum_{g \in S}\chi_j(g)$$
			- Note that the characters are orthogonal, so we may view the sum of characters as inner products with the trivial character. Only the trivial rep survives.
			- $$\operatorname{Tr}\rho=\frac{1}{|G|} \sum_{g \in S}\chi_e(g)=1$$
		- Obviously the proof does **not** work if the stabilizer space is degenerate.
		-
	-