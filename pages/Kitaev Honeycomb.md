# Refs
	- [[2006_Kitaev_Anyons in an exactly solved model and beyond]]
- # Problems and Questions #card
  card-last-interval:: 31.26
  card-repeats:: 1
  card-ease-factor:: 2.36
  card-next-schedule:: 2023-08-29T18:28:51.208Z
  card-last-reviewed:: 2023-07-29T12:28:51.208Z
  card-last-score:: 3
  collapsed:: true
	- ## Unsolved
		- The honeycomb seems the only known frustrated model to exhibit topological order. Could we extend it?
			- Would anyonic operators be the key?
			- Or some comparison to Levin-Wen, which is frustration-free?
		- The local Hilbert space is 2D and can well be encapsulated by a single fermionic mode. Why bother embedding it into a 4D space?
		  id:: 64c27e7e-e01d-45b9-accc-c06dfd136c42
		  collapsed:: true
			- Aesthetic viewpoint
			  collapsed:: true
				- Quantize as two modes preserve the 'equality' between spin-up and spin-down.
				- $X=c_1,Y=c_2$ while $Z=ic_1 c_2$, which is unsymmetric and ugly.
			- Commutation Relations
			  collapsed:: true
				- If we quantize a single qubit, it would have two majorana operators with $c_1=\sigma^X$ and $c_2=\sigma^Y$.
				  However, Pauli operators at different sites could then **anti-commute**, which is unacceptable.
			- But why does the embedding work?
		- It seems exchanging two majorana operators always incur -1. Why do we call it 'nonabelian anyons'?
		  collapsed:: true
			- It is claimed that ((64cdaf2b-8ee3-468a-b16e-f7c2f1bb30f3)) and the proof is beautiful. Read it.
			  collapsed:: true
			- Another viewpoint is the boundary CFT and chiral edge modes, which implies nontrivial bulk CFT.
			- Topobook ((64c2810d-1950-4c85-9460-2bf755f46683)).
			  collapsed:: true
				- #+BEGIN_TIP
				  Lots of relevant thoughts in the exercise!
				  #+END_TIP
				- The operator of braiding two anyons is 
				  $$U_{ij}=\frac {e^{i\alpha}} {\sqrt 2} [1+\gamma_i\gamma_j]$$
				- We can verify the $U_{ij}$ indeed form a rep of braid group.
				  collapsed:: true
					- Hint: It is the **unitary operators** that form a braiding group. Not commutation relations of the anyon operators themselves.
	- ## Solved
		- What does 'gauge' mean in the model?
			- It means that different configurations are related by $D_j$, the gauge transformatiom operators.
			  Thus the related configurations are equivalent in a sense.
			- What is the ((64b59d7c-e86b-44d0-8f85-1c3052d9b4e2))?
		- Is the system bosonic or fermionic? -- Fermionic.
			- This determines what is considered **local**.
			- We introduced a set of operators satisfying CCR (or CAR) in the Hilbert space.
			  collapsed:: true
				- We required the operators at different sites to anti-commute for simplicity, i.e. to have ((64b44bb7-1b1b-4fda-9690-8018ad7cb6c1))
			- To go between CCR and CAR we need a highly-nonlocal transformation (i.e. second step of [[Jordan-Wigner Transformation]]).
				- On the other hand, the step from fermionic operators to majorana representations is local.
			-
