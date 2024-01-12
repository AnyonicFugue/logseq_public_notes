alias:: von-Neumann Entropy

- # Definition
	- Bipartite
		- $$S=-\operatorname{Tr}(\rho_A \ln \rho_A) $$
- # Properties
  id:: 6590e5bc-7f96-4144-a03b-c8b4ece60d31
	- Concavity
	  $$
	  S\left(\sum_{i=1}^k \lambda_i \rho_i\right) \geq \sum_{i=1}^k \lambda_i S\left(\rho_i\right)
	  $$
	-
	- Triangle inequality #card
	  card-last-interval:: 84
	  card-repeats:: 3
	  card-ease-factor:: 2.8
	  card-next-schedule:: 2023-07-04T01:29:13.813Z
	  card-last-reviewed:: 2023-04-11T01:29:13.813Z
	  card-last-score:: 5
	  id:: 654072b8-d6b1-4205-9b8d-756ff4b290e0
		- $\left|S\left(\rho_A\right)-S\left(\rho_B\right)\right| \leq S\left(\rho_{A B}\right) \leq S\left(\rho_A\right)+S\left(\rho_B\right)$
		- Right side
			- Known as subadditivity. Prove by [[Relative Entropy]] and $\log(\rho_A\otimes\rho_B)=\log(\rho_A)\otimes I+ I\otimes\log(\rho_B)$
		- Left side
			- [TODO]
		- *In principle they can all be solved by the variational method (with a Lagrange multiplier)
	-
	- Strong subadditivity #card
	  card-last-score:: 5
	  card-repeats:: 1
	  card-next-schedule:: 2024-02-05T07:12:32.507Z
	  card-last-interval:: 31.26
	  id:: 6590e387-581c-499d-8987-207a3fd0042d
	  card-ease-factor:: 2.6
	  card-last-reviewed:: 2024-01-05T01:12:32.507Z
		- For any tri-partite state $\rho^{123}$ the following holds
		  $$
		  S\left(\rho^{123}\right)+S\left(\rho^2\right) \leq S\left(\rho^{12}\right)+S\left(\rho^{23}\right)
		  $$
		- Take *subsystem 2 = empty*, this goes back to ordinary sub-additivity.
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