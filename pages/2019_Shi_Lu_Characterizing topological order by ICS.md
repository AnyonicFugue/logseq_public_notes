- ![2019_Shi_Lu_Characterizing topological order by the.pdf](file://zotero_link/Research/Undergrad Thesis/2019_Shi_Lu_Characterizing topological order by the.pdf)
- # Setup
	- Definitions
	  collapsed:: true
		- The information convex for a frustration-free local Hamiltonian
			- $\Sigma\left(\Omega, \Omega^{\prime}\right)$ us the set of reduced density matrices on subsystem $\Omega$ obtained from reduced density matrices on a larger subsystem $\Omega^{\prime}$ which minimize the Hamiltonian $H_{\Omega^{\prime}}$
				- i.e.
				  $$
				  \Sigma\left(\Omega, \Omega^{\prime}\right) \equiv\left\{\sigma_{\Omega} \mid \sigma_{\Omega}=\operatorname{tr}_{\left[\Omega^{\prime} \backslash \Omega\right]} \rho_{\Omega^{\prime}} \text { where } \operatorname{tr}\left[H_{\Omega^{\prime}} \rho_{\Omega^{\prime}}\right]=0\right\}
				  $$
			- Note that we select the convention that the ground state is eigen to all local terms with eigenvalue zero.
	- Notations
	  collapsed:: true
		- $$
		  \sigma_{\Omega}^1 := t r_{\bar{\Omega}}|\psi\rangle\langle\psi|
		  $$
			- $\bar{\Omega}$ is the complement of $\Omega$.
			- $|\psi\rangle$ is the ground state.
		- Information convex set
			- $$
			  \Sigma\left(\Omega, \Omega^{\prime}\right) \equiv\left\{\sigma_{\Omega} \mid \sigma_{\Omega}=\operatorname{tr}_{\left[\Omega^{\prime} \backslash \Omega\right]} \rho_{\Omega^{\prime}} \text { where } \operatorname{tr}\left[H_{\Omega^{\prime}} \rho_{\Omega^{\prime}}\right]=0\right\}
			  $$
	- (Untwisted) QD model with (untwisted) boundary
		- The boundary is labeled by a subgroup $K \sub G$
		- Labels of the graph
		  collapsed:: true
			- bulk link $e$, bulk vertex $v$
			- boundary link $e^{\prime}$, boundary vertex $v^{\prime}$
			- face $f$
			- ((660cb3a6-ebf2-4c49-9a12-540eb05fa216))
		- The Hilbert space
		  collapsed:: true
			- For each boundary link $e'$ is $|K|$ dimensional:
			  $$\mathcal{H}_{e^{\prime}}=\operatorname{span}\left\{|k\rangle_{e^{\prime}} \mid k \in K\right\}$$
		- The Hamiltonian
			- collapsed:: true
			  $$
			  H=\sum_v\left(1-A_v\right)+\sum_f\left(1-B_f\right)+\sum_{v^{\prime}}\left(1-A_{v^{\prime}}^K\right)
			  $$
				- $$
				  A_v \equiv \frac{1}{|G|} \sum_{g \in G} A_v^g ; \quad B_f \equiv B_s^1 ; \quad A_{v^{\prime}}^K \equiv \frac{1}{|K|} \sum_{k \in K} A_{v^{\prime}}^k
				  $$
				- ((660cb4cf-295c-4d27-b439-dc86a453eca5))
			- Properties
			  collapsed:: true
				- All terms in the Hamiltonian commute
				- $A_v, B_f, A_{v^{\prime}}^K$ are projectors
				- For a system with $D^2$ topology (i.e. cover a disk $D^2$ with lattice), it can be shown that there is a unique ground state $|\psi\rangle$ that can be written as (up to normalization)
				  $$
				  |\psi\rangle=\prod_v A_v \cdot \prod_{v^{\prime}} A_{v^{\prime}}^K|1,1, \cdots, 1\rangle .
				  $$
					- Here, 1 represents the identity of group $G$ (or $K$ ).
					- This ground state is an equal weight superposition of all "zero flux configurations".
- # ((660b7ff7-1255-4a7c-9a88-92e49caef155))
	- Basic properties
		- Theorem III.5. One obtains a convex subset of $\Sigma\left(\Omega, \Omega^{\prime}\right)$ when one replaces $\Omega^{\prime}$ by a larger subsystem $\Omega^{\prime \prime}$, i.e. $\Sigma\left(\Omega, \Omega^{\prime \prime}\right) \subseteq \Sigma\left(\Omega, \Omega^{\prime}\right) \quad$ for $\quad \Omega^{\prime} \subseteq \Omega^{\prime \prime}$
- # ((660d5121-ff54-4c0f-b51c-24d6ec7205dc))
	- Lowest energy conditions
		- Prop. Consider a reduced density matrix $\rho_{\Omega^{\prime}}=\sum_\alpha \lambda_\alpha|\alpha\rangle_{\Omega^{\prime} \Omega^{\prime}}\langle\alpha|$  that minimizes the Hamiltonian $H_{\Omega^{\prime}}$. Then
		  collapsed:: true
		  $$\operatorname{tr}\left(H_{\Omega^{\prime}} \rho_{\Omega^{\prime}}\right)=0 \quad \Leftrightarrow \quad H_{\Omega^{\prime}}|\alpha\rangle_{\Omega^{\prime}}=0 \quad \forall \alpha$$
			- RHS -> LHS is obvious.
			- LHS -> RHS: Note that the smallest eigenvalue of $H$ is set to be 0, so we have
			  $$\langle \alpha | H | \alpha \rangle \geq 0$$
		- This doesn't hold for operators having support outside the region.
		  background-color:: red
		- Corollary. A state has minimal energy <-> annihilated by $A_v$ and $B_f$ having support **only in the region**.
		-
		- [Prop](((660e26b5-f9cf-46c6-9eb5-050b4cd92cf8))). For operators with support both in and out the region, we have
		  $$
		  A_v^g(\Omega) \sigma_{\Omega} A_v^{\bar{g}}(\Omega)=A_{v^{\prime}}^k(\Omega) \sigma_{\Omega} A_{v^{\prime}}^{\bar{k}}(\Omega) \quad \forall v, v^{\prime} \in \partial \Omega, \quad g \in G, k \in K .
		  $$
			- Proof
				- We should consider a larger region to include supports of $A_v$,
				  $$
				  \sigma_{\Omega}=\operatorname{tr}_{\left[\Omega^{\prime} -\Omega\right]}|\alpha\rangle_{\Omega^{\prime} \Omega^{\prime}}\langle\alpha|
				  $$
				- $A_v^g|\alpha\rangle_{\Omega^{\prime}}=|\alpha\rangle_{\Omega^{\prime}}$ and $A_{v^{\prime}}^k|\alpha\rangle_{\Omega^{\prime}}=|\alpha\rangle_{\Omega^{\prime}}$, for $v, v^{\prime} \in \partial \Omega$ and $g \in G, k \in K$.
		-
	- Prop. Info convex set for a general region:
	  id:: 660d5224-fe2c-4b59-8882-1b0985b1b5ea
	  collapsed:: true
	  $$
	  |\alpha\rangle_{\Omega^{\prime}}=\sum_{\left\{h_a^I\right\}, \lambda} \sqrt{p_{\left\{h_a^I\right\}}^\lambda} \left|\left\{h_a^I\right\} ; \lambda\right\rangle_{\Omega} \otimes\left|\left\{h_a^I\right\} ; \lambda\right\rangle_{\Omega^{\prime} \backslash  _\Omega} \quad \Rightarrow \quad \sigma_{\Omega}=\sum_{\left\{h_a^I\right\}, \lambda} p_{\left\{h_a^I\right\}}^\lambda\left|\left\{h_a^I\right\} ; \lambda\right\rangle_{\Omega \quad \Omega} \left\langle\left\{h_a^I\right\} ; \lambda \mid\right.$$
		- Here $I=1, \cdots, M$ labels the number of disconnected pieces of $\partial \Omega \cap \partial \bar{\Omega}(\bar{\Omega}$ is the complement of $\Omega)$.
			- $\left\{h_a^I\right\}$ is a set of link values $h_a^I \in G$, with $a=1, \cdots N_I$ labeling the links crossing the $I$th component of the boundary.
			- Define $h_1^I h_2^I \cdots h_{N_I}^I=h^I$. Note that we do not require $h^I=e$ (trivial total string along any piece of boundary), but we require $\prod_I h^I=e$.
		- When there is more than one piece of the boundary, **not all p_h must be equal**; the disk is a special case.
			- For example, in the case of a torus we could select four $p_{\{h\}}$ to form a convex combination (of the extreme points).
	- Technique. Minimal diagram
		- Since the ICS is invariant under continuous deformations (to be proved), we may select the simplest region with the given topology for easy calculation.
		- Disk
		  collapsed:: true
			- ((660e1826-7307-45a0-a69a-91b157cea088))
		- Annulus
		  collapsed:: true
			- ((660e1819-6935-4fb2-ac5d-2507c017d1f5))
	- ## Examples
		- [Disk](((660e17f0-a477-4267-922f-0737070c982e)))
			- $$
			  \sigma_{\omega_1}^1=\frac{1}{|G|^{n-1}} \sum_{\left\{h_a\right\}}\left|\left\{h_a\right\}\right\rangle_{\omega_1 \omega_1}\left\langle\left\{h_a\right\}\right| .
			  $$
		- Annulus
			- $$
			  \Sigma^*\left(\Omega_1\right)=\left\{\sigma_{\Omega_1}^* \mid \sigma_{\Omega_1}^*=\sum_{(c, R)} p_{(c, R)} \sigma_{\Omega_1}^{*(c, R)}\right\}
			  $$
				- $c$ is a conjugacy class of $G$
				- $E(c)$ is the centralizer group of $c$
				- $R$ is an irrep of $E(c)$ and $\Gamma$ is the rep matrix.
			- $$
			  \sigma_{\Omega_1}^{*(c, R)}=\frac{1}{|c|^2 \cdot n_R^2} \sum_u \sum_v|(c, R)(u, v)\rangle\langle(c, R)(u, v)|
			  $$
				- $$
				  \begin{aligned}
				  |(c, R)(u, v)\rangle & \equiv A_1^{p_i} A_2^{p_{i^{\prime}}} \sum_{t \in E(c)} \sqrt{\frac{n_R}{|E(c)|}} \bar{\Gamma}_R^{j j^{\prime}}(t)\left|r_c, r_c, t\right\rangle=\sum_{t \in E(c)} \sqrt{\frac{n_R}{|E(c)|}} \bar{\Gamma}_R^{j j^{\prime}}(t)\left|c_i, c_{i^{\prime}}, p_i t \bar{p}_{i^{\prime}}\right\rangle \\
				  & \Rightarrow\left\langle(c, R)(u, v) \mid\left(c^{\prime}, R^{\prime}\right)\left(u^{\prime}, v^{\prime}\right)\right\rangle=\delta_{c, c^{\prime}} \delta_{R, R^{\prime}} \delta_{u, u^{\prime}} \delta_{v, v^{\prime}} .
				  \end{aligned}
				  $$
			- Proof
				- Consider the minimal diagram
				  ((660e1819-6935-4fb2-ac5d-2507c017d1f5))
				- First we need the conditions that
				  2) $\bar{B} \sigma_{\Omega_1}^*=\sigma_{\Omega_1}^*$, where $B|h, H, t\rangle=\delta_{h, t H \bar{t}}|h, H, t\rangle$.
				  3) $A_1^g \sigma_{\Omega_1}^* A_1^{\bar{g}}=A_2^g \sigma_{\Omega_1}^* A_2^{\bar{g}}=\sigma_{\Omega_1}^*$ for $\forall g \in G$, where $A_1^g|h, H, t\rangle=|g h \bar{g}, H, g t\rangle$ and $A_2^g|h, H, t\rangle=|h, g H \bar{g}, t \bar{g}\rangle$.