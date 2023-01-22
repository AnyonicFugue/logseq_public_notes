- [[References]]
	- ![2007_Grillet_Abstract algebra.pdf](file://C:/Users/10309/Nutstore/1/sync/zotero/Mathematics/Abstract Algebra/2007_Grillet_Abstract algebra.pdf)
- [[Luroth Theorem]]
	- Let $K$ be a field and $M$ be an intermediate field between $K$ and $K(X)$, for some indeterminate $X$. Then there exists a rational function $f(X) \in K(X)$ such that $M=K(f(X))$.
		- $K(X)$ is a transcendental extension.
		- In other words, every intermediate extension between $K$ and $K(X)$ is a simple extension.
- [[Field]]
	- Resultant and Discriminant
		- [[Resultant]] of two polynomials
			- Def
				- $f(X)=a_m\left(X-\alpha_1\right) \cdots\left(X-\alpha_m\right), g(X)=b_n(X-\beta_1)...(X-\beta_n)$
				- $$\begin{aligned} \operatorname{Res}(f, g) & =a_m^n b_n^m \prod_{i, j}\left(\alpha_i-\beta_j\right) \\ & =a_m^n \prod_i g\left(\alpha_i\right)=(-1)^{m n} b_n^m \prod_j f\left(\beta_j\right)\end{aligned}$$
			- ((63c0a684-6cd0-4449-bb38-4278a8f304b2)) If $K$ is a field and $f, g \in K[X]$, then $\operatorname{Res}(f, g)=0$ if and only if $f$ and $g$ have a common root in $\bar{K}$.
		- [[Discriminant]] of a polynomial
			- Def
				- Let $f(X)=a_n\left(X-\alpha_1\right) \cdots\left(X-\alpha_n\right)$ be a polynomial of degree $n \geqq 1$ with coefficients in a field $K$ and not necessarily distinct roots $\alpha_1, \ldots, \alpha_n$ in $\bar{K}$. The discriminant of $f$ is
				  $$
				  \operatorname{Dis}(f)=a_n^{2 n-2} \Pi_{1 \leqq i<j \leqq n}\left(\alpha_i-\alpha_j\right)^2 .
				  $$
			- ((63c0a6c5-915b-4040-bad6-53634a83f21e)) Let $K$ be a field. A nonconstant polynomial $f \in K[X]$ is separable over $K$ if and only if $\operatorname{Dis}(f) \neq 0$.
		- Let $K$ be a field. If $f \in K[X]$ has degree $n \geqq 2$ and leading coefficient $a_n$, then $\operatorname{Res}\left(f, f^{\prime}\right)=(-1)^{n(n-1) / 2} a_n \operatorname{Dis}(f)$.
- [[Galois Theory]]
-