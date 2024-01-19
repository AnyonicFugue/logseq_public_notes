alias:: MPS, Projected Entangled Pair State, PEPS, Tensor Product State, TPS

-
- # PEPS Formalism #card
  collapsed:: true
  card-last-interval:: 31.26
  card-repeats:: 1
  card-ease-factor:: 2.6
  card-next-schedule:: 2023-12-16T06:47:09.522Z
  card-last-reviewed:: 2023-11-15T00:47:09.522Z
  card-last-score:: 5
	- Start from a (virtual) chain of maximally entangled pairs.
	  collapsed:: true
		- ((64c68156-c82e-4925-994b-08a60283cd79))
		- Each pair is in
		  $$
		  |\psi\rangle=\frac{1}{\sqrt{D}} \sum_{\alpha=1}^D|\alpha \alpha\rangle
		  $$
	- Perform the projection from the virtual space to the physical space.
		- $$
		  P=\sum_{i, \alpha, \beta} A_{i, \alpha, \beta}|i\rangle\langle\alpha \beta|
		  $$
	- Proposition. After the projection, the state is 
	  collapsed:: true
	  $$
	  |\psi\rangle=\sum_{i_1, i_2 \ldots i_N} \operatorname{Tr}\left(A_{i_1} A_{i_2} \ldots A_{i_N}\right)\left|i_1 i_2 \ldots i_N\right\rangle
	  $$
		- Obviously the maximally entangled pair forces the summation of indices.
	- Generalize to TPS
		- Start from $$|\psi\rangle=\frac{1}{\sqrt{D}} \sum_{\alpha=1}^D|\alpha \alpha\rangle$$
		- $$
		  P=\sum_{i, \alpha, \ldots, \gamma} T_{\alpha, \ldots, \gamma}^i|i\rangle\langle\alpha \ldots \gamma|
		  $$
		-
- # Questions and Problems #card
  collapsed:: true
  card-last-interval:: 33.94
  card-repeats:: 1
  card-ease-factor:: 2.6
  card-next-schedule:: 2023-11-20T22:48:23.723Z
  card-last-reviewed:: 2023-10-18T00:48:23.723Z
  card-last-score:: 5
	- ((64c6b051-edfc-488a-8dd7-626fb927f0f3))
	- What makes the difference between scalars and matrices?
		- Intuitively, the trace makes matrices at different sites 'entangled'.
		- For scalars we have the decomposition
		  $$\sum _{i_{1} ,i_{2} ,\dotsc ,i_{N}} a_{i_{1}}^{[1]} a_{i_{2}}^{[2]} \dotsc a_{i_{N}}^{[N]}| i_{1} i_{2} \dotsc i_{N}\rangle =\otimes _{j=1,...,N}\left(\sum _{i_{j}} a_{i_{j}}^{[j]}| i_{j}\rangle \right)$$
		  while there is no counterpart of trace, since taking the trace is essentially a 'global' operation and cannot be factored into sites.
	- What language (higher than conventional linear algebra) suits describing tensor networks?
	  What properties could capture the LRE features?
	-
	- Could we perform wavefunction renormalization **without** knowing the exact ground state?
	  id:: 64c59214-6656-41ef-b0ff-283d4062fc9b
		- Like that of calculating entanglement entropy of stabilizer formalism...
	-
	- ## To Examine
		- TODO How to unify WFR and TNR? How to systematically factor product degrees of freedom and throw them away?
		  id:: 64c905ac-b67f-49b6-9303-441e4ac1f6ab
			- Try a few examples, e.g. Ising, toric code
