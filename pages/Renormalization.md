- ((63902f14-d931-401b-a27f-5d9f95c9791c))
	- For example, physical mass of electrons are not the bare mass.
- # Principles and the Paradigm #card
	- ## Empirical Knowledge
		- We can't probe physics at arbitrarily high $E$.
			- Therefore, integrating to $k \to \infty$ is a huge **extrapolation**. (It's miraculous this doesn't fail completely).
			- We can't even be sure that the theory is local or Lorentz covariant at high $E$.
			- #+BEGIN_IMPORTANT
			  Humankind is limited.
			  But this is also a gift and a spectacle; such fragile creatures can try to probe greater and greater structures as $E \to \infty$!
			  #+END_IMPORTANT
			- But can't we?
				- We can't know the full details, but is it possible to test a few **principles** (e.g. Lorentz covariance)?
				- Also, divergence is the prescence of high-energy physics. #[[Thoughts/Math and Physics]]
					- To be more accurate, theoretically there are divergences, but experimentally nothing is divergent. Therefore some mechanism must protect the observables from diverging.
		- Observations at $E \lesssim E_{\max }$ shouldn't depend esssentially on high energies.
		  id:: 6447451d-a5e6-4238-b04e-d4ea94425152
			- Intuitively plausible.
				- Mr. Shao argued it from the uncertainty principle (we can't determine arbitrarily small details with finite energy), which seems not so convincing.
			- **Corollary**. Physical quantities should be independent of regularization.
	- **Conjecture**. We can replace the [[Bare]] quantities by physical quantities ($m_0$ by $m$, $e_0$ by $e$, ...) in the Lagrangian and obtain testable predictions.
		- This is highly nontrivial!
			- In principle the form of the Lagrangian should also change.
			-
	- However, what does high $E$ mean?
		- In QM we always have **eigen energy** and **expectation value**. Which is the $E$ here?
- # Schemes of Regularization
	- [[Dimensional Regularization]]
	- [[Cutoff]] Regularization
- # Renormalized Perturbation Theory
	-
	- Idea #card
		- The 'real world of QFT' is quite messy. We must consider lots of renormalizations; what's worse, we don't know how to obtain a divergence-free result.
		- Therefore we do two things to obtain an elegant formalism:
		  1. Redefine the field and constants to account for all renormalization
		  2. Let the divergences cancel by comparing different kinematics (momenta)
		- #+BEGIN_CAUTION
		  It's like I suddenly find that the simple world in QFT1, where the propagator is a simple $\frac i {p^2-m^2+i\varepsilon}$ and we don't have to worry about loops or divergences, is supported by a dark and complicated 'real world'...
		  #+END_CAUTION
	- Renormalized Field
		- Starting point:
		  $$
		  \int d^4 x e^{i p \cdot x}\left\langle\Omega\left|T\left\{\phi_0(x) \phi_0(0)\right\}\right| \Omega\right\rangle \stackrel{p^2 \rightarrow m^2}{\longrightarrow} \frac{i Z}{p^2-m^2+i \varepsilon}+\cdots
		  $$
			- We want to get rid of the awkward factor of $Z$, which is even divergent.
		- Def. $\phi_0=\sqrt{Z} \phi$
			- $\phi_0$ is the bare field and $\phi$ is the renormalized one
			- Correspondingly, the **renormalized Green function** writes
			  $$G^{(n)}( x_{1} \cdots x_{n}) =(\sqrt{Z} )^{-n} G_{0}^{(n)}( x_{1} \cdots x_{n}) \equiv (\sqrt{Z} )^{-n} \left\langle \Omega| T\{\phi _{0}( x_{1}) \cdots \phi _{0}( x_{n})\}|\Omega \right\rangle $$
			  where all factors of $Z$ are killed.
			-
	- ## Scheme 1: Cancel the Divergences in the Bare Lagrangian
		- (1) Compute $m,\lambda,Z$ as functions of $m_0,\lambda_0$ to the required order.
			- There are bound to be divergences.
		- (2) Determine $m$ and $\lambda$ at a reference point (e.g. the threshold), where they can be measured **experimentally**.
			- Reinforcements ready!
		- (3) Compute the bare Green function $G_n^{(0)}$ ;
		  express $\lambda_0,m_0$ by $\lambda,m$ and multiply it by $(\sqrt Z)^{-n}$
			- In expressing $\lambda_0,m_0$ by $\lambda,m$ we let the divergences cancel.
		- Finally we obtain the renormalized Green function, which we expect be **divergence-free** and **regularization-independent**.
		-
	- ## Scheme 2: Rewrite the Lagrangian by Physical Quantities
		- (1) Write $\phi_0=\sqrt{Z} \phi, m_0^2=m^2+\delta m^2, \lambda_0=z_\lambda \lambda \tilde{\mu}^{2 \varepsilon}$ where $z, \delta m^2, z_\lambda$ are to be determined.
		- (2) Rearrange the Lagrangian into a 'physical part' and a 'counter part':
		  $$\begin{aligned}
		  \mathcal{L} = & \frac{1}{2}\left( \partial ^{\mu } \phi _{0} \partial _{\mu } \phi _{0} -m_{0}^{2} \phi _{0}^{2}\right) -\frac{\lambda _{0}}{4!} \phi _{0}^{4}\\
		  = & \frac{1}{2} Z\partial ^{\mu } \phi \partial _{\mu } \phi -\frac{1}{2} Z\left( m^{2} +\delta m^{2}\right) \phi ^{2} -Z_{\lambda } Z^{2}\tilde{\mu }^{2\varepsilon }\frac{\lambda }{4!} \phi ^{4}\\
		  = & \left\{\frac{1}{2} \partial ^{\mu } \phi \partial _{\mu } \phi -\frac{1}{2} m^{2} \phi ^{2} -\frac{\lambda \tilde{\mu }^{2\varepsilon }}{4!} \phi ^{4}\right\} \ \text{(Physical)} \ +\\
		   & \left\{\frac{1}{2} (Z-1)\partial ^{\mu } \phi \partial _{\mu } \phi -\frac{1}{2}\left[ (Z-1)m^{2} +Z\delta _{m}^{2}\right] \phi ^{2} -\left( Z_{\lambda } Z^{2} -1\right)\frac{\lambda \tilde{\mu }^{2\varepsilon }}{4!} \phi ^{4}\right\} \ \text{(Counter)}
		  \end{aligned}$$
			- The counter term is to cancel all effects of renormalization and keep the formalism simple and elegant.
		- (3) Determine the counter terms order by order from the requirement that
		  ![image.png](../assets/image_1682478526468_0.png)
		  Which translates into
		  $$\left.\Pi\left(p^2, m^2\right)\right|_{p^2=m^2}=\left.0 , \quad \frac{d \Pi}{d p^2}\right|_{p^2=m^2}=0$$
			- Which means the **physical propagator** is simple and elegant.
			- Note that it is not guaranteed that there is a solution which works at all order.
			  background-color:: yellow
			  In fact the existence is itself extremely nontrivial.
		- *Illustration of how to determine the counterterms
			- 1-loop order:
				- ![image.png](../assets/image_1682478589893_0.png){:height 178, :width 1035}
				- $$\begin{aligned}
				  \overset{\text{Cutoff Regularization}}{=} & \frac{-i\lambda }{32\pi ^{2}}\left[ \Lambda ^{2} -m^{2}\ln\frac{\Lambda ^{2}}{m^{2}} +o\left(\frac{m^{4}}{\Lambda ^{2}}\right)\right] -i\left( \delta _{z} p^{2} +\delta _{m}\right)\\
				  \stackrel{p^{2}\rightarrow m^{2}}{\Longrightarrow } & \left\{\begin{array}{ l }
				  \delta _{Z} m^{2} +\delta \left( m^{2}\right) =-\frac{\lambda }{32\pi ^{2}}\left[ \Lambda ^{2} -m^{2}\ln\frac{\Lambda ^{2}}{m^{2}} +o\left(\frac{m^{4}}{\Lambda ^{2}}\right)\right]\\
				  \delta _{Z} =0
				  \end{array}\right. \\
				  \Longrightarrow  & \delta \left( m^{2}\right) =-\frac{\lambda }{32\pi ^{2}}\left[ \Lambda ^{2} -m^{2}\ln\frac{\Lambda ^{2}}{m^{2}} +0\left(\frac{m^{4}}{\Lambda ^{2}}\right)\right]
				  \end{aligned}$$
			- 2-loop order
				- ![image.png](../assets/image_1682478818350_0.png){:height 350, :width 863}
- # Thoughts
	- ## Flaws of Perturbation Theory?
		- From the viewpoint of exact diagonalization
			- The behaviors of low energy levels are completely determined by their energies and evolve according to $e^{iE_n t}$.
			- High energies shall not have any influences on the low energy levels!
		- However, if we want to calculate the transition amplitude perturbatively, we must sum over **all** energy levels (if we want to go beyond the first order).
			- See ((644730bc-03b5-48b5-a75e-c31bdf1e5919))
			- This can be explained in another viewpoint: We're in the **wrong basis**.
				- We've selected the eigenstates of the unperturbed Hamiltonian, which in general is a superposition of the eigenstates of the full Hamiltonian, with possibly eigenstates of arbitrarily high energies.
			-
	- ## Divergence, Cutoff and New Physics
		- Fluid mechanics
			- Microscopic degrees of freedom (motion of the atoms) behave as macroscopic degrees of freedom (transportation, sound waves) after renormalization.
			- When the scale is too small, macroscopic fluid mechanics breaks down. 
			  It implies the existence of finer structures at the atomic level.
		- [[QFT]]
			- ((63902fd3-2777-45da-a15d-df163f153399))
			- It is a miracle that the [[Photon]] has zero mass!
- # Example
	- $\phi \phi \to \phi \phi$ at 1-loop for $\phi^4$ theory
		- Draw the diagrams:
		  ![image.png](../assets/image_1682470852307_0.png)
		- The amplitude can be calculated by dimensional regularization:
		  $$iT=(\sqrt{Z} )^{4}\tilde{G}_{amp}^{(4)}( q_{1} q_{2} ,p_{1} p_{2})$$
		  $$
		  \tilde{G}_{a m p}^{(4)}=-i \lambda_0\left\{1-\frac{\lambda_0 \tilde{\mu}^{-2 \varepsilon}}{32 \pi^2}\left[\frac{3}{\varepsilon}-3 \ln \frac{m_0^2}{\mu^2}-A(s)-A(t)-A(u)\right]+o\left(\lambda_0^2\right)\right\}
		  $$
			- $\tilde \mu$ is introduced to keep the mass dimension to zero (at $d=4-2\varepsilon$)
			- $\sqrt Z$ appears since the renormalized field $\phi =\frac 1 {\sqrt Z} \phi_0$. Here the internal fields are renormalized ones (the propagators are $\frac i {p^2-m^2+i\varepsilon}$), but the external fields are **not**.
			- $s,t,u$ are the ((64238e6c-1aa2-4233-b9ab-a0b3e391eda2))
		- The amplitude is **divergent** at $d=4$. But we can still make some sense out of this. #card
			- Idea: We can measure $\lambda$ at some reference scattering process (e.g. at the shreshold, i.e. $s=4m^2,u=t=0$).
			  Then we can compare different momenta to **cancel the divergence**.
				- In other words, experimental data could also be a valuable input -- to fix a 'reference' not available from first principles! #[[Thoughts/Math and Physics]]
				- This works since the UV divergence arises from the loop momenta and is independent of external momenta.
			- Specifically:
				- The effective coupling $\lambda$ satisfies
				  $$
				  \left.(\sqrt{Z})^4 \tilde{G}_{a m p}^{(4)}\right|_{s=4 m^2, u=t=0} \equiv-i \lambda \tilde{\mu}^{2 \varepsilon}
				  $$
				  which can be measured experimentally.
				- With cut-off regularization, we can write down
				  $$
				  \lambda=\lambda_0\left\{1-\frac{\lambda_0}{32 \pi^2}\left[3 \ln \frac{\Lambda^2}{m_0^2}-3-A\left(4 m^2\right)\right]+\cdots\right\}
				  $$
				- Then we express the amplitudes at other kinematics by $\lambda$:
				  $$\begin{aligned}
				  (\sqrt{Z} )^{4}\tilde{G}_{amp}^{(4)} = & -i\lambda \tilde{\mu }^{2\varepsilon }\left\{1+\frac{\lambda }{32\pi ^{2}}\left[\frac{3}{\varepsilon } -3\ln\frac{m_{0}^{2}}{\mu ^{2}} -A\left( 4m^{2}\right)\right] +o\left( \lambda ^{2}\right)\right\}\\
				   & \times \left\{1-\frac{\lambda }{32\pi ^{2}}\left[\frac{3}{\varepsilon } -3\ln\frac{m_{0}^{2}}{\mu ^{2}} -A(s)-A(t)-A(u)\right] +o\left( \lambda ^{2}\right)\right\}\\
				  = & -i\lambda \left\{1+\frac{\lambda }{32\pi ^{2}}\left[ A(s)+A(t)+A(u)-A\left( 4m^{2}\right)\right] +o\left( \lambda ^{2}\right)\right\}
				  \end{aligned}$$
				  which is free from divergence and $Z$!
				-
		-
-