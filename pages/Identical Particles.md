alias:: Second Quantization

-
- # Basics
  collapsed:: true
	- The wavefunction must be **completely symmetric** for bosons and **completely anti-symmetric** for Fermions.
	- Note that it contains both the spatial and spin part, i.e.
	  $$
	  \psi\left(\mathbf{r}_1, \mathbf{r}_2\right) \chi(s_1,s_2)=\epsilon\psi\left(\mathbf{r}_2, \mathbf{r}_1\right) \chi(s_2,s_1)
	  $$
		- $\psi$ is spatial part and $\chi$ is spin part.
		- e.g. $(\phi_1(r_1)\phi_2(r_2)-\phi_1(r_2)\phi_2(r_1))\otimes(\chi(s_1)\chi(s_2))$ is a valid fermionic state.
		  It's spatial part is anti-symmetric while the spin part is symmetric.
	-
- # Second Quantization
	- ## Motivation
	  collapsed:: true
		- States of identical particles are greatly limited, so the traditional description has lots of redundancy.
		- Occupation numbers would be a good substitute.
	- ## Bosons
	  collapsed:: true
		- CCR
			- $\left[\hat{b}_k, \hat{b}_{k^{\prime}}^{\dagger}\right]=\delta_{k k^{\prime}} \quad$ and $\quad\left[\hat{b}_k, \hat{b}_{k^{\prime}}\right]=\left[\hat{b}_k^{\dagger}, \hat{b}_{k^{\prime}}^{\dagger}\right]=0$
		- Explicitly form:
		  $$\begin{aligned} & \hat{b}_k\left|n_1, \ldots, n_k, \ldots\right\rangle=\sqrt{n_k}\left|n_1, \ldots, n_k-1, \ldots\right\rangle \\ & \hat{b}_k^{\dagger}\left|n_1, \ldots, n_k, \ldots\right\rangle=\sqrt{n_k+1}\left|n_1, \ldots, n_k+1, \ldots\right\rangle\end{aligned}$$
			- $\hat{N} \equiv \sum_k \hat{n}_k=\sum_k \hat{b}_k^{\dagger} \hat{b}_k$
		- N-body operator
	- ## Fermions
		- #+BEGIN_WARNING
		  We would have minuses when exchanging operators. So be careful of their **order**!
		  #+END_WARNING
		- CAR
			- $\left\{\hat{c}_k, \hat{c}_l^{\dagger}\right\}=\delta_{k l} \quad$ and $\quad\left\{\hat{c}_k^{\dagger}, \hat{c}_l^{\dagger}\right\}=\left\{\hat{c}_k, \hat{c}_l\right\}=0$
		- Explicit form
			- $$
			  \begin{aligned}
			  & a_i^{\dagger}\left|n_1, \ldots, n_i, \ldots, n_N\right\rangle= \begin{cases}(-1)^{\sum_{j<i} n_j}\left|n_1, \ldots, n_i+1, \ldots, n_N\right\rangle & n_i=0 \\
			  0 & n_i=1\end{cases} \\
			  & a_i\left|n_1, \ldots, n_i, \ldots, n_N\right\rangle= \begin{cases}(-1)^{\sum_{j<i} n_j}\left|n_1, \ldots, n_i-1, \ldots, n_N\right\rangle & n_i=1 \\
			  0 & n_i=0\end{cases}
			  \end{aligned}
			  $$
	- ## N-body operator
	  collapsed:: true
		- 1-body
		  collapsed:: true
			- $\hat{F}=\sum_{k_1 k_2} f_{k_1 k_2} \hat{b}_{k_1}^{\dagger} \hat{b}_{k_2} \quad$ with $\quad f_{k_1 k_2}=\left\langle k_1|\hat{f}| k_2\right\rangle$
		- 2-body
		  collapsed:: true
			- $\hat{G}=\frac{1}{2} \sum_{k^{\prime} l^{\prime}, l k} g_{k^{\prime} l^{\prime}, l k} \hat{b}_{k^{\prime}}^{\dagger} \hat{b}_{l^{\prime}}^{\dagger} \hat{b}_l \hat{b}_k$
			- Also can be viewed as scattering
		- The generalization to n-body shall be similar: Sum the possible scatterings, then divide by $n!$.
	- ## Changing representations
	  collapsed:: true
		- ## Transformation Law #card
		  card-last-interval:: 30
		  card-repeats:: 1
		  card-ease-factor:: 2.6
		  card-next-schedule:: 2023-05-13T11:35:34.196Z
		  card-last-reviewed:: 2023-04-13T11:35:34.196Z
		  card-last-score:: 5
		  collapsed:: true
			- We could change the basis
			  id:: 640846c2-c0a4-42de-8fa9-8c9b4a1faed0
			  $$\hat d_a=\sum_b \langle\psi_a|\phi_b\rangle \hat c_b$$
			- Intuitively, extract the $\psi_a$ part in $\phi_b$
			-
		- ## Field Operators
		  collapsed:: true
			- collapsed:: true
			  $$\hat{\psi}\left(\mathbf{r}^{\prime}\right)=\sum_k \hat{b}_k \psi_k\left(\mathbf{r}^{\prime}\right)$$
				- $\psi_k(r):=\langle r|k\rangle$
				-
			- CCR
			  collapsed:: true
				- $\begin{aligned} {\left[\hat{\psi}\left(\mathbf{r}^{\prime \prime}\right), \hat{\psi}^{\dagger}\left(\mathbf{r}^{\prime}\right)\right] } & =\delta\left(\mathbf{r}^{\prime \prime}-\mathbf{r}^{\prime}\right), \\ {\left[\hat{\psi}\left(\mathbf{r}^{\prime \prime}\right), \hat{\psi}\left(\mathbf{r}^{\prime}\right)\right]=\left[\hat{\psi}^{\dagger}\left(\mathbf{r}^{\prime \prime}\right), \hat{\psi}^{\dagger}\left(\mathbf{r}^{\prime}\right)\right] } & =0 .\end{aligned}$
				-
