- ![2015_Zhang_Grover_Vishwanath_General procedure for determining braiding and.pdf](file://zotero_link/Research/TO in Kitaev Honeycomb/Anyon Data from Microscopic Data/2015_Zhang_Grover_Vishwanath_General procedure for determining braiding and.pdf)
-
- #+BEGIN_NOTE
  The key point is that EE is a **nonlinear** data, which could be used to distinguish different sets of basis.
  Also it is already shown to be robust, thus highly applicable.
  #+END_NOTE
-
-
- # Setup
	- Minimum entropy state $\left\{\left|\Xi_a^{(\alpha)}\right\rangle\right\} \equiv\left|\Xi^{(\alpha)}\right\rangle$
		- The MES basis for a bipartition $\alpha$
	- Orthonormal basis of the ground space $|\xi_a \rangle$
		- The MES is related to the basis by $\left|\Xi_b^{(\alpha)}\right\rangle=e^{i \phi_b^{(\alpha)}} U_{a b}^{(\alpha)} \mid \xi_a \rangle$
		- $$
		  V^{(\alpha)}=\operatorname{diag}\left(e^{i \phi_b^{(\alpha)}}\right)
		  $$
		-
		- In view of the arbitrary permutations of MESs, we should rewrite it as
		  $$
		  U_{a b}^{(\alpha)}=\bar{U}_{a b^{\prime}}^{(\alpha)} P_{b^{\prime} b}^{(\alpha)}, \quad\left|\Xi_b^{(\alpha)}\right\rangle=\bar{U}_{a b^{\prime}}^{(\alpha)} V_{b^{\prime} b^{\prime}}^{(\alpha)} P_{b^{\prime} b}^{(\alpha)}\left|\xi_a\right\rangle
		  $$
		  where $P^{(\alpha)}$ is a permutation matrix.
	- Nontrivial loops $T^\alpha_a$
		- $\alpha$ denotes the bipartition
		- $a$ denotes the quasiparticle
	- Modular transformation $\mathcal F(S,U)$
	  collapsed:: true
		- Note that $S$ is shearing and $U$ is the Dehn twist.
			- Don't forget that $U^\alpha$ also denotes the coefficients of the MESs!
		- Also viewed as a transformation between primitive vectors, from the primitive vectors $\vec{w}_{i=1,2}^{(1)}$ in to $\vec{w}_{i=1,2}^{(2)}$
			- In the special case ((651a659e-4772-4b4e-927a-58b269fb9640)) , the transformation can be identified with
			  $$
			  S=\left(\begin{array}{rr}
			  0 & 1 \\
			  -1 & 0
			  \end{array}\right)
			  $$
	- Third entanglement bipartition:
	  collapsed:: true
	  $$
	  \vec{w}_2^{(3)}=\vec{w}_2^{(1)}+\vec{w}_2^{(2)}
	  $$
		- ((651a6af9-ff1b-42b4-907b-0634cd8936e5))
		- Obviously corresponding to a twist.
- # Key Observations
	- Proposition. The ground states having minimum EE (with respect to a non-contractible cut of the lattice) have pure anyon fluxes.
		- TODO Verify by toric code.
	- Theorem. The modular $S$ matrix is given by the overlap between MESs corresponding to bipartitions in $x$ and $y$ direction respectively:
	  $$
	  \mathcal{S}_{a b}=\left\langle\Xi_a^{(1)} \mid \Xi_b^{(2)}\right\rangle
	  $$
		- This procedure can be further simplified in the presence of certain rotation symmetry $R$, which relates the two sets MESs $\left|\Xi^{(2)}\right\rangle=R\left|\Xi^{(1)}\right\rangle$. For example, $R_{\pi / 2}: \hat{x} \rightarrow \hat{y}$ gives $\mathcal{S}=\left\langle\Xi^{(1)}\left|R_{\pi / 2}\right| \Xi^{(1)}\right\rangle$.
		- On the other hand, there might be some undetermined phase factors, which can be fixed by the requirement that all $S$ matrix elements related to the identity quasiparticle are $1$.
		-
		- In view of the possible permutations, we should rewrite it as
		  $$
		  \mathcal{S}=\left(P^{(2)}\right)^{-1}\left(V^{(2)}\right)^{-1}\left(\bar{U}^{(2)}\right)^{-1} \bar{U}^{(1)} V^{(1)} P^{(1)}
		  $$
		- How to fix the ordering?
		  background-color:: red
			- Essentially calculate the T matrix and diagonalize it.
			- Another method is to use Verlinde formula to find the fusion rule, which is of partial help.
	- Theorem. With the third bipartition, we can overcome the ordering problem and fix the $S$ matrix by
	  $$
	  \begin{aligned}
	  \mathcal{S}= & \left\{R\left[\left(\bar{U}^{(2)}\right)^{-1} \bar{U}^{(1)}\right]\right\}^{-1} R\left[\left(\bar{U}^{(2)}\right)^{-1} \bar{U}^{(3)}\right] \\
	  & \times R\left[\left(\bar{U}^{(3)}\right)^{-1} \bar{U}^{(1)}\right] .
	  \end{aligned}
	  $$
	-
- # T matrix
	- Proposition. With a $2\pi/3$ rotational symmetry, the T matrix is determined via $\mathcal{T S}=$ $\left\langle\Xi^{(1)}\left|R_{2 \pi / 3}\right| \Xi^{(1)}\right\rangle$.
	- In addition, we can extract the chiral central charge by
	  $$
	  \mathcal{T}_a=\theta_a \exp (-i 2 \pi c / 24) \\
	  (TS)^3=1
	  $$
	- This paper **cannot** uniquely pin down the $T$ matrix, but the later paper by Francuz did this.
-
-
-