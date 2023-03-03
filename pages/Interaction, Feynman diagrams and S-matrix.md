- # Setup and Definitions
  collapsed:: true
	- Incoming and outgoing states
		- $\begin{aligned} & \left.\left.\mid\left\{p_i\right\}(t) \text { in }\right\rangle_I=U(t,-\infty) \mid\left\{p_i\right\} \text { in }\right\rangle_H \\ & \left.\left.\mid\left\{p_i\right\}(t) \text { out }\right\rangle_I=U(t,+\infty) \mid\left\{p_i\right\} \text { out }\right\rangle_H\end{aligned}$
		- Completeness relation
			- $\sum |\{p_i\}in\rangle\langle\{p_i\}in|=\sum |\{p_i\}in\rangle\langle\{p_i\}in|=\mathbb 1$
			- Note that this assumption is modified when [[Bound States]] are present.
	-
	- Mandelstam variables
	  collapsed:: true
		- ((636af081-5d67-4758-887c-ba004b190b71))
		- ((637b326c-0792-4cf0-b2e5-d861201c971c))
		-
- Gell-Mann-Low formula #card
  collapsed:: true
	- $$\langle\Omega|T\{\phi(x) \phi(y)\}| \Omega\rangle=\lim _{T \rightarrow \infty(1-i e)} \frac{\left\langle 0\left|T\left\{\phi_I(x) \phi_I(y) \exp \left[-i \int_{-T}^T d t H_I(t)\right]\right\}\right| 0\right\rangle}{\left\langle 0\left|T\left\{\exp \left[-i \int_{-T}^T d t H_I(t)\right]\right\}\right| 0\right\rangle}$$
	- Notes
		- The fields in $V_I$ are free fields since they evolve according to the free Hamiltonian
		- [[Haag's Theorem]] actually forbids the interaction picture for relativistic QFT.
			- Actually this is a notoriously difficult mathematical problem to construct interacting QFT satisfying the [[Wightman Axioms]].
			-
- # Källén-Lehmann Spectral  Representation
  collapsed:: true
	- Peskin ((639094ce-9088-4138-a4b5-7ac7f96f7d15))
	- Thought
		- Insert a completeness relation into the middle of $\langle\Omega|T \phi(x) \phi(y)| \Omega\rangle$.
	- ## Key points
		- ### Assumptions in Use
		  collapsed:: true
			- ((63fc166f-9a06-42b7-a7e3-947eff93ae12))
			- ((63fc5025-5650-4054-ba3a-0520194bfb13))
		- ### Completeness relations
			- For a free theory we only need to consider the 1p part.
			- 1-p
				- $$
				  (\mathbf{1})_{1-\text { particlc }}=\int \frac{d^3 p}{(2 \pi)^3} \frac{1}{2 E_{\mathbf{p}}}|\mathbf{p}\rangle\langle\mathbf{p}|
				  $$
				- In other words, zero-momentum state is unique for 1-particle.
			- For an **interacting** theory, multi-particle states could also be created by the field operator.
			- General
				- id:: 63973120-efca-48be-9b42-55cc35b82675
				  $$
				  \mathbf{1}=|\Omega\rangle\langle\Omega|+\sum_\lambda \int \frac{d^3 p}{(2 \pi)^3} \frac{1}{2 E_{\mathbf{p}}(\lambda)}| \lambda_{\mathbf{p}}\rangle\left\langle\lambda_{\mathbf{p}}\right|
				  $$
				- $\lambda$ denotes the distinct Lorentz sections. States within a section could be related to each other by boosts.
				- Since the spectrum is a continuum, the sum should actually be an integration.
		- Insert the relation
			- $$\langle\Omega|\phi(x) \phi(y\rangle| \Omega\rangle=\sum_\lambda \int \frac{d^3 p}{(2 \pi)^3} \frac{1}{2 E_{\mathbf{p}}(\lambda)}\left\langle\Omega|\phi(x)| \lambda_{\mathbf{p}}\right\rangle\left\langle\lambda_{\mathbf{p}}|\phi(y)| \Omega\right\rangle$$
				- The vacuum diagonal element is zero.
			- $\begin{aligned}\left\langle\Omega^{\prime} |\phi(x) |\lambda_{\mathbf{p}}\right\rangle & =\left\langle\Omega\left|e^{i P \cdot x} \phi(0) e^{-i P \cdot x}\right| \lambda_{\mathbf{p}}\right\rangle \\ & =\left.\left\langle\Omega|\phi(0)| \lambda_{\mathbf{p}}\right\rangle e^{-i p \cdot x}\right|_{p^0=E_{\mathbf{p}}} \\ & =\left.\left\langle\Omega|\phi(0)| \lambda_0\right\rangle e^{-i p \cdot x}\right|_{p^0=E_{\mathbf{p}}}\end{aligned}$
				- 1st line: Just a change of basis. P is the generator of translations.
				- 2nd: Extract the eigenvalues
				- 3rd: ((63996ae9-da3c-4b64-94cd-0250fbb3555f)).
					- The field operator, the vacuum and the inner product are invariant under boosts.
					- Thus only $|\lambda_{\mathbf{p}}\rangle$ would be boosted. Moreover we can boost it to $p=0$.
		- Introduce an integration over p to obtain the heaviside function, $\langle\Omega|\phi(x) \phi(y)| \Omega\rangle=\sum_\lambda \int \frac{d^4 p}{(2 \pi)^4} \frac{i}{p^2-m_\lambda^2+i \epsilon} e^{-i p \cdot(x-y)}\left|\left\langle\Omega|\phi(0)| \lambda_0\right\rangle\right|^2$
			- Familiar form! A propagator multiplied by a weight (spectral density).
	- ## Form of the representation #card
		- $$\langle\Omega|T \phi(x) \phi(y)| \Omega\rangle=\int_0^{\infty} \frac{d M^2}{2 \pi} \rho\left(M^2\right) D_F\left(x-y ; M^2\right)$$
			- $\rho\left(M^2\right)$ is called the **spectral density**.
				- A delta function at $M^2=m^2$ (physical mass, not bare mass), a continuum for $M^2 \gtrsim 4m^2$
			- Intuitively, the 2-point correlation function can be decomposed into contributions of different effective masses.
	- ## Relation to the Propagator #card
		- We perform a Fourier transformation to see the thing more clearly in the momentum space.
			- $$\begin{aligned} & \int d^4 x e^{i p \cdot x}\langle\Omega|T \phi(x) \phi(0)| \Omega\rangle=\int_0^{\infty} \frac{d M^2}{2 \pi} \rho\left(M^2\right) \frac{i}{p^2-M^2+i \epsilon} \\ &= \frac{i Z}{p^2-m^2+i \epsilon}+\int_{\sim 4 m^2}^{\infty} \frac{d M^2}{2 \pi} \rho\left(M^2\right) \frac{i}{p^2-M^2+i \epsilon}\end{aligned}$$
				- Familiar Feynman propagator!
		- ((63904004-1719-49a0-a4ed-ae545a9d3ac2)), but with field-strength renormalizations.
		- ### 1-particle part
			- $\rho\left(M^2\right)=2 \pi \delta\left(M^2-m^2\right) \cdot Z+\left(\right.$ nothing else until $\left.M^2 \gtrsim(2 m)^2\right)$
			- Z is the field-strength renormalization.
				- Note that $Z=1$ in free theory, but $Z<1$ in interacting theories.
				- $\left|\left\langle\Omega|\phi(0)| 1_0\right\rangle\right|^2=Z<1$. Physically, the field operator creates a bunch of different states, so the amplitude of $1_0$ is smaller than 1.
				-
			- m here is ((63903e92-e09c-4f19-8a07-012214461679))
			- $m_0$ in the Lagrangian is the ((63903ea6-2939-4f43-9d05-c658b31ce1ae))
		- ((63904079-1b0a-4901-9470-1714586e2e26))
		- ((6390416f-d1e2-4be7-a6dc-5ca7e71d8cd4))ds. We just need to modify the transformation rules under Lorentz transformations.
		  collapsed:: true
			- Dirac field ((63904193-3f90-4077-a320-ee734d2a3f38))
		-
	-
- # [[Feynman rules]]
	- Feynman rules for fermions
		- Generalize TOP and normal-ordering
		- Generalized Wick's [TODO]
- # Topics
	- A fundamental difficulty: We need the states to be asymptotic in the **interaction theory**. However, we only knows how to create **free** plane waves.
	  collapsed:: true
		- ((63675402-6c64-443b-b71c-90c3a99a4842))
		- For the vacuum we use ((636753ab-e737-4f19-a1d8-e33ab15c71fc)), which used the property that the vacuum has the lowest energy.
		- Not so good for general states.
	- [[Helicity]] structure in scattering
	  collapsed:: true
		- High-E limit #card
		  card-last-interval:: 24
		  card-repeats:: 2
		  card-ease-factor:: 2.46
		  card-next-schedule:: 2023-03-13T00:58:19.808Z
		  card-last-reviewed:: 2023-02-17T00:58:19.809Z
		  card-last-score:: 5
			- All fermions can be regarded as massless.
			- For $\xi=\left(\begin{array}{l}1 \\ 0\end{array}\right)$, ((6379c82e-aa21-424e-9d43-339a251a9bc2))
				- And the same for spin down.
				- Note $p^3$ is $p^z$. The formula can be verified directly by #TODO
			- ((6379cf92-7252-44e9-b63d-ce792967a710))
				- Note that it is different for fermions and anti-fermions.
			- In other words, now [[Helicity]] and [[Chirality]] becomes identical.
		- Contribution of different helicities
			- Idea: Use the projectors $\frac{1\pm\gamma^5}{2}$ to get certain helicities.
			- ((6379d13b-9ca8-4786-9cf5-265e23751503))
				- $\gamma^5$ anticommutes with any single $\gamma^\mu$
				- LHS determines the helicity of u, while RHS determines v.
			- Proceed by the common process to obtain $|M|^2$ and $\frac{d \sigma}{d \Omega}$, we can obtain all contributions of the different combinations.
				- Exercise: what are the possible combinations for $e^{+} e^{-} \rightarrow \mu^{+} \mu^-$? #card
				  card-last-interval:: 169.81
				  card-repeats:: 4
				  card-ease-factor:: 2.66
				  card-next-schedule:: 2023-08-14T20:14:10.930Z
				  card-last-reviewed:: 2023-02-26T01:14:10.931Z
				  card-last-score:: 5
					- Input and output can be $(++),(--)$ respectively.
					- 4 in total.
	- Crossing symmetry
	  collapsed:: true
		- He claims to easily relate 
		  $e^{+} e^{-} \rightarrow \mu^{+} \mu^{-}$ and $e^{-} \mu^{-} \rightarrow e^{-} \mu^{-}$
		  by a substitution of variable ((6379d42d-2944-458f-9110-e369a7bb0a42))
			- Both of them only have one diagram, with a photon propagator in the middle.
			- The kinetics are similar.
	- [[LSZ Formula]]
	- Properties of the [[S-matrix]]
		- [[Lorentz invariance]]
		- Unitarity
			- [[Optical Theorem]]