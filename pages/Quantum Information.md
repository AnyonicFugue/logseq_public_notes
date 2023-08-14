- [[Quantum Error Correction]]
- # Entropy and Quantification of Information
	- [[Entanglement Entropy]]
		- $\mathcal{S}\left(\rho_A\right)=-\operatorname{Tr}\left[\rho_A \log \rho_A\right]=-\operatorname{Tr}\left[\rho_B \log \rho_B\right]=\mathcal{S}\left(\rho_B\right)$. Manifestly basis independent.
		- Basically, we perform the partial trace $Tr_B$ over the entire state.
		- If $\rho_A$ has zero Von-Neumann entropy, i.e. $\rho_A$ is pure, then the entire state is non-entangled.
		-
		- [Entropy of entanglement - Wikipedia](https://en.loveeleven.ml/wiki/Entropy_of_entanglement)
-
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
	- Triangle inequality of [[Entanglement Entropy]] #card
	  card-last-interval:: 84
	  card-repeats:: 3
	  card-ease-factor:: 2.8
	  card-next-schedule:: 2023-07-04T01:29:13.813Z
	  card-last-reviewed:: 2023-04-11T01:29:13.813Z
	  card-last-score:: 5
		- $\left|S\left(\rho_A\right)-S\left(\rho_B\right)\right| \leq S\left(\rho_{A B}\right) \leq S\left(\rho_A\right)+S\left(\rho_B\right)$
		- Right side: Known as subadditivity. Prove by [[Relative Entropy]] and $\log(\rho_A\otimes\rho_B)=\log(\rho_A)\otimes I+ I\otimes\log(\rho_B)$
		- Left side: [TODO]
		- *In principle they can all be solved by the variational method (with a Lagrange multiplier)
	- Fidelity #card
	  card-last-interval:: 25.01
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2023-02-26T03:50:21.794Z
	  card-last-reviewed:: 2023-02-01T03:50:21.794Z
	  card-last-score:: 5
		- $F(\rho, \sigma)=\operatorname{tr} \sqrt{\sqrt{\rho} \sigma \sqrt{\rho}}$
		- A measure of how close two density matrices are.
		-
		- Properties: $F(\rho, \sigma)\le1$, with the equality sign holds only for $\rho=\sigma$
-
-
-
- [[Bell's Inequality]]
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
	  card-last-interval:: 42
	  card-repeats:: 2
	  card-ease-factor:: 2.7
	  card-next-schedule:: 2023-08-10T01:33:36.789Z
	  card-last-reviewed:: 2023-06-29T01:33:36.790Z
	  card-last-score:: 5
		- We have two observers.
			- Alice may choose from a set of observations $\{x_i\}$, and Bob from $\{y_j\}$.
			- They would obtain measurement results in $\{a_i\}$  and $\{b_j\}$
		-
		- Non-signaling
			- $\sum_{b} p(a b \mid x y)=\sum_{b} p\left(a b \mid x y^{\prime}\right)$ for all $a, x, y, y^{\prime}$ (Also for fixed y)
		- Local
			- $p(a b \mid x y)=\int_{\Lambda} \mathrm{d} \lambda q(\lambda) p(a \mid x, \lambda) p(b \mid y, \lambda)$