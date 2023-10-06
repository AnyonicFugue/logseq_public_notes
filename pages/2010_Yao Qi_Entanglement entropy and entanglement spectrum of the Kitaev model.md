type:: paper_reading

- ![2010_Yao_Qi_Entanglement entropy and entanglement spectrum of.pdf](file://zotero_link/Research/TO in Kitaev Honeycomb/2010_Yao_Qi_Entanglement entropy and entanglement spectrum of.pdf)
- # Observations and Comments
	- The Renyi entropy of the gauge part is independent of the order. Thus we may calculate an arbitrary Renyi entropy for convenience.
		- However the fermion part depends on the order.
	- There is a numerical algorithm for the EE of the fermion part, thus MESs might be found numerically.
- # Derivation of the EE
	- ## Setup
	  collapsed:: true
		- Parition of the lattice
		  collapsed:: true
			- ((64dcdcd8-ac6a-4c83-b30b-6fb12670cf8b))
			- We regroup those gauge fields on the boundary links to introduce new Z2 gauge variables which lives in A and B exclusively.
		- We suppose the boundary length is $2L$.
		- Links across the boundary
		  $$
		  \overline{a_n b_n}, n=1, \cdots 2 L
		  $$
		- Transformed gauge field
		  collapsed:: true
			- $$
			  \hat{w}_{A, n}=i \gamma_{a_{2 n-1}}^\alpha \gamma_{a_{2 n}}^\beta
			  $$
			- $$
			  \hat{w}_{B, n}=i \gamma_{b_{2 n-1}}^\alpha \gamma_{b_{2 n}}^\beta
			  $$
			- This is a 'reconnection' of the gauge fields.
		- Gauge configuration
		  collapsed:: true
		  $$
		  |u\rangle=\left|u_A, u_B, u_p\right\rangle
		  $$
			- $\left|u_A\right\rangle,\left|u_B\right\rangle$, and $\left|u_p\right\rangle$ are gauge fields in $A, B$, and those across the boundary respectively.
		- Separation of gauge transformations into two parts:
		  collapsed:: true
		  $$
		  X_g=i^{|g|(|g|-1) / 2} \prod_{i \in q} \gamma_j^x \gamma_j^y \gamma_j^z \quad Y_g=i^{|g|(|g|-1) / 2} \prod_{i \in q} \eta_j
		  $$
			- $g$ is the region to be gauge transformed and $|g|$ denotes to the number of sites in $g$.
			  collapsed:: true
				- $$
				  |\Psi\rangle=\frac{1}{\sqrt{2^{N+L+1}}} \sum_{g, w_A=w_B} D_g\left|u_A, w_A ; u_B, w_B\right\rangle|\phi(u)\rangle
				  $$
			- The ordering of sites in the two products is implicitly taken to be the same such that $X_q Y_q=D_q$.
			- Intuitively, $X_g$ is the gauge field transformation while $Y_g$ is the majorana field transformation. Combining them restores the gauge transformations $D_j$.
			- Note that $X_g^2=Y_g^2=1$.
		- collapsed:: true
		  $$
		  X_g=(-i)^{\left|g_A\right|\left|g_B\right|} X_{g_B \equiv g \cap B} X_{g_A \equiv g \cap A} \text { and } Y_g=i^{\left|g_A\right|\left|g_B\right|} Y_{g_A} Y_{g_B}
		  $$
			- $A$ and $B$ are two parts of the lattice in the bipartition.
			- Note that $X$ is B first A second and $Y$ is A first B second, so there is an extra minus.
		- Fermion-parity projectors in two regions:
		  collapsed:: true
		  $$
		  P_{A, F}^{x_A(w)}=\frac{1+x_A(w) Y_A}{2},P_{B, F}^{x_B(w)}=\frac{1+x_B(w) Y_B}{2}
		  $$
			- $F$ stands for fermion.
			- $x_A(w)$ denotes the total fermion parity in region $A$.
			  collapsed:: true
			  Note that the fermion parity depends on $w$, the reconnected gauge fields.
				- The reconnected gauge fields $w$ are a large superposition.
	- Finding the appropriate basis to rewrite the ground state
	  collapsed:: true
		- Proposition. 
		  collapsed:: true
		  $$
		  \left| \forall p,u_p =1\right\rangle=\frac{1}{\sqrt{2^L}} \sum_{w_{An}=w_{Bn}=\{ \pm 1\}}\left|w_A, w_B\right\rangle
		  $$
			- Note that the states in RHS could be redefined up to a phase.
			- For general values of $u$, the only change are the signs of RHS terms.
			  collapsed:: true
				- However, to obtain MES, it is crucial how the signs change and how to work out the superposition.
			- Therefore the theorem actually says that any definite boundary configuration corresponds to an equal-amplitude superposition.
			- Proof. Draw a minimal case of 4 majoranas. The general case follows.
		-
		- Therefore we could rewrite the wavefunction:
		  collapsed:: true
		  $$
		  |\Psi\rangle=\frac{1}{\sqrt{2^{N+L+1}}} \sum_{g, w_A=w_B} D_g\left|u_A, w_A ; u_B, w_B\right\rangle|\phi(u)\rangle
		  $$
			- $|\phi(u)\rangle$ is the free fermion part.
			- Q: Why $|\phi(u)\rangle$ doesn't depend on $w$?
			  collapsed:: true
				- First of all, the wavefunction could be rewritten as
				  $$\sum_{\{u\}} |u\rangle \otimes |\phi(u)\rangle$$
				- We just selected a **single** $\{u\}$ and rewrite it as
				  $$|u\rangle=\sum_w |u_A; u_B; w\rangle$$
		- By factoring the gauge field transformation and the majorana field transformation, we may write
		  collapsed:: true
		  $$
		  \begin{aligned}
		  |\Psi\rangle & =\frac{1}{\sqrt{2^{N+L+1}}} \sum_{g, w_A=w_B} X_g\left|u_A, w_A ; u_B, w_B\right\rangle \otimes Y_g|\phi(u)\rangle, \\
		  & =\frac{1}{\sqrt{2^{N+L+1}}} \sum_{g, w} X_{g_B}\left|u_B, w\right\rangle \otimes  X_{g_A}\left|u_A, w\right\rangle \otimes  Y_{g_A} Y_{g_B}|\phi(u)\rangle
		  \end{aligned}
		  $$
			- $u$ is the standard configuration with all $u=1$.
			- In the last line we divided the gauge configuration into A-part and B part. 
			  Also we denoted $w_A=w_B$ as $w$.
	- Calculate the reduced density matrix
	  collapsed:: true
		- collapsed:: true
		  $$
		  \begin{aligned}
		  \rho_A & =\operatorname{Tr}_B[|\Psi\rangle\langle\Psi|] \\
		  & =\frac{1}{2^{N+L+1}} \sum_{g, g^{\prime}, w, w^{\prime}}\left\langle u_B, w^{\prime}\left|X_{g_B^{\prime}}^{\dagger} X_{g_B}\right| u_B, w\right\rangle X_{g_A}\left|u_A, w\right\rangle\left\langle u_A, w^{\prime}\right| X_{g_A^{\prime}}^{\dagger} \cdot \operatorname{Tr}_{B, F}\left[Y_{g_A} Y_{g_B}|\phi(u)\rangle\langle\phi(u)| Y_{g_B^{\prime}}^{\dagger} Y_{g_A^{\prime}}^{\dagger}\right]
		  \end{aligned}
		  $$
			- The gauge part and the fermion part are explicitly separated.
			- The reduced density matrix of the gauge part of $B$ is $X_{g_B}\left |u_B,w\right\rangle \left\langle u_B, w^{\prime}\right|X_{g_B^{\prime}}^{\dagger}$. 
			  collapsed:: true
			  Taking trace is just taking the inner product of the bra and ket.
				- Proof. Express the trace by a basis.
		- Proposition. 
		  collapsed:: true
		  $$
		  \left\langle u_B, w^{\prime}\left|X_{g_B^{\prime}}^{\dagger} X_{g_B}\right| u_B, w\right\rangle=\delta_{w, w^{\prime}}\left(\delta_{g_B^{\prime}, g_B}+x_B(w) \delta_{g_B^{\prime}, B-g_B}\right)
		  $$
			- Intuition
			  collapsed:: true
				- This means the configurations by different gauge transformations are **almost orthogonal**.
				  They are orthogonal if we rule out the redundant ones.
				- However, $\prod_j D_j$ is **not** the identity operator.
				  collapsed:: true
					- It doesn't alter gauge field configurations and commute with $c_i c_j$, but since different $c_i c_j$ anti-commute, they can't have definite eigenvalues simultaneously.
					- Therefore $D_j$ could add different phases to different eigenstates of $c_i c_j$.
			- The first term in the parenthesis means that $w=w'$ thus $X_{gB}$ and $X_{g'B}$ are identical.
			- The second term means that $X_{gB}$ and $X_{g'B}$ differs by **all gauge transformations in B**.
			  Since we have reconnected the edges, the total effect is a scalar factor $x_B(w)$ and the configuration isn't changed.
			- collapsed:: true
			  $$
			  x_B(w)=\left\langle u_B, w\left|X_{B-g_B}^{\dagger} X_{g_B}\right| u_B, w\right\rangle=\left\langle u_B, w\left|X_B\right| u_B, w\right\rangle=\prod_{{i j}\in B} u_{i j} \prod_{n=1}^L w_n
			  $$
				- The product of all edges in the region.
		- Therefore,
		  collapsed:: true
		  $$
		  \begin{aligned}
		  \rho_A & =\frac{1}{2^{N+L+1}} \sum_{g_A, g_A^{\prime}, w} \sum_{g_B} X_{g_A}\left|u_A, w\right\rangle\left\langle u_A, w\right| X_{g_A^{\prime}}^{\dagger} \cdot Y_{g_A} \operatorname{Tr}_{B, F}\left[|\phi(u)\rangle\langle\phi(u)|\left(1+Y_B\right)\right] Y_{g_A^{\prime}}^{\dagger} \\
		  & =\frac{1}{2^{N_A+L}} \sum_{g_A, g_A^{\prime}, w} X_{g_A}\left|u_A, w\right\rangle\left\langle u_A, w\right| X_{g_A^{\prime}}^{\dagger} \cdot Y_{g_A} \operatorname{Tr}_{B, F}\left[|\phi(u)\rangle\langle\phi(u)|\left(\frac{1+x_B(w) Y_B}{2}\right)\right] Y_{g_A^{\prime}}^{\dagger} \\
		  &=\frac{1}{2^{N_A+L}} \sum_{g_A, g_A^{\prime}, w} X_{g_A}\left|u_A, w\right\rangle\left\langle u_A, w\right| X_{g_A^{\prime}}^{\dagger} \cdot Y_{g_A} \operatorname{Tr}_{B, F}\left[|\phi(u)\rangle\langle\phi(u)|\left(P_{B, F}^{x_B(w)}\right)\right] Y_{g_A^{\prime}}^{\dagger} 
		  \end{aligned}
		  $$
			- Proposition.
			  collapsed:: true
			  $$\operatorname{Tr}_{B,F}\left[ Y_{g_{B}} |\phi (u)\rangle \langle \phi (u)|\left(\frac{1+x_{B} (w)Y_{B}^{\dagger }}{2}\right) Y_{g_{B}}^{\dagger }\right] =\langle \phi (u)|\left(\frac{1+x_{B} (w)Y_{B}^{\dagger }}{2}\right) |\phi (u)\rangle $$
				- Note that $Y_g^\dagger=Y_g$.
			- Therefore the terms are all identical for different $g_B$. That's why $N$ becomes $N_A$.
	-
	- Notes
	  collapsed:: true
		- The partial trace on $B$ doesn't depend on the gauge configuration.
	-
	- Employ the replica trick
		- Start from
		  $$\begin{aligned}
		  \rho _{A} & =\frac{1}{2^{N_{A} +L}}\sum _{g_{A} ,g_{A}^{\prime } ,w} X_{g_{A}}| u_{A} ,w> < u_{A} ,w| X_{g_{A}^{\prime }}^{\dagger } \otimes Y_{g_{A}}\operatorname{Tr}_{B,F}\left[ |\phi (u)\rangle \langle \phi (u)|\left( P_{B,F}^{x_{B} (w)}\right)\right] Y_{g_{A}^{\prime }}^{\dagger }
		  \end{aligned}$$
		- We have
		  collapsed:: true
		  $$\begin{aligned}
		  \rho _{A}^{2} & =\frac{1}{2^{2( N_{A} +L)}}\sum _{g_{1A} ,g_{1A}^{\prime } ,w_{1}}\sum _{g_{2A} ,g_{2A}^{\prime } ,w_{2}} X_{g_{1A}}| u_{A} ,w_{1}> < u_{A} ,w_{1}| X_{g_{1A}^{\prime }}^{\dagger } X_{g_{2A}}| u_{A} ,w_{2}> < u_{A} ,w_{2}| X_{g_{2A}^{\prime }}^{\dagger }\\
		   & \otimes Y_{g_{1A}}\operatorname{Tr}_{B,F}\left[ |\phi (u)\rangle \langle \phi (u)|\left( P_{B,F}^{x_{B} (w_{1} )}\right)\right] Y_{g_{1A}^{\prime }}^{\dagger } Y_{g_{2A}}\operatorname{Tr}_{B,F}\left[ |\phi (u)\rangle \langle \phi (u)|\left( P_{B,F}^{x_{B} (w_{2} )}\right)\right] Y_{g_{2A}^{\prime }}^{\dagger }
		  \end{aligned}$$
			- The key is that 
			  $$< u_{A} ,w_{1}| X_{g_{1A}^{\prime }}^{\dagger } X_{g_{2A}}| u_{A} ,w_{2}> =\delta _{w_{1} ,w_{2}}( \delta _{g_{1A}^{\prime } ,g_{2A}} +x( w_{1}) \delta _{g_{1A}^{\prime } ,A-g_{2A}})$$
			  which is already used in simplifying the reduced density matrix.
		-
		- Plugging in the delta functions, we obtain
		  $$
		  \rho_A^2=\frac{1}{2^{N_A+2 L-1}} \sum_{g_A, g_A^{\prime}, w} X_{g A}\left|u_A, w\right\rangle\left\langle u_A, w\right| X_{g^{\prime} A}^{\dagger} \cdot Y_{g A} \rho_{A, F}^{x_B(w)} P_{A, F}^{x_A(w)} \rho_{A, F}^{x_B(w)} Y_{g^{\prime} A}
		  $$
		-
		- Similarly, we have
		  $$\rho_A^n=\frac{1}{2^{N_A+n L-n+1}} \sum_{g_A, g_A^{\prime}, w} X_{g A}\left|u_A, w\right\rangle\left\langle u_A, w\right| X_{g^{\prime} A} \cdot Y_{g A} \rho_{A, F}^{x_B(w)}\left(P_{A, F}^{x_A(w)} \rho_{A, F}^{x_B(w)}\right)^{n-1} Y_{g^{\prime}}$$
		- $$
		  \operatorname{Tr}_A\left[\rho_A^n\right]=\frac{1}{2^{n(L-1)}} \sum_w \operatorname{Tr}_A\left(P_{A, F}^{x_A(w)} \rho_{A, F}^{x_B(w)}\right)^n
		  $$
		- Note that the $2^L$ configurations of $w$ could be divided into two equal parts corresponding to different parities.
		- $$
		  \begin{aligned}
		  \operatorname{Tr}_{A}\left[ \rho _{A}^{n}\right] & =\frac{1}{2^{(n-1)(L-1)}}\operatorname{Tr}_{A}\left[\left( P_{A,F}^{p_{A}} \rho _{A,F}^{p_{B}}\right)^{n} +\left( P_{A,F}^{-p_{A}} \rho _{A,F}^{-p_{B}}\right)^{n}\right]\\
		   & =\frac{1}{2^{(n-1)(L-1)}}\operatorname{Tr}_{A}\left[\left( P_{A,F}^{p_{A}} \rho _{A,F}^{p_{B}}\right) +\left( P_{A,F}^{-p_{A}} \rho _{A,F}^{-p_{B}}\right)\right]^{n}\\
		   & =\frac{1}{2^{(n-1)(L-1)}}\operatorname{Tr}_{A}\left[ \rho _{A,F}^{n}\right]
		  \end{aligned}
		  $$
			- $\rho_{A, F}=\rho_{A, F}^{+}+\rho_{A, F}^{-}=\operatorname{Tr}_B[|\phi(u)\rangle\langle\phi(u)|]$ is the **free** fermion density matrix without fermion number parity constraint in the $\mathrm{B}$ region.
			- To obtain the second line from the first line, we note that the cross terms vanish due to projections to different fermion parities.
		- Obviously the prefactor corresponds to the $Z_2$ gauge field
		-
- The derivation of the TEE is indeed dazzling. I should make some sense out of it. #card
  background-color:: yellow
  card-last-interval:: 31.26
  card-repeats:: 1
  card-ease-factor:: 2.36
  card-next-schedule:: 2023-10-08T07:11:18.056Z
  card-last-reviewed:: 2023-09-07T01:11:18.057Z
  card-last-score:: 3
	- Which are the key points?
		- Transform the gauge field
	- Which properties are used?
		- In taking the partial trace, if $\rho=|A\rangle \langle B|$, then 
		  $$\operatorname{Tr}(\rho)=\sum_i \langle e_i | A\rangle \langle B |e_i \rangle=\sum_i \langle B  |e_i \rangle\langle e_i | A \rangle$$
			- i.e. Commutativity of scalars
		-
- Result
  collapsed:: true
	- $$
	  \operatorname{Tr}_A\left[\rho_A^n\right]=\operatorname{Tr}_{A, G}\left[\rho_{A, G}^n\right] \cdot \operatorname{Tr}_{A, F}\left[\rho_{A, F}^n\right]
	  $$
		- Here $\rho_{A, F}=\operatorname{Tr}_B[|\phi(u)\rangle\langle\phi(u)|]$ and $\rho_{A, G}=\operatorname{Tr}_B[|G(u)\rangle\langle G(u)|]$ are the reduced density matrices for the **free** Majorana fermion state $|\phi(u)\rangle$, and a pure $Z_2$ gauge field, respectively,
		- The ground state of the $Z_2$ gauge field $|G(u)\rangle$ is given by a equal weight superposition of all the $2^{N-1}$ gauge field configurations $|\tilde{u}\rangle$ that are gauge equivalent to $|u\rangle$, i.e., $|G(u)\rangle=2^{-(N-1) / 2} \sum_{\tilde{u} \simeq u}|\tilde{u}\rangle$.
	- Then the EE could be separated into the gauge part and the fermion part.
		- Explicit calculation shows that $S_G=(L-1) \log 2$ and the fermion part has the form $S_F=\alpha L+o(1)$, where $\alpha$ is a positive constant and $o(1)$ represents terms which vanish as $L \rightarrow \infty$.
	- In the thermodynamic limit, the total entanglement entropy is given by
	  $$
	  S=(\alpha+\log 2) L-\log 2
	  $$
		- Note that the quantum dimensions of TC and ising are identical, both 2.
	-
	- Physically, such a simplification occurs because the effect of the gauge transformation $D_g$ on the fermion state in region $B$ is canceled out once the trace over gauge field configurations is taken.
		- But in toric code we could also view vertices as gauge transformations. Would the same occur?