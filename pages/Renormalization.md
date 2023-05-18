- ((63902f14-d931-401b-a27f-5d9f95c9791c))
	- For example, physical mass of electrons are not the bare mass.
- # Principles and the Paradigm #card
  collapsed:: true
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
  collapsed:: true
	- [[Dimensional Regularization]]
	- [[Cutoff]] Regularization
- # Schemes of Renormalization
  collapsed:: true
	- ## Scheme 1: Cancel the Divergences via Physical Quantities #card
	  collapsed:: true
		- Idea
			- Physical quantities like $m,\lambda$ can be determined experimentally.
			- Thus we first express $m,\lambda$ as a function of $m_0,\lambda_0$ and vice versa.
			  The expression must be formally divergent.
			- When we wish to calculate some observable $A$, $A(m_0,\lambda_0)$ is formally divergent,
			  but $A(m_0(m,\lambda),\lambda_0(m,\lambda))$ is **not**.
		- (1) Compute $m,\lambda,Z$ as functions of $m_0,\lambda_0$ to the required order.
			- There are bound to be divergences.
		- (2) Determine $m$ and $\lambda$ at a reference point (e.g. the threshold), where they can be measured **experimentally**.
			- Reinforcements ready!
		- (3) Compute the bare Green function $G_n^{(0)}$ ;
		  express $\lambda_0,m_0$ by $\lambda,m$ and multiply it by $(\sqrt Z)^{-n}$
			- In expressing $\lambda_0,m_0$ by $\lambda,m$ we let the divergences cancel.
		- Finally we obtain the renormalized Green function, which we expect be **divergence-free** and **regularization-independent**.
		-
	- ## Scheme 2: Cancel the Divergent Diagrams by Counter-terms #card
	  collapsed:: true
		- Idea
			- Rewrite the Lagrangian as a physical part and a counter-term part
			- The latter part produce diagrams which cancel the divergent diagrams of the physical part.
			  Thus we may only consider tree-level diagrams of the physical part.
		- (1) Write $\phi_0=\sqrt{Z} \phi, m_0^2=m^2+\delta m^2, \lambda_0=Z_\lambda \lambda \tilde{\mu}^{2 \varepsilon}$ where $Z, \delta m^2, Z_\lambda$ are to be determined.
		- (2) Rearrange the Lagrangian into a 'physical part' and a 'counter part':
		  $$\begin{aligned}
		  \mathcal{L} = & \frac{1}{2}\left( \partial ^{\mu } \phi _{0} \partial _{\mu } \phi _{0} -m_{0}^{2} \phi _{0}^{2}\right) -\frac{\lambda _{0}}{4!} \phi _{0}^{4}\\
		  = & \frac{1}{2} Z\partial ^{\mu } \phi \partial _{\mu } \phi -\frac{1}{2} Z\left( m^{2} +\delta m^{2}\right) \phi ^{2} -Z_{\lambda } Z^{2}\tilde{\mu }^{2\varepsilon }\frac{\lambda }{4!} \phi ^{4}\\
		  = & \left\{\frac{1}{2} \partial ^{\mu } \phi \partial _{\mu } \phi -\frac{1}{2} m^{2} \phi ^{2} -\frac{\lambda \tilde{\mu }^{2\varepsilon }}{4!} \phi ^{4}\right\} \ \text{(Physical)} \ +\\
		   & \left\{\frac{1}{2} (Z-1)\partial ^{\mu } \phi \partial _{\mu } \phi -\frac{1}{2}\left[ (Z-1)m^{2} +Z\delta {m}^{2}\right] \phi ^{2} -\left( Z_{\lambda } Z^{2} -1\right)\frac{\lambda \tilde{\mu }^{2\varepsilon }}{4!} \phi ^{4}\right\} \ \text{(Counter)}
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
	- ## Scheme 3: Modified Minimal Subtraction
	  collapsed:: true
		- Idea
			- This is similar to scheme 2. But we change the requirement here:
			  In scheme 2 we require the counterterms make $\Pi=0$ and $\frac {d\Pi}{dp^2}=0$ at $p^2=m^2$.
			  Here we only require the counterterms to cancel the divergences.
		- Example in $\phi^4$ theory
			- $$\begin{aligned}
			  -i\Pi  = & \frac{-i\lambda }{32\pi ^{2}}\left( -m^{2}\right)\left(\frac{1}{\varepsilon } -\ln\frac{m^{2}}{\mu ^{2}} +1\right) -i\left( \delta _{Z} p^{2} +\delta _{m}\right)\\
			  \text{ on-shell:} \ \delta _{m} = & \frac{\lambda }{32\pi ^{2}} m^{2}\left(\frac{1}{\varepsilon } -\ln\frac{m^{2}}{\mu ^{2}} +1\right) \ \ \text{so that } \Pi | _{p^{2} =m^{2}} =0\\
			  \overline{MS} \ \ :\ \ \delta _{m} = & \frac{\lambda }{32\pi ^{2}} m^{2}\frac{1}{\varepsilon } \ \text{Only cancelling the divergence}
			  \end{aligned}$$
			- Thus we can compare the physical mass (on-shell mass) and the MS mass:
			  $$\begin{aligned}
			  m_{0}^{2} = & m_{\text{phys }}^{2} +\delta m_{\text{phys }}^{2} =m_{\text{phys }}^{2}\left[ 1+\frac{\lambda }{32\pi ^{2}}\left(\frac{1}{\varepsilon } -\ln\frac{m_{\text{phys }}^{2}}{\mu ^{2}} +1\right)\right]\\
			  = & \overline{m}^{2} (\mu )+\delta \overline{m}^{2} (\mu )=\overline{m}^{2} (\mu )\left[ 1+\frac{\lambda }{32\pi ^{2}}\left(\frac{1}{\varepsilon }\right) +\cdots \right]\\
			  m_{\text{phys }}^{2} = & \overline{m}^{2} (\mu )\left[ 1+\frac{\lambda }{32\pi ^{2}}\left(\ln\frac{\overline{m}^{2} (\mu )}{\mu ^{2}} +1\right) +o\left( \lambda ^{2}\right)\right]
			  \end{aligned}$$
			- We see that the mass in the MS scheme is dependent on the scale factor $\mu$. This is a common feature for quantities in the scale-dependent renormalization schemes.
			  background-color:: yellow
	- ## Scheme 4: On-Shell Renormalization
		- Idea
			- We want the propagator to be in the desired form when $p^2 \to m^2$.
		- The bare propagator:
		  $$S_0^{(2)}(p)=\int d^4 x e^{i p \cdot x}\left\langle\Omega\left|T\left\{\psi_0(x) \bar{\psi}_0(0)\right\}\right| \Omega\right\rangle \\
		  \overset{p^2 \to m^2}{\to} Z_2 \frac{i(\not p+m)}{p^2-m^2+i \varepsilon}+\text { non-singular. }$$
			- Note that fields in the first line are bare fields, but mass in the second line is the **physical** mass.
			- The physical meaning: At low energies ($p^2 - m^2$ not large), the propagator is the physical propagator.
				- Note that the propagator is not only defined for on-shell momenta.
		- The renormalized propagator:
		  $$S^{(2)}(p)=\frac{i}{p-m-\Sigma(p, m)} \quad \stackrel{p^2 \rightarrow m^2}{\longrightarrow} \frac{i}{\not p-m+i \varepsilon}$$
			-
