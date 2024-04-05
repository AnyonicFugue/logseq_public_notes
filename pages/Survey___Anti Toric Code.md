# Intuition
	- Adding a plaquette doesn't alter the topology of the lattice, but it could alter the cohomology class of the sheaf (collection of density matrices / information convex sets)!
	- What is an obstruction?
		- We have lots local data, with some compatibility condition on overlapping regions.
		- We can use some transformations (adding a coboundary) to fix certain local inconsistency, but globally it cannot be consistent everywhere.
	- In general the coefficients could not factorize (some states are not product states).
		- A minimal example
			- Given two qubits, we can have very general states $a|00\rangle + b|01\rangle + c|10\rangle + d|11\rangle$
				- In general there is no factorization $(r_0 |0\rangle + r_1 |1\rangle) \otimes (s_0 |0\rangle + s_1 |1\rangle)$
			- The reduced density matrices are
			  $$
			  \begin{align*}
			  \rho _{1} & =\begin{pmatrix}
			  |a|^{2} +|b|^{2} & ac^{*} +bd^{*}\\
			  a^{*} c+b^{*} d & |c|^{2} +|d|^{2}
			  \end{pmatrix}\\
			  \rho _{2} & =\begin{pmatrix}
			  |a|^{2} +|c|^{2} & ab^{*} +cd^{*}\\
			  a^{*} b+c^{*} d & |b|^{2} +|d|^{2}
			  \end{pmatrix}
			  \end{align*}
			  $$
		- However, the string-net model has the special feature that once the boundary configuration is fixed, the bulk is completely determined.
			- Loosely speaking, the density matrix has some factorization property.
				- However, it is different from the factorization of pure states, since different boundary configurations are classically mixed.
	- The structure should distinguish classical mix from quantum superposition.
- # TODOs
  collapsed:: true
	- Compare to the orientation problem of Mobius strip and Penrose's impossible figure for example.
	-
- # Ideas
  collapsed:: true
	- The problem could first be studied by $Z_2$ cohomology (selecting the string basis), then generalized to a **basis-independent formulation**.
		- Should the $Z_2$ cohomology be $U(1)$ cohomology in fact?
	- Is there always a solution to the merging problem (marginal problem) if $$S(AB)+S(BC)-S(B) \geq 0$$?
		- Intuitively, Petz recovery could always work in this case.
	- We could generalize to any anti quantum double or anti LW model.
	- The definition ((660b714e-44f2-4829-bdd7-c952d8cd4905)) could suffer from topological obstructions.
	- Definition. Closed sets on the lattice
		- A basis is the set of all plaquettes (more precisely, the set of the set of edges of the same plaquettes)
		-
- # Setup
	- The Hamiltonian is
	  $$H_{anti}=- \sum_v A_v + \sum_p B_p$$
		- $$
		  A_v=\prod_{j \in \partial v} \sigma_j^z \quad B_p=\prod_{j \in \partial p} \sigma_j^x
		  $$
		- Note that the Hamiltonian of conventional toric code is $$H= - \sum_v A_v - \sum_p B_p$$
- # Frustration
	- In the conventional toric code, we know that the ground state is the 'equal-weight superposition of closed-string configurations'. Why?
		- To minimize the energy, we enforce $A_v = B_p =1$.
		- $A_v=1$ requires strings to be closed.
		- $B_p = 1$ means the configuration before and after flipping plaquette $p$ should have equal weight.
	- It seems we can construct the ground state for anti toric code in a similar way.
		- To minimize the energy, we enforce $A_v = 1, B_p =-1$.
		- $A_v=1$ requires strings to be closed.
		- $B_p = -1$ means the configuration after flipping plaquette $p$ should have an extra minus in its weight (compared to the configuration before flipping $p$).
	- However, on a closed surface with an odd number of plaquettes, we cannot have all $B_p=-1$ since $\prod_p B_p= 1$!
	  background-color:: red
	-
- # Merging Problem and Obstruction
	- The frustration can be rephrased in the viewpoint of quantum marginal problem.
		- #+BEGIN_TIP
		  The quantum marginal problem:
		  Given reduced density matrices for subsystems of a multipartite quantum system, can we 'merge' the reduced density matrices, find a total density matrix compatible with the given reduced density matrices?
		  #+END_TIP
	- For the toric code, we know that density matrices on disks must be the classical mix of boundary string configurations (and a equal-weight linear superposition of equivalent bulk configurations).
	  Also, the local density matrices can be merged to global ones (the solution space is 1-dimensional on the sphere and 4-dimensional on the torus).
	-
	- For the anti toric code, we hope that the density matrices on disks are the classical mix of boundary string configurations (and a superposition of equivalent bulk configurations).
	- Smaller disks can always be merged to larger disks, but they cannot be merged to a closed surface with an odd number of plaquettes!
	  background-color:: red
		- This is a kind of topological obstruction.