- # Could a Lattice Be Bosonic or Fermionic?
  collapsed:: true
	- First we should make the question clear; an ambiguous question cannot obtain an unambiguous answer.
		- Rephrase:
		  > For a many-body system on a lattice, must the wavefunction be completely symmetric, completely anti-symmetric or arbitrary?
		- > If not, how much do they differ on physical observables?
	- What is a lattice system?
		- We give a number of **sites**, with a Hilbert space on each site.
		- Rephrased, the sites and (a basis) of the local Hilbert spaces give the levels of the system.
			- For example, a spin-1/2 lattice system -> Each site contains two levels, namely $|\uparrow\rangle$ and $|\downarrow\rangle$.
		- There's just an additional constraint that the local occupation number of each site is well-defined and being one.
		  collapsed:: true
			- Roughly speaking, the state could be a huge superposition of states with well-defined occupation numbers.
			  Each summand has 1 particle at each site.
	- Therefore, lattice systems inherently suit the fermionic description (even if the physical d.o.f. are spin-1!) since each level has either 0 or 1 particles.
		- In this case, the fermionic creation and annihilation operators don't have intrinsic meanings. They're just a set of linear operators on the space, satisfying certain anti-commutation relations.
		  id:: 64b48b82-84da-4b28-83de-30ce1ef5338a
