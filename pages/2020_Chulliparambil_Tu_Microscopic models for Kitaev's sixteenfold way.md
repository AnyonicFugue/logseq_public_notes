- ![2020_Chulliparambil_Tu_Microscopic models for Kitaev's sixteenfold way.pdf](file://zotero_link/Research/Anyon Data from Microscopic Data/2020_Chulliparambil_Tu_Microscopic models for Kitaev's sixteenfold way.pdf)
- # The Models
  collapsed:: true
	- ## Setup
	  collapsed:: true
		- This family of models is deﬁned on the square (honeycomb) lattice for even (odd) ν.
		- For $\nu=2 q$ and $2 q+1\left(q \in \mathbb{N}_0\right)$, the models a $2^{q+1}$-dimensional Hilbert space at each lattice site.
		- The local operators for constructing the Hamiltonian are given by the generators of a $2^{q+1}$-dimensional representation of the Clifford algebra, $\Gamma^\alpha(\alpha=1, \ldots, 2 q+3)$
			- They are Hermitian and satisfy $\left\{\Gamma^\alpha, \Gamma^\beta\right\}=2 \delta_{\alpha \beta}$.
			- Their commutators $\Gamma^{\alpha \beta}=\frac{i}{2}\left[\Gamma^\alpha, \Gamma^\beta\right]$.
		- $$
		  H=-\sum_{\langle i j\rangle_\gamma} J_\gamma\left(\Gamma_i^\gamma \Gamma_j^\gamma+\sum_{\beta=\gamma_{\mathrm{m}}+1}^{2 q+3} \Gamma_i^{\gamma \beta} \Gamma_j^{\gamma \beta}\right)
		  $$
			- $\langle i j\rangle_\gamma$ denotes for different types of links between neighboring sites.
			  collapsed:: true
				- $\gamma_{\mathrm{m}}=4$ for the square lattice and 3 for the honeycomb lattice.
				- ((651bd24b-e12c-4fef-9016-83ffb28b58bb))
			- When $\nu=1$, $q=0,\gamma_m=3$, thus no second term.
		- Perturbation to the gapless phase
			- $$
			  H^{\prime}=-\kappa \sum_{\circlearrowright\langle i j k\rangle_{\gamma \gamma^{\prime}}}\left(\Gamma_i^\gamma \Gamma_j^{\gamma \gamma^{\prime}} \Gamma_k^{\gamma^{\prime}}-\sum_{\beta=\gamma_{\mathrm{m}}+1}^{2 q+3} \Gamma_i^{\beta \gamma} \Gamma_j^{\gamma \gamma^{\prime}} \Gamma_k^{\gamma^{\prime} \beta}\right)
			  $$
				- $\circlearrowright\langle i j k\rangle_{\gamma \gamma^{\prime}}$ refers to the clockwise summation over three sites within the same plaquette such that $i$ and $j$ ( $j$ and $k$ ) are connected via a link of type $\gamma\left(\gamma^{\prime}\right)$.
			- In the majorana representation it reads
			  $$
			  \tilde{H}^{\prime}=\kappa \sum_{\circlearrowright\langle i j k\rangle_{\gamma \gamma^{\prime}}} u_{i j} u_{j k}\left(i c_i c_k+\sum_{\beta=\gamma_{\mathrm{m}}+1}^{2 q+3} i b_i^\beta b_k^\beta\right)
			  $$
				- Again second-nearest hopping.
	- ## Solution
		- Majorana transformation
			- $$
			  \Gamma_j^\alpha=i b_j^\alpha c_j, \quad \Gamma_j^{\alpha \beta}=i b_j^\alpha b_j^\beta
			  $$
				- $$
				  \alpha=1, \ldots, 2 q+3
				  $$
			- $$
			  D_j \equiv i^{q+2} b_j^1 b_j^2 \cdots b_j^{2 q+3} c_j=-1
			  $$
			- Then
			  $$
			  \tilde{H}=\sum_{\langle i j\rangle_\gamma} J_\gamma u_{i j}\left(i c_i c_j+\sum_{\beta=\gamma_{\mathrm{m}}+1}^{2 q+3} i b_i^\beta b_j^\beta\right)
			  $$
				- $$
				  u_{i j}=i b_i^\gamma b_j^\gamma
				  $$
			- The solution is completely analogous to the original model.
