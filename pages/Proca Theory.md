- # Setup
	- Massive spin-1, $\mathcal{L}=-\frac{1}{4} F_{\mu \nu} F^{\mu \nu}+\frac{1}{2} m^2 A_\mu A^\mu$
- # Quantization
	- ## EOM
		- Solving the EL equation, we obtain $m^2 A^\mu- \partial_v\left(\partial^\mu A^v-\partial^v A^\mu\right)=0$.
		- Act $\partial_{\mu}$ on it, we obtain the constraint that $\partial_\mu A^{\mu}=0$.
			- Why is the constraint just all the information? Generally partials would lead to loss of information. #Learning-TODO
		- Thus the EOM becomes 
		  $$(m^2+\partial_\nu \partial^\nu)A^\mu=0$$.
	- ## Quantization
		- Classically 
		  $$A^\mu(x)=\sum_{\lambda=1}^3 \int \frac{d^3 p}{(2 \pi)^3} a_{p\lambda}\varepsilon^\mu(\vec{p}, \lambda) e^{i p \cdot x}$$
		- The corresponding field operator is clearly 
		  $$A_\mu(x)=\int \frac{d^3 p}{(2 \pi)^3} \frac{1}{\sqrt{2 \omega_p}} \sum_{\lambda=1}^3\left[\varepsilon_\mu(p, \lambda) a_{p, \lambda} e^{-i p \cdot x}+\varepsilon_\mu^*(p, \lambda) a_{p, \lambda}^{\dag} e^{i p \cdot x}\right]$$.
			-
			- $p_\mu \varepsilon^\mu$ leads to three independent modes.
		- $\sum_{\lambda=1}^3 \varepsilon_\mu(\beta, \lambda) \varepsilon_\nu^*(\beta, \lambda)=-g_{\mu \nu}+\beta_\mu \beta_\nu / m^2$
			- This can be easily proven in the rest frame, then it holds in all frames by Lorentz invariance.
		-
- # CCR and Causality
	- $\left[A_\mu(x), A_\nu(y)\right]=\left(-g_{\mu \nu}-\frac{\partial_\mu \partial_v}{m^2}\right) \Delta(x-y)$, where $\Delta(x-y)=\int \frac{d^3 p}{(2 \pi)^3 2 \omega_p}\left[e^{-i p \cdot(x-y)}-e^{i p \cdot(x-y)}\right]$
		- Obviously it is zero for spacelike separations. Easy to prove by invoking Lorentz invariance.
	- $\left[A^i(t, \vec{x}), \pi^j(t, \vec{y})\right]=-i \delta^{i j} \delta^{(3)}(\vec{x}-\vec{y})$