- # Renormalized Perturbation Theory
  collapsed:: true
	- Idea #card
	  collapsed:: true
		- The 'real world of QFT' is quite messy. We must consider lots of renormalizations; what's worse, we don't know how to obtain a divergence-free result.
		- Therefore we do two things to obtain an elegant formalism:
		  1. Redefine the field and constants to account for all renormalization
		  2. Let the divergences cancel by comparing different kinematics (momenta)
		- #+BEGIN_CAUTION
		  It's like I suddenly find that the simple world in QFT1, where the propagator is a simple $\frac i {p^2-m^2+i\varepsilon}$ and we don't have to worry about loops or divergences, is supported by a dark and complicated 'real world'...
		  #+END_CAUTION
	- Renormalized Field
	  collapsed:: true
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
- # Systematic Analysis
  collapsed:: true
	- Summary #card
	  collapsed:: true
		- Starting point: How to characterize renormalizability?
		- Idea: Determine convergence by the power of momenta in the integrand
		  collapsed:: true
			- Note that the integrand is always a fraction of polynomials in $p$, whose UV convergence can be determined by the power analysis.
		- Detailed analysis
		  collapsed:: true
			- Divergent subdiagrams:
			- Multi-loop diagrams:
		- Final theorem of renormalizability:
		  (a) $\Delta_i \geqslant 0$ for all vertices
		  (b) $\mathcal{L}$ contains all vertices compatible with the symmetries of the (regularized) theory. (The regularization may break a symmetry Then it is no longer a symmetry of $\mathcal{L}$)
	- ## Starting point
	  collapsed:: true
		- Question: Is all theories renormalizable? If not, how to characterize renormalizability?
		  background-color:: red
		- Intuitively, we only have a finite number of parameters (mass, coupling constant, etc). Can we cancel divergences in **all** diagrams by the finite parameters?
	- ## Setup
	  collapsed:: true
		- Notations
		  collapsed:: true
			- $\gamma$ : 1PI Feynmann diagram
			- $L$ : number of loops
			- $I_{f}$ : number of internal lines (propagators) of field of type $f$
			- $E_{f}$: number of external lines (propagators) of field of type $f$
			- $s_f$: The propagator of field $f$ is asymptotically $1/(k^2)^{1-s_f}$
			  collapsed:: true
				- e.g. $s_f=0$ for scalar fields, $s_f=1/2$ for Dirac fields.
			- $V_{i}$ : number of vertices of type $i$
			- $a_{i}$ : number of derivatives on fields in vertex of type $i$
			- $n_{if}$: number of fields of type $f$ in vertex of type $i$
			- $d$ : Spacetime dimension
			-
		- Definitions
		  collapsed:: true
			- Degree of divergence, $D(\gamma)$
			  collapsed:: true
				- {Maximal power of momenta in the numerator, including the integration measure} - {maximal power of momenta in the denominator}
				- Example. 
				  ![image.png](../assets/image_1683335815102_0.png){:height 307, :width 957}
	- ## Simplifications
	  collapsed:: true
		- Note that lines connecting 1PI diagrams cannot contain loops, so we may just analyze 1PI diagrams.
		  collapsed:: true
			- Analogous to 'analyze path-connected spaces'.
	- ## Counting the divergences
	  collapsed:: true
		- Idea
		  collapsed:: true
			- Count the total powers of momenta (numerator - denominator).
			  If the power is greater than zero, then the diagram surely diverges.
		- Proposition. If $D(\gamma) \geq 0$, then the diagram must be divergent.
		  collapsed:: true
			- If $D(\gamma)=0$, the integration behaves like $\int \frac {dx}{x}$, which is **logarithmically divergent**.
		- Proposition. $D(\gamma)=\sum_f I_f\left(2 s_f-2\right)+\sum_i V_i a_i+d L$
		  collapsed:: true
			- The first term is the momenta from the propagators.
			- The second term is the momenta from the vertices.
			  collapsed:: true
				- Note that here we assumed there's no momenta contribution if there's no derivative.
			- The third term counts the contribution from the integration measure.
			  collapsed:: true
				- Each independent loop gives rise to a free momentum to be integrated over.
		- ### Simplify the expression by graph theory
		  collapsed:: true
			- Proposition. For connected diagrams, $L=\sum_f I_f-\sum_i V_i+1$.
			  collapsed:: true
				- This is Euler's formula, $V-E+F=2$.
				- Note that $L=F-1$, since the face $\mathbb R^2-\gamma$ isn't a loop.
			- Proposition. $2I_f+E_f=\sum_i V_i n_{if}$
	- ## Divergence of Subdiagrams
	  collapsed:: true
		- The above counting still has a flaw:
		  collapsed:: true
		  A subdiagram can still be divergent even if $D(\gamma)<0$.
			- Example.
			  ![image.png](../assets/image_1683338439631_0.png)
		- **Nevertheless, the problem can be fixed.**
		  collapsed:: true
			- In the above example:
			  We have a counterterm $\delta_m$ for the divergent subdiagram, thus we can use the following diagram to cancel the divergence:
			  ![image.png](../assets/image_1683338589549_0.png)
			- More generally, we can always divide the diagram to find the divergent subdiagram with $D(\eta) \geq 0$
			  collapsed:: true
				- Theorem (Weinberg). A diagram is convergent iff all subdiagrams $\eta$ satisfy $D(\eta)<0$.
				  collapsed:: true
					- This ensures we can always find $\eta$ if there's divergence in the whole diagram.
	- ## Divergence of multi-loop diagrams
	  collapsed:: true
		- Example in $\phi^4$ theory
		  collapsed:: true
			- ![image.png](../assets/image_1683338760672_0.png)
			- Compute by dimensional regularization: 
			  $$
			  \Gamma=\lambda^2 \times\left\{\rho^2[\cdots]-m^2\left[\frac{a}{\varepsilon^2}+\frac{2 a}{\varepsilon} \ln \frac{\mu^2}{p^2}+\frac{b}{\varepsilon}+\text { finite }\right]\right\}
			  $$
			- **Problem**
			  collapsed:: true
				- It's impossible to cancel the divergence by $\delta_m$ or $\delta\lambda$, since they cannot produce the desired momentum-dependence of $\ln (p^2)$
			- **Solution?**
			  collapsed:: true
				- We can also construct loop diagrams from the counterterms!
				- This diagram would produce the desired divergence-cancelling:
				  ![image.png](../assets/image_1683338935892_0.png)
	- Theorem.
	  collapsed:: true
	  $$\begin{aligned}
	  D(\gamma ) & = d-\sum _{f} E_{f}\left(\frac{d}{2} -1+s_{f}\right) -\sum _{i} V_{i} \Delta _{i}\\
	   & \text{ with } \Delta _{i} \equiv d-a_{i} -\sum _{f} n_{if}\left(\frac{d}{2} -1+s_{f}\right)
	  \end{aligned}$$
		- This can be proven by plugging in the above propositions.
		- But its meaning is quite deep. 
		  collapsed:: true
		  If $D(\gamma)$ decreases with the number of external lines and vertices, as the theorem suggests, then we only have **finite** diagrams with $D(\gamma) \geq 0$.
			- Example. Scalar field theory:
			- $$\begin{array}{ c c c }
			   \begin{array}{l}
			  Corresponding\\
			  Parameters
			  \end{array} &  \begin{array}{l}
			  Green\\
			  Functions
			  \end{array} &  \begin{array}{l}
			  Maximal\\
			  value\ of\ D( \gamma )
			  \end{array}\\
			  \delta m^{2} ,\ \ Z & \phi \phi  & 2\\
			  \delta _{\lambda _{3}} & \phi \phi \phi  & 1\\
			  \delta _{\lambda _{4}} & \phi \phi \phi \phi  & 0
			  \end{array}$$
			- All higher-order diagrams have $D(\gamma)<0$!
		- Proposition. For an interaction vertex of type $i$, $[g_i]=\Delta_i$ #card
		  id:: 64584d97-557f-41f3-84d3-5a851bb4c2c9
		  card-last-interval:: 30
		  card-repeats:: 1
		  card-ease-factor:: 2.6
		  card-next-schedule:: 2023-06-12T01:04:17.678Z
		  card-last-reviewed:: 2023-05-13T01:04:17.678Z
		  card-last-score:: 5
		  collapsed:: true
			- Starting points
			  collapsed:: true
				- $S=\int d^dx \mathcal L$ is dimensionless.
				- $$G_F(k):=\int d^dx e^{-ikx} \langle \phi_f(x) \phi_f(0) \rangle \sim \frac 1 {(k^2)^{1-s_f}}$$
	-
	- ## The Renormalizability Theorem
	  collapsed:: true
		- Definition. Renormalizable #card
		  collapsed:: true
			- All physical quantities can be rendered finite by a reparameterization of fields, masses and couplings.
			- An interaction is **super-renormalizable** if $\Delta_i >0$.
		- Theorem. Conditions for renormalizability:
		  collapsed:: true
		  (a) $\Delta_i \geqslant 0$ for all vertices
		  (b) $\mathcal{L}$ contains all vertices compatible with the symmetries of the (regularized) theory. (The regularization may break a symmetry Then it is no longer a symmetry of $\mathcal{L}$)
			- The first guarantees that we won't obtain new divergences by adding vertices (going to higher orders)
			- The second could be motivated by the following case:
			  collapsed:: true
				- Consider the double-scalar theory
				  $$
				  \mathcal{L}=\sum_{i=1,2} \frac{1}{2}\left(\partial^\mu \phi_i \partial_\mu \phi_i-m_i^2 \phi_i^2\right)-\frac{\lambda}{4 !} \phi_1^2 \phi_2^2
				  $$
				- The $\phi_1\phi_1 \to \phi_1\phi_1$ scattering:
				  ![image.png](../assets/image_1683338322322_0.png)
				- We must have a $\lambda_1 \phi_1^4$ term to cancel the divergence here! Thus we shall assume the term was present in the original Lagrangian and can be reparameterized.
