alias:: von-Neumann Entropy

- # Definition
	- Bipartite
		- $$S=-\operatorname{Tr}(\rho_A \ln \rho_A) $$
- # Properties
  id:: 6590e5bc-7f96-4144-a03b-c8b4ece60d31
	- ## Common Techniques
	  collapsed:: true
		- (Partial) Purification
		  id:: 65bf321e-a250-41e2-b075-20f64714bf41
		  collapsed:: true
			- After purification, we have the powerful property that
			  collapsed:: true
			  $$S_A=S_{X-A}$$
				- The system after purification is denoted as $X$
			- Partial purification means the state is still mixed, but with better properties.
			  collapsed:: true
				-
	- ## Mutual information
	  collapsed:: true
		- Def #card
		  card-last-interval:: 84
		  card-repeats:: 3
		  card-ease-factor:: 2.8
		  card-next-schedule:: 2023-08-04T00:34:44.300Z
		  card-last-reviewed:: 2023-05-12T00:34:44.300Z
		  card-last-score:: 5
			- $$
			  I_{A B}=S_A+S_B-S_{A \cup B}
			  $$
			- Intuitively, how much one can infer about $B$ if one knows $A$.
				- If the whole system is in a pure state but $S_A$ and $S_B$ are at the maximum, this means that each eigenstate of $\rho_A$ **1-1 corresponds** to another of $\rho_B$. Thus $I_{AB}$ reaches it maximum.
				- If the density matrix of the whole system is a product of two sub density matrices, then $A$ and $B$ are **independent**, thus $I_{AB}=0$
			- Related: ((66066aef-cf20-45c6-92cd-ba34b683703d))
				- $$I(A:B)=S(A)-H(A|B)$$
		- When $I_{AB}=0$, $\rho^{A B}=\rho^A \otimes \rho^B$
		  id:: 65bef3dc-5772-4c63-9a72-feea334f3165
		  collapsed:: true
			- See P516 of Nielson & Chuang
		-
		- ((658b78c9-df4c-47bf-b17f-c4c459d25fa6))
	- Basic arithmetics
	  collapsed:: true
		- $$S(a \rho)=-a \ln a + a S(\rho)$$
		- $$S(\rho_1 \otimes \rho_2) = S(\rho_1) + S(\rho_2)$$
		-
	- Concavity
	  collapsed:: true
		- $$
		  S\left(\sum_{i=1}^k \lambda_i \rho_i\right) \geq \sum_{i=1}^k \lambda_i S\left(\rho_i\right)
		  $$
		- $$
		  \left(S_{A B}-S_B\right)_{\sum_i p_i \rho^i} \geq \sum_i p_i\left(S_{A B}-S_B\right)_{\rho^i}
		  $$
	- Triangle (Araki-Lieb) inequality and conditions for saturation #card
	  card-last-score:: 5
	  card-repeats:: 3
	  card-next-schedule:: 2023-07-04T01:29:13.813Z
	  card-last-interval:: 84
	  id:: 654072b8-d6b1-4205-9b8d-756ff4b290e0
	  card-ease-factor:: 2.8
	  card-last-reviewed:: 2023-04-11T01:29:13.813Z
		- $\left|S\left(\rho_A\right)-S\left(\rho_B\right)\right| \leq S\left(\rho_{A B}\right) \leq S\left(\rho_A\right)+S\left(\rho_B\right)$
		- Proof
		  collapsed:: true
			- *In principle they can all be solved by the variational method (with a Lagrange multiplier)
			- Right side
			  collapsed:: true
				- Known as subadditivity. Prove by [[Relative Entropy]] and $\log(\rho_A\otimes\rho_B)=\log(\rho_A)\otimes I+ I\otimes\log(\rho_B)$
			- Left side
			  collapsed:: true
				- [TODO]
		-
		- ((65bf3b5d-b6c7-4d48-b7da-dd97be006572)). The following conditions about density matrix $\rho_{B C}$ are equivalent:
		  id:: 65bf06ea-128e-4b76-8ea9-fc14687d28fa
		  collapsed:: true
		  (1) $\left(S_{B C}+S_C-S_B\right)_\rho=0$ (saturated triangle).
		  (2) Any state $\rho_{A B C}$ which reduces to $\rho_{B C}$ on $B C$ has $I(A: C)_\rho=0$ and $I(A: C \mid B)_\rho=0$.
		  (3) For any expression of the form $\rho_{B C}=\sum_i q_i \rho_{B C}^i$, where $\left\{q_i\right\}$ is a probability distribution with $q_i>0, \forall i$ and $\left\{\rho_{B C}^i\right\}$ is a set of density matrices, we have
		  $$
		  \forall i, \quad \rho_C=\operatorname{Tr}_B \rho_{B C}^i
		  $$
		  (4) Let $\rho_{B C}=\sum_i q_i\left|i_{B C}\right\rangle\left\langle i_{B C}\right|$, with $q_i>0, \forall i$ and $\left\langle i_{B C} \mid j_{B C}\right\rangle=\delta_{i, j}, \forall i, j$, we have
		  $$
		  \forall i, j \quad \operatorname{Tr}_B\left|i_{B C}\right\rangle\left\langle j_{B C}\right|=\delta_{i, j} \rho_C 
		  $$
			- Takeaway message
			  collapsed:: true
				-
			-
			- (1) -> (2)
			  collapsed:: true
				- First, purify the state.
				- Then invoke a corollary of SSA.
			- (2) -> (1)
			  collapsed:: true
				- Take the state to be pure.
			-
			- (1)(2) -> (3)
			  collapsed:: true
				- This can be most easily proved by [partial purification](((65bf321e-a250-41e2-b075-20f64714bf41))).
				-
				- Intoduce $A$ such that
				  $$\rho_{A B C}=\sum_i q_i\left|i_A\right\rangle\left\langle i_A\right| \otimes \rho_{B C}^i$$
				- Note that ((65bef3dc-5772-4c63-9a72-feea334f3165)), which implies the desired result.
			- (3) -> (1)
			  collapsed:: true
				- First purify the state.
				- After some straightforward algebraic manipulations, property (3) leads to the desired result.
			-
			- (3) -> (4)
			  collapsed:: true
				- This step is the most interesting; it involves a tricky construction.
				- First, introduce an auxiliary system $A$ to purify the state into 
				  collapsed:: true
				  $$\left|\Psi_{A B C}\right\rangle=\sum_i \sqrt{q_i}\left|i_A\right\rangle \otimes\left|i_{B C}\right\rangle$$
					- Here $\left\{\left|i_A\right\rangle\right\}$ is an orthonormal basis of the Hilbert space $\mathcal{H}_A$.
				-
				- Proposition. For an arbitrary orthonormal basis $\left\{\left|\phi_A^i\right\rangle\right\}$ we could define $p_i \rho_{B C}^i \equiv\left\langle\phi_A^i \mid \Psi_{A B C}\right\rangle\left\langle\Psi_{A B C} \mid \phi_A^i\right\rangle$.
				- Consider the "off-diagonal" basis which contains a basis vector $\left|\varphi_{i j}^\theta\right\rangle=\frac{1}{\sqrt{2}}\left(\left|i_{A}\right\rangle+e^{i \theta}\left|j_{A}\right\rangle\right)$ with $i \neq j$ and $\theta \in[0,2 \pi]$.
				- After simple manipulations, we see
				  $$
				  e^{i \theta} \operatorname{Tr}_B\left|i_{B C}\right\rangle\left\langle j_{B C}\left|+e^{-i \theta} \operatorname{Tr}_B\right| j_{B C}\right\rangle\left\langle i_{B C}\right|=0 .
				  $$
				- Therefore, $\operatorname{Tr}_B\left|i_{B C}\right\rangle\left\langle j_{B C}\right|=0$ for $i \neq j$.
			- (4) -> (1)
			  collapsed:: true
				- Very easy after purifying the whole state.
	- [[Strong Subadditivity]]
	  card-last-score:: 5
	  card-repeats:: 1
	  card-next-schedule:: 2024-02-05T07:12:32.507Z
	  card-last-interval:: 31.26
	  id:: 6590e387-581c-499d-8987-207a3fd0042d
	  card-ease-factor:: 2.6
	  card-last-reviewed:: 2024-01-05T01:12:32.507Z
	  collapsed:: true
	- Non-increasing under single-party quantum channels
	  collapsed:: true
		- $I(X:Y)$ does not increase under a quantum channel acting only on either $X$ or $Y$.
		  id:: 65c0467f-673e-4b62-a58e-f040c2ff59b7
		- $I(X: Y \mid Z)$ does not increase under a quantum channel acting only on either $X$ or $Y$.
		  id:: 65c0467f-b2c0-48a6-93a6-a1e7f69b5e4a
