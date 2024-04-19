alias:: CPTP Map

-
- # Unitary Representation
	- $$
	  U|\psi\rangle_1|0\rangle_2 \equiv \sum_k E_k|\psi\rangle_1|k\rangle_2,
	  $$
		- $\left\{|k\rangle_2\right\}$ is an orthonormal basis for subsystem 2, whose dimension is given by the number of Kraus operators appearing in the operator-sum representation.
- # Kraus Operator
  id:: 63840eb6-970a-4787-ad25-13a3cc29ece5
	- Def #card
	  card-last-interval:: 252.3
	  card-repeats:: 4
	  card-ease-factor:: 2.9
	  card-next-schedule:: 2024-01-07T07:55:26.428Z
	  card-last-reviewed:: 2023-04-30T00:55:26.429Z
	  card-last-score:: 5
		- A Kraus operator is defined as
		  $$E_k \equiv{ }_2\langle k|U| 0\rangle_2$$
			- U is some unitary evolution of the **total** system.
			- 0 is the initial state of the environment
		- Evolution of density matrix
			- $$\rho_1^{\prime}=\sum_k E_k \rho_1 E_k^{\dagger}$$
			- Essentially tracing out the environment.
			- For a pure state $|\psi\rang$, the final state is a classical mix of $E_k|\psi\rang$
			- The map $$S:\rho_1 \mapsto \rho_1'$$ is called ((6371e68c-e4f9-4b7b-870e-5a144d39cb75))
			- The map always maps a density matrix to another one.
		- Proposition.
		  $$\sum_k E_k^{\dagger} E_k=\sum_k{ }_2\left\langle 0\left|U^{\dagger}\right| k\right\rangle_2{ }_2\langle k|U| 0\rangle_2={ }_2\left\langle 0\left|U^{\dagger} U\right| 0\right\rangle_2=I_1$$
	- Equivalence of 2 sets of Kraus operators
	  card-last-score:: 5
	  card-repeats:: 4
	  card-next-schedule:: 2024-07-16T19:00:42.729Z
	  card-last-interval:: 329.28
	  card-ease-factor:: 2.8
	  card-last-reviewed:: 2023-08-22T13:00:42.730Z
	  collapsed:: true
		- Two superoperators $\mathbb{S}\left(\rho_1\right)=\sum_k E_k \rho_1 E_k^{\dagger}$ and $\mathbb{S}^{\prime}\left(\rho_1\right)=\sum_k F_k \rho_1 F_k^{\dagger}$ are equivalent if and only if there exists a **unitary** matrix $W$ such that $F_i=\sum_j W_{i j} E_j$.
			- Essentially, W is the basis transformation between two bases of the environment.
	- ((661b485a-21c0-46b8-a066-83a195a0a5a5)) (The Kraus representation theorem) A map $\mathbb{S}: \rho_1 \rightarrow$ $\rho_1^{\prime}$ satisfying the following requirements has a Kraus representation and a unitary representation:
	  (1) is linear
	  (2) preserves hermiticity
	  (3) preserves trace
	  (4) is completely positive
		- We say that $\mathbb{S}$ is positive if, for a non-negative $\rho_1, \rho_1^{\prime}=\mathbb{S}\left(\rho_1\right)$ is also non-negative.
		- The complete positivity of $\mathbb{S}$ is a stronger requirement. It means that, for any extension of the Hilbert space $\mathcal{H}_1$ to $\mathcal{H}_1 \otimes \mathcal{H}_E$, the superoperator $\mathbb{S} \otimes \mathbb{I}_E$ is positive.
			- That is, if we add any system $E$ that has a trivial dynamics (the identity $\mathbb{I}_E$ means that no state of $E$ is changed), independently of the dynamics of system 1, the resulting superoperator $\mathbb{S} \otimes \mathbb{I}_E$ must be positive.
			- This requirement is physically motivated since, in general, it cannot be excluded that the two systems are initially entangled.
				- If this is the case and we call $\rho_{1 E}$ the density matrix corresponding to the initially entangled state, then $\rho_{1 E}^{\prime} \equiv\left(\mathbb{S} \otimes \mathbb{I}_E\right)\left(\rho_{1 E}\right)$ must be a valid density matrix.
				- This implies the positivity of $\mathbb{S} \otimes \mathbb{I}_E$ for any $E$, namely the complete positivity of $\mathbb{S}$.