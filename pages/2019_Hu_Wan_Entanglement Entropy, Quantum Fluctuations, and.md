- ![2019_Hu_Wan_Entanglement Entropy, Quantum Fluctuations, and.pdf](file://zotero_link/Research/Undergrad Thesis/2019_Hu_Wan_Entanglement Entropy, Quantum Fluctuations, and.pdf)
- # BlackBoxes
	- Fusion basis
	  id:: 658e8ba6-1b94-4444-8aee-bf614de7f002
		- To open the blackbox, I need to refer to Kitaev's quantum double paper (and Simon's topobook) to find out quasi-particles in QD.
	- ((658e9738-e5ce-4a72-b67a-9f4949c46f2b))
- # Setup
  collapsed:: true
	- We restrict to states with trivial holonomy, i.e. $$B_p=1$$ for all p.
	- Holonomy basis
	  id:: 658e3328-d79d-4351-b526-e5c759d904ed
	  collapsed:: true
		- The basis of $\mathcal{H}^{B_p=1}$ is labeled by values of Wilson lines,
		  $$
		  \left\{\left|g_v ; g_\alpha\right\rangle\right\}
		  $$
		- The non-local transformation: for any path $p$ connecting $v_0$ to $v$, we define
		  $$
		  g_p:=\prod_{e \in p_{v v_0}} a_e
		  $$
		  i.e. the Wilson line.
			- Notes
				- In the trivial-holonomy subspace, homotopic paths give equal group elements.
				- Group elements could be restored from paths,
				  $$
				  \left\{a_e\right\} \cong\left\{g_v ; g_\alpha\right\}_{v \neq v_0}
				  $$
					- $g_\alpha$ denotes elements on nontrivial loops.
	- ((658e8ba6-1b94-4444-8aee-bf614de7f002))
	  id:: 658e8a79-79ae-4d3e-9608-13ec9f614f3c
		- The idea is to transform from group elements to representations.
			- Note that representations label flux quasi-particles.
		- collapsed:: true
		  $$
		  |j m n\rangle=\sqrt{\frac{d_j}{|G|}} \sum_{g \in G} \overline{\rho_{m n}^j(g)}|g\rangle
		  $$
			- Note
				- The transformation is unitary and invertible.
				- As a piece of evidence, $|G|=\sum_i d_i^2$, thus the dimensions of LHS and RHS match.
				-
			- $j$ labels the irrep.
			- $m,n$ are matrix indices.
			- From orthogonality, the inverse transformation is
			  $$
			  |g\rangle=\sqrt{\frac{d_j}{|G|}} \sum_{j m n} \rho_{m n}^j(g)|j m n\rangle
			  $$
		- Perform the transformation on each site of EB, we have
		  ((658e88ff-f635-435f-a718-12083aacc17e))
			- $$
			  \begin{aligned}
			  & \left|j_1 m_1, j_2 m_2, \ldots, j_L m_L ; \eta\right\rangle \\
			  := & \sum_{n_1, n_2, \ldots, n_L} T_{j_1 n_1, j_2 n_2, \ldots, j_L n_L}^\eta\left|j_1 m_1 n_1, j_2 m_2 n_2, \ldots, j_L m_L n_L\right\rangle,
			  \end{aligned}
			  $$
			- $T$ is a tensor invariant under representations of $G$,
			  $$
			  \sum_{n_i^{\prime}} \rho_{n_i n_i^{\prime}}^{j_i} T_{j_1 n_1, j_2 n_2, \ldots, j_i n_i^{\prime}, \ldots, j_L n_L}^\eta=T_{j_1 n_1, j_2 n_2, \ldots, j_i n_i, \ldots, j_L n_L}^\eta
			  $$
			- $\eta$ labels DOFs on internal lines, i.e. DOFs absorbed by the tensor.
		-
- # ((658e2d9a-a4b1-4395-85b5-3aef350caa65))
  collapsed:: true
	- Main result
		- ((658e2dad-f1ec-4e64-af79-e0b9f1e5f3b8))
	- Picture
		- ((658e2dd5-11ac-41ad-b382-cf1dceb299b8))
		- After tracing out region B, region A seems a physical boundary bursting with quasi-particles.
- # ((658e2f1f-4d32-420c-a067-d02c041d527a))
  collapsed:: true
	- First, briefly review QD and TC.
	- Then we define the ((658e3328-d79d-4351-b526-e5c759d904ed)).
	- Proposition. In the basis, 
	  collapsed:: true
	  $$
	  \begin{align*}
	  A_v\left|g_1, \ldots, g_v, \ldots, g_{V-1} ; g_\alpha\right\rangle & =\frac{1}{|G|} \sum_h\left|g_1, \ldots, h g_v, \ldots, g_{V-1} ; g_\alpha\right\rangle \\
	  A_{v_0}\left|g_1, \ldots, g_{V-1} ; g_\alpha\right\rangle & =\frac{1}{|G|} \sum_h\left|g_1 h^{-1}, \ldots, g_{V-1} h^{-1} ; h g_\alpha h^{-1}\right\rangle
	  \end{align*}
	  $$
	  where $v_0$ is the basis point.
		- The convention of $A_v$ is
		  ((658e6b4e-9a2d-428e-be8b-53777dcd3283))
		  but the convention of the holonomy basis is outgoing.
