- [[References]]
	- [[2020_Rudner_Lindner_The Floquet Engineer's Handbook]]
		- Formalism and basic theory.
	- ![2019_Oka_Kitamura_Floquet Engineering of Quantum Materials.pdf](file://zotero_link/Research/Floquet/2019_Oka_Kitamura_Floquet Engineering of Quantum Materials.pdf)
- # Questions
	- How is the effective Hamiltonian related to physical behaviors?
		- [Here](((648ff108-034f-4286-b3d4-f6fd2a121c87))) they take the effective Hamiltonian for granted and claim the model to be that of a static Hamiltonian (Haldane model).
		- [Here](((648ff30b-dd82-4f04-9d08-f983307e8d59))) they calculated the linear response (Hall conductance), which seems more physical.
- # Basic Theory
	- ## Setup
	  collapsed:: true
		- The system is periodically driven, with period $T$.
		- Floquet states
		  $$
		  \left|\psi_n(t+T)\right\rangle=e^{-i \varepsilon_n T / \hbar}\left|\psi_n(t)\right\rangle
		  $$
		- Quasi-stationary states
		  $$
		  \left|\psi_n(t)\right\rangle=e^{-i \varepsilon_n t / \hbar}\left|\Phi_n(t)\right\rangle, \quad\left|\Phi_n(t+T)\right\rangle=\left|\Phi_n(t)\right\rangle
		  $$
			- Separate the time-dependence. #Techniques
		- Fourier transformations
			- $$
			  \left|\Phi_n(t)\right\rangle=\sum_m e^{-i m \omega t}\left|\phi_n^{(m)}\right\rangle
			  $$
			- $$
			  H(t)=\sum_m e^{-i m \omega t} H^{(m)}
			  $$
		- The projector
		  $$
		  \mathcal{P}(\omega t)=\operatorname{diag}\left(\cdots, e^{-i m \omega t} \mathbf{1}_{d \times d}, e^{-i(m+1) \omega t} \mathbf{1}_{d \times d} \cdots, \right)
		  $$
			- With the projector we can compactly express the mapping between the extended space and the physical Hilbert space:
			  $$
			  \begin{aligned}
			  \left|\Phi_n(t)\right\rangle & =\mathcal{P}(\omega t) \varphi_n \\
			  & =\sum_m e^{-i m \omega t}\left|\varphi_n^{(m)}\right\rangle
			  \end{aligned}
			  $$
		- Floquet Brillione zone
			- An energy interval $\epsilon_{min} < \epsilon < \epsilon_{min}+\hbar \omega$
			- This is to fix the redundancy.
	- ## Floquet Theorem and Effective Hamiltonian
		- Floquet Theorem. There is an orthonomal basis of 'Floquet states', $\left\{\left|\psi_n(t)\right\rangle\right\}$, which satisfy $\left|\psi_n(t+T)\right\rangle=e^{-i \varepsilon_n T / \hbar}\left|\psi_n(t)\right\rangle$. #card
		  collapsed:: true
		  card-last-interval:: 33.94
		  card-repeats:: 1
		  card-ease-factor:: 2.6
		  card-next-schedule:: 2023-09-12T11:00:31.627Z
		  card-last-reviewed:: 2023-08-09T13:00:31.628Z
		  card-last-score:: 5
			- The parameter $\varepsilon_n$ is the **quasi-energy** of Floquet state $\left|\psi_n(t)\right\rangle$.
			- Proof
				- Consider the evolution operator
				  $$U(T)=\mathcal{T} e^{-\frac{i}{\hbar }\int _{0}^{T} dt^{\prime } H\left( t^{\prime }\right)}$$.
				- It has an orthonormal basis of eigenvectors since it is unitary.
				  Obviously the basis vectors are the desired Floquet states.
		- Proposition. If we change the starting time of a period, the effective Hamiltonian only changes by a unitary transformation (which can be viewed as a basis transformation).
			- $$e^{-i \hat{H}_{\mathrm{F}}\left(\alpha_1\right) T}=\hat{U}^{\dagger}\left(\alpha_2, \alpha_1\right) e^{-i \hat{H}_{\mathrm{F}}\left(\alpha_2\right) T} \hat{U}\left(\alpha_2, \alpha_1\right)$$
			- Therefore the similarity transformation could be absorbed by the exponential:
			  $$
			  \hat{H}_{\mathrm{F}}\left(\alpha_1\right)=\hat{U}^{\dagger}\left(\alpha_2, \alpha_1\right) \hat{H}_{\mathrm{F}}\left(\alpha_2\right) \hat{U}\left(\alpha_2, \alpha_1\right)
			  $$
	- ## Analysis in Fourier space
	  collapsed:: true
		- Theorem. We may solve the Floquet states in the form of an eigenequation
		  card-last-interval:: 31.26
		  card-repeats:: 1
		  card-ease-factor:: 2.6
		  card-next-schedule:: 2023-07-28T06:50:30.667Z
		  card-last-reviewed:: 2023-06-27T00:50:30.667Z
		  card-last-score:: 5
		  $$\mathcal{H}\boldsymbol{\varphi }_{n} =\varepsilon _{n}\boldsymbol{\varphi }_{n}$$
		  where
		  $$\begin{aligned}
		  \mathcal{H} & =\left(\begin{array}{ c c c c }
		  \ddots  & H^{(-1)} & H^{(-2)} & \\
		  H^{(1)} & H_{0} -m\hbar \omega  & H^{(-1)} & H^{(-2)}\\
		  H^{(2)} & H^{(1)} & H_{0} -(m+1)\hbar \omega  & H^{(-1)}\\
		   & H^{(2)} & H^{(1)} & \ddots 
		  \end{array}\right)\\
		  \varphi _{n} & =\left(\begin{array}{ c }
		  \vdots \\
		  \left| \phi _{n}^{(m)}\right> \\
		  \left| \phi _{n}^{(m+1)}\right> \\
		  \vdots 
		  \end{array}\right)
		  \end{aligned}$$ #card
			- Notes
				- Here the vector space is $\mathcal V^\omega=(\mathbb C ^ \omega)^\omega$, where $\mathcal V$ is the original Hilbert space.
					- The 'component' of a vector here is a state $|\phi\rangle \in \mathcal V$.
					- It is indeed a vector space, since vectors can be added and multiplied by scalars.
				- $\mathcal H \in \mathcal L(\mathcal V^\omega)$.
				- Q: It seems that the degrees of freedom has somewhat 'increased'. How to explain the paradox?
				  background-color:: pink
					- A: The d.o.f. has not increased.
					  $\Phi$ has time-dependence, so we're solving for a time-dependent function!
					- Here we simply express the time-dependence by the Fourier coefficients.
			- An intuitive picture: Effective lattice in the Fourier space
				- ((64570780-0ad1-467c-837e-f714c10c257a))
					- $m \hbar \omega$ serves as an 'uniform external electric field'
						- When $\omega = 0$ the eigenstates would become Bloch states.
					- The **driving** becomes **hopping** between sites in the Fourier space.
						- Here the author takes a single harmonic driving, so there's only hopping between adjacent Fourier levels (analogous to the tight-binding model)
			- Proof
				- Start by the Schrodinger equation
				  $$
				  i \hbar \frac{d}{d t}|\psi_n(t)\rangle=H(t)|\psi_n(t)\rangle
				  $$
				- Perform **Fourier transformation** to both $\psi_n$ and $H$, then compare the 'coefficients' for $e^{-imt}$, we can obtain
				  $$
				  \left(\varepsilon_n+m \hbar \omega\right)\left|\phi_n^{(m)}\right\rangle=\sum_{m^{\prime}} H^{\left(m-m^{\prime}\right)}\left|\phi_n^{\left(m^{\prime}\right)}\right\rangle
				  $$
				- It's easy to observe it has the structure of an eigenequation, with $\tilde H_{mn}=H^{(m-n)}$.
		- From this equation we can (in principle) solve for all quasi-energies and Floquet states.
			- It avoids the pain of time-integration by Fourier transformation! #card
			  card-last-interval:: 42
			  card-repeats:: 2
			  card-ease-factor:: 2.7
			  card-next-schedule:: 2023-08-10T01:35:41.776Z
			  card-last-reviewed:: 2023-06-29T01:35:41.777Z
			  card-last-score:: 5
				- Fourier transformation: Calculus of time -> Algebra of momenta
		- Proposition (Normalization of eigenstates). 
		  collapsed:: true
		  $$
		  \sum _{m}\left< \phi _{n}^{(m+k)} |\phi _{n}^{(m )}\right> =\delta _{k0}
		  $$
			- Starting point:
			  $| \psi _{n} (t)\rangle$ is normalized and so is $| \Phi _{n} (t)\rangle$.
			- Write down the orthonormality condition after Fourier transformation:
			  \begin{equation*}
			  \begin{aligned}
			  < \Phi _{n} (t)|\Phi _{n} (t)>  & =\left(\sum _{m_{1}} \langle \phi _{n}^{(m_{1} )} |e^{im_{1} \omega t}\right)\left(\sum _{m_{2}} e^{-im_{2} \omega t}\left| \phi _{n}^{(m_{2} )}\right> \right)\\
			   & =\sum _{m_{1}}\sum _{m_{2}} e^{i( m_{1} -m_{2}) \omega t}\left< \phi _{n}^{(m_{1} )} |\phi _{n}^{(m_{2} )}\right> \\
			   & =\sum _{k} e^{ik\omega t}\sum _{m_{2}}\left< \phi _{n}^{(m_{2} +k)} |\phi _{n}^{(m_{2} )}\right> 
			  \end{aligned}
			  \end{equation*}
			- We know that LHS is $1$ at all time, so only $k=0$ survives in the summation:
			  \begin{equation*}
			  \begin{aligned}
			  \sum _{m}\left< \phi _{n}^{(m+k)} |\phi _{n}^{(m )}\right>  & =\delta _{k0}
			  \end{aligned}
			  \end{equation*}
				-
		- Proposition. (Redundancy of Solutions) The quasi-energies can be arbitrarily shifted by multiples of $\hbar \omega$ without affecting the state $|\psi_n\rangle$.
		  collapsed:: true
			- Note here the quasi-energy is defined in the sense that
			  $$\mathcal{H}\boldsymbol{\varphi }_{n} =\varepsilon _{n}\boldsymbol{\varphi }_{n}$$
			- Proof
				- Start from the equation
				  $$
				  \left(\varepsilon_n+m \hbar \omega\right)\left|\phi_n^{(m)}\right\rangle=\sum_{m^{\prime}} H^{\left(m-m^{\prime}\right)}\left|\phi_n^{\left(m^{\prime}\right)}\right\rangle
				  $$
				- Define $\tilde\phi_n^{(m)}=\phi_n^{(m-k)}$, then perform substitutions $m \to m+k, m' \to m'+k'$, the equation can be rewritten as
				  $$
				  \left(\varepsilon_n+(m+k) \hbar \omega\right)\left|\tilde\phi_n^{(m)}\right\rangle=\sum_{m^{\prime}} H^{\left(m-m^{\prime}\right)}\left|\tilde\phi_n^{\left(m^{\prime}\right)}\right\rangle
				  $$
				  where the shift of the quasi-energy is manifest.
			- Remarks
				- Thus in the extended space, each physical solution is encoded infinite times.
				- The redundancy is **expected** from the definition $$\left|\psi_n(t+T)\right\rangle=e^{-i \varepsilon_n T / \hbar}\left|\psi_n(t)\right\rangle$$. #card
				  card-last-interval:: 31.26
				  card-repeats:: 1
				  card-ease-factor:: 2.6
				  card-next-schedule:: 2023-09-06T18:30:50.546Z
				  card-last-reviewed:: 2023-08-06T12:30:50.547Z
				  card-last-score:: 5
					- First, be sensitive to the redundancy in $e^{i\theta}$! 
					  We are expected to find a correspondence to the redundancy later. If not, we should ask why in turn.
					- Generally, ((64565059-ba36-4bfd-8fa8-516fa601aab3))
				-
		- Proposition (Localized eigenstates in Fourier space). The wavefunction falls off exponentially outside a finite range.
		  collapsed:: true
			- This guarantees that we can safely truncate the infinite-dimensional matrix in computation!
			  background-color:: yellow
				- Of course this would break the redundancy of solutions, but this doesn't matter.
			- It can be better explained by the picture: ((64570780-0ad1-467c-837e-f714c10c257a))
			- The energy is finite (actually $\epsilon_{min} < \epsilon < \epsilon_{min}+\hbar \omega$), so the wavefunction must fall off fast enough in the region of $|m| \gg 1$.
			- See [here](((64570949-fdbf-4862-9ae0-08c620620f74))) for reference.
	- Theorem. The winding number of the Floquet band vanishes.
		- [ref](((6458f435-7f01-4215-8b7b-77cffad95f95)))
		-
- # Floquet Perturbation Theory
  collapsed:: true
	- ## Analogue of Time-Independent Perturbation Theory
	  collapsed:: true
		- It can be most conveniently formulated in the notations of [[2018_Rodriguez-Vega_Lentz_Seradjeh_Floquet Perturbation Theory]].
		- Key idea
			- Conceptually remove the time-dependence by [[Lifting]] #Strategy :
			  $$\begin{aligned}
			  \epsilon _{\alpha } & =\epsilon _{\alpha (0)} +\epsilon _{\alpha (1)} +\epsilon _{\alpha (2)} +\cdots ,\\
			  | \overline{\phi _{\alpha }} \rangle \rangle  & =|\overline{\phi _{\alpha (0)}} \rangle \rangle +|\overline{\phi _{\alpha (1)}} \rangle \rangle +|\overline{\phi _{\alpha (2)}} \rangle \rangle +\cdots 
			  \end{aligned}$$
				- It is a rather strange idea, but seems very efficient in notion!
		- Result
			- $$\begin{aligned}
			  \epsilon _{\alpha (i)} & =\langle\langle \overline{\phi _{\alpha (0)}} |\hat{V} |\overline{\phi _{\alpha (i-1)}} \rangle\rangle ,\\
			  |\overline{\phi _{\alpha (i)}} \rangle\rangle  & =\widehat{\hat{P}}_{\alpha }\widehat{\hat{G}}_{0\alpha }\widehat{\hat{P}}_{\alpha }\left[\widehat{\hat{V}} |\overline{\phi _{\alpha (i-1)}} \rangle\rangle -\sum _{j=1}^{i-1} \epsilon _{\alpha (i-j)} |\overline{\phi _{\alpha (j)}} \rangle\rangle \right]
			  \end{aligned}$$
			- Explicitly:
			  $$\begin{aligned}
			  \epsilon _{\alpha (1)} & =\int _{0}^{T}< \phi _{\alpha (0)} (t)|{\hat{V}} (t)|\phi _{\alpha (0)} (t)> \frac{\mathrm{d} t}{T}\\
			  | \overline{\phi _{\alpha (1)}} \rangle \rangle  & =\sum _{(\beta ,n)\neq (\alpha ,0)}\frac{\langle \langle \phi _{\beta n(0)} | \hat{\hat{V}} |\overline{\phi _{\alpha (0)}} \rangle \rangle }{\epsilon _{\alpha (0)} -\epsilon _{\beta (0)} -n \Omega}| \phi _{\beta n(0)} \rangle \rangle 
			  \end{aligned}$$
	- ## Analogue of Time-Dependent Perturbation Theory
	  collapsed:: true
		- Setup
			- Here $H_{int}$ is time-independent.
			- Generally methods here can be easily generalized to cases where $H_{int}$ also has period $T$.
			- For non-periodical $H_{int}$, just calculate each cycle separately.
		- See [here](((64589611-210b-4bf9-a5ef-74e8c148fef6))) for reference.
		- Floquet Fermi's Golden rule
			- $$
			  W_{f i}=\frac{2 \pi}{\hbar}\left|M_{f i}\right|^2 \delta\left(\varepsilon_f-\varepsilon_i\right)
			  $$
				- $$
				  \begin{aligned}
				  M_{f i} & =\sum_{m m^{\prime}} \frac{1}{T} \int_0^T d t e^{-i\left(m-m^{\prime}\right) \omega t}\left\langle\phi_f^{\left(m^{\prime}\right)}\left|H_{\mathrm{int}}\right| \phi_i^{(m)}\right\rangle \\
				  & =\sum_m\left\langle\phi_f^{(m)}\left|H_{\mathrm{int}}\right| \phi_i^{(m)}\right\rangle
				  \end{aligned}
				  $$
			- Written compactly:
			  $$
			  W_{f i}=\frac{2 \pi}{\hbar}\left|\boldsymbol{\varphi}_f^{\dagger} \mathcal{H}_{\mathrm{int}} \boldsymbol{\varphi}_i\right|^2 \delta\left(\varepsilon_f-\varepsilon_i\right)
			  $$
			- Note that the formula is quite similar to a perturbation theory in the extended space,
			  $$
			  i \hbar \frac{d}{d \tau} \boldsymbol{\Psi}(\tau)=\left[\mathcal{H}+\mathcal{H}_{\mathrm{int}}\right] \mathbf{\Psi}(\tau)
			  $$
				- Lots of conceptual simplifications would follow.
- # Topics
	- ((6458f435-7f01-4215-8b7b-77cffad95f95)) Vanishing of the winding number
		- Related to topological properties
	- ((6459a497-7859-4007-b80f-bd6b56f8a1eb)) Green function and spectral function
	- ((6459a4b1-837c-4f70-8e3b-cdf71317da87)) Floquet-Kubo formula: Linear response in an additional weak perturbation, with a much longer period
	  id:: 6459a4a9-9d84-436f-adfa-d5005dda7050
	-
- # Example
  collapsed:: true
	- Gap opening at the Dirac point
		- Setup
			- $$
			  H_n(\mathbf{k})=v\left[\hbar \mathbf{k}-e A_0 \hat{\mathbf{e}}_n\right] \cdot \boldsymbol{\sigma}
			  $$
			- The drive has 4 steps in each cycle, pointing to $x,y,-x,-y$ separately.
				- ((6458f2e6-96eb-492c-8bdd-5417898fa90f))
		- Solution
			- $$
			  U(\mathbf{k}=0, T)=e^{-i \phi \sigma_y} e^{-i \phi \sigma_x} e^{i \phi \sigma_y} e^{i \phi \sigma_x}
			  $$
				- $$
				  \phi=e v A_0 T /(4 \hbar)
				  $$
			- Take the high-frequency limit, i.e. $\phi \ll 1$:
			  $$
			  \begin{aligned}
			  U(\mathbf{k}=0, T) & =\mathbf{1}+\phi^2\left[\sigma_x, \sigma_y\right]+\mathcal{O}\left(\phi^3\right) \\
			  & =\mathbf{1}+2 i \phi^2 \sigma_z \approx e^{2 i \phi^2 \sigma_z}
			  \end{aligned}
			  $$
				- Note that the better strategy is to calculate $\frac {d^2 U}{d\phi^2}$ rather than a brute-force expansion.
			- We can see the effective Hamiltonian is like $-2\hbar \phi^2 \sigma_z/T$ and the gap is opened!
			  background-color:: yellow
		- Remarks
			- First note the *gap* is defined for the **effective Hamiltonian**.
			  In other ways, we are examining the spectrum (band) of the effective Hamiltonian.
				- This makes sense when $\omega \gg 1$.
			-