alias:: QED

- [[Quantization]] of EM field
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
  collapsed:: true
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
- Radiative Corrections
	- [[Loop-diagrams]]
		- Overall scheme #card
			- Write out the vertex function and analyze the possible ingredients by some general principles.
			- A brief ((637cbf81-c429-40c1-ac36-c05a0c2b58c8)) in Peskin
		- The loops leads to [[Ultraviolet Divergence]] and [[Infrared Divergence]].
		- The vertex function
			- ((637c7ca7-9ad3-4bef-91c6-02723922d5e0))
			- Denoted as $-i e \Gamma^\mu\left(p^{\prime}, p\right)$
		- General analysis of the vertex function
		  collapsed:: true
			- First of all, the only possible recipes are $p,p',\gamma^\mu,m,e,$ pure numbers.
			- [[Lorentz covariance]]
			  collapsed:: true
				- Forcing ((637c7d3f-7675-407b-85c7-0f9398e74aa0))
					- ((637c7d9c-c89f-4466-83ff-7e89c733ef8b))
				- Moreover, the only possible nontrivial scalar is $p^\mu p'_\mu$, since $p^2=m^2$
			- [[Ward identity]]
				- $(p^\mu-p'^\mu)\Gamma_\mu=0$
				- Obviously this forces $C=0$
				- ((637c7e07-4519-4a7f-825d-65eb89a46046)) #card
					- [[Ward identity]] actually applies to the S-matrix element, not to the vertex function. So everything can be traced back to the [[S-matrix]].
			- ((637c7efe-edc6-41a0-8de5-02abe2f76eb1))
				- Thus we can express a linear combination of $\gamma^\mu$ and $p^\mu+p'^\mu$ by $\gamma^\mu$ and $\sigma^{\mu\nu}q_\nu$
				-
			- Final result of the vertex function #card
				- ((637c7f9b-ad14-479b-abec-cbcd8300bf7f))
			-
			-
		- Evaluation of the vertex function
			- Notation. ((637c8bcc-7c8a-4541-9ea3-0955c3bc1cc2))
			- By the Feynman rules, the expression for the correction is ((637c8bd8-d9ef-481c-a08a-3ec965b618a4))
				- The definition of $\Gamma^\mu$ contains $-ie$, so the one of the inner vertex is cancelled.
				- The second line uses the third ((637c8c74-1534-4627-bdd0-c5cf7f409a67))
				- Why the gamma matrices in the last term $2 m\left(k+k^{\prime}\right)^\mu$ disappear? #Problem
			- Feynman parameters #Trick
			  collapsed:: true
				- Idea: {{cloze Introduce auxiliary parameters to simplify the expression, then change the order of integration.}}
					- The trick is usually followed by changing the order of integrations and shifting integration variables (To complete the square).
					- So there's the inherent problem: Can we really exchange the order of integration? #Thoughts
						- Similar problems abound. For example, lots of things don't converge absolutely.
				- ((637c9a80-85fe-4e5c-bc14-36cd4b691001))
				- ((637c9a87-b8af-4b42-ac19-a8b8c3edb007)) #card
					- Proof. Differentiate the first identity
				- ((637c9aa2-ba77-453f-8139-1e1a97735c0c)) #card
					- The proof is to be completed.
			- Apply the trick of Feynman parameters to 6.38
				- Show the reference again ((637c8bd8-d9ef-481c-a08a-3ec965b618a4))
				- ((637c9f2a-2b53-4a3e-a235-c66a85253329))
					- The denominator is $D=\ell^2-\Delta+i \epsilon$, where $\ell \equiv k+y q-z p$, $\Delta \equiv-x y q^2+(1-z)^2 m^2$
				-
				- The numerator shall be expressed by $\ell$ and p.
				- The expressions can be simplified by the symmetry of the integration
					- ((637c9fce-166f-48b1-b4c1-d30e725f0b4c))
						- The first vanishes, because $\ell$ and $-\ell$ have equal weights.
						- The second can also be seen from symmetry. The factor can also be easily obtained.
			- By some regrouping, we arrive at ((637ca07a-4f49-4ee5-b3da-b7cd50150fa7))
				- This corresponds to ((637c7f9b-ad14-479b-abec-cbcd8300bf7f))
			- We can evaluate the integral by [[Wick rotation]]
				- ((637cbac0-aa10-4074-9829-429c036ea575))
				- Results
					- ((637cbae1-e476-44b1-b8fa-f17eea4c3dbb))
					- ((637cbaec-83a0-4693-8150-80cd0de2e40a))
						- This is problematic for m=3, which is precisely our situation.
						  **We need to fix it.**
			- $F_2$ has neither UV or IR divergence. Thus ((637cbe69-069f-425b-b517-7959ec93212d))
				- This gives the correction of ((637c804b-50a9-466d-b43a-e89fdce7ac75)) at $\frac\alpha{2\pi}$
				-
			- On the other hand, $F_1$ has both UV and IR. So we need some magic to fix the problems.
				- Pauli-Villars [[Regularization]] to fix UV
					- Problem: The integration of $\ell^2$ terms diverge for m=3.
					- Replace the photon propagator ((637cbbb3-04ff-4a2e-81be-c3f54ca16692))
						- $\Lambda$ is a very large mass, corresponding to an infinitely heavy photon.
						- When k becomes very large, the second term cancels the first term, thus avoiding divergence.
					- In terms with the heavy photon:
						- ((637cbc71-4997-4022-b049-6a0c72527a7e))
							- The numerator algebra is unchanged.
					- Thus the integral ((637cbaec-83a0-4693-8150-80cd0de2e40a)) is replaced by ((637cbce6-b55c-4e4b-a472-3f10a0915751))
				- Intermediate result: ((637cbf4e-c94b-4357-8ff5-7bd50ba89e50))
					- Brutal way to interpret the parameter: Since we know ad hoc that $F_1(0)=1$, ((637cc029-8dee-4ce9-b39f-62204db82286)) Where the subtracted term is the 'correction' to $F_1(0)$
				- Introduce a small photon mass to fix IR
					- Problem: $F_1$ diverges at $q^2=0$.
						- ((637cc1bb-4657-4d3d-bbb4-be6d6404ac3c))
						-
			-
	- [[Bremsstrahlung]]
- Obtain macroscopic results from QED
  collapsed:: true
	- Use Born's approximation to link to [[Quantum Mechanics]]
		- Add a [[Classical]] external field ((637c75c9-97e2-45d5-8b25-33c61663e7d0))
		- Lande g-factor
		  id:: 637c804b-50a9-466d-b43a-e89fdce7ac75
			- ((637c8054-2570-47cb-b075-f0dc3f8279a6))
			- The second term is the anomalous magnetic moment.
		- See Peskin P210
	-