- # ((658e6b7c-ab60-4ca6-b864-e44c66943735))
	- Here we examine EE on a sphere.
	- We select two basis points in each region and label the basis by Wilson lines from these points:
	  collapsed:: true
	  ((658e6c1f-47f8-4999-803f-b92317efd2a8))
		- $$
		  g_1^{\prime-1} g_1=g_2^{\prime-1} g_2=\cdots=g_L^{\prime-1} g_L
		  $$
		- It is equivalent to selecting $v_A$ as the basis point and specifying $g_1, g_2, ..., g_L; g_{v_B}$. Nothing new.
	-
	- ## Ground state and reduced density matrix
		- Proposition. The ground state is
		  collapsed:: true
		  $$
		  \begin{aligned}
		  |\Phi\rangle & =\sum_{g_1, \ldots, g_L, h}\left|g_1 h, \ldots, g_L h ; g_1, \ldots, g_L\right\rangle \\
		  & \equiv \sum_{g_v, h}\left|g_v h ; g_v\right\rangle
		  \end{aligned}
		  $$
			- To obtain the ground state, we can use the symmetrization technique, i.e. act on any basis element by all vertex operators:
			  collapsed:: true
			  $$
			  \begin{aligned}
			  & A_{v_A} A_{v_B} \prod_{v=1}^L A_v\left|g_1, \ldots, g_L ; g_1^{\prime}, \ldots, g_L^{\prime}\right\rangle \\
			  = & \sum_{h_1, \ldots, h_L} \sum_{h_A, h_B}\left|h_1 g_1 h_A^{-1}, \ldots, h_L g_L h_A^{-1} ; h_1 g_1^{\prime} h_B^{-1}, \ldots, h_L g_L^{\prime} h_B^{-1}\right\rangle \\
			  = & \sum_{\tilde{g}_1, \ldots, \tilde{g}_L, h}\left|\tilde{g}_1 h, \ldots, \tilde{g}_L h ; \tilde{g}_1, \ldots, \tilde{g}_L\right\rangle
			  \end{aligned}
			  $$
				- $$
				  \tilde{g}_i:=h_i g_i^{\prime} h_B^{-1} , \quad h:=h_B g_1^{\prime-1} g_1 h_A^{-1}
				  $$
				- Actually we should sum over all vertices.
				- Here we only list the EB vertices and **implicit assume** that all other vertices already satisfy $A_v=1$.
				- The last equality used the trivial-holonomy condition.
			- A renaming of group elements leads to the desired result.
		- Proposition. The reduced density matrix of region A is
		  $$
		  \rho_A=\frac{1}{|G|^2} \sum_{g_v, h, h^{\prime}}\left|g_v h\right\rangle\left\langle g_v h^{\prime}\right|
		  $$
			- It suffices to note that the above proposition is already a Schmidt decomposition.
	- ## Calculate EE
		- Proposition. $\rho_A$ is a projection operator with a proper prefactor, i.e. all nonzero eigenvalues are equal.
			- $$
			  \begin{aligned}
			  \rho_A^2 & =\frac{1}{|G|^4} \sum_{g_v, h, h^{\prime}} \sum_{\bar{g}_v, \bar{h}, \bar{h}^{\prime}}\left|g_v h\right\rangle\left\langle\bar{g}_v \bar{h}^{\prime}\right|\left\langle g_v h^{\prime} \mid \bar{g}_v \bar{h}^{\prime}\right\rangle \\
			  & =\frac{1}{|G|^4} \sum_c \sum_{g_v, h, \bar{h}^{\prime}}\left|g_v h\right\rangle\left\langle g_v c^{-1} \bar{h}^{\prime}\right| \sum_{\bar{g}_v, \bar{h}, h^{\prime}} \delta_{\bar{g}_v^{-1} g_v, c} \delta_{\bar{h}^{\prime} h^{\prime-1}, c} \\
			  & =\rho_A
			  \end{aligned}
			  $$
		- Proposition. Under this normalization,
		  $$
		  S= \log \operatorname{tr} \rho_A = (L-1) \log |G|
		  $$
			- Since all pure states are equally weighted, $W=\operatorname{tr} \rho_A$ is the number of probable pure states.
	- ## Fusion basis and pure states
		- [Proposition](((658e9737-872f-4ba9-a294-dbe282a02020))). Quasi-particles on EB must fuse to a trivial charge.
		  id:: 658e9738-e5ce-4a72-b67a-9f4949c46f2b
		- Proposition. 
		  $$
		  \rho_A=P_G\left(\sum_{g_v}\left|g_v\right\rangle\left\langle g_v\right|\right) P_G=P_G \mathbb{1}_{EB} P_G=P_G
		  $$
			- $$P_G=\frac 1 {|G|} \sum_h h_*$$
			  where $h_*$ is the right multiplication by h.
			- Intuitively, $P_G$ enforces a global G-symmetry, as a consequence of gauge-invariance in region A.
			- Therefore, the nonzero eigenspace of $\rho_A$ is the space of all states of quasiparticles on EB that are invariant under this global $G$-symmetry. 
			  The $\eta$ is nothing but a set of good quantum numbers of this global symmetry.
		- Proposition. In the fusion basis,
		  $$
		  \rho_A=\sum_{j_v m_v, \eta}\left|j_v m_v ; \eta\right\rangle\left\langle j_v m_v ; \eta\right|
		  $$
			- In this basis, we can also count $W=|G|^{L-1}$. See ((658e99ab-a372-46ef-8be9-d53f9de78994)).
		-