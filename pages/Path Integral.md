- # Def
	- Feynman Kernel
		- $$K( q'' ,t'';q' ,t') :=_{H}\left< q'',t''|q^{\prime } ,t^{\prime }\right> _{H} =_{s}\left< q''( t'')\left| e^{-iH\left( t^{\prime \prime } -t^{\prime }\right)}\right| q^{\prime }\left( t^{\prime }\right)\right> _{s}$$
		-
	-
- # QM Version
	- Start by 
	  $$K( q'' ,t'';q' ,t') :=_{H}\left< q'',t''|q^{\prime } ,t^{\prime }\right> _{H} =_{s}\left< q''( t'')\left| e^{-iH\left( t^{\prime \prime } -t^{\prime }\right)}\right| q^{\prime }\left( t^{\prime }\right)\right> _{s}$$ 
	  and insert many interim positions $| r_i \rangle \langle r_i|$
	- $$
	  \begin{aligned}
	  K\left(\mathbf{r}_i, t_i, \mathbf{r}_{i-1}, t_{i-1}\right) & =\left\langle\mathbf{r}_i\left|\hat{U}\left(t_i, t_{i-1}\right)\right| \mathbf{r}_{i-1}\right\rangle=\left\langle\mathbf{r}_i\left|e^{-i \epsilon \hat{H} / \hbar}\right| \mathbf{r}_{i-1}\right\rangle \\
	  & =\left\langle\mathbf{r}_i\left|e^{-i \epsilon\left[\hat{\mathbf{p}}^2 / 2 m+V(\hat{\mathbf{r}})\right] / \hbar}\right| \mathbf{r}_{i-1}\right\rangle \\
	  & =e^{-i \epsilon V\left(\mathbf{r}_i\right) / \hbar} \underbrace{\left\langle\mathbf{r}_i\left|e^{-i \epsilon \hat{\mathbf{p}}^2 / 2 m \hbar}\right| \mathbf{r}_{i-1}\right\rangle}_{\text {free particle propagator }} \\
	  & =e^{-i \epsilon V\left(\mathbf{r}_i\right) / \hbar}\left(\frac{m}{2 \pi \hbar i \epsilon}\right)^{\frac{3}{2}} e^{i \epsilon m \mathbf{v}_i^2 / 2 \hbar} \\
	  & =\left(\frac{m}{2 \pi \hbar i \epsilon}\right)^{\frac{3}{2}} e^{\frac{i}{\hbar} \epsilon\left[\frac{1}{2} m \mathbf{v}_i^2-V\left(\mathbf{r}_i\right)\right]} \\
	  & =\left(\frac{m}{2 \pi \hbar i \epsilon}\right)^{\frac{3}{2}} e^{\frac{i}{\hbar} \int_{t_i}^{t_{i+1}} \mathscr{L}(\mathbf{r}, \mathbf{r}, t) d t} \\
	  & =\left(\frac{m}{2 \pi \hbar i \epsilon}\right)^{\frac{3}{2}} e^{\frac{i}{\hbar} S\left(t_{i+1}, t_i\right)}
	  \end{aligned}
	  $$
		- Exercise. Calculate the free-particle propagator. #card
		  card-last-interval:: 32.51
		  card-repeats:: 1
		  card-ease-factor:: 2.6
		  card-next-schedule:: 2023-05-06T23:33:23.468Z
		  card-last-reviewed:: 2023-04-04T11:33:23.468Z
		  card-last-score:: 5
	- Thus 
	  $$
	  K\left(\mathbf{r}^{\prime}, t^{\prime}, \mathbf{r}, t\right)=\mathscr{C} \int \mathscr{D}[\mathbf{r}(t)] e^{\frac{i}{\hbar} S[\mathbf{r}(t)]}
	  $$
	-
