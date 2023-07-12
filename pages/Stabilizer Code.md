- Ref
	- ((6385f734-efe2-495a-b391-7de87b0e5590))
-
- # Defs
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
	- Theorem. $\left\langle\psi\left|E_a^{\dagger} E_b\right| \psi\right\rangle=C_{a b}$ iff either one of the following holds:
	  (1) $E_a^{\dagger} E_b \in \mathcal{S}$;
	  (2) There is an $M \in \mathcal{S}$ that anti-commutes with $E_a^{\dagger} E_b$.
		- (1) is 'non-distinguishability'. Prove orthogonality of different states as an exercise! #Learning-TODO
		- (2) means that $E_a^{\dagger} E_b$ flips the eigenvalue of $M$, thus detectable.
	-