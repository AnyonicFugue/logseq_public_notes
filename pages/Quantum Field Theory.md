alias:: [[QFT]]

-
- # Setup and Notations
  collapsed:: true
	- $|\Omega\rangle$ is the interactive vacuum, while $|0\rangle$ is the free vacuum.
	- $G\left(x_1, \cdots, x_n\right)=\left\langle\Omega\left|T\left\{\phi\left(x_1\right) \cdots \phi\left(x_n\right)\right\}\right| \Omega\right\rangle$
	-
	- ## Assumptions about the Hilbert Space #card
	  collapsed:: true
	  card-last-interval:: 31.26
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2023-05-26T07:00:49.798Z
	  card-last-reviewed:: 2023-04-25T01:00:49.799Z
	  card-last-score:: 5
		- #+BEGIN_NOTE
		  Not a rigorous structure, but seems natural in perturbation theories.
		  #+END_NOTE
		- A unique ground state $|\Omega\rangle$ with momentum $q_{\nu a c}^\mu=0$
			- Note we don't consider GSD or spontaneous symmetry breaking here.
		- A continuum of single-particle states $|p\rangle$ eigen to the Hamiltonian, with $p^2=m^2\geq 0$
		  id:: 63fc166f-9a06-42b7-a7e3-947eff93ae12
			- 'Continuum' means that any 3-momenta is allowed.
		- The spectra is a continuum for $p^2 \gtrsim 4 m^2$
			- These correspond to multi-particle states. Interaction between them leads to the continuum.
			- However the spectrum is **not** strictly greater than $4m^2$, since attracting interaction lowers the energy.
		-
		- Other ones
			- A theory is an irreducible representation of the operator algebra. Equivalently, we can always relate two states in the Hilbert space by some operator.
			  id:: 63fc4f1b-f3c8-4e99-a31f-add4fe16f8ec
				- For a single theory, we can relates 1-particle states by boosts.
				  id:: 63fc5025-5650-4054-ba3a-0520194bfb13
			- There shall be a basis of states corresponding to the classical field configurations, which would be used in [[Path Integral]].
	- [[Classical Field Theory]]
	  collapsed:: true
		- Noether's theorem #card
		  card-last-interval:: 24
		  card-repeats:: 2
		  card-ease-factor:: 2.7
		  card-next-schedule:: 2023-03-26T14:12:47.860Z
		  card-last-reviewed:: 2023-03-02T14:12:47.861Z
		  card-last-score:: 5
		  id:: 63e86248-d68b-4d57-bed2-c7a0d75b3be7
			- $$\begin{aligned}
			  \partial _{\mu } j^{\mu } (x) & =0,\ \ \text{ for } \ \ j^{\mu } (x)=\frac{\partial \mathcal{L}}{\partial (\partial _{\mu } \phi )}\frac{\delta \phi }{\delta \alpha } -\mathcal{J}^{\mu }
			  \end{aligned}$$
			- Points: EOM, construct full derivative
			-
			- Proof
				- Consider a Lagrangian with sym. $\alpha$
				- L must be inv. under different $\alpha$, up to a 4-divergence $\partial_\mu \mathcal{J}^{\mu }$:
				  $$\begin{aligned}
				  \frac{\delta \mathcal{L}}{\delta \alpha } & =\frac{\partial \mathcal{L}}{\partial \phi }\frac{\delta \phi }{\delta \alpha } +\left(\frac{\partial \mathcal{L}}{\partial (\partial _{\mu } \phi )}\right) \partial _{\mu } (\frac{\delta \phi }{\delta \alpha } )\\
				   & =\partial _{\mu }\left(\frac{\partial \mathcal{L}}{\partial (\partial _{\mu } \phi )}\frac{\delta \phi }{\delta \alpha }\right) +\alpha \left[\frac{\partial \mathcal{L}}{\partial \phi } -\partial _{\mu }\left(\frac{\partial \mathcal{L}}{\partial (\partial _{\mu } \phi )}\right)\right]\frac{\delta \phi }{\delta \alpha }
				  \end{aligned}$$
				- Substitute EOM: We're done.
			- Example
				- [[Energy-momentum Tensor]] 
				  $\mathcal{T}_{\mu \nu}=\sum_{n} \frac{\partial \mathcal{L}}{\partial\left(\partial_{\mu} \phi_{n}\right)} \partial_{\nu} \phi_{n}-g_{\mu \nu} \mathcal{L}$
			- Ref. Peskin, ((63805db9-661f-470f-9403-3ff9ae8aa7dd))
