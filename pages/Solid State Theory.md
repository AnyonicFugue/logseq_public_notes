type:: [[Course]]

-
- ![2012_Phillips_Advanced Solid State Physics.pdf](file://zotero_link/Physics/Courses/Solid State/2012_Phillips_Advanced Solid State Physics.pdf)
- # Problem-Solving Tricks
  collapsed:: true
	- Diagonalizing tight-binding model
	  collapsed:: true
		- Perform a FT to the momentum space
		  collapsed:: true
			- Note that the momenta is a continuum, not discreet.
			- Normalization can be determined by taking $k=0$.
		-
- # Slater Determinant
  collapsed:: true
	- Summary #card
	  collapsed:: true
		- We want to calculate the wavefunction of a certain fermionic state, say $\prod_{\lambda_\alpha<0} c_\alpha^{\dag}|0\rangle$
		- collapsed:: true
		  $$
		  \begin{aligned}
		  & \left\langle\vec{r}_1, \cdots, \vec{r}_N \mid G S\right\rangle=\left\langle 0\left|\hat\psi\left(\vec{r}_1\right) \cdots \hat{\psi}\left(\vec{r}_N\right) \prod_{\lambda_\alpha<0} c_\alpha^{\dag}\right| 0\right\rangle \\
		  = & \sum\langle 0| c_{\alpha_1} \phi_{\alpha_1}\left(\vec{r}_1\right) \cdots c_{\alpha_N} \phi_{\alpha_N}\left(\vec{r}_N\right) \prod_{\lambda_\alpha<0}c_\alpha^\dag|0\rangle
		  \end{aligned}
		  $$
			- $\langle 0|\hat\psi\left(\vec{r}_1\right) \cdots \hat{\psi}\left(\vec{r}_N\right)$ contains symmetrization, while the definition of wavefunctions do not.
			  However, since the fermionic state is itself anti-symmetrical, it makes no difference.
			- The second line is expanding the field operators in the $\alpha$ representation.
		- Obviously the result is a sum of different permutations with signs.
		  collapsed:: true
			- $$
			  \begin{aligned}
			  \left\langle\vec{r}_1, \cdots, \vec{r}_N \mid G S\right\rangle & =\sum_{\left\{\alpha_1 \cdots \alpha_N\right\}}\operatorname{sgn}\left(\alpha_1, \cdots \alpha_N\right) \phi_{\alpha_1}\left(\vec{r}_1\right) \cdots \phi_{\alpha_N}\left(r_N\right) \\
			  & =\operatorname{Det}\left[\phi_{\alpha_i}\left(\vec{r}_j\right)\right]_{ij}
			  \end{aligned}
			  $$
- # [[Hatree-Fock Approximation]] #card
  collapsed:: true
	- ## Idea
	  collapsed:: true
		- Use the variation principle to find out the ground state energy.
		- However, we **fix** the levels to be occupied and **vary the states**.
	- ## Expand the Hamiltonian as 1 and 2 body operators
	  collapsed:: true
		- $\hat{h}_{1} =-\frac{\hbar ^{2}}{2m} \Delta +V (\mathbf{r} )$
		- $\hat{h}_2=\frac{e^{2}}{| \mathbf{r}_{1} -\mathbf{r}_{2}| }$
		- Therefore $\hat H_1=\sum_{\nu \lambda}\langle\nu|\widehat{h}(1)| \lambda\rangle a_\nu^{\dagger} a_\lambda$, $\hat H_2=\frac{1}{2} \sum_{\nu \lambda \alpha \beta}\left\langle\nu \lambda\left|\frac{e^2}{\left|\mathbf{r}_1-\mathbf{r}_2\right|}\right| \alpha \beta\right\rangle a_\nu^{\dagger} a_\lambda^{\dagger} a_\beta a_\alpha$
		-
	- ## Generalized [[Wick's Theorem]]
	  id:: 64085b6c-2d37-476b-92d3-3527157ccbbf
	  collapsed:: true
		- Examples
		  collapsed:: true
			- card-last-interval:: 31.26
			  card-repeats:: 1
			  card-ease-factor:: 2.6
			  card-next-schedule:: 2023-05-15T17:39:08.044Z
			  card-last-reviewed:: 2023-04-14T11:39:08.044Z
			  card-last-score:: 5
			  collapsed:: true
			  $$\left< a_{\nu }^{\dagger } a_{\lambda }^{\dagger } a_{\beta } a_{\alpha }\right> :=\left< \psi _{0} |a_{\nu }^{\dagger } a_{\lambda }^{\dagger } a_{\beta } a_{\alpha } |\psi _{0}\right> =( \delta _{\nu \alpha } \delta _{\lambda \beta } -\delta _{\nu \beta } \delta _{\lambda \alpha })< \hat{n}_{\alpha }> < \hat{n}_{\beta }> .$$
			  Where $|\psi _{0}> =\prod _{a\in A} c_{a}^{\dagger } |0\rangle$ #card
				- The inner operators must pair up to have nonzero amplitudes.
				- The two kronecker deltas corresponds to two contractions.
	- ## Evaluate Energy Expectations
	  collapsed:: true
		- collapsed:: true
		  $$< \hat{H}_{1}> =\sum _{kl} H_{kl}^{(1)}\left< \psi _{0}\left| \hat{a}_{k}^{\dagger }\hat{a}_{l}\right| \psi _{0}\right>=\sum _{k} H_{kk}^{(1)} n_{k}$$
			- The second equality follows ((64085b6c-2d37-476b-92d3-3527157ccbbf))
		- collapsed:: true
		  $$\begin{aligned}
		  < \hat{H}_{2}>  & =\frac{1}{2}\sum _{k_{1} l_{1} l_{2} k_{2}} H_{k_{1} l_{l} l_{2} k_{2}}^{(2)} < \hat{a}_{k_{1}}^{\dagger }\hat{a}_{l1}^{\dagger }\hat{a}_{l2}\hat{a}_{k_{2}}  >\\
		   & =\frac{1}{2}\sum _{kl}( U_{kl} -J_{kl}) n_{k} n_{l}
		  \end{aligned}$$
			- The first term is **diagonal** and the second term is **exchange**.
		- Express in the position representation,
		  $$
		  \begin{equation*}
		  H_{kk}^{(1)} =\int d^{3} r\ \psi _{k}^{*} (r)\left[ -\frac{\hbar ^{2}}{2m} \Delta +V(r)\right] \psi _{k} (r)
		  \end{equation*}
		  \\
		  \begin{equation*}
		  \begin{aligned}
		   & U_{kl} =\int d^{3} r_{1} d^{3} r_{2} \psi _{k}^{*}( r_{1}) \psi _{l}^{*}( r_{2})\frac{e^{2}}{\mid \overrightarrow{r_{1}} -\vec{r}_{2} \mid } \psi _{l}( r_{2}) \psi _{k}( r_{1})\\
		   & J_{kl} =\int d^{3} r_{1} d^{3} r_{2} \ \ \psi _{k}^{*}( r_{1}) \psi _{l}^{*}( r_{2})\frac{e^{2}}{\mid \overrightarrow{r_{1}} -\vec{r}_{2} \mid } \psi _{l}( r_{1}) \psi _{k}( r_{2})
		  \end{aligned}
		  \end{equation*}$$
		-
	- ## Functional Derivative
	  collapsed:: true
		- Minimize wrt wavefunctions $\phi_k(r)$, with the constraint of normalization enforced by a Lagrangian multiplier.
		  collapsed:: true
			- $$\frac{\delta \left( E_{\mathrm{HF}} -\lambda \int d^{3}\mathrm{r} \ \phi _{k}^{*}( r) \phi _{k}( r)\right)}{\delta \phi _{v}^{*} (\mathbf{r} )} =0$$
		- $$
		  \begin{aligned}
		  {\left[\frac{-\hbar^2}{2 m} \nabla^2+\widehat{V}(\mathbf{r})+\sum_\lambda \int \mathrm{d} \mathbf{r}^{\prime} n_\lambda\left(\mathbf{r}^{\prime}\right) \frac{e^2}{\left|\mathbf{r}-\mathbf{r}^{\prime}\right|}\right] \phi_\nu(\mathbf{r}) } \\
		  -\sum \int d\mathbf{r}^{\prime} \phi_\lambda^*\left(\mathbf{r}^{\prime}\right) \phi_\nu\left(\mathbf{r}^{\prime}\right) \frac{e^2}{\left|\mathbf{r}-\mathbf{r}^{\prime}\right|} \phi_\lambda(\mathbf{r})=\lambda \phi_\nu(\mathbf{r})
		  \end{aligned}
		  $$
		-
- # Electron Gas
  collapsed:: true
	- ## Tight-Binding Model
	  id:: 64238eab-5e73-4970-9129-9cbcc7e974fb
	  collapsed:: true
		- Generally $\hat{H}=\sum_{n i, m j}\left\langle n i\left|\hat{h}_1\right| m j\right\rangle \hat{c}_{n i}^{\dagger} \hat{c}_{m j}$
		  collapsed:: true
			- Sum of hoppings from $mj$ to $ni$.
		- Tight-binding model: Only adjacent hoppings (electrons are localized).
		- Example
		  collapsed:: true
			- Tight-binding on square lattice
			  collapsed:: true
				- $$
				  \hat{H}=-t \sum_{\left\langle ij \right\rangle}\left(\hat{c}_i^{\dagger} c_j+c . c .\right)
				  $$
				- By Fourier transformation, we can diagonalize the Hamiltonian and obtain $E_{\vec{k}}=-2 t\left[\cos \left(k_x a\right)+\cos \left(k_y a\right)\right]$.
	- ## Bloch Wavefunction
	  collapsed:: true
		- Bloch Theorem. $\psi_k(r)=e^{ikr}u_k(r)$ in a periodic potential.
		  collapsed:: true
			- Note that the wavefunction **cannot be normalized** when the system is infinite.
			- Proof
			  collapsed:: true
				- In a periodic potential, the Hamiltonian $H$ commutes with the period-translation operator $T$. Thus we may find their common eigenvectors.
			-
		- Notation
		  collapsed:: true
			- collapsed:: true
			  $$
			  \psi_{n \vec{k}}(\vec{r})=e^{i \vec{k} \cdot \vec{r}} u_{n \vec{k}}(\vec{r})
			  $$
				- The n^th level of Bloch wavevector $k$
			- Normalization
			  collapsed:: true
				- $$
				  \left\langle\psi_{n_1 k_1} \mid \psi_{n_2 k_2}\right\rangle=\frac{1}{V} \delta_{n_1 n_2} \delta^3\left(\vec{k}_1-\vec{k}_2\right)
				  $$
				- Note: $\frac{1}{V}$ is regarded to cancel $\delta^3(0)$.
		-
	- ## Wannier Wavefunction
	  collapsed:: true
		- Idea
		  collapsed:: true
			- Apply Fourier transformation to the Bloch wavevector.
		- Def #card
		  collapsed:: true
			- $$
			  W_{n i}(\vec{r}):=\frac{1}{\sqrt{N}} \cdot \frac{1}{\sqrt{N}} \sum_k \psi_{n k}(\vec{r}) e^{-i \vec{k} \cdot \vec{r}_i}
			  $$
			- $i=(i_1,i_2,i_3)$ is a tuple of integer, $r_i=i_1 \vec{a}_1+i_2 \vec{a}_2+i_3 \vec{a}_3$ is a lattice vector.
			- The extra $\frac 1 {\sqrt N}$ prefactor is to cancel the effect of system size.
		- Properties
		  collapsed:: true
			- The wavefunctions only depend on $r-r_i$, that is, $W_{n i}(\vec{r})=W_n\left(\vec{r}-\vec{r}_i\right)$
			  collapsed:: true
				- Since there's a factor $e^{ikr}$ in $\psi_k(r)$.
				- Moreover, $u_k(r)$ is periodical on the lattice vectors.
		- Fock operators
		  collapsed:: true
			- $$
			  \hat{c}_{n i}:=\frac{1}{\sqrt{V_0}} \int d^3 \vec{r} \hat{\psi}(\vec{r}) W_{n i}^*(\vec{r})
			  $$
			- Obviously they're the Fourier transform of the Block Fock operators.
- # [[Fermi Liquid]]
  collapsed:: true
	- Assumptions of Landau Theory of Fermi Liquids #card
	  card-last-interval:: 31.26
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2023-06-06T18:01:23.668Z
	  card-last-reviewed:: 2023-05-06T12:01:23.668Z
	  card-last-score:: 5
	  collapsed:: true
		- There is still a fermi surface of some shape
		- There are quasiparticle excitations near the fermi surface, which might decay.
		- Energy functional
		  collapsed:: true
			- $$
			  \delta E=\sum_{k \sigma} \varepsilon_k^0 \delta n_0(k)+\frac{1}{2 v} \sum_{k_1 k_2 \sigma_1 \sigma_2} f_{\sigma_1, \sigma_2}\left(k_1, k_2\right) \delta n_{\sigma_1}\left(\vec{k}_1\right) \delta n_{\sigma_2}\left(\vec{k}_2\right)
			  $$
			- The first term is 1-body energy.
			  collapsed:: true
				- $\varepsilon_k^0=\frac{k_F}{m^*}\left(k-k_F\right)$, where $m*$ is the ^^effective mass^^.
			- The second term is 2-body part.
			  collapsed:: true
				- $$
				  \begin{aligned}
				  & f_{\uparrow \uparrow}\left(\vec{k}, \overrightarrow{k^{\prime}}\right)=f^s(\vec{k}, \vec{k'})+f^a\left(\vec{k}, \overrightarrow{k^{\prime}}\right) \\
				  & f_{\downarrow \uparrow}\left(\vec{k}, \overrightarrow{k^{\prime}}\right)=f^s-f^a
				  \end{aligned}
				  $$
				- We may expand by Legendre polynomials (which is a complete set):
				  $$
				  f^{a / s}\left(\vec{k}_1, \vec{k}_2\right)=\sum_{l=0}^{\infty} f_l^{\alpha / s} P_l(\cos \theta)
				  $$
			- Also could be comprehended as a series expansion.
	- Square law of lifetime #card
	  collapsed:: true
		- Consider some electron with energy $\epsilon$ above the fermi surface. 
		  It could decay by scattering with another electron slightly below the fermi surface.
		- collapsed:: true
		  $$\frac{1}{\tau } \varpropto \Gamma \varpropto |u|^{2}\int d^{3}\vec{p}_{1} d^{3}\vec{p}_{2}F(p_1,p_2) 1-f( \varepsilon _{p_{1}})] f( \varepsilon _{p_{2}})[ 1-f( \varepsilon _{p-p_{1} +p_{2}})] \delta (\Sigma\varepsilon )$$
			- $f$ is the occupation number. $F$ is the cross section between $p_1$ and $p_2$.
		- Obviously the volume of the phase space is proportional to $\epsilon^2$.
	- Calculate physical quantities
	  collapsed:: true
		- Heat capacity at low temperatures #card
		  card-last-interval:: 84
		  card-repeats:: 3
		  card-ease-factor:: 2.8
		  card-next-schedule:: 2023-07-28T12:05:20.771Z
		  card-last-reviewed:: 2023-05-05T12:05:20.772Z
		  card-last-score:: 5
		  collapsed:: true
			- First calculate the energy of a certain configuration. The heat capacity would be known once the state density is known.
			  collapsed:: true
				- collapsed:: true
				  $$\begin{aligned}
				  \delta E^{(2)} & =\frac{1}{2V}\sum _{\theta _{1} \theta _{2} \sigma _{1} \sigma _{2}} f_{\sigma _{1} \sigma _{2}( \theta _{1} ,\theta _{2})}\sum _{| \vec{k}_{1}| | \vec{k}_{2}| } \delta n_{\sigma _{1}}(\vec{k}_{1}) \delta n_{\sigma _{2}}(\vec{k}_{2})\\
				   & =\frac{1}{2V}\sum _{\theta _{1} \theta _{2} \sigma _{1} \sigma _{2}} f_{\sigma _{1} \sigma _{2}}( \theta _{1} ,\theta _{2})\left[\sum _{| \vec{k}_{1}| } \delta n_{\sigma _{1}}(\vec{k}_{1})\right]\left[\sum _{| \vec{k}_{2}| } \delta n_{\sigma _{2}}(\vec{k}_{2})\right]
				  \end{aligned}$$
					- Approx: At low temperature $k_1,k_2$ would be close to the fermi surface, thus $f$ only depends on the angles, not the norms.
				- Therefore the 2-body part is zero, only the 1-body part remains.
				- The heat capacity can be calculated like free fermions (by inserting the effective mass).
				  background-color:: yellow
			- Note that Fermi-Dirac distribution shall be used since we're dealing with fermions!
			  background-color:: red
			  collapsed:: true
				- Never see anything like $e^{-\beta E}$.
			- Experimentalists often use this method to obtain the effective mass.
		- Susceptibility #card
		  card-last-interval:: 30
		  card-repeats:: 2
		  card-ease-factor:: 2.7
		  card-next-schedule:: 2023-05-30T01:00:12.385Z
		  card-last-reviewed:: 2023-04-30T01:00:12.386Z
		  card-last-score:: 5
		  collapsed:: true
			- Idea
			  collapsed:: true
				- First obtain the dependence of $E_0$ on $m$.
				- Since $E=E_0-m\cdot h$, m would be obtained by minimizing the total energy.
				  collapsed:: true
					- $\frac{\partial E}{\partial m}=m(h) \cdot \frac{\partial^2 E}{\partial m^2} {=} h$.
					- Note that $\frac {\partial E}{\partial m}=0$ when $m=0$.
				- $\chi$ could be obtained by $m=h\cdot \chi$.
				  collapsed:: true
					- $\chi=\left(\frac{\partial^2 E}{\partial m^2}\right)^{-1}$
			- With external field, $N_{\uparrow } \neq N_{\downarrow } ,\ \ N_{\uparrow } +N_{\downarrow } =N$
			- Suppose the fermi surface shifts from the original one by $\delta_k$
			  collapsed:: true
				- $$M=\mu_B \cdot\left(\delta N_{\uparrow}-\delta N_\downarrow\right) \Rightarrow \delta k_F=\frac{\lambda^2 M}{\mu_B k_F^2 V}$$
				- Take $V=1$ for simplicity.
			- Obviously the energy shift $\delta E \sim \delta k_F^2$
			  collapsed:: true
				- $\delta E_1$ can be calculated like free fermions, just inserting the effective mass.
				- $\delta E^{(2)}=\frac{1}{2 V} \Sigma f_{\sigma_1 \sigma_2}\left(k_1, k_2\right) \delta n_{k_1 \sigma_1} \delta n_{k_2 \sigma_2}$
				  collapsed:: true
					- Insert the expansion by Legendre polynomials, $\delta E_2=V\left(\frac{k_f^2}{2 \pi^2}\right)^2\left(\delta k_f\right)^2 \cdot 2 f_0^a=\frac{f_0^a}{\mu_B^2} \frac{M^2}{2 V}$
					- $\mu_B$ is the Bohr magneton, the magnetic moment of a single electron.
				-
	- Fermi surface nesting
	  collapsed:: true
		- Large segments of a Fermi surface that can be connected to another large segment of another Fermi surface via the reciprocal lattice vector.
		- ![](https://pica.zhimg.com/80/v2-3f777e9aeff5c939327564d80d4b7b4b_720w.webp?source=1940ef5c)
		-
	-
- # Green Function, Correlation and Dissipation
  collapsed:: true
	- Definitions
	  collapsed:: true
		- [[Green Function]] #card
		  card-last-interval:: 31.26
		  card-repeats:: 1
		  card-ease-factor:: 2.6
		  card-next-schedule:: 2023-06-06T18:04:27.576Z
		  card-last-reviewed:: 2023-05-06T12:04:27.577Z
		  card-last-score:: 5
		  collapsed:: true
			- ((640be051-94a7-40d3-bcc0-581ee03f5cdb)) $G_\sigma\left(\mathbf{r}, t ; \mathbf{r}^{\prime}, t^{\prime}\right):=-\mathrm{i} T\left\langle\psi_\sigma(\mathbf{r}, t) \psi_\sigma^{\dagger}\left(\mathbf{r}^{\prime}, t^{\prime}\right)\right\rangle$
			  collapsed:: true
				- T is the time ordering, where 
				  $$
				  T\left(a\left(t_1\right) b\left(t_2\right)\right)= \begin{cases}a\left(t_1\right) b\left(t_2\right), & t_1>t_2, \\ (-1)^P b\left(t_2\right) a\left(t_1\right), & t_2>t_1,\end{cases}
				  $$
				- Don't forget the minus for fermions!
			- Retarded
			  collapsed:: true
				- $$G_\sigma^{\mathrm{R}}\left(\mathbf{r}, t ; \mathbf{r}^{\prime}, t^{\prime}\right) :=-\mathrm{i} \theta\left(t-t^{\prime}\right)\left\langle\left\{\psi_\sigma(\mathbf{r}, t), \psi_\sigma^{\dagger}\left(\mathbf{r}^{\prime}, t^{\prime}\right)\right\}\right\rangle=-\frac{i}{\hbar} \theta(t)\left\langle\left\{c_k(t), \hat{c}_k^{\dagger}(0)\right\}\right\rangle$$
				- $\chi_{B A}^{ret}\left(t, t^{\prime}\right)=\frac{i}{\hbar} \theta\left(t, t^{\prime}\right)\left\langle\left[\hat{B}(t), \hat{A}\left(t^{\prime}\right)\right]\right\rangle$
				  collapsed:: true
					- This follows ((6410762b-de4a-479c-961f-baa5532f6a5d)).
				- Only retarded (from the earlier time $t'$ to the later time $t$) part.
			- Advanced
			  collapsed:: true
				- $G_\sigma^{\mathrm{A}}\left(\mathbf{r}, t ; \mathbf{r}^{\prime}, t^{\prime}\right)=\mathrm{i} \theta\left(t^{\prime}-t\right)\left\langle\left\{\psi_\sigma(\mathbf{r}, t), \psi_\sigma^{\dagger}\left(\mathbf{r}^{\prime}, t^{\prime}\right)\right\}\right\rangle$
				- Only advanced (from the later time $t'$ to the earlier time $t$) part.
		- Correlation function
		- Spectral function
		  collapsed:: true
			- ((640be0e1-63f2-426b-96be-b5b698e93cdb)) $A(k, \omega):=\frac{1}{2 \pi} \int d t e^{i \omega t}\left\langle\left\{c_k(t) c_k^{\dag}(0)\right\}\right\rangle$
			  collapsed:: true
				- Quite analogous to the ((6401b89c-e517-4e8f-ad4e-f98d5b166921))
		-
	- ## Relations
	  collapsed:: true
		- Green function and spectral function #card
		  collapsed:: true
			- collapsed:: true
			  $$A(\vec{k}, \omega) :=\frac{1}{2 \pi} \int d t e^{i \omega t}\left\langle\left\{c_k(t) c_k^{\dag}(0)\right\}\right\rangle =-\frac{1}{\pi} \operatorname{Im} G^R(k, \omega)$$
				- Start from the definition
				  collapsed:: true
				  $$G^R(k,t)=-\frac{i}{\hbar} \theta(t)\left\langle\left\{c_k(t), \hat{c}_k^{\dagger}(0)\right\}\right\rangle$$
					- Note that there is an **anti-commutator** in the retarded Green function!
				- $A=(G^R-\overline{G^R})/(2i)$, which completes the integral to the whole real axis.
			- collapsed:: true
			  $$G^R(\vec{k}, \omega)=\int d \omega^{\prime} \frac{A\left(k, \omega^{\prime}\right)}{\omega-\omega^{\prime}+i \varepsilon}
			  $$
				- Prop. 
				  collapsed:: true
				  $$\begin{aligned} & \int_{-\infty}^{\infty} d \omega^{\prime} f\left(\omega^{\prime}\right)\left\{P \frac{1}{\omega^{\prime}-\omega}+i \pi \delta\left(\omega^{\prime}-\omega\right)\right\} \\ & =\int_{-\infty}^{\infty} d \omega^{\prime} f\left(\omega^{\prime}\right) \frac{1}{\omega^{\prime}-\omega-i \epsilon}\end{aligned}$$
					- The delta function adds back the imaginary part.
				- Invoke ((6401b89c-a4af-4f0c-b59f-d44a3c164ff6)): $\chi_1(\omega)=\frac{1}{\pi} \mathcal{P} \int_{-\infty}^{\infty} \frac{\chi_2\left(\omega^{\prime}\right)}{\omega^{\prime}-\omega} d \omega^{\prime}$
				  collapsed:: true
					- Note that there is an extra minus in the definition of $A$, thus the denominator of the integrand is also minused.
				-
		- Green function and Matsubara Green function
		  collapsed:: true
			- card-last-score:: 5
			  card-repeats:: 1
			  card-next-schedule:: 2023-05-20T14:11:52.084Z
			  card-last-interval:: 32.57
			  card-ease-factor:: 2.6
			  card-last-reviewed:: 2023-04-18T01:11:52.084Z
			  collapsed:: true
			  $$\begin{equation*}
			  G^R(\omega)=G_{AB}(\omega_n )=\int d\omega ^{\prime }\frac{A_{AB}\left( \omega ^{\prime }\right)}{\omega -\omega ^{\prime } +i\varepsilon } \text{ by } i\omega_n \to \omega+i\varepsilon
			  \end{equation*}$$ #card
				- Summary
				  collapsed:: true
					- Obtain the expectation by brute-force sum over the Boltzmann ensemble (spectral representation).
				- \begin{gather*}
				   \\
				  \begin{aligned}
				  G_{AB}( \omega _{n}) & =\int _{0}^{\beta } d\tau G_{AB} (\tau )e^{i\omega _{n} \tau }\\
				   & =-\int _{0}^{\beta } d\tau \langle T\{A(\tau )B(0)\}\rangle e^{i\omega _{n} \tau }\\
				   & =-\int _{0}^{\beta } d\tau \sum _{\alpha \beta }\frac{1}{Z} e^{-\beta E_{\alpha }}\left< \alpha \left| e^{H\tau } Ae^{-H\tau }\right| \beta \right> < \beta |B|\alpha > e^{i\omega _{n} \tau }\\
				   & =-\frac{1}{Z}\sum_{\alpha \beta } e^{-\beta E_{\alpha }}< \alpha | A| \beta > < \beta |B|\alpha > \int _{0}^{\beta } d\tau e^{( i\omega _{n} +E_{\alpha } -E_{\beta }) \tau }\\
				   & 
				  \end{aligned}\\
				  \end{gather*}
				- On the other hand,
				  \begin{equation*}
				  \int _{0}^{\beta } d\tau e^{( i\omega _{n} +E_{\alpha } -E_{\beta }) \tau } =\frac{e^{( i\omega _{n} +E_{\alpha } -E_{\beta }) \beta } -1}{i\omega _{n} +E_{\alpha } -E_{\beta }} =\frac{\eta e^{( E_{\alpha } -E_{\beta }) \beta } -1}{i\omega _{n} +E_{\alpha } -E_{\beta }}
				  \end{equation*}
				  Thus
				  \begin{equation*}
				  G_{AB}( \omega _{n}) =-\frac{1}{Z}\sum{}_{\alpha \beta } e^{-\beta E_{\alpha }}< \alpha | A| \beta > < \beta |B|\alpha > \frac{\eta e^{( E_{\alpha } -E_{\beta }) \beta } -1}{i\omega _{n} +E_{\alpha } -E_{\beta }}
				  \end{equation*}
				- Comparing with
				  \begin{equation*}
				  \begin{aligned}
				  A_{AB} (\omega ) & =\int _{R} dt\ e^{-i\omega t} \langle A(0)B(t)\rangle \\
				   & =\frac{1}{Z}\sum _{\alpha \beta }\left( e^{-\beta E_{\alpha }} -\eta e^{-\beta E_{\beta }}\right) \langle\alpha |A|\beta \rangle \langle \beta |B|\alpha \rangle \delta ( \omega +E_{\alpha } -E_{\beta })
				  \end{aligned}
				  \end{equation*}
				  finishes the proof.
			-
	- ## Examples
	  collapsed:: true
		- Free fermions
		  id:: 64238eab-5b4c-48b1-ac8a-33fe14061048
		  collapsed:: true
			- collapsed:: true
			  $$
			  G^R(\vec{k}, \omega)=\int d \omega^{\prime} \frac{A\left(\vec{k}, \omega^{\prime}\right)}{\omega-\omega^{\prime}+i\epsilon}=\frac{1}{\omega-\xi_k+i\epsilon}
			  $$ #card
				- id:: 64113383-8089-4db4-8a8b-ebc74bfc5ab7
				  $$
				  \begin{aligned}
				  A(\vec{k}, \omega) & \stackrel{\text { def }}{=} \frac{1}{2 \pi} \int d t e^{i \omega t}\left\langle\left\{c_k(t) c_k^{\dag}(0)\right\}\right\rangle \\
				  & =\frac{1}{2 \pi} \int d t e^{i \omega t} e^{-i \xi_k t} 1=\frac{1}{2 \pi} \cdot 2 \pi \delta\left(\omega-\xi_k\right)
				  \end{aligned}
				  $$
				-
	- ## Matsubara Green Function
	  id:: 642f7907-397a-4fd1-b504-e0060ac5a8be
	  collapsed:: true
		- Idea
		  collapsed:: true
			- Introduce an imaginary time to make things easier.
			- Go back to real time by analytical continuation.
		- Def #card
		  collapsed:: true
			- $$
			  G_{A B}\left(\tau_1, \tau_2\right):=-\frac{1}{\hbar}\left\langle T\left\{A\left(\tau_1\right) B\left(\tau_2\right)\right\}\right\rangle
			  $$
			  where $\tau=it$
		- Prop. $G_{AB} (\tau )=\eta G_{AB} (\tau +\beta )$ #card
		  collapsed:: true
			- \begin{equation*}
			  \begin{aligned}
			  G_{AB} (\tau ) & =-\operatorname{Tr}\left\{\frac{1}{z} e^{-\beta H} e^{H\tau } Ae^{-H\tau } B\right\}\\
			  G_{AB} (\tau +\beta ) & =-\operatorname{Tr}\left\{\frac{1}{z} e^{-\beta H} e^{(\tau +\beta ) H} Ae^{-(\beta +\tau )H} B\right\}\\
			   & =-\operatorname{Tr}\left\{\frac{1}{z} e^{\tau H} Ae^{-\tau H} \cdot e^{-\beta H} B\right\}\\
			   & =-\operatorname{Tr}\left\{\frac{1}{z} e^{-\beta H} \cdot B\cdot e^{\tau H} Ae^{-\tau H}\right\}
			  \end{aligned}
			  \end{equation*}
			- Exchange $B$ and $e^{\tau H} Ae^{-\tau H}$ leads to a factor of $\eta$ (1 for bosons, -1 for fermions)
			-
			- The function is periodical, therefore:
			  collapsed:: true
				- Boson. 
				  \begin{equation*}
				  G_{AB}( \omega _{n}) =\int _{0}^{\beta } d\tau G_{AB} (\tau )e^{i\omega _{n} \tau } ,\omega _{n} =\frac{2\pi }{\beta } n
				  \end{equation*}
				- Fermion.
				  \begin{equation*}
				  G_{AB}( \omega _{n}) =\int _{0}^{\beta } d\tau G_{AB} (\tau )e^{i\omega _{n} \tau } ,\omega _{n} =\frac{\pi }{\beta } \cdot ( 2n+1)
				  \end{equation*}
		- Analytical continuation
		  collapsed:: true
			- Idea
			  collapsed:: true
				- $$G_{AB}( \omega _{n})\rightarrow G_{AB}^{\text{Ret}} (\omega )\ \ \text{ by } i\omega _{n}\rightarrow \omega +i\varepsilon$$
		- Example. Calculate the particle-number correlation
		  collapsed:: true
			-
- # Linear Response
  collapsed:: true
	- Defs and Setup
	  collapsed:: true
		- Linear response function $\chi(t,t')$ #card
		  collapsed:: true
			- $\hat H=\hat H_0-h(t)\hat A$
			- $\langle\hat{B}\rangle(t)=y(t)$ satisfies $y(t)=\int_{-\infty}^t d t^{\prime} \chi\left(t, t^{\prime}\right) h\left(t^{\prime}\right)$
		- Correlation
		  collapsed:: true
			- $S_{B A}\left(t, t^{\prime}\right):=\left\langle\hat{B}(t) \hat{A}\left(t^{\prime}\right)\right\rangle$
	- Introduce ((645712fb-6e94-424c-a970-bb124f0c8e65))
	  collapsed:: true
		- Leave the background part on the observable and the perturbation part to the density matrix (state).
		  collapsed:: true
			- $$
			  \frac{d \rho_I}{d t}=\frac{i}{\hbar} h(t)\left[\hat{A}_I, \hat{\rho}_I\right]
			  $$
		- Approximation
		  collapsed:: true
			- $h(t) \ll 1 . \Rightarrow \rho_I$ varies very slowly!
			- Thus we may approximate $\left[\hat{A}_I, \hat{\rho}_I(t)\right]$ by $\left[\hat{A}_I, \hat{\rho}_I(0)\right]$
			  collapsed:: true
				- $$\hat{\rho }_{I} (t)=\hat{\rho }_{0} +\int _{-\infty }^{t} dt^{\prime }\frac{i}{\hbar } h\left( t^{\prime }\right)\left[\hat{A}_{I}\left( t^{\prime }\right) ,\hat{\rho }_{0}\right]$$
			- collapsed:: true
			  $$y(t)=y(0)+\int _{-\infty }^{t} dt^{\prime }\frac{i}{\hbar } h\left( t^{\prime }\right)\operatorname{tr}\left\{\hat{B}_{I} (t)\left[\hat{A}_{I}\left( t^{\prime }\right) ,\hat{\rho }_{0}\right]\right\}$$
				- We may apply cyclic permutation to the expression inside the trace to obtain 
				  $y(t)=y(0)+\int_{-\infty}^{t^{\prime}} d t^{\prime} h\left(t^{\prime}\right) \ \frac{i}{\hbar}\left\langle\left[\hat{B}_I(t), \hat{A}_I\left(t^{\prime}\right)\right]\right\rangle_{\rho_0}$
				-
		- Conclusion
		  collapsed:: true
			- The kernel is $\chi(t,t')= \frac{i}{\hbar}\left\langle\left[\hat{B}_I(t), \hat{A}_I\left(t^{\prime}\right)\right]\right\rangle_{\rho_0}$ #card
			  id:: 6410762b-de4a-479c-961f-baa5532f6a5d
			  card-last-interval:: -1
			  card-repeats:: 1
			  card-ease-factor:: 2.5
			  card-next-schedule:: 2023-05-21T16:00:00.000Z
			  card-last-reviewed:: 2023-05-21T00:54:57.551Z
			  card-last-score:: 1
			  collapsed:: true
				- Interaction picture to separate $H_0$ and $A$
				- Key idea: Slow-varying approximation
				  collapsed:: true
					- Approximate $\left[\hat{A}_I, \hat{\rho}_I(t)\right]$ by $\left[\hat{A}_I, \hat{\rho}_I(0)\right]$
				- The remainder is purely routine: Write down the integral and use the cyclic symmetry of trace.
	- {{embed ((6401b89c-e517-4e8f-ad4e-f98d5b166921))}}
- # Thomas-Fermi Screening
  collapsed:: true
	- ## Idea
	  collapsed:: true
		- In a Fermi liquid, some positive external charge would attract electrons to gather near it, thus weakens the external field.
		  collapsed:: true
			- The actual field is solved by consistency equations.
		- This can be generalized to the case of some dynamical external field.
	- ## Setup
	  collapsed:: true
		- External field $V_{ext}(r,t)$, effective field $V_{\text {eff }}=V_{\text {ext }}+\delta V$
		  collapsed:: true
			- For an external charge it is $\operatorname{V_{ext}}(\vec{r})=-e \frac{Q}{r}$
		- $\delta n(\vec{r}):=n(\vec{r})-n_0(\vec{r})$
	- RPA Approximation #card
	  id:: 64118d95-90c5-42ef-afcf-2df672505b13
	  card-last-interval:: 30
	  card-repeats:: 1
	  card-ease-factor:: 2.36
	  card-next-schedule:: 2023-05-13T11:33:24.775Z
	  card-last-reviewed:: 2023-04-13T11:33:24.775Z
	  card-last-score:: 3
	  collapsed:: true
		- 1. The behavior is similar to free fermi gas
		  2. The effect on number density is local
	- ## Static
	  collapsed:: true
		- The final result is 
		  collapsed:: true
		  $$
		  \tilde{V}_{\text {eff }}(\vec{k})=-\frac{4 \pi Q e}{k^2+4 \pi \varepsilon^2 N_0}
		  $$ #card
			- Use ((64118d95-90c5-42ef-afcf-2df672505b13)),
			  $$
			  n_0=\sum_{k \sigma} \frac{1}{1+e^{\left.\beta ( \varepsilon_k+\mu\right)}} \quad n(\vec{r})=\sum_{k \sigma} \frac{1}{1+e^{\beta\left[\varepsilon_k(\vec{r})-\mu\right]}}
			  $$
			- Therefore 
			  collapsed:: true
			  $$\begin{aligned}
			  \delta n(r ) & =\frac{\partial n}{\partial V_{\text{eff }} (r)}\operatorname{V_{eff}} (r)=-\frac{\partial n}{\partial \mu } V_{\text{eff}} (r)\\
			   & =-N(0)\operatorname{Veff} (r)
			  \end{aligned}$$
				- N0 is the number density at the fermi surface
			- Plug in $-\Delta \phi=4 \pi[Q \delta(\vec{r})-e \cdot \delta n(\vec{r})]$ and Fourier transformation we could obtain the desired result.
			-
			- Exercise. Obtain the Yukawa potential from the result.
	- ## Dynamic
	  collapsed:: true
		- Setup
		  collapsed:: true
			- $$
			  \hat{H}=\hat{H}_0+\hat{H}^{\prime} . \quad \hat{H}^{\prime}=\int d \vec{r} \hat{n}(\vec{r}, t) \cdot V_{\text {ext }}(\vec{r}, t)
			  $$
			- $$\langle \delta \hat{n} (r,t)\rangle =\int _{-\infty }^{t} dt^{\prime } \chi ^{\text{ret }}\left( r-r',t-t^{\prime }\right) V_{\text{ext }} (r' ,t)$$
		- Prop. 
		  collapsed:: true
		  $$
		  \langle \delta \hat{n} (\vec{k} ,\omega )\rangle =\chi_{0}^{\text{ret }} (\vec{k} ,\omega )V_{\text{ext }} (\vec{k} ,\omega )
		  $$ #card
			- 动量空间卷积变乘积
		-
		-
- # Local Magnetic Moment
  collapsed:: true
	- Summary #card
	  card-last-interval:: 31.26
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2023-06-06T18:07:45.793Z
	  card-last-reviewed:: 2023-05-06T12:07:45.794Z
	  card-last-score:: 5
	  collapsed:: true
		- Single-impurity Anderson Model
		  $$H= \sum_{k \sigma} E_k c^\dag_{k \sigma} c_{k \sigma} + \sum_\sigma E_d c^\dag_{d \sigma} c_{d \sigma} + \sum_{k \sigma}\left(V_{k d} c_{k \sigma}^{\dag} c_{d \sigma}+(c.c.)\right)+U n_{d \uparrow} n_{d \downarrow} .$$
		- Mean-field approximation
		  $$H=\sum _{k\sigma } E_{k} c_{k\sigma }^{\dagger } c_{k\sigma } +\sum _{\sigma } E_{d} c_{d\sigma }^{\dagger } c_{d\sigma } +\sum _{k\sigma }\left( V_{kd} c_{k\sigma }^{\dagger } c_{d\sigma } +(h.c.)\right) + \\Un_{d\uparrow }< n_{d\downarrow }> + U< n_{d\uparrow }> n_{d\downarrow }$$
		-
	- ## Model: Single-impurity Anderson Model
	  collapsed:: true
		- 'Single impurity' corresponds to the second term, which is the orbital electrons at a single site.
		- collapsed:: true
		  $$H= \sum_{k \sigma} E_k c^\dag_{k \sigma} c_{k \sigma} + \sum_\sigma E_d c^\dag_{d \sigma} c_{d \sigma} + \sum_{k \sigma}\left(V_{k d} c_{k \sigma}^{\dag} c_{d \sigma}+(c.c.)\right)+U n_{d \uparrow} n_{d \downarrow} .$$
			- First term: Electrons moving freely in the solid. Could occupy different momenta.
			- Second term: Localized electrons on the $d$ orbit. No summation over space or position.
			- Third term: Hopping between moving electrons and localized ones. We may assume $V_{kd}$ is real.
			  collapsed:: true
				- '轨道杂化'
			- Last term: Columb interaction within the same orbit.
		- Notes on the properties
		  collapsed:: true
			- If we ignore the interaction (hopping) term, the local magnetic moment depends on the position of the Fermi surface.
			  collapsed:: true
				- If surface above $E_d$ but below $E_d + U$, then the orbit would be occupied by a single electron, thus producing a magnetic moment.
			- However, the interaction term would lead to hybridization (杂化) of different states
		- Two limits of the Single-impurity model #card
		  collapsed:: true
			- Notation: $\Delta$ is the width of the energy.
			- collapsed:: true
			  $$
			  U \gg \left|\epsilon_d\right| \gg \Delta
			  $$
				- Weak hybridization
				- Occupation number = 1 -> Local magnetic moment
			- collapsed:: true
			  $$
			  U \gg \Delta \gg |\epsilon_d|
			  $$
				- Strong hybridization. 
				  We can't talk about a well-defined local orbit; rather, the electron is mixed into the Fermi sea.
				-
		-
	- ## [[Mean-Field Approximation]]
	  collapsed:: true
		- collapsed:: true
		  $$\begin{aligned}
		  H_{MF} & =\sum _{k\sigma } E_{k} c_{k\sigma }^{\dagger } c_{k\sigma } +\sum _{\sigma } E_{d} c_{d\sigma }^{\dagger } c_{d\sigma } +\sum _{k\sigma }\left( V_{kd} c_{k\sigma }^{\dagger } c_{d\sigma } +(h.c.)\right) +Un_{d\uparrow }< n_{d\downarrow }> +U< n_{d\uparrow }> n_{d\downarrow }\\
		   & =\sum _{k\sigma } E_{k} c_{k\sigma }^{\dagger } c_{k\sigma } +\sum _{\sigma } E_{d\sigma } c_{d\sigma }^{\dagger } c_{d\sigma } +\sum _{k\sigma }\left( V_{kd} c_{k\sigma }^{\dagger } c_{d\sigma } +(h.c.)\right)
		  \end{aligned}$$
		  where $E_{d\sigma } =E_{d} +U< n_{d,-\sigma }>$.
			- Obtained by ignoring 2nd variation
			- The consistency relation can be obtained by solving $\langle n_{d\uparrow } \rangle$ and  $\langle n_{d\downarrow } \rangle$
		- In principle, the bilinear form above can be diagonalized. But the brute-force calculation is quite arduous.
		  collapsed:: true
			- Note that the simplest way is $\left[ H_{\mathrm{HF}}^{\mathrm{A}} ,a_{n\sigma }^{\dagger }\right] =\epsilon _{n\sigma } a_{n\sigma }^{\dagger }$. Moreover, we don't need to calculate every single commutator; since each exchange either gives -1 or +1, we only need to examine which gives +1 and thus non-commutative. [Exercise]
		- After diagonalization:
		  collapsed:: true
			- $$\hat{H}_{MF} =\sum _{n\sigma } \varepsilon_{n\sigma } c_{n\sigma }^{\dagger } c_{n\sigma }$$
	- ## Obtain [[Green Function]]
	  collapsed:: true
		- #+BEGIN_NOTE
		  We often want Green function rather than the spectrum.
		  #+END_NOTE
		- Calculate the ((642f7907-397a-4fd1-b504-e0060ac5a8be)):
		  collapsed:: true
			- $$G_{dd,\sigma }( \omega _{n}) =-\int _{0}^{\beta } d\tau e^{i\omega _{n} \tau } T\left\{\left< c_{d\sigma } (\tau )c_{d\sigma }^{\dagger } (0)\right> \right\}$$
			- It is hard to calculate directly. But we may first calculate the MGF in the energy representation, then apply a basis transformation.
			  collapsed:: true
				- As a standard result for free fermions, 
				  collapsed:: true
				  $$G_{m\sigma }( w_{n}) =\frac{1}{iw_{n} -\epsilon _{m}}$$
					- Note that here $\omega \to iw_n$
			- We may define a matrix to compactly represent the basis transformation.
			  collapsed:: true
				- $$\hat{G}_{\sigma }( \omega _{n}) =\sum _{n\sigma }\frac{1}{i\omega _{n} -\varepsilon _{n}} |n\sigma \rangle \langle n\sigma |$$
				- Then
				  $$G_{dd,\sigma }( \omega _{n}) =< d\sigma |\hat{G}_{\sigma }( w_{n}) |d\sigma > $$
			- Plug into $( iw_{n} -\hat{h}_{MF})\hat{G}_{\sigma } =\mathbb{1}$:
			  collapsed:: true
				- \begin{aligned}
				  \langle d\sigma |( iw_{n} -\hat{h}_{MF})\hat{G}_{\sigma } |k\sigma \rangle =0:\\
				  ( i\omega _{n} -E_{d\sigma })< d\sigma | \hat{G}( \omega _{n})| \vec{k} \sigma > -V_{kd}< k\sigma | \hat{G}( \omega _{n})| k\sigma > =0.\\
				  ( i\omega _{n} -E_{d\sigma }) G_{d;k\sigma }( \omega _{n}) -V_{kd} G_{k\sigma }( \omega _{n}) =0\\
				   \\\\
				  \langle \vec{k} \sigma |( iw_{n} -\hat{h}_{MF})\hat{G}_{\sigma } |d\sigma \rangle =0:\\
				  ( i\omega _{n} -\epsilon _{k})< \vec{k} \sigma | \hat{C}_{(}( \omega _{n})| d\sigma > -V_{kd}< d\sigma | \hat{G}( \omega _{n})| d\sigma > =0\text{. }\\
				  ( iw_{n} -\epsilon _{k}) G_{k;d\sigma }( w_{n}) -V_{kd} G_{dd,\sigma }( w_{n}) =0.\\
				   \\\\
				  \langle d\sigma |( iw_{n} -\hat{h}_{MF})\hat{G}_{\sigma } |d\sigma \rangle =1:\\
				  ( iw_{n} -E_{d\sigma })< d\sigma | \hat{G}( \omega _{n})| d\sigma > -\sum_k V_{kd}< k\sigma |\hat{G}( \omega _{n}) |d\sigma > =1.\\
				  ( iw_{n} -E_{d\sigma }) G_{dd,\sigma }( w_{n}) - \sum_k V_{kd} G_{k;d\sigma }( w_{n}) =1
				  \end{aligned}
				-
				- We want to solve $G_{dd,\sigma}$ from the above equations.
				  collapsed:: true
					- Use (5), we see that $V_{kd}G_{dd,\sigma}/( iw_{n} -\epsilon _{k})= G_{k;d\sigma }( w_{n})$
					- Plug into the last equation we see $(i\omega_n-E_{d\sigma})G_{dd,\sigma}-\sum_k V_{kd}^2 G_{dd,\sigma}/(i\omega_n-\varepsilon_k)=1$, which allows for solving the desired Green function.
					-
			- Finally
			  $$G_{dd,\sigma }( \omega _{n}) =\frac{1}{i\omega _{n} -E _{d\sigma } -\sum _{k}\frac{V_{kd}^{2}}{i\omega _{n} -\epsilon _{k}}}$$
			  and we may obtain the retarded Green function by analytical continuation $\displaystyle \omega _{n}\rightarrow i( \omega +\epsilon )$
			  \begin{equation*}
			  \left[ G_{dd,\sigma }^{\operatorname{ret}} (\omega )\right]^{-1} =\omega -E_{d\sigma } -\sum _{k}\frac{V_{kd}^{2}}{\omega -\epsilon _{k} +i0^{+}}
			  \end{equation*}
			-
		-
	- ## Self-Energy Correction
	  collapsed:: true
		- collapsed:: true
		  $$\begin{equation*}
		  \Sigma _{d\sigma }^{ret}( \omega ) :=\sum _{k}\frac{V_{kd}^{2}}{\omega -\epsilon _{k} +i0^{+}}
		  \end{equation*}$$
			- This is motivated by 
			  \begin{equation*}
			  \left[ G_{dd,\sigma }^{\operatorname{ret}} (\omega )\right]^{-1} =\omega -E_{d\sigma } -\sum _{k}\frac{V_{kd}^{2}}{\omega -\epsilon _{k} +i0^{+}}
			  \end{equation*}
		- Take real and imaginary parts and the Cauchy principle value:
		  collapsed:: true
		  \begin{gather*}
		  Re\ \Sigma _{d\sigma }^{ret}( \omega ) =\frac{1}{V}\int \frac{d^{3} k}{( 2\pi )^{3}}\frac{V_{kd}^{2}}{\omega -\epsilon _{k} +i0^{+}}\mathbf{P}\left(\frac{V_{kd}^{2}}{\omega -\epsilon _{k}}\right)\\
		  Im\ \Sigma _{d\sigma }^{ret}( \omega ) =\sum _{k} -\pi \delta ( \omega -E_{k}) V_{kd}^{2} =-\pi \left< V_{kd}^{2}\right> _{FS} N( \omega ) \\
		  \\
		  \end{gather*}
			- FS means Fermi surface
		- Then 
		  \begin{equation*}
		  \operatorname{G}_{d\sigma }^{\operatorname{ret}} (\omega )=\frac{1}{\omega -E_{d\sigma } -\operatorname{Re} \Sigma (\omega )-i\operatorname{Im} \Sigma (\omega )}
		  \end{equation*}
		  Compare with the free fermions, we see that the real part shifts the **peak** of the spectrum function and the imaginary part controls the **width** of the peak.
		- Two approximations:
		  collapsed:: true
			- $\displaystyle \Sigma ( \omega )\rightarrow \Sigma ( E_{d\sigma } +Re\ \Sigma )$
			- $\displaystyle Re\ \Sigma \ \rightarrow \ 0$ (Since we can't accurately determine $\displaystyle E_{d\sigma }$ from the first place, it is meaningless to keep a high accuracy of the shift)
			- Therefore, we are actually considering 
			  \begin{equation*}
			  Im\ \Sigma _{d\sigma }^{ret}( \omega ) =-\pi \left< V_{kd}^{2}\right> _{FS} N( E_{d\sigma }) :=-\Delta 
			  \end{equation*}
			  which is consistent with our estimation by Fermi's golden rule (up to a factor of $\displaystyle \pi $)
		- Then 
		  \begin{equation*}
		  G_{dd\sigma }( \omega ) =\frac{1}{\omega -E_{d\sigma } +i\Delta }
		  \end{equation*}
		  Moreover, 
		  \begin{equation*}
		  \rho _{d\sigma } (\omega )=A_{d\sigma } (\omega ):=-\frac{1}{\pi } Im\ G_{dd\sigma }^{ret} (\omega )=\frac{1}{\pi }\frac{\Delta }{(\omega -E_{d\sigma } )^{2} +\Delta ^{2}}
		  \end{equation*}
	- ## Consistency Equation
	  collapsed:: true
		- Idea: First calculate in energy eigenbasis, then use basis transformation.
		  \begin{equation*}
		  \begin{aligned}
		  \langle n_{d\sigma } \rangle  & =\left< c_{d\sigma }^{\dagger } c_{d\sigma } \right\rangle \\
		   & =\sum _{nm}\left< c_{n\sigma }^{\dagger } c_{m\sigma }\right> \langle d\sigma |n\sigma \rangle \langle m\sigma |d\sigma \rangle .\\
		   & =\sum _{n}\left< c_{n\sigma }^{\dagger } c_{n\sigma }\right> \Bigl| \langle d\sigma |n\sigma \rangle \Bigl|^{2}\\
		   & =\sum _{n} f( E_{n\sigma })\Bigl| \langle d\sigma |n\sigma \rangle \Bigl|^{2}
		  \end{aligned}
		  \end{equation*}
		  f is the Fermi-Dirac distribution.
		- Recall that 
		  collapsed:: true
		  \begin{equation*}
		  A_{d\sigma } (\omega )=\sum _{n}\Bigl| \langle d\sigma |n\sigma \rangle \Bigl|^{2} \delta ( \omega -E _{n\sigma })
		  \end{equation*}
			- $$A_{d\sigma}(\omega)=\sum_n \Bigl| \langle d\sigma |n\sigma \rangle \Bigl|^{2} A_{n\sigma}(\omega)$$
			  $$A_{n\sigma}(\omega):=\int dt e^{-i \omega t} \left\langle c_{n\sigma}(t)c^\dagger_{n\sigma}(0) \right\rangle=\delta(\omega-E_{n\sigma})$$
			- This is actually spectral representation.
		- So
		  \begin{equation*}
		  \begin{aligned}
		  \langle n_{d\sigma } \rangle  & =\sum _{n} f( E_{n\sigma })\Bigl| \langle d\sigma |n\sigma \rangle \Bigl|^{2}\\
		   & =\int d\omega \ f( \omega ) A_{d\sigma }( \omega )
		  \end{aligned}
		  \end{equation*}
		- Further simplification: Consider $\displaystyle T=0$, so $\displaystyle f( \omega )$ becomes a heaviside function.
		  \begin{gather*}
		  \begin{aligned}
		  \langle n_{d\sigma } \rangle  & =\sum _{n} f( E_{n\sigma })\Bigl| \langle d\sigma |n\sigma \rangle \Bigl|^{2}\\
		   & =\int _{-\infty }^{0} d\omega \frac{1}{\pi }\frac{\Delta }{(\omega -Ed\sigma )^{2} +\Delta ^{2}}\\
		   & =\frac{1}{\pi }\cot^{-1}\left(\frac{Ed\sigma }{\Delta }\right) =\frac{1}{\pi } \omega ^{-1}(\frac{E_{d} +U\langle n_{d,-\sigma } \rangle }{\Delta } ）
		  \end{aligned}\\
		  \begin{aligned}
		   & \\
		   & 
		  \end{aligned}
		  \end{gather*}
		- Note that spin-up and spin-down depends on each other, so we may not solve directly. However, we can consider whether there'll be symmetry breaking, i.e. $\displaystyle n_{d,\uparrow } \neq n_{d,\downarrow }$
		  collapsed:: true
			- Special case: Consider $\displaystyle E_{d} =-U/2$, now $\displaystyle < n_{d,\uparrow }> +< n_{d,\downarrow }> =1$.
			- Take $\displaystyle < n_{d,\uparrow }> =1/2+x$, we can obtain a consistency relation and examine nonzero solutions.
- # Kondo Effect
  collapsed:: true
	- ## Degenerate Second-Order Perturbation
	  id:: 64239f9f-7660-4553-ab22-80685caf6f6c
	  collapsed:: true
		- Effective Hamiltonian #card
		  collapsed:: true
			- collapsed:: true
			  $$\left< \alpha |H_{eff}^{( 2)} |\beta \right> =\sum _{n} \langle \alpha |W|n\rangle \langle n|W|\beta \rangle \frac{1}{2}\left(\frac{1}{E_{\alpha } -E_{n}} +\frac{1}{E_{\beta } -E_{n}}\right)$$
				- $\alpha,\beta$ are (nearly) degenerate energy levels with $\langle \alpha |W|\beta\rangle =0$
				- $n$ is some state in the excited space
			- Intuitively, we can jump from $\alpha$ to an intermediate state $n$, then jump from $n$ to $beta$, multiplied by an energy factor.
			- Proof
			  collapsed:: true
				- *To be completed
- # Electron-Lattice Interaction
  collapsed:: true
	- Motivation
	  collapsed:: true
		- In a lattice we have the interaction of electrons and nuclei.
		  The electrons move freely in the solid while the nuclei are mainly fixed.
		- We want to write down the second-quantized Hamiltonian for the interaction.
	- Setup
	  collapsed:: true
		- Convention: Lower-case letters for quantities of electrons; upper-case for quantities of nuclei.
	- ## 1D Oscillator Chain and Phonons
	  collapsed:: true
		- Summary
		  collapsed:: true
			- Write down the classical Hamiltonian.
			- Perform Fourier transformation to obtain a decoupled form.
			- Rewrite the Hamiltonian by creation and annihilation operators to obtain oscillators.
		- Classical Hamiltonian:
		  \begin{equation*}
		  H=\sum _{n}\frac{P_{n}^{2}}{2M} +\frac{1}{2} M\omega _{0}^{2}\sum _{n}( X_{n} -X_{n+1})^{2}
		  \end{equation*}
		- Perform Fourier transformation (on the lattice) to obtain the oscillation modes for second quantization:
		  collapsed:: true
		  \begin{gather*}
		  P_{n} =\frac{1}{\sqrt{N}}\sum _{k} e^{ikna}\tilde{P}_{k}\\
		  X_{n} =\frac{1}{\sqrt{N}}\sum _{k} e^{ikna}\tilde{X}_{k}
		  \end{gather*}
			- Comments:
			  collapsed:: true
				- $P_{-k} =P_{k}^{*}$ and $X_{-k} =X_{k}^{*}$
				- $\sum _{n} P_{n}^{2} =\sum _{k} P_{k} P_{k}^{*}$
		- Plug into the expression of the classical Hamiltonian, we obtain
		  \begin{gather*}
		  \begin{aligned}
		  \sum _{n} X_{n} X_{n+1} & =\frac{1}{N}\sum _{n}\sum _{kk'} e^{ikna} X_{k} e^{ik'(n+1)a} X_{k'}\\
		   & =\sum _{k} \ \ e^{ika} X_{-k} X_{k}\\
		  H & =\frac{1}{2M}\sum _{k} P_{-k} P_{k} +\frac{M\omega _{0}^{2}}{2}\left( 2\sum _{n} X_{n}^{2} -2\sum _{k} X_{n} x_{n+1}\right)\\
		   & =\frac{1}{2M}\sum _{k} P_{-k} P_{k} +\frac{M\omega _{0}^{2}}{2}\sum _{k} X_{-k} X_{k}\left[ 2-\left( e^{ika} +e^{-ika}\right)\right]\\
		   & =\frac{1}{2M}\sum _{k} P_{-k} P_{k} +\frac{M\omega _{0}^{2}}{2}\sum _{k} \omega _{k}^{2} X_{-k} X_{k}
		  \end{aligned}\\
		  \omega _{k}^{2} =2\omega _{0}^{2}( 1-\cos ka)\overset{k\ll 1}{=} \omega _{0}^{2} k^{2} a^{2}
		  \end{gather*}
		- Obviously it is a sum of lots of oscillators, so we use second quantization.
		  \begin{equation*}
		  \begin{aligned}
		  [\hat{P}_{n} ,\hat{X}_{m}] & =-i\delta _{nm} .\\
		  [\hat{P}_{k} ,\hat{X}_{k^{\prime }}] & =\frac{1}{N}\sum _{nm}[\hat{P}_{n} ,\hat{X}_{m}] e^{-ikna} e^{-ik^{\prime } ma}\\
		   & =\frac{1}{N} (-i)\sum _{nm} \delta _{nm} e^{-ikna} e^{-ik^{\prime } ma}\\
		   & =-i\frac{1}{N}\sum _{n} e^{i\left( k+k^{\prime }\right) na}\\
		   & =-i\delta _{k+k^{\prime } ,0}\\
		  [\hat{P}_{k} ,\hat{X}_{-k^{\prime }}] & =-i\delta _{kk^{\prime }}
		  \end{aligned}
		  \end{equation*}
		- Now we should write the creation and annihilation operators. $\tilde{Q}_{k}$ and $\tilde{X}_{k}$ are normalized operators, whose coefficient can be determined from the Hamiltonian.
		  \begin{gather*}
		  \tilde{P}_{k} =\frac{1}{\sqrt{2M\omega _{k}}} P_{k} ;\ \ \tilde{Q}_{k} =\sqrt{\frac{M\omega _{k}}{2}} Q_{k}\\
		  b_{k} =\tilde{Q}_{k} +i\tilde{P}_{k}\\
		  \begin{aligned}
		  \hat{H} =\sum _{k}\hat{H}_{k} & =\sum _{k}\frac{1}{2} \omega _{k}\left( b_{k}^{\dagger } b_{k} +b_{-k}^{\dagger } b_{-k} +1\right)\\
		   & =\sum _{k} \omega _{k}\left( b_{k}^{\dagger } b_{k} +\frac{1}{2}\right) .
		  \end{aligned}
		  \end{gather*}
		- Note that this is a bit different from conventional oscillators (eg. $[\hat{P}_{k} ,\hat{X}_{-k^{\prime }}] =-i\delta _{kk^{\prime }}$, $k$ pairs with $-k$), though the final result is similar.
		- Also we may express $X$ and $P$ by creation and annihilation operators:
		  \begin{equation*}
		  \begin{aligned}
		  \hat{X}_{n} & =\sum _{k}\sqrt{\frac{2}{MN\omega _{k}}} e^{ikna}\frac{1}{2}\left( b_{k} +b_{-k}^{+}\right)\\
		   & =\sum _{k}\frac{1}{\sqrt{2MN\omega _{k}}}\left( b_{k} +b_{-k}^{+}\right) e^{ikna}\\
		   & 
		  \end{aligned}
		  \end{equation*}
	- ## Phonons in 3D
	  collapsed:: true
		- Summary
		  collapsed:: true
			- Expand the interaction to second order (the first order vanishes at equilibrium).
			  The bilinear form would lead to a similar result to the oscillator chain.
		- Classical Hamiltonian:
		  \begin{equation*}
		  H=\sum _{i}\frac{P_{i}^{2}}{2M} +\sum _{i< j} V(\vec{R}_{i} -\vec{R}_{j})
		  \end{equation*}
		- Let $\vec{R}_{i} =\overrightarrow{R^{0}}_{i} +\vec{Q}_{i}$, then we may expand the interaction to second order:
		  \begin{equation*}
		  V(\vec{R}_{i} -\vec{R}_{j}) =V_{0} +\frac{1}{2}\sum _{i< j}\frac{\partial ^{2} V}{\partial R^{a} \partial R^{b}}\left( Q_{i}^{a} -Q_{j}^{a}\right)\left( Q_{i}^{b} -Q_{j}^{b}\right)
		  \end{equation*}
		  It would diagonalize if we transform to momentum space.
		- Note that in 3D we also have polarization, so we shall denote the modes by $(\vec{k} ,\lambda )$. The result is 
		  \begin{equation*}
		  H=\sum _{k\lambda }\frac{P_{-k\lambda } P_{k\lambda }}{2M} +V^{0} +\frac{M}{2}\sum _{k\lambda } \omega _{k\lambda }^{2} Q_{-k\lambda } Q_{k\lambda }
		  \end{equation*}
		- The Fourier transformation writes
		  \begin{equation*}
		  Q_{k\lambda } =\frac{1}{\sqrt{N}}\sum _{i}\hat{\lambda }_{k} \cdot \vec{Q}_{i} e^{-i\vec{k} \cdot \vec{R}_{i}^{0}}
		  \end{equation*}
		  where $\hat{\lambda }_{k}$ is the polarization vector.
		- The process of second quantization is analogous to above.
		  \begin{equation*}
		  \hat{H} =V^{0} +\sum _{k\lambda }\left( b_{k\lambda }^{\dagger} b_{k\lambda } +\frac{1}{2}\right) \omega _{k\lambda }
		  \end{equation*}
	- ## Electron-Phonon Interaction
	  collapsed:: true
		- Summary #card
		  collapsed:: true
			- First write down the classical Hamiltonian
			  \begin{equation*}
			  H_{ei} =\sum{}_{ij} V_{ei}(\vec{r}_{j} -\vec{R}_{i}) 
			  \end{equation*}
			- Expand the interaction to first order of $\vec R_i$ and perform Fourier transformation (since translation invariance is manifest).
			- Perform quantization and obtain the scattering vertex
		- collapsed:: true
		  \begin{equation*}
		  H_{ei} =\sum{}_{ij} V_{ei}(\vec{r}_{j} -\vec{R}_{i}) 
		  \end{equation*}
			- Note that 'ei' stands for 'electron-ion'.
		- However, we perform 2nd quantization to electrons while only 1st quantization to nuclei (since they're localized and distinguishable)
		  collapsed:: true
			- \begin{gather*}
			  \vec{R}_{i} =\vec{R}_{i}^{0} +\vec{Q}_{i} =\vec{R}_{i}^{0} +\sum _{k\lambda }\frac{1}{\sqrt{2MN\omega _{k\lambda }}}\left( b_{k\lambda } +b_{-k\lambda }^{+}\right)\hat{\lambda }_{k} e^{i\vec{k} \cdot \vec{R}_{i}^{0}}\\
			  \begin{aligned}
			  H_{ei} & =\sum _{ij} V_{ei}\left(\vec{r}_{j} -\vec{R}_{i}^{0}\right) -\sum _{ij}\frac{\partial V_{ei}}{\partial \vec{r}_{j}}\vec{Q}_{i}\\
			   & =\sum _{is} V_{ei}\left(\vec{r}_{j} -\vec{R}_{i}^{0}\right) -\sum _{ij} \nabla _{j} V_{ei}\overrightarrow{Q_{i}}
			  \end{aligned}
			  \end{gather*}
		- Perform a Fourier transformation to the lattice:
		  collapsed:: true
			- \begin{gather*}
			  V_{ei}(\vec{r}) =\frac{1}{N}\sum _{k} V_{ei}(\vec{k}) e^{ik\cdot r}\\
			  \begin{aligned}
			  H_{ei} & =V^{0} -\sum _{ij} \nabla _{j} V_{ei}\left(\vec{r}_{j} -\vec{R}_{i}^{0}\right) \cdot \vec{Q}_{i}\\
			   & =V^{0} -\sum _{ij} \nabla _{j} \ \frac{1}{N}\sum _{k} V_{ei} (\vec{k} )e^{i\vec{k} \cdot \left(\vec{r}_{j} -\vec{R}_{i}^{0}\right)} \cdot \vec{Q}_{i}\\
			   & =V^{0} -\sum _{ij} \ \frac{1}{N}\sum _{k}( i\vec{k}) V_{ei} (\vec{k} )e^{i\vec{k} \cdot \left(\vec{r}_{j} -\vec{R}_{i}^{0}\right)} \cdot \vec{Q}_{i}\\
			   & =V^{0} -\frac{1}{N}\sum _{ij}\sum _{k}\sum _{q\lambda } \ ( i\vec{k}) V_{ei} (\vec{k} )e^{i\vec{k} \cdot \left(\vec{r}_{j} -\vec{R}_{i}^{0}\right)}\frac{1}{\sqrt{2MN\omega _{q\lambda }}}\left( b_{q\lambda } +b_{-q\lambda }^{\dagger }\right)\hat{\lambda }_{q} e^{i\vec{q} \cdot \vec{R}_{i}^{0}}
			  \end{aligned}
			  \end{gather*}
		- First perform the summation over $i$.
		  collapsed:: true
			- Note that here's a subtlety: $k$ could take continuous values while $q$ must be in the Brillione zone.
			  collapsed:: true
				- In lattices, momenta could differ by a inverse lattice vector.
			- Thus
			  \begin{equation*}
			  \frac{1}{N}\sum _{i} e^{i\vec{k} \cdot \left(\vec{r}_{j} -\vec{R}_{i}^{0}\right)} e^{i\vec{q} \cdot \vec{R}_{i}^{0}} =e^{i\vec{k} \cdot \vec{r}_{j}}\sum _{L} \delta (\vec{k} -\vec{q} +\vec{L})
			  \end{equation*}
			  the summation is over all inverse lattice vectors.
			- \begin{equation*}
			  \begin{aligned}
			  H_{ei} & =V^{0} -\frac{1}{N}\sum _{{i} j}\sum _{k}\sum _{q\lambda } \ ( i\vec{k}) V_{ei} (\vec{k} ) e^{i\vec{k} \cdot \left(\vec{r}_{j} -\vec{R}_{i}^{0}\right)}\frac{1}{\sqrt{2MN\omega _{q\lambda }}}\left( b_{q\lambda } +b_{-q\lambda }^{\dagger }\right)\hat{\lambda }_{q} e^{i\vec{q} \cdot \vec{R}_{i}^{0}}\\
			   & =V^{0} -\sum _{j}\sum _{k}\sum _{q\lambda } e^{i\vec{k} \cdot \vec{r}_{j}}\sum _{L} \delta (\vec{k} -\vec{q} +\vec{L}) \ ( i\vec{k}) V_{ei} (\vec{k} )\frac{1}{\sqrt{2MN\omega _{q\lambda }}}\left( b_{q\lambda } +b_{-q\lambda }^{\dagger }\right)\hat{\lambda }_{q}\\
			   & =V^{0} -\sum _{j}\sum _{L}\sum _{q\lambda }\frac{1}{\sqrt{2MN\omega _{q\lambda }}} e^{i(\vec{q} +\vec{L}) \cdot \vec{r}_{j}} i(\vec{q} +\vec{L}) V_{ei}(\vec{q} +\vec{L})\left( b_{q\lambda } +b_{-q\lambda }^{\dagger }\right)\hat{\lambda }_{q}
			  \end{aligned}
			  \end{equation*}
		- Next we shall consider the summation over $j$.
		  collapsed:: true
			- Trick. 
			  \begin{gather*}
			  \begin{aligned}
			  \sum _{j} e^{i\vec{p} \cdot \vec{r}_{j}} & =\sum _{j}\int d\vec{r} \delta (\vec{r} -\vec{r}_{j}) e^{i\vec{p} \cdot \overrightarrow{r_{j}}}\\
			   & =\sum _{j}\int d\vec{r} \delta (\vec{r} -\vec{r}_{j}) e^{i\vec{p} \cdot \vec{r}}\\
			   & =\int d\vec{r} e^{i\vec{p} \cdot \vec{r}}\sum _{j} \delta \left(\vec{r} -\overrightarrow{r_{j}}\right)\\
			   & =\int d\vec{r} e^{i\vec{p} \cdot \vec{r}} \ \hat{n}( r) :=\hat{\rho }_{p} \ \text{Cautious!}\\
			   & =\int d\vec{r} e^{i\vec{p} \cdot \vec{r}} \psi ^{\dagger }( r) \psi ( r)\\
			   & =\sum _{k^{\prime } k}\int d\vec{r} c_{k^{\prime }}^{\dagger } e^{-i\vec{k} '\cdot \vec{r}} c_{k} e^{i\vec{k} \cdot \vec{r}} e^{i\vec{p} \cdot \vec{r}}\\
			   & =\sum _{kk^{\prime }} c_{k^{\prime }}^{\dagger } c_{k}\int d\vec{r} e^{-i(\overrightarrow{k'} -\vec{k} -\vec{p} )\cdot \vec{r}}\\
			   & =\sum _{k} c_{k+p}^{\dagger } c_{k}
			  \end{aligned}\\
			  \end{gather*}
			  which directly obtains a second-quantized form.
		- Plug all above in, we obtain
		  \begin{equation*}
		  \begin{aligned}
		  H_{ei} & =V^{0} -\sum _{j}\sum _{L}\sum _{q\lambda }\frac{i(\vec{q} +\vec{L})}{\sqrt{2MN\omega _{q\lambda }}} e^{i(\vec{q} +\vec{L}) \cdot \vec{r}_{j}} V_{ei}(\vec{q} +\vec{L})\left( b_{q\lambda } +b_{-q\lambda }^{\dagger }\right)\hat{\lambda }_{q}\\
		   & =V^{0} -\sum _{k}\sum _{L}\sum _{q\lambda }\frac{i(\vec{q} +\vec{L})}{\sqrt{2MN\omega _{q\lambda }}} c_{k+q+L}^{\dagger } c_{k} V_{ei}(\vec{q} +\vec{L})\left( b_{q\lambda } +b_{-q\lambda }^{\dagger }\right)\hat{\lambda }_{q}
		  \end{aligned}
		  \end{equation*}
		- Define
		  collapsed:: true
		  \begin{equation*}
		  M_{qL\lambda } =-\frac{i(\vec{q} +\vec{L})}{\sqrt{2M\omega _{q\lambda }}}\hat{\lambda }_{q} V_{ei}(\vec{q} +\vec{L})
		  \end{equation*}
		  We obtain
		  \begin{equation*}
		  \begin{aligned}
		  H_{ei} & =V^{0} +\frac{1}{N}\sum _{k}\sum _{L}\sum _{q\lambda } M_{qL\lambda } c_{k+q+L}^{\dagger } c_{k}\left( b_{q\lambda } +b_{-q\lambda }^{\dagger }\right)
		  \end{aligned}
		  \end{equation*}
			- Note that $c_{k+q+L}^{\dagger } c_{k}\left( b_{q\lambda } +b_{-q\lambda }^{\dagger }\right)$ corresponds to a scattering vertex, where an income electron scatters to obtain a momentum of $q+L$, while a phonon might be created or annihilated. (on lattices momenta are modulo $L$).
	- ## Effective Electron-Electron Interaction
	  id:: 6454f1b7-ff0b-480d-8fa3-7795a4bcbc51
	  collapsed:: true
		- Motivation
		  collapsed:: true
			- We'd like to integrating out the d.o.f. of phonons and obtain the effect on electrons.
			- For example, the phonon-intermediated interaction accounts for the formation of Cooper pairs.
		- Setup
		  collapsed:: true
			- Here we ignore inverse lattice vectors and polarizations for convenience.
			- The intermediate states have a phonon with momentum $\pm q$.
			  collapsed:: true
				- Note that the intermediate state is **not unique**!
				  We can emit a phonon from $k'$ to $k$ with momentum $q$, or from $k$ to $k'$ with $-q$.
			- The initial state has two electrons with momentum $k,k'$.
			  The final state has two electrons with momentum $k+q,k'-q$.
		-
		- The idea is to invoke ((64239f9f-7660-4553-ab22-80685caf6f6c)) to obtain the effective Hamiltonian.
		- There can be two processes:
		  collapsed:: true
			- ![A.png](../assets/A_1681528965917_0.png)
			  collapsed:: true
				- \begin{aligned}
				  \left< k+q,k'-q\left| H^{(2)}\right| kk^{\prime }\right> _{A} & =\frac{1}{N} M_{-q} M_{q}\\
				   & \frac{1}{2}\left(\frac{1}{\varepsilon _{k} -\varepsilon _{k+q} -\omega _{q}} +\frac{1}{\varepsilon _{k-q} -\varepsilon _{k'} -\omega _{q}}\right)
				  \end{aligned}
				- Here
				  $$W=\frac{1}{N}\sum _{k}\sum _{p} M_{p} c_{k+p}^{\dagger } c_{k}\left( b_{p} +b_{-p}^{\dagger }\right)$$
				- $$E_\alpha=\varepsilon_k+\varepsilon_{k'},E_n=\varepsilon_{k+q}+\varepsilon_{k'}+\omega_{-q}=\varepsilon_{k+q}+\varepsilon_{k'}+\omega_{q}$$
			- ![B.png](../assets/B_1681528972374_0.png)
			  collapsed:: true
				- collapsed:: true
				  \begin{aligned}
				  \left< k+q,k'-q\left| H^{(2)}\right| kk^{\prime }\right> _{B} & =\frac{1}{N} M_{q} M_{-q}\\
				   & \frac{1}{2}\left(\frac{1}{\varepsilon _{k'} -\varepsilon _{k'-q} -\omega _{q}} +\frac{1}{\varepsilon _{k+q} -\varepsilon _{k} -\omega _{q}}\right)
				  \end{aligned}
					-
		- Collecting all those above, we obtain
		  $$\begin{aligned}
		  H^{(2)} & =\frac{1}{2}\sum _{kk^{\prime } q}\frac{1}{N}| M_{q}| ^{2} c_{k'+q}^{\dagger } c_{k^{\prime } -q}^{\dagger } c_{k^{\prime }} c_{k}\\
		   & \left(\frac{1}{\epsilon _{k} -\epsilon _{k+q} -\omega _{q}} +\frac{1}{\epsilon _{k+q} -\epsilon _{k} -\omega _{q}}\right)\\
		   & =\frac{1}{N}\sum _{kk^{\prime } q}| M_{q}| ^{2}\frac{-\omega _{q}}{\omega _{q}^{2} -( \epsilon _{k} -\epsilon _{k+q})^{2}} c_{k'+q}^{\dagger } c_{k^{\prime } -q}^{\dagger } c_{k^{\prime }} c_{k}
		  \end{aligned}$$
-
- # [[Localization]]
  collapsed:: true
	- Summary
	  collapsed:: true
		- Two limits to be examined frequently: metallic and localized.
	- ## Model and Picture
	  collapsed:: true
		- Model: ((64238eab-5e73-4970-9129-9cbcc7e974fb)) with impurities
		  collapsed:: true
			- Two limits
		- Self-averaging Assumption
	- ## Weak Localization
	  collapsed:: true
		- What's weak localization?
		  collapsed:: true
			- Low density of disorder
		- Characteristic scale
		  collapsed:: true
			- Def
			- $\gamma \ll 1$: The classical limits holds!
		- To show that something uncommon is present, we calculate the first-order quantum correction to the conductance and obtain an unphysical result.
		  collapsed:: true
			- Compare classical and quantum transition probability
			  collapsed:: true
				- Classical: Sum up probabilities.
				  $$P_{a \to b}=\sum_i P^i_{a \to b}$$
				- Quantum: Sum up amplitudes.
				  $$P_{a \to b}=|\sum_i A_i|^2$$
				- #+BEGIN_NOTE
				  Usually the cross-terms cancel and the quantum picture goes back to the classical picture.
				  However, the cross terms sometimes play a huge role, which we're interested in here.
				  #+END_NOTE
			- Situation with large quantum corrections
			  collapsed:: true
				- The particle traces a loop in the space of states, i.e. the probability is $P_{a \to a}$
				  collapsed:: true
					- The point is that the path can be **reversed**, then TRS comes into play.
				- The system has time-reversal symmetry
				- Here the quantum probability 
				  $$|A_i+A_{\bar i}|=4|A_i|^2=4P_i$$
				  which is significantly different from the classical one.
			- *Detailed calculation is omitted here. Could refer to Philip Phillips or the handwritten notes.
			- ### Conclusion
			  collapsed:: true
				- The perturbative calculation of the conductance **diverges** when $T \to 0$ and $d=1,2$, which is a hint of localization.
	- ## Thouless Number and [[RG]]
	  collapsed:: true
		- Thouless Number
		  collapsed:: true
			- Def. 
			  collapsed:: true
			  $$g(L):=\frac{2\hbar}{e^2} G(L) \equiv \frac{2\hbar}{e^2} \frac 1 R$$
				- Intuitively, a dimensionless 'conductance'!
				- Generally we want a quantity independent of the system size (like $\sigma$).
				  But here $g(L)$, depending on the size $L$, turns out to be more convenient in RG, which concerns **how the properties change with the system size**.
			- It can be related to a microscopic definition $\frac{\Delta E}{dE/dN}$, which can be argued from the limits of metals and localized states.
		- RG method #card
		  collapsed:: true
			- *Reminder card. No need to recall the details; just appreciate the thought.*
			- Quantity to be concerned:
			  collapsed:: true
			  $$\beta(\ln g):=\lim_{L \to \infty} \frac {d \ln g(L)}{d \ln L}$$
				- This is the **relevance** of $g(L)$.
				  If $\beta > 1$ the system would flow to a conductor (metal-like); if $\beta < 1$ it flows to an insulator (localization-like)
			- Two limits
			  collapsed:: true
				- Metallic
				  collapsed:: true
					- $\sigma \to \sigma_0$, $g(L) \sim \sigma_0 L^{d-2}$
					- $\beta \to d-2$
				- Localized
				  collapsed:: true
					- $g \sim e^{-L / \xi}$ (corresponding to the decay of the wavefunction)
					- $\beta \sim -L/ \xi \to -\infty$
			- Assumption
			  collapsed:: true
				- $\beta(\ln g)$ is monotone in $\ln g$
				  collapsed:: true
					- Mr. Qi gave a diagram:
					  ![image.png](../assets/image_1682215160056_0.png){:height 274, :width 335}
					- This is still a bit problematic for me.
					  background-color:: red
					  collapsed:: true
						- $\ln g$ is a **function** of $L$, not a scalar. So is $\beta$ a functional?
						- Then what does 'monotone' mean? We could say 'a function is monotone in a variable', but what is 'a functional is monotone in a function'?
						- $\ln g$ in the diagram should actually mean 'the asymptotic behavior of $\ln g$, or 'how close a system is to a metal'.
			- Conclusion
			  collapsed:: true
				- When $d=3$: $\beta=1$ when $\ln g \to \infty$. So there is a critical point of localization.
				  collapsed:: true
					- The parameter of criticality is 'how metallic it is'.
				- When $d=1,2$: $\beta$ always smaller than zero, thus always localized?
				  collapsed:: true
					- Actually this is not the case; we haven't seen localization in 1D or 2D electron systems.
					  collapsed:: true
						- Mr. Qi said this is due to interaction and decoherence, but I'm suspicious.
						- I think it is more likely that the behavior of $\beta$ cannot be described by a single parameter (such as $\ln g$).
				-
				-
- # [[Quantum Phase Transition]]
-