- # Examples
	- ## Naive Example: 2-Qubit System
	  collapsed:: true
		- $|00\rangle +|11\rangle$ is entangled.
		  collapsed:: true
			- Different Viewpoints
				- Factor the state
				  collapsed:: true
					- The state couldn't be factored anymore (which is a vague expression), thus the two 'branches' are independent (which is also rather vague) and of equal weight.
				- Density matrix and partial trace
				  collapsed:: true
					- collapsed:: true
					  $$\rho =\left [\begin{array}{ c c|c c }
					  1 & 0 & 0 & 1\\
					  0 & 0 & 0 & 0\\
					  \hline
					  0 & 0 & 0 & 0\\
					  1 & 0 & 0 & 1
					  \end{array} \right ]$$
						- The **big blocks** correspond to the second qubit and the **position inside a block** corresponds to the first qubit.
						  collapsed:: true
							- For example, $|01\rangle \langle 01|=( |0\rangle \langle 0|) \otimes ( |1\rangle \langle 1|)$, 
							  which corresponds to the upleft ($|0_{1} \rangle \langle 0_{1} |$) of the downright block ($|1_{2} \rangle \langle 1_{2} |$)
						- To take the partial trace, we only concern the **diagonal blocks**.
						- Thus 
						  $$\rho _{A} =\left[\begin{array}{ c c }
						  1 & 0\\
						  0 & 1
						  \end{array}\right]$$
				- Partial information of the system
				  collapsed:: true
					- If we are localized in the first qubit, we don't know about the second qubit.
					- Therefore we must guess the state of second qubit, with probability of the i^{th} state given by $|c_i|^2$
		- $|00\rangle +|01\rangle +|10\rangle +|11\rangle$ is not entangled.
		  collapsed:: true
			- Different Viewpoints
				- Density matrix and partial trace
					- $$\rho =\left[\begin{array}{ c c|c c }
					  1 & 1 & 1 & 1\\
					  1 & 1 & 1 & 1\\
					  \hline
					  1 & 1 & 1 & 1\\
					  1 & 1 & 1 & 1
					  \end{array}\right]$$
					- $$\rho _{A} =\left[\begin{array}{ c c }
					  1 & 1\\
					  1 & 1
					  \end{array}\right]$$
					- The two eigenvalues of $\rho_A$ are 0 and 2, which means the state is pure.
				- Partial information of the system
					- Whether the second qubit is in $|0\rangle$ or $|1\rangle$, the first qubit is always in $|0\rangle+|1\rangle$.
					- Thus the information is complete.
		- $\frac 1 {\sqrt 3}(|00\rangle +|01\rangle +|10\rangle)$
			- $$\frac{1}{\sqrt{3}} (|00\rangle +|01\rangle +|10\rangle )=\frac{\sqrt{2}}{\sqrt{3}} (\frac{|00\rangle +|10\rangle }{\sqrt{2}}) +\frac{1}{\sqrt{3}} |01\rangle $$
			- Therefore the eigenvalues of the density matrix are $2/3$ and $1/3$ respectively.
		- #+BEGIN_TIP
		  'Traverse the states of the second qubit' is precisely taking the partial trace!
		  #+END_TIP
