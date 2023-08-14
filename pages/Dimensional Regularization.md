- # Idea
	- Compute the Feynman diagram as an analytic function of the dimensionality of spacetime. Take $d \to 4$ in the end.
		- This seems problematic. Generally physics depends sensitively on the spacetime dimension, not to mention the strangeness of non-integer dimensions.
		- Though non-integer dimensions makes a bit sense via [[Gamma Function]] .
	- (3+1)D is very special; it incurs divergences, behaviors away from mean-field theories, etc. #Observations
- # Summary
	- $$\int \frac{d^4 k_E}{(2 \pi)^4} \longrightarrow \tilde{\mu}^{4-d} \int \frac{d^d k_E}{(2 \pi)^d} \quad \text { with } \tilde{\mu} \equiv \mu \sqrt{\frac{e^{\gamma_E}}{4 \pi}}$$
		- $\tilde \mu$ is introduced to keep the mass dimension.
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
- # Examples
	- $$\begin{align*}
	  I_{1} \equiv  & \int \frac{d^{4} k'}{( 2\pi )^{4}}\frac{1}{\left\{k^{\prime 2} -\Delta \right\}^{2}}\\
	  \rightarrow  & i\tilde{\mu }^{4-d}\int \frac{d^{d} k'_{E}}{( 2\pi )^{d}}\frac{1}{\left\{k'{_{E}}^{2} +\Delta \right\}^{2}}\\
	  = & i\tilde{\mu }^{\varepsilon }\frac{1}{(4\pi )^{d/2}}\frac{\Gamma \left( n-\frac{d}{2}\right)}{\Gamma (n)}\left(\frac{1}{\Delta }\right)^{n-\frac{d}{2}}\\
	  = & \frac{2i}{(4\pi )^{2}}\left(\frac{1}{\varepsilon } +\ln \Delta +\ln \mu \right)
	  \end{align*}$$
	- $$\begin{align*}
	  I_{2} \equiv  & \int \frac{d^{4} k'}{( 2\pi )^{4}}\frac{k^{\prime 2}}{\left\{k^{\prime 2} -\Delta \right\}^{2}}\\
	  \rightarrow  & -i\tilde{\mu }^{4-d}\int \frac{d^{d} k'_{E}}{( 2\pi )^{d}}\frac{k'{_{E}}^{2}}{\left\{k'{_{E}}^{2} +\Delta \right\}^{2}}\\
	  = & -i\tilde{\mu }^{\varepsilon }\frac{1}{(4\pi )^{d/2}}\frac{d}{2}\frac{\Gamma \left( n-\frac{d}{2} -1\right)}{\Gamma (n)}\left(\frac{1}{\Delta }\right)^{n-\frac{d}{2} -1}\\
	  = & \frac{4i}{(4\pi )^{2}}\left(\frac{1}{\varepsilon } +\ln \mu +\ln \Delta \right) \Delta 
	  \end{align*}$$