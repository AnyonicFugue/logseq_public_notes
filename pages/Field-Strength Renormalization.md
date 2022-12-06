- Peskin
  id:: 63903248-5ecc-4f16-8bab-63ae5ea8de98
	- Summary #card
		- Goal: calculate the corrections to the electron propagator.
			- This renormalizes mass, not charge.
		- General analysis of the correction
			- $$\langle\Omega|\phi(x) \phi(y)| \Omega\rangle=\sum_\lambda \int \frac{d^4 p}{(2 \pi)^4} \frac{i}{p^2-m_\lambda^2+i \epsilon} e^{-i p \cdot(x-y)}\left|\left\langle\Omega|\phi(0)| \lambda_0\right\rangle\right|^2$$
				- Key technique: ((63973120-efca-48be-9b42-55cc35b82675))
				- In other words, the Hilbert space consists of **several Lorentz sectors**
			- Interpretation: Each sector corresponds to a group of 'particles'. $\left\langle\Omega|\phi(0)| \lambda_0\right\rangle$ is the probability of creating it from vacuum.
		- Use 1PI diagrams to simplify the sum
			- ((63996a20-7140-4eed-a808-ddbee821afb6))
		- $\begin{aligned} \int d^4 x\langle\Omega| T \psi(x) & \bar{\psi}(0)|\Omega\rangle e^{i p \cdot x} \\ & =\frac{i}{\not p-m_0}+\frac{i}{\not p-m_0}\left(\frac{\Sigma(\not p)}{\not p-m_0}\right)+\frac{i}{\not p-m_0}\left(\frac{\Sigma(\not p)}{\not p-m_0}\right)^2+\cdots \\ & =\frac{i}{\not p-m_0-\Sigma(\not p)} \end{aligned}$
			- Renormalized mass corresponds to the singularity (assumed only one) in the propagator
		- Perform the integration
			- ((6390421c-b60b-469d-89ca-ba3cfd888f4e))
				- $$
				  -i \Sigma_2(p)=(-i e)^2 \int \frac{d^4 k}{(2 \pi)^4} \gamma^\mu \frac{i\left(\not k+m_0\right)}{k^2-m_0^2+i \epsilon} \gamma_\mu \frac{-i}{(p-k)^2-\mu^2+i \epsilon}
				  $$
			-
			- Pure routines: ((63973120-916a-488f-9ed8-27ee2535f0c1)), complete the square, shift integration variable, Wick rotation.
			- Then we'll find that the integration is divergent.
		- Perform [[Pauli-Villars Regularization]] to compute the lowest-order contribution
			- $$\frac{i}{(4 \pi)^2} \log \left(\frac{\Delta_{\Lambda}}{\Delta}\right)$$
			- Still divergent.
	- # Remember to also make flashcards!
	- Rewrite the Lagrangians
		- $\mathcal{L}=-\frac{1}{4} Z_3\left(F_{\mu \nu}\right)_r^2+Z_2 \bar{\psi}_r\left(i \not \partial-m_0\right) \psi_r-Z_2 Z_3^{\frac{1}{2}} e_0 \bar{\psi}_r \gamma^\mu \psi_r A_\mu^r$
		- $$\begin{aligned}
		  \mathcal{L} & =\mathcal{L}^{(1)}+\mathcal{L}^{(2)} \\
		  & =\left(-\frac{1}{4} F_{\mu \nu}^2+\bar{\psi}(i \not \partial-m) \psi-e \bar{\psi} \gamma^\mu \psi A_\mu\right)+\left(-\frac{1}{4} \delta_3 F_{\mu \nu}^2+\bar{\psi}\left(i \delta_2 \not \partial-\delta_m\right) \psi-e \delta_1 \bar{\psi} \gamma^\mu \psi A_\mu\right)
		  \end{aligned}$$
			- $Z_i=1+\delta_i$, $\delta_i$ are called **counter terms**.
	- ((639094ce-9088-4138-a4b5-7ac7f96f7d15)) General analysis of propagators
		- ((6390331c-7c49-4e6a-a6ca-696572b0f022))
			- Non-perturbative analysis is often quite exotic and abstract, but provide more insight. #Thoughts
		- ((6390335e-a793-430c-8a22-87c12f7ff053))
			- Does this hold for general interacting states?
			- He writes ((639033da-bf24-48bf-a704-d1aebf9aa3b5)), which seem to justify the claim. But can we do this for interacting states?
		- ((63903a83-0912-45ba-90fd-b1560f31adc1)), i.e. boost an eigenstate to obtain all possible momenta.
			- But we may not obtain all eigenstates in this way. We may not change particle numbers, or even relative velocities of the particles, by boosting.
			- Does he assume H to have (formal) Lorentz invariance?
			  background-color:: red
				- Intuitively, we can arbitrarily boost an on-shell particle.
			- Maybe still justified by the '4-momentum operator'.
		- Completeness relation
			- 1-p
				- $$
				  (\mathbf{1})_{1-\text { particlc }}=\int \frac{d^3 p}{(2 \pi)^3} \frac{1}{2 E_{\mathbf{p}}}|\mathbf{p}\rangle\langle\mathbf{p}|
				  $$
				- In other words, zero-momentum state is unique for 1-particle.
			- General
				- id:: 63973120-efca-48be-9b42-55cc35b82675
				  $$
				  \mathbf{1}=|\Omega\rangle\langle\Omega|+\sum_\lambda \int \frac{d^3 p}{(2 \pi)^3} \frac{1}{2 E_{\mathbf{p}}(\lambda)}| \lambda_{\mathbf{p}}\rangle\left\langle\lambda_{\mathbf{p}}\right|
				  $$
				- Boost all momenta from zero-momentum states.
		- Insert the relation
			- $$\langle\Omega|\phi(x) \phi(y\rangle| \Omega\rangle=\sum_\lambda \int \frac{d^3 p}{(2 \pi)^3} \frac{1}{2 E_{\mathbf{p}}(\lambda)}\left\langle\Omega|\phi(x)| \lambda_{\mathbf{p}}\right\rangle\left\langle\lambda_{\mathbf{p}}|\phi(y)| \Omega\right\rangle$$
				- The vacuum diagonal element is zero.
			- $\begin{aligned}\left\langle\Omega^{\prime} |\phi(x) |\lambda_{\mathbf{p}}\right\rangle & =\left\langle\Omega\left|e^{i P \cdot x} \phi(0) e^{-i P \cdot x}\right| \lambda_{\mathbf{p}}\right\rangle \\ & =\left.\left\langle\Omega|\phi(0)| \lambda_{\mathbf{p}}\right\rangle e^{-i p \cdot x}\right|_{p^0=E_{\mathbf{p}}} \\ & =\left.\left\langle\Omega|\phi(0)| \lambda_0\right\rangle e^{-i p \cdot x}\right|_{p^0=E_{\mathbf{p}}}\end{aligned}$
				- 1st line: Just a change of basis. P is the generator of translations.
				- 2nd: Extract the eigenvalues
				- 3rd: ((63996ae9-da3c-4b64-94cd-0250fbb3555f)).
		- Introduce an integration over p to obtain the heaviside function, $\langle\Omega|\phi(x) \phi(y)| \Omega\rangle=\sum_\lambda \int \frac{d^4 p}{(2 \pi)^4} \frac{i}{p^2-m_\lambda^2+i \epsilon} e^{-i p \cdot(x-y)}\left|\left\langle\Omega|\phi(0)| \lambda_0\right\rangle\right|^2$
			- Familiar form!
		- ((63903dc0-decd-4562-9c8f-9f20c0b8fbe3))
			- $$\langle\Omega|T \phi(x) \phi(y)| \Omega\rangle=\int_0^{\infty} \frac{d M^2}{2 \pi} \rho\left(M^2\right) D_F\left(x-y ; M^2\right)$$
				- $$
				  \rho\left(M^2\right)=\sum_\lambda(2 \pi) \delta\left(M^2-m_\lambda^2\right)\left|\left\langle\Omega|\phi(0)| \lambda_0\right\rangle\right|^2
				  $$
				  Called **spectral density**
				- Intuitively, the 2-point correlation function can be decomposed into contributions of different effective masses.
			- Fourier Transformation
				- ((63903fa9-eb94-4b67-944e-453099d998c0))
					- Familiar Feynman propagator!
				- ((63904004-1719-49a0-a4ed-ae545a9d3ac2)), but with field-strength renormalizations
		- 1-particle part
			- ((63903e68-8a6e-48a0-9986-d91b226fea87))
			- Z is the field-strength renormalization
			- m here is ((63903e92-e09c-4f19-8a07-012214461679))
			- $m_0$ in the Lagrangian is the ((63903ea6-2939-4f43-9d05-c658b31ce1ae))
		- ((63904079-1b0a-4901-9470-1714586e2e26))
		- ((6390416f-d1e2-4be7-a6dc-5ca7e71d8cd4))ds. We just need to modify the transformation rules under Lorentz transformations.
		  collapsed:: true
			- Dirac field ((63904193-3f90-4077-a320-ee734d2a3f38))
		-
	- Electron self-energy
		- ((6390421c-b60b-469d-89ca-ba3cfd888f4e))
		- ((6390428b-6de4-484a-911d-f6844fc10ba1))
			- Bare mass.
		- [[1PI]] diagrams
			- ## To obtain the complete result, we must sum all Feynman diagrams.
			- Def
				- Any diagram that cannot be split in two by removing a single line
				- ((63904489-d38e-4c14-b1e2-45ee3ff06317))
				- Define ((639044b6-c729-4c9a-835f-8a273b874d9f))
			- They serve as building blocks of all Feynman diagrams
			- Sum all possible diagrams
				- ((63996a20-7140-4eed-a808-ddbee821afb6))
				- Note that $\Sigma(p)$ commutes with $\not p$, since $\Sigma(p)$ is a function only of pure numbers and $\not p$. In fact, we can consider $\Sigma(p)$ to be a function of $\not p$, writing $p^2=(\not p)^2$. Then we can rewrite each electron propagator as $i /\left(\not p-m_0\right)$. #card
					- Reminder card: By analyzing the only possible quantities, we can obtain some commutation relations.
					- Very convenient! Simplify the matrix equation into an algebraic equation.
				- Sum up the geometric series, obtain the next line
		- $\begin{aligned} \int d^4 x\langle\Omega| T \psi(x) & \bar{\psi}(0)|\Omega\rangle e^{i p \cdot x} \\ & =\frac{i}{\not p-m_0}+\frac{i}{\not p-m_0}\left(\frac{\Sigma(\not p)}{\not p-m_0}\right)+\frac{i}{\not p-m_0}\left(\frac{\Sigma(\not p)}{\not p-m_0}\right)^2+\cdots \\ & =\frac{i}{\not p-m_0-\Sigma(\not p)} \end{aligned}$
			- 'Slash in the numerator' denotes the inverse matrix.
			- Correction to electron mass
				- Mass is indicated by the pole in the denominator.
				- m is the solution to $\left.\left[\not p-m_0-\Sigma(\not p)\right]\right|_{\not p=mI}=0$
			- Correction to the propagator
				- We want to retain a similar form to $\frac{i}{\not p-m_0}$
				- $\not p-m_0-\Sigma(\not p)=(\not p-m) \cdot\left(1-\left.\frac{d \Sigma}{d \not p}\right|_{\not p=m}\right)+\mathcal{O}\left((\not p-m)^2\right)$
					- Obtained by differentiating wrt $\not p$
				- Thus $Z_2^{-1}=1-\left.\frac{d \Sigma}{d \not p}\right|_{\not p=m}$
					- $Z_2$ is defined as the correction **factor** of the propagator.
	- Lowest-order correction to 1PI 
	  id:: 639042c5-a7a2-45aa-a0a6-3d3d10be46e9
	  collapsed:: true
		- ((639042b9-c9fd-499a-8cdc-12c6adff64fd))
			- Note that the 'lines connected on it' aren't counted in this diagram.
		- $$
		  -i \Sigma_2(p)=(-i e)^2 \int \frac{d^4 k}{(2 \pi)^4} \gamma^\mu \frac{i\left(\not k+m_0\right)}{k^2-m_0^2+i \epsilon} \gamma_\mu \frac{-i}{(p-k)^2-\mu^2+i \epsilon}
		  $$
			- IR is regularized by $\mu$.
		-
		- [[Feynman parameter]] to combine the denominators
		  id:: 63973120-916a-488f-9ed8-27ee2535f0c1
			- $$
			  \frac{1}{k^2-m_0^2+i \epsilon} \frac{1}{(p-k)^2-\mu^2+i \epsilon}=\int_0^1 d x \frac{1}{\left[k^2-2 x k \cdot p+x p^2-x \mu^2-(1-x) m_0^2+i \epsilon\right]^2}
			  $$
			- Then complete the square
		- Intermediate. 
		  $$
		  -i \Sigma_2(p)=-e^2 \int_0^1 d x \int \frac{d^4 \ell}{(2 \pi)^4} \frac{-2 x \not p+4 m_0}{\left[\ell^2-\Delta+i \epsilon\right]^2}
		  $$
		- PV regularization
			- $$
			  \begin{aligned}
			  \int \frac{d^4 \ell}{(2 \pi)^4} \frac{1}{\left[\ell^2-\Delta\right]^2} & \rightarrow \frac{i}{(4 \pi)^2} \int_0^{\infty} d \ell_E^2\left(\frac{\ell_E^2}{\left[\ell_E^2+\Delta\right]^2}-\frac{\ell_E^2}{\left[\ell_E^2+\Delta_{\Lambda}\right]^2}\right) \\
			  & =\frac{i}{(4 \pi)^2} \log \left(\frac{\Delta_{\Lambda}}{\Delta}\right)
			  \end{aligned}
			  $$
	- ## Final result
		- $$
		  \Sigma_2(p)=\frac{\alpha}{2 \pi} \int_0^1 d x\left(2 m_0-x \not p\right) \log \left(\frac{x \Lambda^2}{(1-x) m_0^2+x \mu^2-x(1-x) p^2}\right)
		  $$
			- $m_0$ is a multiple of the identity matrix.
		- The correction **diverges**, which fits the physical intuition that the energy of EM field of a point-like charge diverges.
	- Remarkably, $\delta F_1(0)+\delta Z_2=0$
		- This is not a coincidence.
		- ((639095f7-eca6-4422-b053-b1f4c26be60c)) in ((638d5442-2da2-466c-8e73-91b7fff0a3a3))
-