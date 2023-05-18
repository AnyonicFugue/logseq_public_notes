- # Idea
	- Compute the Feynman diagram as an analytic function of the dimensionality of spacetime. Take $d \to 4$ in the end.
		- This seems problematic. Generally physics depends sensitively on the spacetime dimension, not to mention the strangeness of non-integer dimensions.
		- Though non-integer dimensions makes a bit sense via [[Gamma Function]] .
	- (3+1)D is very special; it incurs divergences, behaviors away from mean-field theories, etc. #Thoughts
- # Summary
	- Modify some rules
		- In $d$ dimensions, $g^{\mu \nu}$ obeys $g_{\mu \nu} g^{\mu \nu}=d$. Thus, if the numerator of a symmetric integrand contains $\ell^\mu \ell^\nu$, we should replace
		  $$
		  \ell^\mu \ell^\nu \rightarrow \frac{1}{d} \ell^2 g^{\mu \nu}
		  $$
		- Thus $(1-\frac 1 2)g^{\mu\nu} \to (1-\frac 2 D)g^{\mu\nu}$, which may fuse with $\Gamma(1-\frac 2 D)$
		-
	- $$\int \frac{d^d \ell_E}{(2 \pi)^d} \frac{1}{\left(\ell_E^2+\Delta\right)^n}=\frac{1}{(4 \pi)^{d / 2}} \frac{\Gamma\left(n-\frac{d}{2}\right)}{\Gamma(n)}\left(\frac{1}{\Delta}\right)^{n-\frac{d}{2}}$$
	- $$\int \frac{d^d \ell_E}{(2 \pi)^d} \frac{\ell_E^2}{\left(\ell_E^2+\Delta\right)^n}=\frac{1}{(4 \pi)^{d / 2}} \frac{d}{2} \frac{\Gamma\left(n-\frac{d}{2}-1\right)}{\Gamma(n)}\left(\frac{1}{\Delta}\right)^{n-\frac{d}{2}-1}$$
	-
- # Example
	-