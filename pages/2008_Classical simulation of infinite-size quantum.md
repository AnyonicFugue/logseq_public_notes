- ![2008_Jordan_Orus et al_Classical simulation of infinite-size quantum.pdf](file://zotero_link/Physics/Numerical Methods/TEBD/2008_Jordan_Orus et al_Classical simulation of infinite-size quantum.pdf)
  title:: 2008_Classical simulation of infinite-size quantum
- # Setup
	- ## Notations
		- $\mathcal E$ is the network of double tensors
		- $\mathcal{E}^{\left[\vec{r}_1, \vec{r}_2\right]}$ is the **environment** obtained by removing the double tensors $a^{\left[\vec{r}_1\right]}$ and $a^{\left[\vec{r}_2\right]}$.
	- $$
	  H=\sum_{\vec{r}_1, \vec{r}_2} h^{\left[\vec{r}_1 \vec{r}_2\right]}
	  $$
		- The Hamiltonian is a sum of local terms that only involve nearest neighbor sites.
		  I think the principle could be easily extended to more-body interactions (or simply use the magnetic field).
	- Double tensor
	  $$
	  a_{\bar{u} \overline{d l} \bar{r}}^{[\vec{r}]} \equiv \sum_s A_{s u d l r}^{[\vec{r}]}\left(A_{s u^{\prime} d^{\prime} l^{\prime} r^{\prime}}^{[\vec{r}]}\right)^*
	  $$
	- Translationally invariant system
	  ((65142b4a-44a2-4263-aa94-46cec449c012))
		- a,b are the double tensors corresponding to $A$ and $B$.
- Key Claims
	- ((65142b26-ea97-414e-8aa0-cfbb3f2c2267))
	-
- # The Approximation
	- First we approximate the environment $\mathcal{E}^{\left[\vec{r}_1, \vec{r}_2\right]}$ with an infinite strip $\mathcal{F}^{\left[\vec{r}_1, \vec{r}_2\right]}$; then we approximate $\mathcal{F}^{\left[\vec{r}_1, \vec{r}_2\right]}$ with a small set of tensors $\mathcal{G}^{\left[\vec{r}_1, \vec{r}_2\right]}=\left\{G_1, \cdots, G_6\right\}$.
		- ((65142bc0-4700-4a20-bc2f-ed6b1aaf1b85))
			- First approximate the environment
			- Then approximate the strip
	- [Step 1.](((65142c4c-ffbf-48cf-878d-85e251503d92))) Consider a transfer matrix $R$ consisting of an infinite strip of reduced tensors $a$ and $b$
	  collapsed:: true
		- $R$ can be regarded as a linear operator acting on an infinite chain where each site is described by a vector space of dimension $D^2$.
			- ((65142ce1-1146-4537-98ba-a4e564d9c34b))
		- Let $|\Phi\rangle$ denote the **dominant eigenvector** of $R$.
			- The eigenvector of $R, R|\Phi\rangle=\lambda|\Phi\rangle$, with the eigenvalue $\lambda$ of largest eigenvalue.
		- By construction $R$ is invariant under shifts by two sites of the infinite chain - and so is $|\Phi\rangle$.
		- Dominant vectors
			- We use an iMPS, characterized by just two tensors $\{C, D\}$ and with Schmidt rank $\chi$, to represent an approximation of $|\Phi\rangle$.
				- We obtain this iMPS by simulating (repeated) multiplication by $R$ on an initial state $\left|\Phi_0\right\rangle$ with the iTEBD algorithm and
				  $$
				  |\Phi\rangle=\lim _{p \rightarrow \infty} \frac{R^p\left|\Phi_0\right\rangle}{\| R^p\left|\Phi_0\right\rangle \|}
				  $$
			- Similarly, we use another iMPS with ensors $\left\{C^{\prime}, D^{\prime}\right\}$ to encode the left dominant eigenvector $\left\langle\Phi^{\prime}\right|$ of $R,\left\langle\Phi^{\prime}\right| R=\lambda\left\langle\Phi^{\prime}\right|$, which also accounts for an infinite half lane.
			- Then $\mathcal{F}^{\left[\vec{r}_1, \vec{r}_2\right]}$ is built from these two iMPS and a strip f reduced tensors $a$ and $b$.
	- [Step 2.](((65142d60-dbcd-47a5-bf31-b6cee9c46f4f))) A transfer matrix $S$ is defined in terms of the tensors $\left\{a, b, C, D, C^{\prime}, D^{\prime}\right\}$
		- Recall that $C,D,C',D'$ encode the dominant eigenvectors.
		- $S$ can be regarded as a linear operator acting on three sites with local vector space dimensions $\chi, D^2$ and $\chi$.
			- ((65142de1-8a1d-459b-823f-d6e3870c85d7))
		- Again, its dominant eigenvector $|\Omega\rangle$, encoded in a three-legged tensor $X$, is computed from an initial state $\left|\Omega_0\right\rangle$ using the fact that
		  $$
		  |\Omega\rangle=\lim _{q \rightarrow \infty} \frac{S^q\left|\Omega_0\right\rangle}{\| S^q\left|\Omega_0\right\rangle \|}
		  $$
			- Similarly encode the right dominant vector by $X'$.
		- Then $\mathcal{G}^{\left[\vec{r}_1 \vec{r}_2\right]}$ is a (circular) MPS consisting of the six tensors $\left\{C, D, C^{\prime}, D^{\prime}, X, X^{\prime}\right\}$.
			- Like the first step, leaving only one finite strip and replace the infinite part by the dominant eigenvectors.