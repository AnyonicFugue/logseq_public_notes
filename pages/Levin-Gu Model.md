- ![2012_Levin_Gu_Braiding statistics approach to.pdf](file://zotero_link/Physics/SPT/2012_Levin_Gu_Braiding statistics approach to.pdf)
- # Comments
	- Here we have done two things: (1) Extend the Hilbert space (2) Define a transformation of the Hamiltonian (to impose gauge invariance of the ground state)
	- Can we define gauging on a quantum state, without referring to a Hamiltonian?
		- The really mysterious part is the mapping between Hilbert spaces. In the models in this paper, we rely on a really good representation (basis) of the wavefunction.
		- $\tau_l^z=\sigma_p^z \sigma_q^z$ is a map of operators; the states do not have a 'multiplication'.
- # Setup
	- Two different Hamiltonians on the same lattice.
		- $$H_0 = - \sum_p \sigma^x_p$$
			- Each $p$ labels a vertex, which is a spin.
		- $$
		  H_1=-\sum_p B_p, \quad B_p=-\sigma_p^x \prod_{\left\langle p q q^{\prime}\right\rangle} i^{\frac{1-\sigma_q^z \sigma^z_{q^{\prime}}}{2}}
		  $$
		- ((660bef61-62e8-4cad-8314-08ca2390f132))
	- Symmetry
		- So called *Ising symmetry*, i.e. the symmetry group is $\{1,g\} \cong Z_2$, with
		  $$g=\prod_p \sigma^x_p$$
			- Both $H_0$ and $H_1$ commute with $g$.
		- Note that for both Hamiltonians, the ground state is gapped and unique, so the symmetry is not broken spontaneously.
	- The notion of symmetric protected topological orders
		- In brief, SPTs are systems that cannot be smoothly deformed to a product state without breaking the symmetry.
		- Here $H_0$ is the trivial $Z_2$ SPT and $H_1$ is the nontrivial $Z_2$ SPT. It is known that we only have one nontrivial SPT in 2D.
- # Ground State
	- Prop. The ground state $\Psi_1$ is a superposition of all domain wall configurations, but each configuration enters with a sign $(-1)^{N_{d w}}$ where $N_{d w}$ is the total number of domain walls.
		- ((660bf03c-6661-48a7-973c-10f61f7b26e4))
		- Note that 
		  $$\prod_{\left\langle p q q^{\prime}\right\rangle} i^{\frac{1-\sigma_q^z \sigma^z_{q^{\prime}}}{2}}$$
		  induces a factor of $i$ for each pair of neighboring spins $q, q^{\prime}$ that have opposite values of $\sigma^z$.
			- In particular, since the number of such pairs is necessarily even, the product always reduces to a factor of $\pm 1$.
- # Gauging
	- The idea is to couple spins to a $Z_2$ gauge field to promote the **global** symmetry to a **gauge** symmetry.
	- Step 1. Extend and **restrict** the Hilbert space
		- Put a $Z_2$ gauge field on each link $pq$.
			- The two basis vectors could be labeled by the eigenvalue of $\sigma^z$,
			  $$
			  \mu_{p q}^z= \pm 1
			  $$
		- To get rid of the original d.o.f.s. we should restrict to the gauge-invariant subspace defined by the following condition,
		  $$
		  \prod_{q \in \partial p} \mu_{p q}^x=\sigma_p^x
		  $$
	- Step 2. Minimal coupling
		- Replacing each spin-spin interactions like $\sigma_q^z \sigma_{q^{\prime}}^z$ with $\sigma_q^z \mu_{q q^{\prime}}^z \sigma_{q^{\prime}}^z$.
	- Step 3. Impose gauge invariance by an energy cost term
		- Multiply every term by
		  $$
		  O_p=\prod_{\langle p q r\rangle}\left(1+\mu_{p q}^z \mu_{q r}^z \mu_{r p}^z\right) / 2
		  $$
			- Project to the subspace with $\mu_{p q}^z \mu_{q r}^z \mu_{r p}^z=1$, i.e. zero-flux subspace
		- Add a term of the form $-\sum_{\langle p q r\rangle} \mu_{p q}^z \mu_{q r}^z \mu_{r p}^z$ to the Hamiltonian.
			- This term ensures that the states with vanishing $\mathbb{Z}_2$ flux have the lowest energy.
	- Results
		- $$
		  \begin{aligned}
		  & \widetilde{H}_0=-\sum_p \sigma_p^x O_p-\sum_{\langle p q r\rangle} \mu_{p q}^z \mu_{q r}^z \mu_{r p}^z \\
		  & \widetilde{H}_1=-\sum_p \widetilde{B}_p O_p-\sum_{\langle p q r\rangle} \mu_{p q}^z \mu_{q r}^z \mu_{r p}^z
		  \end{aligned}
		  $$
			- $$
			  \widetilde{B}_p=-\sigma_p^x \prod_{\left\langle p q q^{\prime}\right\rangle} i^{\frac{1-\sigma_q^z \mu_{q q^{\prime}}^z \sigma_{q^{\prime}}^z}{2}}
			  $$
	- ## Mapping to toric code and double semion
		- Intuition
			- Every spin configuration $\left\{\sigma_p^z= \pm 1\right\}$ on the triangular lattice defines a corresponding **domain wall** configuration on the dual lattice (honeycomb lattice).
				- Note that the domain walls are defined in the basis of $Z$, while the Ising symmetry is given by $X$. Very mysterious.
				- How to understand the mapping (since it is different from the symmetry representation)? Reps of groups?
			- Formally, this correspondence is given by $$\tau_l^z=\sigma_p^z \sigma_q^z$$
				- Where $l$ is the link separating sites $pq$, $\tau_l^z=\mp 1$ corresponds to the presence or absence of a domain wall between the spin $p$ and spin $q$.
		- However, we should actually use the gauged models $\tilde H_0$ and $\tilde H_1$.
			- The problem with the direct mapping $\sigma_p^z \sigma_q^z \mapsto \tau_l^z$ is, we could only obtain states satisfying
			  $$
			  Q_v=\prod_{l \in v} \tau_l^z
			  $$
			  i.e. The map is not surjective.
			- The gauged models doesn't have the problem.
		- The map is defined by setting $\tau_l^z=\sigma_p^z \sigma_q^z \mu_{p q}^z, \tau_l^x=\mu_{p q}^x$
			- $l$ is the link connecting sites $p$ and $q$.
		- The result
			- $$
			  \begin{aligned}
			  & H_{t . c}=-\sum_v Q_v-\sum_p\left(\prod_{l \in p} \tau_l^x\right) P_p \\
			  & H_{d . s}=-\sum_v Q_v+\sum_p\left(\prod_{l \in p} \tau_l^x \prod_{l \in \operatorname{legs} \text { of } p} i^{\frac{1-\tau_l^z}{2}}\right) P_p
			  \end{aligned}
			  $$
				- $Q_v=\prod_{l \in v} \tau_l^z$, $P_p=\prod_{v \in n}\left(1+Q_v\right) / 2$
			-