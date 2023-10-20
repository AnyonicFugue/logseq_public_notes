- Main result. For a 'regular' equation
  $$
  \frac{\mathrm{d}}{\mathrm{d} x}\left[p(x) \frac{\mathrm{d} y}{\mathrm{~d} x}\right]+q(x) y=-\lambda w(x) y
  $$
  on a finite interval $[a,b]$, we have a complete solution of real eigenvalues.
	- Regular
		- the coefficient functions $p, q, w$ and the derivative $p^{\prime}$ are all continuous on $[a, b]$;
		- $p(x)>0$ and $w(x)>0$ for all $x \in[a, b]$;
		- the problem has separated boundary conditions of the form:
		  $$
		  \begin{array}{ll}
		  \alpha_1 y(a)+\alpha_2 y^{\prime}(a)=0 & \alpha_1, \alpha_2 \text { not both } 0 \\
		  \beta_1 y(b)+\beta_2 y^{\prime}(b)=0 & \beta_1, \beta_2 \operatorname{not} \text { both } 0
		  \end{array}
		  $$
	- The eigenvalues $\lambda_1, \lambda_2, \ldots$ are real and can be numbered so that
	  $$
	  \lambda_1<\lambda_2<\cdots<\lambda_n<\cdots \rightarrow \infty
	  $$
	- Corresponding to each eigenvalue $\lambda_n$ is a unique (up to constant multiple) eigenfunction $y_n=y_n(x)$ with exactly $n-1$ zeros in $[a, b]$, called the $n$th fundamental solution.
	- The normalized eigenfunctions $y_n$ form an orthonormal basis under the $w$-weighted inner product in the Hilbert space $L^2([a, b], w(x) \mathrm{d} x)$; that is,
	  $$
	  \left\langle y_n, y_m\right\rangle=\int_a^b y_n(x) y_m(x) w(x) \mathrm{d} x=\delta_{n m},
	  $$
	  where $\delta_{n m}$ is the Kronecker delta.
-