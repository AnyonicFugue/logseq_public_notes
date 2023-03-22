type:: [[Course]]

-
- ![2012_Phillips_Advanced Solid State Physics.pdf](file://zotero_link/Physics/Courses/Solid State/2012_Phillips_Advanced Solid State Physics.pdf)
- # Problem-Solving Tricks
	- Diagonalizing tight-binding model
		- Perform a FT to the momentum space
			- Note that the momenta is a continuum, not discreet.
			- Normalization can be determined by taking $k=0$.
		-
- # Slater Determinant
  collapsed:: true
	- Summary #card
		- We want to calculate the wavefunction of a certain fermionic state, say $\prod_{\lambda_\alpha<0} c_\alpha^{\dag}|0\rangle$
		- $$
		  \begin{aligned}
		  & \left\langle\vec{r}_1, \cdots, \vec{r}_N \mid G S\right\rangle=\left\langle 0\left|\hat\psi\left(\vec{r}_1\right) \cdots \hat{\psi}\left(\vec{r}_N\right) \prod_{\lambda_\alpha<0} c_\alpha^{\dag}\right| 0\right\rangle \\
		  = & \sum\langle 0| c_{\alpha_1} \phi_{\alpha_1}\left(\vec{r}_1\right) \cdots c_{\alpha_N} \phi_{\alpha_N}\left(\vec{r}_N\right) \prod_{\lambda_\alpha<0}c_\alpha^\dag|0\rangle
		  \end{aligned}
		  $$
			- $\langle 0|\hat\psi\left(\vec{r}_1\right) \cdots \hat{\psi}\left(\vec{r}_N\right)$ contains symmetrization, while the definition of wavefunctions do not.
			  However, since the fermionic state is itself anti-symmetrical, it makes no difference.
			- The second line is expanding the field operators in the $\alpha$ representation.
		- Obviously the result is a sum of different permutations with signs.
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
		- Examples
			- $$\left< a_{\nu }^{\dagger } a_{\lambda }^{\dagger } a_{\beta } a_{\alpha }\right> :=\left< \psi _{0} |a_{\nu }^{\dagger } a_{\lambda }^{\dagger } a_{\beta } a_{\alpha } |\psi _{0}\right> =( \delta _{\nu \alpha } \delta _{\lambda \beta } -\delta _{\nu \beta } \delta _{\lambda \alpha })< \hat{n}_{\alpha }> < \hat{n}_{\beta }> .$$
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
		- Generally $\hat{H}=\sum_{n i, m j}\left\langle n i\left|\hat{h}_1\right| m j\right\rangle \hat{c}_{n i}^{\dagger} \hat{c}_{m j}$
			- Sum of hoppings from $mj$ to $ni$.
		- Tight-binding model: Only adjacent hoppings (electrons are localized).
		- Example
			- Tight-binding on square lattice
				- $$
				  \hat{H}=-t \sum_{\left\langle ij \right\rangle}\left(\hat{c}_i^{\dagger} c_j+c . c .\right)
				  $$
				- By Fourier transformation, we can diagonalize the Hamiltonian and obtain $E_{\vec{k}}=-2 t\left[\cos \left(k_x a\right)+\cos \left(k_y a\right)\right]$.
	- ## Bloch Wavefunction
	  collapsed:: true
		- Bloch theorem
			- $\psi_k(r)=e^{ikr}u_k(r)$ in a periodic potential.
		- Notation
			- $$
			  \psi_{n \vec{k}}(\vec{r})=e^{i \vec{k} \cdot \vec{r}} u_{n \vec{k}}(\vec{r})
			  $$
				- The n^th level of Bloch wavevector $k$
			- Normalization
				- $$
				  \left\langle\psi_{n_1 k_1} \mid \psi_{n_2 k_2}\right\rangle=\frac{1}{V} \delta_{n_1 n_2} \delta^3\left(\vec{k}_1-\vec{k}_2\right)
				  $$
				- Note: $\frac{1}{V}$ is regarded to cancel $\delta^3(0)$.
		-
	- ## Wannier Wavefunction
	  collapsed:: true
		- Idea
			- Apply Fourier transformation to the Bloch wavevector.
		- Def #card
			- $$
			  W_{n i}(\vec{r}):=\frac{1}{\sqrt{N}} \cdot \frac{1}{\sqrt{N}} \sum_k \psi_{n k}(\vec{r}) e^{-i \vec{k} \cdot \vec{r}_i}
			  $$
			- $i=(i_1,i_2,i_3)$ is a tuple of integer, $r_i=i_1 \vec{a}_1+i_2 \vec{a}_2+i_3 \vec{a}_3$ is a lattice vector.
			- The extra $\frac 1 {\sqrt N}$ prefactor is to cancel the effect of system size.
		- Properties
			- The wavefunctions only depend on $r-r_i$, that is, $W_{n i}(\vec{r})=W_n\left(\vec{r}-\vec{r}_i\right)$
				- Since there's a factor $e^{ikr}$ in $\psi_k(r)$.
				- Moreover, $u_k(r)$ is periodical on the lattice vectors.
		- Fock operators
			- $$
			  \hat{c}_{n i}:=\frac{1}{\sqrt{V_0}} \int d^3 \vec{r} \hat{\psi}(\vec{r}) W_{n i}^*(\vec{r})
			  $$
			- Obviously they're the Fourier transform of the Block Fock operators.
- # [[Fermi Liquid]]
  collapsed:: true
	- Assumptions of Landau Theory of Fermi Liquids #card
		- There is still a fermi surface of some shape
		- There are quasiparticle excitations near the fermi surface, which might decay.
		- Energy functional
			- $$
			  \delta E=\sum_{k \sigma} \varepsilon_k^0 \delta n_0(k)+\frac{1}{2 v} \sum_{k_1 k_2 \sigma_1 \sigma_2} f_{\sigma_1, \sigma_2}\left(k_1, k_2\right) \delta n_{\sigma_1}\left(\vec{k}_1\right) \delta n_{\sigma_2}\left(\vec{k}_2\right)
			  $$
			- The first term is 1-body energy.
				- $\varepsilon_k^0=\frac{k_f}{m^*}\left(k-k_F\right)$, where $m*$ is the ^^effective mass^^.
			- The second term is 2-body part.
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
		- $$\frac{1}{\tau } \varpropto \Gamma \varpropto |u|^{2}\int d^{3}\vec{p}_{1} d^{3}\vec{p}_{2}F(p_1,p_2) 1-f( \varepsilon _{p_{1}})] f( \varepsilon _{p_{2}})[ 1-f( \varepsilon _{p-p_{1} +p_{2}})] \delta (\Sigma\varepsilon )$$
			- $f$ is the occupation number. $F$ is the cross section between $p_1$ and $p_2$.
		- Obviously the volume of the phase space is proportional to $\epsilon^2$.
	- Calculate physical quantities
		- Heat capacity at low temperatures #card
		  collapsed:: true
			- First calculate the energy of a certain configuration. The heat capacity would be known once the state density is known.
				- $$\begin{aligned}
				  \delta E^{(2)} & =\frac{1}{2V}\sum _{\theta _{1} \theta _{2} \sigma _{1} \sigma _{2}} f_{\sigma _{1} \sigma _{2}( \theta _{1} ,\theta _{2})}\sum _{| \vec{k}_{1}| | \vec{k}_{2}| } \delta n_{\sigma _{1}}(\vec{k}_{1}) \delta n_{\sigma _{2}}(\vec{k}_{2})\\
				   & =\frac{1}{2V}\sum _{\theta _{1} \theta _{2} \sigma _{1} \sigma _{2}} f_{\sigma _{1} \sigma _{2}}( \theta _{1} ,\theta _{2})\left[\sum _{| \vec{k}_{1}| } \delta n_{\sigma _{1}}(\vec{k}_{1})\right]\left[\sum _{| \vec{k}_{2}| } \delta n_{\sigma _{2}}(\vec{k}_{2})\right]
				  \end{aligned}$$
					- Approx: At low temperature $k_1,k_2$ would be close to the fermi surface, thus $f$ only depends on the angles, not the norms.
				- Therefore the 2-body part is zero, only the 1-body part remains.
				- The heat capacity can be calculated like free fermions (by inserting the effective mass).
				  background-color:: yellow
			- Experimentalists often use this method to obtain the effective mass.
		- Susceptibility #card
		  card-last-interval:: 27.15
		  card-repeats:: 1
		  card-ease-factor:: 2.6
		  card-next-schedule:: 2023-04-16T04:32:04.890Z
		  card-last-reviewed:: 2023-03-20T01:32:04.890Z
		  card-last-score:: 5
			- Idea
				- First obtain the dependence of $E_0$ on $m$.
				- Since $E=E_0-m\cdot h$, m would be obtained by minimizing the total energy.
					- $\frac{\partial E}{\partial m}=m(h) \cdot \frac{\partial^2 E}{\partial m^2} {=} h$.
				- $\chi$ could be obtained by $m=h\cdot \chi$.
					- $\chi=\left(\frac{\partial^2 E}{\partial m^2}\right)^{-1}$
			- With external field, $N_{\uparrow } \neq N_{\downarrow } ,\ \ N_{\uparrow } +N_{\downarrow } =N$
			- Suppose the fermi surface shifts from the original one by $\delta_k$
				- $$M=\mu_B \cdot\left(\delta N_{\uparrow}-\delta N_\downarrow\right) \Rightarrow \delta k_F=\frac{\lambda^2 M}{\mu_B k_F^2 V}$$
				- Take $V=1$ for simplicity.
			- Obviously the energy shift $\delta E \sim \delta k_F^2$
				- $\delta E_1$ can be calculated like free fermions, just inserting the effective mass.
				- $\delta E^{(2)}=\frac{1}{2 V} \Sigma f_{\sigma_1 \sigma_2}\left(k_1, k_2\right) \delta n_{k_1 \sigma_1} \delta n_{k_2 \sigma_2}$
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
			- ((640be051-94a7-40d3-bcc0-581ee03f5cdb)) $G_\sigma\left(\mathbf{r}, t ; \mathbf{r}^{\prime}, t^{\prime}\right):=-\mathrm{i} T\left\langle\psi_\sigma(\mathbf{r}, t) \psi_\sigma^{\dagger}\left(\mathbf{r}^{\prime}, t^{\prime}\right)\right\rangle$
				- T is the time ordering, where 
				  $$
				  T\left(a\left(t_1\right) b\left(t_2\right)\right)= \begin{cases}a\left(t_1\right) b\left(t_2\right), & t_1>t_2, \\ (-1)^P b\left(t_2\right) a\left(t_1\right), & t_2>t_1,\end{cases}
				  $$
				- Don't forget the minus for fermions!
			- Retarded
				- $G_\sigma^{\mathrm{R}}\left(\mathbf{r}, t ; \mathbf{r}^{\prime}, t^{\prime}\right)=-\mathrm{i} \theta\left(t-t^{\prime}\right)\left\langle\left\{\psi_\sigma(\mathbf{r}, t), \psi_\sigma^{\dagger}\left(\mathbf{r}^{\prime}, t^{\prime}\right)\right\}\right\rangle$
				- $x_{B A}^{ret}\left(t, t^{\prime}\right)=\frac{i}{\hbar} \theta\left(t, t^{\prime}\right)\left\langle\left[\hat{B}(t), \hat{A}\left(t^{\prime}\right)\right]\right\rangle$
					- This follows ((6410762b-de4a-479c-961f-baa5532f6a5d)).
				- Only retarded (from the earlier time $t'$ to the later time $t$) part.
			- Advanced
				- $G_\sigma^{\mathrm{A}}\left(\mathbf{r}, t ; \mathbf{r}^{\prime}, t^{\prime}\right)=\mathrm{i} \theta\left(t^{\prime}-t\right)\left\langle\left\{\psi_\sigma(\mathbf{r}, t), \psi_\sigma^{\dagger}\left(\mathbf{r}^{\prime}, t^{\prime}\right)\right\}\right\rangle$
				- Only advanced (from the later time $t'$ to the earlier time $t$) part.
		- Correlation function
		- Spectral function
			- ((640be0e1-63f2-426b-96be-b5b698e93cdb)) $A_\sigma(\omega, \mathbf{p})=-\frac{1}{\pi} \operatorname{Im} G_\sigma^{\mathrm{R}}(\omega, \mathbf{p})$
				- Quite analogous to the ((6401b89c-e517-4e8f-ad4e-f98d5b166921))
			-
	- ## Fermionic Green Function
		- Def
			- $$G_{\sigma_1 \sigma_2}^R\left(r_1, t_1; r_2, t_2\right):=-\frac{i}{\hbar} \theta\left(t-t^{\prime}\right)\left\langle\left\{\psi_{\sigma_1}\left(r_1, t_1\right), \psi_{\sigma_2}^{\dagger}\left(r_2, t_2\right)\right\}\right\rangle$$
				- Always use anti-commutators for fermions.
			- $$
			  \tilde{G}^R(\vec{k}, \omega):=\int dt e^{-i\omega t}\int d^3 \vec{r}\ e^{-i \vec{k} \cdot \vec{r}}\ G^R(\vec{r}, t) 
			  $$
			- $A(k, \omega):=-\frac{1}{\pi} \operatorname{Im} G^R(k, \omega)$
				- Exercise. $A(\vec{k}, \omega) {=} \frac{1}{2 \pi} \int d t \ e^{i \omega t}\left\langle\left\{c_k(t) c_k^{\dag}(0)\right\}\right\rangle$ #card
					- $A=(G^R-\overline{G^R})/(2i)$, which completes the integral to the whole real axis.
				- Exercise. 
				  $$G^R(\vec{k}, \omega)=\int d \omega^{\prime} \frac{A\left(k, \omega^{\prime}\right)}{\omega-\omega^{\prime}+i \varepsilon}
				  $$ #card
					- Prop. 
					  $$\begin{aligned} & \int_{-\infty}^{\infty} d \omega^{\prime} f\left(\omega^{\prime}\right)\left\{P \frac{1}{\omega^{\prime}-\omega}+i \pi \delta\left(\omega^{\prime}-\omega\right)\right\} \\ & =\int_{-\infty}^{\infty} d \omega^{\prime} f\left(\omega^{\prime}\right) \frac{1}{\omega^{\prime}-\omega-i \epsilon}\end{aligned}$$
						- The delta function adds back the imaginary part.
					- Invoke ((6401b89c-a4af-4f0c-b59f-d44a3c164ff6)): $\chi_1(\omega)=\frac{1}{\pi} \mathcal{P} \int_{-\infty}^{\infty} \frac{\chi_2\left(\omega^{\prime}\right)}{\omega^{\prime}-\omega} d \omega^{\prime}$
						- Note that there is an extra minus in the definition of $A$, thus the denominator of the integrand is also minused.
		- Exercise. $\tilde{G}^R(\vec{k} , t):=\int d^3 \vec{r} \ G^R(\vec{r}, t) e^{-i \vec{k} \cdot \vec{r}}$ is equal to $-\frac{i}{\hbar} \theta(t)\left\langle\left\{c_k(t), \hat{c}_k^{\dagger}(0)\right\}\right\rangle$ #card
			- That is, FT of the Green function is equal to the Green function of the FT representation.
		- Example. Free fermions
			- Calculate 
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
				- Quite interesting. The spectral function, defined as the full correlation function, is the imaginary part of the Green function.
- # Linear Response
  collapsed:: true
	- Defs and Setup
		- Linear response function $\chi(t,t')$ #card
			- $\hat H=\hat H_0-h(t)\hat A$
			- $\langle\hat{B}\rangle(t)=y(t)$ satisfies $y(t)=\int_{-\infty}^t d t^{\prime} \chi\left(t, t^{\prime}\right) h\left(t^{\prime}\right)$
		- Correlation
			- $S_{B A}\left(t, t^{\prime}\right):=\left\langle\hat{B}(t) \hat{A}\left(t^{\prime}\right)\right\rangle$
	- Introduce [[Interaction Picture]]
	  collapsed:: true
		- Leave the background part on the observable and the perturbation part to the density matrix (state)
		- Basics
			- $$\begin{aligned}
			  \hat{O}_{I} (t) & :=e^{iH_{0} t}\hat{O}_{S} (t)e^{-iH_{0} t}\\
			  \frac{d}{dt}\hat{O}_{I} & =\frac{i}{\hbar }[\hat{H}_{0} ,\hat{O}_{I}] +e^{iH_{0} t}\frac{d\hat{O}_{s}}{dt} e^{-iH_{0} t}\\
			   & 
			  \end{aligned}$$
			- $$
			  \frac{d \rho_I}{d t}=\frac{i}{\hbar} h(t)\left[\hat{A}_I, \hat{\rho}_I\right]
			  $$
		- Approximation
			- $h(t) \ll 1 . \Rightarrow \rho_I$ varies very slowly!
			- Thus we may approximate $\left[\hat{A}_1, \hat{P}_I(t)\right]$ by $\left[\hat{A}_1, \hat{P}_I(0)\right]$
				- $$\hat{\rho }_{I} (t)=\hat{\rho }_{0} +\int _{-\infty }^{t} dt^{\prime }\frac{i}{\hbar } h\left( t^{\prime }\right)\left[\hat{A}_{I}\left( t^{\prime }\right) ,\hat{\rho }_{0}\right]$$
			- $$y(t)=y(0)+\int _{-\infty }^{t} dt^{\prime }\frac{i}{\hbar } h\left( t^{\prime }\right)\operatorname{tr}\left\{\hat{B}_{I} (t)\left[\hat{A}_{I}\left( t^{\prime }\right) ,\hat{\rho }_{0}\right]\right\}$$
				- We may apply cyclic permutation to the expression inside the trace to obtain 
				  $y(t)=y(0)+\int_{-\infty}^{t^{\prime}} d t^{\prime} h\left(t^{\prime}\right) \ \frac{i}{\hbar}\left\langle\left[\hat{B}_I(t), \hat{A}_I\left(t^{\prime}\right)\right]\right\rangle_{\rho_0}$
				-
		- Conclusion
			- The kernel is $\chi(t,t')= \frac{i}{\hbar}\left\langle\left[\hat{B}_I(t), \hat{A}_I\left(t^{\prime}\right)\right]\right\rangle_{\rho_0}$ #card
			  id:: 6410762b-de4a-479c-961f-baa5532f6a5d
				- Interaction picture to separate $H_0$ and $A$
				- Slow-varying approximation
				- Cyclic permutation
	- {{embed ((6401b89c-e517-4e8f-ad4e-f98d5b166921))}}
- # Thomas-Fermi Screening
	- ## Idea
		- In a Fermi liquid, some positive external charge would attract electrons to gather near it, thus weakens the external field.
			- The actual field is solved by consistency equations.
		- This can be generalized to the case of some dynamical external field.
	- ## Setup
		- External field $V_{ext}(r,t)$, effective field $V_{\text {eff }}=V_{\text {ext }}+\delta V$
			- For an external charge it is $\operatorname{V_{ext}}(\vec{r})=-e \frac{Q}{r}$
		- $\delta n(\vec{r}):=n(\vec{r})-n_0(\vec{r})$
	- RPA Approximation #card
	  id:: 64118d95-90c5-42ef-afcf-2df672505b13
		- 1. The behavior is similar to free fermi gas
		  2. The effect on number density is local
	- ## Static
		- The final result is 
		  $$
		  \tilde{V}_{\text {eff }}(\vec{k})=-\frac{4 \pi Q e}{k^2+4 \pi \varepsilon^2 N_0}
		  $$ #card
			- Use ((64118d95-90c5-42ef-afcf-2df672505b13)),
			  $$
			  n_0=\sum_{k \sigma} \frac{1}{1+e^{\left.\beta ( \varepsilon_k+\mu\right)}} \quad n(\vec{r})=\sum_{k \sigma} \frac{1}{1+e^{\beta\left[\varepsilon_k(\vec{r})-\mu\right]}}
			  $$
			- Therefore 
			  $$\begin{aligned}
			  \delta n(r ) & =\frac{\partial n}{\partial V_{\text{eff }} (r)}\operatorname{V_{eff}} (r)=-\frac{\partial n}{\partial \mu } V_{\text{eff}} (r)\\
			   & =-N(0)\operatorname{Veff} (r)
			  \end{aligned}$$
				- N0 is the number density at the fermi surface
			- Plug in $-\Delta \phi=4 \pi[Q \delta(\vec{r})-e \cdot \delta n(\vec{r})]$ and Fourier transformation we could obtain the desired result.
			-
			- Exercise. Obtain the Yukawa potential from the result.
	- ## Dynamic
		- Setup
			- $$
			  \hat{H}=\hat{H}_0+\hat{H}^{\prime} . \quad \hat{H}^{\prime}=\int d \vec{r} \hat{n}(\vec{r}, t) \cdot V_{\text {ext }}(\vec{r}, t)
			  $$
			- $$\langle \delta \hat{n} (r,t)\rangle =\int _{-\infty }^{t} dt^{\prime } \chi ^{\text{ret }}\left( r-r',t-t^{\prime }\right) V_{\text{ext }} (r' ,t)$$
		- Prop. 
		  $$
		  \langle \delta \hat{n} (\vec{k} ,\omega )\rangle =x_{0}^{\text{ret }} (\vec{k} ,\omega )V_{\text{ext }} (\vec{k} ,\omega )
		  $$ #card
			- 动量空间卷积变乘积
		-
		-