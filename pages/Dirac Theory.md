- # Setup and Definitions
	- Gamma matrices
	  collapsed:: true
		- Defs
		  collapsed:: true
			- ((6379ca4e-553b-460f-89c6-0fbde5c7f0d9))
			- ((6379ca39-4ba2-4254-9131-88e223be6a0c))
				- ((6379caaa-1758-4942-a553-19b721e4a1c2))
		- Commutation relations (including those with $\gamma^5$)  #card
		  card-last-score:: 5
		  card-repeats:: 3
		  card-next-schedule:: 2023-04-06T04:55:38.292Z
		  card-last-interval:: 67.2
		  card-ease-factor:: 2.8
		  card-last-reviewed:: 2023-01-29T00:55:38.292Z
			- ((6379ca88-2a1b-4068-a7f7-0cb7197d696c))
			- ((6379ca9b-6830-497a-b6bc-0aaec1f62441))
		- Trace Tricks
			- Central trick: Compare anticommutation to cyclic permutation ((636a0bbd-c463-4b27-9bdf-29f7e78ed455))
			- ((636a0b9a-df35-40b3-9e91-9c2560aa064f))
			- Conclusion: ((636a0c10-4b26-4d64-ab89-433cccab88a3))
			- More properties
				- ((636a0c8b-0a46-4264-934f-cd22e44ec60e))
				- ((636a0c90-f02b-443d-859f-94f734dd5990))
				  Reversing order
				- Contraction identities
				  id:: 637c8c74-1534-4627-bdd0-c5cf7f409a67
					- ((636a0c99-3ccf-426e-a1fb-95d1deaf677e))
				- Easily proven by anticommutation and symmetry of $g_{\mu\nu}$
		- Gordon identity
		  id:: 637c7efe-edc6-41a0-8de5-02abe2f76eb1
			- ((637c7f07-18ee-4d3d-bdc4-3bde16d6d924))
		- $\not p u(p)=m \cdot u(p)$ and $\bar{u}\left(p^{\prime}\right) \not p^{\prime}=\bar{u}\left(p^{\prime}\right) \cdot m$
			- This is just Dirac equation.
			-
		- Basic properties
			- Adjoint
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
	- Spin sums
		- ((636a4d10-45b5-432b-b4c2-a66dfdcfd93a))
	- Normalization
		- Ref. Peskin P48
		- $$
		  \bar{v}^r(p) v^s(p)=-2 m \delta^{r s} \quad \text { or } \quad v^{r \dagger}(p) v^s(p)=+2 E_{\mathbf{p}} \delta^{r s}
		  $$
		- $$
		  \bar{u}^r(p) v^s(p)=\bar{v}^r(p) u^s(p)=0
		  $$