- Overall scheme #card
  card-last-interval:: 24
  card-repeats:: 2
  card-ease-factor:: 2.7
  card-next-schedule:: 2023-02-25T03:52:34.749Z
  card-last-reviewed:: 2023-02-01T03:52:34.750Z
  card-last-score:: 5
	- Write out the vertex function and analyze the possible ingredients by some general principles.
		- Lorentz invariance, Ward identity, possible quantities
	- A brief ((637cbf81-c429-40c1-ac36-c05a0c2b58c8)) in Peskin
- The loops leads to [[Ultraviolet Divergence]] and [[Infrared Divergence]].
- The vertex function
	- ((637c7ca7-9ad3-4bef-91c6-02723922d5e0))
	- Denoted as $-i e \Gamma^\mu\left(p^{\prime}, p\right)$
- General analysis of the vertex function
  collapsed:: true
	- First of all, the only possible recipes are $p,p',\gamma^\mu,m,e,$ pure numbers.
	- [[Lorentz covariance]] forces $\Gamma^\mu=\gamma^\mu \cdot A+\left(p^{\prime \mu}+p^\mu\right) \cdot B+\left(p^{\prime \mu}-p^\mu\right) \cdot C$
		- ((637c7d9c-c89f-4466-83ff-7e89c733ef8b))
		- Moreover, the only possible nontrivial scalar is $p^\mu p'_\mu$, since $p^2=m^2$
	- [[Ward identity]]
		- $(p^\mu-p'^\mu)\Gamma_\mu=0$
			- Apply for the virtual photon.
			- $q^\mu=p^\mu-p'^\mu$
		- Obviously this forces $C=0$
	- $q_\mu \gamma^\mu$ vanishes when sandwiched between $\bar{u}\left(p^{\prime}\right)$ and $u(p)$ #card
	  card-last-interval:: 67.2
	  card-repeats:: 3
	  card-ease-factor:: 2.8
	  card-next-schedule:: 2023-05-19T16:15:48.941Z
	  card-last-reviewed:: 2023-03-13T12:15:48.941Z
	  card-last-score:: 5
		- Proof
			- $q_\mu=p_\mu-p'_\mu$
			- The rest is invoking Dirac equation.
		- Some terms are always zero when calculating amplitudes.
	- ((637c7efe-edc6-41a0-8de5-02abe2f76eb1))
	  collapsed:: true
		- Thus we can express a linear combination of $\gamma^\mu$ and $p^\mu+p'^\mu$ by $\gamma^\mu$ and $\sigma^{\mu\nu}q_\nu$
		-
	- Final result of the vertex function #card
	  card-last-interval:: 24
	  card-repeats:: 2
	  card-ease-factor:: 2.7
	  card-next-schedule:: 2023-02-03T23:47:12.223Z
	  card-last-reviewed:: 2023-01-10T23:47:12.225Z
	  card-last-score:: 5
		- ((637c7f9b-ad14-479b-abec-cbcd8300bf7f))
	-
	-
- Evaluation of the vertex function
  collapsed:: true
	- Notation. ((637c8bcc-7c8a-4541-9ea3-0955c3bc1cc2))
	- By the Feynman rules, the expression for the correction is ((637c8bd8-d9ef-481c-a08a-3ec965b618a4))
	  collapsed:: true
		- The definition of $\Gamma^\mu$ contains $-ie$, so the one of the inner vertex is cancelled.
		- The second line uses the third ((637c8c74-1534-4627-bdd0-c5cf7f409a67))
		- Why the gamma matrices in the last term $2 m\left(k+k^{\prime}\right)^\mu$ disappear? #Inbox/Problem
		  id:: 63c14165-99e3-4b5f-ae75-f1c13f66ef2e
	- Apply the trick of [[Feynman parameter]] to 6.38
	  collapsed:: true
		- Show the reference again ((637c8bd8-d9ef-481c-a08a-3ec965b618a4))
		- ((637c9f2a-2b53-4a3e-a235-c66a85253329))
		  collapsed:: true
			- The denominator is $D=\ell^2-\Delta+i \epsilon$, where $\ell \equiv k+y q-z p$, $\Delta \equiv-x y q^2+(1-z)^2 m^2$
		-
		- The numerator shall be expressed by $\ell$ and p.
		- The expressions can be simplified by the symmetry of the integration
		  collapsed:: true
			- ((637c9fce-166f-48b1-b4c1-d30e725f0b4c))
			  collapsed:: true
				- The first vanishes, because $\ell$ and $-\ell$ have equal weights.
				- The second can also be seen from symmetry. The factor can also be easily obtained.
	- By some regrouping, we arrive at ((637ca07a-4f49-4ee5-b3da-b7cd50150fa7))
	  collapsed:: true
		- This corresponds to ((637c7f9b-ad14-479b-abec-cbcd8300bf7f))
	- We can evaluate the integral by [[Wick rotation]]
	  collapsed:: true
		- ((637cbac0-aa10-4074-9829-429c036ea575))
		- Results
		  collapsed:: true
			- ((637cbae1-e476-44b1-b8fa-f17eea4c3dbb))
			- ((637cbaec-83a0-4693-8150-80cd0de2e40a))
			  collapsed:: true
				- This is problematic for m=3, which is precisely our situation.
				  **We need to fix it.**
	- $F_2$ has neither UV or IR divergence. Thus ((637cbe69-069f-425b-b517-7959ec93212d))
	  collapsed:: true
		- This gives the correction of ((637c804b-50a9-466d-b43a-e89fdce7ac75)) at $\frac\alpha{2\pi}$
		-
	- On the other hand, $F_1$ has both UV and IR. So we need some magic to fix the problems.
	  collapsed:: true
		- [[Pauli-Villars Regularization]] to fix UV
		  collapsed:: true
			- Problem: The integration of $\ell^2$ terms diverge for m=3.
			- Replace the photon propagator ((637cbbb3-04ff-4a2e-81be-c3f54ca16692))
			  collapsed:: true
				- $\Lambda$ is a very large mass, corresponding to an infinitely heavy photon.
				- When k becomes very large, the second term cancels the first term, thus avoiding divergence.
			- In terms with the heavy photon:
			  collapsed:: true
				- ((637cbc71-4997-4022-b049-6a0c72527a7e))
				  collapsed:: true
					- The numerator algebra is unchanged.
			- Thus the integral ((637cbaec-83a0-4693-8150-80cd0de2e40a)) is replaced by ((637cbce6-b55c-4e4b-a472-3f10a0915751))
		- Intermediate result: ((637cbf4e-c94b-4357-8ff5-7bd50ba89e50))
		  collapsed:: true
			- Brutal way to interpret the parameter: Since we know ad hoc that $F_1(0)=1$, ((637cc029-8dee-4ce9-b39f-62204db82286)) Where the subtracted term is the 'correction' to $F_1(0)$
		- Introduce a small photon mass to fix IR
		  collapsed:: true
			- Problem: $F_1$ diverges at ((638da965-b083-46b4-ab32-2b53a57c236f)).
			- With a mass $\mu$, the denominator of the photon propagator becomes $(k-p)^2-\mu^2$
- Intermediate result of $F_1$
  collapsed:: true
	- $$
	  \begin{aligned}
	  F_1\left(q^2\right)=1 & +\frac{\alpha}{2 \pi} \int_0^1 d x d y d z \delta(x+y+z-1) \\
	  & \times\left[\log \left(\frac{m^2(1-z)^2}{m^2(1-z)^2-q^2 x y}\right)+\frac{m^2\left(1-4 z+z^2\right)+q^2(1-x)(1-y)}{m^2(1-z)^2-q^2 x y+\mu^2 z}\right. \\
	  & \left.\quad-\frac{m^2\left(1-4 z+z^2\right)}{m^2(1-z)^2+\mu^2 z}\right]+\mathcal{O}\left(\alpha^2\right)
	  \end{aligned}
	  $$
- Deal with the IR in $F_1$
  id:: f148e065-772b-439d-8fb3-cb4024bdd0d6
	- Note that we just show that IR can be fixed. We don't make a precise calculation of $F_1$. The full calculation can be found in Schwartz.
	-
	- We only deal with the divergent part here, where we can set $z=1,x=y=0$.
	  collapsed:: true
		- $F_1^{(divergent)}\left(q^2\right)=\frac{\alpha}{2 \pi} \int_0^1 d z \int_0^{1-z} d y\left[\frac{-2 m^2+q^2}{m^2(1-z)^2-q^2 y(1-z-y)+\mu^2}-\frac{-2 m^2}{m^2(1-z)^2+\mu^2}\right]$
		- Change variables $y=(1-z) \xi, \quad w=(1-z)$, we obtain 
		  $F_1(q^2)=\frac{\alpha}{4 \pi} \int_0^1 d \xi\left[\frac{-2 m^2+q^2}{m^2-q^2 \xi(1-\xi)} \log \left(\frac{m^2-q^2 \xi(1-\xi)}{\mu^2}\right)+2 \log \left(\frac{m^2}{\mu^2}\right)\right]$
	- Thus the divergent part is $-\frac{\alpha}{2 \pi} f_{\mathrm{IR}}\left(q^2\right) \log \left(\frac{-q^2 \text { or } m^2}{\mu^2}\right)$
	  collapsed:: true
		- $f_{\mathrm{IR}}\left(q^2\right)=\int_0^1\left(\frac{m^2-q^2 / 2}{m^2-q^2 \xi(1-\xi)}\right) d \xi-1$
	- The effect on the cross section
	  collapsed:: true
		- Since $F_1$ multiplies $\gamma^\mu$ in the matrix element, the contribution is the divergent part multiplies the tree-level cross section.
		  collapsed:: true
			- See ((638d5442-3687-4c97-90bc-528034d71a30))
		- ($\frac{d \sigma}{d \Omega})^{(divergent)}\simeq\left(\frac{d \sigma}{d \Omega}\right)_0 \cdot\left[-\frac{\alpha}{\pi} f_{\mathrm{IR}}\left(q^2\right) \log \left(\frac{-q^2 \text { or } m^2}{\mu^2}\right)+\mathcal{O}\left(\alpha^2\right)\right]$
		- In the ((638dfd14-b08e-4238-a2fb-adc882a365a1)) $-q^2 \gg m^2$
		  collapsed:: true
			- $$\begin{aligned} \int_0^1 d \xi \frac{-q^2 / 2}{-q^2 \xi(1-\xi)+m^2} & \simeq \frac{1}{2} \int_0 d \xi \frac{-q^2}{-q^2 \xi+m^2}+\left(\begin{array}{c}\text { equal contribution } \\ \text { from } \xi \approx 1\end{array}\right) \\ & =\log \left(\frac{-q^2}{m^2}\right)\end{aligned}$$
			- $F_1\left(-q^2 \rightarrow \infty\right)=1-\frac{\alpha}{2 \pi} \log \left(\frac{-q^2}{m^2}\right) \log \left(\frac{-q^2}{\mu^2}\right)$
		-