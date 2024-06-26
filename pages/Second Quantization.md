- # Motivation
	- States of identical particles are greatly limited, so the traditional description has lots of redundancy.
	- Occupation numbers would be a good substitute.
- # Bosons
	- Basics
		- $\left[\hat{b}_k, \hat{b}_{k^{\prime}}^{\dagger}\right]=\delta_{k k^{\prime}} \quad$ and $\quad\left[\hat{b}_k, \hat{b}_{k^{\prime}}\right]=\left[\hat{b}_k^{\dagger}, \hat{b}_{k^{\prime}}^{\dagger}\right]=0$
		- $\begin{aligned} & \hat{b}_k\left|n_1, \ldots, n_k, \ldots\right\rangle=\sqrt{n_k}\left|n_1, \ldots, n_k-1, \ldots\right\rangle \\ & \hat{b}_k^{\dagger}\left|n_1, \ldots, n_k, \ldots\right\rangle=\sqrt{n_k+1}\left|n_1, \ldots, n_k+1, \ldots\right\rangle\end{aligned}$
		- $\hat{N} \equiv \sum_k \hat{n}_k=\sum_k \hat{b}_k^{\dagger} \hat{b}_k$
	- N-body operator
- # Fermions
	- Note
		- We would have minuses when exchanging operators. So be careful of their **order**!
		-
	- Basics
		- $\left\{\hat{c}_k, \hat{c}_l^{\dagger}\right\}=\delta_{k l} \quad$ and $\quad\left\{\hat{c}_k^{\dagger}, \hat{c}_l^{\dagger}\right\}=\left\{\hat{c}_k, \hat{c}_l\right\}=0$
- # N-body operator
	- 1-body
		- $\hat{F}=\sum_{k_1 k_2} f_{k_1 k_2} \hat{b}_{k_1}^{\dagger} \hat{b}_{k_2} \quad$ with $\quad f_{k_1 k_2}=\left\langle k_1|\hat{f}| k_2\right\rangle$
	- 2-body
		- $\hat{G}=\frac{1}{2} \sum_{k^{\prime} l^{\prime}, l k} g_{k^{\prime} l^{\prime}, l k} \hat{b}_{k^{\prime}}^{\dagger} \hat{b}_{l^{\prime}}^{\dagger} \hat{b}_l \hat{b}_k$
		- Also can be viewed as scattering
	- The generalization to n-body shall be similar: Sum the possible scatterings, then divide by $n!$.
- # Changing representations
	- ## Transformation Law #card
	  card-last-interval:: 30
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2023-05-13T11:35:34.196Z
	  card-last-reviewed:: 2023-04-13T11:35:34.196Z
	  card-last-score:: 5
		- We could change the basis
		  id:: 640846c2-c0a4-42de-8fa9-8c9b4a1faed0
		  $$\hat d_a=\sum_b \langle\psi_a|\phi_b\rangle \hat c_b$$
		- Intuitively, extract the $\psi_a$ part in $\phi_b$
		-
	- ## Field Operators
		- $$\hat{\psi}\left(\mathbf{r}^{\prime}\right)=\sum_k \hat{b}_k \psi_k\left(\mathbf{r}^{\prime}\right)$$
			- $\psi_k(r):=\langle r|k\rangle$
			-
		- CCR
			- $\begin{aligned} {\left[\hat{\psi}\left(\mathbf{r}^{\prime \prime}\right), \hat{\psi}^{\dagger}\left(\mathbf{r}^{\prime}\right)\right] } & =\delta\left(\mathbf{r}^{\prime \prime}-\mathbf{r}^{\prime}\right), \\ {\left[\hat{\psi}\left(\mathbf{r}^{\prime \prime}\right), \hat{\psi}\left(\mathbf{r}^{\prime}\right)\right]=\left[\hat{\psi}^{\dagger}\left(\mathbf{r}^{\prime \prime}\right), \hat{\psi}^{\dagger}\left(\mathbf{r}^{\prime}\right)\right] } & =0 .\end{aligned}$
			-