- # Setup
  collapsed:: true
	- ((64b2f4f6-a87c-4d76-93a6-e29234589b11))
	  collapsed:: true
		- The lattice could be divided into 2 classes.
		- Each unit cell contains two vertices, i.e. one white and one black.
	- collapsed:: true
	  $$
	  H=-J_x \sum_{x \text {-links }} \sigma_j^x \sigma_k^x-J_y \sum_{y \text {-links }} \sigma_j^y \sigma_k^y-J_z \sum_{z \text {-links }} \sigma_j^z \sigma_k^z
	  $$
		- It's often beneficial to consider the general setting!
	- We embed the 2D space of each spin into a 4D space.
	- Extended space $\tilde M$
	  collapsed:: true
		- The dimension is 4 since each mode (spin-up and spin-down) can be occupied or unoccupied.
		- The physical space is 2D since the occupation number must be 1.
	- Majorana operators $b^x, b^y, b^z$, $c$
	  collapsed:: true
		- Note that two majorana operators corresponds to a fermionic mode.
	- Physical space $M$
	  collapsed:: true
		- Defined by $|\xi\rangle \in \mathcal{M}$ if and only if $D|\xi\rangle=|\xi\rangle$ where $D=b^x b^y b^z c$
	- Extended Pauli Operators
		- $$
		  \widetilde{\sigma}^x=i b^x c, \quad \widetilde{\sigma}^y=i b^y c, \quad \widetilde{\sigma}^z=i b^z c .
		  $$
		- Proposition. (i) They preserve the physical space. (ii) restrictions obey the same commutation relations as Pauli operators.
			- (i) They all commute with $D$.
			- (ii) They indeed anticommute with each other.
		- Note
			- They don't require anti-commutation between different sites.
	- Link operators
	  collapsed:: true
		- $$ \hat{u}_{j k}=i b_j^{\alpha_{j k}} b_k^{\alpha_{j k}}$$
	- Plaquette operators
	  collapsed:: true
		- $$
		  w_p=\prod_{(j, k) \in \operatorname{boundary}(p)} u_{j k} \quad(j \in \text { even sublattice, } k \in \text { odd sublattice })
		  $$
	- ## Notations
	  collapsed:: true
		- Check operators
		  $$
		  K_{j k}= \begin{cases}\sigma_j^x \sigma_k^x, & \text { if }(j, k) \text { is an } x \text {-link; } \\ \sigma_j^x \sigma_k^y, & \text { if }(j, k) \text { is an } y \text {-link } \\ \sigma_j^x \sigma_k^z, & \text { if }(j, k) \text { is an } z \text {-link }\end{cases}
		  $$
		- Plaquette operators
		  $$
		  W_p=\sigma_1^x \sigma_2^y \sigma_3^z \sigma_4^x \sigma_5^y \sigma_6^z=K_{12} K_{23} K_{34} K_{45} K_{56} K_{61}
		  $$
			- ((64b2f58e-6dcc-4ad7-ad98-5226751aebbb))
			- Note that it commutes with any check.
