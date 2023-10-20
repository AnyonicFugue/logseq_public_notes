# Legendre Polynomial
id:: 652a397b-1db6-479e-a8ae-d1bead690b94
	- Equivalent definitions
		- In this approach, the polynomials are defined as an orthogonal system with respect to the weight function $w(x)=1$ over the interval $[-1,1]$.
			- That is, $P_n(x)$ is a polynomial of degree $n$, such that
			  $$
			  \int_{-1}^1 P_m(x) P_n(x) d x=0 \quad \text { if } n \neq m
			  $$
		- $$
		  \left(1-x^2\right) P_n^{\prime \prime}(x)-2 x P_n^{\prime}(x)+n(n+1) P_n(x)=0
		  $$
		- $$
		  P_n(x)=\frac{1}{2^n n !} \frac{d^n}{d x^n}\left(x^2-1\right)^n
		  $$
	- Orthogonality
		- $$
		  \int_{-1}^1 P_m(x) P_n(x) d x=\frac{2}{2 n+1} \delta_{m n}
		  $$
	- Low orders
		- $$
		  \begin{array}{|r|r|}
		  \hline n & P_n(x) \\
		  \hline 0 & 1 \\
		  \hline 1 & x \\
		  \hline 2 & \frac{1}{2}\left(3 x^2-1\right) \\
		  \hline 3 & \frac{1}{2}\left(5 x^3-3 x\right) \\
		  \hline 4 & \frac{1}{8}\left(35 x^4-30 x^2+3\right)
		  \end{array}
		  $$