- # Effective QFT
  collapsed:: true
	- Two motivations
	  collapsed:: true
		- (a) Is a non-renormalizable theory (i.e. containing some $\Delta_i<0$) completely unpredictive and useless?
		- (b) Can we integrate out some heavy degrees of freedom to obtain a simpler effective theory?
	- Example 1. A non-renormalizable theory
	  collapsed:: true
		- $$
		  \mathcal{L}=\frac{1}{2}\left(\partial^\mu \phi \partial_\mu \phi-m^2 \phi^2\right)-\frac{\lambda_4}{4 !} \phi^4-\frac{\lambda_6}{6 !} \phi^6
		  $$
		- $[\lambda_6]=-2$, which means $\Delta_6=-2$ by the [theorem](((64584d97-557f-41f3-84d3-5a851bb4c2c9))). Thus the theory is non-renormalizable, i.e. we'd need infinite counter terms to cancel the divergences.
		- However, if we consider a scattering process with all momenta (including the internal ones!) is smaller than some energy scale $E$, then the theory may still make sense.
		  collapsed:: true
			- Equivalent to a cutoff!
		- Specifically, the higher the power of the interaction, the more it is suppressed, thus we may ignore interactions higher than a certain power..
	- Example 2. Integrate out the heavy d.o.f.
	  collapsed:: true
		- collapsed:: true
		  $$
		  \mathcal{L}=\partial_\mu \phi^{\dagger} \partial^\mu \phi-m^2 \phi^{\dagger} \phi+\frac{1}{2} \partial_\mu \rho \partial^\mu \rho-\frac{1}{2} M^2 \rho^2-\frac{k_3}{3 !} \rho^3-g \rho \phi^{\dagger} \phi
		  $$
			- Note that it is **super-renormalizable**.
		- Now consider some process where $p_i,p_j,m \ll M$, i.e. The $\rho$ particle is very heavy.
			- Thought: The $\rho$ particles cannot be produced, only act as internal lines.
			  we can find an effective Lagrangian $\mathcal L_{eff}$ s.t.
			  $$T_{\beta \alpha }\big |_{ computed\ with\ \mathcal{L}} =T_{\beta \alpha }\big |_{ computed\ with\ \mathcal{L}_{eff}} +o((\frac{E}{M})^a)$$
			-
			- The process of determining the coupling constant is called **matching**.
				- The idea is comparing the scattering processes of the effective theory and the original theory.
				  By requiring that the amplitudes are identical, we can fix the effective coupling constants.
				- $\phi^4$ term:
				  ![image.png](../assets/image_1683509553855_0.png){:height 314, :width 869}
				- $\phi^6$ term:
				  ![image.png](../assets/image_1683509575362_0.png){:height 347, :width 712}
				- And so on and so on.
			-
			-
			-
