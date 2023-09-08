alias:: Second Quantization

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
  collapsed:: true
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
- [[Projects/Anyonic Operator]]
  id:: 64b547b0-8027-43a3-a8a9-25f9fcdd65b6
  collapsed:: true