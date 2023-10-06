- ![2020_Francuz_Dziarmaga et al_Determining topological order from infinite.pdf](file://zotero_link/Research/TO in Kitaev Honeycomb/Anyon Data from Microscopic Data/2020_Francuz_Dziarmaga et al_Determining topological order from infinite.pdf)
- ![2020_Francuz_Dziarmaga_Determining non-Abelian topological order from.pdf](file://zotero_link/Research/TO in Kitaev Honeycomb/Anyon Data from Microscopic Data/2020_Francuz_Dziarmaga_Determining non-Abelian topological order from.pdf)
- ![Supplimentary.pdf](file://zotero_link/Research/TO in Kitaev Honeycomb/Anyon Data from Microscopic Data/Supplimentary.pdf)
- # Questions and Problems
	- It seems we only obtain the 'original' part of the doubled model.
		- TC is doubled $Z_2$, but we only obtain a $Z_2$, which is sort of like a 'boundary theory'.
- # Idea
  collapsed:: true
	- First numerically find an iPEPS, which is a superposition of all ground states
	- Then find projectors represented by MPOs to project to pure ground states.
		- To be specific, the projectors correspond to intertwining operators between degenerate boundary eigenvectors.
		- This idea is very interesting.
		- More generally, how to characterize that whether a ground state is pure or superposed?
- # Setup
  collapsed:: true
	- Tensor network
		- Two tensors $A_{a b c}^i$ and $B_{a b c}^i$ in a unit cell
		- Double tensors $\mathbb A$ and $\mathbb B$
	- PEPS transfer matrix (TM) $\Omega$
		- Obtained by contracting a whole line of $\mathbb A$ and $\mathbb B$.
		- [:span]
		- Note that $\Omega$ is a superposition of two topological sectors, thus the reduced density matrix is also a direct sum of two contributions:
		  $$
		  \mathbb{V}_{\text {cut }}=\mathbb{V}^{\mathbb{I}} \oplus \mathbb{V}^e \Rightarrow \rho_{\text {cut }}=\rho^{\mathbb{I}} \oplus \rho^e
		  $$
	- Eigenvector of a PEPS transfer matrix
		- Idea: In the thermodynamic limit, only leading eigenvectors survive.
			- $$
			  \left.\Omega^v \approx \omega \sum_{i=1}^n \mid v_i^R\right)\left(v_i^L\left|, \quad \Omega^h \approx \omega \sum_{i=1}^n\right| v_i^U\right)\left(v_i^D \mid\right.
			  $$
		- Vertical eigenvectors
		  collapsed:: true
			- ((6517edf3-3f1e-4bff-9ca5-74f242c889d7))
			- Note that the new inner indices are the right inner indices of $\Omega$.
		- Horizontal eigenvectors
		  collapsed:: true
			- ((6517ee05-eb18-4b98-8930-8c94be78c0c9))
			- Defined similarly, just on top of the lattice.
		- Proposition. Biorthonormality:
		  $$
		  \begin{aligned}
		  & \delta_{i j}=\left(v_i^L \mid v_j^R\right) \\
		  & \delta_{i j}=\left(v_i^U \mid v_j^D\right)
		  \end{aligned}
		  $$
			- I don't know how to prove it at first sight. Maybe first accept it.
	- Intertwining operators (MPO symmetries)
		- Maps between basis elements of the degenerate eigenspace.
		- ## Toric Code
		  collapsed:: true
			- Vertical
				- $$
				  v_1 Z_{\mathrm{v}}=v_2, \quad Z_{\mathrm{v}} v_2=v_1
				  $$
			- Horizontal
				- $$
				  h_1 Z_{\mathrm{h}}=h_2, \quad Z_{\mathrm{h}} h_2=h_1
				  $$
		- Proposition. The symmetries form an algebra.
			- Note that this only holds when restricted to the space of boundary eigenvectors.
			- Structure constants
				- $$
				  Z_a Z_b=\sum_c N_{a b}^c Z_c
				  $$
- # Examples of symmetry MPO
  collapsed:: true
	- ## Fibonacci
	  collapsed:: true
		- 2 boundary fixed points
		- One non-trivial symmetry $Z_2$, such that
		  $$
		  v_1^L \cdot Z_2^v=v_2^L \\
		  v_2^L \cdot Z_2^v=v_1^L+v_2^L
		  $$
		- Thus the fusion rule
		  $$
		  Z_2^v \cdot Z_2^v=1^v+Z_2^v
		  $$
		  which is the same as Fibonacci anyons!
			- Note that this rule only holds in the space spanned by fixed-point boundaries.
	- ## Ising string net
	  collapsed:: true
		- 3 boundary fixed points
		- 2 non-trivial MPO symmetries
		  $$
		  v_1^L \cdot Z_\sigma^v=v_2^L, \quad v_1^L \cdot Z_\psi^v=v_3^L .
		  $$
		  which satisfy
		  $$
		  v_2^L \cdot Z_\sigma^v=v_1^L+v_3^L, v_3^L \cdot Z_\psi^v=v_1^L, v_2^L \cdot Z_\psi^v=v_2^L, v_3^L \cdot Z_\sigma^v=v_2^L
		  $$
		- Thus the Ising fusion rule.
		-
- # PEPS transfer matrices and eigenvectors
  collapsed:: true
	- Problem
		- Since the system is topological, the eigenvectors must be degenerate.
	- In the diagonal basis, $v_1$ and $v_2$ take the following form:
	  $$
	  v_1=\rho^{\mathbb{I}} \oplus \rho^e, \quad v_2=\rho^{\mathbb{I}} \oplus-\rho^e
	  $$
	-
- # Impurity Transfer Matrices
  collapsed:: true
	- Insert intertwining operators into the tensor network to change boundary conditions.
	  collapsed:: true
		- Example. Toric code
			- ((6517cdc8-dcbe-4323-86a9-91da0ee21e28))
			- $Z_h$ creates a vertical impurity ($Z_2$ string), thus allowing us to access the remaining sectors $m$ and $\epsilon$.
		-
	- Corresponding eigenvectors
	  collapsed:: true
		- ((6517cdab-e903-4eb6-9905-04b1c9993fb2))
			- The double lines are dropped here.
			- Note that $\mathbb X_1$ is obtained variationally.
		- In these way we obtain the remaining 2 eigenvectors corresponding to the remaining 2 sectors.
	- [Claim.](((6518d31b-8bc4-4af8-a27e-18aebf33cc7b))) The eigenvectors can be obtained from
	  background-color:: red
	  $$
	  \left(x_i^L\left|\tilde{\Omega}_v\right| x_j^R\right)=\lambda\left(x_i^L \mid x_j^R\right)
	  $$
		- I can't see why the equation is equivalent to the original eigenequation.
	- Intertwining operators
	  collapsed:: true
		- Note that we must also add a tensor $\mathbb F$ to the symmetry operators so that they can act on boundary eigenvectors.
			- ((6517cce1-5dd6-4747-bd49-0505826e5d0d))
		- Note that we should first select tensors related by 
		  $$v_i^L {z}_{i j}=v_j^L$$
		  then solve for
		  $$
		  x_i^L \widetilde{z}_{i j}=x_j^L .
		  $$
		  .
		-
	- Proposition. They impurity MPO symmetries should also satisfy
	  $$
	  \widetilde{Z}_a^v \cdot \widetilde{Z}_b^v=\sum_c \widetilde{N}_{a b}^c \widetilde{Z}_c^v
	  $$
		- Note that the coefficients are not integers in general and depend on normalization.
	-
- # Projectors onto definite fluxes
	- They are useful for TEE, but not essential for S and T matrices.
		- We just need a basis (not necessarily orthogonal) for the ground space.
		  After obtaining S and T in the basis, we can diagonalize T.
	-
	- The key seems the isomorphism group of the UMTC?
	-
	- Projectors could be constructed from the symmetry operators.
	- In general, we are to find linear combinations of symmetry operators (including identity!)
	  $$
	  P=\sum_a c_a Z_a^{\imath}
	  $$
	  satisfying $P^2=P$.
	-
	- ## Toric Code
	  collapsed:: true
		- Periodic sector
			- $$
			  P^{ \pm}=\left(\mathbb{I} \pm Z_{\mathrm{v}}\right) / 2
			  $$
			- $$
			  \left|\Psi^{\mathbb{I}}\right\rangle \sim|\Psi\rangle+\left|\Psi_{\mathrm{v}}\right\rangle, \quad\left|\Psi^e\right\rangle \sim|\Psi\rangle-\left|\Psi_{\mathrm{v}}\right\rangle
			  $$
		- Anti-periodic
			- $$
			  \tilde P^{ \pm}=\left(\mathbb{I} \pm \tilde Z_{\mathrm{v}}\right) / 2
			  $$
			- $$
			  \left|\Psi^m\right\rangle \sim\left|\Psi_{\mathrm{h}}\right\rangle+\left|\Psi_{\mathrm{hv}}\right\rangle, \quad\left|\Psi^\epsilon\right\rangle \sim\left|\Psi_{\mathrm{h}}\right\rangle-\left|\Psi_{\mathrm{hv}}\right\rangle
			  $$
	- ## Fibonacci
		- $$
		  P_{ \pm}=\frac{1}{\sqrt{5}}\left(\phi^{ \pm 1} 1 \mp Z_2^v\right)
		  $$
	- ## Ising
		- $$
		  \begin{aligned}
		  & P_{1,2}=\frac{1}{2}\left(1^v \pm Z_\psi^v\right) \\
		  & P_{3,4}=\frac{1}{4}\left(31^v-Z_\psi^v\right) \pm \frac{1}{\sqrt{8}} Z_\sigma^v \\
		  & P_{5,6}=\frac{1}{4}\left(1^v+Z_\psi^v\right) \pm \frac{1}{\sqrt{8}} Z_\sigma^v
		  \end{aligned}
		  $$
		- However they are not independent.
		  $$P_3 \cdot P_4 = P_2, \quad P_5 + P_6= P_1$$
- # Impurity Projectors
	- We could numerically find projectors to definite impurities, but I'm not sure what does it mean.
- # TEE
	- Summary
		- 2nd Renyi entropy is easy to compute here. Also it is known to coincide with von Neumann TEE in string-net models.
		- In short, we put the system on an infinite cylinder, make a cut, project to pure anyon fluxes, then go to the limit of infinite width.
-
	-