alias:: von-Neumann Entropy

- # Definition
	- Bipartite
		- $$S=-\operatorname{Tr}(\rho_A \ln \rho_A) $$
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
	- [[TEE]] in [[Toric Code]] #card
	  card-last-score:: 5
	  card-repeats:: 1
	  card-next-schedule:: 2023-04-27T01:15:26.451Z
	  card-last-interval:: 25.01
	  card-ease-factor:: 2.6
	  card-last-reviewed:: 2023-04-02T01:15:26.451Z
	  id:: 6498e102-7d82-4736-8535-b3d2e3043a31
	  collapsed:: true
		- ((63f9ab7a-5493-4741-8119-f9751148f6a8))
			- The correlation, corresponding to the blue strings, are generally nonlocal and topological.
		- What's different in TEE? Why don't we have to calculate the partial trace?
		  background-color:: purple
			- The key is that we can find a **clever basis** for states in region B, 
			  i.e. the basis corresponding to boundary configurations.
				- Another sort of [[Bulk-Boundary Correspondence]].
				- Note that the picture is precise when the state is written as a Schmidt decomposition, which requires each 'component' in both subsystem to be orthonormal.
				-
			- Good properties of the basis
				- A state uniquely corresponds to a boundary configuration
				- All boundary configurations have the same weight
				- *Could be explicitly written easily by loops
			-
		- Calculation
		  collapsed:: true
			- Now we calculate TEE of a certain **ground state**.
			  collapsed:: true
				- That is, we can fix a homotopy class.
				- Do so for excited states. [[Research/To Be Investigated]]
			- We need to decompose the ground state into $|\psi\rangle:=\sum c_i \cdot\left|\psi_{A i}\right\rangle \cdot|\alpha\rangle \cdot\left|\psi_{B i}\right\rangle$
			  collapsed:: true
				- The three terms corresponds to A, boundary and B.
				- In principle all configs in B have independent contributions to the reduced density matrix of A. But we may take $\psi_B$ to be a superposition state.
			- **Observations**
			  collapsed:: true
				- Allowed configurations inside a region is only dependent on the boundary config, not on the config of the other region.
				- Inside a region, each action of $B_p$ would create a new valid config (from the reference config). Moreover, they're all independent.
					- Therefore the weights of all boundary configs are equal!
				- Different boundary configs always generate independent configs in A and B.
			- Therefore, we only need to count the allowed boundary configs. They're all of equal weight.
			  collapsed:: true
				- We must have an even number of blue strings crossing the boundary.
				- $N=\sum_{k}C_{L}^{2k}$, where L is the length of the boundary.
				- By some combinatoric, we obtain $N=2^{L-1}$.
		- Result:
		  collapsed:: true
		  $$S=(L-1)\ln 2$$
			- The constant term $-\ln2$ is related to the quantum dimension of TC.
			- It is worth noting that if region $A$ has two boundaries as in Fig. $33.4$ we will get instead
			  $$
			  \mathcal{S}_{A, B}=(M-2) \log 2
			  $$
				- In other words, each piece of boundary adds a constraint.
				- Could we investigate other topologically nontrivial boundaries? #Possibility
					- Moreover, we may investigate higher dimensional topo orders with higher dimensional boundaries.
					- Reminiscent of [[Homology]] :)
- # Relation with [[Stabilizer Code]] #card
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