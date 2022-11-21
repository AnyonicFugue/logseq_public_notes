alias:: QED

- [[Quantization]]
	- $$\begin{aligned}
	  &A_\mu(x)=\int \frac{d^3 p}{(2 \pi)^3} \frac{1}{\sqrt{2 E_p}} \sum_{\lambda=0}^3 \epsilon_\mu^\lambda(p)\left(a_p^\lambda e^{-i p \cdot x}+a_p^{\lambda \dagger} e^{i p \cdot x}\right) \\
	  &\pi_\mu(x)=\int \frac{d^3 p}{(2 \pi)^3}(+i) \sqrt{\frac{E_p}{2}} \sum_{\lambda=0}^3 \epsilon_\mu^\lambda(p)\left(a_p^\lambda e^{-i p \cdot x}-a_p^{\lambda \dagger} e^{i p \cdot x}\right)
	  \end{aligned}$$
	-
- From [[Yukawa theory]] to QED #card
  collapsed:: true
	- ((636908da-dc02-4ff9-bc45-1b3b3c4e8517))
		- So elegant! $\gamma^\mu$ marries $A_\mu$
		- Would different choice of gamma affect physics? eg. Weyl or Majarona? #Problem
	- ((636909d9-c786-4017-88e5-4c0d88ed061e))
	- See [[Feynman rules]]
- Elementary processes
  id:: 636e47fc-2b5b-48d2-abe9-e9892ac50a40
	- Fermion-fermion
		- ((636a08cd-dc0b-497c-84e8-1209396c615e))
		- ((636907ca-d056-409f-b6b2-bfb023a167a1))
		- ((63690837-39c9-4e6c-974f-7db6c09a9bc5))
			- The mass would be ignored!
		- ((63690855-079b-41b7-95c3-4e8e1dd1b950))
			- The expression isn't difficult. But to find $|\mathcal{M}|^2$, we need to **find its complex conjugation**
		- Conjugation of bi-spinor products ((636a0984-d932-4dd2-a89e-963d90acda08))
		- ((636a0a09-665c-450a-81b8-fc919bb5d8e5)). Thus we can use spin sums to simplify the expression.
			- Actually **sum** over outgoing spins and **average** over incoming spins
		- ((636a4a63-f308-41ef-96ff-d1d2aaefe3d4)) and obtain the lovely traces
		  ((636a0aa2-99ca-44c2-80cf-e497cb4a1354))((636a0ab1-74ca-4f2b-b875-c0045fad2016))
			- ((636a0ace-b81b-4ff0-8e67-0e1acf8f3264))
		- Continue to evaluate the probability
			- ((636a0d35-79e4-45a4-b9a7-7cd329e624ee))
			  ((636a0d4c-c42b-434b-bb47-95702c4eef39))
				- Note $\not p$ is actually $p_\alpha \gamma^\alpha$
			- Plug the above expression in:
			  ((636a0e49-de93-4428-ae7d-ac04fa1beecb))
			- Select [[Center-of-mass]] frame:
			-
		- Final result:
		  id:: 63703fc2-9ae7-47f5-9a16-84dda6ae25bc
			- ((636a0ea3-dbd5-40f4-bf1b-0fe2940a0762))
			  With ((636a0eb0-2a64-48c7-89eb-ee8b61d66889))
	- Note: The 'phase-space dependence' originates from ((636a108d-1c99-463c-bd06-6105cdf58bbd)), where we don't care about the momenta of the particles coming out, only direction.
	- [[Compton scattering]]
		- Key points #card
			- Draw **two** diagrams
			- Simplifications
				- Use some basic relations ((6379e1d5-cde6-45c1-9024-4b12b6a35650)) to simplify the denominator
				- Use ((6379e3b6-ac3e-4770-a535-ccfaeb1e3f28)) to simplify the numerator.
			- Perform spin sums
		- Two diagrams
			- ((6379d890-1f5b-4f30-9855-5dbd1a1b68be))
				- Can we have antifermions in the inner line? #card
					- NO. The contractions with external fermions enforce this.
		- Invoking the Feynman rules, we can write down the total M matrix 
		  $i \mathcal{M}=\bar{u}\left(p^{\prime}\right)\left(-i e \gamma^\mu\right) \epsilon_\mu^*\left(k^{\prime}\right) \frac{i(\not p+\not k+m)}{(p+k)^2-m^2}\left(-i e \gamma^\nu\right) \epsilon_\nu(k) u(p)$
		  $+\bar{u}\left(p^{\prime}\right)\left(-i e \gamma^\nu\right) \epsilon_\nu(k) \frac{i\left(\not p-\not k^{\prime}+m\right)}{\left(p-k^{\prime}\right)^2-m^2}\left(-i e \gamma^\mu\right) \epsilon_\mu^*\left(k^{\prime}\right) u(p)\\=-i e^2 \epsilon_\mu^*\left(k^{\prime}\right) \epsilon_\nu(k) \bar{u}\left(p^{\prime}\right)\left[\frac{\gamma^\mu(\not p+\not k+m) \gamma^\nu}{(p+k)^2-m^2}+\frac{\gamma^\nu\left(\not p-\not k^{\prime}+m\right) \gamma^\mu}{\left(p-k^{\prime}\right)^2-m^2}\right] u(p)$
		- Simplifications
			- ((6379e1d5-cde6-45c1-9024-4b12b6a35650)) To simplify the denominators
			- ((6379e3b6-ac3e-4770-a535-ccfaeb1e3f28)) to simplify the numerators.
				- The last equality can be proven by the spin sums.
		- ((6379e410-066b-4ee4-a4e2-ac831ae0bcbf))
		- Now we need to sum the polarizations over the photons and the electrons.
			- The sum for the spins is familiar.
			- The trick for photons #card
				- ((6379e47e-61a5-4599-985f-889017c30915))
				- This isn't an actual equality, but it works in calculating the scatterings.
				- Proof
					- ((637ae38e-ce30-44e7-a6b9-67dec4cec7ed))
					- $\sum_\epsilon\left|\epsilon_\mu^*(k) \mathcal{M}^\mu(k)\right|^2=\sum_\epsilon \epsilon_\mu^* \epsilon_\nu \mathcal{M}^\mu(k) \mathcal{M}^{\nu *}(k)$
					- Select k in z direction for simplicity  $\epsilon_1^\mu=(0,1,0,0) ; \quad \epsilon_2^\mu=(0,0,1,0)$. 
					  We obtain $\sum_\epsilon\left|\epsilon_\mu^*(k) \mathcal{M}^\mu(k)\right|^2=\left|\mathcal{M}^1(k)\right|^2+\left|\mathcal{M}^2(k)\right|^2$
					- By [[Ward identity]], $\mathcal{M}^0=\mathcal{M}^3$
					- Thus ((637ae426-99ad-4d34-868f-db59435efe39))
		- The rest is just squaring M and performing the spin sums.
			- Note that you may find extra $\gamma^0$ in $(\gamma^\mu)^\dag=\gamma^0\gamma^\mu\gamma^0$
			- The extra gammas are absorbed in $\bar u(p)=u^\dag(p)\gamma^0$
			-
		- Final result
			- ((637ae60f-71b1-4bbd-bfba-96333ac6ecc9))