- # Characterization of Topo Orders
	- Two features: GSD and topological spin
	- Topo spin
	  collapsed:: true
		- Still using boundary CFT
		- Key formula: For two different sectors on a finite boundary,
		  $$E_a-E_0=\frac{2\pi v}{L_1}(h_a+h_{\bar a})$$
			- Citing big yellow book
			- $a$ labels a primary field ( $\bar{a}$ being its conjugate)
			- $h_a$ is the conformal weight of this field (with $h_a=h_{\bar{a}}$ )
			- $v$ is velocity of the CFT.
		- The topological spin of the anyon is related to $h_a$ via $\theta=2 \pi h_a$.
		- $v$ is extracted from the linear dispersion of the edge spectrum.
- # Ground-State Degeneracy
	- In short, we examine the total fermion parity and discard the states with wrong fermion parities.
	  collapsed:: true
		- In the language of gauge constraints, $\prod_j D_j$ and $1$ generate the same gauge field configuration.
		  But if $\prod_j D_j |\psi\rangle$ and $1 |\psi\rangle$ cancel, then the state doesn't survive the projection.
	- ## Setup
		- PBC and APBC
		  collapsed:: true
			- PBC: The gauge choice of all $u=-1$
			- APBC: Flipping the signs of all $u$ along an open path.
			- ((651cd9b2-d863-4fbf-a298-39e89e07a161))
				- Flipping all $u$ on the grey path creates APBC in the $n_1$ direction.
		- We require that both $L_x$ and $L_y$ of the torus be even.
			- However, this requirement seems unjustified. Could we allow tori of odd lengths?
		- $$
		  c_{\mathbf{k}, s}=\sqrt{\frac{1}{2 N}} \sum_j c_{j, s} e^{-i \mathbf{k} \cdot \mathbf{R}_j}
		  $$
			- $$
			  c_{-\mathbf{k}, s}=c_{\mathbf{k}, s}^{\dagger}
			  $$
		- Time-reversal (TR) invariant points
			- They will need special care!
			- $$\mathbf{k}=-\mathbf{k}+\mathbf{G}$$
				- $G$ is a reciprocal lattice vector
			- For the TR-invariant points, one has $c_{-\mathbf{k}, s}=c_{\mathbf{k}, s}^{\dagger}=c_{\mathbf{k}, s}$ and $\left(c_{\mathbf{k}, s}\right)^2=1 / 2$.
				- The latter is very interesting. Let me try to prove it.
				- $$\begin{aligned}
				  ( c_{\mathbf{k} ,s})^{2} & =\frac{1}{2N}\sum _{j,l} c_{j,s} c_{l,s} e^{-i\mathbf{k} \cdot (\mathbf{R}_{j} +\mathbf{R}_{l})}\\
				   & =\frac{1}{2N}\sum _{j}( c_{j,s})^{2} e^{-2i\mathbf{k} \cdot \mathbf{R}_{j}}\\
				   & =\frac{1}{2N}\sum _{j} e^{-2i\mathbf{k} \cdot \mathbf{R}_{j}}
				  \end{aligned}$$
				- The problem is at the Fourier transformation. Is it always zero?
				-
				- As a simpler case, let's consider $\sum_n e^{ina}=\sum_n (e^{ia})^n$.
					- If $e^{ia}$ is a general complex number, the sum is zero.
					- However, when $e^{ia}$ is real, the sum could become nontrivial!
				- The requirement $\mathbf{k}=-\mathbf{k}+\mathbf{G}$ is similar to the reality condition, since $k \to -k$ is taking the complex conjugate and $e^{iGR_j}=1$.
				-
				-
			- Tt could be rescaled to define a Majorana mode $\tilde{c}_{\mathbf{k}, s}=\sqrt{2} c_{\mathbf{k}, s}$ satisfying $\left(\tilde{c}_{\mathbf{k}, s}\right)^2=1$.
	-
	- Fermion parity in a unit cell:
	  collapsed:: true
	  $$
	  \begin{aligned}
	  & \left(i b_{\mathrm{A}}^1 b_{\mathrm{B}}^1\right)\left(i b_{\mathrm{A}}^2 b_{\mathrm{B}}^2\right) \ldots\left(i b_{\mathrm{A}}^{2 q+3} b_{\mathrm{B}}^{2 q+3}\right)\left(i c_{\mathrm{A}} c_{\mathrm{B}}\right) \\& =(-1)^q\left(i^{q+2} b_{\mathrm{A}}^1 b_{\mathrm{A}}^2 \ldots b_{\mathrm{A}}^{2 q+3} c_{\mathrm{A}}\right)\left(i^{q+2} b_{\mathrm{B}}^1 b_{\mathrm{B}}^2 \ldots b_{\mathrm{B}}^{2 q+3} c_{\mathrm{B}}\right) \\
	  & =(-1)^q .
	  \end{aligned}
	  $$
		- Note that 
		  $$
		  i^{q+2} b^1 b^2 \ldots b^{2 q+3} c=-1
		  $$
	- Therefore the total fermion parity must be **even** since we required even lengths, thus even number of sites.
	-
	- The total fermion parity could be factored into two parts:
	  collapsed:: true
	  $$
	  Q=Q_1 Q_2
	  $$
		- $Q_1$ is the parity for itinerant fermions:
		  $$
		  Q_1=\left\{\begin{array}{l}
		  \prod_j\left(i b_{j, \mathrm{~A}}^5 b_{j, \mathrm{~B}}^5\right) \cdots\left(i b_{j, \mathrm{~A}}^{2 q+3} b_{j, \mathrm{~B}}^{2 q+3}\right)\left(i c_{j, \mathrm{~A}} c_{j, \mathrm{~B}}\right) \quad \text { for square lattice } \\
		  \prod_j\left(i b_{j, \mathrm{~A}}^4 b_{j \mathrm{~B}}^4\right) \cdots\left(i b_{j, \mathrm{~A}}^{2 q+3} b_{j, \mathrm{~B}}^{2 q+3}\right)\left(i c_{j, \mathrm{~A}} c_{j, \mathrm{~B}}\right) \quad  
		   \text { for honeycomb lattice } \\
		  \end{array}\right.
		  $$
		- $Q_2$ is the parity for gauge fields:
		  $$Q_2=\left\{\begin{array}{l}\prod_j\left(i b_{j, \mathrm{~A}}^1 b_{j, \mathrm{~B}}^1\right) \cdots\left(i b_{j, \mathrm{~A}}^4 b_{j, \mathrm{~B}}^4\right) \quad \text { for honeycomb lattice }\\
		   \prod_j\left(i b_{j, \mathrm{~A}}^1 b_{j, \mathrm{~B}}^1\right) \cdots\left(i b_{j, \mathrm{~A}}^3 b_{j, \mathrm{~B}}^3\right) \quad \text { for square lattice } \\ \end{array}\right.$$
		- Recall that
		  $$
		  \tilde{H}=\sum_{\langle i j\rangle_\gamma} J_\gamma u_{i j}\left(i c_i c_j+\sum_{\beta=\gamma_{\mathrm{m}}+1}^{2 q+3} i b_i^\beta b_j^\beta\right)
		  $$
			- $$
			  u_{i j}=i b_i^\gamma b_j^\gamma
			  $$
	- ## Parity of itinerant fermions
	- ## Parity of Gauge Field
		- The conclusion is that it is always even.
	-
	- ## Conclusion
		- $$
		  \begin{aligned}
		  & Q\left|\Psi_F\left(\left\{u_0^{--}\right\}\right)\right\rangle \otimes\left|\left\{u_0^{--}\right\}\right\rangle=\left|\Psi_F\left(\left\{u_0^{--}\right\}\right)\right\rangle \otimes\left|\left\{u_0^{--}\right\}\right\rangle \\
		  & Q\left|\Psi_F\left(\left\{u_0^{-+}\right\}\right)\right\rangle \otimes\left|\left\{u_0^{-+}\right\}\right\rangle=\left|\Psi_F\left(\left\{u_0^{-+}\right\}\right)\right\rangle \otimes\left|\left\{u_0^{-+}\right\}\right\rangle \\
		  & Q\left|\Psi_F\left(\left\{u_0^{+-}\right\}\right)\right\rangle \otimes\left|\left\{u_0^{+-}\right\}\right\rangle=\left|\Psi_F\left(\left\{u_0^{+-}\right\}\right)\right\rangle \otimes\left|\left\{u_0^{+-}\right\}\right\rangle \\
		  & Q\left|\Psi_F\left(\left\{u_0^{++}\right\}\right)\right\rangle \otimes\left|\left\{u_0^{++}\right\}\right\rangle=(-1)^\nu\left|\Psi_F\left(\left\{u_0^{++}\right\}\right)\right\rangle \otimes\left|\left\{u_0^{++}\right\}\right\rangle
		  \end{aligned}
		  $$
		- Thus the $++$ boundary condition (all $u=1$) doesn't survive the symmetrization!