- # Spin Operator
  collapsed:: true
	- Spin and Lorentz symmetry #card
		- In principle, spins are conserved currents of the Lorentz symmetry.
		- Moreover, the current naturally decomposes into an orbital part and an internal part, corresponding to orbital angular momentum and spin.
	- Here the field transforms as $A^\mu(x) \longrightarrow \Lambda_\nu^\mu A^\nu\left(\Lambda^{-1} x\right)$, where $\Lambda^\mu_\nu=\frac{i}{2} \Omega_{\rho \sigma}\left(J^{\rho \sigma}\right)^\mu_\nu$
	- Invoke ((63e86248-d68b-4d57-bed2-c7a0d75b3be7))
		- $\frac{\delta A^{\nu} }{\delta \Omega_{\rho \sigma} }$ has two parts.
			- $$\frac{\delta A^v}{\delta\left(\Omega_{\rho \sigma}\right)}=\frac{\delta \Lambda_\mu^v}{\delta\left(\Omega_{\rho \sigma}\right)} \cdot A^\mu+\Lambda_\mu^v \cdot \partial_\alpha A^\mu \cdot \frac{\delta\left(\Lambda^{-1}\right)^\alpha_\beta}{\delta \Omega_{\rho\sigma}} \cdot x^\beta$$
			- Obviously the first part corresponds to spin and the second part corresponds to orbital angular momentum.
		- Thus the spin part is $-F^\mu{ }_\nu \frac{i}{2}(J_{\rho\sigma})^\nu_\alpha A^\alpha$.
	- Spin corresponds to the rotations, i.e. $\rho, \sigma=1,2,3$.
		- Note that it is perfectly legitimate to say the current corresponding to a single generator.
		- Take $\left(J^{\rho \sigma}\right)^{\mu \nu}=i\left(g^{\rho \mu} g^{\sigma \nu}-g^{\sigma \mu} g^{\rho \nu}\right)$, we find
		  $$\left(\mathcal J^\mu\right)_{\rho \sigma}=\frac{1}{2} F^\mu_{\ \nu}\left(g^{\rho v} A^\sigma-g^{\sigma v} A^\rho\right)$$
		- The spin is the conserved charge, $Q^{i j}=\int d^3 x \mathcal J^0=\int d^3 x\left(F^{0 j} A^i-F^{0 i} A^j\right)$
	- Write in the form of 3-vectors, we obtain the conclusion
		- $$
		  \begin{aligned}
		  S^k=\frac{1}{2} \varepsilon^{i j k} Q^{i j} & =\frac{1}{2} \varepsilon^{i j k} \int d^3 x\left(F^{0 j} A^i-F^{0 i} A^j\right) \\
		  & =\frac{1}{2} \int d^3 x\left(-\varepsilon^{i j k} \pi^j A^i+\varepsilon^{i j k} \pi^i A^j\right) \\
		  \vec{S} & =\int d^3 x \ \vec{\pi} \times \vec{A}
		  \end{aligned}
		  $$
	- Notes
		- $a_{p, \lambda|0\rangle}^{+}$ aren't eigenstates of the spin operator.
		- We may go to the helicity basis 
		  $$
		  \left\{\begin{array}{l}
		  a_{p,+}=\frac{1}{\sqrt{2}}\left(a_{p, 1}-i a_{p, 2}\right) \\
		  a_{p,-}=\frac{1}{\sqrt{2}}\left(a_{p, 1}+i a_{p, 2}\right) \\
		  a_{p, 0}=a_{p, 3}
		  \end{array}\right.
		  $$
- # Propagator
	- $$
	  \begin{aligned}
	  D_F^{\mu \nu}(x-y) & =\left\langle 0\left|T\left\{A^\mu(x) A^\nu(y)\right\}\right| 0\right\rangle \\
	  & =\theta\left(x^0-y^0\right)\left(-g^{\mu \nu}-\frac{\partial^\mu \partial^\nu}{m^2}\right) D(x-y)+\theta\left(y^0-x^0\right)\left(-g^{\mu \nu}-\frac{\partial^\mu \partial^\nu}{m^2}\right) D(y-x)
	  \end{aligned}
	  $$
		- Why can we write the propagator in this form? #card
			- $$A_\mu(x)=\int \frac{d^3 p}{(2 \pi)^3} \frac{1}{\sqrt{2 \omega_p}} \sum_{\lambda=1}^3\left[\varepsilon_\mu(p, \lambda) a_{p, \lambda} e^{-i p \cdot x}+\varepsilon_\mu^*(p, \lambda) a_{p, \lambda}^{\dag} e^{i p \cdot x}\right]$$. 
			  The extra term is the sum over polarizations, so we just need to add $-g^{\mu \nu}-\frac{\partial^\mu \partial^\nu}{m^2}$ before every scalar-field quantities.
	- Prop. 
	  $$
	  \begin{aligned}
	  & \theta\left(x^0-y^0\right) \partial_0^2 D(x-y)+\theta\left(y^0-x^0\right) \partial_0^2 D(y-x) \\
	  = & \partial_0^2 D_F(x-y)-\delta^{\prime}\left(x^0-y^0\right)[\phi(x), \phi(y)]-2 \delta\left(x^0-y^0\right) \frac{\partial}{\partial x^0}[\phi(x), \phi(y)]
	  \end{aligned}
	  $$
		-
	-
-