- # Anyonic Operators
  id:: 64b547b0-8027-43a3-a8a9-25f9fcdd65b6
  collapsed:: true
	- ## Keywords and References
		- Clifford Algebra
			- For majorana operators
		- Generalized Clifford Algebra, or Sylvester's generalized Pauli matrices
			- Precisely my 'anyonic operators'.
				- They're defined for a single qudit.
				- Can we find an operation similar to JW transformation to restore the necessary phases for more qubits?
			- [[2010_Jagannathan_On generalized Clifford algebras and their physical application]]
	- ## Definitions
	  collapsed:: true
		-
			-
	- ## Idea
	  collapsed:: true
		- In Kitaev honeycomb we just introduced a set of convenient operators satisfying CAR.
		- In principle we can also introduce some operators on the space satisfying an anyonic commutation relation, i.e.
		  collapsed:: true
		  $$
		  \begin{aligned}
		  & a_i^{\dagger}\left|n_1, \ldots, n_i, \ldots, n_N\right\rangle= \begin{cases}\lambda(\{n\})\left|n_1, \ldots, n_i+1, \ldots, n_N\right\rangle & n_i=0 \\
		  0 & n_i=1\end{cases} \\
		  & a_i\left|n_1, \ldots, n_i, \ldots, n_N\right\rangle= \begin{cases}\lambda(\{n\})\left|n_1, \ldots, n_i-1, \ldots, n_N\right\rangle & n_i=1 \\
		  0 & n_i=0\end{cases}
		  \end{aligned}
		  $$
			- As a special case, we can take $\lambda(\{n\})=(e^{i\theta})^{\sum_{j<i} n_j}$
		- Moreover we can construct **nonabelian** anyonic operators, i.e. the actions depend on the fusion outcomes (supersectors).
			- Be careful! The notion of 'nonabelian' isn't very clear here.
			- Majorana anyons are 'nonabelian', while the exchanges of majorana operators don't depend on 'fusion outcomes'.
			- The reason is that braidings are defined differently!
		- This might be used to construct some exactly solvable models...
	- ## Questions and Problems
	  collapsed:: true
		- ((64c2b3f6-31ad-42b3-9226-4160400c2729))
		- The Sylvester matrices aren't Hermitian, so it is doubtful whether measurement makes sense.
	- ## Attempt: From Sylvester's Matrices to Anyons
	  id:: 64d93625-fd1d-46bc-83ac-79cf3df4dd16
	  collapsed:: true
		- ### Problems
		  collapsed:: true
			- $c_m c_l$ isn't Hermitian.
			  collapsed:: true
				- Though when $p$ is even it has eigenvalues $\pm 1$, it couldn't have more.
				- On the other hand, $SU(2)_k$ theories could have multiple fusion channels.
				- Maybe this is another sign of the non-locality.
		- Definitions
		  collapsed:: true
			- collapsed:: true
			  $$b_{2j-1}=\Lambda_j, b_{2j}=\Sigma_j$$
				- Note that $b$ at different j (sites) commute.
				- $b_{2j-1}b_{2j}=\omega b_{2j}b_{2j-1}$
			- id:: 64d936a0-51cb-4e3d-a146-ed4f0fd97482
			  collapsed:: true
			  $$c_{2j-1}=(b_1^{-1} b_2 ... b_{2j-3}^{-1} b_{2j-2}) b_{2j-1}, c_{2j}=(b_1^{-1} b_2 ... b_{2j-3}^{-1} b_{2j-2}) b_{2j}$$
				- Similar to the JW transformation.
				- Note that $b_{2j}b_{2j-1}^{-1}=\omega b_{2j-1}^{-1}b_{2j}$. Thus the inverse reinstalls the correct phase factor.
				- For example, $c_1=b_1, c_2=b_2, c_3=b_1^{-1} b_2 b_3, c_4=b_1^{-1} b_2 b_4$.
		- Braiding rules
		  collapsed:: true
			-
		-
	- ## Observations
		- There are lots of majorana operators with relatively few modes.
		  collapsed:: true
			- Explicit matrices for the operators:
			  $$ \begin{array}{l}
			  c_{1} =\begin{bmatrix}
			  0 & 1\\
			  1 & 0
			  \end{bmatrix} =\sigma _{x}, \quad c_{2} =\begin{bmatrix}
			  0 & i\\
			  -i & 0
			  \end{bmatrix} =\sigma _{y}
			  \end{array}$$
			- My original construction:
			  $$c_{1} =\begin{bmatrix}
			  0 & 0 & 1 & 0\\
			  0 & 0 & 0 & 1\\
			  1 & 0 & 0 & 0\\
			  0 & 1 & 0 & 0
			  \end{bmatrix} , \quad \ c_{2} =\begin{bmatrix}
			  0 & 1 & 0 & 0\\
			  1 & 0 & 0 & 0\\
			  0 & 0 & 0 & -1\\
			  0 & 0 & -1 & 0
			  \end{bmatrix}$$
			- i.e. The representation decomposes!
				- Explicit decomposition:
		- In principle we can introduce different sets of operators onto the linear space.
		  They do not affect the linear structure, however they do affect the notion of **locality** since JW transformation (and alike) is highly nonlocal.
		- ### The Viewpoint of Representations
			- A single fermionic mode is an irrep of $Cl_2(2)$, i.e. the order-2 2-element Clifford algebra.
			- For $n$ modes, we can decompose the rep of $Cl_2(2n)$ into $\oplus_n Cl_2(2)$ by 'removing the exchange phase'.
				- It should also hold for general anyonic operators.
	- ## Possibilities
	  collapsed:: true
		- Upper cap of the space
		  collapsed:: true
			- In lattice models we always require the local occupation numbers to be 1, i.e. select a physical subspace of the Fock space.
			- Thus we can freely designate behaviors of the operators when $n>1$.
				- e.g. Majorana operators satisfy $c_j^2=I$ while fermionic operators satisfy $a_k^2=(a_k^\dag)^2=0$.
				- Similarly, we can require the operators to be cyclic / nilpotent / expand infinitely ...
					- Note that *cyclic* contains *quasi-cyclic* since $(e^{i\theta}c_j)^m=e^{im\theta}c_j^m$.
					- Cyclic and nilpotent both give lots of information about the eigenstructures.
		- Different shapes of the lattice
		  collapsed:: true
			- This could greatly affect the commutation relations.
			  e.g. 4 edges per vertex -> 4 swaps
		- Generalized (anti-)commutation relations
		  collapsed:: true
			- We can define generalized brackets, i.e.
			  $$[A,B]=AB-e^{i\theta}BA$$
				- By making the transformation $\theta \to \theta+\pi$, we obtain $AB+e^{i\theta}BA$.
	- ## Attempts
	  collapsed:: true
		- q-cyclic
		  collapsed:: true
			- $$a_{i}| n_{1} ,\dotsc ,n_{i} ,\dotsc ,n_{N}> =e^{i\left(\sum _{j< i} n_{j}\right)\frac{2\pi }{q}}| n_{1} ,\dotsc ,( n_{i} +1) \ \bmod q,\dotsc ,n_{N}> $$
			- This satisfies $a_i a_j = e^{i \frac {2\pi} q}a_j a_i$ for $j<i$ and $a_i^q=1$.
		- q-nilpotent
		- General combination of fermionic operators
		  background-color:: red
		  collapsed:: true
			- Def. A general combination is an invertible linear combination of fermionic operators.
			- Proposition. Change of commutation relations under the invertible combination satisfies (...)
			- Shortcoming: $c_j$ and $c_k$ could only anti-commute, which is a huge constraint.
			  background-color:: red
		-