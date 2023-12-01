# Definition
	- The Pfaffian is defined for any (complex) anti-symmetric matrix.
		- **NOT** anti-hermitian!
	- $$\operatorname{pf}(A)=\frac1{2^nn!}\sum_{\sigma\in S_{2n}}\operatorname{sgn}(\sigma)\prod_{i=1}^na_{\sigma(2i-1),\sigma(2i)}$$
	- Recursive
		- $$\operatorname{pf}(A)=\sum_{\overset{j=1}{j\neq i}}^{2n}(-1)^{i+j+1+\theta(i-j)}a_{ij}\operatorname{pf}(A_{\hat{i}\hat{j}})$$
		- $\theta$ is the step function.
- # Properties
	- #+BEGIN_TIP
	  The spectral theorem for skew-symmetric matrices can be of great help.
	  #+END_TIP
	- $$\operatorname{pf}(A)^2=\det(A)$$
	- $$\operatorname{pf}(BAB^\mathrm{T})=\det(B)\operatorname{pf}(A)$$
		- B is arbitrary, not necessarily orthogonal or invertible.
	- For an $2n \times 2n$ matrix:
	  $$\begin{aligned}
	  &\operatorname{pf}(A^\mathrm{T})=(-1)^n\operatorname{pf}(A). \\
	  &\operatorname{pf}(\lambda A)=\lambda^n\operatorname{pf}(A). \\
	  &\operatorname{pf}(A)^2=\det(A).
	  \end{aligned}$$
	- Block matrices
		- $$\begin{aligned}A_1\oplus A_2&=\begin{bmatrix}A_1&0\\0&A_2\end{bmatrix},\\\operatorname{pf}(A_1\oplus A_2)&=\operatorname{pf}(A_1)\operatorname{pf}(A_2).\end{aligned}$$
	- Trace identity
		- $$\operatorname{pf}(A)\operatorname{pf}(B)=\exp(\frac12\operatorname{tr}\log(A^\mathrm{T}B))$$
-
-