- # [[Renormalization Group]]
- # Thoughts
  collapsed:: true
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
  collapsed:: true
	- $\phi \phi \to \phi \phi$ at 1-loop for $\phi^4$ theory
	  collapsed:: true
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
		  card-last-interval:: 32.57
		  card-repeats:: 1
		  card-ease-factor:: 2.6
		  card-next-schedule:: 2023-06-06T01:52:08.575Z
		  card-last-reviewed:: 2023-05-04T12:52:08.576Z
		  card-last-score:: 5
		  collapsed:: true
			- Idea: We can measure $\lambda$ at some reference scattering process (e.g. at the shreshold, i.e. $s=4m^2,u=t=0$).
			  Then we can compare different momenta to **cancel the divergence**.
				- In other words, experimental data could also be a valuable input -- to fix a 'reference' not available from first principles! #[[Thoughts/Math and Physics]]
				- This works since the UV divergence arises from the loop momenta and is independent of external momenta.
			- Specifically:
				- The effective coupling $\lambda$ at the threshold satisfies
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
	- Renormalization of [[QED]]
		- Setup
			- $$\begin{aligned}
			  & A_0^\mu(x)=\sqrt{Z_3} A^\mu(x), \quad \psi_0(x)=\sqrt{Z_2} \psi(x) \\
			  & e_0=Z_e e , \zeta_0=Z_\zeta \zeta , m_0=Z_m m 
			  \end{aligned}$$