- # Causality and Propagators
  collapsed:: true
	- $\langle 0|[\phi(x), \phi(y)]| 0\rangle=0$ for spacelike separation, which preserves [[Causality]].
		- Use some invariance/symmetry to simplify the problem. ([[Lorentz invariance]] in this case) #Techniques
	-
	- [[Propagator]], or time-ordered product
		- $$\langle 0|\phi(x) \phi(y)| 0\rangle=\int \frac{d^3 p}{(2\pi)^3} \cdot \frac{1}{2 E_p} \cdot e^{-i p(x-y)}:=D(x-y)$$
		- [[Feynman Propagator]]
		  id:: 129a2538-6668-4ae1-a5cc-a7cf58e6122b
			- Def
				- $D_{F}( x_{1} ,x_{2}) =\langle 0| T\{\phi _{0}( x_{1}) \phi _{0}( x_{2})\}| 0\rangle =\int \frac{d^{4} k}{(2\pi )^{4}}\frac{i}{k^{2} -m^{2} +i\varepsilon } e^{ik( x_{1} -x_{2})}$
				- Points: Exponential term from $a_p e^{ipx}$; denominator produces singularities.
			-
			- Core point: $$\frac{e^{-iE_{k} \tau } \theta (\tau )+e^{iE _{k} \tau } \theta (-\tau )}{2E_k}=\lim _{\varepsilon \rightarrow 0}\int _{-\infty }^{\infty }\frac{dp_0}{2\pi}\frac{i }{p_0 ^{2} -E _{k}^{2} +i\varepsilon } e^{-ip_0 \tau }$$ 
			  'Phase multiples Heaviside'
			- Note tha $D_F$ is the [[Green Function]] of KG operator, i.e. 
			  $$\left(\partial^\mu \partial_\mu+m^2\right) D_F(x-y)=-i \delta^4(x-y)$$
		- Dirac Propagator
			- Def
				- $$\begin{aligned}
				  &S_F(x-y)=\int \frac{d^4 p}{(2 \pi)^4} \frac{i(\not p+m)}{p^2-m^2+i \epsilon} e^{-i p \cdot(x-y)}\\
				  &=\left\{\begin{aligned}
				  \langle 0|\psi(x) \bar{\psi}(y)| 0\rangle & \text { for } x^0>y^0 \text { (close contour below) } \\
				  -\langle 0|\bar{\psi}(y) \psi(x)| 0\rangle & \text { for } x^0<y^0 \text { (close contour above) }
				  \end{aligned}\right.\\
				  &\equiv\langle 0|T \psi(x) \bar{\psi}(y)| 0\rangle
				  \end{aligned}$$
			- This is $-(i\gamma^\mu p_\mu+m)D_F(x-y)$.
				- With the 'dirac operator' $i\gamma^\mu p_\mu-m$ acting on it, we obtain $(\square+m^2)D_F(x-y)\cdot \mathbb1_4$.
				- The same idea as obtaining KG eq. from Dirac eq.
			-
			- Exercise. The [[Time-ordered product]] gives the correct propagator
				- Tip: Modify $$\frac{e^{-iE_{k} \tau } \theta (\tau )+e^{iE _{k} \tau } \theta (-\tau )}{2E_k}=\lim _{\varepsilon \rightarrow 0}\int _{-\infty }^{\infty }\frac{dp_0}{2\pi}\frac{i }{p_0 ^{2} -E _{k}^{2} +i\varepsilon } e^{-ip_0 \tau }$$
				- Use Lorentz invariance (or change of integration variables)
			-
			- Take care of the minus sign! (Compare ((129a2538-6668-4ae1-a5cc-a7cf58e6122b)) )
	-
- # Specific Theories
  collapsed:: true
	- [[Klein-Gordon Theory]]
	- [[Yukawa Theory]]
	- [[Quantum Electrodynamics]]
	- [[Proca Theory]]
	-
- # [[Interaction, Feynman diagrams and S-matrix]]
- # [[Renormalization]]
- # [[Path Integral]]