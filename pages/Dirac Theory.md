- # Setup and Definitions
	- Gamma matrices
		- Defs
		  collapsed:: true
			- ((64687320-d1b2-4af7-bd0c-7242ecddab2d)) Weyl Representation
			  $$
			  \gamma^0=\left(\begin{array}{cc}
			  0 & 1 \\
			  1 & 0
			  \end{array}\right) ; \quad \gamma^i=\left(\begin{array}{cc}
			  0 & \sigma^i \\
			  -\sigma^i & 0
			  \end{array}\right)
			  $$
			- ((646872fb-ea96-4092-b8b8-cbd9fdb677ac))
			  $$
			  \gamma^5 \equiv i \gamma^0 \gamma^1 \gamma^2 \gamma^3=-\frac{i}{4 !} \epsilon^{\mu \nu \rho \sigma} \gamma_\mu \gamma_\nu \gamma_\rho \gamma_\sigma
			  $$
				- $$
				  \gamma^5=\left(\begin{array}{cc}
				  -1 & 0 \\
				  0 & 1
				  \end{array}\right)
				  $$
				- Note that the $i$ in the front is necessary to ensure $(\gamma^5)^2=1$, since $(\gamma^i)^2 \neq 1$.
		- Commutation relations (including those with $\gamma^5$)  #card
		  card-last-score:: 5
		  card-repeats:: 4
		  card-next-schedule:: 2024-01-20T08:00:13.197Z
		  card-last-interval:: 252.3
		  card-ease-factor:: 2.9
		  card-last-reviewed:: 2023-05-13T01:00:13.197Z
		  collapsed:: true
			- $$\begin{equation}
			  \left\{\gamma^\mu, \gamma^\nu\right\} \equiv \gamma^\mu \gamma^\nu+\gamma^\nu \gamma^\mu=2 g^{\mu \nu} \times \mathbf{1}_{n \times n}
			  \end{equation}$$
			- $$
			  \left\{\gamma^5, \gamma^\mu\right\}=0
			  $$
		- Trace Tricks
		  collapsed:: true
			- Central trick: Compare anticommutation to cyclic permutation.
			- ((636a0b9a-df35-40b3-9e91-9c2560aa064f))
			- Conclusion: ((64687282-d09a-42fa-a78e-4760d81a8691))
			  \begin{aligned}
			  \operatorname{tr}(\mathbf{1}) & =4 \\
			  \operatorname{tr}\left(\text { any odd \# of } \gamma^{\prime} \mathrm{s}\right) & =0 \\
			  \operatorname{tr}\left(\gamma^\mu \gamma^\nu\right) & =4 g^{\mu \nu} \\
			  \operatorname{tr}\left(\gamma^\mu \gamma^\nu \gamma^\rho \gamma^\sigma\right) & =4\left(g^{\mu \nu} g^{\rho \sigma}-g^{\mu \rho} g^{\nu \sigma}+g^{\mu \sigma} g^{\nu \rho}\right) \\
			  \operatorname{tr}\left(\gamma^5\right) & =0 \\
			  \operatorname{tr}\left(\gamma^\mu \gamma^\nu \gamma^5\right) & =0 \\
			  \operatorname{tr}\left(\gamma^\mu \gamma^\nu \gamma^\rho \gamma^\sigma \gamma^5\right) & =-4 i \epsilon^{\mu \nu \rho \sigma}
			  \end{aligned}
			- More properties
				- ((636a0c8b-0a46-4264-934f-cd22e44ec60e))
				- ((636a0c90-f02b-443d-859f-94f734dd5990))
				  Reversing order
				- Contraction identities
				  id:: 637c8c74-1534-4627-bdd0-c5cf7f409a67
				  collapsed:: true
					- ((636a0c99-3ccf-426e-a1fb-95d1deaf677e))
				- Easily proven by anticommutation and symmetry of $g_{\mu\nu}$
		- Gordon identity
		  id:: 637c7efe-edc6-41a0-8de5-02abe2f76eb1
		  collapsed:: true
			- ((637c7f07-18ee-4d3d-bdc4-3bde16d6d924))
		- $\not p u(p)=m \cdot u(p)$ and $\bar{u}\left(p^{\prime}\right) \not p^{\prime}=\bar{u}\left(p^{\prime}\right) \cdot m$
		  collapsed:: true
			- This is just Dirac equation.
			-
		- Basic properties
		  collapsed:: true
			- Adjoint
			  collapsed:: true
				- $\gamma^0 \gamma^\mu \gamma^0=\left(\gamma^\mu\right)^{\dagger}$
			-
		-
	- u and v
	  collapsed:: true
		- ((636af6f3-6995-4fda-bf09-03a50b003b20))
		  ((636af708-6711-4e17-84ba-4140af6f67b4))
		- ((636af73d-e54f-4317-a2e4-f57d5c26e3f5))
		  ((636af72c-0e40-427d-ad62-609da8b78213))
		-
	- Quantization
		- $$
		  \begin{aligned}
		  & \psi(x)=\int \frac{d^3 p}{(2 \pi)^3} \frac{1}{\sqrt{2 E_{\mathbf{p}}}} \sum_s\left(a_{\mathbf{p}}^s u^s(p) e^{-i p \cdot x}+b_{\mathbf{p}}^{s \dagger} v^s(p) e^{i p \cdot x}\right) \\
		  & \bar{\psi}(x)=\int \frac{d^3 p}{(2 \pi)^3} \frac{1}{\sqrt{2 E_{\mathbf{p}}}} \sum_s\left(b_{\mathbf{p}}^s \bar{v}^s(p) e^{-i p \cdot x}+a_{\mathbf{p}}^{s \dagger} \bar{u}^s(p) e^{i p \cdot x}\right)
		  \end{aligned}
		  $$
- # Lorentz Transformations and Spins
	- Transformation Law
		- $\Lambda_{\frac{1}{2}}=\exp \left(-\frac{i}{2} \omega_{\mu \nu} S^{\mu \nu}\right)$
		- $S^{i j}=\frac{i}{4}\left[\gamma^i, \gamma^j\right]=\frac{1}{2} \epsilon^{i j k}\left(\begin{array}{cc}\sigma^k & 0 \\ 0 & \sigma^k\end{array}\right) \equiv \frac{1}{2} \epsilon^{i j k} \Sigma^k$
- Dirac equation
  id:: 6385f0a2-e52f-444e-b94f-41d91b3b69c4
	- $(i\gamma^\mu\partial_\mu -m) \psi=0$
		- Plane wave: $(\not p-m)\psi=0$
- Spin identities
  collapsed:: true
	- Spin sum
		- ((636a4d10-45b5-432b-b4c2-a66dfdcfd93a))
	- Normalization
		- Ref. Peskin P48
		- $$
		  \bar{v}^r(p) v^s(p)=-2 m \delta^{r s} \quad \text { or } \quad v^{r \dagger}(p) v^s(p)=+2 E_{\mathbf{p}} \delta^{r s}
		  $$
		- $$
		  \bar{u}^r(p) v^s(p)=\bar{v}^r(p) u^s(p)=0
		  $$