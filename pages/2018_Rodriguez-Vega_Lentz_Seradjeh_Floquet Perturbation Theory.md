type:: paper_reading

-
- ![2018_Rodriguez-Vega_Lentz_Seradjeh_Floquet Perturbation Theory.pdf](file://zotero_link/Research/Floquet/2018_Rodriguez-Vega_Lentz_Seradjeh_Floquet Perturbation Theory.pdf)
- # Notations
	- Floquet states and quasi-stationary states
	  $$
	  \left|\psi_\alpha(t)\right\rangle=e^{-i \epsilon_\alpha t}\left|\phi_\alpha(t)\right\rangle
	  $$
	- Time-dependent Floquet Hamiltonian $\hat{H}(t)-i \frac{\mathrm{d}}{\mathrm{d} t}$
	- $$\begin{aligned} & \hat{U}\left(t, t_0\right)=\hat{\Phi}(t) e^{-i\left(t-t_0\right) \hat{H}_F} \hat{\Phi}\left(t_0\right)^{\dagger} \\ & e^{-i t \hat{H}_F}=\sum_\alpha e^{-i \epsilon_\alpha t}\left|\phi_\alpha(0)\right\rangle\left\langle\phi_\alpha(0)\right| \\ & \hat{\Phi}(t)=\sum_\alpha\left|\phi_\alpha(t)\right\rangle\left\langle\phi_\alpha(0)\right|\end{aligned}$$
		- Floquet Hamiltonian $H_F$
	- collapsed:: true
	  $$
	  \mathscr{F}=\mathscr{H} \otimes \mathscr{I}
	  $$
		- Extended space $\mathscr F$
			- Lifting of a loop 
			  $$
			  \left.\left.\left|\phi_t\right\rangle\right\rangle:=|\phi(t)\rangle \mid t\right)
			  $$
			- Center of a loop
			  $$
			  |\bar{\phi}\rangle\rangle \equiv \int_0^T\left|\phi_t\right\rangle\rangle \frac{\mathrm{d} t}{T}
			  $$
				- A compact way to express a time-dependent state!
		- Hilbert space $\mathscr H$
		- Space of bounded periodic function $\mathscr I$
		  collapsed:: true
			- Two Bases
				- Time basis
				  $$
				  \left.\left(t^{\prime} \mid t\right)=T \delta\left(t-t^{\prime}\right), \quad \int_0^T \mid t)(t \mid \frac{\mathrm{d} t}{T}=\hat{I}\right.
				  $$
				- Fourier basis
				  \begin{aligned}
				  |n)=\int _{0}^{T} e^{-in \Omega t} |t)\frac{\mathrm{d} t}{T} ,\ \ n\in \mathbb{Z}\\
				  (n|m)=\delta _{nm} ,\ \ \sum _{n\in \mathbb{Z}} |n) (n|=\hat{I}
				  \end{aligned}
				- Inverse transformation
				  $$|t)=\sum _{n\in \mathbb{Z}} e^{in \Omega t} |n)$$
		- We denote the states in $\mathscr{H}, \mathscr{I}$, and $\mathscr{F}$ respectively by $|\cdot\rangle, \mid \cdot)$, and $|\cdot\rangle\rangle$ and the operators acting on each respective space as $\hat{O}, \hat{O}$, and $\hat{\hat{O}}$.
			- The Hilbert space is conventional; the extended space is 'double Hilbert'
	- Operators in the spaces
	  collapsed:: true
		- Fourier integral
			- $$
			  \hat{\hat{\mu}}_n=\hat{I} \otimes \int_0^T \mid t) e^{+i n \Omega t}(t \mid \frac{\mathrm{d} t}{T}
			  $$
			- Prop. 
			  $$
			  \left.\hat{\mu}_n|\bar{\phi}\rangle\right\rangle=\int_0^T e^{+i n \Omega t}\left|\phi_t\right\rangle\rangle \frac{\mathrm{d} t}{T} \equiv\left|\phi_n\right\rangle\rangle
			  $$
		- Derivative
			- $$
			  \hat{\hat{Z}}_t=\hat{I} \otimes \sum_{n \in \mathbb{Z}} \mid n) n \Omega(n \mid
			  $$
				- Motivation: The derivative operator in the Fourier space becomes $e^{i\omega t} \mapsto i\omega e^{i\omega t}$
			- Prop.
			  $$
			  \hat{\hat{Z}}_t|\bar{\phi}\rangle\rangle=\int_0^T i \frac{\mathrm{d}|\phi(t)\rangle}{\mathrm{d} t} \mid t) \frac{\mathrm{d} t}{T} \equiv i|\overline{\mathrm{d} \phi / \mathrm{d} t}\rangle\rangle
			  $$
	- The Floquet Schrodinger equation and solutions
		- $$
		  \left(\hat{\hat{H}}-\hat{Z}_t\right)\left|\overline{\phi_\alpha}\rangle\right\rangle=\epsilon_\alpha\left|\overline{\phi_\alpha}\rangle\right\rangle
		  $$
		- Plug in the redundancy of solutions to obtain a **complete** eigenbasis:
		  $$
		  \left(\hat{H}-\hat{Z}_t\right)\left|\phi_{\alpha n}\right\rangle\rangle=\epsilon_{\alpha n}\left|\phi_{\alpha n}\right\rangle\rangle
		  $$
			- $$
			  \epsilon_{\alpha n} \equiv \epsilon_\alpha+n \Omega
			  $$
-