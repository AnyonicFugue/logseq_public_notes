- [[Entanglement]]
	- [[Entanglement Entropy]]
- [[Quantum Error Correction]]
- [[Bell's Inequality]]
  collapsed:: true
	- Playground: Bell's state.
		- It provides entanglement, the central ingredient.
	- Version1. suppose there are 3 possible measurements.
		- Realism: A particle must have definite outcomes for each axis.
		- Locality: Bob and Alice are independent.
		- *Property of Bell-state: Anti-correlated.
		-
		- We would have $p(\boldsymbol{a}+, \boldsymbol{b}+) \leq p(\boldsymbol{a}+, \boldsymbol{c}+)+p(\boldsymbol{c}+, \boldsymbol{b}+)$.
		- In QM: $p(\boldsymbol{a}+, \boldsymbol{b}+)=\frac{1}{2} \sin ^2\left(\frac{\theta_{\boldsymbol{a b}}}{2}\right)$[Exercise].
		   if we take $a,b$ orthogonal and $c$ divides the angle equally.
	- Version2. CHSH
	-
	- General Description #card
	  card-last-interval:: 117.6
	  card-repeats:: 3
	  card-ease-factor:: 2.8
	  card-next-schedule:: 2024-07-21T15:31:29.431Z
	  card-last-reviewed:: 2024-03-26T01:31:29.431Z
	  card-last-score:: 5
		- We have two observers.
			- Alice may choose from a set of observations $\{x_i\}$, and Bob from $\{y_j\}$.
			- They would obtain measurement results in $\{a_i\}$  and $\{b_j\}$
		-
		- Non-signaling
			- $\sum_{b} p(a b \mid x y)=\sum_{b} p\left(a b \mid x y^{\prime}\right)$ for all $a, x, y, y^{\prime}$ (Also for fixed y)
		- Local
			- $p(a b \mid x y)=\int_{\Lambda} \mathrm{d} \lambda q(\lambda) p(a \mid x, \lambda) p(b \mid y, \lambda)$
- [[Quantum Marginal Problem]]
- # Separability
	- Definition. A mixed state is separable if its density matrix could be written as a convex combination of tensor products, i.e.
	  $$\rho_{AB}= \sum_i p_i \rho_A^i \otimes \rho_B^i$$