- # Relation with [[Stabilizer Code]] #card
  card-last-interval:: 42
  card-repeats:: 2
  card-ease-factor:: 2.7
  card-next-schedule:: 2024-02-06T01:06:51.392Z
  card-last-reviewed:: 2023-12-26T01:06:51.392Z
  card-last-score:: 5
  collapsed:: true
	- See [[2004_Fattal_Cubitt et al_Entanglement in the stabilizer formalism]]
	- Theorem. Suppose the stabilizer group $\mathcal G$ has a unique common +1 eigenstate. If we partition the lattice into $A$ and $B$, then 
	  $$S_{AB}=\frac 1 2 (\operatorname{rank}(\mathcal G)-\operatorname{rank}(\mathcal G_A)-\operatorname{rank}(\mathcal  G_B))$$
	  where $G_A$ is the subgroup of stabilizers acting trivially on region $A$ and similar for $B$.
		- Intuitively, we want to count the stabilizers 'crossing the boundary'.
		  However these stabilizers **do not** constitute a group, so we should define it as a quotient $G/\langle G_A,G_B \rangle$.
		  Thus the rank could be calculated by subtracting the rank of the kernel.
		-
		- First use the [proposition](((64b2d7a5-5f96-414a-8dd5-5649cdf05cd9))) to express the density matrix as the sum of stabilizers.
		- Proposition. When taking partial trace over $A$, any $g$ such that $\operatorname{sup}(g) \cap A \neq \empty$ is zero.
		  id:: 64b2d7a5-03fc-4db4-b894-699ecf6a1661
			- This is obvious since all stabilizers are generated by Pauli operators.
	- Generalization to $n$-partite:
	  $$S_n=\operatorname{rank}(\mathcal G)-\operatorname{rank}(\langle \mathcal G_{A_1}, ..., \mathcal G_{A_n} \rangle)$$