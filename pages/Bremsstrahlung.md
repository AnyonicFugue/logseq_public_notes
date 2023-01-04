- ((638c4d2d-93bd-48eb-a06d-f3ee129fa405))
  collapsed:: true
	- Scheme
		- Write down the current $j^\mu(x)=e \int d \tau \frac{d y^\mu(\tau)}{d \tau} \delta^{(4)}(x-y(\tau))$
		- Solve Maxwell's equation $\tilde{A}^\mu(k)=-\frac{1}{k^2} \tilde{j}^\mu(k)$ in Fourier space, than go back to position space. #Trick
		- Calculate the energy radiated.
	- Result
		- Number of photons $=\frac{\alpha}{\pi} \int_0^{k_{\max }} d k \frac{1}{k} \mathcal{I}\left(\mathbf{v}, \mathbf{v}^{\prime}\right)$
- Note that he models the scattering process as an infinitely fast change of momentum.
- Quantum calculation
  collapsed:: true
	- Summary #card
	  card-last-interval:: 16
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2023-01-01T05:48:20.136Z
	  card-last-reviewed:: 2022-12-16T05:48:20.138Z
	  card-last-score:: 5
		- Two diagrams ((638c4eb7-7eef-4a64-b904-5757a3634520))
			- Note that an on-shell electron can't still be on-shell after emitting a photon. Fortunately the internal electrons can be off-shell.
		- Calculate the amplitude (until divergences pop up)
			- Write down the amplitude by the Feynman rules: $\begin{aligned} i \mathcal{M}=-i e \bar{u}\left(p^{\prime}\right) & \left(\mathcal{M}_0\left(p^{\prime}, p-k\right) \frac{i(\not p-\not k+m)}{(p-k)^2-m^2} \gamma^\mu \epsilon_\mu^*(k)\right. \\ & \left.+\gamma^\mu \epsilon_\mu^*(k) \frac{i\left(\not p^{\prime}+\not k +m\right)}{\left(p^{\prime}+k\right)^2-m^2} \mathcal{M}_0\left(p^{\prime}+k, p\right)\right) u(p)\end{aligned}$
				- No integrations here.
			- Very soft photon -> Approximate $M_0$ independent of k; ignore k in the numerators
				- $i \mathcal{M}=\bar{u}\left(p^{\prime}\right)\left[\mathcal{M}_0\left(p^{\prime}, p\right)\right] u(p) \cdot\left[e\left(\frac{p^{\prime} \cdot \epsilon^*}{p^{\prime} \cdot k}-\frac{p \cdot \epsilon^*}{p \cdot k}\right)\right]$.
				   The Brems part can be separated.
			- As shown in HW6, $2 f_{\mathrm{IR}}\left(q^2\right)=I\left(\beta, \beta^{\prime}\right)$
				- $d \sigma\left[e^{-}(p) \rightarrow e^{-}\left(p^{\prime}\right)+\gamma\right]=d \sigma_0\left[e^{-}(p) \rightarrow e^{-}\left(p^{\prime}\right)\right] \times \frac{\alpha}{\pi} I\left(\beta, \beta^{\prime}\right) \times \frac{d E_\gamma}{E_\gamma}$
				- $I\left(\beta, \beta^{\prime}\right)=\int \frac{d \Omega_k}{4 \pi}|\boldsymbol{k}|^2\left[\frac{2 p \cdot p^{\prime}}{(k \cdot p)\left(k \cdot p^{\prime}\right)}-\frac{m^2}{(k \cdot p)^2}-\frac{m^2}{\left(k \cdot p^{\prime}\right)^2}\right]$
		- Regularize the divergence
			- Pretend that the photon has a small mass $\mu$. Then the integration has a lower limit.
			- Obtain Sudakov double log when $-q^2 \to \infty$.
	- Simplifications
		- Soft-photon approximation
			- Assume the photon is very soft, then $\mathcal{M}_0\left(p^{\prime}, p-k\right) \approx \mathcal{M}_0\left(p^{\prime}+k, p\right) \approx \mathcal{M}_0\left(p^{\prime}, p\right)$.
			- We can also ignore k in the numerators.
		- Dirac equation
		- $p^2=m^2, k^2=0$
	- Intermediate result
		- $i \mathcal{M}=\bar{u}\left(p^{\prime}\right)\left[\mathcal{M}_0\left(p^{\prime}, p\right)\right] u(p) \cdot\left[e\left(\frac{p^{\prime} \cdot \epsilon^*}{p^{\prime} \cdot k}-\frac{p \cdot \epsilon^*}{p \cdot k}\right)\right]$
		- Normal scattering times a factor for photon emissions.
	- Probability and cross section, where the divergence appears.
		- Since the matrix element is the product of two parts, just integrate over the photon variable until a suitable cutoff.
		- The photon part
			- $d( prob )=\frac{d^3 k}{(2 \pi)^3} \sum_\lambda \frac{e^2}{2 k}\left|\boldsymbol{\epsilon}_\lambda \cdot\left(\frac{\mathbf{p}^{\prime}}{p^{\prime} \cdot k}-\frac{\mathbf{p}}{p \cdot k}\right)\right|^2$
			- Total probability $\approx \frac{\alpha}{\pi} \int_0^{|\mathbf{q}|} d k \frac{1}{k} \mathcal{I}\left(\mathbf{v}, \mathbf{v}^{\prime}\right)$
				- Where q is the cutoff.
		- **It diverges near q=0!!!** This is the [[IR]] divergence.
	- Dealing with the divergence in Bremsstrahlung
	  id:: 74b31acc-246f-48b4-99c9-63059f858425
		- ((638d646a-e830-409c-b369-6a78f7f92674))
			- The divergent part becomes
			  $$\begin{aligned}
			  d \sigma\left(p \rightarrow p^{\prime}+\gamma(k)\right) & =d \sigma\left(p \rightarrow p^{\prime}\right) \cdot \frac{\alpha}{2 \pi} \log \left(\frac{-q^2}{\mu^2}\right) \mathcal{I}\left(\mathbf{v}, \mathbf{v}^{\prime}\right) \\
			  &  \underset{-q^2 \rightarrow \infty}{\approx} d \sigma\left(p \rightarrow p^{\prime}\right) \cdot \frac{\alpha}{\pi} \log \left(\frac{-q^2}{\mu^2}\right) \log \left(\frac{-q^2}{m^2}\right)
			  \end{aligned}$$
			- Note that we only calculated under the limit $-q^2 \rightarrow \infty$ to obtain the [[Sudakov Double Logarithms]].
		-
		-
-