- # Solution
	- Strategy
		- ((64b2f633-ff39-4862-92e9-a8827906ea71))
		- ((64b4a3a2-5a8e-4828-8059-2d5fdb0ec212))
		- ((64b442f1-bf2d-40cd-926a-9629bc86763d))
	- Summary #card
	  collapsed:: true
		- First, transform to the majorana representation and the extended space.
			- The lattice system is not essentially fermionic.
			  ((64b48b82-84da-4b28-83de-30ce1ef5338a))
			- Therefore we **introduced** a set of convenient operators (satisfying some rather strong CAR) to simplify the solution!
		- After recasting the Hamiltonian in the extended form, we can find lots of **conserved quantities** $u_{jk}$.
		- Thus we can use their eigenvalues to simplify the solution. Moreover, any combination of eigenvalues exist.
	-
	- ## Basic Properties
	  collapsed:: true
		- $D$ anticommutes with any single majorana operator.
		- $D^2=1$ and the $+1$ and $-1$ multiplicities are equal.
		  collapsed:: true
			- The second properties follows anticommutation.
		- $\widetilde{\sigma}^\alpha(\alpha=x, y, z)$ commutes with $D$ (so that $\mathcal{M}$ is preserved).
		- $\left(\widetilde{\sigma}^\alpha\right)^{\dagger}=\widetilde{\sigma}^\alpha,\left(\widetilde{\sigma}^\alpha\right)^2=1$, and
		  $$
		  \widetilde{\sigma}^x \widetilde{\sigma}^y \widetilde{\sigma}^z=i b^x b^y b^z c=i D
		  $$
			- The last equation is consistent with the formula $\sigma^x \sigma^y \sigma^z=i$ because $D$ acts as the identity operator on the subspace $\mathcal{M}$.
		-
	- ## Extended Hamiltonian
	  collapsed:: true
		- The idea is to replace the Pauli operators by the extended Pauli operators.
		- $$
		  \begin{aligned}
		   \widetilde{H}=\frac{i}{4} \sum_{j, k} \hat{A}_{j k} c_j c_k, \quad \hat{A}_{j k} & =\left\{\begin{array}{cl}
		  2 J_{\alpha_{j k}} \hat{u}_{j k} & \text { if } j \text { and } k \text { are connected } \\
		  0 & \text { otherwise}
		  \end{array}\right. \\
		  & \hat{u}_{j k}=i b_j^{\alpha_{j k}} b_k^{\alpha_{j k}} \\
		  &
		  \end{aligned}
		  $$
			- $\alpha_{jk}$ takes value in $x,y,z$.
			- The reason is 
			  $$
			  \widetilde{K}_{j k}=\left(i b_j^\alpha c_j\right)\left(i b_k^\alpha c_k\right)=-i\left(i b_j^\alpha b_k^\alpha\right) c_j c_k
			  $$
			- Notes
				- $u_{jk}=-u_{kj}$
				- Each edge is counted twice, so the prefactor is $1/4$.
				- We keep $i$ in $u_{jk}$ to ensure $u_{jk}^2=1$, which would be quite convenient.
				- If we use the combination $b_j^\alpha c_j$, then $b_j^\alpha c_j$ and $b_j^\beta c_j$ anti-commute, which is undesirable.
				  Thus we use another combination.
		- A beautiful diagrammatic representation:
		  collapsed:: true
		  ((64b44b79-886b-4eb4-ad32-9158770a65fa))
			- ((64b44b9c-9c41-4142-a64e-968b5e4dbe19))
	- ## Construct Solutions
	  collapsed:: true
		- Observation. (i) $u_{jk}$ commute with each other (ii) $u_{jk}$ commute with the Hamiltonian!
		  id:: 64b44bb7-1b1b-4fda-9690-8018ad7cb6c1
		  collapsed:: true
			- (i) Different $u$ have two anti-commutations.
			- (ii) $u_{jk}$ commutes with any $c_jc_k$.
		- Propositon. (i) $u_{jk}^2=1$, thus the eigenvalues are $\pm 1$. (ii) All combination of eigenvalues of $u_{jk}$ exist.
		  collapsed:: true
			- (ii) We can use $b^{\alpha_{jk}}_k$ (or $b^{\alpha_{jk}}_j$) to flip the eigenvalue of $u_{jk}$ without affecting others.
		- Split of the space into eigenspaces of $u$:
		  id:: 64b5994d-9ffd-446d-9084-6d09b7d60d38
		  collapsed:: true
			- $$
			  \widetilde{\mathcal{L}}=\bigoplus_u \widetilde{\mathcal{L}}_u
			  $$
			- $u$ stands for the collection of all $u_{j k}$.
			- The restriction of Hamiltonian to the subspace $\widetilde{\mathcal{L}}_u$ is by 'removing hats'
		-
		- Notes
		  collapsed:: true
			- $c_i c_j$ and $c_j c_k$ **do not commute**, thus it is improper to write down a 'majorana representation' yet.
			- The subspace $\tilde {\mathcal L}_u$ isn't gauge invariant (eigen to $D_j$).
		- Therefore we perform the **symmetrization** again:
		  collapsed:: true
		  $$
		  \left|\Psi_w\right\rangle=\prod_j\left(\frac{1+D_j}{2}\right)\left|\widetilde{\Psi}_u\right\rangle
		  $$
			- $w$ denotes the equivalence class of $u$.
		- What are the equivalence classes?
		  collapsed:: true
			- $D_j$ flips the three adjacent $u_{jk}$, i.e. add a loop of plaquettes.
				- Rephrased, it preserves the plaquette eigenvalues
			- Therefore we can use the eigenvalues of the plaquette operators $w_p= \pm 1$ and the homotopy class to denote the equivalence class.
		-
	- ## Solve the Spectrum of the Quadratic Hamiltonian
		- Observations
			- A gauge transformation $D_j$ flip all three adjacent $u$ while keeping $w_p$ and $H$ invariant.
				- Therefore we need only solve in a specific gauge configuration and use $D_j$ to superpose all equivalent configurations.
			- When the system is put on the torus, there can be inequivalent configurations corresponding to the same $\{w_p\}$.
			- The ground state is vortex-free, i.e. all $w_p=1$.
			-
		- Step 1. Analyze the quadratic Hamiltonian
		  collapsed:: true
			- collapsed:: true
			  $$
			  H(A)=\frac{i}{4} \sum_{j, k} A_{j k} c_j c_k
			  $$
				- $A$ is a real anti-symmetric matrix of size $m=2N$, encoding the eigenvalues of $\{u_{jk}\}$.
				- Proposition. The prefactor satisfies $[-i H(A),-i H(B)]=-i H([A, B])$, thus the Lie algebra is isomorphic to $\mathfrak{so}(2m)$. #card
					- The proof is not hard.
						- To make $c_jc_k$ and $c_l c_m$ anti-commute, we must identify a pair.
						- On the other hand, elements of $\mathfrak{so}(2m)$ are precisely anti-symmetric real matrices.
					- However, why should we care about the fact?
					  background-color:: yellow
						- Maybe it is always a good thing to note the underlying structure.
			- The strategy of solution is reducing it to a 'canonical form'
			  collapsed:: true
			  $$
			  H_{\text {canonical }}=\frac{i}{2} \sum_{k=1}^m \varepsilon_k b_k^{\prime} b_k^{\prime \prime}=\sum_{k=1}^m \varepsilon_k\left(a_k^{\dagger} a_k-\frac{1}{2}\right), \quad \varepsilon_k \geqslant 0
			  $$
				- $b_k^{\prime}, b_k^{\prime \prime}$ are called **normal modes** and $a_k^{\dagger}=\frac{1}{2}\left(b_k^{\prime}-i b_k^{\prime \prime}\right), a_k=\frac{1}{2}\left(b_k^{\prime}+i b_k^{\prime \prime}\right)$ are the corresponding creation and annihilation operators.
				- Q: All majorana operators are on an equal footing, so what's special about the form?
				  background-color:: pink
					- Here the operators are paired up and each pair appears exactly once.
			- Thus we should find an orthogonal transformation to make $A$ quasi-diagonal, i.e.
			  collapsed:: true
			  $$
			  \begin{gathered}
			  \left(b_1^{\prime}, b_1^{\prime \prime}, \ldots, b_m^{\prime}, b_m^{\prime \prime}\right)=\left(c_1, c_2, \ldots, c_{2 m-1}, c_{2 m}\right) Q, \quad Q \in \mathrm{O}(2 m), \\
			  A=Q\left(\begin{array}{ccccc}
			  0 & \varepsilon_1 & & & \\
			  -\varepsilon_1 & 0 & & & \\
			  & & \ddots & & \\
			  & & & 0 & \varepsilon_m \\
			  & & & -\varepsilon_m & 0
			  \end{array}\right) Q^T .
			  \end{gathered}
			  $$
				- Why should $Q$ be orthogonal?
					- We can use $\{c_m,c_n\}=2\delta_{mn}$.
			- The ground state has every occupation number zero, thus the energy is
			  collapsed:: true
			  $$
			  E=-\frac{1}{2} \sum_{k=1}^m \varepsilon_k=-\frac{1}{4} \operatorname{Tr}|i A|
			  $$
				- The function $|\cdot|$ acts on the **eigenvalues**, the eigenvectors being fixed. (In fact, any function of a real variable can be applied to Hermitian matrices.)
				- The factor is $1/2$ rather than $1/4$ since each mode is counted twice by the anti-symmetric matrix.
		- Step 2. Perform Fourier transformation to make use of translation invariance
			- We study the configuration where all $u=1$.
			- $$
			  \begin{gathered}
			  H=\frac{1}{2} \sum_{\mathbf{q}, \lambda, \mu} i \widetilde{A}_{\lambda \mu}(\mathbf{q}) a_{-\mathbf{q}, \lambda} a_{\mathbf{q}, \mu}, \quad \widetilde{A}_{\lambda \mu}(\mathbf{q})=\sum_t e^{i\left(\mathbf{q}, \mathbf{r}_t\right)} A_{0 \lambda, t \mu} \\
			  a_{\mathbf{q}, \lambda}=\frac{1}{\sqrt{2 N}} \sum_s e^{-i\left(\mathbf{q}, \mathbf{r}_s\right)} c_{s \lambda}
			  \end{gathered}
			  $$
				- $(s,\lambda)$ denotes the sites, where $s$ is the unit cell and $\lambda$ is the position inside the cell.
				- The basis of the translation group is selected as ((64c2c028-bfa3-41b9-bc70-d5f70b943a13))
				- Note that $a_{\mathbf{q}, \lambda}^{\dagger}=a_{-\mathbf{q}, \lambda}$ and $\{a_{\mathbf{p}, \mu}, a_{\mathbf{q}, \lambda}^{\dagger}\}=\delta_{\mathbf{p q}} \delta_{\mu \lambda}$, thus the definition of creation and annihilation operators makes sense.
					- However, note that $p$ and $-p$ are intertwined.
				-
		- Result:
		  $$
		  \begin{gathered}
		  i \widetilde{A}(\mathbf{q})=\left(\begin{array}{cc}
		  0 & i f(\mathbf{q}) \\
		  -i f(\mathbf{q})^* & 0
		  \end{array}\right), \quad \varepsilon(\mathbf{q})= \pm|f(\mathbf{q})|, \\
		  f(\mathbf{q})=2\left(J_x e^{i\left(\mathbf{q}, \mathbf{n}_1\right)}+J_y e^{i\left(\mathbf{q}, \mathbf{n}_2\right)}+J_z\right),
		  \end{gathered}
		  $$
			- Diagonalization
			  id:: 64e4c247-88fb-4f65-a2dc-612c882c026d
				- Consider
				  collapsed:: true
				  $$\begin{aligned}
				  M & =\begin{bmatrix}
				  0 & x\\
				  x^{*} & 0
				  \end{bmatrix} ,u=\left(\begin{array}{ c }
				  1\\
				  a
				  \end{array}\right)\\
				  Mu & =\left(\begin{array}{ c }
				  xa\\
				  x^{*}
				  \end{array}\right)\\
				  \end{aligned}$$
					- Note that we **cannot** directly write $a_{\pm}=\pm \sqrt{\frac {x^*} x}$.
				- Sign problem of the square root
				  collapsed:: true
					- In short, when taking $f(p) \to -f(p)$, the eigenvectors shall not change but the eigenvalues should obtain a minus.
					  This is not reflected if we write $\lambda_{\pm} = \pm \sqrt{x^* x}$.
				- Take a concrete route: Write $x=re^{i\theta}$.
					- $$\begin{align*}
					  x & =re^{i\theta }\\
					  a^{2} & =\frac{x^{*}}{x} =e^{-2i\theta }\\
					  a_{+} & =e^{-i\theta } =\frac{x^{*}}{|x|} ,\lambda _{+} =r=|x|\\
					  a_{-} & =-e^{-i\theta } =-\frac{x^{*}}{|x|} ,\lambda _{-} =-r
					  \end{align*}$$
					-
				-
			- Pluggin in $x=if(p)$,
			  $$\begin{align*}
			  b_{p,\pm }^{\dagger } & =\frac{1}{\sqrt{2}}\left( a_{p,1}^{\dagger } \pm {\frac{-if^{*}( p)}{|f( p)|}} a_{p,2}^{\dagger }\right)
			  \end{align*}$$
		- Note that we don't need a chemical potential to decides which states are occupied here, since the eigenenergies are **absolute**.
			- i.e. The modes with $\varepsilon < 0$ are occupied and those with $\varepsilon > 0$ are not.
		- Is the phase gapless?
		  collapsed:: true
			- 'Gapless' means we can find a $\mathbf{q}$ such that $f(\mathbf{q})=0$
			- Prop. The equation has solutions iff 
			  $$
			  \left|J_x\right| \leqslant\left|J_y\right|+\left|J_z\right|, \quad\left|J_y\right| \leqslant\left|J_x\right|+\left|J_z\right|, \quad\left|J_z\right| \leqslant\left|J_x\right|+\left|J_y\right| .
			  $$
				- Obviously it is necessary.
				- Sufficient: We can both adjust the amplitude and direction of $q$ to obtain any combination of phases.
			-
		- ((64c2c17e-d382-461c-8c36-d7caf82af369))
- # Alternative Solution: [[Jordan-Wigner Transformation]]
  collapsed:: true
	- See [[2016_Kitaev honeycomb tensor networks]]
	-
- # Properties of the Gapped Phase
	- Kitaev uses perturbation theory -- and he doesn't see this as something problematic!
	  card-last-interval:: 32.57
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2023-09-11T01:50:31.337Z
	  card-last-reviewed:: 2023-08-09T12:50:31.337Z
	  card-last-score:: 5
	  id:: 64c2c2a2-6905-4877-870f-dcaf68bb8bf0
- # The View of Gauge Theory
  collapsed:: true
	- $D_j$ are gauge transformation operators.
		- Physical <-> Invariant under $D_j$ <-> Equal superposition of equivalent configurations
	- The variables $u_{k j}$ are a $\mathbb{Z}_2$ gauge field.
	- $w_p$ corresponds to the magnetic flux.
	- ## Def
		- Fermionic path operator
			- $$
			  W\left(j_0, \ldots, j_n\right)=K_{j_n j_{n-1}} \ldots K_{j_1 j_0}=\left(\prod_{s=1}^n-i \hat{u}_{j_s j_{s-1}}\right) c_n c_0
			  $$
			- Since it could be defined in terms of spins, it is manifestly gauge invariant.
			- If the path is closed, the operator is a [[Wilson Loop]]
	- ## Time-Reversal Operator
	  id:: 64b59d7c-e86b-44d0-8f85-1c3052d9b4e2
	  collapsed:: true
		- The time-reversal operator is a conjugate-linear unitary operator $T$ such that
		  $$
		  T \sigma_j^\alpha T^{-1}=-\sigma_j^\alpha, \quad T b_j T^{-1}=b_j, \quad T c_j T^{-1}=c_j .
		  $$
			- See ((64b5a006-d313-41a7-a875-e5bec6e3b0cd))
		- Therefore $T$ commutes with the Hamiltonian and the Wilson loop.
		- Multiplying the equation $W_l|\Psi\rangle=w_l|\Psi\rangle$ by $T$, we get $W_l T|\Psi\rangle=w_l^* T|\Psi\rangle$.
			- For the honeycomb all eigenvalues are real, so TRS isn't broken.
			- However for non-bipartite graphs, e.g. triangles, $T$ **does not** preserve the field configuration, which incurs a symmetry-protected degeneracy.
			-