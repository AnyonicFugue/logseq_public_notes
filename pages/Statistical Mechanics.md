- [[References]]
	- ![2022_Pathria_Beale_Statistical mechanics.pdf](file://zotero_link/Physics/Courses/Statistical/2022_Pathria_Beale_Statistical mechanics.pdf) Pathria_Beale
	- Altland
	-
- Altland
	- 3
		- Essentially, Integrations over fields are just discrete versions of [[Gaussian integral]].
		- Inverse matrix is replaced by kernel([[Green Function]])
	- 5.1
		- Turn [[Ising model]] into $\phi^4$ theory
			- $$\begin{aligned}
			  &H\left(\left\{\sigma_{i}\right\}_{i}\right)=-\left[\sum_{i j} \sigma_{i} J_{i j} \sigma_{j}+h \sum_{j} \sigma_{j}\right] \\
			  &Z=\Sigma e^{-\beta H}=\Sigma e^{\sigma^{T} K \sigma+\sigma^T h1} \quad K=\beta J \\
			  &\int d^{N} \psi e^{-\psi^{T} k^{-1} \psi}=x^{N / 2}(\operatorname{det} K)^{1 / 2} \\
			  &\text{Substitute }\tilde{\psi}=\psi-K \sigma \\
			  &I=\int d^{N} \tilde{\psi} e^{-(\widetilde{\psi}+k \sigma)^{T} k^{-1}(\tilde{\psi}+k \sigma)} \\
			  &=\int d^{N} \tilde{\psi} e^{-\tilde{\psi}^{T} k^{-1} \tilde{\psi}} e^{-2 \sigma^{T} \psi} e^{-\sigma^{T} k \sigma}
			  \end{aligned}$$
			- $e^{\sigma^TK\sigma+\sigma^T h1}=I\int d^{N} \tilde{\psi} e^{-\tilde{\psi}^{T} K^{-1} \tilde{\psi}} e^{-\sigma^{T} (2\psi+h1)}$
			- Sum over $\sigma$, we can obtain the partition function in an integral form.
			- $h1$ stands for a vector with all components being $h$
-
-
- II
	- [[Saddle point integration]]
	  collapsed:: true
		- Example
			- Calculate the partition function of some [[Canonical ensemble]].
				- $Z=\int dE\ \Omega(E)\ e^{-\beta E}=\int dE\ e^{f(E)}$, 
				  where $f(E)=$
				- Expand the integral near the most probable energy:
	- [[Effective Theory]]
	  collapsed:: true
		- Divide the [[Degrees of freedom]] into high-energy group $X_h$ and a low-energy group $X_l$
		- Full [[Partition function]]: $Z=\sum\limits_{X_l}\sum\limits_{X_h}e^{-\beta E(X_l,X_h)}$
		-
		- We may first perform the high-energy sum, then we can obtain $E_{\text {eff }}\left(X_l\right):=-k_B T \ln \sum_{X_h} e^{-\beta E\left(x_1, x_n\right)}$.
			- Note that the result is exact. If we plug this back, we can restore the full partition function.
		- The high-energy part can be dealt with by [[Approximations]], eg. expansions.
		  That's why we choose to sum over the high-E ones, not the low-E ones.
		-
		- Example: [[Ising model ]] and connected diagrams
			- Trick. $e^{K \sigma_i \sigma_j}=\cosh K\left(1+\sigma_i \sigma_j \tanh K\right)$
				- This allows easy expansion of K.
			- $Z=\sum_{\left\{\sigma_i\right\}} \sum_{\langle i j\rangle}e^{K \sigma_i \sigma_j}=\sum_{\left\{\sigma_i\right\}} \sum_{\langle i j\rangle} \cosh K\left(1+\sigma_i \sigma_j \tanh K\right)\\=(\cosh K)^C \sum_{\langle i j\rangle} \left(1+\sigma_i \sigma_j \tanh K\right)$
			-
			- $\sum_{\langle i j\rangle} \left(1+\sigma_i \sigma_j \tanh K\right)$ can be expanded by order.
			- Note that the spins must pair to obtain nonzero results, since $\langle \sigma_i\rangle=0$.
			  So we must have connected diagrams(where each vertex is covered even times).
			-
			- Correlation functions
				- $\begin{aligned}\left\langle\sigma_i \sigma_j\right\rangle &=\frac{1}{Z} \sum_{\left\{\sigma_i\right\}} \sigma_i \sigma_j e^{\beta J \sum_{i, j} \sigma_i \sigma_j} \\ &=\frac{1}{Z} \sum_{\left\{\sigma_i\right\}} \sigma_i \sigma_j \prod_{\langle k l\rangle} \cosh K\left(1+\sigma_k \sigma_l\tanh K \right) \end{aligned}$
				- Open strings: ![](local://C:/Users/10309/remnote/remnote-624a8cdd2a47080035c9f8d6/files/ovs200ot_qh9DqBznH9gfbhTRHo5GbSHCGnAFrFLSmzRtJAAFP4IJD4uw-VbN5ZvXXrpbXhsJFDL5DV-te7RmyrxrFKZAORLmFh9DaR4HN-YuqdXXnMJaqVGIh8MNp5P.png)
			-
			- Linked-cluster theorem #card
				- $F=-kT\ln Z\propto \{Connected\ diagrams\}$
				- In calculating correlation functions, also only connected diagrams need to be considered.
		-
	- [[Gaussian theory]]
	  collapsed:: true
		- Summary #card
			- After Fourier transforming to momentum space, different momenta decouple. So the correlation functions are easy to evaluate.
		- $$F=\int d^D r\left[\frac{1}{2}(\nabla \phi)^2+\frac{r}{2} \phi^2\right]$$
		- [[Fourier Transformation]] to momentum space, $\phi(x)=\int \frac{d^{3 k}}{(2 a)^3} \tilde\phi(k) e^{i \vec{k} \cdot \vec{x}}$ 
		  collapsed:: true
			- Note that $\tilde{\phi}(k)=\tilde{\phi}^*(-k)$ to keep $\phi(x)$ real.
				- Actually $Re\ \tilde{\phi}(k):= \tilde{\Phi}_r(k)$ and $Im\ \tilde{\phi}(k) :=\tilde{\Phi}_i(k)$ and are two independent real fields.
				- Then $Re\ \tilde{\phi}(k)=Re\ \tilde{\phi}(-k)$, $Im\ \tilde{\phi}(k)=-Im\ \tilde{\phi}(-k)$.
				  So we may take that only the momenta with $k_x>0$ as independent.
			-
			- $\nabla \phi(x)=\int \frac{d^3 k}{(2 x)^3} \tilde{\phi}(k) \cdot i \vec{k} e^{i \vec{k} \cdot \vec{x}}$
			- $\int d^D x \cdot \frac{r}{2} \phi^2=\frac{1}{2} \int \frac{d^3 k}{(2 \pi)^3} \widetilde{\phi}(-k) \widetilde{\phi}(k) \cdot r$
		- Results
			- $$E[\tilde{\phi}]= \int \frac{d^3 k}{(2 \pi)^3} \tilde{\phi}(-k) \widetilde{\phi}(k)\frac 1 2 \left(k^2+r\right)=\frac{1}{2} \int \frac{d^3 k}{(2 \pi)^3}\left[\tilde{\Phi}_r^2(k)+\tilde{\Phi}_i^2(k)\right]\left(k^2+r\right)$$
			- $$\left\langle\tilde{\phi}_r^2(k)\right\rangle=\left\langle\tilde{\phi}_i^2(k)\right\rangle=\frac{1}{k^2+r}$$
			- $$\begin{aligned}
			  &\langle\tilde{\phi}(-k) \tilde{\phi}(k)\rangle=\left\langle\widetilde{\phi}_r^2(k)+\widetilde{\phi}_i^2(k)\right\rangle=\frac{2}{k^2+r} \\
			  &\langle\tilde{\phi}(k) \tilde{\Phi}(k)\rangle=0
			  \end{aligned}$$
	- Methods for simulation
	  collapsed:: true
		- Monte-Carlo method
			- Idea
				- Use randomized time-evolution to simulate ensemble average.
		- Wolff Algorithm
			- Idea #card
				- Flip a cluster of spins at a stroke to accelerate.
				- 'Reality' of the algorithm is guaranteed by [[Detailed balance]].
		- How to find the [[Critical point]]
			- Binder cumulant
				- $1-\frac {\lang m^4\rang}{3\lang m^2 \rang ^2}$
				- Distinguish between FM and PM phases.
		- Data collapsing
			- Physical quantities obey some universal scaling relations.
			- We may plot lots of data in one diagram. If they fall on a single curve (the universal function), then the criticality is justified.
	- [[Mean-field theory]]
	  collapsed:: true
		- Idea
			- Let $\sigma_i-\langle\sigma_i\rangle:=\delta_i$ be a small quantity. Ignore higher order terms.
			- Plug the result back to the model to obtain self-consistency equation.
		- Self-consistency: $\langle\delta_i\rangle=0$.
			- Note that in Ising model the spin can only be $\pm1$.
	- [[Phase Transition]] and [[Criticality]]
	  collapsed:: true
		- Criticality of Van der Waals gas #card
		  collapsed:: true
			- Equation $\left(p+\frac{a}{v^2}\right)(v-b)=R T$
				- ![IVCJdvJM199kI26xcSqNF__dOXAW-eTJqdaF_vj0XQf7xtK4fyvBd2S_daDTNgbEkRtnjyPqq2xnGJbwxPmZ2nebYRj1MwZNAjgX07H2mOZngUE62EObknQ6HY5g36vW.png](../assets/IVCJdvJM199kI26xcSqNF_dOXAW-eTJqdaF_vj0XQf7xtK4fyvBd2S_daDTNgbEkRtnjyPqq2xnGJbwxPmZ2nebYRj1MwZNAjgX07H2mOZngUE62EObknQ6HY5g36vW_1669207663643_0.png)
				-
				- ![u7_2RPVOJmEfQwHz2KxSU-dlgVQ2pAp2WPmX1RWExeRaJGg5nY2C0FSGnjfPLh7u97jnPqN_rtF6vaWTsI-gJUcNaYeNg8hZO-UBdl4kaU8p4FzceN7ioSYHcV0Hqt4q.png](../assets/u7_2RPVOJmEfQwHz2KxSU-dlgVQ2pAp2WPmX1RWExeRaJGg5nY2C0FSGnjfPLh7u97jnPqN_rtF6vaWTsI-gJUcNaYeNg8hZO-UBdl4kaU8p4FzceN7ioSYHcV0Hqt4q_1669207716097_0.png)
				- The images are taken from Wikipedia.
			- Note that the hollowed region where $\frac {dp}{dV}>0$ is **unphysical. **So the region shall actually correspond to a **gas-liquid transition.**
			- At $T_c$, the phase transition becomes continuous.
			- Critical equation→$\frac{d p}{d v}=0, \frac{d^2 p}{d v^2}=0$
		- Ising
			- [[Mean-field theory]] approach
				- Self consistency $m=\tanh [\beta(q J m+h)]$
		- Landau's theory
			- Use m as an order parameter.
			- $Z_2$ symmetry ⇒ Only even-order terms can survive.
			- $$\begin{aligned}
			  &F=F_0+r(T) m^2+u m^4 \\
			  &F=F_0+\frac{1}{2} a t m^2+\frac{1}{4} c m^4
			  \end{aligned}$$
				- The equilibrium minimizes F. We can obtain the critical point and the critical exponents.
		- [[Critical exponents]]
			- $\alpha$
				- $C_V \sim \begin{cases}t^{-\alpha}, & t \rightarrow 0^{+} \\ |t|^{-\alpha^{\prime}}, & t \rightarrow 0^{-}\end{cases}$
			- $\beta$
				- $m \sim|t|^\beta \quad t \rightarrow 0^{-}$
			- $\gamma$
				- $\chi_0=\left.\frac{\partial m}{\partial h}\right|_{h=0}=|t|^{-\gamma}$
				- Only for $t \to 0^+$
			- $\delta$
				- $t=0$(precise), $m \sim h^{1 / \delta}$
			- $\eta$
				- $\langle\psi(0) \psi(r)\rangle \propto r^{-d+2-\eta}$
			- $\nu$
				- Correlation length $\xi\sim t^{-\nu}$
		-
	- [[Renormalization]] 
	  collapsed:: true
		- Momentum shell
			- Thought of the approach #card
				- We integrate a bit of high-energy degrees of freedom, then examine how the system changes.
				  At the critical point, the system shall be insensitive to a rescaling.
				- In this case, we make use of the momentum [[Cutoff]].
					- This is a bit strange, since the cutoff seems 'unphysical' to me. It is a device to make the integral convergent.
			-
			- Overall scheme #card
				- **Integrate** out large-energy d.o.f. 
				  $$\begin{aligned}
				  F_{\text {eff }}\left[\phi_<\right] &=-\ln \int D\left[\phi_>\right] e^{-F[\phi]} \\
				  &=-\ln \int D\left[\phi_{>}\right] e^{-\int d^D x\left[\frac{1}{2}(\nabla \phi)^2+\frac{r}{2}\phi^2+\frac{u}{4 !} \phi^4\right]}
				  \end{aligned}$$
				  Note that this is **exact**.
				- **Rescale** the coordinates to restore the former form(eg. same cutoff)
					- Require that the system keeps invariant and find proper scaling dimensions.
					- For example, $[\phi]=,[x]=-1$ #TODO
				- Write the change under an infinitesimal change, thus obtaining the **RG equation** and find fixed points.
			-
			- Model: $F=\int d^D r\left[\frac{1}{2}(\nabla \phi)^2+\frac{r}{2} \phi^2+\frac{u}{4 !} \phi^4\right]$  Phi^4 theory.
			-
			- Step1. Integrate
			  collapsed:: true
				- For the free theory(u=0): Different momenta are decoupled.
					- $$E[\tilde{\phi}]= \int \frac{d^3 k}{(2 \pi)^3} \tilde{\phi}(-k) \widetilde{\phi}(k)\frac 1 2 \left(k^2+r\right)=\frac{1}{2} \int \frac{d^3 k}{(2 \pi)^3}\left[\tilde{\Phi}_r^2(k)+\tilde{\Phi}_i^2(k)\right]\left(k^2+r\right)$$
				- This motivates us to write $\phi=\phi_>+\phi_<$ , 
				  $$\begin{aligned}
				  &\phi_\alpha^<(x):=\int_0^{\Lambda / b} \frac{d^D k}{(2\pi)^D} \tilde{\phi}(k) e^{i k x} \\
				  &\phi_\alpha^{>}(x)=\int_{\Lambda / b}^{\Lambda} \frac{d^D k}{(2\pi)^D} \tilde{\phi}(k) e^{i k x}
				  \end{aligned}$$
					- Note that we take $b-1<<1$ here.
				- Then we have $$Z_>:=\int D\left[\phi_{>}\right] e^{-\int d^D x\left[\frac{1}{2}(\nabla \phi)^2+\frac{r}{2}\phi^2+\frac{u}{4 !} \phi^4\right]}\\=\int D\left[\phi_{>}\right] e^{\left.-\int d^D x\left\{\left[\frac{1}{2}\left(\nabla \phi_<\right)^2+\frac{1}{2} r \phi_<^2\right)\right]+\left[\frac{1}{2}\left(\nabla \phi_>\right)^2+\frac{1}{2} r \phi_{>}^2\right]+\frac{u}{4 !}\left(\phi_<+\phi_{>}\right)^4\right\}}\\=e^{-\int d^D x\left\{\left[\frac{1}{2}\left(\nabla \phi_<\right)^2+\frac{1}{2} r \phi_<^2\right)\right]}\int D\left[\phi_{>}\right] e^{\left.-\int d^D x\left\{\left[\frac{1}{2}\left(\nabla \phi_<\right)^2+\frac{1}{2} r \phi_<^2\right)\right]+\left[\frac{1}{2}\left(\nabla \phi_>\right)^2+\frac{1}{2} r \phi_{>}^2\right]+\frac{u}{4 !}\left(\phi_<+\phi_{>}\right)^4\right\}}$$
					- In the last line we can easily see that the Gaussian part of the low-energy is separated.
				- Thus, $${F_{eff}}\left[\phi_c\right]=\int d^D x\left[\frac{1}{2}\left(\vec{\nabla} \phi_<\right)^2+\frac{r}{2} \phi_{<}^2\right]-\ln Z_{>}-\ln \left\langle e^{-\int d^D x \cdot \frac{u}{4 !}\left(\phi_<+\phi_>\right)^4}\right\rangle_{z_{>}} .$$
					- The second term is a constant, which we don't care.
					- We always love the form of **expectation, **which allows us to eliminate vacuum graphs.
				-
				- Next task: Evaluate the high-momenta integral perturbatively.
					- Draw Feynman diagrams. Fix the coefficients manually.
					- Integrate in momentum space; easy to make approximations.
			- Step2. Rescale
			  collapsed:: true
				- $\tilde\Lambda=b\Lambda,\tilde x=x/b$ to have $\tilde\Lambda=\Lambda$
				- All other quantities rescale according to their dimensions
			- Step3. Write RG equation and find fix points
			  collapsed:: true
				- Trick: set $\epsilon=4-D$, expand wrt $\epsilon$
				-
				- Relevance of coupling constants #card
					- Thought: The irrelevant ones vanish in the rescaling process
					- Criteria: Scaling dimension
					- [g]>0 ⇒ Relevant
					  [g]=0 ⇒ Marginal
					  [g]<0 ⇒ Irrelevant
				-
				- Stability of the fix points #card
					- Essentially, when the system is a bit off the fix point, would it fall back to the fix point or drift away?
					-
					- Method: Examine the eigenvalues of the RG equation.
			-
		- 1/N expansion
		- Position space
	- [[Nonequilibrium]] statistics
		- In equilibrium statistics, we don't know anything of the dynamics. In principle we only know the spectrum.
		- Here a lot more interesting things would emerge.
		- Diffusion
		  collapsed:: true
			- Fick's law #card
				- ((637e1fcc-f63b-4263-ae21-3f325af2890a))
			- Continuity equation
				- $\nabla \cdot \boldsymbol{j}(\boldsymbol{r}, t)+\frac{\partial n(\boldsymbol{r}, t)}{\partial t}=0$
		- [[Brownian motion]]
		  collapsed:: true
			- ((637e1ecc-4512-4afb-904b-baedb81808a6))
				- Formulation
				  collapsed:: true
					- Particle at x=0 when t=0
					- Walk for l each step at a random direction
					- The steps are uncorrelated
				- Summary #card
				  collapsed:: true
					- The distribution of the position tends to be Gaussian after a large number of jumps.
					- The average is zero, while the square deviation adds up at each step.
					- ((637e1f66-cd2e-4736-a58a-f243ab833dab))
					  collapsed:: true
						- D is the diffusion coefficient.
						- $\tau$ is the time for a single step
			- ((637e200d-781d-4108-a25a-782b8b561888))
				- Formulation
					- $M \frac{d v}{d t}=-\frac{v}{B}+\boldsymbol{F}(t) ; \quad \overline{\boldsymbol{F}(t)}=0$
						- F is a random force
						- B corresponds to viscosity
				- Summary #card
				  collapsed:: true
					- There are three possible operations: Multiply x or v; integrate t; take ensemble average.
					- When all these are useless, we can solve the ODE directly.
					- ((637e20b2-8778-42e0-aa87-a00cd31171f9))
					- ((637e20d9-4cb8-4aef-bd85-d419ff73e31c))
						- This needs solving the ODE.
		- ((637e2117-23ec-4369-8b80-8dc4c6e7c618))
		  collapsed:: true
			- We study an ensemble of particles and study how they evolve (and reach equilibrium)
			- Summary #card
				- Master equation
					- $$\frac{\partial f(x, t)}{\partial t}=\int_{-\infty}^{\infty}\left\{-f(x, t) W\left(x, x^{\prime}\right)+f\left(x^{\prime}, t\right) W\left(x^{\prime}, x\right)\right\} d x^{\prime}$$
					- Where W is the propagator
				- Assume that the propagator is nonzero only within a small range. Then we perform Taylor expansion to 2nd order.
				- Fokker-Planck equation
					- $$
					  \begin{gathered}
					  \frac{\partial f(x, t)}{\partial t}=-\frac{\partial}{\partial x}\left\{\mu_1(x) f(x, t)\right\}+\frac{1}{2} \frac{\partial^2}{\partial x^2}\left\{\mu_2(x) f(x, t)\right\} \\
					  \mu_1(x)=\int_{-\infty}^{\infty} \xi W(x ; \xi) d \xi=\frac{\langle\delta x\rangle_{\delta t}}{\delta t}=\left\langle v_x\right\rangle \\
					  \mu_2(x)=\int_{-\infty}^{\infty} \xi^2 W(x ; \xi) d \xi=\frac{\left\langle(\delta x)^2\right\rangle_{\delta t}}{\delta t}
					  \end{gathered}
					  $$
					-
			-
		- Fluctuation-Dissipation Theorem
			- Motivation
				- Dissipation is the response to external perturbations.
				- Fluctuation can also be viewed as perturbations to the system (by god).
			- Settings and Definitions
				- $\lang x\rang =0$ when the external field is zero.
				- Linear response function $\chi$
					- $$
					  \langle x(t)\rangle:=\int_{-\infty}^t d t^{\prime} h\left(t^{\prime}\right) \chi\left(t^{\prime}, t\right)
					  $$
					- By time-translation invariance, we may write it as $\chi(t-t')$
					- This only works for small $h(t)$
				- Correlation
					- $$
					  A_x(t):=\langle x(t) x(0)\rangle
					  $$
				- $$
				  \begin{aligned}
				  &A_x(\omega):=\int d t A_x(t) e^{-i \omega t} \\
				  &\chi(\omega):=\int d t x(t) e^{-i \omega t}
				  \end{aligned}
				  $$
				- Classical
					- $E=E_0(x)-h(t)x$
				- Quantum
					- $$
					  \hat{H}=\hat{H}_0-h(t) \hat{B}
					  $$
			- Summary #card
				- The imaginary part of (Fourier-transformed) linear response function is proportional to (Fourier-transformed) correlation function.
				- Classical version
					- $$
					  A_x(\omega)=\frac{2 k T}{\omega} \operatorname{Im} \chi(\omega)
					  $$
					- Proof
						- Consider the case where the field is $h_0 \theta (-t)$
						- Write 
						  $$
						  \langle x(t)\rangle=\int d x^{\prime} d x \ x^{\prime} P\left(x^{\prime}, t \mid x, 0\right) W(x, 0)
						  $$
							- $W(x,0)$ is the distribution at t=0.
						- Invoke Boltzman distribution and $h<<1$ to perform expansions to relate $\langle x(t)\rangle$ with $A_x(t)$
						- On the other hand, $\langle x(t)\rangle$ can be related to linear response by def.
						- The theorem follows by comparison.
				- Quantum version
					- $$
					  \operatorname{Im} \chi(\omega)=\frac{1-e^{-\beta \omega}}{2} A_x(\omega)
					  $$
					- Proof
						- Write $\hat{\rho}(t)=\hat{\rho}_{e q}+\hat{\delta \rho}(t)$
						- Write the Heisenberg equation and discard second-order terms
						- $\delta\hat{\rho}(t)=\frac{i}{\hbar} \int_{-\infty}^t h\left(t^{\prime}\right) e^{-\frac{i}{\hbar} H_0\left(t-t^{\prime}\right)}\left[\hat{B}, \hat{\rho}_{e q}\right] e^{\frac{i}{\hbar} H_0\left(t-t^{\prime}\right)} d t^{\prime}$
						- Next, consider $\langle\hat{\delta A}(t)\rangle =\langle A(t)\rangle:=\operatorname{Tr}(\hat{A} \delta \hat{p})=\frac{i}{\hbar} \int_{-\infty}^t h\left(t^{\prime}\right) \operatorname{Tr}\left\{\left[\hat{A}(t), \hat{B}\left(t^{\prime}\right)\right] \hat{p}_{e q}\right\} d t$
							- Absorb the evolution into the operators.
						- Insert completeness relations to absorb $H_0$
							- ![image.png](../assets/image_1669212892551_0.png)
						- The rest is very simple.