- # 1D case
	- ## Setup
	  collapsed:: true
		- Notations
		  collapsed:: true
			- $D$ is the **inner dimension** of the MPS.
			- $d_k$ is the dimension of the local physical degree of freedom.
			-
		- Definitions
			- Matrix product state
			  card-last-interval:: 33.94
			  card-repeats:: 1
			  card-ease-factor:: 2.6
			  card-next-schedule:: 2023-09-12T11:00:23.961Z
			  card-last-reviewed:: 2023-08-09T13:00:23.962Z
			  card-last-score:: 5
				- collapsed:: true
				  $$
				  |\psi\rangle=\sum_{i_1, i_2, \ldots, i_N} \operatorname{Tr}\left(A_{i_1}^{[1]} A_{i_2}^{[2]} \ldots A_{i_N}^{[N]}\right)\left|i_1 i_2 \ldots i_N\right\rangle
				  $$
					- $A_{i_k}^{[k]}$s are $D \times D$ matrices on site $k$, $i_k=1 \ldots d_k$.
				- ((64c5a290-b014-45d4-9fc7-833ca91aa487))
				  collapsed:: true
					- $\alpha,\beta$ are the inner indices to be contracted.
					-
			- Double tensor
			  collapsed:: true
				- $$
				  \mathbb{E}_{\alpha \gamma, \beta \chi}=\sum_i A_{i, \alpha \beta} \times\left(A_{i, \gamma \chi}\right)^*
				  $$
				- ((64c66350-a47a-4539-8121-83612d4564f3))
				- Note that there are two ways of viewing the double tensor.
				  collapsed:: true
					- When performing diagonalization to restore matrices from the double tensor, we group $\alpha,\beta$ together and $\gamma,\chi$ together. 
					  id:: 64c6bff9-672b-4d2d-a8c6-adfdf7e38b0e
					  i.e. $\mathbb{E}=\sum_i A_i \otimes A_i^* \in W \otimes W$ while viewing $A_i$ as a **vector** in some $W$.
					- When using it to contract, we group $\alpha,\gamma$ together and $\beta,\chi$ together. 
					  i.e. $\mathbb{E}=\sum_i A_i \otimes A_i^* \in \operatorname{Hom}(V \otimes V)$ while viewing $A_i$ as an **operator**.
			- Injective #card
			  collapsed:: true
			  card-last-interval:: 31.26
			  card-repeats:: 1
			  card-ease-factor:: 2.6
			  card-next-schedule:: 2023-09-06T18:29:38.199Z
			  card-last-reviewed:: 2023-08-06T12:29:38.199Z
			  card-last-score:: 5
				- There are several equivalent expressions.
				- The canonical form has only one block.
				  logseq.order-list-type:: number
				- There exists a finite $L_0$ such that the set of matrices
				  logseq.order-list-type:: number
				  $$
				  \tilde{A}_{I_{L_0}}=A_{i_1} \ldots A_{i_{L_0}}
				  $$
				  spans the the whole space of $D \times D$ matrices.
				-
	- ## Basic Facts
	  collapsed:: true
		- Each state in a finite-dimensional space could be represented as an MPS if D is large enough.
		  collapsed:: true
			- For a system with $N$ sites and $d$ local d.o.f. the Hilbert space has $d^N$ dimensions.
			- We can select $D=d^N$, with each dimension representing a basis of the whole Hilbert space.
			- All matrices $A_i^{(k)}$ are diagonal. The diagonal elements are nonzero iff the configuration just has $|k\rangle$ at $i^{th}$ site.
			-
		- The representation is efficient if we select D smartly.
		  collapsed:: true
			- With fixed $D$ for a state of $N$ spins, the number of parameters involved is at most $\sum_k N d_k D^2$.
			  collapsed:: true
				- N sites in total.
				- d matrices each site.
				- D^2 for a single matrix.
			- The number of parameters needed is $\prod_k d_k$ in the generic case.
		- If $D=1$, the state is a product state.
		  collapsed:: true
			- $$\begin{aligned}
			  |\psi \rangle  & =\sum _{i_{1} ,i_{2} ,\dotsc ,i_{N}} a_{i_{1}}^{[1]} a_{i_{2}}^{[2]} \dotsc a_{i_{N}}^{[N]}| i_{1} i_{2} \dotsc i_{N}\rangle \\
			   & =\otimes _{j=1,...,N}\left(\sum _{i_{j}} a_{i_{j}}^{[j]}| i_{j}\rangle \right)
			  \end{aligned}$$
		- The double tensor is positive in combining $\alpha \beta$ and $\gamma \chi$, but not necessarily the other way. #card
		  card-last-interval:: 31.26
		  card-repeats:: 1
		  card-ease-factor:: 2.6
		  card-next-schedule:: 2023-09-05T19:05:54.337Z
		  card-last-reviewed:: 2023-08-05T13:05:54.338Z
		  card-last-score:: 5
			- Recall the definition $\mathbb E_{\alpha\beta\gamma\chi}:= \sum_i A^i_{\alpha\beta} A^{i*}_{\gamma\chi}$
		- Obtain matrices from a double tensor
		  collapsed:: true
			- In short, view it as an Hermitian bilinear form and diagonalize.
		- Basis transformations
		  collapsed:: true
			- We can perform unitary transformations on the basis states $\{|i_k\rangle\}$ and the corresponding matrices $\{A_{i_k}\}$.
			-
			- Two set of matrices $A_i$ and $B_i$ are related by a unitary transformation $U$ on the physical index $i$ **iff** they give rise to the same double tensor. #card
			  collapsed:: true
			  card-last-interval:: 33.94
			  card-repeats:: 1
			  card-ease-factor:: 2.6
			  card-next-schedule:: 2023-09-12T10:59:59.629Z
			  card-last-reviewed:: 2023-08-09T12:59:59.629Z
			  card-last-score:: 5
				- Necessity is obvious.
				  collapsed:: true
					- $$
					  \mathbb{E}_B=\sum_j B_{j, \alpha \beta} \times\left(B_{j, \gamma \chi}\right)^*=\sum_{i i^{\prime} j} U_{i j} U_{i^{\prime} j}^* A_{i, \alpha \beta} \times\left(A_{i^{\prime}, \gamma \chi}\right)^*=\sum_i A_{i, \alpha \beta} \times\left(A_{i, \gamma \chi}\right)^*=\mathbb{E}_A
					  $$
				- Sufficiency is harder.
					- Idea
						- If we can prove the two sets of matrices could be related by an invertible transformation, then the transformation must be unitary.
					- Step 1. Prove for the case where the matrices are linear independent.
					  collapsed:: true
						- ((64c66feb-f6e4-4adf-88cb-64ecf551e7e9))
						- First we rephrase the problem in an elegant way.
						  collapsed:: true
							- We have a vector space $V$ and an anti-linear convolute map $\dagger$.
							- For two linear independent sets of vectors $\{e_i\}$ and $\{f_j\}$ such that $\sum_i e_i \otimes e_i^\dagger$ and $\sum_j f_j \otimes f_j^\dagger$, we want to show $e_i$ and $f_j$ span the same subspace.
						- Then it becomes very easy: We first ((64c66f21-d71f-4cf2-a4d8-44d974454f65)) $\{e_1,...e_n,f_{j_1},...,f_{j_m}\}$.
						- Obviously if there are indeed $f$ in the list, then it can't be $\sum_i e_i \otimes e_i^\dagger$ and $\sum_j f_j \otimes f_j^\dagger$.
					- Step 2. Extend to non linear-independent case.
					  collapsed:: true
						- The argument of a maximal linear independent list still holds, only assailed by some cross terms.
			- Corollary. States up to a unitary transformation <-> Same double tensor.
		- Theorem. If the eigenspace of the largest eigenvalue of the double tensor is one-dimensional, then all correlations decays exponentially. #card
		  collapsed:: true
		  card-last-interval:: 28.64
		  card-repeats:: 1
		  card-ease-factor:: 2.6
		  card-next-schedule:: 2023-08-31T03:55:39.131Z
		  card-last-reviewed:: 2023-08-02T12:55:39.132Z
		  card-last-score:: 5
			- Preparation
			  collapsed:: true
				- To have a finite norm as $N \to \infty$, we shall set the largest eigenvalue of $\mathbb E$ to 1.
				- The is always allowed, since it's only a scaling of coefficients.
			- $$
			  \left\langle O_1 O_2\right\rangle-\left\langle O_1\right\rangle\left\langle O_2\right\rangle=\frac{\operatorname{Tr}\left(\mathbb{E}^{N-L-2} \mathbb{E}\left[O_1\right] \mathbb{E}^L \mathbb{E}\left[O_2\right]\right)}{\operatorname{Tr}\left(\mathbb{E}^N\right)}-\frac{\operatorname{Tr}\left(\mathbb{E}^{N-1} \mathbb{E}\left[O_1\right]\right) \operatorname{Tr}\left(\mathbb{E}^{N-1} \mathbb{E}\left[O_2\right]\right)}{\operatorname{Tr}^2\left(\mathbb{E}^N\right)}
			  $$
			-
			- Denote the projection onto the eigenspace of eigenvalue $\lambda$ as $P_\lambda$. When $L \to \infty$ and $N \to \infty$, the correlation function becomes approximately
			  collapsed:: true
			  $$
			  \frac{\operatorname{Tr}\left(P_1 \mathbb{E}\left[O_1\right]P_1 \mathbb{E}\left[O_2\right]\right)}{\operatorname{Tr}\left(P_1\right)}-\frac{\operatorname{Tr}\left(P_1 \mathbb{E}\left[O_1\right]\right) \operatorname{Tr}\left(P_1 \mathbb{E}\left[O_2\right]\right)}{\operatorname{Tr}^2\left(P_1\right)}
			  $$
				- Note that $P_1^2=P_1$.
			- When $P_1$ is one-dimensional, both terms are
			  collapsed:: true
			  $$
			  \left\langle v_1\left|\mathbb{E}\left[O_1\right]\right| v_1\right\rangle\left\langle v_1\left|\mathbb{E}\left[O_2\right]\right| v_1\right\rangle
			  $$
			  which cancels.
				- Note that $|v_1\rangle \in \mathrm{GL}(V)$ isn't a quantum state, but an eigenvector of the double tensor.
				- The trace is 1.
			- When $P_1$ is higher dimensional, we have
			  $$
			  \frac{\sum_{i, j}\left\langle v_i\left|\mathbb{E}\left[O_1\right]\right|{ }v_j\right\rangle\left\langle v_j\left|\mathbb{E}\left[O_2\right]\right| v_i\right\rangle}{\operatorname{Tr}\left(P_1\right)}-\frac{\sum_{i, j}\left\langle v_i\left|\mathbb{E}\left[O_1\right]\right| v_i\right\rangle\left\langle v_j\left|\mathbb{E}\left[O_2\right]\right| v_j\right\rangle}{\operatorname{Tr}^2\left(P_1\right)}
			  $$
			  which could be nonzero.
	- ## Entanglement Area Law
	  collapsed:: true
		- Note that the double tensor determines the state up to **on-site unitary transformations**, thus **all** entanglement information (including short-range) is contained.
		- It is claimed that MPS puts an upper bound $\ln (D^2)$ on the entanglement entropy via double tensors.
		  collapsed:: true
			- However, double tensors seem not the most convenient tool to express the density matrix.
	- ## Canonical Form
	  id:: 64c69deb-c2c4-4b90-9848-ec3506076588
	  collapsed:: true
		- ((64b4848e-7e80-4fe8-a1f1-319b6f009d6f))
		- Theorem. Given a TI state on a finite ring, we can always decompose the matrices $A_i$ of any of its TI MPS representations as
		  card-last-interval:: 32.57
		  card-repeats:: 1
		  card-ease-factor:: 2.6
		  card-next-schedule:: 2023-09-12T01:28:44.591Z
		  card-last-reviewed:: 2023-08-10T12:28:44.592Z
		  card-last-score:: 5
		  $$
		  A_i=\left(\begin{array}{ccc}
		  \lambda_1 A_i^1 & 0 & 0 \\
		  0 & \lambda_2 A_i^2 & 0 \\
		  0 & 0 & \cdots
		  \end{array}\right),
		  $$
		  where $1 \geq \lambda_j>0$ for every $j$ and the matrices $A_i^j$ in each block verify the conditions:
		  1. $\sum_i A_i^j A_i^{j \dagger}=\mathbb{1}$.
		  2. $\sum_i A_i^{j \dagger} \Lambda^j A_i^j=\Lambda^j$, for some diagonal positive and full-rank matrices $\Lambda^j$.
		  3. $\mathbb{1}$ is the only fixed point of the operator $\mathcal{E}_j(X)=\sum_i A_i^j X A_i^{j \dagger}$. #card
			- Notes
				- The operator $\mathcal{E}_j(X)=\sum_i A_i^j X A_i^{j \dagger}$ is precisely the double tensor.
			- Corollaries
				- The MPS $|\psi\rangle$ represented by $A_i$ can be written as a superposition of $\left|\psi^{(j)}\right\rangle$'s, represented by matrices $A_i^{(j)}$.
				  collapsed:: true
				  $$
				  |\psi\rangle=\sum_j\left|\psi^{(j)}\right\rangle
				  $$
					- The basis is still the same for all $k$, but different $A_i^{(j)} gives different states.
			- See [[quant-ph/0608197] Matrix Product State Representations (arxiv.org)](https://arxiv.org/abs/quant-ph/0608197).
	- ## Existence of Parent Hamiltonian #card
	  collapsed:: true
	  card-last-interval:: 32.51
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2023-09-06T01:08:18.329Z
	  card-last-reviewed:: 2023-08-04T13:08:18.329Z
	  card-last-score:: 5
		- Theorem (Injective Case). A parent Hamiltonian can be constructed for a finite dimensional matrix product state with finite correlation length, such that the matrix product state is the **unique gapped** ground state of the parent Hamiltonian. #card
		  collapsed:: true
		  card-last-interval:: 31.26
		  card-repeats:: 1
		  card-ease-factor:: 2.6
		  card-next-schedule:: 2023-09-14T18:57:07.611Z
		  card-last-reviewed:: 2023-08-14T12:57:07.612Z
		  card-last-score:: 5
			- The procedure for constructing the parent Hamiltonian is as follows:
			  1. take a large enough but finite segment of length $l$ of the chain
			  2. calculate the reduced density matrix $\rho_l$ of this segment
			  3. write the projection operator $P_l$ onto the support space of $\rho_l$
			  The parent Hamiltonian is the MPS is then the sum of all such local projectors
			  $$
			  H=\sum_i\left(1-P_l^i\right)
			  $$
			- Idea
			  collapsed:: true
				- Construct projection operators to the known state.
			- Proof
			  collapsed:: true
				- Denote a basis of the support space as $|\phi_1\rangle, ..., |\phi_n\rangle$.
				- The state of the whole system must be $|\psi\rangle=\sum_i \phi_i\rangle \otimes |\chi_i\rangle$. Obviously it is a ground state.
				- Uniqueness is harder, but 'it can be shown'.
		- Theorem (Non-injective case). If the MPS isn't injective, a parent Hamiltonian can be constructed which is still gapped but has a degenerate ground space spanned by all $\left|\psi^{(k)}\right\rangle$ 's.
		  collapsed:: true
			- To construct such a parent Hamiltonian, first notice that on large enough segments, the support space of the reduced density matrices $\rho_l^{(k)}$ and $\rho_l^{\left(k^{\prime}\right)}$ are orthogonal to each other.
			- The parent Hamiltonian can then be written as
			  $$
			  H=\sum_i \sum_k\left(1-\left(P_l^i\right)^{(k)}\right)
			  $$
			  which is obviously the sum of all short-range correlated components.
			-
	- ## [[Renormalization Group]] #card
	  collapsed:: true
	  card-last-interval:: 42
	  card-repeats:: 2
	  card-ease-factor:: 2.7
	  card-next-schedule:: 2023-12-08T00:19:56.446Z
	  card-last-reviewed:: 2023-10-27T00:19:56.446Z
	  card-last-score:: 5
		- #+BEGIN_NOTE
		  This is the most exciting part -- systematically finding the structure of LRE!
		  #+END_NOTE
		- ((64c6a836-1ad4-44cd-9bd4-ae0ed8e5cbd7))
			- Step 1. Represent MPS by double tensors $\mathbb E$
			- Step 2. Combine adjacent double tensors into a new one $\tilde{\mathbb E}$
			- Step 3. Diagonalize $\tilde{\mathbb{E}}_{\alpha \gamma, \beta^{\prime} \chi^{\prime}}$ (by taking it as a matrix with row index $\alpha \beta^{\prime}$ and column index $\gamma \chi^{\prime}$. It is easy to see that with such a recombination, $\tilde{\mathbb{E}}$ is a positive) **discard zero eigenvalues** and obtain the new MPS by
			  $$
			  \tilde{A}_{\alpha \beta^{\prime}}^{\tilde{i}}=\sqrt{\lambda_i} V_{\tilde{i}, \alpha \beta^{\prime}}
			  $$
				- $$
				  \tilde{\mathbb{E}}_{\alpha \gamma, \beta^{\prime} \chi^{\prime}}=\sum_{\tilde{i}} \lambda_{\tilde{i}} V_{\tilde{i}, \alpha \beta^{\prime}} V_{\tilde{i}, \gamma \chi^{\prime}}^*
				  $$
				- This is viewing an operator $T \in \operatorname{Hom}(V) \simeq V \otimes V^*$.
				- Diagonalize -> $T=\sum \lambda_i |v_i\rangle\langle v_i|$
				- The map from a vector to its dual is realized by the inner product, which is **anti-linear**.
				  Thus the complex conjugation.
		- Which dimensions change when we contract adjacent double tensors?
		  collapsed:: true
			- Matrix: $D \times D$.
			- Double tensor: $D^2 \times D^2$, could be viewed as $\mathcal L(D^2)$.
			  Still $\mathcal L(D^2)$ after contraction.
			- Rank of $\mathbb E$ is an interesting topic, since the 'rank' depends on the grouping of matrices.
			  collapsed:: true
				- In general, an operator in $\mathcal L(D^2)$ has rank at most $D^2$.
				- However, if we take the [first viewpoint](((64c6bff9-672b-4d2d-a8c6-adfdf7e38b0e))), then the rank is at most $d$.
		- What does 'zero eigenvalue' mean? Does throwing it away remove local entanglement?
		  id:: 64c6b051-edfc-488a-8dd7-626fb927f0f3
		  collapsed:: true
			- See an example.
		- Proof
			- $\tilde{\mathbb E}$ is positive.
			  collapsed:: true
				- Directly follows $xx^* \geq 0$.
			- $\tilde{\mathbb E}$ contains entanglement information *between the pair and the rest of the system*, but not *within the pair*.
			  collapsed:: true
				- To be more precise, only $\tilde{\mathbb E}$ counts in the reduced density matrix.
				- $$\begin{aligned}
				  |\psi \rangle  & =\sum _{i_{1} ,\dotsc ,i_{N}}\operatorname{Tr}\left( A_{i_{1}}^{[1]} \dotsc A_{i_{N}}^{[N]}\right)| i_{1} \dotsc i_{N} \rangle \\
				  \rho =|\psi \rangle \langle \psi | & =\sum _{i_{1} ,\dotsc ,i_{N} ;j_{1} ,...,j_{N}}\operatorname{Tr}\left( A_{i_{1}}^{[1]} \dotsc A_{i_{N}}^{[N]}\right)\operatorname{Tr}\left( A{_{j_{1}}^{[1]}}^{*} \dotsc A{_{j_{N}}^{[N]}}^{*}\right)| i_{1} \dotsc i_{N} \rangle \langle j_{1} \dotsc j_{N} |\\
				   & =\sum _{i_{1} ,\dotsc ,i_{N} ;j_{1} ,...,j_{N}}\operatorname{Tr}\left\{\left( A_{i_{1}}^{[1]} \otimes A{_{j_{1}}^{[1]}}^{*}\right) \dotsc \left( A_{i_{N}}^{[N]} \otimes A{_{j_{N}}^{[N]}}^{*}\right)\right\}| i_{1} \dotsc i_{N} \rangle \langle j_{1} \dotsc j_{N} |
				  \end{aligned}$$
				- $$\begin{aligned}
				  \operatorname{Tr}_{\{1,2\}} \rho  & =\sum _{i_{1} ,i_{2}}\sum _{i_{3} ,\dotsc ,i_{N} ;j_{3} ,...,j_{N}}\operatorname{Tr}\{\left( A_{i_{1}}^{[1]} \otimes A{_{i_{1}}^{[1]}}^{*}\right)\left( A_{i_{2}}^{[2]} \otimes A{_{i_{2}}^{[2]}}^{*}\right) \times \left( A_{i_{1}}^{[3]} \otimes A{_{j_{1}}^{[3]}}^{*}\right) \dotsc \\
				   & \left( A_{i_{N}}^{[N]} \otimes A{_{j_{N}}^{[N]}}^{*}\right)\} \times | i_{3} \dotsc i_{N}> \langle j_{3} \dotsc j_{N} |\\
				   & =\sum _{i_{3} ,\dotsc ,i_{N} ;j_{3} ,...,j_{N}}\operatorname{Tr}\left\{\mathbb{E}_{1}\mathbb{E}_{2} \times \left( A_{i_{1}}^{[3]} \otimes A{_{j_{1}}^{[3]}}^{*}\right) \dotsc \left( A_{i_{N}}^{[N]} \otimes A{_{j_{N}}^{[N]}}^{*}\right)\right\}\\
				   & \times | i_{3} \dotsc i_{N}> \langle j_{3} \dotsc j_{N} |
				  \end{aligned}$$
				-
			- collapsed:: true
				-
	- Theorem. There is no intrinsic topological order in 1D bosonic systems. #card
	  collapsed:: true
	  card-last-interval:: 31.26
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2023-12-17T06:41:57.902Z
	  card-last-reviewed:: 2023-11-16T00:41:57.903Z
	  card-last-score:: 5
		- Main line of the proof
			- Gapped 1D bosonic state -> Short-range correlated (injective) MPS.
			  logseq.order-list-type:: number
			- Injective MPS -> The largest eigenvalue of the double tensor is nondegenerate.
			  logseq.order-list-type:: number
			- Study the thermodynamic limit: Only the largest eigenstate survives, which leads to a product state
			  logseq.order-list-type:: number
			- Show that the product double-tensor structure indicates a product state.
			  logseq.order-list-type:: number
			- ((64c7b982-ecf8-47d4-919b-c3ceaf0b8610))
		- Step 1
		  collapsed:: true
			- A very interesting topic. We shall better understand the role of gap here.
			  id:: 64c84429-d174-419e-a027-ac09c02254c0
		- Step 2
		  collapsed:: true
			- See ((64c69deb-c2c4-4b90-9848-ec3506076588)), property 3.
			  'Fixed point' <-> Eigenvector with eigenvalue +1.
		- Step 3. Prove the diagonalization of $\Lambda$.
			- Let the left eigenvector is $\Lambda_{\alpha \gamma}^l$ and the right eigenvector is $\Lambda_{\beta \chi}^r$
			  collapsed:: true
			  $$
			  \mathbb{E}_{\alpha \gamma, \beta \chi}=\Lambda_{\alpha \gamma}^l\left(\Lambda_{\beta \chi}^r\right)^*+\ldots
			  $$
				- What's the difference between left and right eigenvectors?
				  collapsed:: true
					- (Right) eigenvector: nonzero $v \in \mathbf{C}^n$ s.t. $(\lambda I-A) v=0$, i.e.,
					  $$
					  A v=\lambda v
					  $$
					- Left eigenvector: nonzero $w \in \mathbf{C}^n$ s.t. $w^T(\lambda I-A)=0$, i.e.,
					  $$
					  w^T A=\lambda w^T
					  $$
					- We can write
					  $$A=\sum \lambda_i |v_i\rangle \langle v_i|$$
					  where the left eigenvector is precisely the dual of the right eigenvector.
					- In any orthogonal basis, taking the dual is precisely taking the complex conjugate.
						- Note that though the complex conjugate isn't basis independent, the point is that the basis transformation would also be conjugated. Thus the complex conjugation is the same in any ONB.
			- Since it is naturally an ONB here, we should have $\Lambda_{\alpha \gamma}^r=\Lambda_{\alpha \gamma}^l$
			- In the thermodynamic limit,
			  $$\lim_{n \to \infty} \mathbb{E}^n :=\mathbb{E}^{(\infty)}=|\Lambda\rangle \langle\Lambda|$$
			- Now we should decompose $\mathbb E$ back to obtain matrices.
			- Proposition. Since $\mathbb{E}^{\infty}$ is positive when treated as a matrix with row index $\alpha \beta$ and colomn index $\gamma \chi$, $\Lambda^l$ is also positive (up to a phase) when treated as a matrix. #card
			  collapsed:: true
			  card-last-interval:: 31.26
			  card-repeats:: 1
			  card-ease-factor:: 2.6
			  card-next-schedule:: 2023-09-05T18:55:49.486Z
			  card-last-reviewed:: 2023-08-05T12:55:49.486Z
			  card-last-score:: 5
				- Viewpoint: $\Lambda \in \operatorname{Hom}(V)$.
				  $$\mathbb E = \Lambda \otimes \Lambda^* \in \operatorname{Hom}(V \otimes V^*)$$
				- Step 1. Find an eigenvalue $\lambda_1$ of $\Lambda$ with corresponding eigenvector $v_1$.
				  Multiply $1/\lambda_1$ to make $e^{i \theta}\lambda_1 =1$.
				- Step 2. Select an vector $u \otimes v_1^*$.
				  Then we know $\langle u \otimes v_1^* | \mathbb E | u \otimes v_1^*\rangle=\langle u | \Lambda | u\rangle \langle v | \Lambda^* | u\rangle = \langle v_1^* | \Lambda | v_1^*\rangle \geq 0$.
				-
			- Therefore we can decompose $\Lambda_{\alpha \gamma}=\sum_i \lambda_i v_\alpha^i\left(v_\gamma^i\right)^*$, and
			  $$
			  \left(A^{(\infty)}\right)_{\alpha \beta}^{i^l, i^r}=\sqrt{\lambda_{i^l} \lambda_{i^r}} v_\alpha^{i^l} v_\beta^{i^r}
			  $$
			  which is precisely ((64c7c826-5f2d-441d-9dd8-053d55a0192b))
		- Step 4. Show that the product matrix structure indicates a product state.
			- Note that $$|\psi\rangle=\sum_{i_1, i_2, \ldots, i_N} \operatorname{Tr}\left(A_{i_1}^{[1]} A_{i_2}^{[2]} \ldots A_{i_N}^{[N]}\right)\left|i_1 i_2 \ldots i_N\right\rangle$$, or ((64c5a290-b014-45d4-9fc7-833ca91aa487)).
			- Product matrices -> The coefficients of the left side and the right side has no correlations, i.e. the left and the right are not entangled.
			- Note that we can select an arbitrary (very long) window, thus the matrices could be factored anywhere.
			- Thus the structure is actually ((64c7ccd9-9767-4ed6-9704-5f4fe3fe7d0e))
			  which is manifestly SRE.
	- ## Examples
		- D=2, GHZ state #card
		  collapsed:: true
		  card-last-interval:: 32.57
		  card-repeats:: 1
		  card-ease-factor:: 2.6
		  card-next-schedule:: 2023-10-25T14:02:12.672Z
		  card-last-reviewed:: 2023-09-23T01:02:12.673Z
		  card-last-score:: 5
			- $$
			  A_0=\left(\begin{array}{ll}
			  1 & 0 \\
			  0 & 0
			  \end{array}\right), A_1=\left(\begin{array}{ll}
			  0 & 0 \\
			  0 & 1
			  \end{array}\right)
			  $$
			- Note that $A_\alpha A_\beta = \delta_{\alpha \beta}$.
			- Wavefunction
			  collapsed:: true
				- $$
				  |G H Z\rangle=|0\rangle^{\otimes N}+|1\rangle^{\otimes N}
				  $$
			- Injectivity
			  collapsed:: true
				- No.
				- The double tensor is $\left(\begin{array}{llll}1 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 1\end{array}\right)$.
				- The set of matrices only contain $A_{0 \ldots 0}=\left(\begin{array}{ll}1 & 0 \\ 0 & 0\end{array}\right), A_{1 \ldots 1}=\left(\begin{array}{ll}0 & 0 \\ 0 & 1\end{array}\right)$, no matter how long the segment is.
		- AKLT state
		  collapsed:: true
			- Setup: d=3 (Spin-1), D=3
			  collapsed:: true
				- $$
				  |x\rangle=\frac{1}{\sqrt{2}}(-|-1\rangle+|1\rangle),|y\rangle=\frac{-i}{\sqrt{2}}(|-1\rangle+|1\rangle),|z\rangle=-|0\rangle
				  $$
				- $$
				  A_{-1}=-(X-i Y) / \sqrt{2}, A_0=-Z, A_1=(X+i Y) / \sqrt{2}
				  $$
			- Injectivity
			  collapsed:: true
				- Yes.
				- $$
				  A_{x x}=A_{y y}=A_{z z}=I, A_{x y}=-A_{y x}=i Z, A_{y z}=-A_{z y}=i X, A_{z x}=-A_{x z}=i Y
				  $$
				  which spans the whole space of 2x2 matrices.
				-
- # Higher Dimensions: TPS
	- ## Open Problems #card
	  collapsed:: true
	  card-last-interval:: 31.26
	  card-repeats:: 1
	  card-ease-factor:: 2.36
	  card-next-schedule:: 2024-02-04T07:15:47.548Z
	  card-last-reviewed:: 2024-01-04T01:15:47.548Z
	  card-last-score:: 3
		- How to determine whether a state is short-range correlated?
			- we can find some mathematical characteristic to capture the notion, not necessarily computationally efficient.
			- Tt is known that there are injective tensor product states whose correlation functions only decay polynomially.
	- ## Definitions: TPS, Gauge DOF, Double Tensor #card
	  card-last-interval:: 31.26
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2024-01-31T07:04:46.779Z
	  card-last-reviewed:: 2023-12-31T01:04:46.780Z
	  card-last-score:: 5
		- TPS
			- A tensor product state in a many-body spin system is 
			  $$
			  |\psi\rangle=\sum_{i_1, i_2, \ldots i_m \ldots} \operatorname{tTr}\left(T^{i_1} T^{i_2} \ldots T^{i_m} \ldots\right)\left|i_1 i_2 \ldots i_m \ldots\right\rangle
			  $$
			  where $\operatorname{tTr}$ means contracting the inner indices.
		- Gauge degree of freedom
		  card-last-interval:: 32.57
		  card-repeats:: 1
		  card-ease-factor:: 2.6
		  card-next-schedule:: 2023-09-03T02:07:16.463Z
		  card-last-reviewed:: 2023-08-01T13:07:16.463Z
		  card-last-score:: 5
			- We can insert many pairs of basis transformations (invertible operators) inverse to each other. The contraction would be exactly the same.
			-
		- Double Tensor
		  card-last-interval:: 28.64
		  card-repeats:: 1
		  card-ease-factor:: 2.6
		  card-next-schedule:: 2023-08-31T03:55:27.634Z
		  card-last-reviewed:: 2023-08-02T12:55:27.634Z
		  card-last-score:: 5
			- $$
			  \mathbb{T}_{\alpha \ldots \gamma, \tilde{\alpha} \ldots \tilde{\gamma}}=\sum_i T_{\alpha \ldots \gamma}^i\left(T_{\tilde{\alpha} \ldots \tilde{\gamma}}^i\right)^*
			  $$
	- ## Basic Facts
	  collapsed:: true
		- Norm and expectation value #card
		  collapsed:: true
		  card-last-interval:: 31.21
		  card-repeats:: 1
		  card-ease-factor:: 2.6
		  card-next-schedule:: 2023-09-08T17:59:14.105Z
		  card-last-reviewed:: 2023-08-08T12:59:14.105Z
		  card-last-score:: 5
			- Norm: ((64c6719d-c663-4af8-9ba7-ad5ae575886e))
			  collapsed:: true
				- Intuitively, the lower layer is the complex conjugate.
				  'Connecting physical indices' corresponds to 'sum over basis states'.
			- collapsed:: true
			  $$
			  \langle\psi \mid \psi\rangle=\operatorname{tTr}(\mathbb{T}[1] \mathbb{T}[2] \ldots \mathbb{T}[m] \ldots)
			  $$
				- Proof
				  collapsed:: true
					- $$\begin{aligned}
					  \langle \psi |\psi \rangle  & =\sum _{i_{1} ,i_{2} ,\dotsc ,i_{N}} |\operatorname{Tr}\left( A_{i_{1}}^{[1]} A_{i_{2}}^{[2]} \dotsc A_{i_{N}}^{[N]}\right) |^{2}\\
					   & =\sum _{i_{1} ,i_{2} ,\dotsc ,i_{N}}\operatorname{Tr}\left( A_{i_{1}}^{[1]} A_{i_{2}}^{[2]} \dotsc A_{i_{N}}^{[N]}\right)\operatorname{Tr}\left( A_{i_{1}}^{[1]*} A_{i_{2}}^{[2]*} \dotsc A_{i_{N}}^{[N]*}\right)\\
					   & =\sum _{i_{1} ,i_{2} ,\dotsc ,i_{N}}\operatorname{Tr}\left\{\left( A_{i_{1}}^{[1]} \otimes A_{i_{1}}^{[1]*}\right)\left( A_{i_{2}}^{[2]} \otimes A_{i_{2}}^{[2]*}\right) \dotsc \left( A_{i_{N}}^{[N]} \otimes A_{i_{N}}^{[N]*}\right)\right\}\\
					   & =\operatorname{Tr}\left\{\left(\sum _{i_{1}} A_{i_{1}}^{[1]} \otimes A_{i_{1}}^{[1]*}\right)\left(\sum _{i_{2}} A_{i_{2}}^{[2]} \otimes A_{i_{2}}^{[2]*}\right) \dotsc \left(\sum _{i_{N}} A_{i_{N}}^{[N]} \otimes A_{i_{N}}^{[N]*}\right)\right\}
					  \end{aligned}$$
			- Expectation value: ((64c671a5-c090-4c8e-978a-74d7b28a32e7))
			  collapsed:: true
			- $$
			  \langle O\rangle=\frac{\operatorname{tTr}\left(\mathbb{T}[1] \mathbb{T}[2] \ldots \mathbb{T} \mathbb{T}_O[n] \ldots \mathbb{T}[m] \ldots\right)}{\operatorname{tTr}(\mathbb{T}[1] \mathbb{T}[2] \ldots \mathbb{T}[n] \ldots \mathbb{T}[m] \ldots)}
			  $$
				- $$
				  \left(\mathbb{T}_O\right)_{\alpha \ldots \gamma, \tilde{\alpha} \ldots \tilde{\gamma}}=\sum_{i, j} O_{i j} T_{\alpha \ldots \gamma}^i\left(T_{\tilde{\alpha} \ldots \tilde{\gamma}}^j\right)^*
				  $$
				- The proof is very much the similar.
		- collapsed:: true
	- ## [[Toric Code]] and Symmetry of TPS #card
	  collapsed:: true
	  card-last-interval:: 31.26
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2023-12-30T07:28:39.776Z
	  card-last-reviewed:: 2023-11-29T01:28:39.777Z
	  card-last-score:: 5
		- *Symmetry is indeed a great concept, but does the classical Z-flipping properly capture the notion?
		  background-color:: pink
		- Notes
			- The idea still comes from anyon strings.
			- Obviously the spirit is quite similar to the construction of parent Hamiltonians. We just interpret terms in the frustration-free Hamiltonian as 'constraint tensors'.
			- The construction is easily generalized to Levin-Wen models.
		- ### TPS
		  collapsed:: true
			- Vertex tensor
				- No physical index.
				- $T_{i j k l}=1$, if $i+j+k+l=0 \bmod 2$
				- $T_{i j k l}=0$, if $i+j+k+l=1 \bmod 2$
			- Edge tensor
				- $t_{00}^0=t_{11}^1=1$, all other terms are 0.
			- ((64c7f62b-6d6a-426f-b022-07220a9f00e5))
			- Proof
				- Vertex tensors enforce the constraint of 'no broken strings'.
				  collapsed:: true
				- The two physical states of the edge tensors corresponds to *string* and *no string* respectively.
		- ### The $Z_2$ symmetry
			- Z does nothing to the tensor when the index is 0 and changes the sign of the tensor when the index is 1.
			- Obviously both the vertex and edge tensors have $Z_2$ symmetry in the proper sense:
			  ((64c7f701-9cf6-458b-9e95-98079b6c4aff))
		- ### Basic Facts
		  collapsed:: true
			- Proposition. The symmetry prevents the tensor network from being injective, since only symmetric tensor states are allowed.
				-
			- Note that the symmetry could be extended to the Hilbert space, i.e. $Z$ acting on inner indices <-> $\sigma_Z$ acting on edges.
				- However, since tensor networks are discrete and 'classical', the operator is restricted by the classical configurations.
		- ### Stability and Symmetry
		  collapsed:: true
			- A bit problematic when calculating the norms of Schmidt states. Further investigation needed.
			  background-color:: red
			- Summary
				- Break the symmetry of vertex tensors by a small perturbation.
				- Calculate the EE by calculating the weights of different boundary configurations.
				- Examine the behavior at $N \to \infty$.
				  We should see the disappearance of TEE (subleading term).
			- We modify all vertex tensors a bit by 
			  $$T_{i j k l}=1,\text{if} \quad i+j+k+l=0 \bmod 2 \\
			  T_{i j k l}=\varepsilon, \text{if} \quad i+j+k+l=1 \bmod 2$$
			  and see the result.
			- Calculate EE
				- First note that the states factor according to boundary configurations,
				  $$
				  \left|\psi_{\text {toric code }}^{\varepsilon}\right\rangle=\sum_b \beta_b\left|\phi_b^{\text {out }}\right\rangle\left|\phi_b^{\text {in }}\right\rangle
				  $$
					- Our task is to calculate: (1) The norms of $\beta_b$ (2) The norm of the whole state
				- Calculate (2)
				  collapsed:: true
					- To calculate the norm, form the double tensor $\mathbb{T}$ and $\mathbb{S}$ as
					  $$
					  \mathbb{T}_{i j k l, i^{\prime} j^{\prime} k^{\prime} l^{\prime}}=T_{i j k l} \times T_{i^{\prime} j^{\prime} k^{\prime} l^{\prime}}^*, \mathbb{S}_{i j, i^{\prime} j^{\prime}}=\sum_n t_{i j}^n\left(t_{i^{\prime} j^{\prime} j^{\prime}}^n\right)^*
					  $$
					- Combine each $\mathbb{T}$ with the four $\mathbb{S}$ around it, we obtain the double tensor $\mathbb{T}^{\prime}$
					  $$
					  \begin{aligned}
					  & \mathbb{T}_{i j k l, i^{\prime}=i}^{\prime} j^{\prime}=j k^{\prime}=k l^{\prime}=l=1, \quad \text { if } i+j+k+l=0 \bmod 2 ; \\
					  & \mathbb{T}_{i j k l, i^{\prime}=i}^{\prime} j^{\prime}=j k^{\prime}=k l^{\prime}=l=\varepsilon^2, \quad \text { if } i+j+k+l=1 \bmod 2
					  \end{aligned}
					  $$
					- Contracting the $\mathbb{T}^{\prime}$ tensors on each site gives us the norm of the wave function.
						- It happens that such a contraction can be done easily with a **change of basis** for the inner indices. For each pair of inner indices $i i^{\prime}, j j^{\prime}, k k^{\prime}, l l^{\prime}$, apply transformation
						  $$
						  |00\rangle+|11\rangle \rightarrow|\tilde{0}\rangle,|00\rangle-|11\rangle \rightarrow|\tilde{1}\rangle
						  $$
						  $\mathbb{T}^{\prime}$ is transformed into
						  $$
						  \mathbb{T}_{\tilde{0} 0 \tilde{0} \tilde{0}}^{\prime}=\frac{1+\varepsilon^2}{2}, \mathbb{T}_{\tilde{1} \tilde{1} \tilde{1} \tilde{1}}^{\prime}=\frac{1-\varepsilon^2}{2} \text {, all other terms are zero }
						  $$
					- Obviously, this tensor network can be contracted easily and gives the norm of the wave function
					  $$
					  \text { norm }=\left\langle\psi_{\text {toric code }}^{\varepsilon} \mid \psi_{\text {toric code }}^{\varepsilon}\right\rangle=2^N\left(1+\varepsilon^2\right)^N+2^N\left(1-\varepsilon^2\right)^N
					  $$
				- Calculate (1)
					- The technique is the same and we obtain
					  $$
					  \left|\beta_b\right|^2=\frac{2^N}{2^m}\left(\left(1+\varepsilon^2\right)^N+\left(1-\varepsilon^2\right)^N+\left(1+\varepsilon^2\right)^{N_i}\left(1-\varepsilon^2\right)^{N_o}+\left(1-\varepsilon^2\right)^{N_i}\left(1+\varepsilon^2\right)^{N_o}\right)
					  $$
						- $N_i$ is the number of vertices inside a region and $N_o$ is the number of vertices outside the region.
						- Independent of the boundary configuration?!
						  background-color:: red
					- Taking the limit of large system size $N_i \rightarrow \infty, N \rightarrow \infty$
					  $$
					  \left|\beta_b\right|^2 / \text { norm }=\frac{1}{2^m}
					  $$
			- Therefore $S=m$ and **TEE is zero**.
	- ## Examples
		- 2D Ising and Symmetry Breaking
			- $$
			  H^{\mathrm{tIsing}}=-J \sum_{<i j>} Z_i Z_j
			  $$
			- TPS:
			  $$
			  T_{0000}^{\uparrow}=1, T_{1111}^{\downarrow}=1, \text { all other terms being } 0
			  $$
				- $$
				  \left|\psi_{\mathrm{GHZ}}\right\rangle=\frac{1}{\sqrt{2}}(|00 \ldots 0\rangle+|11 \ldots 1\rangle)
				  $$
			- Observation. Simultaneous block-diagonalizability of all tensors implies symmetry breaking.
				- It seems fairly trivial, since block-diagonal tensors imply long-range entangled states.
		-