- # QFT Version
	- Ref
		- Peskin [9.2](((642bc322-b8dc-4d82-ade0-a452daad6a1d)))
	- ## Fundamental formula #card
		- $$
		  \left\langle\phi_b(\mathbf{x})\left|e^{-i H T}\right| \phi_a(\mathbf{x})\right\rangle=\int \mathcal{D} \phi \exp \left[i \int_0^T d^4 x \mathcal{L}[\phi]\right]
		  $$
		  with constraints $\phi_a(\mathbf{x})$ at $x^0=0$ and $\phi_b(\mathbf{x})$ at $x^0=T$
			- Note that $\mathcal L[\phi]$ is the Lagrangian of a **classical** field, while $|\phi_a(x)\rangle$ (actually $\phi_a(x)|0\rangle$) is a **quantum state**.
			- Therefore, the constraints actually mean that there's a certain quantum-classical correspondence.
				- Compare to QM: The quantum state $|x\rangle$ corresponds to a particle at position $x$.
		- How is it consistent with the Hamiltonian formulation?
		  background-color:: red
	- ## Formula for correlation functions #card
	  card-last-interval:: 30
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2023-05-07T11:19:51.760Z
	  card-last-reviewed:: 2023-04-07T11:19:51.763Z
	  card-last-score:: 5
		- $$
		  \left\langle\Omega\left|T \phi_H\left(x_1\right) \phi_H\left(x_2\right)\right| \Omega\right\rangle=\lim _{T \rightarrow \infty(1-i c)} \frac{\int \mathcal{D} [\phi] \phi\left(x_1\right) \phi\left(x_2\right) \exp \left[i \int_{-T}^T d^4 x \mathcal{L}\right]}{\int \mathcal{D} [\phi] \exp \left[i \int_{-T}^T d^4 x \mathcal{L}\right]}
		  $$
			- This is quite similar to Gellmann-Low, but fundamentally different since here's a functional integration.
		- Proof
			- Observation: The pair of constraints in integration corresponds to the initial and final states.
			  Thus we break the integration into $\int \mathcal{D} \phi(x)=\int \mathcal{D} \phi_1(\mathbf{x}) \int \mathcal{D} \phi_2(\mathbf{x}) \int_{\substack{\phi\left(x_1^0, \mathbf{x}\right)=\phi_1(\mathbf{x}) \\ \phi\left(x_2^0, \mathbf{x}\right)=\phi_2(\mathbf{x})}} \mathcal{D} \phi(x)$
	-
		-
	- ## Obtain [[Feynman rules]]
		- Example: Calculate $\int \mathcal{D} \phi e^{i S_0}$ and $\int \mathcal{D} \phi e^{i S_0} \phi\left(x_1\right) \phi\left(x_2\right)$ for the [[Klein-Gordon Theory]]
			- See [Peskin](((642bcdd1-ada5-4c3a-8ad9-6365a54ee3d4)))
			- Standard Technique #card
				- Discretize the spacetime and do Fourier transformation, then different momenta decouple.
				- For the correlation function, we obtain things like
				  $$
				  \begin{aligned}
				  & \frac{1}{V^2} \sum_{m, l} e^{-i\left(k_m \cdot x_1+k_l \cdot x_2\right)}\left(\prod_{k_n^0>0} \int d \operatorname{Re} \phi_n d \operatorname{Im} \phi_n\right) \\
				  & \times\left(\operatorname{Re} \phi_m+i \operatorname{Im} \phi_m\right)\left(\operatorname{Re} \phi_l+i \operatorname{Im} \phi_l\right) \\
				  & \times \exp \left[-\frac{i}{V} \sum_{k_n^0>0}\left(m^2-k_n^2\right)\left[\left(\operatorname{Re} \phi_n\right)^2+\left(\operatorname{Im} \phi_n\right)^2\right]\right] \\
				  &
				  \end{aligned}
				  $$
					- For $m \neq l$ the integration vanishes since the integrand is odd. Only $m = \pm l$ terms are nonzero.
					  This is momentum conservation!
					- For higher-order correlations, the momenta pair up to obtain even terms.
					  This is Wick's theorem!
				- [[Generating Functional]]
					- Idea
						- Set $Z[J] \equiv \int \mathcal{D} \phi \exp \left[i \int d^4 x[\mathcal{L}+J(x) \phi(x)]\right]$.
						  Each derivative $-i \frac{\delta}{\delta J\left(x_0\right)}$ multiplies $\phi(x_0)$ to the integrand.
					- Examples
						- $$
						  \left\langle 0\left|T \phi\left(x_1\right) \phi\left(x_2\right)\right| 0\right\rangle=\left.\frac{1}{Z_0}\left(-i \frac{\delta}{\delta J\left(x_1\right)}\right)\left(-i \frac{\delta}{\delta J\left(x_2\right)}\right) Z[J]\right|_{J=0}
						  $$
					- Rules
						- $$
						  \frac{\delta}{\delta J(x)} J(y)=\delta^{(4)}(x-y)
						  $$
						-