- # $Z_2$ Cohomology in the closed-string picture?
	- The key is that we should assign a sign for each closed-string configuration, subject to the constraint that flipping a plaquette adds a minus.
	- ## Notation
	  collapsed:: true
		- The whole lattice is denoted $M$
		- $A$ denotes a subsystem
		  collapsed:: true
			- $\mu_A$ denotes some **boundary** string configuration of $A$
			- $\Omega_A$ denotes the set of all closed-string configurations on $A$
			  collapsed:: true
				- $\omega_A \in \Omega_A$ denotes some closed-string configuration on all of $A$
		- $p$ denotes a plaquette and $B_p$ denotes the action to flip all edges the plaquette
		- Restriction of a closed string configuration
		  collapsed:: true
			- For a subsystem $A_1 \sub A$, $\omega_A|_{A_1}$ means restriction of the closed-string configuration $\omega_A$ to the subsystem $A_1$.
		-
	- Definition. Local sign structure
	  collapsed:: true
		- For a subsystem $A$, a **local sign structure** is a map $f_A: \Omega_A \to Z_2 =\{-1, +1\}$, satisfying the condition:
		  collapsed:: true
		  For any plaquette $p \in A$ and any closed-string configuration $\omega_A \in \Omega_A$, $f(B_p \cdot \omega_A)=-f(\omega_A)$
			- Flipping a plaquette should add a minus to the sign.
	- Definition. Partition of local sign structures
	  collapsed:: true
		- For a subsystem $A$ and a partition of $A$ into two disjoint subsystems $A_1$ and $A_2$, a **partition** of the local sign structure $f_A$ are local sign structures $f_{A \to A_1}$ on $A_1$ and $f_{A \to A_2}$ on $A_2$, with the following condition:
		  id:: 660d00a0-bc1e-447f-84a1-2682dbdeb2ff
		  $$f_A(\omega_A)=f_{A \to A_1}(\omega_A|_{A_1}) \cdot f_{A \to A_2}(\omega_A|_{A_2})$$
		- #+BEGIN_NOTE
		  The partition is not unique. We have some freedoms, which are probably coboundaries of the cohomology.
		  #+END_NOTE
		-
	- Definition. Consistency of partitions of local sign structures
	  collapsed:: true
		- For two subsystems $A$ and $B$, we partition $f_A$ into $f_{A \to A-B}$ and $f_{A \to A \cap B}$, as well as partition $f_B$ into $f_{B \to B-A}$ and $f_{B \to B \cap A}$
		- The partitions are said to be **consistent** if
		  $$f_{A \to A \cap B}= f_{B \to B \cap A}$$
	- Definition. Merging of local sign structures
	  collapsed:: true
		- For two subsystems $A$ and $B$, with sign structures $f_A, f_B$ and consistent partitions, the **merging** of $f_A$ and $f_B$ is a sign structure on $A \cup B$
		  $$f_A \oplus f_B: \Omega_{A \cup B} \to Z_2$$
		  such that for any $\omega_{AB} \in \Omega_{A \cup B}$, we have
		  $$f_A \oplus f_B(\omega_{AB}) = f_{A \to A-B}(\omega_{AB}|_{A-B}) \cdot f_{A \to A \cup B}(\omega_{AB}|_{A \cup B}) \cdot f_{B \to B-A}(\omega_{AB}|_{B-A})$$
		- Note that if we have consistent partitions of sign structures on $A$ and $C$ respectively, merging $f_A$ with $f_B$ doesn't break consistency with $C$.
	- collapsed:: true
	  #+BEGIN_TIP
	  Now, the merging problem is that for many given local sign structures, can we find appropriate partitions of local sign structures that are consistent everywhere, so they can be merged into a global sign structure?
	  #+END_TIP
		-
	- Does the structure lead to a product density matrix or a product state (factorized coefficients)?
	  background-color:: red
		- No. There is one important requirement: When we partition a region $A$ into $A_1$ and $A_2$ and correspondingly partition the sign structure, **not any two configuration of the subregions can pair**. The boundary configurations must match.
	- ## Quasi-Factorization, Purification and CMI
		-
- # Quantum formulation
	- The above formulation is dependent on the basis (closed-string picture). We need something independent of basis.
	-
	-
	-